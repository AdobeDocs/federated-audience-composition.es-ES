---
title: Privacidad y seguridad en la composición de audiencias federadas
description: Descubra cómo la Composición de audiencias federada trata la privacidad y seguridad de los datos de usuario, incluidas funciones como la gobernanza de datos, la aplicación del consentimiento, el control de acceso, el cifrado de datos y el cumplimiento de la privacidad.
source-git-commit: b505a4f0ac9ac7350e2879f4f54f93a69b73f96c
workflow-type: tm+mt
source-wordcount: '1085'
ht-degree: 1%

---


# Privacidad y seguridad en Federated Audience Composition

La composición federada de audiencias cumple con numerosas prácticas de seguridad para proteger los datos durante el procesamiento.

## Privacy Service {#privacy}

La Composición de audiencias federada proporciona los datos federados que Adobe Experience Platform y Adobe Journey Optimizer deben utilizar. Sin embargo, la Composición de audiencias federada **no** almacena los datos de clientes de ninguno de los almacenes de datos. Como resultado, puede utilizar Adobe Experience Platform Privacy Service para cumplir con las solicitudes del interesado y de eliminación de datos.

Por ejemplo, cuando se crea una audiencia utilizando el bloque de actividad de guardado en el lienzo de maquetación, la audiencia resultante se almacena en el lago de datos en Experience Platform como una audiencia externa. Esta audiencia externa está marcada con su campo de identidad y área de nombres de identidad. Como resultado, puede utilizar Privacy Service para acceder a esos perfiles y eliminarlos con una audiencia externa.

Como alternativa, después de crear un enriquecimiento de perfil utilizando la actividad de guardar perfil en el lienzo de maquetación, el enriquecimiento resultante se almacena en Experience Platform como esquema habilitado para perfiles y conjunto de datos habilitado para perfiles. Estos datos de enriquecimiento están marcados con un campo de identidad y un área de nombres de identidad. Como resultado, puede utilizar Privacy Service para acceder a estos perfiles y limpiarlos.

Para obtener más información sobre Privacy Service, lea la [descripción general de Privacy Service](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/home){target="_blank"}.

### Solicitudes de privacidad {#privacy-requests}

En Privacy Service, puede crear y administrar solicitudes de privacidad individuales para acceder a datos de clientes y eliminarlos de Federated Audience Composition. Privacy Service proporciona una [interfaz de usuario](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=es){target="_blank"} y una [API RESTful](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/api/overview){target="_blank"} para ayudarle a administrar las solicitudes de datos de los clientes.

Para obtener más información sobre cómo crear y administrar solicitudes de privacidad, lea [trabajos de privacidad en la guía de la interfaz de usuario de Privacy Service](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Aplicación de políticas de consentimiento {#consent}

Federated Audience Composition, a través de Experience Platform, ofrece herramientas que le permiten automatizar la aplicación del consentimiento, lo que garantiza que está activando audiencias en función del consentimiento proporcionado a sus clientes.

Por ejemplo, cuando se crea una audiencia utilizando el bloque de actividad de guardado en el lienzo de maquetación, la audiencia resultante se almacena en el lago de datos en Experience Platform como una audiencia externa. Experience Platform admite automáticamente la validación del consentimiento durante la activación. Para obtener más información, lea las [Preguntas frecuentes sobre el servicio de segmentación](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Como alternativa, después de crear un enriquecimiento de perfil utilizando la actividad de guardar perfil en el lienzo de maquetación, el enriquecimiento resultante se almacena en Experience Platform como esquema habilitado para perfiles y conjunto de datos habilitado para perfiles. Para los perfiles existentes, los atributos de consentimiento disponibles se respetan automáticamente durante la activación. Para los perfiles nuevos, los atributos de consentimiento proporcionados durante la ingesta de perfiles se respetan automáticamente durante la activación. Para obtener más información sobre la aplicación de consentimientos a los perfiles, lea la [guía de grupos de campos de consentimientos y preferencias](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Para obtener más información sobre la aplicación de consentimientos, lea la [guía de la interfaz de usuario para administrar directivas](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Ciclo de vida de los datos {#data-lifecycle}

Dado que la Composición de audiencias federada **no** almacena los datos de clientes de ninguno de los almacenes de datos, puede usar Experience Platform para administrar el ciclo de vida de los datos. Con la administración avanzada del ciclo de vida de los datos, puede administrar el ciclo de vida de los datos tanto a nivel de conjunto de datos como de registro.

Por ejemplo, cuando se crea una audiencia utilizando el bloque de actividad de guardado en el lienzo de maquetación, la audiencia resultante se almacena en el lago de datos de Experience Platform como una audiencia externa. Dado que estos datos están **no** almacenados en la Composición de audiencias federada, los datos de audiencia y los conjuntos de datos correspondientes se eliminan automáticamente cuando la audiencia se elimina en Audience Portal.

Como alternativa, después de crear un enriquecimiento de perfil utilizando la actividad de guardar perfil en el lienzo de maquetación, el enriquecimiento resultante se almacena en Experience Platform como esquema habilitado para perfiles y conjunto de datos habilitado para perfiles. Como resultado, puede usar Ciclo de vida de datos para acceder a los perfiles y limpiarlos.

Para obtener más información sobre el uso del ciclo de vida de datos, lea [Resumen del ciclo de vida de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Etiquetas de uso de datos {#data-usage-labels}

Las etiquetas de uso de datos permiten categorizar conjuntos de datos y campos en función de las políticas de gobernanza que se aplican a esos datos. Después de crear una audiencia con composiciones, puede aplicar las etiquetas de datos adecuadas al esquema resultante para asegurarse de que cumple las restricciones de uso requeridas.

Para obtener más información sobre cómo usar etiquetas de datos, lea la [descripción general de las etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Cifrado {#encryption}

La composición flexible de audiencias proporciona cifrado mediante cifrado de datos en reposo, cifrado de datos en tránsito y claves administradas por el cliente.

Los datos en reposo hacen referencia a los datos de clientes que se utilizan en la Composición de audiencias federada. El proveedor de servicios en la nube cifra los datos y estos se utilizan en la Composición de audiencias federada en su forma cifrada.

Los datos en tránsito se refieren a los datos del cliente cuando se mueven de un componente a otro en la Composición de audiencias federada. Los datos se mantienen cifrados en todos los componentes de Composición de audiencia federada mediante TLS 1.3 en HTTPS.

Para obtener más información sobre cómo administra Adobe el cifrado de datos, lea la guía sobre el cifrado de datos [en Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Claves gestionadas por el cliente {#customer-managed-keys}

Las claves administradas por el cliente le permiten tener el control de sus datos, ya que le permiten utilizar sus propias claves de cifrado para cifrar sus datos. Dado que la Composición de audiencias federada **no** almacena ninguno de los datos del cliente, puede usar claves administradas por el cliente directamente en las audiencias y enriquecimientos resultantes, ya que se almacenarán en el lago de datos en Experience Platform.

Para obtener más información sobre las claves administradas por el cliente, lea la [guía de claves administradas por el cliente](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Registro de auditoría {#audit-log}

Todas las operaciones de creación, lectura, actualización y eliminación realizadas en Composición de audiencia federada se registran en la pista de auditoría. Puede utilizar este registro de auditoría para realizar un seguimiento de estas acciones, exigir responsabilidades y admitir auditorías de cumplimiento.

Para obtener más información, lea la [descripción general de la pista de auditoría](/help/admin/audit-trail.md){target="_blank"}.

## Control de acceso {#access-control}

Puede controlar el acceso a la Composición de audiencia federada tanto en el nivel de campo como en el de rol. Puede utilizar estos controles de acceso para aplicar políticas de gobernanza de datos, limitar la exposición de información confidencial y alinear el acceso con las responsabilidades del usuario.

Para obtener más información sobre el control de acceso en Federated Audience Composition, lea la [Guía de acceso a Federated Audience Composition](/help/start/feature-access.md){target="_blank"}.

## Localización de datos {#data-localization}

La composición de audiencias federada **no** almacena datos de clientes. Como resultado, debe asegurarse de que **solo** conecta las bases de datos externas con la región de zona protegida correspondiente para mantener los datos en la misma región. Si conecta una base de datos de otra región a una zona protegida, Adobe **no** es responsable de la localización de datos.

## Pasos siguientes {#next-steps}

Después de leer esta guía, tendrá una mejor comprensión de las funciones de privacidad y seguridad que se utilizan para Federated Audience Composition, incluidas la gobernanza de datos, el cumplimiento de la privacidad, la aplicación del consentimiento, la administración del ciclo vital de datos y el control de acceso.
