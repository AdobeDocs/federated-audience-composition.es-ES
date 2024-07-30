---
title: Preguntas frecuentes
description: Preguntas frecuentes sobre la composición de audiencias federada de Adobe Experience Platform
badge: label="Disponibilidad limitada" type="Informative"
exl-id: 68cc0ae5-5c41-425f-8b10-ab3515294006
source-git-commit: dd19c6a8170a87c10fd8534bf2aa63adcf360529
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 78%

---

# Preguntas frecuentes {#faq}

A continuación se muestra una lista de preguntas más frecuentes sobre la Composición de audiencias federada de Adobe Experience Platform. Encuentre las preguntas frecuentes globales sobre el Servicio de segmentación de Adobe Experience Platform en [esta página](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/faq){target="_blank"}.


+++¿Cuáles son los permisos necesarios para acceder a la composición de público federado?

La composición de audiencias federada requiere paquetes de Adobe Real-time Customer Data Platform y Adobe Journey Optimizer Prime o Ultimate. También debe haber adquirido el complemento Federated Audience Composition.

Para utilizar la Composición de audiencia de audiencia federada, cada usuario debe agregarse a un perfil específico creado para cada zona protegida. Para obtener más información, consulte la página [Composición de audiencias federadas de acceso](access-prerequisites.md).

+++

+++¿Cuáles son los almacenes en la nube admitidos?

En esta versión, la composición de público federado es compatible con lo siguiente:

* Amazon Redshift
* Azure Synapse
* Google BigQuery
* Snowflake
* Vertica Analytics

+++


+++¿Se pueden consultar varios almacenes de datos en la misma composición?

Sí, es posible consultar varios almacenes en la misma composición y combinar datos de varias fuentes. Normalmente, cada [actividad de composición](../compositions/orchestrate-activities.md) (consulta, enriquecimiento, división, etc.) ejecuta una o varias instrucciones SQL en función de la configuración de la actividad, las bases de datos de destino (puede haber varios casos de acceso de datos federado) y los resultados de una o más tablas de trabajo con el resultado de la ejecución. Estas tablas de trabajo se utilizan como entrada para actividades consecutivas.

+++

+++ ¿Puedo acceder a toda mi base de datos utilizando la composición de público federado?

No, es decisión suya si desea configurar el acceso a una base de datos o esquema dedicado o compartido. Le recomendamos que cree un esquema para la composición de público federado y que copie/comparta únicamente conjuntos de datos de casos empresariales.
+++



+++¿Tengo acceso a todas las tablas del esquema dedicado?

Sí, una vez establecida la conexión, la composición de público federado puede utilizarse para descubrir todas las tablas basándose en los derechos iniciales definidos. A continuación, puede utilizar el editor de esquemas visuales para lo siguiente:

* Descubrir las columnas y las claves principales de las tablas
* Crear etiquetas descriptivas para esas tablas
* Crear etiquetas descriptivas para cada columna
* Ocultar las columnas innecesarias
* Guardar la descripción de esas tablas
+++


+++¿Hay algún almacenamiento temporal en la composición de público federado?

No, la composición de público federado solo almacena metadatos (descripciones de esquema). No hay datos de clientes en transición. <!--The Audience export flow is done directly from Adobe Experience Platform Audience Portal (via [Destination](../connections/destinations.md)) to the customer database. The creation and update flow is done directly from your data warehouse database to Adobe Experience Platform Audience Portal.-->

+++

+++¿La composición de público federado almacena una copia física de esa lista de personas para enviarla a sistemas descendentes?

La composición de público federado no mantiene ninguna copia física de los datos. La frecuencia se configura en la composición para definir cada cuánto tiempo se actualizan los datos. Adobe Experience Platform no almacena los datos de público resultantes más tiempo del requerido por los casos de uso o la acción del cliente.

Por ejemplo:

* En el caso de la creación de audiencias, esta se crea en el almacén y se puede utilizar la composición de audiencia federada para realizar tareas de composición y manipulación de datos adicionales antes de publicar la audiencia resultante y los atributos asociados mediante Adobe Experience Platform Audience Portal. La definición de público y los atributos asociados se transfieren a Adobe Experience Platform.
Tenga en cuenta que la caducidad de los datos actuales para los públicos generados externamente es de 30 días. La caducidad de los datos reduce la cantidad excesiva de datos que se almacena en una organización. Una vez transcurrido el período de caducidad de los datos, el conjunto de datos asociado sigue siendo visible dentro del inventario de conjuntos de datos, pero ya no es posible activar el público y el recuento de perfiles se mostrará como cero. Obtenga más información en la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* En caso de un enriquecimiento de público, el punto de partida es el público existente de Adobe Experience Platform. Aquí se pueden ver dos escenarios:
   1. Incorporar atributos adicionales de carga útil del público desde el almacén de datos federado: en este caso, los atributos adicionales que se añaden provienen de la definición del público. La caducidad de los datos para los públicos generados de forma externa es la misma que la mencionada anteriormente: 30 días.
   1. Refine la audiencia de Adobe Experience Platform existente en función de los atributos adicionales que existan en su almacén de datos. <!--For example, you have an audience of customers who have shown interest in a particular product on the website for the last two months. You now want to take this audience and further segment it using Federated Audience Composition to only include customers who have a high credit score. The credit score is deemed sensitive and individual credit score data points are not copied over from the data warehouse.-->
+++

+++Si los datos de los patrones de casos de uso de Creación de audiencias y Enriquecimiento de audiencias no se mantienen, ¿cómo se almacenan temporalmente?

Los datos de público resultantes no se mantienen indefinidamente en Adobe Experience Platform ni en la composición de público federado. No se conservará más tiempo del requerido por su caso de uso. Los atributos de público introducidos como parte de la carga útil del público se mantienen únicamente como parte de la definición del público. La duración de conservación se basa en el TTL definido para cualquier público, el valor predeterminado es de 30 días.

+++

+++¿Puedo eliminar un público cargado personalizado?

No, en la versión actual no puede eliminar las audiencias cargadas personalizadas. <!--that are not used in downstream activation directly in Audience Portal by simply selecting delete from the actions menu. Learn more in [Adobe Experience Platform documentation](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-do-i-put-an-audience-in-the-deleted-state){target="_blank"}.-->

+++

+++Si combino datos de varias fuentes, ¿cómo se unen esos datos? ¿Se usa el servicio de identidad?

No, el servicio de identidad no se utiliza durante una composición. Los datos entre las distintas fuentes utilizadas en la composición se unen mediante una lógica definida por el usuario (tal y como se expresa en el modelo subyacente), por ejemplo, ID de CRM, número de cuenta de usuario, etc. Debe seleccionar la identidad que se utiliza como identificador en el público para poder seleccionarla en el almacén de datos. En un público resultante de la composición de público federado, debe identificar el espacio de nombres de identidad para la identidad en el conjunto de datos resultante.

+++

<!--
+++If I want to combine federated data with datasets that live in Adobe Experience Platform, how is this done?

Likewise, the Identity Service is not being leveraged in this scenario either. The data model underpinning a composition needs to express how the data warehouse data and the audience to be enriched are related. e.g. assume an existing audience in Adobe Experience Platform contains several attributes, among which is the CRM ID. Assume transactional data is in the data warehouse containing purchases with various attributes, including the CRM ID of the purchaser. The end-user would have to specify that the CRM ID for both objects is used to stitch the two objects together.

+++
-->
