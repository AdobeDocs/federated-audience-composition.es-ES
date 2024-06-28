---
audience: end-user
title: Uso de la actividad AND-join
description: Aprenda a utilizar la actividad AND-join
source-git-commit: e2e708a21aa0e2d1724f5ba79caf10ef803ae818
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 66%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Actividad AND-join"
>abstract="El **And-join** esta actividad le permite sincronizar varias ramas de ejecución de una composición. Se activa una vez que han finalizado todas las actividades anteriores. Esto le permite asegurarse de que ciertas actividades han finalizado antes de continuar ejecutando la composición."

El **And-join** esta actividad le permite sincronizar varias ramas de ejecución de una composición.

Esta actividad solo activa su transición saliente una vez que se activan todas las transiciones entrantes; es decir, una vez que todas las actividades anteriores han finalizado. Esto le permite asegurarse de que ciertas actividades han finalizado antes de continuar ejecutando la composición.

## Configuración de la actividad And-join {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Configurar la actividad de AND-join"
>abstract="Seleccione las actividades que desea unir. En el menú desplegable **Conjunto principal**, elija qué población de transición entrante desea conservar."

Siga estos pasos para configurar la actividad **Combinación-Y**:

1. Añada varias actividades, como actividades del canal, para formar al menos dos ramas de ejecución diferentes.
1. Añada una actividad **Combinación-Y** a cualquiera de las ramas.
1. En la sección **Opciones de combinación**, compruebe todas las actividades anteriores que desee combinar.
1. En el menú desplegable **Conjunto principal**, elija qué población de transición entrante desea conservar. La transición saliente solo puede contener una de las poblaciones de transición entrantes.

