---
audience: end-user
title: Enriquecimiento de públicos de Adobe Experience Platform con datos externos
description: Aprenda a refinar y enriquecer las audiencias de Adobe Experience Platform con datos de sus bases de datos federadas mediante el destino de composición de audiencias federadas.
exl-id: 03c2f813-21c9-4570-a3ff-3011f164a55e
TQID: https://experienceleague.adobe.com/g32ycFuhXFq68NmBJjunWZT3m4JpmL108bhMSs-4EYc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ce79e1b9216ca69020155978ac84f29577c5ff8d
workflow-type: tm+mt
source-wordcount: 774
ht-degree: 5%

---

# Enriquecimiento de públicos de Adobe Experience Platform con datos externos {#connect-aep-fac}

>[!CONTEXTUALHELP]
>id="dc_new_destination"
>title="Crear un destino"
>abstract="Introduce la configuración para conectarte a la nueva base de datos federada. Utilice el botón **[!UICONTROL Conectar con destino]** para validar la configuración."

Adobe Experience Platform permite la integración perfecta de audiencias desde Audience Portal con sus bases de datos externas mediante **Adobe Federated Audience Composition destination**. Con esta integración, puede aprovechar las audiencias existentes en las composiciones y enriquecerlas o refinarlas con datos de bases de datos externas para crear nuevas audiencias.

Para ello, debe configurar una nueva conexión en Adobe Experience Platform al destino de composición de audiencia federada de Adobe. Puede utilizar un planificador para enviar una audiencia determinada a frecuencias regulares y seleccionar los atributos específicos que desea incluir, como los ID para la reconciliación de datos. Si ha aplicado políticas de gobernanza y privacidad a su audiencia, se conservarán y se devolverán al portal de audiencia una vez que se haya actualizado la audiencia.

Por ejemplo, supongamos que almacena información de compra en su almacén de datos y tiene una audiencia de Adobe Experience Platform dirigida a los clientes interesados en un producto específico en los últimos dos meses. Con el destino de composición de audiencia federada, puede:

* Refine la audiencia en función de la información de compra. Por ejemplo, puede filtrar la audiencia para dirigirse a los clientes que hayan realizado una compra de más de 150 dólares.
* Enriquezca la audiencia con campos relacionados con las compras, como el nombre del producto y la cantidad comprada.

## Activar audiencia en destino {#activate}

En el catálogo Destinos de Adobe Experience Platform, seleccione el destino Composición de audiencia federada. En el panel derecho, seleccione **[!UICONTROL Configurar nuevo destino]**.

![El botón Configurar nuevo destino está resaltado en el catálogo de destinos.](assets/destinations/new.png)

Aparecerá la página **[!UICONTROL Configurar nuevo destino]**. En esta página, puede configurar los detalles del destino, incluido el nombre, la descripción, el tipo de conexión y la base de datos federada.

![Se muestra la página Configurar nuevo destino, que muestra los detalles que se deben agregar para crear el destino.](assets/destinations/configure.png)

En la sección **[!UICONTROL Alertas]**, puede habilitar las alertas para recibir notificaciones sobre el estado del flujo de datos a su destino. Estas incluyen alertas para retrasos de ejecución del flujo de datos, errores de ejecución, ejecuciones correctas, inicios de ejecución y saltos de activación.

Para obtener más información acerca de las alertas, lea la documentación de Adobe Experience Platform acerca de la suscripción de [a alertas de destinos mediante la interfaz de usuario](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/ui/alerts){target="_blank"}.

![Se muestran las alertas disponibles para el destino.](assets/destinations/alerts.png)

Una vez que hayas terminado de configurar los detalles de tu destino, selecciona **[!UICONTROL Siguiente]**. Aparece el paso **[!UICONTROL Política de gobernanza y acciones de aplicación]**. En esta página, puede definir las políticas de control de datos y asegurarse de que los datos utilizados sean compatibles cuando las audiencias se envíen y estén activas.

Cuando termine de seleccionar las acciones de marketing deseadas para el destino, seleccione **[!UICONTROL Crear]**.

Se crea la nueva conexión con el destino. Ahora puede activar audiencias para enviar al destino. Elija el destino al que desea activar las audiencias, seguido de **[!UICONTROL Siguiente]**.

![El botón de activación está resaltado.](assets/destinations/activate.png)

Se muestra el paso **[!UICONTROL Scheduling]**. Puede seleccionar las audiencias que desee activar en el destino. Para configurar una programación, seleccione ![icono de lápiz](assets/do-not-localize/Smock_Edit_18_N.svg) para editar la programación de exportación.

![Se muestra la página Activar destino.](assets/destinations/schedule.png)

Aparece la ventana emergente **[!UICONTROL Programando]**. En esta ventana emergente, puede definir las opciones de exportación de archivos, la frecuencia y la programación.

![Se muestra la ventana emergente de programación.](assets/destinations/schedule-2.png)

>[!NOTE]
>
>Para activar las audiencias más rápido, seleccione la opción **[!UICONTROL Después de la evaluación del segmento]** para almacenar en déclencheur el trabajo de activación inmediatamente después de que finalice el trabajo diario de segmentación por lotes de Platform.
>
>Para obtener información detallada sobre cómo configurar la programación y los nombres de archivo, lea las siguientes secciones de la documentación de Adobe Experience Platform:
>
>* [Programar exportación de audiencias](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#scheduling){target="_blank"}
>* [Configurar nombres de archivo](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#configure-file-names){target="_blank"}

En el paso **[!UICONTROL Asignación]**, seleccione qué campos de atributo e identidad desea exportar para sus audiencias.

>[!IMPORTANT]
>
>Usted **no puede** utilizar columnas generadas por el sistema al activar en destinos. Si se selecciona una columna generada por el sistema, se producirá un error.

Para obtener más información, lea la [sección de asignación](https://experienceleague.adobe.com/es/docs/experience-platform/destinations/ui/activate/activate-batch-profile-destinations#mapping){target="_blank"} en la documentación de Adobe Experience Platform.

![Se muestra la página de atributos de asignación.](assets/destinations/attributes.png)

Revise la configuración de destino y la configuración de audiencia y, a continuación, seleccione **[!UICONTROL Finalizar]**.

![Se muestra la página de destino de revisión.](assets/destinations/review.png)

Las audiencias seleccionadas ahora están activadas para la nueva conexión. Para agregar más audiencias que enviar con esta conexión, vuelva a la página **[!UICONTROL Activar audiencias]**. Las audiencias no se pueden eliminar una vez activadas.
