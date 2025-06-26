---
audience: end-user
title: Introducción a las composiciones
description: Obtenga más información acerca de cómo empezar con las composiciones
exl-id: 92142d16-3483-4f6e-afde-9f88d5d7d1c4
source-git-commit: 5c16e22587cbbbe5bc87cfa4f22210aa8108341c
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 16%

---

# Introducción a las composiciones {#compositions}

>[!AVAILABILITY]
>
>Para acceder a las composiciones, necesita uno de los siguientes permisos:
>
>-**Administrar composiciones federadas**
>&#x200B;>-**Ver composiciones federadas**
>
>Para obtener más información sobre los permisos requeridos, lea la [guía de control de acceso](/help/governance-privacy-security/access-control.md).

La Composición de audiencia federada permite crear composiciones, donde puede aprovechar varias actividades en un lienzo visual para crear audiencias. Después de crear la composición, las audiencias resultantes se guardan en Adobe Experience Platform y se pueden aprovechar en destinos de Experience Platform y Adobe Journey Optimizer para clientes de destino.

![Se muestra un flujo de trabajo de composición de muestra dentro de Composición de audiencia federada.](assets/gs-compositions/composition-example.png){zoomable="yes"}{width="70%"}

## Acceso y administración de composiciones {#access}

>[!CONTEXTUALHELP]
>id="dc_composition_list"
>title="Composiciones"
>abstract="En esta pantalla, puede acceder a la lista completa de composiciones, comprobar su estado actual, las fechas de última/siguiente ejecución y crear una nueva composición."

Se puede acceder a las composiciones desde el menú **[!UICONTROL Audiencias]** de Adobe Experience Platform, en la pestaña **[!UICONTROL Composiciones federadas]** de la sección **[!UICONTROL Clientes]**.

Desde esta pantalla, puede crear nuevas composiciones y acceder a las existentes. También puede duplicar o eliminar una composición existente seleccionando el botón ![elipses](/help/assets/icons/more.png) junto a su nombre.

También puede ver información sobre las composiciones, incluido el nombre, el estado, el creador y la fecha de la última modificación.

| Estado | Descripción |
| ------ | ----------- |
| **[!UICONTROL Borrador]** | La composición se ha creado y guardado. |
| **[!UICONTROL En curso]** | La composición se ha ejecutado y se está ejecutando. |
| **[!UICONTROL Detenido]** | La ejecución de la composición ha finalizado y se ha detenido. |
| **[!UICONTROL En pausa]** | La ejecución de la composición se ha pausado. |
| **[!UICONTROL Erróneo]** | La ejecución de la composición ha encontrado un error. Para ver más información sobre el error, abra la composición y acceda a los registros. |

Puede aprender a iniciar o detener una composición en la [guía de inicio y supervisión de la composición](./start-monitor-composition.md).

![Se muestra una lista de las composiciones disponibles.](assets/gs-compositions/compositions-list.png){zoomable="yes"}{width="70%"}{align="center"}

Para refinar la lista y encontrar la composición que está buscando, puede buscar en la lista y filtrar composiciones por sus estados o fechas de último procesamiento.

También puede personalizar la lista añadiendo o quitando columnas. Para ello, seleccione el botón **[!UICONTROL Configurar columnas]** y agregue o quite las columnas de salida que desee.

![Se muestra una lista de las columnas disponibles que puede agregar a la página de exploración de composiciones.](assets/gs-compositions/compositions-columns.png){zoomable="yes"}{width="70%"}{align="center"}

### Aplicar etiquetas de acceso {#access-labels}

Para aplicar etiquetas de acceso a una composición específica, seleccione la composición, seguida de **[!UICONTROL Administrar acceso]**.

![El botón &quot;Administrar acceso&quot; está resaltado en el lienzo de composición.](assets/gs-compositions/select-manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

Aparece la ventana emergente **[!UICONTROL Administrar acceso]**. En esta página, puede aplicar las etiquetas de acceso y control de datos aplicables a su composición.

![Se muestra la ventana emergente Administrar acceso. Muestra una lista de todas las etiquetas disponibles que se pueden aplicar a la composición.](assets/gs-compositions/manage-access.png){zoomable="yes"}{width="70%"}{align="center"}

| Tipo de etiqueta | Descripción |
| ---------- | ----------- |
| Etiquetas de contrato | Las etiquetas de contrato (etiquetas &quot;C&quot;) se utilizan para categorizar los datos que tienen obligaciones contractuales o están relacionados con las políticas de gobernanza de datos de su organización. |
| Etiquetas de identidad | Las etiquetas de identidad (etiquetas &quot;I&quot;) se utilizan para categorizar los datos que pueden identificar o contactar a una persona específica. |
| Etiquetas confidenciales | Las etiquetas confidenciales (etiquetas &quot;S&quot;) se utilizan para categorizar a usted y/o a su organización como confidenciales. |
| Etiquetas de Partner Ecosystem | Las etiquetas de ecosistema de socio se utilizan para categorizar los datos de fuentes externas a su organización. |

Para obtener más información sobre las etiquetas de acceso y control de datos, lea el [glosario de etiquetas de uso de datos](https://experienceleague.adobe.com/es/docs/experience-platform/data-governance/labels/reference).

## Pasos siguientes

Después de leer esta guía, ha aprendido a tener acceso, administrar y crear etiquetas de acceso para sus composiciones. Para obtener más información sobre cómo trabajar con audiencias en su conjunto, lea la [guía de audiencias](../start/audiences.md).
