---
audience: end-user
title: Introducción a los modelos de datos
description: Obtenga información sobre cómo iniciar modelos de datos
exl-id: 7e1f74c4-b89a-480c-8e12-0257a71e629d
source-git-commit: d8fd926a445e65b6c7310d2ceac5a83ba9fece3f
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 34%

---


# Introducción a los modelos de datos {#data-model-beta}

>[!AVAILABILITY]
>
>Para acceder a los modelos de datos, necesita uno de los siguientes permisos:
>
>-**Administrar modelo de datos federado**
>>-**Ver modelo de datos federado**
>
>Para obtener más información sobre los permisos necesarios, consulte la [guía de control de acceso](/help/governance-privacy-security/access-control.md).

## ¿Qué es un modelo de datos? {#data-model-start}

Un modelo de datos es un conjunto de esquemas, audiencias y los vínculos entre ellos. Se utiliza para federar audiencias con datos de bases de datos.

En Federated Audience Composition, puede crear y administrar modelos de datos directamente en la vista Lienzo. Esto incluye agregar esquemas y audiencias, así como definir los vínculos entre ellos en función de su caso de uso.

Más información sobre [esquemas](../customer/schemas.md#schema-start) y [audiencias](../start/audiences.md).

Por ejemplo, puede ver debajo una representación de un modelo de datos: las tablas con su nombre y los vínculos entre ellas.

![](assets/datamodel.png){zoomable="yes"}

## Creación de un modelo de datos {#data-model-create}

Para crear un modelo de datos, siga estos pasos:

1. En la sección **[!UICONTROL Datos federados]**, acceda al menú **[!UICONTROL Modelos]** y vaya a la pestaña **[!UICONTROL Modelo de datos]**.

   Seleccione el botón **[!UICONTROL Crear modelo de datos]**.

   ![](assets/datamodel_create.png){zoomable="yes"}

2. Defina el nombre de su modelo de datos y seleccione el botón **[!UICONTROL Crear]**.

3. En el panel del modelo de datos, seleccione **[!UICONTROL Agregar esquemas]** para elegir el esquema asociado con el modelo de datos.

   ![](assets/datamodel_schemas.png){zoomable="yes"}

4. Además, puede agregar audiencias al modelo de datos. Seleccione **[!UICONTROL Agregar audiencias]** para definir los grupos de destino.

   ![](assets/datamodel-audiences.png){zoomable="yes"}

5. Establezca conexiones entre las tablas del modelo de datos para garantizar relaciones de datos precisas. Para obtener más información, lea la sección [crear vínculos](#data-model-links).

6. Después de completar la configuración, selecciona **[!UICONTROL Guardar]** para aplicar los cambios.

## Crear vínculos {#data-model-links}

>[!NOTE]
>
>Si está creando un vínculo con varias uniones, solo puede utilizar la misma combinación de esquemas de origen y destino una vez.

>[!BEGINTABS]

>[!TAB Vista de tabla]

Para crear vínculos entre tablas del modelo de datos desde la pestaña de vista de tabla, siga estos pasos:

1. Seleccione el icono de ![tres puntos](/help/assets/icons/more.png) seguido de **[!UICONTROL Crear vínculo]** junto a uno de la tabla o seleccione **[!UICONTROL Crear vínculos]** dentro de la sección **[!UICONTROL Vínculos]**:

   ![](assets/datamodel_createlinks.png){zoomable="yes"}

2. Rellene el formulario proporcionado para definir el vínculo.

   ![](assets/datamodel_link.png){zoomable="yes"}

   **Cardinalidad**

   * **1-N**: una ocurrencia de la tabla de origen puede tener varias ocurrencias correspondientes de la tabla de destino, pero una ocurrencia de la tabla de destino puede tener como máximo una ocurrencia correspondiente de la tabla de origen.

   * **N-1**: una ocurrencia de la tabla de destino puede tener varias ocurrencias correspondientes de la tabla de origen, pero una ocurrencia de la tabla de origen puede tener como máximo una ocurrencia correspondiente de la tabla de destino.

   * **1-1**: una ocurrencia de la tabla de origen puede tener como máximo una ocurrencia correspondiente de la tabla de destino.

   Para crear un vínculo de unión múltiple, seleccione el icono de signo más. Ahora puede crear varias uniones entre los campos de esquema.

   ![El botón más está resaltado, lo que le permite crear un vínculo de unión múltiple para el modelo.](assets/multi-join.png){zoomable="yes"}

Todos los vínculos definidos para el modelo de datos se enumeran a continuación:

![](assets/datamodel_alllinks.png){zoomable="yes"}

>[!TAB Vista de lienzo]

Para crear vínculos entre tablas del modelo de datos desde la pestaña Vista de lienzo, siga estos pasos:

1. Acceda a la vista Lienzo del modelo de datos y elija las dos tablas que desea vincular

2. Seleccione el botón ![](assets/do-not-localize/Smock_AddCircle_18_N.svg) junto a Source Join y, a continuación, arrastre y guíe la flecha hacia Target Join para establecer la conexión.

   ![](assets/datamodel.gif){zoomable="yes"}

3. Complete el formulario proporcionado para definir el vínculo y seleccione **[!UICONTROL Aplicar]** una vez configurado.

   ![](assets/datamodel-canvas-1.png){zoomable="yes"}

   **Cardinalidad**

   * **1-N**: una ocurrencia de la tabla de origen puede tener varias ocurrencias correspondientes de la tabla de destino, pero una ocurrencia de la tabla de destino puede tener como máximo una ocurrencia correspondiente de la tabla de origen.

   * **N-1**: una ocurrencia de la tabla de destino puede tener varias ocurrencias correspondientes de la tabla de origen, pero una ocurrencia de la tabla de origen puede tener como máximo una ocurrencia correspondiente de la tabla de destino.

   * **1-1**: una ocurrencia de la tabla de origen puede tener como máximo una ocurrencia correspondiente de la tabla de destino.

4. Todos los vínculos definidos en el modelo de datos se representan como flechas en la vista de lienzo. Seleccione una flecha entre dos tablas para ver los detalles, realizar ediciones o quitar el vínculo según sea necesario.

   ![](assets/datamodel-canvas-2.png){zoomable="yes"}

5. Utilice la barra de herramientas para personalizar y ajustar el lienzo.

   ![](assets/datamodel-canvas-3.png)

   * **[!UICONTROL Aumentar]**: amplíe el lienzo para ver los detalles del modelo de datos con mayor claridad.
   * **[!UICONTROL Reducir]**: reduzca el tamaño del lienzo para obtener una vista más amplia del modelo de datos.
   * **[!UICONTROL Ajustar vista]**: ajuste el zoom para ajustar todos los esquemas y/o audiencias dentro del área visible.
   * **[!UICONTROL Alternar interactividad]**: habilita o deshabilita la interacción del usuario con el lienzo.
   * **[!UICONTROL Filtro]**: elija qué esquema desea mostrar en el lienzo.
   * **[!UICONTROL Forzar diseño automático]**: organice automáticamente los esquemas o audiencias para mejorar la organización.

>[!ENDTABS]

## Cómo realizar el vídeo {#data-model-video}

Aprenda a crear un modelo de datos en este vídeo:

>[!VIDEO](https://video.tv.adobe.com/v/3432020)
