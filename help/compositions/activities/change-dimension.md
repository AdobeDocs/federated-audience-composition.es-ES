---
audience: end-user
title: Uso de la actividad Change dimension
description: Aprenda a utilizar la actividad de la dimensión Cambiar
badge: label="Disponibilidad limitada" type="Informative"
exl-id: e71017bd-6d2f-4ace-b2d9-cbfbb537d127
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 42%

---

# Cambiar dimensión {#change-dimension}

>[!CONTEXTUALHELP]
>id="dc_orchestration_dimension_complement"
>title="Generación de un complemento"
>abstract="Puede generar una transición saliente adicional con la población restante, que se excluyó como duplicado. Para ello, active la opción **[!UICONTROL Generar complemento]**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_change_dimension"
>title="Actividad cambiar dimensión"
>abstract="Esta actividad le permite cambiar el esquema, también conocido como dimensión de segmentación, a medida que genera un público. Desplace el eje en función de la plantilla de datos y del esquema de entrada. Por ejemplo, puede cambiar del esquema “contratos” al esquema &quot;clientes&quot;."

La actividad **Cambiar dimensión** le permite cambiar el esquema, también conocido como dimensión de segmentación, mientras crea su audiencia. Desplaza el eje según la plantilla de datos y el esquema de entrada.

## Configuración de la actividad Change dimension {#configure}

Siga estos pasos para configurar la actividad **Cambiar dimensión**:

1. Agregue una actividad **Cambiar dimensión** a su composición.

   ![](../assets/change-dimension.png)

1. Defina el **nuevo esquema**. Durante el cambio de esquema, se guardan todos los registros.

1. Ejecute la composición para ver el resultado. Compare los datos de las tablas antes y después de la actividad **Change dimension** y compare la estructura de las tablas de composición.

<!--
## Example {#example}

In this example, we want to send an SMS delivery to all the profiles who have made a purchase. To do this, we first use a **[!UICONTROL Build audience]** activity linked to a custom "Purchase" targeting dimension to target all purchases that occurred.

We then use a **[!UICONTROL Change dimension]** activity to switch the workflow targeting dimension to "Recipients". This allows us to be able to target the recipients who match the query.
-->

