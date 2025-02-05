---
title: Novedades de la composición de público federado de Experience Platform
description: Últimas actualizaciones y notas de la versión
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: 51a6c6154452ae56e495312f1d4e909f4eb2d06e
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 88%

---

# Notas de la versión {#rn-new}

[!DNL Federated Audience Composition] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan en estas notas de la versión. [!DNL Federated Audience Composition] está creado de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información acerca de estos cambios en [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.


## Actualización de febrero de 2025 {#fac-25-01}

A partir de la versión de febrero, [!DNL Federated Audience Composition] empezará a aplicar el acceso de las interfaces de **Federated data management** y **Federated Compositions** al usuario al que se ha concedido el permiso **Administrar datos federados**.

Recomendamos a los usuarios que se pongan en contacto con los administradores para que se agregue este permiso a su función a fin de seguir teniendo acceso a la interfaz de usuario [!DNL Federated Audience Composition].

Para aprender a asignar este permiso, consulte la [documentación detallada](feature-access.md).

## Versión de noviembre de 2024 {#fac-24-11}

### Mejoras {#fac-24-11-improvements}

Esta versión incorpora la mejora que se indica a continuación.

* **Lista de direcciones IP permitidas**

  Al añadir una base de datos federada en la interfaz de usuario de Adobe Experience Platform, ahora puede ver directamente las direcciones IP asociadas con las instancias de Composición de público federado. Esto le permite copiar y autorizar fácilmente estas IP para conectarse a la base de datos y tener mayor seguridad y flexibilidad. [Más información](../connections/connections.md)

## Versión de octubre de 2024 {#fac-24-10}

>[!AVAILABILITY]
>
>Anteriormente disponible para un conjunto de organizaciones (LA), la composición de público federado de Adobe Experience Platform ya está disponible para todos los usuarios (GA). Este complemento se activa en función de su oferta y solo es visible con los permisos asociados. [Más información](access-prerequisites.md)
>

### Compatibilidad {#fac-24-10-compat}

Con esta nueva versión, la composición de público federado ahora es compatible con los sistemas que se enumeran a continuación.

* **Compatibilidad con Databricks**

  Ahora puede establecer conexiones con bases de datos de Databricks mediante la composición de público federado. [Más información](../connections/federated-db.md#databricks)

* **Compatibilidad con acceso seguro a Snowflake a través de AWS PrivateLink**

  Ahora se admite el acceso seguro al almacén de datos externo de Snowflake a través de un vínculo privado. Tenga presente que la cuenta de Snowflake debe estar alojada en Amazon Web Services (AWS) y ubicada en la misma región que el entorno de composición de público federado. Póngase en contacto con su representante de Adobe para obtener ayuda sobre la configuración del acceso seguro a su cuenta de Snowflake. [Más información](../connections/federated-db.md#snowflake)

* **Compatibilidad con Amazon Redshift sin servidor**

  Con esta nueva versión, la composición de público federado admite [Amazon Redshift sin servidor](https://aws.amazon.com/redshift/redshift-serverless/){target="_blank"}.

### Mejoras {#fac-24-10-improvements}

Esta versión incorpora las mejoras que se enumeran a continuación.

* **Actualizar esquemas existentes**

  Cuando se crea, modifica o elimina una columna en una base de datos federada, ahora puede detectar y aplicar los cambios haciendo clic en el botón **[!UICONTROL Actualizar esquema]** del esquema correspondiente. [Más información](../customer/schemas.md#schema-refresh)

* **Asociar un modelo de datos con una nueva composición**

  Al crear una composición, ahora puede seleccionar el modelo de datos que desea asociarle. Con esta nueva opción, la configuración de las actividades es más sencilla, ya que solo están disponibles las tablas del modelo de datos asociado. [Más información](../compositions/create-composition.md)

## Versión de julio de 2024: composición de público federado (disponibilidad limitada) {#fac-la}

La composición de público federado es una función complementaria que proporciona a las empresas un acceso flexible y ampliado a los almacenes de datos empresariales para componer públicos utilizando conjuntos de datos empresariales esenciales y potenciar las experiencias iniciadas por la marca y en el momento. Con este nuevo enfoque, como usuario de [Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/home){target="_blank"} o [Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/ajo-home){target="_blank"}, puede federar los datos de público directamente desde su almacén de datos existente para enriquecer los públicos de Adobe Experience Platform en un solo sistema.

La composición de público federado responde a la creciente demanda del mercado para las empresas que necesitan la flexibilidad de componer públicos con conjuntos de datos de almacén. Esto permite a las empresas reducir el movimiento de datos y, al mismo tiempo, poner los datos de público esenciales a disposición de los equipos de marketing para satisfacer los requisitos de los casos de uso y potenciar las experiencias personalizadas. 

Obtenga más información acerca de las funciones de la composición de público federado en [esta página](get-started.md) y en las [Preguntas frecuentes](faq.md).

Para obtener información detallada sobre los requisitos previos para acceder a las composiciones de público federado y las protecciones actuales, consulte [esta página](access-prerequisites.md).

