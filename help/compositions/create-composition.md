---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
source-git-commit: 194ae763f5040f11eba0fe30aa302064f5d0606a
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 9%

---


# Crear y ejecutar una composición {#create-compositions}

>[!CONTEXTUALHELP]
>id="dc_workflow_creation_properties"
>title="Propiedades del flujo de trabajo"
>abstract="En esta pantalla, elija la plantilla que desea utilizar para crear el flujo de trabajo y especifique una etiqueta. Expanda la sección OPCIONES ADICIONALES para configurar más opciones, como el nombre interno del flujo de trabajo, su carpeta, zona horaria y grupo de supervisores. Se recomienda encarecidamente seleccionar un grupo de supervisores para que los operadores sean alertados si se produce un error."

## Creación de la composición {#create}

Para crear una composición, siga estos pasos:

1. Acceda a la **[!UICONTROL Audiencias]** y seleccione la opción **[!UICONTROL Composiciones federadas]** pestaña.

1. Haga clic en **[!UICONTROL Crear composición]** botón.

1. En el **[!UICONTROL Propiedades]** , especifique una etiqueta para la composición y haga clic en **[!UICONTROL Crear]**.

1. Se muestra el lienzo de composición. Ahora puede configurar la composición agregando tantas actividades como sea necesario para adaptarlas a sus necesidades antes de ejecutarla. También se pueden configurar ajustes adicionales, como la etiqueta de la maquetación u opciones relacionadas con la gestión de errores durante la ejecución de la maquetación.

Obtenga más información en estas secciones:

* [Configurar los ajustes de la composición](#starting-audience)
* [Añadir actividades](#action-activities)
* [Ejecutar la composición y supervisar su ejecución](#save)

## Configurar los ajustes de la composición {#settings}

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_properties"
>title="Propiedades de composición"
>abstract="En esta sección se proporcionan propiedades de composición genéricas a las que también se puede acceder al crear la composición."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_segmentation"
>title="Segmentación de composición"
>abstract="De forma predeterminada, sólo se conservan las tablas de trabajo de la última ejecución de la composición. Puede activar esta opción para mantener las tablas de trabajo con fines de prueba. Debe usarse. **solamente** en entornos de ensayo o desarrollo. Nunca se debe comprobar en un entorno de producción."

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_error"
>title="Configuración de la administración de errores"
>abstract="En esta sección, puede definir cómo administrar los errores durante la ejecución. Puede optar por pausar el proceso, omitir un determinado número de errores o detener la ejecución de la composición."

Haga clic en **Configuración** para acceder a opciones adicionales para la maquetación:

* **[!UICONTROL Etiqueta]**: cambie la etiqueta de la composición.

* **[!UICONTROL Mantener el resultado de poblaciones provisionales entre dos ejecuciones]**: De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la composición. Las tablas de trabajo de ejecuciones anteriores se depuran mediante un flujo de trabajo técnico, que se ejecuta diariamente.

  Si esta opción está activada, las tablas de trabajo se conservarán incluso después de ejecutar la composición. Puede utilizarlo con fines de prueba y, por lo tanto, debe utilizarlo **solamente** en entornos de ensayo o desarrollo. Nunca se debe comprobar en un flujo de trabajo de producción.

* **[!UICONTROL Administración de errores]**: Esta sección permite definir las acciones que se deben realizar si una actividad de composición presenta errores. Hay tres opciones posibles:

   * **[!UICONTROL Suspender el proceso]**: la composición se pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la composición con el **[!UICONTROL Reanudar]** botones.
   * **[!UICONTROL Ignorar]**: el estado de la tarea que activó el error cambia a **[!UICONTROL Error]**, pero la composición mantiene el **[!UICONTROL Iniciado]** estado.
   * **[!UICONTROL Anular el proceso]**: la composición se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la composición con el **[!UICONTROL Inicio]** botón.

* **[!UICONTROL Consecutive errors]**: especifique el número de errores que se pueden ignorar antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la composición cambia a **[!UICONTROL Error]**. Si el valor de este campo es 0, la composición nunca se detendrá, independientemente del número de errores.

## Añadir actividades {#activities}

El lienzo de composición le permite configurar para que añada tantas actividades como sea necesario en la composición para adaptarlas a sus necesidades.

Para ello, haga clic en el botón + de la ruta de composición y añada la actividad deseada. Se abre el panel derecho, que le permite configurar la actividad recién agregada. [Obtenga más información sobre las actividades en composiciones y cómo configurarlas](../compositions/activities/about-activities.md)

Para quitar una actividad del lienzo, selecciónela y haga clic en el botón eliminar en el panel derecho. Si la actividad que desea eliminar es una actividad principal de otras actividades de la composición, se muestra un mensaje que le permite especificar si desea eliminar sólo la actividad seleccionada o todas sus actividades secundarias.

## Ejecutar la composición {#execute}

Una vez que la composición esté lista, haga clic en **[!UICONTROL Inicio]** para ejecutarlo y guardar las audiencias resultantes en Adobe Experience Platform. &quot;Puede monitorizar la ejecución del flujo de trabajo mediante el **Registros** botón. Hay tres pestañas disponibles para ayudarle a monitorizar la ejecución:

* **[!UICONTROL Registros]**:
* **[!UICONTROL Tareas]**:
* **[!UICONTROL Variables]**:
