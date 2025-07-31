---
audience: end-user
title: Actividad Cambiar datos de Source
description: Descubra cómo puede utilizar la actividad Cambiar fuente de datos para cambiar la fuente de datos utilizada por la composición, lo que proporciona más flexibilidad para administrar los datos en una composición.
exl-id: 8f8e627a-fef9-42b8-a42a-bfa1c421b202
source-git-commit: 59983bb7fd0f8886cc38bfcfc8d7005db4747ac0
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# Cambio de la fuente de datos

>[!IMPORTANT]
>
>Las actividades **[!UICONTROL Cambiar dimensión]** y **[!UICONTROL Cambiar fuente de datos]** deberían **no** agregarse en una fila. Si necesita usar ambas actividades consecutivamente, incluya una actividad **[!UICONTROL Enrichment]** entre ellas. Esto garantiza una ejecución adecuada y evita posibles conflictos o errores.

La actividad **[!UICONTROL Cambiar fuente de datos]** le permite cambiar la fuente de datos que usa su composición.

## Configurar {#configure}

Después de agregar una actividad **[!UICONTROL Cambiar fuente de datos]** al lienzo, puede definir la fuente de datos para el flujo de trabajo.

![La opción de origen de datos está resaltada en el área de trabajo de Composición de audiencia federada.](/help/compositions/assets/change-data-source/configure.png){zoomable="yes"}{width="70%"}

| Fuente | Descripción |
| ------ | ----------- |
| Cuenta externa de FDA | Una base de datos de nube externa conectada a la Composición de audiencia federada. |

Después de seleccionar **[!UICONTROL cuenta externa de FDA]**, puede elegir con qué cuenta externa desea conectarse.

![Se muestra la ventana emergente que muestra las opciones de cuenta externa.](/help/compositions/assets/change-data-source/fda-external-account.png){zoomable="yes"}{width="70%"}
