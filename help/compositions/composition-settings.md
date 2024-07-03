---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 2%

---


# Configurar los ajustes de la composición {#settings}

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

Al acceder a una composición, puede acceder a ajustes avanzados que le permiten, por ejemplo, definir cómo debe comportarse la composición en caso de error o gestionar el retraso tras el cual debe depurarse el historial de la composición.

Para acceder a las opciones adicionales de la composición, haga clic en **Configuración** situado encima del lienzo.

![](assets/composition-create-settings.png)

Los ajustes disponibles son los siguientes:

* **[!UICONTROL Etiqueta]**: cambie la etiqueta de la composición.

* **[!UICONTROL Mantener el resultado de poblaciones provisionales entre dos ejecuciones]**: De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la composición. Las tablas de trabajo de ejecuciones anteriores se depuran mediante una composición técnica que se ejecuta diariamente.

  Si esta opción está activada, las tablas de trabajo se conservarán incluso después de ejecutar la composición. Puede utilizarlo con fines de prueba y, por lo tanto, debe utilizarlo **solamente** en entornos de ensayo o desarrollo. Nunca se debe comprobar en una composición de producción.

* **[!UICONTROL Administración de errores]**: Esta sección permite definir las acciones que se deben realizar si una actividad de composición presenta errores. Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: la composición se pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la composición con el **[!UICONTROL Reanudar]** botones.
   * **[!UICONTROL Ignorar]**: el estado de la tarea que activó el error cambia a **[!UICONTROL Error]**, pero la composición mantiene el **[!UICONTROL Iniciado]** estado.
   * **[!UICONTROL Anular el proceso]**: la composición se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la composición con el **[!UICONTROL Inicio]** botón.

* **[!UICONTROL Consecutive errors]**: especifique el número de errores que se pueden ignorar antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la composición cambia a **[!UICONTROL Error]**. Si el valor de este campo es 0, la composición nunca se detendrá, independientemente del número de errores.
