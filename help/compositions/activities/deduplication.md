---
audience: end-user
title: Uso de la actividad de anulación de duplicación
description: Aprenda a utilizar la actividad de anulación de duplicación
source-git-commit: 56d9cc6489557c12761cd3fe8f3b7a61a71ece21
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 60%

---


# Anulación de duplicación {#deduplication}

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_fields"
>title="Campos para identificar los duplicados"
>abstract="En la sección **Campos para identificar los duplicados**, haga clic en el botón **Añadir atributo** para especificar los campos para los que los valores idénticos permiten identificar los duplicados, tales como: dirección de correo electrónico, nombre, apellidos, etc. El orden de los campos permite especificar los que se procesarán en primer lugar."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication"
>title="Actividad de anulación de duplicación"
>abstract="La actividad de **anulación de duplicación** permite eliminar duplicados en los resultados de las actividades entrantes. Se utiliza principalmente después de actividades de segmentación y antes de actividades que permiten el uso de datos direccionados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_complement"
>title="Generación de un complemento"
>abstract="Puede generar una transición saliente adicional con la población restante, que se excluyó como duplicado. Para ello, active la opción **Generar complemento**"

>[!CONTEXTUALHELP]
>id="dc_orchestration_deduplication_settings"
>title="Configuración de la anulación de duplicación"
>abstract="Para eliminar duplicados en los datos entrantes, defina el método de anulación de duplicación en los campos siguientes. De forma predeterminada, solo se guarda un registro. También debe seleccionar el modo de anulación de duplicación en función de una expresión o un atributo. De forma predeterminada, el registro que se va a excluir de los duplicados se selecciona de forma aleatoria."

La actividad **Deduplication** le permite eliminar duplicados en los resultados de las actividades entrantes, por ejemplo perfiles duplicados en la lista de destinatarios. La actividad **Deduplication** se utiliza generalmente después de actividades de segmentación y antes de actividades que permiten el uso de datos de destino.

## Configuración de la actividad de anulación de duplicación{#deduplication-configuration}

Siga estos pasos para configurar la actividad **Deduplication**:

1. Agregue una actividad **Deduplication** a su composición.

1. Si la actividad tiene varias transiciones de entrada, seleccione la transición que se utilizará para realizar la anulación de duplicación en la lista desplegable **[!UICONTROL Conjunto principal]**

1. En la sección **Campos para identificar los duplicados**, haga clic en el botón **Añadir atributo** para especificar los campos para los que los valores idénticos permiten identificar los duplicados, tales como: dirección de correo electrónico, nombre, apellidos, etc. El orden de los campos permite especificar los que se procesarán en primer lugar.

   ![](../assets/deduplication.png)

1. En la sección **Configuración de anulación de duplicación**, seleccione el número de **duplicados únicos que desea conservar**. El valor predeterminado de este campo es 1. El valor 0 le permite mantener todos los duplicados.

   Por ejemplo, si los registros A y B se consideran duplicados del registro Y, y un registro C se considera un duplicado del registro Z:

   * Si el valor del campo es 1: solo se guardan los registros Y y Z.
   * Si el valor del campo es 0: se guardan todos los registros.
   * Si el valor del campo es 2: se conservan los registros C y Z y se conservan dos registros de A, B e Y, al azar o en función del método de deduplicación seleccionado posteriormente.

1. Seleccione el **método de deduplicación** que se va a utilizar:

   * **Selección aleatoria**: Selecciona aleatoriamente el registro que se va a excluir de los duplicados.
   * **Uso de una expresión**: mantenga los registros en los que el valor de la expresión introducida sea el más pequeño o el más grande.
   * **Valores no vacíos**: Mantenga los registros para los que la expresión no está vacía.
   * **Siguiendo una lista de valores**: defina una prioridad de valor para uno o varios campos. Para definir los valores, haga clic en **Atributo** para seleccionar un campo o crear una expresión y, a continuación, agregue los valores a la tabla adecuada. Para definir un nuevo campo, haga clic en el **botón Agregar** ubicado sobre la lista de valores.

1. Seleccione la opción **Generate complement** si desea utilizar la población restante. El complemento está formado por todos los duplicados. A continuación, se agregará una transición adicional a la actividad.

<!--
## Example{#deduplication-example}

In the following example, use a deduplication activity to exclude duplicates from the target before sending a delivery. The identified duplicated profiles are added to a dedicated audience that can be reused if necessary. Choose the **Email** address to identify the duplicates. Keep 1 entry and select the **Random** deduplication method.

![](../assets/workflow-deduplication-example.png)
-->
