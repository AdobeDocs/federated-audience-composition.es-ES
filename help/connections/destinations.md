---
audience: end-user
title: Enriquecimiento de públicos de Adobe Experience Platform con datos externos
description: Aprenda a refinar y enriquecer las audiencias de Adobe Experience Platform con datos de sus bases de datos federadas mediante el destino de composición de audiencias federadas.
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
source-git-commit: 9b951f74443ac149e837c3f52ca265acabd407b9
workflow-type: tm+mt
source-wordcount: '610'
ht-degree: 8%

---

# Enriquecimiento de públicos de Adobe Experience Platform con datos externos {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Crear un destino"
>abstract="Introduce la configuración para conectarte a la nueva base de datos federada. Utilice el botón **[!UICONTROL Conectar con destino]** para validar la configuración."

Adobe Experience Platform permite la integración perfecta de audiencias desde Audience Portal con sus bases de datos externas mediante **Adobe Federated Audience Composition destination**. Con esta integración, puede aprovechar las audiencias existentes en las composiciones y enriquecerlas o refinarlas con datos de bases de datos externas para crear nuevas audiencias.

Para ello, debe configurar una nueva conexión en Adobe Experience Platform al destino de composición de audiencia federada de Adobe. Puede utilizar un planificador para enviar una audiencia determinada a frecuencias regulares y seleccionar los atributos específicos que desea incluir, como los ID para la reconciliación de datos. Si ha aplicado políticas de gobernanza y privacidad a su audiencia, se conservarán y se devolverán al portal de audiencia una vez que se haya actualizado la audiencia.

Por ejemplo, supongamos que almacena información de compra en su almacén de datos y tiene una audiencia de Adobe Experience Platform dirigida a los clientes interesados en un producto específico en los últimos dos meses. Con el destino de composición de audiencia federada, puede:

* Refine la audiencia en función de la información de compra. Por ejemplo, puede filtrar la audiencia para dirigirse a los clientes que hayan realizado una compra de más de 150 $.
* Enriquezca la audiencia con campos relacionados con las compras, como el nombre del producto y la cantidad comprada.

Los pasos principales para enviar audiencias de Adobe Experience Platform a la Composición de audiencias federada de Adobe son los siguientes:

1. Acceda al catálogo de destinos de Adobe Experience Platform y seleccione el destino de composición de audiencia federada.

   En el panel derecho, seleccione **[!UICONTROL Configurar nuevo destino]**.

   ![](assets/destination-new.png)

1. Escriba un nombre para la nueva conexión y seleccione **[!UICONTROL Tipo de conexión]** de las siguientes conexiones disponibles:

   * Amazon Redshift
   * Azure Synapse Analytics
   * Google BigQuery
   * Snowflake
   * Vertica Analytics
   * Databricks
   * Microsoft Fabric

1. Seleccione la **[!UICONTROL base de datos federada]** a la que desee conectarse, seguida de **[!UICONTROL Siguiente]**.

   ![](assets/destination-configure.png)

1. En la sección **[!UICONTROL Alertas]**, puede habilitar las alertas para recibir notificaciones sobre el estado del flujo de datos a su destino.

   Para obtener más información sobre las alertas, consulte la documentación de Adobe Experience Platform sobre la suscripción de [a alertas de destinos mediante la interfaz de usuario](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/alerts){target="_blank"}

1. En el paso **[!UICONTROL Política de gobernanza y acciones de aplicación]**, puede definir las políticas de gobernanza de datos y asegurarse de que los datos utilizados sean compatibles cuando las audiencias se envíen y estén activas.

   Cuando termine de seleccionar las acciones de marketing deseadas para el destino, seleccione **[!UICONTROL Crear]**.

1. Se crea la nueva conexión con el destino. Ahora puede activar audiencias para enviar al destino. Para ello, selecciónelo en la lista, seguido de **[!UICONTROL Siguiente]**

   ![](assets/destination-activate.png)

1. Seleccione las audiencias que desee enviar.

1. Seleccione el icono ![](assets/do-not-localize/Smock_Edit_18_N.svg) para editar la programación de exportación.

   ![](assets/destination-schedule.png)

1. Defina las opciones del archivo de exportación. Para activar las audiencias más rápido, seleccione la opción **[!UICONTROL Después de la evaluación del segmento]** para almacenar en déclencheur el trabajo de activación inmediatamente después de que finalice el trabajo diario de segmentación por lotes de Platform.

   ![](assets/destination-schedule-2.png)

   >[!NOTE]
   >
   >Encontrará información detallada sobre cómo configurar la programación y los nombres de archivo en las siguientes secciones de la documentación de Adobe Experience Platform:
   >
   >* [Programar exportación de audiencias](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
   >* [Configurar nombres de archivo](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

1. En el paso **[!UICONTROL Asignación]**, seleccione qué campos de atributo e identidad desea exportar para sus audiencias. Para obtener más información, vea el [paso de asignación](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"} en la documentación de Adobe Experience Platform.

   ![](assets/destination-attributes.png)

1. Revise la configuración de destino y la configuración de audiencia y, a continuación, seleccione **[!UICONTROL Finalizar]**.

   ![](assets/destination-review.png)

Las audiencias seleccionadas ahora están activadas para la nueva conexión. Para agregar más audiencias que enviar con esta conexión, vuelva a la página **[!UICONTROL Activar audiencias]**. Las audiencias no se pueden eliminar una vez activadas.
