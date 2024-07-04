---
audience: end-user
title: Uso de la actividad de reconciliación
description: Aprenda a utilizar la actividad de reconciliación
source-git-commit: b21306cefe6e9e66263012110a7f89f2d92b38a5
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 41%

---


# Reconciliación {#reconciliation}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation"
>title="Actividad de reconciliación"
>abstract="El **Reconciliación** La actividad permite definir el vínculo entre los datos de la base de datos y los datos de una tabla de trabajo."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_field"
>title="Campo de selección de reconciliación"
>abstract="Campo de selección de reconciliación"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_condition"
>title="Condición de creación de reconciliación"
>abstract="Condición de creación de reconciliación"

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_complement"
>title="Complemento de generación de reconciliación"
>abstract="Complemento de generación de reconciliación"

El **Reconciliación** La actividad de permite definir el vínculo entre los datos de la base de datos y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un sistema externo.

<!--For example, the **Reconciliation** activity can be placed after a **Load file** activity to import non-standard data into the database. In this case, the **Reconciliation** activity lets you define the link between the data in the Adobe Campaign database and the data in the work table.-->

## Prácticas recomendadas {#reconciliation-best-practices}

Mientras que el **Enriquecimiento** la actividad permite definir datos adicionales para procesarlos en la composición (se puede utilizar un **Enriquecimiento** actividad para combinar datos procedentes de varios conjuntos o para crear vínculos a un recurso temporal), **Reconciliación** La actividad le permite vincular datos no identificados a recursos existentes.

>[!NOTE]
>La operación de reconciliación implica que los datos de las dimensiones vinculadas ya están en la base de datos.  Por ejemplo, si importa un archivo de compras que muestre qué producto se compró, a qué hora, por qué cliente, etc., el producto y el cliente ya deben existir en la base de datos.

## Configuración de la actividad Reconciliación {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting"
>title="Dimensión de segmentación"
>abstract="Seleccionar la nueva dimensión de segmentación. Una dimensión permite definir la población objetivo: destinatarios, suscriptores de la aplicación, operadores, suscriptores, etc. De forma predeterminada, está seleccionada la dimensión de segmentación actual."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_rules"
>title="Reglas de reconciliación"
>abstract="Seleccione las reglas de reconciliación que desee utilizar para la anulación de duplicación. Para utilizar atributos, seleccione **Atributos simples** y seleccione los campos de origen y destino. Para crear su propia condición de reconciliación utilizando el modelador de consultas, seleccione la opción **Condiciones de reconciliación avanzadas**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_targeting_selection"
>title="Seleccionar la dimensión de segmentación"
>abstract="Seleccione la dimensión de segmentación con la que se reconciliarán los datos de entrada."

>[!CONTEXTUALHELP]
>id="dc_orchestration_keep_unreconciled_data"
>title="Mantener datos no reconciliados"
>abstract="De forma predeterminada, los datos no reconciliados se mantienen en la transición de salida y están disponibles en la tabla de trabajo para usarlos en el futuro. Para quitar los datos no reconciliados, desactive la opción **Mantener datos no reconciliados**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_reconciliation_attribute"
>title="Atributo de reconciliación"
>abstract="Seleccione el atributo que desea utilizar para conciliar los datos y confirmar."

Siga estos pasos para configurar el **Reconciliación** actividad:

1. Añadir un **Reconciliación** actividad en la composición. <!--This activity should be added following a transition containing a population whose targeting dimension does not directly come from Adobe Campaign. -->

1. Seleccionar la nueva dimensión de segmentación. Una dimensión permite definir la población objetivo: destinatarios, suscriptores de la aplicación, operadores, suscriptores, etc. <!--[Learn more about targeting dimensions](../../audience/about-recipients.md#targeting-dimensions).-->

1. Seleccione los campos que se utilizarán para la reconciliación. Se pueden utilizar uno o más criterios de reconciliación.

   1. Para utilizar atributos para reconciliar datos, seleccione **Atributos simples** opción. El **Source** field enumera los campos disponibles en la transición de entrada que se van a conciliar. El **Destino** field corresponde a los campos de la dimensión de segmentación seleccionada. Los datos se concilian cuando el origen y el destino son iguales. Por ejemplo, seleccione la opción **Correo electrónico** para deduplicar perfiles en función de su dirección de correo electrónico.

      Para añadir otros criterios de reconciliación, haga clic en **Añadir regla** botón. Si se especifican varias condiciones de vínculo, todas deben verificarse para que los datos puedan vincularse.

   <!--     ![](../assets/workflow-reconciliation-criteria.png)-->

   1. Para utilizar otros atributos para reconciliar datos, seleccione la opción **Condiciones de reconciliación avanzadas** opción. A continuación, puede crear su propia condición de reconciliación utilizando el modelador de consultas. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md).-->

1. Puede filtrar los datos para conciliarlos mediante el **Crear filtro** botón. Esto permite crear una condición personalizada mediante el modelador de consultas. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

De forma predeterminada, los datos no conciliados se mantienen en la transición saliente y están disponibles en la tabla de trabajo para su uso futuro. Para quitar los datos no reconciliados, desactive la opción **Mantener datos no reconciliados**.

<!--
## Example {#reconciliation-example}

The following example demonstrates a workflow that creates an audience of profiles directly from an imported file containing new clients. It is made up of the following activities:

The workflow is designed as follows:

![](../assets/workflow-reconciliation-sample-1.0.png)

 
It is built with the following activities:

* A [Load file](load-file.md) activity uploads a file containing profiles data that were extracted from an external tool.

    For example:

    ```
    lastname;firstname;email;birthdate;
    JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
    PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
    WEAVER;Justin;justin_w@testmail.com;11/15/1990;
    MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
    REESE;Richard;rreese@testmail.com;02/08/1987;
    ```

* A **Reconciliation** activity which identifies the incoming data as profiles, by using the **email** and **Date of birth** fields as reconciliation criteria.

    ![](../assets/workflow-reconciliation-sample-1.1.png)

* A [Save audience](save-audience.md) activity to create a new audience based on these updates. You can also replace the **Save audience** activity by an **End** activity if no specific audience needs to be created or updated. Recipient profiles are updated in any case when you run the workflow.


## Compatibility {#reconciliation-compat}

The **Reconciliation** activity does not exist in the Client console. All **Enrichments** activities created in the Client console with the reconciliation options enabled are displayed as **Reconciliation** activities in Campaign Web user interface.
-->
