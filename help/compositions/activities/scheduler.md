---
audience: end-user
title: Uso de la actividad Planificador
description: Descubra más información sobre cómo utilizar la actividad Planificador
source-git-commit: 7f73f5f81561fabe6f4ef2ff77f13d386a7927b3
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 26%

---


# Planificador {#scheduler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_scheduler"
>title="Actividad planificador"
>abstract="La actividad **Planificador** le permite programar cuándo comienza la composición de la audiencia. La actividad debe considerarse como un inicio programado. Solo puede utilizarse como primera actividad de una composición."

La actividad **Scheduler** es una actividad **Flow control**. Permite programar cuándo se inicia la composición. La actividad debe considerarse como un inicio programado. Solo puede utilizarse como primera actividad de la composición.

## Configure la actividad Planificador {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_validity"
>title="Validez del planificador"
>abstract="Puede definir un período de validez para el planificador. Puede ser permanente (predeterminado) o válido hasta una fecha específica."

>[!CONTEXTUALHELP]
>id="dc_orchestration_schedule_options"
>title="Opciones del planificador"
>abstract="Defina la frecuencia del planificador. Se puede ejecutar en un momento específico, una o varias veces al día, a la semana o al mes."

Siga estos pasos para configurar la actividad **Planificador**:

1. Agregue una actividad **Planificador** a su composición.

1. Configure **Frecuencia de ejecución**:

   * **Una vez**: la composición se ejecuta una sola vez.

   * **Diario**: la composición se ejecuta a una hora específica una vez al día.

   * **Varias veces al día:** la composición se ejecuta regularmente varias veces al día. Puede configurar ejecuciones en momentos específicos o de forma periódica.

     >[!NOTE]
     >
     >No programe una composición para que se ejecute durante más de 15 minutos, ya que podría limitar el rendimiento general del sistema y crear bloques en la base de datos.

   * **Semanal**: la composición se ejecuta en un momento determinado una o varias veces a la semana.

   * **Mensual**: la composición se ejecuta en un momento determinado una o varias veces al mes. Puede seleccionar meses cuando necesite que se ejecute la composición. También puede configurar ejecuciones en días de semana del mes específicos, como el segundo martes de mes.

1. Defina los detalles de ejecución según la frecuencia seleccionada. Los campos de detalle pueden variar según la frecuencia utilizada (tiempo, frecuencia de repetición, días especificados, etc.).

1. Haga clic en **Previsualizar horas de inicio** para comprobar la programación de las siguientes diez ejecuciones de la composición.

1. Defina el periodo de validez del planificador:

   * **Permanente (nunca caduca)**: la composición se ejecuta según la frecuencia especificada, sin límites en el lapso de tiempo ni número de iteraciones.

   * **Período de validez**: la composición se ejecuta según la frecuencia especificada, hasta una fecha específica. Debe especificar las fechas de inicio y finalización.

>[!NOTE]
>
>Si desea iniciar la composición de inmediato, puede hacer clic en **Ejecutar tarea pendiente** en la barra de acciones superior del planificador. Este botón sólo está disponible cuando se ha iniciado la composición.

<!--## Example{#scheduler-example}

In the following example, the activity is configured so that the composition runs several times a day at 9 and 12 AM, every day of the week from October 1st, 2023 to January 1st, 2024.-->

