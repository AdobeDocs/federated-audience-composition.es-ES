---
title: Requisitos previos y protecciones para la composición de público federado
description: Conozca los requisitos previos, permisos y protecciones para la composición de público federado
exl-id: 661a838f-146e-4d68-bb2d-319827caee3a
source-git-commit: 9b951f74443ac149e837c3f52ca265acabd407b9
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 92%

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
* Google BigQuery
* Snowflake
* Vertica Analytics
* Microsoft Fabric

Puede aprender a crear una conexión con estos sistemas en la [descripción general de las conexiones](../connections/home.md).

## Zonas protegidas

Al adquirir la Composición de público federado, tiene derecho a dos zonas protegidas. Para cualquier solicitud de aprovisionamiento de zona protegida adicional, póngase en contacto con su representante de Adobe.

Para ver la lista de las zonas protegidas de composición de público federado activas, siga los pasos que se indican a continuación:

1. Desde la composición de público federado, acceda al menú **[!UICONTROL Uso de licencias]** en **[!UICONTROL Administración]**.

1. Seleccione el icono ![](assets/do-not-localize/Smock_InfoOutline_18_N.svg) de **[!UICONTROL Volumen total de salida de datos]** para acceder a las propiedades de su zona protegida.

   ![](assets/sandbox_1.png)

1. La información sobre la zona protegida se muestra en la ventana emergente Propiedades.

   ![](assets/sandbox_2.png)

## Permisos {#permissions}

Para acceder a la Composición de público federado, los usuarios deben añadirse al perfil de producto específico de la zona protegida creado tras la compra y se les debe asignar el permiso **[!UICONTROL Administrar datos federados]**. [Más información](/help/governance-privacy-security/access-control.md)

## Lista de IP permitidas {#ip}

Para permitir de forma segura que composición de público federado acceda a sus bases de datos, póngase en contacto con su representante de Adobe para obtener las direcciones IP de los servidores de composición de público federado que accederán a ellas. Estas direcciones IP se muestran al añadir una base de datos federada en la interfaz de usuario de Adobe Experience Platform. [Más información](../connections/home.md)

Añada estas direcciones IP a la lista de permitidos para conceder acceso a la composición de público federado.

## Combinar políticas {#merge-policies}

Si su zona protegida utiliza una política de combinación de **prioridad del conjunto de datos**, póngase en contacto con el Servicio de atención al cliente de Adobe para añadir el conjunto de datos `Halos UPS` a su política de combinación.

Para obtener más información sobre las políticas de combinación, consulte la [información general sobre políticas de combinación](https://experienceleague.adobe.com/es/docs/experience-platform/profile/merge-policies/overview).

## Mecanismos de protección y limitaciones {#fac-guardrails}

* Los derechos, limitaciones de productos y protecciones de rendimiento enumerados en la [documentación de Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/es/docs/experience-platform/profile/guardrails){target="_blank"} se aplican a la Composición de público federado.

* La composición de público federado admite la exportación de públicos grandes, con tamaños de archivo superiores a 1 GB. Para obtener un rendimiento óptimo, el tamaño máximo de archivo recomendado es de hasta 20 GB.
