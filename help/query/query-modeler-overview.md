---
audience: end-user
title: Uso del modelador de consultas
description: Aprenda a trabajar con el modelador de consultas.
source-git-commit: f6730819712ffcbe815517a4406dac7e8fb9779c
workflow-type: tm+mt
source-wordcount: '376'
ht-degree: 8%

---

# Uso del modelador de consultas {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Modelador de consultas"
>abstract="Defina criterios de filtrado para los destinatarios o cualquier otra dimensión de segmentación de la base de datos."

El modelador de consultas simplifica el proceso de filtrado de la base de datos en función de diversos criterios. Además, el modelador de consultas puede administrar consultas muy complejas y largas de forma eficaz, lo que ofrece una mayor flexibilidad y precisión. Además, admite filtros predefinidos dentro de las condiciones, lo que le permite refinar las consultas con facilidad mientras utiliza expresiones avanzadas y operadores para estrategias completas de segmentación y segmentación de audiencia.

## Acceso al modelador de consultas

El modelador de consultas está disponible en todos los contextos en los que necesite definir reglas para filtrar datos.

| Uso | Ejemplo |
|  ---  |  ---  |
| **Definir audiencias**: especifique la población a la que desea dirigirse en sus composiciones y cree nuevas audiencias adaptadas a sus necesidades sin esfuerzo. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalizar actividades de flujo de trabajo**: aplique reglas dentro de las actividades de flujo de trabajo, como **Split** y **Reconciliación**, para cumplir con sus requisitos específicos. [Descubra más información sobre las actividades de flujo de trabajo](../compositions/activities/about-activities.md) | ![](assets/access-workflow.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Filtros predefinidos**: Cree filtros predefinidos que sirvan de accesos directos durante varias operaciones de filtrado, tanto si trabaja con listas de datos como si forma la audiencia para una entrega. | ![](assets/access-predefined-filter.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalización de listas**: Cree reglas personalizadas para filtrar los datos mostrados en listas como destinatarios, envíos, listas, etc. | ![](assets/access-lists.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Interfaz del modelador de consultas {#interface}

El modelador de consultas proporciona un lienzo central en el que generar la consulta y un panel derecho que proporciona información sobre la misma.

![](assets/query-interface.png){zoomable="yes"}

### El lienzo central {#canvas}

El lienzo central del modelador de consultas es donde se agregan y combinan los diferentes componentes de la creación de la consulta. [Obtenga información sobre cómo crear una consulta](build-query.md)

La barra de herramientas situada en la esquina superior derecha del lienzo proporciona opciones para manipular fácilmente los componentes de la consulta y desplazarse por el lienzo:

* **Modo de selección múltiple**: seleccione varios componentes de filtrado para copiarlos y pegarlos en la ubicación que desee.
* **Rotar**: cambie el lienzo verticalmente.
* **Ajustar a pantalla**: adapte el nivel de zoom del lienzo a la pantalla.
* **Alejar** / **Ampliar**: Aleje o en el lienzo.
* **Mostrar mapa**: abre una instantánea del lienzo en el que se muestra que se encuentra.

### El panel Propiedades de la regla {#rule-properties}

En el lado derecho, la **[!UICONTROL Propiedades de regla]** Este panel proporciona información sobre la consulta. Permite realizar varias operaciones para comprobar la consulta y asegurarse de que se adapta a sus necesidades. [Obtenga información sobre cómo comprobar y validar la consulta](build-query.md#check-and-validate-your-query)
