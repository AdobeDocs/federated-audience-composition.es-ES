---
audience: end-user
title: Introducción a los esquemas
description: Aprenda a empezar con esquemas
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 5c16e22587cbbbe5bc87cfa4f22210aa8108341c
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 18%

---

# Introducción a los esquemas {#schemas}

>[!AVAILABILITY]
>
>Para acceder a los esquemas, necesita uno de los siguientes permisos:
>
>-**Administrar esquema federado**
>>-**Ver esquema federado**
>
>Para obtener más información sobre los permisos requeridos, lea la [guía de control de acceso](/help/governance-privacy-security/access-control.md).

>[!CONTEXTUALHELP]
>id="dc_schema_create_select_tables"
>title="Seleccionar tablas"
>abstract="Seleccione las tablas que desea añadir al modelo de datos."

>[!CONTEXTUALHELP]
>id="dc_schema_create_key"
>title="Clave"
>abstract="Seleccione una clave para la reconciliación de datos."

>[!CONTEXTUALHELP]
>id="dc_schema_create_schema_name"
>title="Nombre del esquema"
>abstract="Introduzca el nombre del esquema."

>[!CONTEXTUALHELP]
>id="dc_schema_edit_description"
>title="Descripción del esquema"
>abstract="La descripción del esquema enumera columnas, tipos y etiquetas. También puede comprobar la clave de reconciliación para el esquema. Para actualizar la definición del esquema, haga clic en el icono de lápiz."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Seleccione la base de datos fuente que desea filtrar"
>abstract="Puede filtrar los esquemas en función de su fuente. Selecciona una o varias bases de datos federadas para mostrar sus esquemas."

## ¿Qué es un esquema? {#schema-start}

Un esquema es una representación de una tabla de la base de datos. Es un objeto dentro de la aplicación que define cómo se asocian los datos a las tablas de la base de datos.

Al crear un esquema, puede definir una representación de la tabla en la Composición de audiencias federada de Experience Platform:

* Asigne un nombre descriptivo para simplificar la comprensión del usuario
* Decidir la visibilidad de cada campo, según su uso real
* Seleccione su clave principal para vincular esquemas entre ellos según sea necesario en el [modelo de datos](../data-management/gs-models.md#data-model-start)

>[!CAUTION]
>
>Al conectar varios entornos limitados con la misma base de datos, debe utilizar esquemas de trabajo diferentes.
>

## Creación de un esquema {#schema-create}

Para crear esquemas en Composición de audiencia federada, siga los pasos a continuación:

1. En la sección **[!UICONTROL Datos federados]**, obtenga acceso al menú **[!UICONTROL Modelos]**. Vaya a la pestaña **[!UICONTROL Esquema]** y haga clic en **[!UICONTROL Crear esquema]**.

   ![](assets/schema_create.png){zoomable="yes"}

   Este paso le permite acceder a una nueva pantalla con una lista desplegable en la que puede encontrar las bases de datos conectadas a su entorno. Obtenga más información acerca de la conexión a la base de datos en [esta sección](../connections/connections.md#connections-fdb).

1. Seleccione la base de datos de origen en la lista y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/schema_tables.png){zoomable="yes"}

   Puede ver la lista de todas las tablas de la base de datos.

1. Seleccione las tablas para las que desea crear el esquema.

1. Cada tabla seleccionada genera un esquema con las columnas seleccionadas. Configure el esquema y sus columnas según sea necesario.

   ![](assets/schema_fields.png){zoomable="yes"}

   Para cada tabla, puede:

   * cambiar la etiqueta del esquema
   * añadir una descripción
   * cambie el nombre de todas las etiquetas de campo y establezca su visibilidad
   * seleccione la clave principal del esquema

   El esquema se puede definir de la siguiente manera:

   ![](assets/schema_example.png)

1. Después de completar la configuración, haz clic en **[!UICONTROL Listo]**.

## Edición de un esquema {#schema-edit}

Para editar un esquema, siga estos pasos:

1. Acceda al esquema creado anteriormente.

1. Haz clic en el botón **[!UICONTROL Editar]**.

   ![](assets/schema_edit.png){zoomable="yes"}

1. Desde la ventana **[!UICONTROL Editar esquema]**, puede acceder y configurar las mismas opciones que al [crear un esquema](#schema-create).

   ![](assets/schema_edit_orders.png){zoomable="yes"}

## Vista previa de datos en un esquema {#schema-preview}

Para obtener una vista previa de los datos de la tabla representada por su esquema, vaya a la pestaña **[!UICONTROL Data]** como se muestra a continuación.

Haga clic en el vínculo **[!UICONTROL Calcular]** para obtener una vista previa del número total de grabaciones.

![](assets/schema_data.png){zoomable="yes"}

Haga clic en el botón **[!UICONTROL Configurar columnas]** para cambiar la visualización de datos.

![](assets/schema_columns.png){zoomable="yes"}

## Actualizar un esquema {#schema-refresh}

Las tablas de una base de datos federada se pueden actualizar, agregar o quitar. En estos casos, debe actualizar el esquema en Adobe Experience Platform para alinearlo con los cambios más recientes. Para ello, haga clic en los tres puntos junto al nombre del esquema que desea actualizar y seleccione **Actualizar esquema**.

También puede actualizar la definición del esquema al editarla.

![](assets/schema_refresh.png){zoomable="yes"}


## Eliminar un esquema {#schema-delete}

Para eliminar un esquema, haga clic en el botón **[!UICONTROL Más]** y, a continuación, elija **[!UICONTROL Eliminar]**.

![](assets/schema_delete.png){zoomable="yes"}
