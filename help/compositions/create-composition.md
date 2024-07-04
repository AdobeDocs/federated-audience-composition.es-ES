---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
source-git-commit: be24c32977cdccab0a5fc7e77a033f4d2b746b9f
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 2%

---


# Crear y configurar la composición {#create}

El primer paso para crear una composición es definir su etiqueta y configurar ajustes adicionales si es necesario.

## Creación de la composición {#create-the-composition}

1. Acceda a la **[!UICONTROL Audiencias]** y seleccione la opción **[!UICONTROL Composiciones federadas]** pestaña.

1. Haga clic en **[!UICONTROL Crear composición]** botón.

   ![](assets/composition-create.png)

1. En el **[!UICONTROL Propiedades]** , especifique una etiqueta para la composición y haga clic en **[!UICONTROL Crear]**.

1. Se muestra el lienzo de composición. Ahora puede configurar la composición agregando tantas actividades como sea necesario para adaptarlas a sus necesidades antes de ejecutarla:

   * [Aprenda a organizar actividades](#action-activities)
   * [Obtenga información sobre cómo iniciar y supervisar una composición](#save)

## Configurar los ajustes de la composición {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Propiedades de composición"
>abstract="En esta sección se proporcionan propiedades de composición genéricas a las que también se puede acceder al crear la composición."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Segmentación de composición"
>abstract="De forma predeterminada, sólo se conservan las tablas de trabajo de la última ejecución de la composición. Puede activar esta opción para mantener las tablas de trabajo con fines de prueba. Debe usarse. **solamente** en entornos de ensayo o desarrollo. Nunca se debe comprobar en un entorno de producción."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Configuración de la administración de errores"
>abstract="En esta sección, puede definir cómo administrar los errores durante la ejecución. Puede optar por pausar el proceso, omitir un determinado número de errores o detener la ejecución de la composición."

Al acceder a una composición, puede acceder a ajustes avanzados que le permiten, por ejemplo, definir cómo debe comportarse la composición en caso de error.

Para acceder a las opciones adicionales de la composición, haga clic en **Configuración** situado en la sección superior de la pantalla de creación de la composición.

![](assets/composition-create-settings.png)

Los ajustes disponibles son los siguientes:

* **[!UICONTROL Etiqueta]**: cambie la etiqueta de la composición.

* **[!UICONTROL Mantener el resultado de poblaciones provisionales entre dos ejecuciones]**: De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la composición. Las tablas de trabajo de ejecuciones anteriores se depuran mediante una composición técnica que se ejecuta diariamente.

  Si esta opción está activada, las tablas de trabajo se conservarán incluso después de ejecutar la composición. Puede utilizarlo con fines de prueba y, por lo tanto, debe utilizarlo **solamente** en entornos de ensayo o desarrollo. Nunca se debe comprobar en una composición de producción.

* **[!UICONTROL Administración de errores]**: Esta opción permite definir las acciones que se deben realizar si una actividad de maquetación presenta errores. Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: la composición se pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la composición con el **[!UICONTROL Reanudar]** botones.
   * **[!UICONTROL Ignorar]**: el estado de la tarea que activó el error cambia a **[!UICONTROL Error]**, pero la composición mantiene el **[!UICONTROL Iniciado]** estado.
   * **[!UICONTROL Anular el proceso]**: la composición se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la composición con el **[!UICONTROL Inicio]** botón.

* **[!UICONTROL Consecutive errors]**: especifique el número de errores que se pueden ignorar antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la composición cambia a **[!UICONTROL Error]**. Si el valor de este campo es 0, la composición nunca se detendrá, independientemente del número de errores.
