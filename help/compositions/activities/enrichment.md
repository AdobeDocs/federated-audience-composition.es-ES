---
audience: end-user
title: Uso de la actividad Enrichment
description: Aprenda a utilizar la actividad de enriquecimiento
source-git-commit: ed642303540f5c2395e25dddfed20f2cb4970982
workflow-type: tm+mt
source-wordcount: '1123'
ht-degree: 40%

---

# Enriquecimiento {#enrichment}

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment"
>title="Actividad de enriquecimiento"
>abstract="La actividad de **enriquecimiento** permite mejorar los datos de destino con información adicional de la base de datos. Normalmente se utiliza en una composición después de actividades de segmentación."

>[!CONTEXTUALHELP]
>id="dc_orchestration_enrichment_data"
>title="Actividad de enriquecimiento"
>abstract="Una vez añadidos los datos de enriquecimiento a la composición, pueden utilizarse en las actividades añadidas después de la **Enriquecimiento** actividad para segmentar perfiles en grupos distintos según sus comportamientos, preferencias y opciones."

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
>abstract="Seleccione los datos que desea utilizar para enriquecer la composición. Se pueden seleccionar dos tipos de datos de enriquecimiento: un único atributo de enriquecimiento de la dimensión de público destinatario o un vínculo de recopilación, que es un vínculo con una cardinalidad 1-N entre las tablas."

El **Enriquecimiento** esta actividad permite mejorar los datos de destino con información adicional de la base de datos federada. Normalmente se utiliza en composiciones después de actividades de segmentación.

Los datos de enriquecimiento pueden provenir de los siguientes lugares:

* **Desde la misma tabla de trabajo** como el que se segmentó en la composición:

  *Oriente un grupo de clientes y agregue el campo &quot;Fecha de nacimiento&quot; a la tabla de trabajo actual*.

* **De otra tabla de trabajo**:

  *Seleccione como público destinatario a un grupo de clientes y añada los campos “Cantidad” y “Tipo de producto” procedentes de la tabla “Comprar”*.

Una vez añadidos los datos de enriquecimiento a la composición, pueden utilizarse en las actividades añadidas después de la **Enriquecimiento** actividad para segmentar a los clientes en grupos distintos según sus comportamientos, preferencias y opciones.

<!--For instance, you can add to the working table information related to customers' purchases and use this data to personalize emails with their latest purchase or the amount spent on these purchases.-->

## Añadir una actividad de enriquecimiento {#enrichment-configuration}

Siga estos pasos para configurar la actividad **Enriquecimiento**:

1. Añada actividades como **Generar público destinatario** y **Combinar**.
1. Añada una actividad **Enriquecimiento**
1. Si se han configurado varias transiciones en la composición, puede utilizar el **[!UICONTROL Conjunto principal]** para definir qué transición debe utilizarse como conjunto principal para enriquecerse con datos.

## Añadir datos de enriquecimiento {#enrichment-add}

1. Clic **Añadir datos de enriquecimiento** y seleccione el atributo que se utilizará para enriquecer los datos.

   Puede seleccionar dos tipos de datos de enriquecimiento: un único atributo de enriquecimiento de la dimensión de destino o un vínculo de recopilación. Cada uno de estos tipos se detalla en los ejemplos siguientes:

   * [Atributo de enriquecimiento único](#single-attribute)
   * [Vínculo de colección](#collection-link)

<!--
>[!NOTE]
>
>The **Edit expression button** in the attribute selection screen allows you to build advanced expressions to select the attribute. [Learn how to work with the expression editor](../../query/expression-editor.md)-->

## Creación de vínculos entre tablas {#create-links}

El **[!UICONTROL Definición de vínculo]** permite crear un vínculo entre los datos de la tabla de trabajo y la base de datos. Por ejemplo, si carga datos de un archivo que contiene el número de cuenta, el país y el correo electrónico de los destinatarios, debe crear un vínculo hacia la tabla del país para actualizar esta información en sus perfiles.

Hay varios tipos de vínculos disponibles:

* **[!UICONTROL 1 enlace simple de cardinalidad]**: Cada registro del conjunto principal se puede asociar con un registro de los datos vinculados y solo con uno.
* **[!UICONTROL 0 o 1 enlace simple de cardinalidad]**: Cada registro del conjunto principal puede asociarse con 0 o 1 registro de los datos vinculados, pero no más de uno.
* **[!UICONTROL Enlace de colección de cardinalidad N]**: Cada registro del conjunto principal se puede asociar con 0, 1 o más registros (N) de los datos vinculados.

Para crear un vínculo, siga estos pasos:

1. En el **[!UICONTROL Definición de vínculo]** , haga clic en **[!UICONTROL Añadir vínculo]** botón.

1. En el **Tipo de relación** , elija el tipo de vínculo que desea crear.

1. Identifique el objetivo al que desea vincular el conjunto principal:

   * Para vincular una tabla existente en la base de datos, elija **[!UICONTROL Esquema de base]** y seleccione la tabla que desee en la **[!UICONTROL Esquema de destino]** field.
   * Para vincular con datos de la transición de entrada, elija **Esquema temporal** y seleccione la transición cuyos datos desee utilizar.

1. Defina los criterios de reconciliación para hacer coincidir los datos del conjunto principal con el esquema vinculado. Hay dos tipos de uniones disponibles:

   * **Unión simple**: seleccione un atributo específico para hacer coincidir los datos de los dos esquemas. Clic **Añadir unión** y seleccione la **Source** y **Destino** atributos que se utilizarán como criterios de reconciliación.
   * **Unión avanzada**: cree un vínculo con condiciones avanzadas. Clic **Añadir unión** y haga clic en **Crear condición** para abrir el modelador de consultas.

Una muestra de composición que utiliza vínculos está disponible en el [Ejemplos](#link-example) sección.

## Ejemplos {#example}

### Atributo de enriquecimiento único {#single-attribute}

A continuación, simplemente añadimos un único atributo de enriquecimiento, por ejemplo, la fecha de nacimiento. Siga estos pasos:

1. Haga clic dentro del campo **Atributo**.
1. Seleccione un campo simple de la dimensión de segmentación, en nuestro ejemplo, la fecha de nacimiento.
1. Haga clic en **Confirmar**.

### Vínculo de colección {#collection-link}

En este caso de uso más complejo, seleccionaremos un vínculo de colección, que es un vínculo con una cardinalidad 1-N entre tablas. Vamos a recuperar las tres últimas compras con un importe menor a 100 €. Para ello, debe definir lo siguiente:

* un atributo de enriquecimiento: el campo **Cantidad total**
* número de líneas que se van a recuperar: 3
* un filtro: filtre los artículos que superen los 100 €
* un orden: orden descendente en el campo **Fecha del pedido**.

#### Añadir el atributo {#add-attribute}

Aquí es donde se selecciona el vínculo de colección que se utilizará como datos de enriquecimiento.

1. Haga clic dentro del campo **Atributo**.
1. Haga clic en **Mostrar atributos avanzados**.
1. Seleccione el campo **Cantidad total** de la tabla **Compras**.

#### Definir la configuración de la colección{#collection-settings}

A continuación, defina cómo se recopilan los datos y el número de registros que desea recuperar.

1. Seleccionar **Recopilar datos** en el menú desplegable **Seleccione cómo se recopilan los datos**.
1. Escriba &quot;3&quot; en el campo **Líneas a recuperar (Columnas a crear)**.

Si desea, por ejemplo, obtener la cantidad promedio de compras para un cliente, seleccione **Datos acumulados** en su lugar y seleccione **Promedio** en el menú desplegable **Función de acumulado**.

#### Definición de los filtros{#collection-filters}

Aquí, definimos el valor máximo del atributo de enriquecimiento. Filtramos los elementos superiores a 100 $. <!--[Learn how to work with the query modeler](../../query/query-modeler-overview.md)-->

1. Haga clic en **Editar filtros**.
1. Añada los dos filtros siguientes: **Cantidad total** existe Y **Cantidad total** es menor que 100. El primero filtra los valores NULOS, ya que aparecerían como el valor más alto.
1. Haga clic en **Confirmar**.

#### Definición de la ordenación{#collection-sorting}

Ahora necesitamos aplicar la ordenación para recuperar las tres **últimas** compras.

1. Active la opción **Habilitar ordenación**.
1. Haga clic dentro del campo **Atributo**.
1. Seleccione el campo **Fecha del pedido**.
1. Haga clic en **Confirmar**.
1. Seleccione **Descendente** desde el menú desplegable **Ordenar**.


### Enriquecimiento con datos vinculados {#link-example}

El ejemplo siguiente muestra una composición configurada para crear un vínculo entre dos transiciones. La primera transición identifica los datos de perfil mediante una actividad de consulta, mientras que la segunda transición incluye datos de compra almacenados en un archivo cargado mediante una actividad de archivo de carga.

* El primero **Enriquecimiento** la actividad vincula nuestro conjunto principal (datos del **Consulta** actividad) con el esquema de **Cargar archivo** actividad. Esto nos permite hacer coincidir cada perfil objetivo por la consulta con los datos de compra correspondientes.
* Un segundo **Enriquecimiento** actividad se añade para enriquecer los datos de la tabla de composición con los datos de compra procedentes de **Cargar archivo** actividad. Esto nos permite utilizar esos datos en actividades adicionales, por ejemplo, para personalizar mensajes enviados a los clientes con información sobre su compra.





<!--

Add other fields
use it in delivery


cardinality between the tables (1-N)
1. select attribute to use as enrichment data

    display advanced fields option
    i button

    note: attributes from the target dimension

1. Select how the data is collected
1. number of records to retrieve if want to retrieve a collection of multiple records
1. Apply filters and build rule

    select an existing filter
    save the filter for reuse
    view results of the filter visually or in code view

1. sort records using an attribute

leverage enrichment data in campaign

where we can use the enrichment data: personalize email, other use cases?

## Example

-->
