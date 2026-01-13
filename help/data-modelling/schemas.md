---
audience: end-user
title: Introducción a los esquemas
description: Aprenda a empezar con esquemas
exl-id: 2c939185-f1c1-4f2b-ae1b-e2539e121eff
source-git-commit: 9b951f74443ac149e837c3f52ca265acabd407b9
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 16%

---

# Información general de esquemas {#schemas}

>[!AVAILABILITY]
>
>Para acceder a los esquemas, necesita uno de los siguientes permisos:
>
>-**Administrar esquema federado**
>-**Ver esquema federado**
>
>Para obtener más información sobre los permisos necesarios, consulte la [guía de control de acceso](/help/governance-privacy-security/access-control.md).

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
>abstract="La descripción del esquema enumera columnas, tipos y etiquetas. También puede comprobar la clave de reconciliación para el esquema. Para actualizar la definición del esquema, seleccione el icono de lápiz."

>[!CONTEXTUALHELP]
>id="dc_schema_filter_sources"
>title="Seleccione la base de datos fuente que desea filtrar"
>abstract="Puede filtrar los esquemas en función de su fuente. Selecciona una o varias bases de datos federadas para mostrar sus esquemas."

Un esquema es una representación de una tabla de la base de datos. Es un objeto dentro de la aplicación que define cómo se asocian los datos a las tablas de la base de datos.

Al crear un esquema, puede definir una representación de la tabla en la Composición de audiencias federada de Experience Platform:

* Asigne un nombre descriptivo para simplificar la comprensión del usuario
* Decidir la visibilidad de cada campo, según su uso real
* Seleccione su clave principal para vincular esquemas entre ellos según sea necesario en el [modelo de datos](../data-modelling/models.md#data-model-start)

>[!CAUTION]
>
>Al conectar varios entornos limitados con la misma base de datos, debe utilizar esquemas de trabajo diferentes.

## Creación de un esquema {#schema-create}

Para crear un esquema en Federated Audience Composition, seleccione **[!UICONTROL Modelos]** en la sección **[!UICONTROL Datos federados]**. En la ficha **[!UICONTROL Esquema]**, seleccione **[!UICONTROL Crear esquema]**.

![El botón Crear esquema está resaltado en la sección de esquema Federate Audience Composition.](assets/schemas/schema_create.png){zoomable="yes"}

Aparece la ventana emergente **[!UICONTROL Seleccionar base de datos federada]**. En esta ventana emergente, puede seleccionar la [base de datos de origen](/help/connections/home.md), seguida de **[!UICONTROL Siguiente]**.


![](assets/schemas/schema_tables.png){zoomable="yes"}

Aparece la ventana emergente **Seleccionar tabla**. En esta ventana emergente, puede seleccionar las tablas que desea utilizar para crear el esquema.

![Se muestra la ventana emergente Seleccionar tabla.](assets/schemas/select-table.png){zoomable="yes"}

Cada tabla seleccionada genera un esquema con las columnas seleccionadas. Para cada tabla, puede cambiar la etiqueta del esquema, agregar una descripción, cambiar el nombre de la etiqueta del campo, establecer la visibilidad de la etiqueta del campo y seleccionar la clave principal del esquema.

![](assets/schemas/schema-fields.png){zoomable="yes"}

>[!NOTE]
>
>Si habilita **[!UICONTROL Usar clave compuesta]** pero solo selecciona una clave para usar, la clave se tratará como una clave principal de esquema estándar.

Además, puede crear una clave que esté formada por varias columnas de esquema. Active **[!UICONTROL Usar clave compuesta]** y marque las claves que desee usar como clave compuesta.

![](assets/schemas/composite-key.png){zoomable="yes"}

Después de completar la configuración, selecciona **[!UICONTROL Listo]** para terminar de crear el esquema.

## Edición de un esquema {#schema-edit}

Para editar un esquema, seleccione el esquema creado anteriormente en la página **Esquemas**.

Aparecerá la página de detalles del esquema. Seleccione el ![icono de lápiz](/help/assets/icons/edit.png) para editar el esquema.

![](assets/schemas/schema_edit.png){zoomable="yes"}

En la ventana **[!UICONTROL Editar esquema]**, puede acceder y configurar las mismas opciones que al [crear un esquema](#schema-create).

![](assets/schemas/schema_edit_orders.png){zoomable="yes"}

## Vista previa de datos en un esquema {#schema-preview}

Para obtener una vista previa de los datos de la tabla representada por su esquema, vaya a la pestaña **[!UICONTROL Data]** como se muestra a continuación.

Seleccione el vínculo **[!UICONTROL Calcular]** para obtener una vista previa del número total de grabaciones.

![](assets/schemas/schema_data.png){zoomable="yes"}

Seleccione el botón **[!UICONTROL Configurar columnas]** para cambiar la visualización de datos.

![](assets/schemas/schema_columns.png){zoomable="yes"}

## Actualizar un esquema {#schema-refresh}

Las tablas de una base de datos federada se pueden actualizar, agregar o quitar. En estos casos, debe actualizar el esquema en Adobe Experience Platform para alinearlo con los cambios más recientes. Para ello, seleccione el ![icono de tres puntos](/help/assets/icons/more.png) junto al nombre del esquema seguido de **[!UICONTROL Actualizar esquema]**.

También puede actualizar la definición del esquema al editarla.

![](assets/schemas/schema_refresh.png){zoomable="yes"}

## Eliminar un esquema {#schema-delete}

Para eliminar un esquema, seleccione el ![icono de tres puntos](/help/assets/icons/more.png), seguido de **[!UICONTROL Eliminar]**.

![](assets/schemas/schema_delete.png){zoomable="yes"}
