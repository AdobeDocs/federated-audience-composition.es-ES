---
title: Privacidad y seguridad en la composición de público federado
description: Descubra cómo la composición de público federado aborda el tema de la privacidad y seguridad de los datos de usuario, incluyendo funciones como la gobernanza de datos, la aplicación del consentimiento, el control de acceso, el cifrado de datos y el cumplimiento de la privacidad.
exl-id: 677e26e7-1294-4f62-a5ce-17b65e84c65e
source-git-commit: 8076a7851d0cd5cd84a7c48c6f1783b452864903
workflow-type: ht
source-wordcount: '1085'
ht-degree: 100%

---

# Privacidad y seguridad en la composición de público federado

La composición de público federado cumple con numerosas prácticas de seguridad para proteger sus datos durante el procesamiento.

## Privacy Service {#privacy}

La composición de público federado proporciona los datos federados para que Adobe Experience Platform y Adobe Journey Optimizer los utilicen. Sin embargo, la composición de público federado **no** almacena datos de los clientes procedentes de los almacenes de datos. Como resultado, puede utilizar Adobe Experience Platform Privacy Service para cumplir con las solicitudes de los interesados y de eliminación de datos.

Por ejemplo, cuando se crea un público utilizando el bloque de guardar actividad en el lienzo de composición, el público resultante se almacena en el lago de datos de Experience Platform como un público externo. Este público externo está marcado con su campo de identidad y espacio de nombres de identidad. Como resultado, puede utilizar Privacy Service para acceder a esos perfiles y eliminarlos con un público externo.

Como alternativa, después de crear un enriquecimiento de perfil utilizando la actividad de guardar perfil en el lienzo de la composición, el enriquecimiento resultante se almacena en Experience Platform como un esquema habilitado para perfiles y un conjunto de datos habilitado para perfiles. Estos datos de enriquecimiento están marcados con un campo de identidad y un espacio de nombres de identidad. Como resultado, puede utilizar Privacy Service para acceder a estos perfiles y limpiarlos.

Para obtener más información sobre Privacy Service consulte la [información general sobre Privacy Service](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/home){target="_blank"}.

### Solicitudes de privacidad {#privacy-requests}

En Privacy Service, puede crear y administrar las solicitudes individuales para acceder a datos de los clientes y eliminarlos de la composición de público federado de Adobe. Privacy Service proporciona una [interfaz de usuario](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=es){target="_blank"} y una [API de RESTful](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/api/overview){target="_blank"} para administrar las solicitudes de datos de los clientes.

Para obtener más información sobre cómo crear y administrar solicitudes de privacidad, consulte los [trabajos de privacidad en la guía de la interfaz de usuario de Privacy Service](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/ui/user-guide){target="_blank"}.

## Aplicación de las políticas de consentimiento {#consent}

La composición de público federado, a través de Experience Platform, ofrece herramientas que le permiten automatizar la aplicación del consentimiento, lo que garantiza que active públicos en función del consentimiento proporcionado a sus clientes.

Por ejemplo, cuando se crea un público utilizando el bloque de guardar actividad en el lienzo de composición, el público resultante se almacena en el lago de datos de Experience Platform como un público externo. Experience Platform admite automáticamente la validación del consentimiento durante la activación. Para obtener más información, lea las [Preguntas frecuentes sobre el servicio de segmentación](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/faq#consent){target="_blank"}.

Como alternativa, después de crear un enriquecimiento de perfil utilizando la actividad de guardar perfil en el lienzo de la composición, el enriquecimiento resultante se almacena en Experience Platform como un esquema habilitado para perfiles y un conjunto de datos habilitado para perfiles. En los perfiles existentes, los atributos de consentimiento disponibles se respetan automáticamente durante la activación. En los perfiles nuevos, los atributos de consentimiento proporcionados durante la ingesta de perfiles se respetan automáticamente durante la activación. Para obtener más información sobre la aplicación de consentimientos a los perfiles, consulte la [guía del grupo de campos de consentimientos y preferencias](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/field-groups/profile/consents){target="_blank"}.

Para obtener más información sobre la aplicación de consentimientos, consulte la [guía de la interfaz de usuario para administrar políticas](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/policies/user-guide#consent-policy){target="_blank"}.

## Ciclo de vida de los datos {#data-lifecycle}

Dado que la composición de público federado **no** almacena los datos de los clientes procedentes de los almacenes de datos, puede usar Experience Platform para administrar el ciclo de vida de los datos. Con la administración avanzada del ciclo de vida de los datos, puede administrar el ciclo de vida de los datos tanto a nivel de conjunto de datos como de registro.

Por ejemplo, cuando se crea un público utilizando el bloque de guardar actividad en el lienzo de la composición, el público resultante se almacena en el lago de datos de Experience Platform como un público externo. Dado que estos datos **no** están almacenados en la composición de público federado, los datos de público y los conjuntos de datos correspondientes se eliminan automáticamente cuando el público se elimina en Audience Portal.

Como alternativa, después de crear un enriquecimiento de perfil utilizando la actividad de guardar perfil en el lienzo de la composición, el enriquecimiento resultante se almacena en Experience Platform como un esquema habilitado para perfiles y un conjunto de datos habilitado para perfiles. Como resultado, puede usar el ciclo de vida de los datos para acceder a los perfiles y limpiarlos.

Para obtener más información sobre el ciclo de vida de los datos, consulte la [información general sobre el ciclo de vida de los datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-lifecycle/home){target="_blank"}.

## Etiquetas de uso de datos {#data-usage-labels}

Las etiquetas de uso de datos permiten categorizar conjuntos de datos y campos en función de las políticas de gobernanza que se aplican a esos datos. Después de crear un público usando composiciones, puede aplicar las etiquetas de datos adecuadas al esquema resultante para asegurarse de que cumple las restricciones de uso requeridas.

Para obtener más información sobre el uso de etiquetas de datos, lea la [información general sobre las etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/overview){target="_blank"}.

## Cifrado {#encryption}

La composición de público flexible proporciona cifrado mediante el cifrado de datos en reposo, el cifrado de datos en tránsito y claves administradas por el cliente.

Los datos en reposo hacen referencia a los datos de clientes que se utilizan en la composición de público federado. El proveedor de servicios en la nube cifra los datos y estos se utilizan en la composición de público federado en su forma cifrada.

Los datos en tránsito hacen referencia a los datos del cliente cuando se mueven de un componente a otro en la composición de público federado. Los datos se mantienen cifrados en todos los componentes de composición de público federado mediante TLS 1.3 a través de HTTPS.

Para obtener más información sobre cómo administra Adobe el cifrado de datos, lea la guía sobre el [cifrado de datos en Experience Platform](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/encryption){target="_blank"}.

### Claves administradas por el cliente {#customer-managed-keys}

Las claves administradas por el cliente le permiten tener el control de sus datos, ya que le permiten utilizar sus propias claves de cifrado para cifrar sus datos. Dado que la composición de público federado **no** almacena los datos del cliente, puede usar claves administradas por el cliente directamente en los públicos y enriquecimientos resultantes, ya que se almacenan en el lago de datos en Experience Platform.

Para obtener más información sobre las claves administradas por el cliente, consulte la [guía de claves administradas por el cliente](https://experienceleague.adobe.com/es/docs/experience-platform/landing/governance-privacy-security/customer-managed-keys/overview){target="_blank"}.

## Registro de auditoría {#audit-log}

Todas las operaciones de creación, lectura, actualización y eliminación realizadas en la composición de público federado se registran en la pista de auditoría. Puede utilizar este registro de auditoría para realizar un seguimiento de estas acciones, exigir responsabilidades y respaldar las auditorías de cumplimiento.

Para obtener más información, lea la [información general sobre la pista de auditoría](/help/admin/audit-trail.md){target="_blank"}.

## Control de acceso {#access-control}

Puede controlar el acceso a la composición de público federado tanto a nivel de campo como de función. Puede utilizar estos controles de acceso para aplicar políticas de gobernanza de datos, limitar la exposición de información confidencial y alinear el acceso con las responsabilidades del usuario.

Para obtener más información sobre el control de acceso en la composición de público federado, consulte la [guía de acceso a la composición de público federado](/help/start/feature-access.md){target="_blank"}.

## Localización de datos {#data-localization}

La composición de público federado **no** almacena los datos de los clientes. Como resultado, debe asegurarse de conectar **solamente** las bases de datos externas con la región de zona protegida correspondiente para mantener los datos en la misma región. Si conecta una base de datos de otra región a una zona protegida, Adobe **no** se hace responsable de la localización de los datos.

## Pasos siguientes {#next-steps}

Después de leer esta guía, comprenderá mejor las funciones de privacidad y seguridad que se utilizan para la composición de público federado, entre ellas, la gobernanza de datos, el cumplimiento de la privacidad, la aplicación del consentimiento, la administración del ciclo vital de datos y el control de acceso.
