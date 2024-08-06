---
audience: end-user
title: Trabajar con públicos
description: Descubra cómo trabajar con públicos
badge: label="Disponibilidad limitada" type="Informative"
exl-id: c6507624-1dc9-43f9-a3ad-c3dc9689f8c7
source-git-commit: f549f1611bfe6deb6dc684e3a0d9c968ba7c184a
workflow-type: ht
source-wordcount: '311'
ht-degree: 100%

---

# Trabajar con públicos {#gs-audiences}

La composición de público federado de Experience Platform le permite [crear composiciones](../compositions/gs-compositions.md), donde puede aprovechar diversas actividades en un lienzo visual para crear públicos y almacenarlos en Adobe Experience Platform Audience Portal

A continuación, puede tener estos públicos como objetivo en Journey Optimizer o activarlos en cualquier destino admitido por Adobe Experience Platform.

## Creación de públicos mediante composiciones{#creation}

Para crear públicos utilizando la composición de público federado, debe crear una composición que incluya la actividad **[!UICONTROL Guardar público]**. Esta actividad le permite guardar el público en Audience Portal y seleccionar campos de las bases de datos externas para incluirlos en el público. [Obtenga información sobre cómo configurar la actividad Guardar público](../compositions/activities/save-audience.md)

Los públicos creados con la Composición de datos federados de Adobe incluyen todos los campos seleccionados en la actividad **[!UICONTROL Guardar público]** y se almacenan en Audience Portal junto con todos los públicos de Adobe Experience Platform.

Después de ejecutar la composición, el público resultante se guarda en Adobe Experience Platform como público externo y está disponible en Adobe Real-Time Customer Data Platform o Adobe Journey Optimizer. 

Puede activar estos públicos en cualquier destino admitido por Adobe Experience Platform. Aprenda a trabajar con destinos en [Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/home){target="_blank"}

>[!NOTE]
>
>Los públicos creados con la composición de público federado de Adobe no se pueden editar. Para realizar modificaciones en uno de estos públicos, debe crear un público nuevo con una composición.

## Acceso al público en Adobe Experience Platform {#access-audience}

A los públicos creados con Composición de público federado se accede desde Audience Portal, que está en el menú **Públicos**.

La pestaña **[!UICONTROL Examinar]** lista todos los públicos existentes almacenados en Adobe Experience Platform. Puede identificar los públicos de la composición de público federado en la lista mediante la columna **[!UICONTROL Origen]** o los filtros disponibles en el panel izquierdo.

![](assets/audiences-list.png)

Para obtener más información sobre cómo trabajar con públicos en Adobe Experience Platform, consulte la [documentación de Audience Portal](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

<!-- add link to this donc once published: https://jira.corp.adobe.com/browse/PLAT-198674-->