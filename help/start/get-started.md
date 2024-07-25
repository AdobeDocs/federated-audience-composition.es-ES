---
title: Introducción a Federated Audience Composition
description: Descubra qué es la Composición de audiencia federada de Adobe y cómo utilizarla en Adobe Experience Platform
badge: label="Disponibilidad limitada" type="Informative"
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: e0f74c25e2f57098ce65c8cdf032a90b4eecdaba
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 11%

---

# Introducción a Federated Audience Composition {#gs-fac}

La Composición de audiencias federada es un complemento para Adobe Real-time Customer Data Platform y Adobe Journey Optimizer que le permite crear y enriquecer audiencias de sus almacenes de datos de terceros e importarlas a Adobe Experience Platform. Federated Audience Composition ofrece una solución fácil y potente para conectar su almacén de datos empresarial directamente en Adobe Real-time Customer Data Platform o Adobe Journey Optimizer y realizar consultas en las tablas de su almacén de datos.

La Composición de audiencias federada de Adobe ayuda a los usuarios de aplicaciones de Adobe Experience Platform a acceder a los datos de sus clientes almacenados en sus almacenes de datos y plataformas de almacenamiento en la nube como Amazon Redshift, Azure synapse Analytics y más. Los datos del cliente pueden almacenarse en varios almacenes de datos y ahora se puede acceder a ellos instantáneamente, sin replicación. Las plataformas compatibles se enumeran en [esta página](../connections/federated-db.md#supported-db).

## Casos de uso {#rn-uc}

A través de una interfaz de usuario fácil de usar para marketing, puede crear reglas de segmentos que consulten su almacén de datos para obtener una lista de usuarios que cumplan los requisitos de un segmento específico necesario para campañas de marketing, acceder a audiencias existentes en el almacén para su activación o enriquecer audiencias de Adobe Experience Platform con puntos de datos adicionales que existan en el almacén.

En esta versión, hay dos casos de uso disponibles: Creación de audiencias y Enriquecimiento de audiencias. El enriquecimiento del perfil estará disponible en una versión futura.

![diagrama](assets/fac-use-cases.png){zoomable="yes"}

## Pasos clave {#gs-steps}

La composición de audiencias federadas de Adobe le permite crear y actualizar audiencias de Adobe Experience Platform directamente desde la base de datos, sin ningún proceso de ingesta.

![diagrama](assets/steps-diagram.png){zoomable="yes"}

Pasos clave:

1. **Integración de datos**: reúna datos de varias fuentes y combínelos en un conjunto de datos unificado. Obtenga información sobre cómo conectar aplicaciones de Adobe Experience Platform y el almacén de datos empresarial, las bases de datos compatibles y cómo configurarlas en [esta sección](../connections/federated-db.md).

2. **Modelado de datos**: Diseñe y cree modelos de datos y esquemas que definan la estructura, las relaciones y las restricciones de los datos. Obtenga más información sobre los esquemas en [esta página](../customer/schemas.md). Aprenda a crear vínculos para el modelo de datos en [esta página](../data-management/gs-models.md).

3. **Transformación de datos**: aplique técnicas de manipulación de datos para modificar el formato, la estructura o los valores de los elementos de datos y hacerlos compatibles o adecuados para aplicaciones o análisis específicos.

4. **Uso de datos**: Cree, organice y genere audiencias. Aprenda a componer audiencias en [esta página](../compositions/gs-compositions.md). También puede actualizar o reutilizar audiencias existentes a través de Adobe Experience Platform Audience Portal y Destinations. Obtenga más información en [esta página](../connections/destinations.md)


>[!NOTE]
>
>Después de ejecutar la maquetación, la audiencia resultante se guarda en Adobe Experience Platform como audiencia externa y está disponible en Adobe Real-Time Customer Data Platform o Adobe Journey Optimizer. Es accesible desde el menú **Audiencias**. [Más información](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}
>



## Más información {#learn}

<!-- Workflow + Workflow activities-->

Ver las preguntas más frecuentes en [esta página](faq.md).

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
