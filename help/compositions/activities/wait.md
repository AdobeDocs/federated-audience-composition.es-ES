---
audience: end-user
title: Uso de la actividad Espera
description: Aprenda a utilizar la actividad de espera
exl-id: 59857bd2-2a0b-4c97-ba4e-048dfd9af8f2
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 45%

---

# Espera {#wait}

>[!CONTEXTUALHELP]
>id="dc_orchestration_wait"
>title="Actividad de espera"
>abstract="La actividad **Espera** se utiliza para retrasar la transición de una actividad a otra."

La actividad **Wait** permite que transcurra un cierto tiempo entre dos actividades que se están ejecutando.

## Configuración{#wait-configuration}

Siga estos pasos para configurar la actividad **Esperar**:

1. Agregue una actividad **Wait** a la composición.

1. Especifique la **Duración** de la espera entre las transiciones entrantes y salientes.

1. Seleccione la unidad de tiempo en el campo **Periodos**: segundos, minutos, horas, días.

   ![](../assets/wait.png)
