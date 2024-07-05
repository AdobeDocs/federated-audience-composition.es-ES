---
audience: end-user
title: Trabajo con actividades
description: Aprenda a trabajar con actividades
source-git-commit: 4ba457f1dcd8b7997931a70d93a95f6a54c51cb5
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 16%

---


# Trabajo con actividades {#activities}

En Federated Audience Composition, puede crear composiciones utilizando dos tipos de actividades:

* **Actividades de segmentación** permite crear uno o más objetivos definiendo una audiencia y dividiendo o combinando estas audiencias mediante operaciones de intersección, unión o exclusión.
* **Control de flujo** Las actividades son específicas para organizar y ejecutar composiciones. Su principal tarea es coordinar las demás actividades.

## Actividades de segmentación

* [Crear actividad de audiencia](build-audience.md): Defina la población objetivo. Puede seleccionar una audiencia existente o utilizar el modelador de consultas para definir su propia consulta.
* [Cambiar dimensión](change-dimension.md): cambie el esquema, también conocido como dimensión de segmentación, a medida que vaya creando la composición.
* [Combinar](combine.md): realice la segmentación en la población entrante. Puede utilizar una unión, una intersección o una exclusión.
* [Deduplicación](deduplication.md): elimine duplicados en los resultados de las actividades entrantes.
* [Enriquecimiento](enrichment.md): defina los datos adicionales que se procesarán en la composición. Con esta actividad, puede aprovechar la transición entrante y configurar la actividad para completar la transición saliente con datos adicionales.
* [Reconciliación](reconciliation.md): Defina el vínculo entre los datos de la base de datos y los datos de una tabla de trabajo, por ejemplo, los datos cargados desde un archivo externo.
* [Guardar audiencia](save-audience.md): actualice una audiencia existente o cree una nueva a partir de la población calculada en sentido ascendente en una composición.
* [Split](split.md): Segmente la población entrante en varios subconjuntos.

## Actividades de control de flujo

* [AND-join](and-join.md): sincronice varias ramas de ejecución de un flujo de trabajo.
* **Fin** : Marca gráfica del final de un flujo de trabajo. Esta actividad no tiene impacto funcional y, por lo tanto, es opcional.
* [Tenedor](fork.md): cree transiciones salientes para el inicio de varias actividades al mismo tiempo.
* [Planificador](scheduler.md): programe cuándo se inicia el flujo de trabajo.
* [Esperar](wait.md): Pause momentáneamente la ejecución de una parte de un flujo de trabajo.
