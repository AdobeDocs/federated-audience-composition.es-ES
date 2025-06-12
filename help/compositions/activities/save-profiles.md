---
audience: end-user
title: Uso de la actividad Guardar perfiles
description: Aprenda a utilizar la actividad Guardar perfiles
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: ca975be136155f69bc84362fde8c283b1c4edffe
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 18%

---

# Guardar perfiles {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Guardar perfiles"
>abstract="La actividad Guardar perfiles permite enriquecer perfiles de Experience Platform federando datos de data warehouses externos, lo que permite mejorar los perfiles de los clientes con atributos adicionales. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Seleccionar esquema de Experience Platform"
>abstract="Elija el esquema de Experience Platform para los perfiles."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Seleccionar el campo de identidad principal"
>abstract="Seleccione la identidad principal que se utilizará para identificar los perfiles segmentados en la base de datos."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Seleccionar esquema de Experience Platform"
>abstract="Elija el esquema de Experience Platform para los perfiles."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode"
>title="Guardar modo de actualización de perfil"
>abstract="Los modos de actualización disponibles para la actividad Guardar perfil incluyen actualización completa e incremental."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_full"
>title="Actualización completa"
>abstract="El modo de actualización completa actualiza el conjunto completo de perfiles para el enriquecimiento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_updatemode_incremental"
>title="Actualización incremental"
>abstract="El modo de actualización incremental actualiza los perfiles que se han modificado desde que se ejecutó el último enriquecimiento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentityfield"
>title="Campo de identidad principal"
>abstract="El campo de identidad principal indica la fuente de verdad al combinar perfiles para el enriquecimiento."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_requiredfieldscheck"
>title="Criterios de campos obligatorios"
>abstract="Un campo obligatorio es un atributo que debe rellenarse para cada perfil o registro al exportar datos. Si falta un campo obligatorio, la exportación no es completa ni válida."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitycheck"
>title="Criterios del campo de identidad principal"
>abstract="El identificador único de cada perfil o registro. Esto garantiza que cada registro se pueda reconocer y hacer coincidir de forma distintiva, lo que evita la duplicación de datos."

La actividad **Guardar perfiles** le permite enriquecer perfiles de Adobe Experience Platform con datos federados desde almacenes externos.

Esta actividad se utiliza generalmente para mejorar los perfiles de los clientes mediante la introducción de atributos y perspectivas adicionales sin mover físicamente o duplicar los datos en la plataforma.

## Configure la actividad Guardar perfiles {#save-profile-configuration}

Siga estos pasos para configurar la actividad **Guardar perfiles**:

1. Agregue una actividad **Guardar perfiles** a su composición.

   ![](../assets/save-profile.png)

1. Especifique la etiqueta de los perfiles que desea crear.

   >[!IMPORTANT]
   >
   >La etiqueta de audiencia debe ser única dentro de la zona protegida actual. No puede ser la misma etiqueta que cualquier audiencia existente.

1. Seleccione el esquema de Adobe Experience Platform que desee utilizar.

   ![](../assets/save-profile-2.png)

1. Elija el campo de identidad principal que se utilizará para identificar perfiles en la base de datos.

1. Si desea reconciliar atributos de datos adicionales, haga clic en **Agregar atributos**.

   A continuación, especifique el campo **Source** (datos externos) y el campo **Destination** (campo de esquema) para cada atributo que desee asignar.

   ![](../assets/save-profile-3.png)

1. Una vez configurado, haga clic en **Iniciar**.
