---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
badge: label="Disponibilidad limitada" type="Informative"
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: bd3223a77f490a43487e21662d8f766d4f9b06fc
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 22%

---

# Crear y configurar la composición {#create}

El primer paso para crear una composición es definir su etiqueta y configurar ajustes adicionales si es necesario.

## Creación de la composición {#create-the-composition}

1. Acceda al menú **[!UICONTROL Audiencias]** y seleccione la pestaña **[!UICONTROL Composiciones federadas]**.

1. Haga clic en el botón **[!UICONTROL Crear composición]**.

   ![](assets/composition-create.png)

1. En la sección **[!UICONTROL Propiedades]**, especifique una etiqueta para la composición y seleccione un modelo de datos. Solo los esquemas asociados a este modelo de datos estarán disponibles en las actividades de la composición.

   ![](assets/composition-select-schema.png)

1. Haga clic en **[!UICONTROL Crear]**. Se muestra el lienzo de composición. Ahora puede configurar la composición agregando tantas actividades como sea necesario para adaptarlas a sus necesidades antes de ejecutarla:

   * [Aprenda a organizar actividades](orchestrate-activities.md)
   * [Aprenda a iniciar y supervisar una composición](start-monitor-composition.md)

## Configuración de los ajustes de la composición {#settings}

>[!CONTEXTUALHELP]
>id="dc_composition_settings_properties"
>title="Propiedades de la composición"
>abstract="En esta sección se proporcionan propiedades genéricas de composición a las que también se puede acceder al crear la composición."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_segmentation"
>title="Segmentación de composición"
>abstract="De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la composición. Puede habilitar esta opción para conservar las tablas de trabajo con fines de prueba. Debe usarse **solamente** en entornos de ensayo o de desarrollo. Nunca se debe marcar en un entorno de producción."

>[!CONTEXTUALHELP]
>id="dc_composition_settings_error"
>title="Configuración de la administración de errores"
>abstract="En esta sección, puede definir cómo administrar los errores durante la ejecución. Puede optar por poner en pausa el proceso, ignorar un determinado número de errores o detener la ejecución de la composición."

Al acceder a una composición, puede acceder a ajustes avanzados que le permiten, por ejemplo, definir cómo debe comportarse la composición en caso de error. Para acceder a estas opciones adicionales, haga clic en el botón **[!UICONTROL Configuración]** ubicado en la sección superior de la pantalla de creación de la composición.

![](assets/composition-create-settings.png)

Los ajustes disponibles son los siguientes:

* **[!UICONTROL Etiqueta]**: cambie la etiqueta de la composición.

* **[!UICONTROL Mantener el resultado de poblaciones provisionales entre dos ejecuciones]**: De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la composición. Las tablas de trabajo de ejecuciones anteriores se depuran mediante una composición técnica que se ejecuta diariamente.

  Si esta opción está activada, las tablas de trabajo se conservarán incluso después de ejecutar la composición. Puede utilizarlo con fines de prueba y, por lo tanto, **solo** debe usarse en entornos de ensayo o desarrollo. Nunca se debe comprobar en una composición de producción.

* **[!UICONTROL Gestión de errores]**: Esta opción le permite definir las acciones que deben realizarse si una actividad de composición tiene errores. Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: la composición se pone en pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la composición con los botones **[!UICONTROL Reanudar]**.
   * **[!UICONTROL Ignorar]**: El estado de la tarea que activó el error cambia a **[!UICONTROL Fallido]**, pero la composición mantiene el estado **[!UICONTROL Iniciado]**.
   * **[!UICONTROL Anular el proceso]**: la composición se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la composición con el botón **[!UICONTROL Iniciar]**.

* **[!UICONTROL Errores consecutivos]**: especifique el número de errores que se pueden omitir antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la composición cambia a **[!UICONTROL Failed]**. Si el valor de este campo es 0, la composición nunca se detendrá, independientemente del número de errores.
