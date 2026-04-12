---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
exl-id: 4f510805-b700-444d-89bb-832eaa1e3242
source-git-commit: 036dcb96d2d831e3a1d6ab50afef5b87e25b564b
workflow-type: tm+mt
source-wordcount: '1603'
ht-degree: 20%

---

# Crear una composición

La composición de público federado le permite crear composiciones, donde puede aprovechar diversas actividades en un lienzo visual para crear públicos. Después de crear la composición, los públicos resultantes se guardan en Adobe Experience Platform y se pueden aprovechar en destinos de Experience Platform y Adobe Journey Optimizer para dirigirse a los clientes.

## Definir la composición {#create}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Propiedades de la composición"
>abstract="En esta pantalla, elija la plantilla que desea utilizar para crear la composición y especifique una etiqueta. Expanda la sección OPCIONES ADICIONALES para configurar más opciones, como el nombre interno de la composición, su carpeta, zona horaria y grupo de supervisores. Se recomienda encarecidamente seleccionar un grupo de supervisores para que los operadores sean alertados si se produce un error."

Para crear una composición, primero deberá definir su etiqueta y, opcionalmente, configurar ajustes adicionales.

Para crear una composición, selecciona **[!UICONTROL Audiencias]** en la sección **[!UICONTROL Cliente]**, seguido de la pestaña **[!UICONTROL Composiciones federadas]**.

![Se resalta la ruta de acceso a la sección Composiciones federadas.](assets/create/access-compositions.png)

Aparecerá la página de exploración de composiciones federadas. Seleccione **[!UICONTROL Crear composición]** para continuar con el proceso de creación de la composición.

![](assets/composition-create.png)

En la sección **[!UICONTROL Propiedades]**, especifique una etiqueta para la composición y seleccione un modelo de datos. Solo los esquemas asociados a este modelo de datos estarán disponibles en las actividades de la composición.

![](assets/composition-select-schema.png)

Seleccione **[!UICONTROL Crear]**. Se muestra el lienzo de composición. Ahora puede configurar la composición añadiendo actividades y transiciones al lienzo.

## Lienzo de composición {#canvas}

En la parte superior del lienzo, puede acceder a una barra de herramientas que proporciona opciones para administrar y navegar por las actividades.

![](assets/canvas-toolbar.png)

Las opciones disponibles incluyen:

* **[!UICONTROL Selección múltiple]**: seleccione varias actividades para eliminarlas todas a la vez o cópielas y péguelas.
* **[!UICONTROL Rotar]**: cambia el lienzo para que se muestre verticalmente.
* **[!UICONTROL Ajustar a la pantalla]**: ajusta el nivel de zoom del lienzo a la pantalla.
* **[!UICONTROL Acercar]** / **[!UICONTROL Alejar]**: Acercar o alejar el lienzo.
* **[!UICONTROL Mostrar mapa]**: abre una instantánea del lienzo en el que se muestra que se encuentra.

## Añadir actividades {#add-activities}

En el lienzo de composición, puede añadir actividades y transiciones que ayuden a definir la audiencia. Las actividades permiten *definir* los componentes de la audiencia, mientras que las transiciones permiten *organizar* el flujo de la composición.

Para obtener más información acerca de las actividades y transiciones disponibles para usar, lea [información general sobre actividades](./activities.md).

## Administrar actividades {#manage-activities}

Puede realizar operaciones en las actividades agregadas dentro del panel de propiedades.

![](assets/activity-actions.png)

Las opciones incluyen:

* **[!UICONTROL Eliminar]**: elimine la actividad del lienzo.
* **[!UICONTROL Disable]/[!UICONTROL Enable]**: Disable or enable the activity. When the composition is executed, disabled activities and the following activities on the same path are not executed and the composition is stopped.
* **[!UICONTROL Pause]/[!UICONTROL Resume]**: Pause or resume the activity. When the composition is executed, it pauses at the paused activity. No se ejecutará la tarea correspondiente ni las que la siguen en la misma ruta.
* **[!UICONTROL Copy]**: Copies the activity to paste it at another location in the composition. To do this, select the **+** button on a transition and select **[!UICONTROL Paste X activity]**. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configure **[!UICONTROL Execution options]** for the selected activity. Available execution options include the following:
  +++Available execution options

  The **[!UICONTROL Properties]** section allows you to configure generic settings regarding the execution of the activity:

   * **[!UICONTROL Execution]**: Define the action to be carried out when the is started.
   * **[!UICONTROL Maximum execution duration]**: Specify a duration such as &quot;30s&quot; or &quot;1h&quot;. If the activity is not finished after the duration specified has been elapsed, an alert is triggered. This has no impact on how the composition functions.
   * **[!UICONTROL Time zone]**: Select the time zone of the activity. Federated Audience Composition allows you to manage the time differences between multiple countries on the same instance. The setting applied is configured when the instance is created.
   * **[!UICONTROL Affinity]**: Force the composition activity to execute on a particular machine. To do this, you must specify one or several affinities for the activity in question.
   * **[!UICONTROL Behavior]**: Define the procedure to follow if asynchronous tasks are used.

  The **[!UICONTROL Error management]** section allows you to specify the action to be carried out should the activity encounter an error.

  The **[!UICONTROL Initialization script]** section lets you initialize variables or modify activity properties. Select the **[!UICONTROL Edit code]** button and type the snippet of code to execute. The script is called when the activity executes.

  +++
* **Logs and tasks**: View the logs and tasks for the selected activity.

## Inicie y monitorice su composición {#start-and-monitor}

Cuando haya terminado de agregar las actividades a la composición, puede iniciar la ejecución de la composición. Para iniciar una composición, seleccione el botón **[!UICONTROL Iniciar]** en la esquina superior derecha de la pantalla.

![](assets/execution-actions.png)

| Acción | Descripción |
| ------ | ----------- |
| **Start** | Inicia la ejecución de la composición y la mueve al estado **En curso**. |
| **Pause** | Pausa la ejecución de la composición y la establece en el estado **Paused**. No se activarán nuevas actividades hasta que se reanude la composición, pero las operaciones en curso **no** se suspenderán. |
| **Reanudar** | Reanuda la ejecución de la composición en pausa y la establece en el estado **En curso**. |
| **Stop** | Detiene la ejecución de la composición y la establece en el estado **Finalizado**. Usted **no puede** reanudar la composición desde el mismo lugar desde el que se detuvo. |
| **Restart** | Detiene y reinicia la ejecución de la composición. |

Cuando se está ejecutando la composición, cada actividad del lienzo se ejecuta en un orden secuencial, hasta que se llega al final de la composición. Puede realizar un seguimiento del progreso de los perfiles de destino en tiempo real mediante un flujo visual. Esto le permite identificar rápidamente el estado de cada actividad y el número de perfiles en transición entre ellas.

![](assets/composition-visual-flow.png)

Los indicadores visuales de la esquina superior derecha de cada actividad muestran el estado de la ejecución:

| Indicador visual | Descripción |
| ---------------- | ------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | La actividad se está ejecutando actualmente. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | La actividad requiere su atención. Esto puede implicar confirmar el envío de una entrega o tomar las medidas necesarias. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | La actividad ha encontrado un error. Para resolver el problema, abra los registros de composición para obtener más información. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | La actividad se ha ejecutado correctamente. |

### Monitorizar registros y tareas {#monitor-logs}

Además, puede ver los registros de composición para asegurarse de que se ejecutan correctamente. Seleccione **[!UICONTROL Registros]** en la barra de herramientas de acciones para ver esta información.

![](assets/logs-button.png)

Aparecerá la pantalla **[!UICONTROL Registros de composición y tareas]**. Esto proporciona un historial de la ejecución de la maquetación, registrando todas las acciones del usuario y los errores encontrados.

El historial se organiza en varias pestañas, que se detallan a continuación:

* La pestaña **[!UICONTROL Log]** contiene el historial de ejecución de todas las actividades de composición. Indexa las operaciones realizadas y los errores de ejecución por orden cronológico.
* La ficha **[!UICONTROL Tareas]** detalla la secuencia de ejecución de las actividades. El botón situado al final de cada tarea le permite enumerar las variables de evento que pasan a través de la actividad.
* La ficha **[!UICONTROL Variables]** enumera todas las variables pasadas en la composición. Está disponible al acceder a los registros y tareas solo desde el lienzo de composición. Ahora está disponible al acceder a los registros desde el panel de propiedades de una actividad.

![](assets/logs-tasks.png)

En todas las pestañas, puede elegir las columnas mostradas y su orden, aplicar filtros y utilizar el campo de búsqueda para encontrar rápidamente la información deseada.

### Suscribirse a alertas {#alerts}

También puede suscribirse a alertas para recibir notificaciones si las ejecuciones de composición federada se han realizado correctamente o no.

Para suscribirse a las alertas, seleccione el ![icono de notificación](/help/assets/icons/bell.png), seguido del ![icono de configuración](/help/assets/icons/settings.png).

![Se resaltan tanto la notificación como los iconos de configuración.](assets/monitor/select-notifications.png){zoomable="yes"}{width="70%"}

Se muestra la página de configuración de notificaciones. En esta página, seleccione **[!UICONTROL Experience Platform]** y elija los canales de alertas que desee. Para ver las notificaciones dentro de la interfaz de usuario, selecciona **[!UICONTROL En la aplicación]**.

![La casilla de verificación en la aplicación está seleccionada en la sección Experience Platform.](assets/monitor/add-alerts.png){zoomable="yes"}{width="50%"}

Con **[!UICONTROL En la aplicación]** seleccionada, se le notificará de los errores y las ejecuciones de composición.

![Se muestran las alertas, que muestran los errores y los aciertos de composición.](assets/monitor/view-alerts.png){zoomable="yes"}{width="70%"}

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

Al acceder a una composición, puede acceder a ajustes avanzados que le permiten, por ejemplo, definir cómo debe comportarse la composición en caso de error.

Para acceder a estas opciones adicionales, seleccione **[!UICONTROL Configuración]** en la sección superior de la pantalla de creación de la composición.

![](assets/composition-create-settings.png)

| Configuración | Descripción |
| -------- | ----------- |
| **[!UICONTROL Etiqueta]** | Actualice el nombre dado a la composición. |
| **[!UICONTROL Mantener el resultado de las poblaciones provisionales entre dos ejecuciones]** | Si esta opción está activada, las tablas de trabajo se conservarán incluso después de ejecutar la composición. De forma predeterminada, solo se conservan las tablas de trabajo de la última ejecución de la composición. Las tablas de trabajo de ejecuciones anteriores se eliminan a diario. Solo debe habilitar esta configuración en un entorno de ensayo o desarrollo. **nunca** debe habilitar esta configuración en un entorno de producción. |
| **[!UICONTROL Administración de errores]** | Define las acciones realizadas si la composición tiene un error. Hay tres opciones posibles: <ul><li>**[!UICONTROL Suspender el proceso]**: la composición se pone en pausa automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reanude la composición con los botones **[!UICONTROL Reanudar]**.</li><li>**[!UICONTROL Ignorar]**: El estado de la tarea que activó el error cambia a **[!UICONTROL Fallido]**, pero la composición mantiene el estado **[!UICONTROL Iniciado]**.</li><li>**[!UICONTROL Anular el proceso]**: la composición se detiene automáticamente y su estado cambia a **[!UICONTROL Error]**. Una vez resuelto el problema, reinicie la composición con el botón **[!UICONTROL Iniciar]**.</li></ul> |
| **[!UICONTROL Consecutive errors]** | Especifique el número de errores que se pueden omitir antes de que se detenga el proceso. Una vez alcanzado este número, el estado de la composición cambia a **[!UICONTROL Failed]**. Si el valor de este campo es 0, la composición nunca se detendrá, independientemente del número de errores. |
