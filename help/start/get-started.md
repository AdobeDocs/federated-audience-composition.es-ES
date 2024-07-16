---
title: Introducción a Federated Audience Composition
description: Descubra qué es la Composición de audiencia federada de Adobe y cómo utilizarla en Adobe Experience Platform
source-git-commit: 25f623cde151824effddea34127a82e8d920f3e2
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 34%

---


# Introducción a Federated Audience Composition {#gs-fac}

La Composición de audiencias federada de Adobe ayuda a los usuarios de aplicaciones de Adobe Experience Platform a acceder a los datos de sus clientes almacenados en el almacén de datos empresarial. Los datos de los clientes pueden residir en varios almacenes de datos y deben ser accesibles al instante, sin replicación.

La composición de audiencias federada de Adobe Experience Platform ofrece una solución fácil y potente para conectar su almacén de datos empresarial directamente en Adobe Real-time Customer Data Platform y realizar consultas en las tablas de su almacén de datos.

## Pasos clave {#gs-steps}

La composición de audiencias federadas de Adobe le permite crear y actualizar audiencias de Adobe Experience Platform directamente desde la base de datos, sin ningún proceso de ingesta.

![diagrama](assets/FAC-diagram.png)

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

## Más información {#learn}

<!-- Workflow + Workflow activities-->



>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Configuración de ejecución"
>abstract="En esta sección, puede configurar las opciones relacionadas con la ejecución del flujo de trabajo, como el número de días que se mantiene el historial del flujo de trabajo."




>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Actividad no editable"
>abstract="Cuando una actividad de **Consulta** o **Enriquecimiento** se configura con datos adicionales en la consola, los datos de enriquecimiento se tienen en cuenta y pasan a la transición de salida, pero no se pueden editar."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Crear un vínculo"
>abstract="Defina la configuración del vínculo."
