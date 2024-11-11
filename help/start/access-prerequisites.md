---
title: Requisitos previos y protecciones para la composición de público federado
description: Conozca los requisitos previos, permisos y protecciones para la composición de público federado
badge: label="Disponibilidad limitada" type="Informative"
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: de5955ad481061c6f8e488c86fc9666736a2fa1e
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 92%

---

# Requisitos previos y protecciones {#fac-access}

La composición de público federado requiere los paquetes de Adobe Real-Time Customer Data Platform o Adobe Journey Optimizer **Prime**, o **Ultimate**. Para acceder a esta función es preciso haber adquirido el complemento Composición de público federado.

>[!AVAILABILITY]
>
>Una vez recibido el correo electrónico de bienvenida de Adobe, la interfaz se actualiza y las funciones estarán disponibles para el usuario luego de unas horas.

## Sistemas compatibles {#supported-systems}

La Composición de audiencia federada admite los siguientes almacenes de nube:

* Amazon Redshift
* Azure Synapse
* Databricks
* Google Big Query
* Snowflake
* Vertica Analytics

Aprenda a crear una conexión con estos sistemas en [esta página](../connections/connections.md).

## Permisos {#permissions}

Al adquirir el complemento Composición de público federado, se crea un perfil de producto para cada zona protegida activa en ese momento. Este perfil de producto se crea en Admin Console, en la tarjeta de producto **Adobe Experience Platform** y sigue la convención de nomenclatura siguiente: `ACP_FAC - <<SandboxName>> - admin.` para acceder a la Composición de público federado para una zona protegida específica, los usuarios deben agregarse al perfil de producto creado para esa zona protegida.

Por ejemplo, si se activa una nueva zona protegida denominada «fac-test», se crea un perfil «ACP_FAC - fac-test - admin» de producto correspondiente. Para acceder a la composición de público federado con esta zona protegida, los usuarios deben añadirse a este perfil de producto.

## Lista de IP permitidas {#ip}

Para permitir que Composición de público federado acceda de forma segura a sus bases de datos, póngase en contacto con su representante de Adobe para obtener las direcciones IP de los servidores de composición de público federado que accederán a ellas.

Añada estas direcciones IP a la lista de permitidos para conceder acceso a composición de público federado.

## Mecanismos de protección y limitaciones {#fac-guardrails}

* En estos momentos, la composición de público federado no está disponible para los clientes [que están ingiriendo datos de mantenimiento](https://experienceleague.adobe.com/es/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"} ni para los clientes del programa de protección de la seguridad y la privacidad de Adobe Journey Optimizer. [Más información](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}.

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Los derechos, limitaciones de productos y protecciones de rendimiento se enumeran en la [documentación de Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails){target="_blank"}.
