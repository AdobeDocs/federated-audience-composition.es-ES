---
title: Novedades de la composición de público federado de Experience Platform
description: Últimas actualizaciones y notas de la versión
hide: true
hidefromtoc: true
exl-id: 23ea1a5d-a0e4-4f47-b0f8-56009bbc0a4a
source-git-commit: a568024516cec999e1e22b6f6deec926fe7083f8
workflow-type: tm+mt
source-wordcount: '1142'
ht-degree: 95%

---

# Notas de la versión {#rn-new}

[!DNL Federated Audience Composition] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan en estas notas de la versión. [!DNL Federated Audience Composition] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Versión de julio de 2025 {#fac-25-7}

Esta versión incorpora los siguientes cambios y mejoras:

* **Disponibilidad del conector Oracle**

  El conector Oracle ya está disponible para su uso con Federated Audience Composition.

* **Alertas de estado de composición**

  Puede suscribirse a Alertas para recibir alertas sobre el éxito y los errores de las ejecuciones de maquetación.

## Versión de junio de 2025 {#fac-25-6}

Esta versión incluye las siguientes mejoras:

* **Disponibilidad general para clientes de Adobe Healthcare Shield**

  A finales de junio, la composición de público federado estará disponible para los clientes de Adobe Healthcare Shield para la creación de públicos, enriquecimiento y casos de uso de enriquecimiento de perfiles.

* **Control de acceso a nivel de objeto**

  La composición de público federado ahora admite el control de acceso a nivel de objeto para aplicar etiquetas de acceso a las composiciones especificadas.

* **Funciones predeterminadas**

  Ahora puede utilizar una de las funciones predeterminadas para administrar los permisos de usuario para el acceso de composición de público federado.

* **Actualizaciones incrementales en casos de uso de enriquecimiento de perfiles**

  La actividad Guardar perfiles ahora admite actualizaciones incrementales. Con las actualizaciones incrementales, puede consultar y actualizar datos incrementales a la vez que enriquece los perfiles con datos de almacenes de datos externos.

## Versión de abril de 2025 {#fac-25-4}

### Mejoras {#fac-25-4-improvements}

Esta versión incorpora las mejoras que se indican a continuación.

* **Vista del lienzo del modelo de datos**

  La vista de lienzo de la sección Modelos de datos mejora la experiencia al permitir la visualización de los modelos de datos y sus vínculos en un diseño de lienzo, junto con la vista tabular existente. [Más información](../data-management/gs-models.md)

* **Asistente de IA**

  El Asistente de IA es una función de la interfaz de usuario diseñada para que pueda navegar y comprender los conceptos de Adobe y obtener datos operativos de su entorno específico. Está disponible en varios productos de Adobe Experience Cloud, incluida la composición de público federado. [Más información](../start/audiences.md)

* **Nombre del modelo de datos**

  Desde el menú Audiencias, la pestaña **Composiciones federadas** ahora muestra el nombre del modelo de datos en lugar del ID, lo que mejora la claridad y la facilidad de uso general.

* **Audiencia**

  El menú Audiencia ahora muestra el nombre o la etiqueta del modelo de datos seleccionado cuando un usuario selecciona un modelo de datos sin audiencias asociadas.

### Compatibilidad {#fac-25-4-compat}

* **Conexión segura de Snowflake**

  Con esta nueva versión, la composición de público federado admite las conexiones seguras de vínculos privados a las bases de datos de Amazon Redshift alojadas en Microsoft Azure. [Más información](../connections/federated-db.md#amazon-redshift)

## Versión de marzo de 2025 {#fac-25-3}

### Mejoras {#fac-25-3-improvements}

Esta versión incorpora las mejoras que se indican a continuación.

* **Permisos de la Composición de público federado**

  A partir de la versión de marzo, [!DNL Federated Audience Composition] empezará a aplicar el acceso de las interfaces de la **administración de datos federados** y las **composiciones federadas** al usuario al que se ha concedido el permiso de **Administrar datos federados**.

  Se recomienda a los usuarios que contacten con los administradores para que les añadan este permiso a su función y puedan seguir accediendo a la interfaz de usuario de [!DNL Federated Audience Composition].

  Para obtener información sobre cómo asignar este permiso, consulte la [documentación detallada](/help/governance-privacy-security/access-control.md).

<!--
* **Data model Canvas view**

    The Canvas view for the Data Models section improves the experience by enabling the visualization of data models and their links in a canvas layout, alongside the existing tabular view. [Learn more](../data-management/gs-models.md)

* **AI Assistant**

    AI Assistant is a user interface feature designed to help you navigate and understand Adobe concepts and get operational insights for your specific environment. It is available in several products across Adobe Experience Cloud, including Federated Audience Composition. [Learn more](ai-assistant.md)
-->


### Compatibilidad {#fac-25-3-compat}

* **Conexión de Databricks**

  Con esta nueva versión, la Composición de público federado ahora admite la conectividad de vínculos privados para las conexiones de bases de datos de Databricks.
Esto incluye conexiones seguras a bases de datos de Databricks alojadas en Amazon Web Services (AWS) a través de un vínculo privado y bases de datos de Databricks alojadas en Microsoft Azure a través de una VPN. [Más información](../connections/federated-db.md#databricks)

* **Soporte para clientes de B2B CDP**

  La Composición de público federado ya está disponible para los clientes de Business-to-Business (B2B) Customer Data Platform (CDP) para casos de uso de públicos basados en personas.

* **Conexión segura de Snowflake**

  Con esta nueva versión, la Composición de público federado admite las conexiones seguras de vínculos privados a las bases de datos de Snowflake alojadas en Microsoft Azure. [Más información](../connections/federated-db.md#snowflake)

## Versión de febrero de 2025 {#fac-25-2}

Esta versión incorpora los cambios que se enumeran a continuación.

* **Compatibilidad con Microsoft Fabric**

  Ahora puede establecer conexiones con bases de datos de Microsoft Fabric mediante la Composición de público federado. [Más información](../connections/federated-db.md)

* **Compatibilidad con Amazon Redshift Spectrum**

  Amazon Redshift Spectrum ahora es compatible con las conexiones de base de datos de Amazon Redshift. [Más información](../connections/federated-db.md#amazon-redshift)

* **Experiencia mejorada de creación de esquemas**

  El proceso de creación de esquemas se ha mejorado a través de una interfaz de usuario actualizada, diseñada para ser más intuitiva y fácil de navegar. Estas mejoras ofrecen a los profesionales de los datos una forma más fluida y eficaz de desarrollar modelos de datos. [Más información](../customer/schemas.md)

* **Compatibilidad con el enriquecimiento del público de Databricks**

  Ahora puede utilizar Databricks en el flujo Leer público, lo que habilita la actividad de las bases de datos de Databricks y permite configurarlas como un nuevo destino. [Más información](../connections/destinations.md)

## Versión de noviembre de 2024 {#fac-24-11}

### Mejoras {#fac-24-11-improvements}

Esta versión incorpora la mejora que se indica a continuación.

* **Lista de direcciones IP permitidas**

  Al añadir una base de datos federada en la interfaz de usuario de Adobe Experience Platform, ahora puede ver directamente las direcciones IP asociadas con las instancias de Composición de público federado. Esto le permite copiar y autorizar fácilmente estas IP para conectarse a la base de datos y tener mayor seguridad y flexibilidad. [Más información](../connections/connections.md)

## Versión de octubre de 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Anteriormente disponible para un conjunto de organizaciones (LA), la composición de público federado de Adobe Experience Platform ya está disponible para todos los usuarios (GA). Esta capacidad se activa en función de su oferta y solo es visible con los permisos asociados. [Más información](access-prerequisites.md)
>

### Compatibilidad {#fac-24-10-compat}

Con esta nueva versión, la composición de público federado ahora es compatible con los sistemas que se enumeran a continuación.

* **Compatibilidad con Databricks**

  Ahora puede establecer conexiones con bases de datos de Databricks mediante la composición de público federado. [Más información](../connections/federated-db.md#databricks)

* **Compatibilidad con acceso seguro a Snowflake a través de AWS PrivateLink**

  Ahora se admite el acceso seguro al almacén de datos externo de Snowflake a través de un vínculo privado. Tenga presente que la cuenta de Snowflake debe estar alojada en Amazon Web Services (AWS) y ubicada en la misma región que el entorno de composición de público federado. Póngase en contacto con su representante de Adobe para obtener ayuda sobre la configuración del acceso seguro a su cuenta de Snowflake. [Más información](../connections/federated-db.md#snowflake)

* **Compatibilidad con Amazon Redshift sin servidor**

  Con esta nueva versión, la composición de público federado admite [Amazon Redshift sin servidor](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Mejoras {#fac-24-10-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

* **Actualizar esquemas existentes**

  Cuando se crea, modifica o elimina una columna en una base de datos federada, ahora puede detectar y aplicar los cambios haciendo clic en el botón **[!UICONTROL Actualizar esquema]** del esquema correspondiente. [Más información](../customer/schemas.md#schema-refresh)

* **Asociar un modelo de datos con una nueva composición**

  Al crear una composición, ahora puede seleccionar el modelo de datos que desea asociarle. Con esta nueva opción, la configuración de las actividades es más sencilla, ya que solo están disponibles las tablas del modelo de datos asociado. [Más información](../compositions/create-composition.md)

## Versión de julio de 2024: composición de público federado (disponibilidad limitada) {#fac-la}

La Composición de público federado proporciona a las empresas un acceso flexible y ampliado a los almacenes de datos empresariales para componer públicos utilizando conjuntos de datos empresariales esenciales y potenciar las experiencias iniciadas por la marca y en el momento. Con este nuevo enfoque, como usuario de [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/home){target="_blank"} o [Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/ajo-home){target="_blank"}, puede federar los datos de audiencia directamente desde su almacén de datos existente para enriquecer las audiencias de Adobe Experience Platform en un solo sistema.

La Composición de público federado responde a la creciente demanda del mercado para las empresas que necesitan la flexibilidad de componer públicos con conjuntos de datos de almacén. Esto permite a las empresas reducir el movimiento de datos y, al mismo tiempo, poner los datos esenciales del público a disposición de los equipos de marketing para satisfacer los requisitos de los casos de uso y potenciar las experiencias personalizadas.

Obtenga más información sobre las funciones de la composición de público federado en [esta página](get-started.md) y en las [Preguntas frecuentes](faq.md).

Para obtener información detallada sobre los requisitos previos para acceder a las composiciones de público federado y las protecciones actuales, consulte [esta página](access-prerequisites.md).
