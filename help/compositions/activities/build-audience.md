---
audience: end-user
title: Uso de la actividad Generar audiencia
description: Aprenda a utilizar la actividad Generar audiencia
source-git-commit: 5fe470ce83a5c3d3df7717bc1203849d99edf430
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 24%

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
1. Especifique si desea crear una audiencia o seleccionar una existente.
1. Configure su audiencia siguiendo los pasos detallados en las pestañas a continuación.

>[!BEGINTABS]

>[!TAB Crear audiencia]

Para crear su propia audiencia, siga estos pasos:

1. Seleccionar **Crear audiencia**.
1. Elija la **Esquema**, también conocida como dimensión de segmentación. El esquema permite definir la población objetivo de la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, el esquema se selecciona en los destinatarios.
1. Haga clic en **Continuar**.
1. Utilice el modelador de consultas para definir la consulta. [Aprenda a trabajar con el modelador de consultas](../../query/query-modeler-overview.md)

>[!TAB Leer audiencia]

Para seleccionar un público destinatario existente, siga estos pasos:

1. Seleccione **Leer público destinatario**.
1. Haga clic en **Continuar**.
1. Seleccione la audiencia.

>[!ENDTABS]

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
