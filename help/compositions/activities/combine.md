---
audience: end-user
title: Uso de la actividad Combinar
description: Aprenda a utilizar la actividad Combinar
exl-id: 395e96d1-0af2-4e59-b599-f57a083b68ca
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 71%

---

# Combinar {#combine}

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine"
>title="Actividad de combinación"
>abstract="La actividad **Combinar** permite realizar la segmentación de la población entrante. Por lo tanto, puede combinar varias poblaciones, excluir parte de ellas o solo mantener datos comunes para varias poblaciones destinatarias."

La actividad **Combinar** permite realizar la segmentación de la población entrante. Por lo tanto, puede combinar varias poblaciones, excluir parte de ellas o solo mantener datos comunes para varios objetivos.

La actividad **Combinar** se puede colocar después de cualquier otra actividad, pero no al principio de la composición. Cualquier actividad se puede colocar después de **Combinar**.

## Configuración de la actividad de combinación {#combine-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_merging_options"
>title="Opciones de combinación de intersección"
>abstract="La **Intersección** le permite mantener solo los elementos comunes a las diferentes poblaciones de entrada de la actividad. En la sección **Conjuntos para unir**, compruebe todas las actividades anteriores que desee unir."

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_merging_options"
>title="Opciones de combinación de exclusión"
>abstract="La **Exclusión** le permite excluir elementos de una población según determinados criterios. En la sección **Conjuntos para unir**, compruebe todas las actividades anteriores que desee unir."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_options"
>title="Selección del tipo de segmentación"
>abstract="Seleccione cómo combinar públicos: unión, intersección o exclusión."

Siga estos pasos comunes para comenzar a configurar la actividad **Combinar**:

1. Agregue varias actividades para formar al menos dos ramas de ejecución diferentes.

1. Añada una actividad **Combinar** a cualquiera de las ramas anteriores.

1. Seleccione el tipo de segmentación: [Union](#union), [Intersection](#intersection) o [Exclusion](#exclusion), y haga clic en **Continue**.

   ![](../assets/combine.png)

1. En la sección **Conjuntos para unirse**, compruebe todas las actividades anteriores a las que desee unirse.

## Unión {#combine-union}

>[!CONTEXTUALHELP]
>id="dc_orchestration_intersection_reconciliation_options"
>title="Opciones de reconciliación de intersección"
>abstract="Seleccione el tipo de reconciliación para definir cómo se gestionan los duplicados."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_reconciliation"
>title="Opciones de reconciliación"
>abstract="Seleccione el **tipo de reconciliación** para definir cómo gestionar duplicados."

En la actividad **Combinar**, puede configurar una **Unión**.

![](../assets/combine-union.png)

Para ello, debe seleccionar **Tipo de reconciliación** para definir cómo se gestionan los duplicados:

* **Solo claves**: este es el modo predeterminado. La actividad solo mantiene un elemento cuando los elementos de las distintas transiciones entrantes tienen la misma clave. Puede usar esta opción solo si las poblaciones entrantes son homogéneas.
* **Una selección de columnas**: seleccione esta opción para definir la lista de columnas a las que desea aplicar la reconciliación de datos. Primero debe seleccionar el conjunto principal (el que contiene los datos de origen) y luego las columnas que se utilizarán para la unión.

## Intersección {#combine-intersection}

En la actividad **Combinar**, puede configurar una **intersección**.

![](../assets/combine-intersection.png)

Para ello, siga los pasos adicionales a continuación:

1. Seleccione el **Tipo de reconciliación** para definir cómo se gestionan los duplicados. Consulte la sección [Unión](#union).
1. Puede marcar la opción **Generar complemento** si desea procesar la población restante. El complemento contendrá la unión de los resultados de todas las actividades entrantes menos la intersección. A continuación, se añadirá una transición saliente adicional a la actividad.

## Exclusión {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="dc_orchestration_exclusion_options"
>title="Reglas de inclusión"
>abstract="Si es necesario, puede manipular las tablas entrantes. De hecho, para excluir un público destinatario de otro esquema, también conocido como dimensión de segmentación, se debe devolver este público destinatario a la misma dimensión de segmentación que el público destinatario principal. Para ello, haga clic en **Añadir una regla** en la sección **Reglas de exclusión** y especifique las condiciones del cambio de esquema. La reconciliación de datos se lleva a cabo mediante un atributo o una unión."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_sets"
>title="Selección de conjuntos para combinar"
>abstract="En la sección **Conjuntos que unir**, seleccione el **Conjunto principal** de las transiciones entrantes. Es el conjunto desde el que se excluyen los elementos. Los demás conjuntos coinciden con elementos antes de excluirse del conjunto principal."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_exclusion"
>title="Reglas de inclusión"
>abstract="Si es necesario, puede manipular las tablas entrantes. De hecho, para excluir un público destinatario de otro esquema, también conocido como dimensión de segmentación, se debe devolver este público destinatario a la misma dimensión de segmentación que el público destinatario principal. Para ello, haga clic en **Añadir una regla** en la sección **Reglas de exclusión** y especifique las condiciones del cambio de esquema. La reconciliación de datos se lleva a cabo mediante un atributo o una unión."

>[!CONTEXTUALHELP]
>id="dc_orchestration_combine_complement"
>title="Complemento de generación de combinación"
>abstract="Active la opción **Generar complemento** para procesar la población restante en una transición adicional."

En la actividad **Combinar**, puede configurar una **Exclusión**.

![](../assets/combine-exclusion.png)

Para ello, debe seguir los pasos adicionales a continuación:

1. En la sección **Conjuntos que unir**, seleccione el **Conjunto principal** de las transiciones entrantes. Es el conjunto desde el que se excluyen los elementos. Los demás conjuntos coinciden con elementos antes de excluirse del conjunto principal.

1. Si es necesario, puede manipular las tablas entrantes. De hecho, para excluir un objetivo de otro esquema, este objetivo debe devolverse al mismo esquema que el objetivo principal. Para ello, haga clic en **Añadir una regla** en la sección **Reglas de exclusión** y especifique las condiciones del cambio de esquema. La reconciliación de datos se realiza mediante un atributo o una unión. <!-- pas compris-->
1. Seleccione la opción **Generar complemento** si desea procesar la población restante. Consulte la sección [Intersección](#intersection).

<!--
## Examples{#combine-examples}

In the following example, we are using a **Combine** activity and we add a **union** to retrieves all the profiles of the two queries: persons between 18 and 27 years old and persons between 34 and 40 years old.

![](../assets/workflow-union-example.png)

The following example shows the **intersection** between two query activities. It is being used here to retrieve profiles who are between 18 to 27 years old and whose email address has been provided.

![](../assets/workflow-intersection-example.png)

The following **exclusion** example shows two queries configured to filter profiles who are between 18 and 27 years old and have an Adobe email domain. The profiles with an Adobe email domain are then excluded from the first set. 

![](../assets/workflow-exclusion-example.png)
-->
