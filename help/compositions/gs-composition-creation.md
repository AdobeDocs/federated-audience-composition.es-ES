---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
badge: label="Disponibilidad limitada" type="Informative"
exl-id: 861440ab-ce14-46aa-a215-b86fc9ffeef0
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 59%

---

# Principios clave de la creación de una composición {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Propiedades de la composición"
>abstract="En esta pantalla, elija la plantilla que desea utilizar para crear la composición y especifique una etiqueta. Expanda la sección OPCIONES ADICIONALES para configurar más opciones, como el nombre interno de la composición, su carpeta, zona horaria y grupo de supervisores. Se recomienda encarecidamente seleccionar un grupo de supervisores para que los operadores sean alertados si se produce un error."

## Qué hay dentro de una composición {#gs-composition-inside}

La composición de audiencias federadas de Experience Platform proporciona un lienzo visual que le permite crear audiencias aprovechando varias actividades (dividir, enriquecer, etc.).

El diagrama de composición es una representación de lo que se supone que debe suceder. Describe las diversas tareas que se realizan y cómo se relacionan entre sí.

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

Cada composición contiene:

* **[!UICONTROL Actividades]**: una actividad es una tarea que se va a realizar. Las distintas actividades disponibles se representan en el diagrama mediante iconos. Cada actividad tiene propiedades específicas y otras propiedades que son comunes a todas las actividades.
* **[!UICONTROL Transiciones]**: las transiciones vinculan una actividad de origen a una actividad de destino y definen su secuencia.
* **[!UICONTROL Tablas de trabajo]**: la tabla de trabajo contiene toda la información que transmite la transición. Cada composición utiliza varias tablas de trabajo. Los datos transmitidos en estas tablas pueden utilizarse en todo el ciclo de vida de la composición.

## Pasos clave para crear una composición {#gs-composition-steps}

Los pasos principales para crear una composición son los siguientes:

1. [Creación y configuración de la composición](../compositions/create-composition.md)
1. [Organización de actividades](../compositions/orchestrate-activities.md)
1. [Ejecutar la composición y supervisar su ejecución](../compositions/start-monitor-composition.md)
