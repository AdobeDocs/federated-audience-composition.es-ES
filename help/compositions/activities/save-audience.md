---
audience: end-user
title: Uso de la actividad Guardar audiencia
description: Aprenda a utilizar la actividad Guardar audiencia
source-git-commit: c151cc316eb9b5df6fa1d09f01455313195dfd07
workflow-type: tm+mt
source-wordcount: '358'
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

   ![](../assets/save-audience.png)

1. Especifique la etiqueta de la audiencia que desea crear.

1. Clic **Añadir asignación de audiencia** a continuación, elija los campos de origen y destino de la audiencia:

   * **Campo de audiencia de Source**:
   * **Campo de audiencia de destino**:

   Repita la operación para agregar tantas asignaciones de audiencia como sea necesario.

1. Seleccione la identidad y el área de nombres principales que se utilizarán para identificar los perfiles de destino en la base de datos:

   * **Campo de identidad principal**: seleccione el campo que desea utilizar para identificar los perfiles. Por ejemplo, su dirección de correo electrónico o número de teléfono.
   * **Área de nombres de identidad**: seleccione el área de nombres que se utilizará para identificar los perfiles, es decir, el tipo de datos que se utilizará como clave de identificación. Por ejemplo, si la dirección de correo electrónico se ha seleccionado como campo de identidad principal, el área de nombres de identidad **Correo electrónico** debe estar seleccionado. Si el identificador único es el número de teléfono, el área de nombres de identidad **Teléfono** debe estar seleccionado.

Después de ejecutar la maquetación, la audiencia resultante se guarda en Adobe Experience Platform y se puede acceder a ella desde el **Audiencias** menú.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
