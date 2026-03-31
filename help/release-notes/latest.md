---
title: Notas de la versión de Federated Audience Composition
description: Últimas actualizaciones y notas de la versión de Federated Audience Composition.
exl-id: d4dcaf31-93cd-4a4e-888a-cf1bbdc4ca03
source-git-commit: d3a97b5887778f910ca8f09f7cb8fa99360a612c
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 8%

---


# Notas de la versión

[!DNL Federated Audience Composition] ofrece continuamente nuevas funciones, mejoras en las existentes y correcciones de errores. Todos los cambios se consolidan en estas notas de la versión. [!DNL Federated Audience Composition] se basa de forma nativa en [!DNL Adobe Experience Platform] y hereda sus últimas innovaciones y mejoras. Obtenga más información sobre estos cambios en las [Notas de la versión de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=es){target="_blank"}.

## Versión de marzo de 2026 {#fac-26-03}

La versión de marzo para Federated Audience Composition admite las siguientes funciones:

### Nuevas funciones {#fac-26-03-feature}

| Segmentación con tecnología de IA |
| --- |
| Ahora puede crear composiciones de audiencia federadas de forma autónoma dentro del asistente de IA. Al utilizar el Asistente de IA para crear la audiencia, el Asistente de IA genera un plan que, después de aprobarlo, se ejecutará en el explorador. Para obtener más información sobre cómo usar el Asistente de IA para crear audiencias, lea la [descripción general del Asistente de IA](/help/start/ai-assistant.md). |

| Asistente de IA para Operational Insights |
| --- |
| Ahora puede hacer preguntas al asistente de IA acerca de las perspectivas operativas dentro de la Composición de audiencias federada. Las áreas compatibles incluyen conexiones, esquemas y modelos de datos. Las composiciones federadas **no** son compatibles con esta versión. Para obtener más información sobre el Asistente de IA en la composición de audiencias federada, lea la [descripción general del Asistente de IA](/help/start/ai-assistant.md). |

## Versión de febrero de 2026 {#fac-26-02}

La versión de febrero para Federated Audience Composition admite las siguientes funciones:

### Nuevas funciones {#fac-26-02-feature}

| Compatibilidad con enriquecimiento de campo |
| --- |
| Ahora puede utilizar la actividad Guardar campo dentro de las composiciones. La actividad Guardar campo permite enriquecer los esquemas de Experience Platform federando datos de almacenes externos y mejorando los esquemas de Experience Platform con atributos adicionales. La actividad de guardar campo admite esquemas B2B y B2C. Para obtener más información acerca del uso de esta actividad, lea [información general sobre las actividades](../compositions/activities.md#save-fields). |

| Compatibilidad con autenticación avanzada para Databricks |
| --- |
| Ahora puede conectarse a Federated Audience Composition con Databricks mediante la autenticación principal del servicio o mediante OAuth 2.0. Para obtener más información acerca de cómo crear una conexión, lea la [descripción general de las conexiones](../connections/home.md#create). |

## Versión de enero de 2026 {#fac-26-01}

La versión de enero de Composición de audiencias federada admite las siguientes nuevas funciones y mejoras:

### Nuevas funcionalidades {#fac-26-01-feature}

| Compatibilidad con la autenticación principal del servicio Azure Synapse |
| --- |
| Ahora puede conectarse a Federated Audience Composition con Azure Synapse mediante una entidad de seguridad de servicio. Para obtener más información acerca de cómo crear una conexión, lea la [descripción general de las conexiones](../connections/home.md#create). |

| Disponibilidad para clientes de Adobe Experience Platform en Amazon Web Service (AWS) |
| --- |
| Ahora puede utilizar la Composición de audiencia federada si la instancia de Experience Platform está en AWS. Para obtener más información sobre Experience Platform en AWS, lea [descripción general de varias nubes](https://experienceleague.adobe.com/en/docs/experience-platform/landing/multi-cloud). |

### Mejoras {#fac-26-01-improvements}

Esta versión incorpora las siguientes mejoras.

- **Configuración de caducidad de datos para audiencias**

  Ahora puede establecer una caducidad de datos al usar la actividad **Guardar audiencia** en una composición.

  Para obtener más información sobre las caducidades de los datos en la Composición de audiencias federada, lee la [guía de actividades](../compositions/activities.md#save-audience).
