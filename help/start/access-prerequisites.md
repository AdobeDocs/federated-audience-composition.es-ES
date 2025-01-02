---
title: Requisitos previos y protecciones para la composición de público federado
description: Conozca los requisitos previos, permisos y protecciones para la composición de público federado
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: d44813e447de92fe8ba7e43c7b0f0ad9f0b07239
workflow-type: ht
source-wordcount: '335'
ht-degree: 100%

---

# Requisitos previos y protecciones {#fac-access}

La composición de público federado requiere los paquetes de Adobe Real-Time Customer Data Platform o Adobe Journey Optimizer **Prime**, o **Ultimate**. Para acceder a esta función es preciso haber adquirido el complemento Composición de público federado.

>[!AVAILABILITY]
>
>Una vez recibido el correo electrónico de bienvenida de Adobe, la interfaz se actualiza y las funciones estarán disponibles para el usuario luego de unas horas.

## Sistemas compatibles {#supported-systems}

La composición de público federado admite los siguientes almacenes en la nube:

* Amazon Redshift
* Azure Synapse
* Databricks
* Google Big Query
* Snowflake
* Vertica Analytics

Aprenda a crear una conexión con estos sistemas en [esta página](../connections/connections.md).

## Zonas protegidas

Al adquirir el complemento composición de público federado, tiene derecho a dos zonas protegidas. Para cualquier solicitud de aprovisionamiento de zona protegida adicional, póngase en contacto con su representante de Adobe.

## Permisos {#permissions}

Al adquirir el complemento Composición de público federado, se crea un perfil de producto para cada zona protegida activa en ese momento. Este perfil de producto se crea en Admin Console, en la tarjeta de producto **Adobe Experience Platform** y sigue la convención de nomenclatura siguiente: `ACP_FAC - <<SandboxName>> - admin.` para acceder a la Composición de público federado para una zona protegida específica, los usuarios deben agregarse al perfil de producto creado para esa zona protegida.

Por ejemplo, si se activa una nueva zona protegida denominada «fac-test», se crea un perfil «ACP_FAC - fac-test - admin» de producto correspondiente. Para acceder a la composición de público federado con esta zona protegida, los usuarios deben añadirse a este perfil de producto.

## Lista de IP permitidas {#ip}

Para permitir de forma segura que composición de público federado acceda a sus bases de datos, póngase en contacto con su representante de Adobe para obtener las direcciones IP de los servidores de composición de público federado que accederán a ellas. Estas direcciones IP se muestran al añadir una base de datos federada en la interfaz de usuario de Adobe Experience Platform. [Más información](../connections/connections.md)

Añada estas direcciones IP a la lista de permitidos para conceder acceso a composición de público federado.

## Mecanismos de protección y limitaciones {#fac-guardrails}

* La composición de público federado no está disponible actualmente para los clientes [que están ingiriendo datos de mantenimiento](https://experienceleague.adobe.com/es/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}. [Más información](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences){target="_blank"}

<!--
* Federated Audience Composition is compatible with Privacy & Security Shield and can be used in all verticals except for healthcare industries. Currently, Federated Audience Composition cannot be licensed to customers looking to ingest health data. [Learn more](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}-->

* Los derechos, limitaciones de productos y protecciones de rendimiento se enumeran en la [documentación de Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails){target="_blank"}.
