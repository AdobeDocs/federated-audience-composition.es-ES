---
audience: end-user
title: Trabajo con actividades
description: Aprenda a trabajar con actividades
exl-id: 1e4e5f53-636f-4f1c-bf2f-cc3b5d6d6dda
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 16%

---

# Trabajo con actividades {#activities}

En Federated Audience Composition, puede crear composiciones utilizando dos tipos de actividades:

* **Las actividades de segmentación** le permiten crear uno o más objetivos definiendo una audiencia y dividiendo o combinando estas audiencias mediante operaciones de intersección, unión o exclusión.
* Las actividades de **control de flujo** son específicas para organizar y ejecutar composiciones. Su principal tarea es coordinar las demás actividades.

## Actividades de segmentación

* [Crear actividad de audiencia](build-audience.md): defina la población objetivo. Puede seleccionar una audiencia existente o utilizar el modelador de consultas para definir su propia consulta.
* [Cambiar dimensión](change-dimension.md): cambie el esquema, también conocido como dimensión de segmentación, mientras crea la composición.
* [Combinar](combine.md): realice la segmentación en la población entrante. Puede utilizar una unión, una intersección o una exclusión.
* [Anulación de duplicación](deduplication.md): elimine duplicados en los resultados de las actividades entrantes.
* [Enriquecimiento](enrichment.md): defina datos adicionales para procesar en su composición. Con esta actividad, puede aprovechar la transición entrante y configurar la actividad para completar la transición saliente con datos adicionales.
* [Reconciliación](reconciliation.md): defina el vínculo entre los datos de la base de datos y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un archivo externo.
* [Guardar audiencia](save-audience.md): actualice una audiencia existente o cree una nueva a partir de la población calculada en sentido ascendente en una composición.
* [Split](split.md): Segmente la población entrante en varios subconjuntos.

## Actividades de control de flujo

* [AND-join](and-join.md): sincronice varias ramas de ejecución de una composición.
* **Fin** : Marca gráficamente el final de una composición. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional.
* [Bifurcación](fork.md): cree transiciones salientes para iniciar varias actividades al mismo tiempo.
* [Programador](scheduler.md): Programe cuando comience la composición.
* [Espera](wait.md): pausa momentáneamente la ejecución de una parte de una composición.
