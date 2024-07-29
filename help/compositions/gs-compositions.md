---
audience: end-user
title: Introducción a las composiciones
description: Aprenda a empezar con composiciones
badge: label="Disponibilidad limitada" type="Informative"
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 3b891232a3a671f8ec12e06b19086f12ef849f1e
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 13%

---

# Introducción a las composiciones {#compositions}

## Qué es una composición {#what}

Adobe Composición de audiencias le permite crear composiciones, donde puede aprovechar varias actividades (dividir, excluir...) en un lienzo visual para crear audiencias. Una vez hecho, las audiencias resultantes se guardan en Adobe Experience Platform junto con las audiencias existentes y se pueden aprovechar en destinos de Adobe Experience Platform y Adobe Journey Optimizer para segmentar clientes. [Aprenda a trabajar con audiencias](../start/audiences.md)

![](assets/composition-example.png)

## Acceso y administración de composiciones {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composiciones"
>abstract="En esta pantalla, puede acceder a la lista completa de composiciones, comprobar su estado actual, las fechas de última/siguiente ejecución y crear una nueva composición."

Se puede acceder a las composiciones desde el menú **[!UICONTROL Audiencias]** de Adobe Experience Platform, en la pestaña **[!UICONTROL Composiciones federadas]**.

Desde esta pantalla, puede crear nuevas composiciones y acceder a las existentes. También puede duplicar o eliminar una composición existente haciendo clic en el botón de puntos suspensivos situado junto a su nombre.

![](assets/compositions-list.png)

Para refinar la lista y encontrar fácilmente la composición que está buscando, puede buscar en la lista y filtrar composiciones por sus estados o fechas de último procesamiento.

También puede personalizar la lista añadiendo o quitando columnas. Para ello, haga clic en el botón **[!UICONTROL Configurar columna]**s y agregue o quite las columnas de salida que desee.

![](assets/compositions-columns.png)

## Estados de las composiciones {#status}

Las composiciones pueden tener varios estados:

* **[!UICONTROL Borrador]**: la composición se ha creado y guardado.
* **[!UICONTROL En curso]**: la composición se ha ejecutado y se está ejecutando.
* **[!UICONTROL Detenido]**: la ejecución de la composición se ha completado y se ha detenido.
* **[!UICONTROL En pausa]**: La ejecución de la composición se ha pausado.
* **[!UICONTROL Erróneo]**: La ejecución de la composición ha encontrado un error. Abra la composición y acceda a los registros y tareas para identificar el error y resolverlo.

Encontrará información detallada sobre cómo iniciar y supervisar una composición en [esta sección](../compositions/start-monitor-composition.md).
