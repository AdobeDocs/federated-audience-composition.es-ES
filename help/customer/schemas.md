---
audience: end-user
title: Introducción a los esquemas
description: Aprenda a empezar con esquemas
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 883ba223f6c78783fae9f6c9617daa1a7e6635de
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 34%

---

# Introducción a los esquemas {#schemas}


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
>abstract="Puede filtrar los esquemas en función de su fuente. Seleccione una o varias bases de datos federadas para mostrar sus esquemas."


## ¿Qué es un esquema? {#schema-start}

Un esquema es un objeto dentro de la aplicación que define cómo se vinculan los datos a las tablas de la base de datos.
Un esquema hace referencia a una tabla.

## Creación de un esquema {#schema-create}

En la sección **[!UICONTROL DATOS FEDERADOS]**, vaya al vínculo **[!UICONTROL Modelos]**. Ahí encontrará la ficha **[!UICONTROL Esquema]**.
Haga clic en el botón **[!UICONTROL Crear esquema]**.

![](assets/schema_create.png){zoomable="yes"}

Seleccione la base de datos de origen en la lista desplegable y haga clic en la ficha **[!UICONTROL Agregar tablas]**

![](assets/schema_tables.png){zoomable="yes"}

Tendrá acceso a todas las tablas de la base de datos y para las que puede crear un esquema.

Al agregar las tablas, tendrá acceso a sus campos y podrá administrar lo que realmente necesita.

![](assets/schema_fields.png){zoomable="yes"}

## Edición de un esquema {#schema-edit}

Para editar un esquema, haga clic en el nombre del esquema en la carpeta de esquemas. Tendrá acceso a la página siguiente.
Haz clic en el botón **[!UICONTROL Editar]**.

![](assets/schema_edit.png){zoomable="yes"}

## Vista previa de datos en un esquema {#schema-preview}

Para obtener una vista previa de los datos de la tabla representada por su esquema, vaya a la pestaña **[!UICONTROL Data]** como se muestra a continuación.

![](assets/schema_data.png){zoomable="yes"}

Puede cambiar la Información general de datos haciendo clic en el botón **[!UICONTROL Configurar columnas]**.

![](assets/schema_columns.png){zoomable="yes"}

## Eliminar un esquema {#schema-delete}

Para eliminar un esquema, haga clic en el botón **[!UICONTROL Más]** y luego en **[!UICONTROL Eliminar]**.

![](assets/schema_delete.png){zoomable="yes"}