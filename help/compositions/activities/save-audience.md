---
audience: end-user
title: Uso de la actividad Guardar audiencia
description: Aprenda a utilizar la actividad de bifurcación
source-git-commit: 05a023a7f7aab719f3771030a7ac8bba57e5bee3
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 12%

---

# Guardado de público {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Guardar un público"
>abstract="Utilice esta actividad para actualizar una audiencia existente o crear una nueva a partir de la población calculada en sentido ascendente en la composición. Los públicos creados se añaden a la lista de públicos y están disponibles en el menú **Públicos**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Generar transición de salida"
>abstract="Utilice esta opción si desea añadir una transición después de la actividad **Guardado de público**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Campo de identidad principal"
>abstract="Seleccione la identidad principal que se utilizará para los perfiles."
>additional-url="https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Obtenga más información en la documentación de Experience Platform"


>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Espacio de nombres de identidad"
>abstract="Seleccione el área de nombres que se utilizará para los perfiles."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces" text="Obtenga más información en la documentación de Experience Platform"



El **Guardar audiencia** esta actividad le permite actualizar una audiencia existente o crear una nueva a partir de la población calculada en sentido ascendente en una composición. Las audiencias creadas se añaden a la lista de audiencias de aplicación y están disponibles a través del **Audiencias** menú.

Esta actividad se utiliza esencialmente para mantener los grupos de población calculados en la misma composición, convirtiéndolos en audiencias reutilizables. Conéctelo a otras actividades de segmentación, como una **Crear audiencia** o una **Combinar** actividad.

## Configuración de la actividad Guardar audiencia {#save-audience-configuration}

Siga estos pasos para configurar el **Guardar audiencia** actividad:

1. Añadir un **Guardar audiencia** actividad a su composición.

1. En el **Modo** , seleccione la acción que desee llevar a cabo:

   * **Crear o actualizar una audiencia existente**: defina un **Etiqueta de audiencia**. Si la audiencia ya existe, se actualiza; de lo contrario, se crea una nueva.

   * **Actualizar una audiencia existente**: elija el **Audiencia** desea actualizar entre la lista de audiencias existentes.

1. Seleccione el **Modo de actualización** que se aplicará a las audiencias existentes:

   * **Reemplazar contenido de audiencia por nuevos datos**: todo el contenido de la audiencia se sustituye. Se pierden los datos antiguos. Solo se conservan los datos de la transición entrante de la actividad Guardar audiencia. Esta opción borra el tipo de audiencia y la dimensión de segmentación de la audiencia actualizada.

   * **Audiencia completa con nuevos datos**: el contenido de audiencia anterior se conserva y se añaden a él los datos de la transición de entrada de la actividad guardar audiencia.

1. Compruebe la **Generación de una transición saliente** si desea añadir una transición después de la variable **Guardar audiencia** actividad.

El contenido de la audiencia guardada está disponible en la vista de detalles de la audiencia, a la que se puede acceder desde el **Audiencias** menú. Las columnas disponibles en esta vista corresponden a las columnas de la transición entrante de la variable **Guardar audiencia** actividad.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
