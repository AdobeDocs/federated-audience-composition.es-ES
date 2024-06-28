---
audience: end-user
title: Introducción a las composiciones
description: Aprenda a empezar con composiciones
source-git-commit: 8f4242b02f2cd135bf4adc3a69db08fe1f812e4e
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 9%

---

# Introducción a las composiciones {#compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Propiedades de composición"
>abstract="En esta sección se proporcionan propiedades de composición genéricas a las que también se puede acceder al crear la composición."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Segmentación de composición"
>abstract="De forma predeterminada, sólo se conservan las tablas de trabajo de la última ejecución de la composición. Puede activar esta opción para mantener las tablas de trabajo con fines de prueba. Debe usarse. **solamente** en entornos de ensayo o desarrollo. Nunca se debe comprobar en un entorno de producción."




## ¿Qué es una composición? {#compositions-start}


>[!CONTEXTUALHELP]
>id="dc_workflow_list"
>title="Composiciones"
>abstract="En esta pantalla, puede acceder a la lista completa de composiciones, comprobar su estado actual, las fechas de última/siguiente ejecución y crear una nueva composición."


## Configuración de la administración de errores  {#error-settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Configuración de la administración de errores"
>abstract="En esta sección, puede definir cómo administrar los errores durante la ejecución. Puede optar por pausar el proceso, omitir un determinado número de errores o detener la ejecución de la composición."

* **[!UICONTROL Administración de errores]**: Este campo permite definir las acciones que se deben realizar si una actividad de maquetación presenta errores.
Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: la composición se pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la composición con el **[!UICONTROL Reanudar]** botones.
   * **[!UICONTROL Ignorar]**: el estado de la tarea que activó el error cambia a **[!UICONTROL Error]**, pero la composición mantiene el **[!UICONTROL Iniciado]** estado.
   * **[!UICONTROL Anular el proceso]**: la composición se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la composición con el **[!UICONTROL Inicio]** botón.

* **[!UICONTROL Consecutive errors]**: este campo está disponible cuando la variable **[!UICONTROL Ignorar]** El valor está seleccionado en **[!UICONTROL En caso de errores]** field. Puede especificar el número de errores que se pueden omitir antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la composición cambia a **[!UICONTROL Error]**. Si el valor de este campo es 0, la composición nunca se detendrá, independientemente del número de errores.
