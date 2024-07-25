---
title: Preguntas frecuentes
description: Preguntas frecuentes
badge: label="Disponibilidad limitada" type="Informative"
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: 03ad7a7ca602379567bca04f3750faa7a15d61db
workflow-type: tm+mt
source-wordcount: '826'
ht-degree: 2%

---

# Preguntas frecuentes {#faq}

A continuación se muestra una lista de preguntas más frecuentes sobre la Composición de audiencias federada. También hay disponible una pregunta frecuente global para el servicio de segmentación de Adobe Experience Platform en [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}.


+++¿Cuáles son los permisos necesarios para acceder a Federated Audience Composition?

La composición de audiencias federada requiere paquetes de Adobe Real-time Customer Data Platform y Adobe Journey Optimizer Prime o Ultimate. No hay permisos específicos para Composición de audiencia federada. El único requisito previo para acceder a esta capacidad es haber adquirido el complemento Federated Audience Composition.

+++

+++¿Qué almacenes de nube son compatibles?

Para esta versión, Composición de audiencia federada es compatible con:

* Amazon Redshift
* Azure synapse
* Google Big Query
* Snowflake
* Vertica Analytics

+++


+++¿Se pueden consultar varios almacenes de datos en la misma composición?

Sí, es posible consultar varios almacenes en la misma composición y combinar datos de varias fuentes.  Normalmente, cada [actividad de composición](../compositions/orchestrate-activities.md) (consulta, enriquecimiento, división, etc.) ejecuta una o varias instrucciones SQL en función de la configuración de la actividad, las bases de datos de destino (puede haber varios casos de acceso de datos federado) y los resultados de una o varias tablas de trabajo con el resultado de la ejecución. Estas tablas de trabajo se utilizan como entrada para actividades consecutivas.

+++

+++ ¿Puedo acceder a toda mi base de datos utilizando Federated Audience Composition?

No, depende de usted configurar el acceso a una base de datos o esquema dedicado o compartido. Le recomendamos que cree un esquema dedicado para la Composición de audiencias federada y que copie/comparta solo conjuntos de datos de casos comerciales.
+++



+++¿Tengo acceso a todas las tablas del esquema dedicado?

Sí, una vez conectada, Federated Audience Composition puede utilizarse para descubrir todas las tablas en función de los derechos iniciales definidos. A continuación, puede utilizar el editor de esquemas visuales para lo siguiente:

* Descubra las columnas y las claves principales de las tablas
* Cree etiquetas descriptivas para esas tablas
* Crear etiquetas descriptivas para cada columna
* Ocultar columnas innecesarias
* Guardar la descripción de esas tablas
+++


+++¿Hay algún almacenamiento temporal en la composición de audiencias federada?

No, la composición de audiencia federada solo almacena metadatos (descripciones de esquema). No hay datos de clientes en transición. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++¿La Composición de audiencia federada almacena una copia física de esa lista de personas para enviarla a sistemas posteriores?

La composición de audiencias federada no mantiene una copia física de los datos. La frecuencia se configura en la composición para definir la frecuencia con la que se actualizarán estos datos. Adobe Experience Platform no almacena los datos de audiencia resultantes más tiempo del requerido por los casos de uso o la acción del cliente.

Por ejemplo:

* En el caso de la creación de audiencias, esta se crea en el almacén y se puede utilizar la composición de audiencia federada para realizar tareas de composición y manipulación de datos adicionales antes de publicar la audiencia resultante y los atributos asociados mediante Adobe Experience Platform Audience Portal. La definición de audiencia y los atributos asociados se transfieren a Adobe Experience Platform.
Tenga en cuenta que la caducidad de los datos actuales para las audiencias generadas externamente es de 30 días. Esta caducidad de los datos reduce la cantidad de datos sobrantes almacenados en una organización. Una vez transcurrido el periodo de caducidad de los datos, el conjunto de datos asociado sigue siendo visible dentro del inventario de conjuntos de datos, pero no puede activar la audiencia y el recuento de perfiles se mostrará como cero. Obtenga más información en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* En el caso de un enriquecimiento de audiencia, el punto de partida es una audiencia de Adobe Experience Platform existente. Se pueden ver dos escenarios aquí:
   1. Incorporar atributos de carga útil de audiencia adicionales desde el almacén de datos federado: en este caso, los atributos adicionales que se agregan se incluyen como parte de esta definición de audiencia. La caducidad de los datos para las audiencias generadas de forma externa es la misma que se describe anteriormente, 30 días.
   1. Refine la audiencia de Adobe Experience Platform existente en función de los atributos adicionales que existan en su almacén de datos. <!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Si los datos de los patrones de casos de uso de Creación de audiencias y Enriquecimiento de audiencias no se mantienen, ¿cómo se almacenan temporalmente?

Los datos de audiencia resultantes no persisten indefinidamente en Adobe Experience Platform ni en Composición de audiencia federada. No se conservará más tiempo del requerido por su caso de uso. Los atributos de audiencia introducidos como parte de la carga útil de audiencia persisten únicamente como parte de la definición de audiencia. La duración de la persistencia se basa en el TTL para cualquier audiencia, el valor predeterminado es de 30 días.

+++

+++¿Puedo eliminar una audiencia cargada personalizada?

Puede eliminar audiencias que no se utilicen en la activación descendente directamente en Audience Portal simplemente seleccionando Eliminar en el menú de acciones. Obtenga más información en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.

+++

+++Si combino datos de varias fuentes, ¿cómo los unimos? ¿Estamos usando el servicio de identidad?

No, el servicio de identidad no se está aprovechando durante una composición. Los datos entre las distintas fuentes utilizadas en la composición se unen mediante una lógica definida por el usuario (tal y como se expresa en el modelo subyacente), por ejemplo, ID de CRM, número de cuenta de usuario, etc. Debe seleccionar la identidad que se utiliza como identificador en la audiencia para seleccionarla en el Data Warehouse. En una audiencia resultante de la Composición de audiencia federada, debe identificar el área de nombres de identidad para la identidad en el conjunto de datos resultante.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->
