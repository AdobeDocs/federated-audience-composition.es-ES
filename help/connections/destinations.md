---
audience: end-user
title: Enviar audiencias a Composición de audiencia federada de Adobe
description: Aprenda a enviar audiencias de Adobe Experience Platform a la Composición de audiencias federada
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 553db3ad6d318e7bddcede352178427255d41781
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 5%

---

# Enviar Adobe Experience Platform a la composición de audiencia federada de Adobe {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Crear un destino"
>abstract="Introduzca la configuración para conectarse a la nueva base de datos federada. Utilice el botón **[!UICONTROL Conectar con destino]** para validar la configuración."

Adobe Experience Platform permite enviar audiencias desde Audience Portal a la Composición de audiencias federada de Adobe. Al hacerlo, puede aprovechar las audiencias existentes en composiciones y combinarlas con datos de bases de datos externas para crear nuevas audiencias o actualizar las existentes.

Para ello, debe configurar una nueva conexión en Adobe Experience Platform al destino de composición de audiencia federada de Adobe. Puede utilizar un planificador para enviar una audiencia determinada a frecuencias regulares y elegir qué campos enviar con la audiencia, como ID para conciliar los datos. Si ha aplicado políticas de gobernanza y privacidad a su audiencia, se conservarán y se devolverán al portal de audiencia una vez que se haya actualizado la audiencia.

Los pasos principales para enviar audiencias de Adobe Experience Platform a la Composición de audiencias federada de Adobe son los siguientes:

1. Acceda al catálogo de destinos de Adobe Experience Platform y seleccione el destino de composición de audiencia federada.

   En el panel derecho, seleccione **[!UICONTROL Configurar nuevo destino]**.

   ![](assets/destination-new.png)

1. Proporcione un nombre para la nueva conexión y elija el **[!UICONTROL tipo de conexión]** que desea usar y la **[!UICONTROL base de datos federada]** a la que desea conectarse y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/destination-configure.png)

   La sección **[!UICONTROL Alertas]** le permite habilitar alertas para recibir notificaciones sobre el estado del flujo de datos a su destino. Para obtener más información sobre las alertas, consulte la guía sobre [suscripción a alertas de destinos mediante la interfaz de usuario](../../ui/alerts.md).

1. En el paso **[!UICONTROL Política de gobernanza y acciones de aplicación]**, puede definir las políticas de gobernanza de datos y asegurarse de que los datos utilizados sean compatibles cuando las audiencias se envíen y estén activas.

   Cuando termine de seleccionar las acciones de marketing deseadas para el destino, haga clic en **[!UICONTROL Crear]**.

1. Se crea la nueva conexión con el destino. Ahora puede activar audiencias para enviar al destino. Para ello, selecciónelo en la lista y haga clic en **[!UICONTROL Siguiente]**

   ![](assets/destination-activate.png)

1. Seleccione las audiencias que desee enviar y haga clic en **[!UICONTROL Siguiente]**.

1. Configure el nombre de archivo y una programación de exportación para las audiencias seleccionadas.

   ![](assets/destination-schedule.png)

   >[!NOTE]
   >
   >Encontrará información detallada sobre cómo configurar la programación y los nombres de archivo en la documentación de Adobe Experience Platform:
   >* [Programar exportación de audiencias](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling)
   >* [Configurar nombres de archivo](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names)

1. En el paso **[!UICONTROL Asignación]**, seleccione qué campos de atributo e identidad desea exportar para sus audiencias. Para obtener más información, vea el [paso de asignación](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping) en la documentación de Adobe Experience Platform.

   ![](assets/destination-attributes.png)

1. Revise la configuración de destino y la configuración de audiencia, y luego haga clic en **[!UICONTROL Finalizar]**.

   ![](assets/destination-review.png)

Las audiencias seleccionadas ahora están activadas para la nueva conexión. Para agregar más audiencias que enviar con esta conexión, vuelva a la página **[!UICONTROL Activar audiencias]**. Las audiencias no se pueden eliminar una vez activadas.
