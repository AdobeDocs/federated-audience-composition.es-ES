---
audience: end-user
title: Uso de la actividad Enrichment
description: Aprenda a utilizar la actividad de enriquecimiento
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 52%

---


# Enriquecimiento {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Actividad de enriquecimiento"
>abstract="La actividad de **enriquecimiento** permite mejorar los datos de destino con información adicional de la base de datos. Normalmente, se utiliza en una composición después de las actividades de segmentación."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Actividad de enriquecimiento"
>abstract="Una vez añadidos los datos de enriquecimiento a la composición, pueden utilizarse en las actividades añadidas después de la actividad **Enriquecimiento** para segmentar perfiles en grupos distintos según sus comportamientos, preferencias y opciones."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_simplejoin"
>title="Definición de vínculo"
>abstract="Cree un vínculo entre los datos de la tabla de trabajo y la base de datos federada."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_reconciliation"
>title="Reconciliación de enriquecimiento"
>abstract="Defina los parámetros de reconciliación."

>[!CONTEXTUALHELP]
>id="dc_targetdata_personalization_enrichmentdata"
>title="Datos de enriquecimiento"
>abstract="Seleccione los datos que desee utilizar para enriquecer la composición. Se pueden seleccionar dos tipos de datos de enriquecimiento: un único atributo de enriquecimiento del esquema, también conocido como dimensión de segmentación, o un vínculo de recopilación, que es un vínculo con una cardinalidad 1-N entre las tablas."

La actividad **Enrichment** le permite mejorar los datos de destino con información adicional de la base de datos federada. Normalmente se utiliza en composiciones después de actividades de segmentación.

Los datos de enriquecimiento pueden provenir de los siguientes lugares:

* **De la misma tabla de trabajo** que la que está dirigida a su composición:

  *Asigne un grupo de clientes y agregue el campo &quot;Fecha de nacimiento&quot; a la tabla de trabajo actual*.

* **De otra tabla de trabajo**:

  *Seleccione como público destinatario a un grupo de clientes y añada los campos “Cantidad” y “Tipo de producto” procedentes de la tabla “Comprar”*.

Una vez que los datos de enriquecimiento se hayan agregado a la composición, se pueden usar en las actividades agregadas después de la actividad **Enrichment** para segmentar a los clientes en grupos distintos según sus comportamientos, preferencias y opciones.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## Configuración de la actividad Enrichment {#enrichment-configuration}

Siga estos pasos para configurar la actividad **Enriquecimiento**:

1. Añada actividades como **Generar público destinatario** y **Combinar**.
1. Añada una actividad **Enriquecimiento**

   ![](../assets/enrichment.png)

1. Si se han configurado varias transiciones en la composición, puede utilizar el campo **[!UICONTROL Conjunto principal]** para definir qué transición debe utilizarse como conjunto principal para enriquecerse con datos.

1. Haga clic en **Agregar datos de enriquecimiento** y seleccione el atributo que se utilizará para enriquecer los datos.

   ![](../assets/enrichment-add.png)

   >[!NOTE]
   >
   >El **botón Editar expresión** de la pantalla de selección de atributos le permite generar expresiones avanzadas para seleccionar el atributo.

<!--PAS VU SUR INSTANCE: You can select two types of enrichment data: a single enrichment attribute from the target dimension, or a collection link. Each of these types is detailed in the examples below:

    * [Single enrichment attribute](#single-attribute)
    * [Collection lnk](#collection-link)-->

## Ejemplos {#example}

### Atributo de enriquecimiento único {#single-attribute}

A continuación, simplemente añadimos un único atributo de enriquecimiento, por ejemplo, la fecha de nacimiento. Siga estos pasos:

1. Haga clic dentro del campo **Atributo**.
1. Seleccione un campo simple del esquema, también conocido como dimensión de segmentación, y la fecha de nacimiento en nuestro ejemplo.
1. Haga clic en **Confirmar**.

<!--### Collection link {#collection-link}

In this more complex use case, we will select a collection link which is a link with a 1-N cardinality between tables. Let's retrieve the three latest purchases that are less than 100$. For this you need to define:

* an enrichment attribute: the **Total amount** field
* the number of lines to retrieve: 3
* a filter: filter out items that are greater than 100$
* a sorting: descendant sorting on the **Order date** field. 

#### Add the attribute {#add-attribute}

This is where you select the collection link to use as enrichment data.

1. Click inside the **Attribute** field.
1. Click **Display advanced attributes**.
1. Select the **Total amount** field from the **Purchases** table. 

#### Define the collection settings{#collection-settings}

Then, define how the data is collected and the number of records to retrieve.

1. Select **Collect data** in the **Select how the data is collected** drop-down.
1. Type "3" in the **Lines to retrieve (Columns to create)** field. 

If you want, for example, to get the average amount of purchases for a customer, select **Aggregated data** instead, and select **Average** in the **Aggregate function** drop-down.

#### Define the filters{#collection-filters}

Here, we define the maximum value for the enrichment attribute. We filter out items that are greater than 100$. [Learn how to work with the query modeler](../../query/query-modeler-overview.md)

1. Click **Edit filters**.
1. Add the two following filters: **Total amount** exists AND **Total amount** is less than 100. The first one filters NULL values as they would appear as the greatest value.
1. Click **Confirm**.

#### Define the sorting{#collection-sorting}

We now need to apply sorting in order to retrieve the three **latest** purchases.

1. Activate the **Enable sorting** option.
1. Click inside the **Attribute** field.
1. Select the **Order date** field.
1. Click **Confirm**. 
1. Select **Descending** from the **Sort** drop-down.-->
