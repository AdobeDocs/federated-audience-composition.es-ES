---
audience: end-user
title: Uso de la actividad Guardar audiencia
description: Aprenda a utilizar la actividad Guardar audiencia
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 6e04c42bf4b83448673851b97227faf953638d1e
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 25%

---


# Guardado de público {#save-audience}

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience"
>title="Guardar un público"
>abstract="Utilice esta actividad para actualizar un público existente o crear uno nuevo a partir de la población calculada en sentido ascendente en la composición. Los públicos creados se añaden a la lista de públicos y están disponibles en el menú **Públicos**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_outbound"
>title="Generar transición de salida"
>abstract="Utilice esta opción si desea añadir una transición después de la actividad **Guardado de público**."

>[!CONTEXTUALHELP]
>id="dc_orchestration_save_audience_primary_identity"
>title="Campo de identidad principal"
>abstract="Seleccione la identidad principal que se utilizará para los perfiles."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-platform/xdm/ui/fields/identity#define-a-identity-field" text="Más información en la Documentación de Experience Platform"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveaudience_namespace"
>title="Espacio de nombres de identidad"
>abstract="Seleccione el área de nombres que se utilizará para los perfiles."
>additional-url="https://experienceleague.adobe.com/es/docs/experience-platform/identity/features/namespaces" text="Más información en la Documentación de Experience Platform"

La actividad **Guardar audiencia** le permite actualizar una audiencia existente o crear una nueva a partir de la población calculada en sentido ascendente en una composición. Las audiencias creadas se agregan a la lista de audiencias de aplicación y están disponibles a través del menú **Audiencias**.

Esta actividad se utiliza esencialmente para mantener los grupos de población calculados en la misma composición, convirtiéndolos en audiencias reutilizables. Conéctelo a otras actividades de segmentación, como una **audiencia de compilación** o una actividad **Combinar**.

## Configuración de la actividad Guardar audiencia {#save-audience-configuration}

Siga estos pasos para configurar la actividad **Guardar audiencia**:

1. Agregue una actividad **Guardar audiencia** a su composición.

   ![](../assets/save-audience.png)

1. Especifique la etiqueta de la audiencia que desea crear.

   >[!IMPORTANT]
   >
   >La etiqueta de audiencia debe ser única dentro de la zona protegida actual. No puede ser la misma etiqueta que cualquier audiencia existente.

1. Haga clic en **Agregar asignación de audiencia** y, a continuación, elija los campos de audiencia de origen y destino:

   * **Campo de audiencia de Source**:
   * **Campo de audiencia de destino**:

   Repita la operación para agregar tantas asignaciones de audiencia como sea necesario.

1. Seleccione la identidad y el área de nombres principales que se utilizarán para identificar los perfiles de destino en la base de datos:

   * **Campo de identidad principal**: seleccione el campo que se usará para identificar los perfiles. Por ejemplo, su dirección de correo electrónico o número de teléfono.
   * **Área de nombres de identidad**: seleccione el área de nombres que se utilizará para identificar los perfiles, es decir, el tipo de datos que se utilizará como clave de identificación. Por ejemplo, si la dirección de correo electrónico se ha seleccionado como campo de identidad principal, se debe seleccionar el área de nombres de identidad **Correo electrónico**. Si el identificador único es el número de teléfono, se debe seleccionar el área de nombres de identidad **Teléfono**.

Después de ejecutar la composición, la audiencia resultante se guarda en Adobe Experience Platform <!-- to check--> y se puede obtener acceso a ella desde el menú **Audiencias**.

<!--

## Example{#save-audience-example}

The following example illustrates a simple audience update from targeting. A scheduler is added to run the workflow once a month. A query recovers all the profiles subscribed to the different application services available. The **Save audience** activity updates the audience by deleting profiles that have unsubscribed from the service since the last workflow execution and by adding the newly subscribed profiles.
-->
