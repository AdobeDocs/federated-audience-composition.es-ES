---
audience: end-user
title: Uso de la actividad Espera
description: Aprenda a utilizar la actividad de espera
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 60%

---

# Espera {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Actividad de espera"
>abstract="La actividad **Espera** se utiliza para retrasar la transición de una actividad a otra."

El **Esperar** actividad permite que transcurra un cierto tiempo entre dos actividades que se están ejecutando. Por ejemplo, para esperar varios días después de una actividad de envío de correo electrónico y, después, analizar las aperturas y los clics generados durante este período antes de realizar cualquier operación de seguimiento (correo electrónico recordatorio, creación de un público, etc.).

## Configuración{#wait-configuration}

Siga estos pasos para configurar la actividad **Esperar**:

1. Añadir un **Esperar** actividad en la composición.

1. Especifique la **Duración** de la espera entre las transiciones entrantes y salientes.

1. Seleccione la unidad de tiempo en la **Períodos** campo: segundos, minutos, horas, días.

