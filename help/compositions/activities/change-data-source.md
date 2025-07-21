---
audience: end-user
title: Actividad Cambiar datos de Source
description: Descubra cómo puede utilizar la actividad Cambiar fuente de datos para cambiar la fuente de datos utilizada por la composición, lo que proporciona más flexibilidad para administrar los datos en una composición.
source-git-commit: 2a21dcde345febdaad0934c8835df5f7ae8c30f6
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---


# Cambio de la fuente de datos

>[!IMPORTANT]
>
>Las actividades **[!UICONTROL Cambiar dimensión]** y **[!UICONTROL Cambiar fuente de datos]** deberían **no** agregarse en una fila. Si necesita usar ambas actividades consecutivamente, incluya una actividad **[!UICONTROL Enrichment]** entre ellas. Esto garantiza una ejecución adecuada y evita posibles conflictos o errores.

La actividad **[!UICONTROL Cambiar fuente de datos]** le permite cambiar la fuente de datos que usa su composición.

## Configurar {#configure}

Después de agregar una actividad **[!UICONTROL Cambiar fuente de datos]** al lienzo, puede definir la fuente de datos para el flujo de trabajo.

![La opción de origen de datos está resaltada en el área de trabajo de Composición de audiencia federada.](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}{align="center"}

| Fuente | Descripción |
| ------ | ----------- |
| Cuenta externa de FDA | Una base de datos de nube externa conectada a Adobe Campaign mediante Federated Audience Composition. |

Después de seleccionar **[!UICONTROL cuenta externa de FDA]**, puede elegir con qué cuenta externa desea conectarse.

![Se muestra la ventana emergente que muestra las opciones de cuenta externa.](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}{align="center"}
