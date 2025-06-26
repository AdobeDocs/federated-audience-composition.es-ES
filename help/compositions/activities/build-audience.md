---
audience: end-user
title: Uso de la actividad Generar audiencia
description: Aprenda a utilizar la actividad Generar audiencia
exl-id: 6fad3e49-e654-4f68-a125-50056c4ae980
source-git-commit: 2c706e8c7d7d282f8ef2f00875608f06e35ffdf8
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 29%

---

# Generar público {#build-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience"
>title="Actividad generar público"
>abstract="La actividad **Generar público** le permite definir el público que entrará en la composición."

La actividad **Generar audiencia** le permite definir la audiencia que entrará en la composición. Para definir la población del público destinatario, puede hacer lo siguiente:

* Seleccione una audiencia de Adobe Experience Platform existente.
* Cree una nueva audiencia con el modelador de consultas definiendo y combinando criterios de filtrado.

## Configuración de la actividad Generar público {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_audienceselector"
>title="Público"
>abstract="Seleccione el público."

Siga estos pasos para configurar la actividad **Generar público destinatario**:

1. Añadir una actividad **Generar público destinatario**.
1. Defina una etiqueta.
1. Especifique si desea crear una audiencia o seleccionar una existente.
1. Configure su audiencia siguiendo los pasos detallados en las pestañas a continuación.

>[!BEGINTABS]

>[!TAB Crear audiencia]

Para crear su propia audiencia, siga estos pasos:

1. Seleccione **Crear audiencia**.
1. Elija el **Esquema**, también conocido como dimensión de segmentación. El esquema permite definir la población objetivo de la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, el esquema se selecciona en los destinatarios.

   ![](../assets/build-audience-create.png)

1. Haga clic en **Continuar**.
1. Utilice el modelador de consultas para definir la consulta y confirmar. [Aprenda a trabajar con el modelador de consultas](../../query/query-modeler-overview.md)

>[!TAB Leer audiencia]

Para seleccionar un público destinatario existente, siga estos pasos:

1. Seleccione **Leer público destinatario**.
1. Haga clic en **Continuar**.

   ![](../assets/build-audience-read.png)

1. Seleccione el público.

>[!ENDTABS]

>[!NOTE]
>
>La opción **Generar una transición saliente** le permite agregar una transición saliente que se activará al final de la ejecución de la actividad si la población de la audiencia está vacía.

<!--
## Examples{#build-audience-examples}

Here is an example of a workflow with two **Build audience** activities. The first one targets the poker players audience, followed by an email delivery. The second one targets the VIP clients audience, followed by an SMS delivery.

![](../assets/workflow-audience-example.png)
-->
