---
audience: end-user
title: Enriquezca las audiencias de Adobe Experience Platform con datos externos
description: Aprenda a refinar y enriquecer las audiencias de Adobe Experience Platform con datos de sus bases de datos federadas mediante el destino de composición de audiencias federadas.
badge: label="Disponibilidad limitada" type="Informative"
source-git-commit: 03e1ec555ae64705e8e7ef49610cba27efd5f58b
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 4%

---

# Enriquezca las audiencias de Adobe Experience Platform con datos externos {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Crear un destino"
>abstract="Introduzca la configuración para conectarse a la nueva base de datos federada. Utilice el botón **[!UICONTROL Conectar con destino]** para validar la configuración."

Adobe Experience Platform permite la integración perfecta de audiencias desde Audience Portal a las bases de datos externas mediante el destino de composición de audiencia federada de Adobe. Al hacerlo, puede aprovechar las audiencias existentes en composiciones y enriquecerlas o refinarlas con datos de bases de datos externas para crear nuevas audiencias o actualizar las existentes.

Para ello, debe configurar una nueva conexión en Adobe Experience Platform al destino de composición de audiencia federada de Adobe. Puede utilizar un planificador para enviar una audiencia determinada a frecuencias regulares y seleccionar los atributos específicos que desea incluir, como los ID para la reconciliación de datos. Si ha aplicado políticas de gobernanza y privacidad a su audiencia, se conservarán y se devolverán al portal de audiencia una vez que se haya actualizado la audiencia.

Por ejemplo, si almacena puntuaciones de crédito de clientes en su almacén de datos y tiene una audiencia de Adobe Experience Platform dirigida a clientes interesados en un producto específico en los últimos dos meses, puede refinar esta audiencia según las puntuaciones de crédito usando el destino de Composición de audiencia federada. Este proceso le permite filtrar la audiencia para incluir solo perfiles con puntuaciones de crédito altas sin transferir datos de puntuación de crédito confidenciales desde el almacén de datos.

Los pasos principales para enviar audiencias de Adobe Experience Platform a la Composición de audiencias federada de Adobe son los siguientes:

1. Acceda al catálogo de destinos de Adobe Experience Platform y seleccione el destino de composición de audiencia federada.

   En el panel derecho, seleccione **[!UICONTROL Configurar nuevo destino]**.

   ![](assets/destination-new.png)

1. Proporcione un nombre para la nueva conexión y elija el **[!UICONTROL tipo de conexión]** que desea usar y la **[!UICONTROL base de datos federada]** a la que desea conectarse y haga clic en **[!UICONTROL Siguiente]**.

   ![](assets/destination-configure.png)

   La sección **[!UICONTROL Alertas]** le permite habilitar alertas para recibir notificaciones sobre el estado del flujo de datos a su destino. Para obtener más información sobre las alertas, consulte la guía sobre [suscripción a alertas de destinos mediante la interfaz de usuario](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts).

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
