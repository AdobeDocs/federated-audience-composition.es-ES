---
title: Acceder a composición de audiencia federada
description: Obtenga información sobre cómo acceder a la Composición de audiencias federada.
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 4e3a74ba09d3d1fa267c4587cb37f6e95831f7c8
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 2%

---

# Acceder a composición de audiencia federada {#fac-access}

## Paquetes y complementos {#package}

La composición de audiencias federada requiere paquetes de Adobe Real-time Customer Data Platform y Adobe Journey Optimizer Prime o Ultimate. Para acceder a esta funcionalidad, debe haber adquirido el complemento Federated Audience Composition.

>[!AVAILABILITY]
>
>Una vez que el usuario haya recibido la notificación de correo electrónico de bienvenida del Adobe, la interfaz podría tardar unas horas más en actualizarse y las funciones disponibles para el usuario.

## Permisos {#permissions}

Al adquirir el complemento Composición de audiencia federada, se crea un perfil de producto para cada zona protegida activa en ese momento. Este perfil de producto se crea en el Admin Console en la tarjeta de producto **Adobe Experience Platform** y sigue esta convención de nombres: `ACP_FAC - <<SandboxName>> - admin.` Para acceder a la Composición de audiencia federada para una zona protegida específica, los usuarios deben agregarse al perfil de producto creado para esa zona protegida.

Por ejemplo, si se activa una nueva zona protegida denominada &quot;fac-test&quot;, se crea un perfil de producto correspondiente &quot;ACP_FAC - fac-test - admin&quot;. Para acceder a la Composición de audiencia federada con esta zona protegida, los usuarios deben añadirse a este perfil de producto.

## Listado de IP permitidas {#ip}

Para permitir que Federated Audience Composition acceda de forma segura a sus bases de datos, póngase en contacto con su representante de Adobe para obtener las direcciones IP de los servidores de Federated Audience Composition que accederán a ellas.

Añada estas direcciones IP a su lista de permitidos para conceder acceso a Composición de audiencia federada.&quot;

## Mecanismos de protección y limitaciones {#fac-guardrails}

* La composición de audiencias federada es compatible con el Escudo de privacidad y seguridad y se puede utilizar en todos los segmentos verticales, excepto en el sector sanitario. Actualmente, la Composición de audiencias federada no se puede conceder con licencia a los clientes que deseen introducir datos de estado. [Más información](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* Los derechos, limitaciones de productos y protecciones de rendimiento enumerados en la [documentación de Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} se aplican a este complemento.
