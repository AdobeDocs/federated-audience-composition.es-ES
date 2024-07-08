---
audience: end-user
title: Uso del modelador de consultas
description: Aprenda a trabajar con el consulta modelador.
source-git-commit: 5d4bdbbb9c903e839b21d22455d870396ac1df7d
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 9%

---

# Uso del modelador de consultas {#segment-builder}

>[!CONTEXTUALHELP]
>id="dc_orchestration_querymodeler_querymessage"
>title="Modelador de consultas"
>abstract="Definir criterios de filtrado para los destinatarios o cualquier otro esquema, también conocido como dimensión de segmentación, de la base de datos."

El consulta modelador simplifica el proceso de filtrado de la base de datos en función de varios criterios. Además, el modelador de consulta puede administrar consultas muy complejas y largas de manera eficiente, ofreciendo una mayor flexibilidad y precisión. Además, admite filtros predefinidos dentro de las condiciones, lo que le permite refinar sus consultas con facilidad mientras utiliza expresiones y operadores avanzados para estrategias integrales de audiencia direccionamiento y segmentación.

## Acceder al modelador de consulta

El modelador de consultas está disponible en todos los contextos en los que necesite definir reglas para filtrar datos.

| Uso | Ejemplo |
|  ---  |  ---  |
| **Define audiencias**: Especifica la población que quieres destino en tus composiciones y crea sin esfuerzo nuevas audiencias adaptadas a tus necesidades. | ![](assets/access-audience.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |
| **Personalice flujo de trabajo actividades**: aplique reglas dentro de las actividades de composición, como **División** y **Reconciliación**, para alinearse con sus requisitos específicos. [Más información sobre las actividades de composición](../compositions/activities/about-activities.md) | ![](assets/access-composition.png){zoomable="yes"}{width="200" align="center" zoomable="yes"} |

## Interfaz del modelador de consultas {#interface}

El modelador de consulta proporciona un lienzo central donde versión su consulta y un panel derecho que proporciona información sobre su consulta.

![](assets/query-interface.png){zoomable="yes"}

### El lienzo central {#canvas}

El lienzo central del modelador de consulta es donde agrega y combina los diferentes componentes que construyen su consulta. [Aprenda a versión una consulta](build-query.md)

La barra de herramientas ubicada en la esquina superior derecha del lienzo ofrece opciones para manipular fácilmente los componentes del consulta y navegar en el lienzo:

* **Varios modo de selección**: seleccione varios componentes de filtrado para copiarlos y pegarlos en la ubicación que desee.
* **Rotar**: Cambia el lienzo verticalmente.
* **Ajustar a pantalla**: Adapta el nivel de zoom del lienzo a tu pantalla.
* **Zoom hacia afuera** / **Zoom hacia adentro**: Zoom hacia afuera o en el lienzo.
* **Mostrar mapa**: Abre una instantánea del lienzo en la que se muestra la ubicación.

### El panel Propiedades de la regla {#rule-properties}

En el lado derecho, el panel de propiedades ]**de la**[!UICONTROL  regla proporciona información sobre los consulta. Le permite realizar diversas operaciones para verificar el consulta y asegurarse de que se adapta a sus necesidades. [Aprenda a comprobar y validar sus consulta](build-query.md#check-and-validate-your-query)
