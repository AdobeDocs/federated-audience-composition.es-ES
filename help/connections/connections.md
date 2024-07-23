---
audience: end-user
title: Crear y administrar conexiones con bases de datos federadas
description: Aprenda a crear y administrar conexiones con bases de datos federadas
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: c1c035d3783af6c3bc94f2ba0aff7ba515fb68e2
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 5%

---

# Creación de conexiones {#connections-fdb}

Trabajar con una base de datos federada directamente en AEP implica establecer una conexión con ella.

Para configurar una conexión con su base de datos, vaya a la sección **[!UICONTROL DATOS FEDERADOS]** y en el vínculo **[!UICONTROL Bases de datos federadas]**, haga clic en el botón **[!UICONTROL Agregar base de datos federada]**.

![](assets/connections_list.png){zoomable="yes"}

Tendrá acceso a la ventana de la conexión **[!UICONTROL Properties]**, con el nombre y el tipo de su base de datos.

![](assets/connections_name.png){zoomable="yes"}

Si selecciona su tipo, tendrá acceso a otras propiedades para rellenar. [Obtenga más información aquí acerca de las bases de datos compatibles](federated-db.md).

![](assets/connections_details.png){zoomable="yes"}

Según el tipo de base de datos, aprenda en los vínculos siguientes la información que necesita para configurar la conexión:

* [Amazon Redshift](federated-db.md#amazon-redshift)
* [Azure synapse](federated-db.md#azure-synapse-redshift)
* [Google Big Query](federated-db.md#google-big-query)
* [Snowflake](federated-db.md#snowflake)
* [Vertica Analytics](federated-db.md#vertica-analytics)

Después de completar los detalles, haga clic en el botón **[!UICONTROL Probar conexión]** y en el botón **[!UICONTROL Implementar funciones]**.
Finalice la creación de la conexión haciendo clic en el botón **[!UICONTROL Guardar]**.

![](assets/connections_testdeploy.png){zoomable="yes"}

Tendrá una descripción general de la conexión a base de datos federada como esta:

![](assets/connections_overview.png){zoomable="yes"}
