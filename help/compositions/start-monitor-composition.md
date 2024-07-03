---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
source-git-commit: b946f8821d965fb00f79f6f5557adcfff1ee2387
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---


# Inicio y supervisión de la composición {#start-monitor}

Una vez creada la composición y diseñadas las tareas que se van a realizar en el lienzo, puede iniciarla y supervisar cómo se está ejecutando.

## Iniciar la composición {#start}

Para iniciar la maquetación, vaya a **[!UICONTROL Composiciones]** para la campaña asociada y haga clic en el **[!UICONTROL Inicio]** en la esquina superior derecha del lienzo.

Una vez que se esté ejecutando la composición, cada actividad del lienzo se ejecuta en un orden secuencial, hasta que se llega al final de la composición.

Puede realizar un seguimiento del progreso de los perfiles de destino en tiempo real mediante un flujo visual. Esto le permite identificar rápidamente el estado de cada actividad y el número de perfiles en transición entre ellas.

## Transiciones de composición {#transitions}

En las composiciones, los datos que pasan de una actividad a otra a través de transiciones se almacenan en una tabla de trabajo temporal. Estos datos se pueden mostrar para cada transición. Para ello, seleccione una transición para abrir sus propiedades en el lado derecho de la pantalla.

* Clic **[!UICONTROL Previsualizar esquema]** para mostrar el esquema de la tabla de trabajo.
* Clic **[!UICONTROL Previsualizar resultados]** para visualizar los datos transportados en la transición seleccionada.

## Monitorización de la ejecución de actividades {#activities}

Los indicadores visuales de la esquina superior derecha de cada cuadro de actividad permiten comprobar su ejecución:

| Indicador visual | Descripción |
|-----|------------|
|  | La actividad se está ejecutando. |
|  | La actividad requiere su atención. Esto puede implicar confirmar el envío de una entrega o realizar la acción necesaria. |
|  | La actividad ha encontrado un error. Para resolver el problema, abra los registros de composición para obtener más información. |
|  | La actividad se ha ejecutado correctamente. |

## Monitorización de registros y tareas {#logs-tasks}

La monitorización de los registros y tareas de las composiciones es un paso clave para analizar las composiciones y asegurarse de que se ejecutan correctamente. Se puede acceder a ellas desde **[!UICONTROL Registros]** que está disponible en la barra de herramientas de acciones y en el panel de propiedades de cada actividad.

El **[!UICONTROL Registros y tareas]** proporciona un historial de la ejecución de la maquetación, registrando todas las acciones del usuario y los errores encontrados. Este historial se guarda durante la duración especificada en la composición [opciones de ejecución](composition-settings.md). Durante esta duración, todos los mensajes se guardan, incluso después de reiniciar la composición. Si no desea guardar los mensajes de una ejecución anterior, haga clic en el **[!UICONTROL Purge history]** botón.

Hay dos tipos de información disponibles:

* El **[!UICONTROL Registro]** contiene el historial de ejecución de todas las actividades de composición. Indexa las operaciones realizadas y los errores de ejecución por orden cronológico.
* El **[!UICONTROL Tareas]** La pestaña detalla la secuencia de ejecución de las actividades.

En ambas pestañas, puede elegir las columnas mostradas y su orden, aplicar filtros y utilizar el campo de búsqueda para encontrar rápidamente la información deseada.

## Comandos de ejecución de composición {#execution-commands}

La barra de acciones de la esquina superior derecha proporciona comandos que le permiten administrar la ejecución de la composición. Puede hacer lo siguiente:

* **[!UICONTROL Inicio]** / **[!UICONTROL Reanudar]** la ejecución de la composición, que luego adquiere el estado En curso. Si la composición estaba en pausa, se reanuda, pero de lo contrario se inicia y las actividades iniciales se activan.

* **[!UICONTROL Pausar]** la ejecución de la composición, que luego adquiere el estado Paused. No se activará ninguna actividad nueva hasta que se reanude, pero las operaciones en curso no se suspenden.

* **[!UICONTROL Detener]** una composición que se está ejecutando y que luego pasará al estado Finished. Las operaciones en curso se interrumpen si es posible. No puede continuar desde la composición desde el mismo lugar en el que se detuvo.
