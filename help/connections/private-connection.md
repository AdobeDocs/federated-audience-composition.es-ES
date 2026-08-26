---
title: Conectarse a la composición de audiencia federada mediante una conexión privada
description: Obtenga información sobre cómo configurar y conectarse a Federated Audience Composition mediante una conexión privada. Esto incluye PrivateLink o una VPN de sitio a sitio.
source-git-commit: c4096e842caf383dee2e43bc80e18e1ac2036faf
workflow-type: tm+mt
source-wordcount: '1634'
ht-degree: 0%

---


# Conectividad privada con Federated Audience Composition

La Composición de audiencias federada admite conexiones privadas con varias bases de datos. Las conexiones privadas le permiten conectarse a almacenes de datos alojados por el cliente sin necesidad de atravesar la red pública de Internet.

## Bases de datos compatibles {#supported-databases}

Las siguientes bases de datos admiten la conectividad privada con Federated Audience Composition:

| Base de datos | Nube | Tipo de conexión privada |
| -------- | ----- | ----------------------- |
| [!DNL Snowflake] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (extremo de la interfaz de VPC) |
| [!DNL Snowflake] | [!DNL Microsoft Azure] | Azure PrivateLink (extremo privado) |
| [!DNL Amazon Redshift] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (extremo de VPC administrado) |
| [!DNL Databricks] | [!DNL Amazon Web Services] (AWS) | AWS PrivateLink (extremo de la interfaz de VPC) |
| [!DNL Databricks] | [!DNL Microsoft Azure] | VPN de sitio a sitio |
| [!DNL Databricks] | [!DNL Google Cloud Platform] (GCP) | VPN de sitio a sitio |
| [!DNL Azure Synapse Analytics] | [!DNL Microsoft Azure] | VPN de sitio a sitio |
| [!DNL Google BigQuery] | [!DNL Google Cloud Platform] (GCP) | VPN de sitio a sitio |

## Snowflake {#snowflake}

>[!AVAILABILITY]
>
>Para usar la conectividad privada con [!DNL Snowflake], **debe** estar al menos en el nivel crítico para la empresa o superior en [!DNL Snowflake]. Para obtener más información sobre la conectividad privada con [!DNL Snowflake], lea la [guía de conectividad privada en la documentación de Snowflake](https://docs.snowflake.com/en/user-guide/private-connectivity-inbound).

El uso de la conectividad privada con [!DNL Snowflake] depende del proveedor de la nube en el que se encuentre la instancia [!DNL Snowflake].

### Amazon Web Service (AWS) {#snowflake-aws}

>[!IMPORTANT]
>
>Antes de continuar, asegúrese de obtener su ID de cuenta de AWS del Servicio de atención al cliente de Adobe. Una vez que obtenga el identificador de su cuenta de AWS, comuníquese con la atención al cliente de [!DNL Snowflake] para que [!DNL Snowflake] pueda autorizar el uso de PrivateLink en su cuenta de AWS.

Una vez que se haya autorizado el uso de su cuenta de AWS con [!DNL Snowflake], deberá obtener valores, incluidos `privatelink-vpce-id`, `privatelink-account-url` y `privatelink_ocsp-url`, para poder obtener el extremo de la interfaz de VPC.

Puede obtener estos valores ejecutando los siguientes comandos en su cuenta de [!DNL Snowflake] como ACCOUNTADMIN:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Una vez ejecutados estos comandos, puede enviar la salida SQL completa al Servicio de atención al cliente de Adobe para que Adobe pueda crear el punto final de la interfaz de VPC.

Para obtener información más detallada sobre cómo crear una conexión PrivateLink con AWS, lea la [guía de AWS PrivateLink](https://docs.snowflake.com/en/user-guide/admin-security-privatelink).

Si desea autorizar el vínculo privado para utilizarlo con un entorno de ensayo interno, póngase en contacto con el servicio de atención al cliente de Adobe para habilitar el entorno.

Para obtener información más detallada sobre cómo crear una conexión PrivateLink con AWS para entornos de ensayo internos, lea la [guía de extremos de la interfaz de VPC de AWS para etapas internas](https://docs.snowflake.com/en/user-guide/private-internal-stages-aws).

### Microsoft Azure {#snowflake-azure}

Para Microsoft Azure, necesitará obtener valores que incluyan `privatelink-pls-id`, `privatelink-account-url` y `privatelink_ocsp-url` para crear el extremo privado de Azure.

Puede obtener estos valores ejecutando los siguientes comandos en su cuenta de Snowflake:

`SELECT SYSTEM$GET_PRIVATELINK_CONFIG();`
`SELECT SYSTEM$ALLOWLIST_PRIVATELINK();`

Una vez ejecutados estos comandos, puede enviar la salida SQL completa al Servicio de atención al cliente de Adobe para que Adobe pueda crear el extremo privado de Azure.

Una vez que Adobe cree el extremo privado de Azure, podrá obtener su ID de recurso de extremo privado. Ahora que tiene el id. de recurso de extremo privado, póngase en contacto con el soporte técnico de [!DNL Snowflake] para autorizar su cuenta de [!DNL Snowflake] y, al mismo tiempo, proporcionar el id. de recurso.

Para obtener información más detallada sobre cómo crear una conexión PrivateLink con Azure, lea la [guía de Azure PrivateLink](https://docs.snowflake.com/en/user-guide/privatelink-azure).

Si desea autorizar el uso de PrivateLink con un entorno de ensayo interno, ejecute el siguiente comando en [!DNL Snowflake], a la vez que proporcione el ID de recurso de ensayo interno que proporciona el Servicio de atención al cliente de Adobe:

`SELECT SYSTEM$AUTHORIZE_STAGE_PRIVATELINK_ACCESS('<internal-stage-private-endpoint-resource-id>');`

Para obtener información más detallada sobre cómo crear una conexión PrivateLink con Azure para entornos de ensayo internos, lea la [guía de extremos privados de Azure para etapas internas](https://docs.snowflake.com/en/user-guide/private-internal-stages-azure).

## Amazon Redshift {#amazon-redshift}

Tanto los clústeres aprovisionados como Redshift Server admiten conexiones privadas con Federated Audience Composition.

>[!IMPORTANT]
>
>Antes de empezar, póngase en contacto con el Servicio de atención al cliente de Adobe para recibir su ID de cuenta de Amazon Web Service (AWS) y su ID de nube privada virtual (VPC). Necesitará **ambos** de estos valores para obtener acceso al extremo entre cuentas. Para obtener información más detallada sobre la concesión de acceso a VPC, lea la [guía sobre la concesión de acceso a VPC](https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-cross-vpc-console-grantor.html).

Una vez que tenga los ID de AWS y de VPC, vaya a AWS Management Console para conceder acceso entre cuentas a un extremo de VPC administrado.

Para un clúster aprovisionado, tenga en cuenta los valores **Identificador de clúster Redshift** y **Identificador de cuenta AWS del propietario del clúster**. Para un Redshift sin servidor, anote los valores de **nombre de grupo de trabajo** y **ID de cuenta de AWS** de propietario.

Después de obtener estos valores, comparta estos detalles con el Servicio de atención al cliente de Adobe para que Adobe pueda crear el punto final de VPC administrado. A continuación, Adobe compartirá los siguientes detalles de conexión con usted: **URL del extremo Redshift**, **URL Redshift JDBC** y **URL Redshift ODBC**.

## Databricks {#databricks}

>[!AVAILABILITY]
>
>Para usar la conectividad privada con Databricks, **debe** estar en un plan Enterprise en Databricks. Para obtener más información sobre la conectividad privada con Databricks, lea la [guía de conceptos de vínculos privados](https://docs.databricks.com/aws/en/security/network/concepts/privatelink-concepts).

El uso de la conectividad privada con Databricks depende del proveedor de la nube en el que se encuentre la instancia de Databricks.

### Amazon Web Service {#databricks-aws}

Antes de configurar con Amazon Web Service, póngase en contacto con el Servicio de atención al cliente de Adobe para que puedan crear un extremo de interfaz de VPC front-end (entrante) que apunte a Databricks. Este extremo cubre la conectividad ODBC de Federated Audience Composition con su espacio de trabajo de Databricks.

Una vez que haya obtenido su ID de extremo de VPC y la región de AWS del Servicio de atención al cliente de Adobe, deberá registrar su extremo de VPC con la información proporcionada por Adobe.

Después de registrar el extremo de VPC, deberá crear un objeto de configuración de acceso privado (PAS). Cuando cree el extremo, establezca el **Nivel de acceso privado** en un nivel de **extremo** y seleccione el extremo de VPC creado anteriormente. Para obtener más información sobre cómo crear opciones de acceso privado, lea la [guía de configuración de PrivateLink de entrada](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-3-create-private-access-settings).

Después de configurar los ajustes de acceso privado, puede adjuntar el extremo de VPC al espacio de trabajo. Para obtener más información sobre cómo crear tu espacio de trabajo con PrivateLink, lee la [guía de configuración de PrivateLink](https://docs.databricks.com/aws/en/security/network/front-end/front-end-private-connect#step-4-create-your-workspace-with-private-link-objects).

Ahora que se han configurado todos los ajustes, puede compartir la URL del espacio de trabajo de Databricks con el Servicio de atención al cliente de Adobe. Una vez que haya compartido la URL del espacio de trabajo de Databricks, Adobe puede establecer la configuración de DNS necesaria para enrutar solicitudes al extremo del espacio de trabajo.

### Microsoft Azure {#databricks-azure}

Se utiliza una VPN de sitio a sitio para conectarse de forma segura desde Adobe al espacio de trabajo de Databricks en Azure. Deberá configurar una puerta de enlace VPN de Azure para establecer el túnel VPN y transmitir sus datos a Adobe de forma segura.

Una vez configurada la puerta de enlace VPN de Azure y el extremo privado Databricks, comparta los siguientes detalles con su representante del Servicio de atención al cliente de Adobe: **Puerta de enlace de red virtual de Azure**, **IP de extremo privado Databricks**, **URL de Workspace Databricks** y **Número de sistema autónomo (ASN)**.

Con estos detalles, Adobe puede establecer los túneles VPN necesarios para su conexión. Después de establecer los túneles VPN, Adobe proporciona las **direcciones IP públicas y privadas del túnel VPN**, **claves previamente compartidas** y **número de sistema autónomo**.

Ahora puede configurar sus túneles VPN en su puerta de enlace de red virtual de Azure. Para obtener más información, lea [conectar AWS y Azure mediante una guía de puerta de enlace VPN](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

### Google Cloud Platform {#databricks-gcp}

Se utiliza una VPN de sitio a sitio para conectarse de forma segura desde Adobe al espacio de trabajo de Databricks en Google Cloud Platform. Debe configurar una puerta de enlace VPN de alta disponibilidad de Google Cloud Platform y un enrutador de la nube para establecer el túnel VPN y transmitir sus datos a Adobe de forma segura.

Una vez configurada la puerta de enlace VPN GCP HA y el enrutador de la nube, comparta los siguientes detalles con el representante del Servicio de atención al cliente de Adobe: **Puerta de enlace VPN GCP HA**, **URL de Workspace de Databricks**, **IP de Private Service Connect (PSC)** y **Número de sistema autónomo (ASN)**.

Con estos detalles, Adobe puede establecer los túneles VPN necesarios para su conexión. Después de establecer los túneles VPN, Adobe proporciona las **direcciones IP públicas y privadas del túnel VPN**, **claves previamente compartidas** y **número de sistema autónomo**.

Ahora puede configurar los túneles VPN en su cuenta de Google Cloud Platform. Para obtener más información, lea la [guía para crear conexiones VPN de alta disponibilidad](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).

## Azure Synapse Analytics {#azure-synapse}

Para conectarse con Azure Synapse Analytics, primero debe crear una puerta de enlace de red virtual de Azure y un punto de conexión privado Synapse. La puerta de enlace de red virtual de Azure le permite enviar tráfico cifrado entre una red virtual de Azure a Synapse, mientras que el punto final privado de Synapse le permite tener una conexión privada para transmitir sus datos de forma segura.

Una vez configurada la puerta de enlace de red virtual de Azure y el punto de conexión privado Synapse, comparta los siguientes detalles con el representante del Servicio de atención al cliente de Adobe: **Puerta de enlace de red virtual de Azure**, **IP de punto de conexión privado Synapse**, **URL de Synapse Workspace** y **Número de servicio autónomo (ASN)**.

Con estos detalles, Adobe puede establecer los túneles VPN necesarios para su conexión. Después de establecer los túneles VPN, Adobe proporciona los **emparejamientos VPN-Túnel**, **claves previamente compartidas** y **número de sistema autónomo**.

Ahora puede configurar sus túneles VPN en su puerta de enlace de red virtual de Azure. Para obtener más información, lea [conectar AWS y Azure mediante una guía de puerta de enlace VPN](https://learn.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-aws-bgp).

## Google Big Query {#gbq}

Para conectarse con Google Big Query, primero deberá crear una puerta de enlace VPN de alta disponibilidad de Google Cloud Platform y un enrutador de la nube.

Una vez configurada la puerta de enlace VPN GCP HA y el enrutador de la nube, comparta los siguientes detalles con el representante del Servicio de atención al cliente de Adobe: **Puerta de enlace VPN GCP HA**, **IP de Conexión de servicio privado (PSC)** y el **Número de sistema autónomo (ASN)**.

Con estos detalles, Adobe puede establecer los túneles VPN necesarios para su conexión. Después de establecer los túneles VPN, Adobe proporciona las **direcciones IP públicas y privadas del túnel VPN**, **claves previamente compartidas** y **número de sistema autónomo**.

Ahora puede configurar los túneles VPN en su cuenta de Google Cloud Platform. Para obtener más información, lea la [guía para crear conexiones VPN de alta disponibilidad](https://docs.cloud.google.com/network-connectivity/docs/vpn/tutorials/create-ha-vpn-connections-google-cloud-aws).
