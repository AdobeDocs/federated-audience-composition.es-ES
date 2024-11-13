---
audience: end-user
title: Uso de la actividad AND-join
description: Aprenda a utilizar la actividad AND-join
exl-id: 9648f17b-e54c-4bc2-8dff-d35c438eeb8b
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 70%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join"
>title="Actividad AND-join"
>abstract="La actividad **And-join** le permite sincronizar varias ramas de ejecución de una composición. Se activa una vez que han finalizado todas las actividades anteriores. Esto le permite asegurarse de que ciertas actividades hayan finalizado antes de continuar con la ejecución de la composición."

La actividad **AND-join** le permite sincronizar varias ramas de ejecución de una composición.

Esta actividad solo activa su transición saliente una vez que se activan todas las transiciones entrantes; es decir, una vez que todas las actividades anteriores han finalizado. Esto le permite asegurarse de que ciertas actividades han finalizado antes de continuar ejecutando la composición.

## Configuración de la actividad And-join {#and-join-configuration}

>[!CONTEXTUALHELP]
>id="dc_orchestration_and-join_merging"
>title="Configuración de la actividad And-join"
>abstract="Seleccione las actividades que desea unir. En el menú desplegable **[!UICONTROL Conjunto principal]**, elija qué población de transición entrante desea conservar."

Siga estos pasos para configurar la actividad **Combinación-Y**:

1. Agregue varias actividades para formar al menos dos ramas de ejecución diferentes.
1. Añada una actividad **Combinación-Y** a cualquiera de las ramas.

   ![](../assets/and-join.png)

1. En la sección **[!UICONTROL Combinar opciones]**, compruebe todas las actividades anteriores que desee sincronizar.
1. En el menú desplegable **[!UICONTROL Conjunto principal]**, elija qué población de transición entrante desea conservar. La transición saliente solo puede contener una de las poblaciones de transición entrantes. Si la actividad no está configurada, la transición saliente seleccionará de forma aleatoria una de las poblaciones entrantes.
