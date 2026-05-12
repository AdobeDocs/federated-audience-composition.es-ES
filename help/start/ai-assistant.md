---
title: Información general del Asistente de IA
description: Obtenga información sobre cómo utilizar el asistente de IA, incluidos el conocimiento del producto, los datos operativos y la creación de composiciones de público federado.
exl-id: f7493a57-e42d-43f9-b20a-1b9b90477a74
TQID: https://experienceleague.adobe.com/j-KXucjaZa4dNSjg5POqxh7KOSUHG5CnBkBLFA6rPVs
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: fda4d9d7b45833d7e080ae80f42b7ca5ce36b3ad
workflow-type: ht
source-wordcount: 651
ht-degree: 100%

---

# Información general del Asistente de IA {#ai-assistant}

El Asistente de IA es una función de interfaz de usuario concebida para ayudarle a navegar y comprender los conceptos de Adobe. Puede utilizar el Asistente de IA con el fin de conocer mejor los casos de uso de conocimiento del producto en varios productos de Adobe Experience Cloud, incluida la composición de público federado.

>[!CAUTION]
>
>Debe aceptar las directrices del usuario de IA generativa de Adobe Experience Cloud para poder utilizar el Asistente de IA. Obtenga más información sobre el acuerdo en la [Información general del Asistente de IA (heredado)](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home){target="_blank"}.

En la composición de público federado, puede acceder al conocimiento del producto para obtener información sobre conceptos de Adobe relacionados con diversos aspectos del proceso. El Asistente de IA admite cuatro tipos de casos de uso: **descubrimiento abierto** (explore los conceptos de productos según la documentación de Experience League), **aprendizaje específico y solución de problemas** (formule preguntas sobre funciones o funcionalidades específicas), **datos operativos** (formule preguntas sobre sus objetos en la composición de público federado) y **creación de composiciones de público federado**.

## Acceso {#access}

Para acceder al Asistente de IA, seleccione ![el icono de Asistente de IA](/help/start/assets/ai-assistant/icon.png) en la barra superior. El Asistente de IA se muestra en la sección derecha de la pantalla. Puede seleccionar ![Profundizar en el texto alternativo de la imagen](assets/do-not-localize/Smock_FullScreen_18_N.svg "el icono de Expandir") para expandir la ventana del Asistente de IA.

![El icono del Asistente de IA aparece resaltado y muestra cómo acceder al Asistente de IA.](/help/start/assets/ai-assistant/access.png)

## Uso del Asistente de IA {#using}

Cuando haya abierto el Asistente de IA, formule su pregunta en el campo situado en la parte inferior de la pantalla y pulse Entrar. Se mostrará la respuesta a su pregunta. Puede usar los pulgares arriba o abajo para evaluar su respuesta.

![Se muestra una pregunta y una respuesta de muestra en el Asistente para IA.](/help/start/assets/ai-assistant/sample-question-answer.png)

## Preguntas de muestra {#sample-questions}

Las siguientes consultas muestran los tipos de preguntas disponibles que puede formular al Asistente de IA:

| Tipo de consulta | Pregunta de muestra |
| ---------- | --------------- |
| Descubrimiento abierto | <ul><li>¿Qué es una composición de público federado?</li></ul> |
| Aprendizaje específico | <ul><li>¿Cómo puedo configurar una cuenta de base de datos federada de Snowflake?</li><li>¿Cómo puedo crear una composición federada?</li></ul> |
| Datos operativos | <ul><li>¿Cuántas bases de datos federadas tengo en mi zona protegida?</li><li>¿Cuántos esquemas he creado en los últimos 30 días?</li></ul> |
| Creación de una composición de público federado | <ul><li>Cree un público federado de clientes que residen en el Reino Unido.</li></ul> |

Además, puede utilizar el Asistente de IA para crear de forma autónoma una composición de público federado.

## Crear un público {#create-audience}

Puede utilizar el Asistente de IA para crear una composición de público federado con indicaciones en lenguaje natural. Cuando utiliza el Asistente de IA para crear un público, dicho asistente elabora un plan basado en su indicación y lo ejecuta en el explorador mediante la automatización con tecnología de IA.

Por ejemplo, si solicita al Asistente de IA que “cree un público federado de clientes que residen en el Reino Unido utilizando el esquema CUSTOMERS_Table”, el asistente de IA diseñará el plan que llevará a cabo para crear el público, incluyendo pasos como, por ejemplo, navegar hasta la página Composiciones federadas, cómo creará el agente la composición y guardar el público vez que se haya completado.

![Se muestra una pregunta y una respuesta de muestra.](/help/start/assets/ai-assistant/ask-create.png)

Si el plan parece preciso, puede seleccionar **[!UICONTROL Ejecutar]** para permitir que el agente realice los pasos de automatización. El agente, dentro del explorador, seguirá de forma autónoma los pasos para crear la composición solicitada dentro de la interfaz de usuario de la composición de público federado. Si, en cualquier momento, desea detener la automatización, seleccione **[!UICONTROL Detener]**.

![El plan se ha ejecutado y el agente lo está ejecutando de forma autónoma.](/help/start/assets/ai-assistant/execute-plan.png)

Actualmente, la habilidad para crear públicos admite las siguientes funciones adicionales:

- Planificador
   - Puede crear composiciones federadas que se ejecuten según una programación recurrente. Los valores admitidos son **Una vez** y **Cada día**.
- Deduplicación
   - Puede anular la duplicación de los registros de datos federados durante la reconciliación de datos

## Próximos pasos

Para obtener más información sobre el Asistente de IA, incluidos ejemplos de objetivos que puede alcanzar con él y cómo funciona, lea la [información general del Asistente IA](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home){target="_blank"}.

Para obtener una lista completa de las preguntas sobre Datos operativos que puede formular para la composición de público federado, lea la [sección de datos operativos](https://experienceleague.adobe.com/es/docs/experience-platform/ai-assistant/home#operational-insights){target="_blank"}.
