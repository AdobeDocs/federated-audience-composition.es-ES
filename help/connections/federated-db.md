---
audience: end-user
title: Introducción a las bases de datos federadas
description: Aprenda a crear y administrar sus bases de datos federadas
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 7a3d03543f6f903c3f7f66299b600807cf15de5e
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 26%

---

# Introducción a las bases de datos federadas {#federated-db}


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_menu"
>title="Bases de datos federadas"
>abstract="Las conexiones existentes a bases de datos federadas se muestran en esta pantalla. Para crear una conexión nueva, haga clic en el botón **[!UICONTROL Añadir base de datos federada]**."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_properties"
>title="Propiedades de la base de datos federada"
>abstract="Introduzca el nombre de la nueva base de datos federada y seleccione su tipo."


>[!CONTEXTUALHELP]
>id="dc_connection_federated_database_details"
>title="Detalles de la base de datos federada"
>abstract="Introduzca la configuración para conectarse a la nueva base de datos federada. Utilice el botón **[!UICONTROL Probar conexión]** para validar la configuración."

Cree, configure, pruebe y guarde la conexión con una base de datos externa.

Bases de datos externas compatibles:

* Snowflake
* Google Big Query
* Azure synapse
* Vertica Analytics
* Amazon Redshift

## Snowflake {#snowflake}

* **[!UICONTROL Servidor]**:

* **[!UICONTROL Usuario]**: Nombre del usuario.

* **[!UICONTROL Contraseña]**: Contraseña de la cuenta de usuario.

* **[!UICONTROL Base de datos]**:

* **[!UICONTROL Esquema de trabajo]**:

* **[!UICONTROL Clave privada]**:
Solo se aceptan archivos .pem

* **[!UICONTROL Opciones]**: el conector admite las opciones detalladas en la tabla siguiente.

| Opción | Descripción |
|---|---|
| esquema de trabajo | Esquema de base de datos que se va a utilizar para tablas de trabajo |
| almacén | Nombre del almacén predeterminado que se va a utilizar. Anula el valor predeterminado del usuario. |
| TimeZoneName | De forma predeterminada, vacío, lo que significa que se utiliza la zona horaria del sistema del servidor de aplicaciones de Campaign Classic. La opción se puede utilizar para forzar el parámetro de sesión TIMEZONE. <br>[Para obtener más información, consulte esta página](https://docs.snowflake.net/manuals/sql-reference/parameters.html#timezone). |
| WeekStart | Parámetro de sesión WEEK_START. De forma predeterminada, se establece en 0. <br>[Para obtener más información, consulte esta página](https://docs.snowflake.com/en/sql-reference/parameters.html#week-start). |
| UseCachedResult | Parámetro de sesión USE_CACHED_RESULTS. De forma predeterminada, se establece en TRUE. Esta opción se puede utilizar para deshabilitar los resultados en caché del Snowflake. <br>[Para obtener más información, consulte esta página](https://docs.snowflake.net/manuals/user-guide/querying-persisted-results.html). |
| bulkThreads | Número de subprocesos que se utilizarán para el cargador en bloque del Snowflake; si hay más subprocesos, se obtiene un mejor rendimiento para cargas en bloque más grandes. De forma predeterminada, se establece en 1. El número se puede ajustar en función del número de hilos de la máquina. |
| chunkSize | Determina el tamaño de archivo del fragmento del cargador en bloque. De forma predeterminada, se establece en 128 MB. Se puede modificar para obtener un rendimiento más óptimo, cuando se utiliza con bulkThreads. Los hilos más activos simultáneamente significan un mejor rendimiento. <br>Para obtener más información, consulte [Documentación del Snowflake](https://docs.snowflake.net/manuals/sql-reference/sql/put.html). |
| StageName | Nombre de la fase interna preaprovisionada. Se utilizará en la carga masiva en lugar de crear una nueva etapa temporal. |

## Google Big Query {#google-big-query}

* **[!UICONTROL Cuenta de servicio]**: Correo electrónico de su **[!UICONTROL cuenta de servicio]**. Para obtener más información, consulte [Documentación de Google Cloud](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

* **[!UICONTROL Proyecto]**: Nombre de su **[!UICONTROL Proyecto]**. Para obtener más información, consulte [Documentación de Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

* **[!UICONTROL Conjunto de datos]**: Nombre de su **[!UICONTROL Conjunto de datos]**. Para obtener más información, consulte [Documentación de Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro).

* **[!UICONTROL Ruta del archivo de claves]**: Cargue el archivo de claves en el servidor. Solo se aceptan archivos .json.

* **[!UICONTROL Opciones]**: el conector admite las opciones detalladas en la tabla siguiente.

| Opción | Descripción |
|:-:|:-:|
| ProxyType | Tipo de proxy utilizado para conectarse a BigQuery mediante conectores ODBC y SDK. </br>HTTP (predeterminado), http_no_túnel, socks4 y socks5 son compatibles actualmente. |
| ProxyHost | Nombre de host o dirección IP donde se puede contactar con el proxy. |
| ProxyPort | Número de puerto en el que se ejecuta el proxy, p. ej. 8080 |
| ProxyUid | Nombre de usuario utilizado para el proxy autenticado |
| ProxyPwd | Contraseña de ProxyUid |
| bqpath | Tenga en cuenta que esto solo es aplicable a la herramienta de carga masiva (Cloud SDK). </br> Para evitar usar la variable PATH o si el directorio google-cloud-sdk debe moverse a otra ubicación, puede especificar con esta opción la ruta exacta al directorio bin del sdk en la nube en el servidor. |
| GCloudConfigName | Tenga en cuenta que esto es aplicable a partir de la versión 7.3.4 y solo para la herramienta de carga masiva (Cloud SDK).</br>: el SDK de Google Cloud utiliza configuraciones para cargar datos en tablas de BigQuery. La configuración denominada `accfda` almacena los parámetros para cargar los datos. Sin embargo, esta opción permite a los usuarios especificar un nombre diferente para la configuración. |
| GCloudDefaultConfigName | Tenga en cuenta que esto es aplicable a partir de la versión 7.3.4 y solo para la herramienta de carga masiva (Cloud SDK).</br>: la configuración activa del SDK de Google Cloud no se puede eliminar sin transferir primero la etiqueta activa a una nueva configuración. Esta configuración temporal es necesaria para volver a crear la configuración principal para cargar datos. El nombre predeterminado para la configuración temporal es `default`, que se puede cambiar si es necesario. |
| GCloudRecreateConfig | Tenga en cuenta que esto es aplicable a partir de la versión 7.3.4 y solo para la herramienta de carga masiva (Cloud SDK).</br> Cuando se establece en `false`, el mecanismo de carga masiva se abstiene de intentar recrear, eliminar o modificar las configuraciones del SDK de Google Cloud. En su lugar, procede con la carga de datos utilizando la configuración existente en el equipo. Esta función es útil cuando otras operaciones dependen de las configuraciones del SDK de Google Cloud. </br> Si el usuario habilita esta opción de motor sin una configuración adecuada, el mecanismo de carga masiva emitirá un mensaje de advertencia: `No active configuration found. Please either create it manually or remove the GCloudRecreateConfig option`. Para evitar más errores, volverá a utilizar el mecanismo de carga masiva predeterminado de inserción de matriz ODBC. |

## Azure synapse Redshift {#azure-synapse-redshift}

* **[!UICONTROL Servidor]**: URL del servidor de Azure synapse

* **[!UICONTROL Cuenta]**: Nombre del usuario

* **[!UICONTROL Contraseña]**: Contraseña de la cuenta de usuario

* **[!UICONTROL Base de datos]**: Nombre de la base de datos

* **[!UICONTROL Options]**

## Vertica Analytics {#vertica-analytics}

* **[!UICONTROL Servidor]**: URL del servidor [!DNL Vertica Analytics]

* **[!UICONTROL Cuenta]**: Nombre del usuario

* **[!UICONTROL Contraseña]**: Contraseña de la cuenta de usuario

* **[!UICONTROL Base de datos]**: Nombre de la base de datos

* **[!UICONTROL Esquema de trabajo]**: Nombre de su esquema de trabajo.

* **[!UICONTROL Opciones]**: el conector admite las opciones detalladas en la tabla siguiente.

El conector admite las siguientes opciones:

| Opción | Descripción |
|---|---|
| TimeZoneName | De forma predeterminada, vacío, lo que significa que se utiliza la zona horaria del sistema del servidor de aplicaciones de Campaign Classic. La opción se puede utilizar para forzar el parámetro de sesión TIMEZONE. |


## Amazon Redshift {#amazon-redshift}

* **[!UICONTROL Servidor]**: nombre del DNS

* **[!UICONTROL Cuenta]**: Nombre del usuario

* **[!UICONTROL Contraseña]**: Contraseña de la cuenta de usuario

* **[!UICONTROL Base de datos]**: Nombre de la base de datos si no se especifica en DSN. Se puede dejar vacío si se especifica en el DSN

* **[!UICONTROL Esquema de trabajo]**: Nombre de su esquema de trabajo. [Más información](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

