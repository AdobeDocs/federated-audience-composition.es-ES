---
audience: end-user
title: Introducción a las bases de datos federadas
description: Aprenda a crear y administrar sus bases de datos federadas
badge: label="Disponibilidad limitada" type="Informative"
exl-id: b8c0589d-4150-40da-ac79-d53cced236e8
source-git-commit: 75f997e4b1c0338a635dff43e2254757fbc5ec69
workflow-type: tm+mt
source-wordcount: '1467'
ht-degree: 16%

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

La composición de audiencias federadas de Experience Platform permite al cliente crear y enriquecer audiencias de los almacenes de datos de terceros e importarlas a Adobe Experience Platform.

Obtenga información sobre cómo crear, configurar, probar y guardar la conexión con la base de datos externa en esta página.

## Bases de datos compatibles {#supported-db}

Con Federated Audience Composition, puede conectarse a las siguientes bases de datos. A continuación se detalla la configuración de cada base de datos.

* [Amazon Redshift](#amazon-redshift)
* [Azure synapse](#azure-synapse-redshift)
* [Google Big Query](#google-big-query)
* [Snowflake](#snowflake)
* [Vertica Analytics](#vertica-analytics)

## Amazon Redshift {#amazon-redshift}

Utilice las bases de datos federadas para procesar la información almacenada en una base de datos externa. Siga los pasos a continuación para configurar el acceso a Amazon Redshift.

1. En el menú **[!UICONTROL Datos federados]**, seleccione **[!UICONTROL Bases de datos federadas]**.

1. Haga clic en **[!UICONTROL Agregar base de datos federada]**.

   ![](assets/federated_database_1.png)

1. Escriba un **[!UICONTROL Nombre]** en la base de datos federada.

1. En el menú desplegable **[!UICONTROL Tipo]**, seleccione Amazon Redshift.

   ![](assets/federated_database_6.png)

1. Configure las opciones de autenticación de Amazon Redshift:

   * **[!UICONTROL Servidor]**: agregue el nombre del DNS.

   * **[!UICONTROL Cuenta]**: Agregue el nombre de usuario.

   * **[!UICONTROL Contraseña]**: Agregue la contraseña de la cuenta.

   * **[!UICONTROL Base de datos]**: Nombre de la base de datos si no se especifica en DSN. Se puede dejar vacío si se especifica en el DSN

   * **[!UICONTROL Esquema de trabajo]**: Nombre de su esquema de trabajo. [Más información](https://docs.aws.amazon.com/redshift/latest/dg/r_Schemas_and_tables.html)

1. Seleccione la opción **[!UICONTROL Probar la conexión]** para comprobar la configuración.

1. Haga clic en el botón **[!UICONTROL Implementar funciones]** para crear las funciones.

1. Una vez completada la configuración, haz clic en **[!UICONTROL Agregar]** para crear tu base de datos federada.

## Azure synapse Redshift {#azure-synapse-redshift}

Utilice las bases de datos federadas para procesar la información almacenada en una base de datos externa. Siga los pasos a continuación para configurar el acceso a Azure synapse Redshift.

1. En el menú **[!UICONTROL Datos federados]**, seleccione **[!UICONTROL Bases de datos federadas]**.

1. Haga clic en **[!UICONTROL Agregar base de datos federada]**.

   ![](assets/federated_database_1.png)

1. Escriba un **[!UICONTROL Nombre]** en la base de datos federada.

1. En la lista desplegable **[!UICONTROL Tipo]**, seleccione Azure synapse Redshift.

   ![](assets/federated_database_4.png)

1. Configure las opciones de autenticación Redshift de Azure synapse:

   * **[!UICONTROL Servidor]**: escriba la dirección URL del servidor de Azure synapse.

   * **[!UICONTROL Cuenta]**: escriba el nombre de usuario.

   * **[!UICONTROL Contraseña]**: escriba la contraseña de la cuenta.

   * **[!UICONTROL Base de datos]** (opcional): escriba el nombre de la base de datos si no se especifica en el DSN.

   * **[!UICONTROL Opciones]**: el conector admite las opciones detalladas en la tabla siguiente.

1. Seleccione la opción **[!UICONTROL Probar la conexión]** para comprobar la configuración.

1. Haga clic en el botón **[!UICONTROL Implementar funciones]** para crear las funciones.

1. Una vez completada la configuración, haz clic en **[!UICONTROL Agregar]** para crear tu base de datos federada.

| Opción | Descripción |
|:-:|:-:|
| Autenticación | Tipo de autenticación admitida por el conector. Valor admitido actual: ActiveDirectoryMSI. Para obtener más información, consulte [Documento SQL](https://learn.microsoft.com/en-us/sql/connect/odbc/using-azure-active-directory?view=sql-server-ver15#example-connection-strings) (Ejemplo de cadenas de conexión n°8) |


## Google Big Query {#google-big-query}

Utilice las bases de datos federadas para procesar la información almacenada en una base de datos externa. Siga los pasos a continuación para configurar el acceso a Google Big Query.

1. En el menú **[!UICONTROL Datos federados]**, seleccione **[!UICONTROL Bases de datos federadas]**.

1. Haga clic en **[!UICONTROL Agregar base de datos federada]**.

   ![](assets/federated_database_1.png)

1. Escriba un **[!UICONTROL Nombre]** en la base de datos federada.

1. En la lista desplegable **[!UICONTROL Tipo]**, seleccione Google Big Query.

   ![](assets/federated_database_3.png)

1. Configure las opciones de autenticación de Google Big Query:

   * **[!UICONTROL Cuenta de servicio]**: escribe el correo electrónico de tu **[!UICONTROL cuenta de servicio]**. Para obtener más información, consulte [Documentación de Google Cloud](https://cloud.google.com/iam/docs/creating-managing-service-accounts).

   * **[!UICONTROL Proyecto]**: Escriba el nombre de su **[!UICONTROL Proyecto]**. Para obtener más información, consulte [Documentación de Google Cloud](https://cloud.google.com/resource-manager/docs/creating-managing-projects).

   * **[!UICONTROL Conjunto de datos]**: escriba el nombre de su **[!UICONTROL Conjunto de datos]**. Para obtener más información, consulte [Documentación de Google Cloud](https://cloud.google.com/bigquery/docs/datasets-intro).

   * **[!UICONTROL Ruta del archivo de claves]**: Cargue el archivo de claves en el servidor. Solo se aceptan archivos .json.

   * **[!UICONTROL Opciones]**: el conector admite las opciones detalladas en la tabla siguiente.

1. Seleccione la opción **[!UICONTROL Probar la conexión]** para comprobar la configuración.

1. Haga clic en el botón **[!UICONTROL Implementar funciones]** para crear las funciones.

1. Una vez completada la configuración, haz clic en **[!UICONTROL Agregar]** para crear tu base de datos federada.

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


## Snowflake {#snowflake}

Utilice las bases de datos federadas para procesar la información almacenada en una base de datos externa. Siga los pasos a continuación para configurar el acceso al Snowflake.

1. En el menú **[!UICONTROL Datos federados]**, seleccione **[!UICONTROL Bases de datos federadas]**.

1. Haga clic en **[!UICONTROL Agregar base de datos federada]**.

   ![](assets/federated_database_1.png)

1. Escriba un **[!UICONTROL Nombre]** en la base de datos federada.

1. En la lista desplegable **[!UICONTROL Tipo]**, seleccione Snowflake.

   ![](assets/federated_database_2.png)

1. Configure las opciones de autenticación del Snowflake:

   * **[!UICONTROL Servidor]**: escriba el nombre de su servidor.

   * **[!UICONTROL Usuario]**: Escriba su nombre de usuario.

   * **[!UICONTROL Contraseña]**: Escriba la contraseña de su cuenta.

   * **[!UICONTROL Base de datos]** (opcional): escriba el nombre de la base de datos si no se especifica en el DSN.

   * **[!UICONTROL Esquema de trabajo]** (opcional): escriba el nombre del esquema de trabajo.

   * **[!UICONTROL Clave privada]**: Haga clic en el campo **[!UICONTROL Clave privada]** para seleccionar los archivos .pem de la carpeta de configuración regional.

   * **[!UICONTROL Opciones]**: el conector admite las opciones detalladas en la tabla siguiente.

1. Seleccione la opción **[!UICONTROL Probar la conexión]** para comprobar la configuración.

1. Haga clic en el botón **[!UICONTROL Implementar funciones]** para crear las funciones.

1. Una vez completada la configuración, haz clic en **[!UICONTROL Agregar]** para crear tu base de datos federada.

El conector admite las siguientes opciones:

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


## Vertica Analytics {#vertica-analytics}

Utilice las bases de datos federadas para procesar la información almacenada en una base de datos externa. Siga los pasos a continuación para configurar el acceso a las Verticas analytics.

1. En el menú **[!UICONTROL Datos federados]**, seleccione **[!UICONTROL Bases de datos federadas]**.

1. Haga clic en **[!UICONTROL Agregar base de datos federada]**.

   ![](assets/federated_database_1.png)

1. Escriba un **[!UICONTROL Nombre]** en la base de datos federada.

1. En la lista desplegable **[!UICONTROL Tipo]**, seleccione Verticas analytics.

   ![](assets/federated_database_5.png)

1. Configure las opciones de autenticación de Verticas analytics:

   * **[!UICONTROL Servidor]**: Agregue la dirección URL del servidor [!DNL Vertica Analytics].

   * **[!UICONTROL Cuenta]**: Agregue el nombre de usuario.

   * **[!UICONTROL Contraseña]**: Agregue la contraseña de la cuenta.

   * **[!UICONTROL Base de datos]** (opcional): escriba el nombre de la base de datos si no se especifica en el DSN.

   * **[!UICONTROL Esquema de trabajo]** (opcional): escriba el nombre del esquema de trabajo.

   * **[!UICONTROL Opciones]**: el conector admite las opciones detalladas en la tabla siguiente.

1. Seleccione la opción **[!UICONTROL Probar la conexión]** para comprobar la configuración.

1. Haga clic en el botón **[!UICONTROL Implementar funciones]** para crear las funciones.

1. Una vez completada la configuración, haz clic en **[!UICONTROL Agregar]** para crear tu base de datos federada.

El conector admite las siguientes opciones:

| Opción | Descripción |
|---|---|
| TimeZoneName | De forma predeterminada, vacío, lo que significa que se utiliza la zona horaria del sistema del servidor de aplicaciones de Campaign Classic. La opción se puede utilizar para forzar el parámetro de sesión TIMEZONE. |
