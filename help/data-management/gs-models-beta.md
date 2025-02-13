---
audience: end-user
title: Introducción a los modelos de datos
description: Obtenga información sobre cómo iniciar modelos de datos
hide: true
hidefromtoc: true
source-git-commit: c3025f4682696352dd5d0999268b4413befe1d66
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 2%

---

# Introducción a los modelos de datos {#data-model-beta}

>[!AVAILABILITY]
>
>Actualmente, el modelo de datos con vista de lienzo está disponible como una versión beta para seleccionar solo usuarios.

## ¿Qué es un modelo de datos? {#data-model-start}

Un modelo de datos es un conjunto de esquemas, audiencias y los vínculos entre ellos. Se utiliza para federar audiencias con datos de bases de datos.

Más información sobre [esquemas](../customer/schemas.md#schema-start) y [audiencias](../start/audiences.md).

Por ejemplo, puede ver debajo una representación de un modelo de datos: las tablas con su nombre y los vínculos entre ellas.

![](assets/datamodel.png){zoomable="yes"}

En la Composición de audiencias federada, es posible crear muchos modelos de datos.

Su creación se basará en el caso de uso: elige las tablas necesarias y las vincula según sus necesidades.

## Creación de un modelo de datos {#data-model-create}

Para crear un modelo de datos, siga estos pasos:

1. En la sección **[!UICONTROL Datos federados]**, acceda al menú **[!UICONTROL Modelos]** y vaya a la pestaña **[!UICONTROL Modelo de datos]**.

   Haga clic en el botón **[!UICONTROL Crear modelo de datos]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

1. Defina el nombre del modelo de datos y haga clic en el botón **[!UICONTROL Crear]**.

1. En el panel del modelo de datos, haga clic en **[!UICONTROL Agregar esquemas]** para elegir el esquema asociado con el modelo de datos.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

1. Haga clic en **[!UICONTROL Agregar audiencias]** para definir los grupos de destino.

1. Establezca conexiones entre las tablas del modelo de datos para garantizar relaciones de datos precisas. [Más información](#data-model-links)

1. Después de completar la configuración, haz clic en **[!UICONTROL Guardar]** para aplicar los cambios.

## Crear vínculos {#data-model-links}

>[!BEGINTABS]

>[!TAB Vista de tabla]

Para crear vínculos entre tablas del modelo de datos desde la pestaña Table view, siga estos pasos:

1. Haga clic en el menú **[!UICONTROL Crear vínculo]** de una de las tablas o haga clic en el botón **[!UICONTROL Crear vínculos]** y elija las dos tablas:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

1. Rellene el formulario proporcionado para definir el vínculo.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Cardinalidad**

   * **1-N**: una incidencia de la tabla de origen puede tener varias incidencias correspondientes de la tabla de destino, pero una incidencia de la tabla de destino puede tener como máximo una incidencia correspondiente de la tabla de origen.

   * **N-1**: una incidencia de la tabla de destino puede tener varias incidencias correspondientes de la tabla de origen, pero una incidencia de la tabla de origen puede tener como máximo una incidencia correspondiente de la tabla de destino.

   * **1-1**: una incidencia de la tabla de origen puede tener como máximo una incidencia correspondiente de la tabla de destino.

Todos los vínculos definidos para el modelo de datos se enumeran a continuación:

![](assets/datamodel_alllinks.png){zoomable="yes"}

>[!TAB Vista de lienzo]

Para crear vínculos entre tablas del modelo de datos desde la pestaña Vista de lienzo, siga estos pasos:

1. Acceda a la vista Lienzo del modelo de datos y elija las dos tablas que desea vincular

1. Haga clic en el botón ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) junto a Source Join y, a continuación, arrastre y guíe la flecha hacia Target Join para establecer la conexión.

   ![](assets/datamodel.gif){zoomable="yes"}

1. Complete el formulario proporcionado para definir el vínculo y haga clic en **[!UICONTROL Aplicar]** una vez configurado.

   ![](assets/datamodel-canvas-1.png){zoomable="yes"}

   **Cardinalidad**

   * **1-N**: una incidencia de la tabla de origen puede tener varias incidencias correspondientes de la tabla de destino, pero una incidencia de la tabla de destino puede tener como máximo una incidencia correspondiente de la tabla de origen.

   * **N-1**: una incidencia de la tabla de destino puede tener varias incidencias correspondientes de la tabla de origen, pero una incidencia de la tabla de origen puede tener como máximo una incidencia correspondiente de la tabla de destino.

   * **1-1**: una incidencia de la tabla de origen puede tener como máximo una incidencia correspondiente de la tabla de destino.

1. Todos los vínculos definidos en el modelo de datos se representan como flechas en la vista de lienzo. Haga clic en una flecha entre dos tablas para ver los detalles, realizar ediciones o quitar el vínculo según sea necesario.

   ![](assets/datamodel-canvas-2.png){zoomable="yes"}

1. Utilice la barra de herramientas para personalizar y ajustar el lienzo.

   ![](assets/datamodel-canvas-3.png)

   * **[!UICONTROL Acercar]**: amplíe el lienzo para ver los detalles del modelo de datos con mayor claridad.
   * **[!UICONTROL Alejar]**: reduzca el tamaño del lienzo para obtener una vista más amplia del modelo de datos.
   * **[!UICONTROL Ajustar vista]**: ajuste el zoom para ajustar todos los esquemas y/o audiencias dentro del área visible.
   * **[!UICONTROL Alternar interactividad]**: habilita o deshabilita la interacción del usuario con el lienzo.
   * **[!UICONTROL Filtro]**: elija qué esquema mostrar en el lienzo.
   * **[!UICONTROL Forzar diseño automático]**: organice automáticamente los esquemas o audiencias para mejorar la organización.

>[!ENDTABS]

## Cómo realizar el vídeo {#data-model-video}

Aprenda a crear un modelo de datos en este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
