---
audience: end-user
title: Información general de esquemas
description: Aprenda a crear y utilizar esquemas para la composición de audiencias federada en la interfaz de usuario de Adobe Experience Platform.
TQID: https://experienceleague.adobe.com/cpkFeiskYDpixNo01llqC3UKK8XfewN7XC2yAf1wOYQ
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: Experience Cloud
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
    internal-label: Governance
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 3b159f95e28414b75b44e41e822e9e3d0e35b537
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 3%
---
# Información general de esquemas {#schemas}

>[!AVAILABILITY]
>
>La nueva experiencia de esquemas solo está disponible para clientes seleccionados. Para obtener más información, póngase en contacto con el Servicio de atención al cliente de Adobe.
>
>Si no tiene acceso a la nueva experiencia de esquemas, lea la [descripción general de esquemas](./schemas.md).
>
>Para acceder a los esquemas, necesita uno de los siguientes permisos:
>
>-**Administrar esquema federado**
>-**Ver esquema federado**
>
>Para obtener más información sobre los permisos necesarios, consulte la [guía de control de acceso](/help/governance-privacy-security/access-control.md).

Un esquema es una representación de una tabla de la base de datos. Es un objeto dentro de la aplicación que define cómo se asocian los datos a las tablas de la base de datos.

Al crear un esquema, puede definir una representación de la tabla en la Composición de audiencias federada de Experience Platform:

* Asigne un nombre descriptivo para simplificar la comprensión del usuario
* Decidir la visibilidad de cada campo, según su uso real
* Seleccione su clave principal para vincular esquemas entre ellos según sea necesario en el [modelo de datos](../data-modelling/models.md#data-model-start)

>[!CAUTION]
>
>Al conectar varios entornos limitados con la misma base de datos, debe utilizar esquemas de trabajo diferentes.

## Creación de un esquema {#create}

>[!CONTEXTUALHELP]
>id="platform_schemas_manageconfiguration"
>title="Administrar configuración"
>abstract="Contenido temporal en blanco."

Para crear un esquema en Federated Audience Composition, seleccione **[!UICONTROL Esquemas]** en la sección **[!UICONTROL Administración de datos]** de la interfaz de usuario de Experience Platform. En la interfaz de usuario de esquemas, seleccione **[!UICONTROL Crear esquema]**.

![Los botones Esquemas y Crear esquema están resaltados en la interfaz de usuario de Esquemas.](/help/data-modelling/assets/integrated/select-create-schema.png)

Una vez que aparezca la ventana emergente Crear esquema, seleccione **[!UICONTROL Relacional]**, seguido de **[!UICONTROL Detectar esquemas]** y **[!UICONTROL Siguiente]** para crear un esquema para la Composición de audiencias federada.

![El botón Detectar esquemas está resaltado en la ventana emergente Crear un esquema relacional.](/help/data-modelling/assets/integrated/select-discover-schemas.png)

Aparece la ventana emergente **[!UICONTROL Seleccionar base de datos federada]**. En esta ventana emergente, puede seleccionar la [base de datos de origen](/help/connections/home.md), seguida de **[!UICONTROL Siguiente]**.

![Se muestra la ventana emergente Seleccionar base de datos federada.](/help/data-modelling/assets/integrated/select-federated-database.png)

## Definir esquema {#define}

>[!CONTEXTUALHELP]
>id="platform_schemas_primarycompositekey"
>title="Clave compuesta"
>abstract="Una clave de esquema que consta de varias columnas de esquema. Marque las columnas que desee utilizar como clave compuesta."

Después de elegir la base de datos federada, puede definir el esquema. Aparecerá la pantalla **[!UICONTROL Agregar datos]**. En esta página, puede seleccionar **[!UICONTROL Agregar tabla]** para elegir qué tablas desea agregar al esquema.

![El botón Agregar tabla está resaltado en la pantalla Agregar datos.](/help/data-modelling/assets/integrated/select-add-table.png)

Aparece la ventana emergente **[!UICONTROL Seleccionar tabla]**. En esta ventana emergente, puede seleccionar las tablas que desea utilizar para crear el esquema.

![Se muestra la ventana emergente Seleccionar tabla.](/help/data-modelling/assets/integrated/select-table.png){zoomable="yes"}

Cada tabla seleccionada genera un esquema con las columnas seleccionadas. Para cada tabla, puede cambiar la etiqueta del esquema, agregar una descripción, cambiar el nombre de la etiqueta del campo, establecer la visibilidad de la etiqueta del campo y seleccionar la clave principal del esquema.

![Las tablas seleccionadas se muestran en la página Agregar datos.](/help/data-modelling/assets/integrated/tables-added.png){zoomable="yes"}

>[!NOTE]
>
>Si elige **[!UICONTROL Clave compuesta]** pero solo selecciona una clave para usar, la clave se tratará como una clave principal de esquema estándar.

Además, puede crear una clave que esté formada por varias columnas de esquema. Seleccione **[!UICONTROL Clave compuesta]** y marque las claves que desee usar como clave compuesta.

![Se seleccionaron tanto la opción Clave compuesta como los esquemas.](/help/data-modelling/assets/integrated/composite-key.png){zoomable="yes"}

Después de completar la configuración, selecciona **[!UICONTROL Listo]** para terminar de crear el esquema.

## Edición de un esquema {#schema-edit}

Para editar un esquema, seleccione el icono de ![elipses](/help/assets/icons/more.png) junto al esquema creado anteriormente en la página **Esquemas**, seguido de **[!UICONTROL Editar]**.

![El botón Editar esquema está resaltado.](/help/data-modelling/assets/integrated/edit-schema.png)

En la ventana **[!UICONTROL Editar esquema]**, puede ver el Editor de esquemas. Para obtener más información sobre el uso del Editor de esquemas, lea la [guía de la interfaz de usuario del esquema](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas#customize-schema).

![Se muestra el Editor de esquemas.](/help/data-modelling/assets/integrated/schema-editor.png)

### Editar relaciones {#relationship-edit}

Para editar las relaciones de un esquema, seleccione **[!UICONTROL Ver diagrama de entidad]** en el Editor de esquemas.

![El botón Ver diagrama de entidad está resaltado.](/help/data-modelling/assets/integrated/view-entity-diagram.png)

Aparecerá la página del diagrama de entidades. En esta página, puede crear vínculos para establecer relaciones entre los esquemas.

![Se muestra el diagrama de entidad.](/help/data-modelling/assets/integrated/entity-diagram.png)

Para obtener más información sobre la creación de vínculos, lea la ficha Vista de lienzo de la [descripción general de los modelos de datos](/help/data-modelling/models.md#data-model-links).

## Vista previa de datos en un esquema {#schema-preview}

Para obtener una vista previa de los datos de la tabla representada por el esquema, vaya a la sección **[!UICONTROL Conjuntos de datos]** y, a continuación, seleccione **[!UICONTROL Examinar]**.

![Se resaltan los conjuntos de datos y los botones Examinar.](/help/data-modelling/assets/integrated/datasets-browse.png)

Seleccione los ![tres puntos](/help/assets/icons/more.png), seguidos de **[!UICONTROL Vista previa del conjunto de datos]** para ver una vista previa de los datos dentro del esquema.

![El botón Vista previa del conjunto de datos está resaltado.](/help/data-modelling/assets/integrated/select-preview-dataset.png)

## Actualizar un esquema {#schema-refresh}

Las tablas de una base de datos federada se pueden actualizar, agregar o quitar. En estos casos, debe actualizar el esquema en Adobe Experience Platform para alinearlo con los cambios más recientes. Para actualizar el esquema, seleccione el botón **[!UICONTROL Más]**, seguido de **[!UICONTROL Administrar configuración]**.

![El botón Administrar configuración está resaltado.](/help/data-modelling/assets/integrated/manage-configuration.png)

Aparece la ventana emergente **[!UICONTROL Editar configuración]**. Seleccione **[!UICONTROL Actualizar]** para actualizar el esquema.

![El botón Actualizar esquema está resaltado.](/help/data-modelling/assets/integrated/refresh-schema.png)

## Eliminar un esquema {#schema-delete}

Para eliminar un esquema en el Editor de esquemas, seleccione **[!UICONTROL Más]**, seguido de **[!UICONTROL Eliminar]**.

![El botón Eliminar esquema está resaltado.](/help/data-modelling/assets/integrated/delete-schema.png)
