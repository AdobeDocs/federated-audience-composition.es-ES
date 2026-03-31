---
title: Información general del asistente de IA
description: Aprenda a utilizar el asistente de IA, incluidos los conocimientos del producto, las perspectivas operativas y la creación de composiciones de audiencia federadas.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
source-git-commit: d3a97b5887778f910ca8f09f7cb8fa99360a612c
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 16%

---

# Información general del Asistente de IA {#ai-assistant}

El Asistente de IA es una función de interfaz de usuario concebida para ayudarle a navegar y comprender los conceptos de Adobe. Puede utilizar el asistente de IA para comprender mejor los casos de uso del conocimiento del producto en varios productos de Adobe Experience Cloud, incluida la Composición de audiencia federada.

>[!CAUTION]
>
>Debe aceptar las directrices del usuario de IA generativa de Adobe Experience Cloud para poder utilizar el Asistente de IA. Obtenga más información acerca del acuerdo en la [descripción general del asistente de IA (heredado)](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home){target="_blank"}.

En la composición de público federado, puede acceder al conocimiento del producto para obtener información sobre conceptos de Adobe relacionados con diversos aspectos del proceso. El Asistente de inteligencia artificial admite cuatro tipos de casos de uso: **descubrimiento abierto** (explore los conceptos de productos según la documentación de Experience League), **aprendizaje y solución de problemas orientados** (haga preguntas sobre características o funcionalidades específicas), **perspectivas operativas** (haga preguntas sobre sus objetos en Federated Audience Composition) y **Creación de composiciones de audiencias federadas**.

## Acceso {#access}

Para acceder al asistente de IA, seleccione ![el icono del asistente de IA](/help/start/assets/ai-assistant/icon.png) en la barra superior. El Asistente de IA se muestra en la sección derecha de la pantalla. Puede seleccionar ![Dive image alt text](assets/do-not-localize/Smock_FullScreen_18_N.svg "el icono Expandir") para expandir la ventana del Ayudante de IA.

![El icono del Asistente de IA aparece resaltado y muestra cómo acceder al Asistente de IA.](/help/start/assets/ai-assistant/access.png)

## Uso del asistente de IA {#using}

Una vez que haya abierto el asistente de IA, introduzca su pregunta en el campo de la parte inferior de la pantalla y pulse Intro. Ahora se muestra la respuesta a su pregunta. Puede usar los pulgares hacia arriba o hacia abajo para evaluar su respuesta.

![Se muestra una pregunta y una respuesta de ejemplo en el Asistente para IA.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Preguntas de muestra {#sample-questions}

Las siguientes consultas muestran los tipos de preguntas disponibles que puede hacer al Asistente de IA:

| Tipo de consulta | Pregunta de muestra |
| ---------- | --------------- |
| Abrir detección | <ul><li>¿Qué es una composición de público federado?</li></ul> |
| Aprendizaje dirigido | <ul><li>¿Cómo puedo configurar una cuenta de base de datos federada de Snowflake?</li><li>¿Cómo puedo crear una composición federada?</li></ul> |
| Datos operativos | <ul><li>¿Cuántas bases de datos federadas tengo en mi zona protegida?</li><li>¿Cuántos esquemas he creado en los últimos 30 días?</li></ul> |
| Creación de una composición de audiencia federada | <ul><li>Cree una audiencia federada de clientes que viven en el Reino Unido.</li></ul> |

Además, puede utilizar el Asistente de IA para crear de forma autónoma una composición de audiencia federada.

## Crear un público {#create-audience}

Puede utilizar el Asistente de IA para crear una composición de audiencia federada con indicadores en lenguaje natural. Cuando utiliza el asistente de IA para crear una audiencia, este crea un plan basado en el mensaje y lo ejecuta en el explorador mediante la automatización con tecnología de IA.

Por ejemplo, si solicita al asistente de IA que &quot;cree una audiencia federada de clientes que viven en el Reino Unido utilizando el esquema CUSTOMERS_Table&quot;, el asistente de IA establecerá el plan que llevará a cabo para crear la audiencia, incluidos pasos como navegar a la página Composiciones federadas, cómo creará el agente la composición y guardar la audiencia una vez que se haya completado.

![Se muestra una pregunta y una respuesta de ejemplo.](/help/start/assets/ai-assistant/ask-create.png)

Si el plan parece preciso, puede seleccionar **[!UICONTROL Ejecutar]** para permitir que el agente pase por su automatización. El agente, dentro del explorador, seguirá de forma autónoma los pasos para crear la composición solicitada dentro de la interfaz de usuario de Composición de audiencia federada. Si, en cualquier momento, desea detener la automatización, seleccione **[!UICONTROL Detener]**.

![El plan se ha ejecutado y el agente lo está ejecutando de forma autónoma.](/help/start/assets/ai-assistant/execute-plan.png)

Actualmente, la habilidad de creación de audiencias admite las siguientes funciones adicionales:

- Planificador
   - Puede crear composiciones federadas que se ejecuten en una programación recurrente. Los valores admitidos son **Once** y **Daily**.
- Deduplicación
   - Puede anular la duplicación de los registros de datos federados durante la reconciliación de datos

## Próximos pasos

Para obtener más información sobre el Asistente de IA, incluidos los objetivos de ejemplo que puede lograr con el Asistente de IA y aprender cómo funciona el Asistente de IA, lea la [descripción general del Asistente de IA](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home){target="_blank"}.

Para obtener una lista completa de las preguntas operativas de Insight que puede hacer sobre la Composición de audiencias federada, lea la [sección de información operativa](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
