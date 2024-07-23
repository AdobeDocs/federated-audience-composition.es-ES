---
audience: end-user
title: Introducción a los esquemas
description: Aprenda a empezar con esquemas
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 75d539eef7b36b721c0df52b2fe9115728cf14d3
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 20%

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

Un esquema es una representación de una tabla de la base de datos. Es un objeto dentro de la aplicación que define cómo se asocian los datos a las tablas de la base de datos.

Al crear un esquema, tendrá la posibilidad de manipular la tabla en FAC :
- Asigne un nombre descriptivo para simplificar la comprensión del usuario
- Decida la visibilidad de cada campo, según su uso real
- Seleccione su clave principal para vincular esquemas entre ellos según sea necesario en el [modelo de datos](../data-management/gs-models.md#data-model-start)

## Creación de un esquema {#schema-create}

Para crear esquemas en FAC, siga los pasos a continuación:
En la sección **[!UICONTROL DATOS FEDERADOS]**, vaya al vínculo **[!UICONTROL Modelos]**. Ahí encontrará la ficha **[!UICONTROL Esquema]**.
Haga clic en el botón **[!UICONTROL Crear esquema]**.

![](assets/schema_create.png){zoomable="yes"}

Tendrá acceso a una nueva interfaz con una lista desplegable donde encontrará lo siguiente
todas las bases de datos conectadas a la aplicación. Más información sobre [conexión a base de datos](../connections/connections.md#connections-fdb).
Seleccione la base de datos de origen en la lista y haga clic en la ficha **[!UICONTROL Agregar tablas]**

![](assets/schema_tables.png){zoomable="yes"}

Tendrá acceso a la lista de todas las tablas de la base de datos.

Al agregar las tablas, para las que desea crear el esquema, tendrá acceso a sus campos como se muestra a continuación.

![](assets/schema_fields.png){zoomable="yes"}

Para cada tabla, puede hacer lo siguiente:
- cambie el nombre de la etiqueta de esquema dada
- añadir una descripción
- cambie el nombre de todos los campos y decida su visibilidad.
- seleccione la clave principal del esquema

Por ejemplo, aquí se importa una tabla, justo después de la etiqueta add :

![](assets/schema_lumaorder.png){zoomable="yes"}

El esquema se puede definir de esta manera:

![](assets/schema_lumaorders.png){zoomable="yes"}

## Edición de un esquema {#schema-edit}

Para editar un esquema, haga clic en el nombre del esquema en la carpeta de esquemas. Tendrá acceso a la página siguiente.
Haz clic en el botón **[!UICONTROL Editar]**.

![](assets/schema_edit.png){zoomable="yes"}

Tendrá acceso a la misma posibilidad que al crear el esquema:
- cambie el nombre de la etiqueta de esquema dada
- añadir una descripción
- cambie el nombre de todos los campos y decida su visibilidad.
- seleccione la clave principal del esquema

![](assets/schema_edit_orders.png){zoomable="yes"}

## Vista previa de datos en un esquema {#schema-preview}

Para obtener una vista previa de los datos de la tabla representada por su esquema, vaya a la pestaña **[!UICONTROL Data]** como se muestra a continuación.
Puede obtener el número total de grabaciones haciendo clic en el vínculo **[!UICONTROL Calcular]**.

![](assets/schema_data.png){zoomable="yes"}

Puede cambiar la Información general de datos haciendo clic en el botón **[!UICONTROL Configurar columnas]**.

![](assets/schema_columns.png){zoomable="yes"}

## Eliminar un esquema {#schema-delete}

Para eliminar un esquema, haga clic en el botón **[!UICONTROL Más]** y luego en **[!UICONTROL Eliminar]**.

![](assets/schema_delete.png){zoomable="yes"}