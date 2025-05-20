---
audience: end-user
title: Uso de la actividad Guardar perfiles
description: Aprenda a utilizar la actividad Guardar perfiles
exl-id: 1c840838-32d5-4ceb-8430-835a235b7436
source-git-commit: fae57356b8e9f5358a39d31cad4883171a310fb6
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 29%

---

# Guardar perfiles {#save-profile}

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Guardar perfiles"
>abstract="La actividad Guardar perfiles permite enriquecer perfiles de Experience Platform federando datos de data warehouses externos, lo que permite mejorar los perfiles de los clientes con atributos adicionales. "

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Seleccionar esquema de AEP"
>abstract="Elija el esquema de Experience Platform para los perfiles."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Seleccionar el campo de identidad principal"
>abstract="Seleccione la identidad principal que se utilizará para identificar los perfiles segmentados en la base de datos."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Seleccionar esquema de AEP"
>abstract="Elija el esquema de Experience Platform para los perfiles."

La actividad **Guardar perfiles** le permite enriquecer perfiles de Adobe Experience Platform con datos federados desde almacenes externos.

Esta actividad se utiliza generalmente para mejorar los perfiles de los clientes mediante la introducción de atributos y perspectivas adicionales sin mover físicamente o duplicar los datos en la plataforma

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
