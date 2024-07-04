---
audience: end-user
title: Uso de la actividad Consulta incremental
description: Aprenda a utilizar la actividad Consulta incremental
hide: true
hidefromtoc: true
source-git-commit: 13e7e75fe1dc175fce9464fa58c7a50b5e6107d4
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 24%

---

# Consulta incremental {#incremental-query}

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Consulta incremental"
>abstract="El **Consulta incremental** Esta actividad le permite consultar la base de datos utilizando el modelador de consultas. Cada vez que se ejecuta esta actividad, se excluyen los resultados de las ejecuciones anteriores. Esto permite buscar solo elementos nuevos."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Historial de consultas incrementales"
>abstract="Historial de consultas incrementales"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Datos procesados de consulta incremental"
>abstract="Datos procesados de consulta incremental"

El **Consulta incremental** esta actividad le permite consultar la base de datos de forma programada. Cada vez que se ejecuta esta actividad, se excluyen los resultados de las ejecuciones anteriores. Esto permite buscar solo elementos nuevos.

El **[!UICONTROL Consulta incremental]** la actividad se puede utilizar para varios tipos de usos:

* Segmentación de individuos para definir el destinatario de un mensaje, la audiencia, etc.
* Exportación de datos. Por ejemplo, puede utilizar la actividad para exportar con regularidad nuevos registros en los archivos. Puede resultar útil si desea utilizar los datos de registro en herramientas externas de sistema de informes o BI.

La población objetivo de ejecuciones anteriores se almacena en la composición. Esto significa que dos composiciones iniciadas a partir de la misma plantilla no comparten el mismo registro. Sin embargo, dos tareas basadas en la misma consulta incremental en la misma composición utilizan el mismo registro.

Si el resultado de una consulta incremental es igual a 0 durante una de sus ejecuciones, la composición se detiene hasta la siguiente ejecución programada de la consulta. Por lo tanto, las transiciones y actividades que siguen a la consulta incremental no se procesan antes de la siguiente ejecución.

## Configuración de la actividad Consulta incremental {#incremental-query-configuration}

Siga estos pasos para configurar el **Consulta incremental** actividad:

1. Añadir un **Consulta incremental** actividad en la composición.

1. En el **[!UICONTROL Audiencia]** , seleccione la **Dimensión de segmentación** luego haga clic en **[!UICONTROL Continuar]**.

   La dimensión de segmentación permite definir la población a la que se dirige la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, el objetivo se selecciona en los destinatarios. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->

1. Utilice el modelador de consultas para definir la consulta, del mismo modo que crea una audiencia al diseñar un nuevo correo electrónico. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. En el **[!UICONTROL Datos procesados]** , seleccione el modo incremental que desea utilizar:

   * **[!UICONTROL Excluir resultados de ejecución anterior]**: Cada vez que se ejecuta la actividad, se excluyen los resultados de las ejecuciones anteriores.

     Los registros ya segmentados en ejecuciones anteriores se pueden registrar un número máximo de días desde el día en que fueron segmentados. Para ello, utilice el **[!UICONTROL Historial en días]** field. Si este valor es cero, los destinatarios nunca se eliminan del registro.

   * **[!UICONTROL Usar un campo de fecha]**: Esta opción permite excluir los resultados de ejecuciones anteriores en función de un campo de fecha específico. Para ello, elija el campo de fecha deseado de la lista de atributos disponibles para la dimensión de segmentación seleccionada. En las siguientes ejecuciones de la composición, solo se recuperarán los datos que se hayan modificado o creado después de la última fecha de ejecución.

     Después de la primera ejecución de la composición, la variable **[!UICONTROL Fecha de la última ejecución]** está disponible. Especifica la fecha que se utilizará para la siguiente ejecución y se actualiza automáticamente cada vez que se ejecuta la composición. Todavía tiene la posibilidad de anular este valor introduciendo manualmente uno nuevo para que se ajuste a sus necesidades.

   >[!NOTE]
   >
   >El **[!UICONTROL Usar un campo de fecha]** El modo permite una mayor flexibilidad en función del campo de fecha seleccionado. Por ejemplo, si el campo especificado corresponde a una fecha de modificación, el modo de campo de fecha permite recuperar datos que se han actualizado recientemente, mientras que el otro modo excluye simplemente las grabaciones que ya estaban segmentadas en una ejecución anterior, incluso si se han modificado desde la última ejecución de la composición.

<!--

## Example {#incremental-query-example}

The following example shows the configuration of a workflow which filters every week the profiles in the Adobe Campaign database that are subscribed to the Yoga Newsletter service, to send them a welcome email.

![](../assets/incremental-query-example.png)

The workflow is made up of the following elements:

* A **[!UICONTROL Scheduler]** activity, to execute the workflow every Monday at 6 am.
* An **[!UICONTROL Incremental query]** activity, which targets all of the current subscribers during the first execution, then only the new subscribers of that week during the following executions.
* An **[!UICONTROL Email delivery]** activity.
-->
