---
audience: end-user
title: Trabajo con actividades
description: Aprenda a trabajar con actividades
exl-id: 1e4e5f53-636f-4f1c-bf2f-cc3b5d6d6dda
source-git-commit: 95f262e44c392c1e3c861a2b77b7736657cb9371
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 35%

---

# Trabajo con actividades {#activities}

En Federated Audience Composition, puede crear composiciones utilizando dos tipos de actividades:

* **Las actividades de segmentación** le permiten crear uno o más objetivos definiendo una audiencia y dividiendo o combinando estas audiencias mediante operaciones de intersección, unión o exclusión.
* Las actividades de **control de flujo** son específicas para organizar y ejecutar composiciones. Su principal tarea es coordinar las demás actividades.

## Actividades de segmentación

>[!NOTE]
>
>Al trabajar con actividades de composición, los nombres de atributo **no pueden** contener espacios.

* [Crear actividad de audiencia](build-audience.md): defina la población objetivo. Puede seleccionar un público existente o utilizar el generador de reglas para definir su propia consulta.
* [Cambiar origen de datos](./change-data-source.md): cambie el origen de datos usado por su composición.
* [Cambiar dimensión](change-dimension.md): cambie el esquema, también conocido como dimensión de segmentación, mientras crea la composición.
* [Combinar](combine.md): realice la segmentación en la población entrante. Puede utilizar una unión, una intersección o una exclusión.
* [Deduplicación](deduplication.md): elimine duplicados en los resultados de las actividades entrantes.
* [Enriquecimiento](enrichment.md): defina datos adicionales para procesar en su composición. Con esta actividad, puede aprovechar la transición entrante y configurar la actividad para completar la transición saliente con datos adicionales.
* [Reconciliación](reconciliation.md): defina el vínculo entre los datos de la base de datos y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un archivo externo.
* [Guardar audiencia](save-audience.md): actualice una audiencia existente o cree una nueva a partir de la población calculada en sentido ascendente en una composición.
* [División](split.md): segmente la población entrante en varios subconjuntos.

## Actividades de control de flujo

* [AND-join](and-join.md): sincronice varias ramas de ejecución de una composición.
* **Fin**: marca gráficamente el final de una composición. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional.
* [Bifurcación](fork.md): crear transiciones de salida para iniciar varias actividades al mismo tiempo.
* [Programador](scheduler.md): Programe cuando comience la composición.
* [Espera](wait.md): pausa momentáneamente la ejecución de una parte de una composición.
