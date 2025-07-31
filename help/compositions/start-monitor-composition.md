---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
exl-id: 1f288312-dd6a-4a62-8ee6-fa2417954d5c
source-git-commit: 59d7d112421e0ff207ce76122593a111ad9c6cc7
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 8%

---

# Inicie y monitorice su composición {#start-monitor}

Una vez creada la composición y diseñadas las tareas que se van a realizar en el lienzo, puede iniciarla y supervisar cómo se está ejecutando.

## Iniciar la composición {#start}

Para iniciar una composición, haga clic en el botón **[!UICONTROL Iniciar]** en la esquina superior derecha de la pantalla. Cuando se está ejecutando la composición, cada actividad del lienzo se ejecuta en un orden secuencial, hasta que se llega al final de la composición.

Puede realizar un seguimiento del progreso de los perfiles de destino en tiempo real mediante un flujo visual. Esto le permite identificar rápidamente el estado de cada actividad y el número de perfiles en transición entre ellas.

![](assets/composition-visual-flow.png)

## Transiciones de composición {#transitions}

En las composiciones, los datos que pasan de una actividad a otra a través de transiciones se almacenan en una tabla de trabajo temporal. Estos datos se pueden mostrar para cada transición. Para ello, seleccione una transición para abrir sus propiedades en el lado derecho de la pantalla.

* Haga clic en **[!UICONTROL Vista previa del esquema]** para mostrar el esquema de la tabla de trabajo.
* Haga clic en **[!UICONTROL Previsualizar resultados]** para visualizar los datos transportados en la transición seleccionada. Esta opción solo está disponible si la opción **[!UICONTROL Keep the result of interim populations between two executions]** está habilitada. [Más información](create-composition.md#settings).

![](assets/transition-preview.png)

## Monitorización de la ejecución de actividades {#activities}

Los indicadores visuales de la esquina superior derecha de cada cuadro de actividad permiten comprobar su ejecución:

| Indicador visual | Descripción |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | La actividad se está ejecutando actualmente. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | La actividad requiere su atención. Esto puede implicar confirmar el envío de una entrega o tomar las medidas necesarias. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | La actividad ha encontrado un error. Para resolver el problema, abra los registros de composición para obtener más información. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | La actividad se ha ejecutado correctamente. |

## Monitorización de registros y tareas {#logs-tasks}

La monitorización de los registros y tareas de las composiciones es un paso clave para analizar las composiciones y asegurarse de que se ejecutan correctamente. Se puede acceder a ellos desde el botón **[!UICONTROL Registros]**, que está disponible en la barra de herramientas de acciones y en el panel de propiedades de cada actividad.

![](assets/logs-button.png)

La pantalla **[!UICONTROL Registros de composición y tareas]** proporciona un historial de la ejecución de la composición, registrando todas las acciones del usuario y los errores encontrados.

<!-- à confirmer, pas trouvé dans les options = The workflow history is saved for the duration specified in the workflow execution options. During this duration, all the messages are therefore saved, even after a restart. If you do not want to save the messages from a previous execution, you have to purge the history by clicking the ![](assets/delete_darkgrey-24px.png) button.-->

El historial se organiza en varias pestañas, que se detallan a continuación:

* La pestaña **[!UICONTROL Log]** contiene el historial de ejecución de todas las actividades de composición. Indexa las operaciones realizadas y los errores de ejecución por orden cronológico.
* La ficha **[!UICONTROL Tareas]** detalla la secuencia de ejecución de las actividades. El botón situado al final de cada tarea le permite enumerar las variables de evento que pasan a través de la actividad.
* La ficha **[!UICONTROL Variables]** enumera todas las variables pasadas en la composición. Está disponible al acceder a los registros y tareas solo desde el lienzo de composición. Ahora está disponible al acceder a los registros desde el panel de propiedades de una actividad.  <!-- à confirmer-->

![](assets/logs-tasks.png)

En todas las pestañas, puede elegir las columnas mostradas y su orden, aplicar filtros y utilizar el campo de búsqueda para encontrar rápidamente la información deseada.

## Suscribirse a alertas {#alerts}

Además, puede suscribirse a alertas para recibir notificaciones si las ejecuciones de composición federada se han realizado correctamente o no.

Para suscribirse a las alertas, seleccione el ![icono de notificación](/help/assets/icons/bell.png), seguido del ![icono de configuración](/help/assets/icons/settings.png).

![Se resaltan tanto la notificación como los iconos de configuración.](assets/monitor/select-notifications.png){zoomable="yes"}{width="70%"}

Se muestra la página de configuración de notificaciones. En esta página, seleccione **[!UICONTROL Experience Platform]** y elija los canales de alertas que desee. Para ver las notificaciones dentro de la interfaz de usuario, selecciona **[!UICONTROL En la aplicación]**.

![La casilla de verificación en la aplicación está seleccionada en la sección Experience Platform.](assets/monitor/add-alerts.png){zoomable="yes"}{width="50%"}

Con **[!UICONTROL En la aplicación]** seleccionada, se le notificará de los errores y las ejecuciones de composición.

![Se muestran las alertas, que muestran los errores y los aciertos de composición.](assets/monitor/view-alerts.png){zoomable="yes"}{width="70%"}

## Comandos de ejecución de composición {#execution-commands}

La barra de acciones de la esquina superior derecha proporciona comandos que le permiten administrar la ejecución de la composición.

![](assets/execution-actions.png)

Las acciones disponibles son:

* **[!UICONTROL Start]**: inicia la ejecución de la composición, que luego adquiere el estado **[!UICONTROL In progress]**. La composición se inicia y se activan las actividades iniciales.

* **[!UICONTROL Reanudar]**: Reanuda la ejecución de la composición que se había pausado. La composición adquiere el estado **[!UICONTROL En curso]**.

* **[!UICONTROL Pausar]** la ejecución de la composición, que luego adquiere el estado **[!UICONTROL Pausado]**. No se activará ninguna actividad nueva hasta que se reanude, pero las operaciones en curso no se suspenden.

* **[!UICONTROL Detener]** una composición que se está ejecutando y que luego adquirirá el estado **[!UICONTROL Finalizado]**. Las operaciones en curso se interrumpen si es posible. No puede continuar desde la composición desde el mismo lugar en el que se detuvo.

* **[!UICONTROL Restart]**: detiene y reinicia una composición. En la mayoría de los casos, esto le permite reiniciarse más rápido, ya que la detención lleva una cierta cantidad de tiempo, y el botón **[!UICONTROL Iniciar]** solo está disponible cuando la detención es efectiva.

