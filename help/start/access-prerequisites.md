---
title: Acceder a composición de audiencia federada
description: Obtenga información sobre cómo acceder a la Composición de audiencias federada.
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 618d1675c28213d7a316f40cd624d282e01297f1
workflow-type: tm+mt
source-wordcount: '275'
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

Sus direcciones IP deben añadirse a la lista de permitidos de para permitir el acceso a su almacén de datos y utilizar Federated Audience Composition. Para añadir sus direcciones IP a la lista de permitidos, póngase en contacto con el representante de Adobe.

## Mecanismos de protección y limitaciones {#fac-guardrails}

* La composición de audiencias federada es compatible con el Escudo de privacidad y seguridad y se puede utilizar en todos los segmentos verticales, excepto en el sector sanitario. Actualmente, la Composición de audiencias federada no se puede conceder con licencia a los clientes que deseen introducir datos de estado. [Más información](https://experienceleague.adobe.com/en/docs/events/customer-data-management-voices-recordings/governance/healthcare-shield){target="_blank"}

* Los derechos, limitaciones de productos y protecciones de rendimiento enumerados en la [documentación de Adobe Real-time Customer Data Platform](https://experienceleague.adobe.com/en/docs/experience-platform/profile/guardrails){target="_blank"} se aplican a este complemento.
