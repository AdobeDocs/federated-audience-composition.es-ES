---
title: Introducción a Federated Audience Composition
description: Descubra qué es la Composición de audiencia federada de Adobe y cómo utilizarla en Adobe Experience Platform
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 856b687afe5fdb22da982bc89b907d2f8dcd6bde
workflow-type: tm+mt
source-wordcount: '1326'
ht-degree: 6%

---


# Introducción a Federated Audience Composition {#gs-fac}

La composición de audiencias federada es un complemento de Adobe Real-time Customer Data Platform y Adobe Journey Optimizer que permite al cliente crear y enriquecer audiencias de los almacenes de datos de terceros e importarlas a Adobe Experience Platform.

La composición de audiencias federada de Adobe Experience Platform ofrece una solución fácil y potente para conectar su almacén de datos empresarial directamente en Adobe Real-time Customer Data Platform o Adobe Journey Optimizer, y realizar consultas en las tablas de su almacén de datos.

La Composición de audiencias federada de Adobe ayuda a los usuarios de aplicaciones de Adobe Experience Platform a acceder a los datos de sus clientes almacenados en sus almacenes de datos y plataformas de almacenamiento en la nube como Amazon Redshift, Azure synapse Analytics y más. Los datos del cliente pueden almacenarse en varios almacenes de datos y ahora se puede acceder a ellos instantáneamente, sin replicación. Las plataformas compatibles se enumeran en [esta página](../connections/federated-db.md#supported-db).


## Casos de uso {#rn-uc}

A través de una interfaz de usuario fácil de usar para marketing, puede crear reglas de segmentos que consulten su almacén de datos para obtener una lista de usuarios que cumplan los requisitos de un segmento específico necesario para campañas de marketing, acceder a audiencias existentes en el almacén para su activación o enriquecer audiencias de Adobe Experience Platform con puntos de datos adicionales que existan en el almacén.

En esta versión, hay dos casos de uso disponibles: Segmentación de audiencia y Enriquecimiento de audiencia. El enriquecimiento del perfil estará disponible en una versión futura.

![diagrama](assets/fac-use-cases.png){zoomable="yes"}

## Pasos clave {#gs-steps}

La composición de audiencias federadas de Adobe le permite crear y actualizar audiencias de Adobe Experience Platform directamente desde la base de datos, sin ningún proceso de ingesta.

![diagrama](assets/steps-diagram.png){zoomable="yes"}

Pasos clave:

* Configuración de ****

   1. Conecte Adobe Experience Platform y su almacén de datos empresarial.
Se admiten las siguientes bases de datos: Snowflake, Google Big Query, Azure synapse, Redshift.
Obtenga más información en [esta página](../connections/federated-db.md)
   1. Cree esquemas para seleccionar qué datos deben ser accesibles desde la interfaz de usuario.
Obtenga más información en [esta página](../customer/schemas.md)
   1. Cree vínculos para el modelo de datos.
Obtenga más información en [esta página](../data-management/gs-models.md)

* **Escribir audiencias**

   1. Diseñe y ejecute composiciones para crear audiencias.
Obtenga más información en [esta página](../compositions/gs-compositions.md)
   1. Actualice o reutilice audiencias existentes a través de Adobe Experience Platform Audience Portal y Destinations.
Obtenga más información en [esta página](../connections/destinations.md)

## Preguntas frecuentes {#faq}

A continuación se muestra una lista de preguntas más frecuentes sobre la Composición de audiencias federada. También hay disponible una pregunta frecuente global para el servicio de segmentación de Adobe Experience Platform en [esta página](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq){target="_blank"}.


+++¿Cuáles son los permisos necesarios para acceder a Federated Audience Composition?

No hay permisos específicos para Composición de audiencia federada. El único requisito previo para acceder a esta capacidad es haber adquirido el complemento Federated Audience Composition.

+++

+++¿Qué almacenes de nube son compatibles?

Para esta versión, Composición de audiencia federada es compatible con:

* Snowflake
* Google Big Query
* Azure synapse
* Amazon Redshift

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

No, la composición de audiencia federada solo almacena metadatos (descripciones de esquema). No hay datos de clientes en transición. El flujo de exportación de audiencias se realiza directamente desde Adobe Experience Platform Audience Portal (a través de [Destination](../connections/destinations.md)) a la base de datos de clientes. El flujo de creación y actualización se realiza directamente desde la base de datos del almacén de datos hasta Adobe Experience Platform Audience Portal.

+++

+++¿La Composición de audiencia federada almacena una copia física de esa lista de personas para enviarla a sistemas posteriores?

La composición de audiencias federada no mantiene una copia física de los datos. La frecuencia se configura en la composición para definir la frecuencia con la que se actualizarán estos datos. Adobe Experience Platform no almacena los datos de audiencia resultantes más tiempo del requerido por los casos de uso o la acción del cliente.

Por ejemplo:

* En el caso de una segmentación de audiencia, la audiencia se crea en su almacén y puede utilizar la composición de audiencia federada para tareas de composición y manipulación de datos adicionales antes de publicar la audiencia resultante y los atributos asociados mediante Adobe Experience Platform Audience Portal. La definición de audiencia y los atributos asociados se transfieren a Adobe Experience Platform.
Tenga en cuenta que la caducidad de los datos actuales para las audiencias generadas externamente es de 30 días. Esta caducidad de los datos reduce la cantidad de datos sobrantes almacenados en una organización. Una vez transcurrido el periodo de caducidad de los datos, el conjunto de datos asociado sigue siendo visible dentro del inventario de conjuntos de datos, pero no puede activar la audiencia y el recuento de perfiles se mostrará como cero. Obtenga más información en [Documentación de Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/faq#how-long-do-externally-generated-audiences-last-for){target="_blank"}.

* En el caso de un enriquecimiento de audiencia, el punto de partida es una audiencia de Adobe Experience Platform existente. Se pueden ver dos escenarios aquí:
   1. Incorporar atributos de carga útil de audiencia adicionales desde el almacén de datos federado: en este caso, los atributos adicionales que se agregan se incluyen como parte de esta definición de audiencia. La caducidad de los datos para las audiencias generadas de forma externa es la misma que se describe anteriormente, 30 días.
   1. Refine la audiencia de Adobe Experience Platform existente en función de los atributos adicionales que existan en su almacén de datos. Por ejemplo, tiene una audiencia de clientes que han mostrado interés en un producto en particular en el sitio web durante los últimos dos meses. Ahora desea tomar esta audiencia y segmentarla aún más mediante la Composición de audiencia federada para incluir solo a los clientes que tienen una puntuación crediticia alta. La puntuación crediticia se considera confidencial y los puntos de datos de puntuación crediticia individuales no se copian del almacén de datos.
+++

+++Si los datos de los patrones de casos de uso de Segmentación de audiencia y Enriquecimiento de audiencia no se mantienen, ¿cómo se almacenan temporalmente?

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

## Más información {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Configuración de ejecución"
>abstract="En esta sección puede configurar opciones relacionadas con la ejecución del flujo de trabajo, como el número de días que se conserva el historial de composición."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Actividad no editable"
>abstract="Cuando una actividad de **Consulta** o **Enriquecimiento** se configura con datos adicionales en la consola, los datos de enriquecimiento se tienen en cuenta y pasan a la transición de salida, pero no se pueden editar."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Crear un vínculo"
>abstract="Defina la configuración del vínculo."
