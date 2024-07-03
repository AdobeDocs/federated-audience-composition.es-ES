---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
source-git-commit: 4ccf3be01abb8d6cb2834f49d83b677edaa61ef7
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 36%

---


# Principios clave de la creación de la composición {#gs-composition-creation}

>[!CONTEXTUALHELP]
>id="dc_composition_creation_properties"
>title="Propiedades de composición"
>abstract="En esta pantalla, elija la plantilla que desea utilizar para crear la composición y especifique una etiqueta. Expanda la sección OPTIONS ADICIONALES para definir más opciones, como el nombre interno de la maquetación, su carpeta, zona horaria y grupo de supervisores. Se recomienda encarecidamente seleccionar un grupo de supervisores para que los operadores sean alertados si se produce un error."

La Composición de datos federada proporciona un lienzo visual que le permite crear audiencias aprovechando varias actividades (dividir, enriquecer, etc.).

## ¿Qué hay dentro de una composición? {#gs-composition-inside}

El diagrama de composición es una representación de lo que se supone que debe suceder. Describe las diversas tareas que se realizan y cómo se relacionan entre sí.

![](assets/composition-example.png){zoomable="yes"} {zoomable="yes"}

Cada composición contiene:

* **Actividades**: una actividad es una tarea que se va a realizar. Las distintas actividades disponibles se representan en el diagrama mediante iconos. Cada actividad tiene propiedades específicas y otras propiedades que son comunes a todas las actividades.

  En un diagrama de composición, una actividad determinada puede producir varias tareas, en particular cuando hay un bucle o acciones recurrentes.

* **Transiciones**: las transiciones vinculan una actividad de origen a una actividad de destino y definen su secuencia.

* **Tablas de trabajo**: la tabla de trabajo contiene toda la información que transmite la transición. Cada composición utiliza varias tablas de trabajo. Los datos transmitidos en estas tablas pueden utilizarse en todo el ciclo de vida de la composición.

## Pasos clave para crear una composición {#gs-composition-steps}

Los pasos principales para crear una composición son los siguientes:

1. [Creación de la composición](#create)
1. [Configurar los ajustes de la composición](#starting-audience)
1. [Añadir y configurar actividades](#action-activities)
1. [Ejecutar la composición y supervisar su ejecución](#save)
