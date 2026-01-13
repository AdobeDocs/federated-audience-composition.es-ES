---
audience: end-user
title: Información general de Query Modeler
description: Aprenda a utilizar el modelador de consultas para definir reglas para filtrar la base de datos.
exl-id: b77b9d1c-61d5-4d6d-9d82-3c72bc9c932a
source-git-commit: 93f4a16d00c71059672c4c6a51ff36debb6c9cee
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 17%

---

# Información general del modelador de consultas {#query-modeler}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Modelador de consultas"
>abstract="Defina los criterios de filtrado para destinatarios o cualquier otro esquema, también conocido como dimensión de segmentación, de la base de datos."

El modelador de consultas simplifica el proceso de filtrado de la base de datos en función de diversos criterios. Además, el modelador de consultas puede administrar consultas muy complejas y largas de forma eficaz, lo que ofrece una mayor flexibilidad y precisión. Además, admite filtros predefinidos dentro de las condiciones, lo que le permite refinar las consultas con facilidad mientras utiliza expresiones avanzadas y operadores para estrategias completas de segmentación y segmentación de audiencia.

## Acceso al modelador de consultas

El modelador de consultas está disponible en todos los contextos en los que necesite definir reglas para filtrar datos.

| Uso | Ejemplo |
|  ---  |  ---  |
| **Definir audiencias**: especifique la población a la que quiere dirigirse en sus composiciones y cree nuevas audiencias adaptadas a sus necesidades sin esfuerzo. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalizar actividades**: aplique reglas dentro de las actividades de composición, como **División** y **Reconciliación**, para alinearlas con sus requisitos específicos. [Más información sobre las actividades de composición](../compositions/activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Interfaz del modelador de consultas  {#interface}

El modelador de consultas proporciona un lienzo central en el que generar la consulta y un panel derecho que proporciona información sobre la misma.

![](assets/query-interface.png){zoomable="yes"}

### El lienzo central {#canvas}

El lienzo central del modelador de consultas es donde se agregan y combinan los diferentes componentes de la creación de la consulta. [Aprenda a crear una consulta](build-query.md)

La barra de herramientas situada en la esquina superior derecha del lienzo proporciona opciones para manipular fácilmente los componentes de la consulta y desplazarse por el lienzo:

* **[!UICONTROL Modo de selección múltiple]**: seleccione varios componentes de filtrado para copiarlos y pegarlos en la ubicación que elija.
* **[!UICONTROL Rotar]**: cambie el lienzo verticalmente.
* **[!UICONTROL Ajustar a pantalla]**: adapta el nivel de zoom del lienzo a la pantalla.
* **[!UICONTROL Alejar]** / **[!UICONTROL Acercar]**: Aleja o en el lienzo.
* **[!UICONTROL Mostrar mapa]**: abre una instantánea del lienzo en el que se muestra que se encuentra.

### El panel Propiedades de la regla {#rule-properties}

En el lado derecho, el panel **[!UICONTROL Propiedades de regla]** proporciona información sobre la consulta. Permite realizar varias operaciones para comprobar la consulta y asegurarse de que se adapta a sus necesidades. Este panel se muestra al armar una consulta para crear un público. [Aprenda a comprobar y validar su consulta](build-query.md#check-and-validate-your-query)
