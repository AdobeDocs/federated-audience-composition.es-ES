---
title: Novedades de la composición de público federado de Experience Platform
description: Últimas actualizaciones y notas de la versión
badge: label="Disponibilidad limitada" type="Informative"
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 61a70f9de0a6cf171a2ff1128b57ae6206be842c
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 53%

---

# Notas de la versión {#rn-new}

[!DNL Federated Audience Composition] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan en estas notas de la versión. [!DNL Federated Audience Composition] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Versión de octubre de 2024 {#fac-24-10}

### Compatibilidad {#fac-24-10-compat}

Con esta nueva versión, Federated Audience Composition ahora es compatible con los sistemas que se enumeran a continuación.

* **Compatibilidad con Databricks**

  Ahora puede establecer conexiones con bases de datos de Databricks mediante Federated Audience Composition. [Más información](../connections/federated-db.md#databricks)

* **Compatibilidad con acceso seguro al Snowflake mediante AWS PrivateLink**

  Ahora se admite el acceso seguro al almacén de datos de Snowflake externo a través de un vínculo privado. Tenga en cuenta que la cuenta de Snowflake debe estar alojada en Amazon Web Service (AWS) y ubicada en la misma región que el entorno de Composición de audiencia federada. Póngase en contacto con su representante de Adobe para obtener ayuda sobre la configuración del acceso seguro a su cuenta de Snowflake. [Más información](../connections/federated-db.md#snowflake)

* **Compatibilidad sin servidor Amazon Redshift**

  Con esta nueva versión, Federated Audience Composition admite [Amazon Redshift Serverless](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Mejoras {#fac-24-10-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

* **Actualizar esquemas existentes**

  Cuando se crea, modifica o elimina una columna en una base de datos federada, ahora puede detectar y aplicar los cambios haciendo clic en el botón **[!UICONTROL Actualizar esquema]** del esquema correspondiente. [Más información](../customer/schemas.md#schema-refresh)

* **Asociar un modelo de datos con una nueva composición**

  Al crear una composición, ahora puede seleccionar el modelo de datos que desea asociar a él. Con esta nueva opción, la configuración de las actividades es más sencilla, ya que solo están disponibles las tablas del modelo de datos asociado. [Más información](../compositions/create-composition.md)

## Versión de julio de 2024: Composición de audiencias federadas (LA) {#fac-la}

>[!AVAILABILITY]
>
>Ahora mismo, la composición de público federado de Adobe Experience Platform solo está disponible para un conjunto de organizaciones (disponibilidad limitada). 
>

La composición de público federado es una función complementaria que proporciona a las empresas un acceso flexible y ampliado a los almacenes de datos empresariales para componer públicos utilizando conjuntos de datos empresariales esenciales y potenciar las experiencias iniciadas por la marca y en el momento. Con este nuevo enfoque, como usuario de [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/home){target="_blank"} o [Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/ajo-home){target="_blank"}, puede federar los datos de público directamente desde su almacén de datos existente para enriquecer los públicos de Adobe Experience Platform en un solo sistema.

La composición de público federado responde a la creciente demanda del mercado para las empresas que necesitan la flexibilidad de componer públicos con conjuntos de datos de almacén. Esto permite a las empresas reducir el movimiento de datos y, al mismo tiempo, poner los datos de público esenciales a disposición de los equipos de marketing para satisfacer los requisitos de los casos de uso y potenciar las experiencias personalizadas. 

Obtenga más información acerca de las funciones de la composición de público federado en [esta página](get-started.md) y en las [Preguntas frecuentes](faq.md).

Para obtener información detallada sobre los requisitos previos para acceder a las composiciones de público federado y las protecciones actuales, consulte [esta página](access-prerequisites.md).

