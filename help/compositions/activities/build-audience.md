---
audience: end-user
title: Uso de la actividad Generar audiencia
description: Aprenda a utilizar la actividad Generar audiencia
source-git-commit: 33a1eb9d4c0c7b847e04ac3f0f9f1881317a2f83
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 37%

---

# Generar público destinatario {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Actividad generar público"
>abstract="El **Crear audiencia** esta actividad le permite definir la audiencia que entrará en la composición."

El **Crear audiencia** esta actividad le permite definir la audiencia que entrará en la composición.

Para definir la población del público destinatario, puede hacer lo siguiente:

<!--* Select an existing audience, created as a list in the client console.-->
* Seleccione un público destinatario de Adobe Experience Platform.
* Cree una nueva audiencia con el generador de modeladores de consultas definiendo y combinando criterios de filtrado.



El **Crear audiencia** la actividad se puede colocar al principio de la composición o después de cualquier otra actividad. Cualquier actividad se puede colocar después de **Crear audiencia**.


## Configuración de la actividad Generar público {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Público"
>abstract="Seleccione la audiencia."

Siga estos pasos para configurar la actividad **Generar público destinatario**:

1. Añadir una actividad **Generar público destinatario**.
1. Defina una etiqueta.
1. Defina el tipo de público destinatario: **Crear la suya propia** o **Leer público destinatario**.
1. Configure su audiencia siguiendo los pasos detallados en las pestañas a continuación.

>[!BEGINTABS]

>[!TAB Cree su propio (consulta)]

Para crear su propia consulta, siga estos pasos:

1. Seleccione **Crear su propia (consulta)**.
1. Elija la **Dimensión de segmentación**. La dimensión de segmentación permite definir la población a la que se dirige la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, el objetivo se selecciona en los destinatarios.<!-- [Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions)-->
1. Haga clic en **Continuar**.
1. Utilice el modelador de consultas para definir la consulta, del mismo modo que crea una audiencia al diseñar un nuevo correo electrónico. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

>[!TAB Leer audiencia]

Para seleccionar un público destinatario existente, siga estos pasos:

1. Seleccione **Leer público destinatario**.
1. Haga clic en **Continuar**.
1. Seleccione la audiencia, del mismo modo que utiliza una audiencia para diseñar una nueva entrega. <!--Refer to this [section](../../audience/add-audience.md).-->

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
