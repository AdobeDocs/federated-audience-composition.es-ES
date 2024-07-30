---
title: Requisitos previos y protecciones para la composición de audiencias federada
description: Conozca los requisitos previos, permisos y protecciones para la Composición de audiencias federada
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 61ad8899f7de601b64c7b42cb873a172fcaea145
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 13%

---

# Requisitos previos y protecciones {#fac-access}

La composición de audiencias federada requiere paquetes de Adobe Real-time Customer Data Platform o Adobe Journey Optimizer **Prime** o **Ultimate**. Para acceder a esta funcionalidad, debe haber adquirido el complemento Federated Audience Composition.

>[!AVAILABILITY]
>
>Una vez recibido el correo electrónico de bienvenida de Adobe, la interfaz se actualiza y las funciones estarán disponibles para el usuario luego de unas horas.

## Permisos {#permissions}

Al adquirir el complemento Composición de audiencia federada, se crea un perfil de producto para cada zona protegida activa en ese momento. Este perfil de producto se crea en el Admin Console en la tarjeta de producto **Adobe Experience Platform** y sigue esta convención de nombres: `ACP_FAC - <<SandboxName>> - admin.` Para acceder a la Composición de audiencia federada para una zona protegida específica, los usuarios deben agregarse al perfil de producto creado para esa zona protegida.

Por ejemplo, si se activa una nueva zona protegida denominada &quot;fac-test&quot;, se crea un perfil de producto correspondiente &quot;ACP_FAC - fac-test - admin&quot;. Para acceder a la Composición de audiencia federada con esta zona protegida, los usuarios deben añadirse a este perfil de producto.

## Listado de IP permitidas {#ip}

Para permitir que Federated Audience Composition acceda de forma segura a sus bases de datos, póngase en contacto con su representante de Adobe para obtener las direcciones IP de los servidores de Federated Audience Composition que accederán a ellas.

Añada estas direcciones IP a la lista de permitidos para conceder acceso a Composición de audiencias federada.

## Mecanismos de protección y limitaciones {#fac-guardrails}

* El uso de audiencias y atributos de Federated Audience Composition no está disponible actualmente con Healthcare Shield y Privacy and Security Shield.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Los derechos, limitaciones de productos y protecciones de rendimiento enumerados en la [documentación de Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails){target="_blank"} se aplican a este complemento.
