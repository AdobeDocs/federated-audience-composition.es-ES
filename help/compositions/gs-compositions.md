---
audience: end-user
title: Introducción a las composiciones
description: Obtenga más información acerca de cómo empezar con las composiciones
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: e26b3cfda7c4de98d1e47fc40edd2b87859c6209
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 100%

---

# Introducción a las composiciones {#compositions}

>[!AVAILABILITY]
>
>Para acceder a las composiciones, necesita uno de los siguientes permisos:
>
>-**Administrar composiciones federadas**
>>-**Ver composiciones federadas**
>
>Para obtener más información sobre los permisos necesarios, consulte [Guía de acceso de la composición de público federado](/help/start/feature-access.md).

## ¿Qué es una composición? {#what}

La composición de público de Adobe le permite crear composiciones, donde puede aprovechar diversas actividades (división, exclusión, etc.) en un lienzo visual para crear públicos. Cuando haya finalizado, los públicos resultantes se guardan en Adobe Experience Platform junto con los públicos existentes y se podrán aprovechar en destinos de Adobe Experience Platform y Journey Optimizer para dirigirse a los clientes. [Descubra cómo trabajar con públicos](../start/audiences.md)

![](assets/composition-example.png)

## Acceso y administración de composiciones {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composiciones"
>abstract="En esta pantalla, puede acceder a la lista completa de composiciones, comprobar su estado actual, las fechas de última/siguiente ejecución y crear una nueva composición."

A las composiciones se puede acceder desde el menú **[!UICONTROL Públicos]** de Adobe Experience Platform, en la pestaña **[!UICONTROL Composiciones federadas]**.

Desde esta pantalla, puede crear nuevas composiciones y acceder a las existentes. También puede duplicar o eliminar una composición existente haciendo clic en el botón de puntos suspensivos situado junto a su nombre.

![](assets/compositions-list.png)

Para refinar la lista y encontrar fácilmente la composición que está buscando, puede buscar en la lista y filtrar las composiciones por su estado o fecha de último procesamiento.

También puede personalizar la lista añadiendo o quitando columnas. Para ello, haga clic en el botón **[!UICONTROL Configurar columnas]** y añada o quite las columnas de salida que desee.

![](assets/compositions-columns.png)

## Estados de las composiciones {#status}

Las composiciones pueden tener varios estados:

* **[!UICONTROL Borrador]**: la composición se ha creado y guardado.
* **[!UICONTROL En curso]**: la composición se ejecutó y se sigue ejecutando en estos momentos.
* **[!UICONTROL Detenido]**: la ejecución de la composición ha finalizado y se ha detenido.
* **[!UICONTROL En pausa]**: la ejecución de la composición se ha puesto en pausa.
* **[!UICONTROL Erróneo]**: se ha encontrado un error en la ejecución de la composición. Abra la composición y acceda a los registros y tareas para identificar el error y resolverlo.

Encontrará información detallada para iniciar y supervisar una composición en [esta sección](../compositions/start-monitor-composition.md).
