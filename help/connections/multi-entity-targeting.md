---
audience: end-user
title: Segmentación De Varias Entidades Con Audiencias De Composición De Audiencias Federadas En Adobe Journey Optimizer
description: Aprenda a segmentar perfiles a partir de audiencias de Composición de audiencias federadas en Adobe Journey Optimizer recorrido.
source-git-commit: 79f05c5a1b025b522a1b88615973d9fe383e3720
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 3%

---


# Segmentación de varias entidades con audiencias de composición de audiencias federadas en Adobe Journey Optimizer

Con la segmentación por entidades múltiples, puede utilizar atributos de audiencia de Composición de audiencia federada como identificadores suplementarios en Adobe Journey Optimizer recorrido. Estos atributos permiten activar audiencias en varias entidades, como cuentas o suscripciones.

## Cree su audiencia en Composición de audiencia federada {#create}

Para empezar con la segmentación por entidades múltiples, primero deberá crear y guardar la audiencia en Composición de audiencia federada.

En la interfaz de usuario de Composición de audiencia, agregue la actividad **Generar audiencia** para crear la audiencia dentro del lienzo de composición federada y agregue la actividad **Guardar audiencia** para configurar las asignaciones de la audiencia, la identidad principal y la caducidad de los datos.

![Se muestra la interfaz de usuario de composición de audiencia federada, que muestra la audiencia.](/help/connections/assets/multi-entity-targeting/build-activity.png)

Una vez que haya finalizado las configuraciones de la audiencia, seleccione **Iniciar** para iniciar la ejecución de la composición. Esta audiencia y su conjunto de datos correspondiente estarán disponibles para su uso en Experience Platform.

Para obtener más información sobre cómo crear una composición en Composición de audiencia federada, lea la [guía Crear una composición](/help/compositions/create-composition.md).

## Activar la audiencia en Adobe Journey Optimizer {#activate}

Una vez finalizada la ejecución de la composición, puede activar la audiencia en Journey Optimizer. En la sección **Administración de Recorrido** de Adobe Journey Optimizer, seleccione **Recorridos** seguido de **Crear recorrido** para abrir la interfaz de usuario de recorrido.

![El botón Crear recorrido de Adobe Journey Optimizer está resaltado.](/help/connections/assets/multi-entity-targeting/select-create-journey.png)

En la interfaz de recorrido, agregue un nodo **Leer audiencia**. Puede configurar este nodo proporcionando una etiqueta y seleccionando la audiencia que ha creado anteriormente.

![El nodo Leer audiencia se muestra en la interfaz de usuario de Journey Optimizer.](/help/connections/assets/multi-entity-targeting/read-journey.png)

Después de elegir la audiencia creada anteriormente, habilita **Usar identificador suplementario**.

![La casilla de verificación Usar identificador suplementario está resaltada.](/help/connections/assets/multi-entity-targeting/enable-use-supplemental-identifier.png)

Ahora puede elegir un identificador suplementario. En la pantalla del selector, seleccione **Modo avanzado** y navegue hasta **Experience Platform**. En esta página, seleccione el nombre de la audiencia que ha creado anteriormente y elija el identificador suplementario que desee utilizar para la audiencia.

![Se muestra el editor de expresiones.](/help/connections/assets/multi-entity-targeting/add-expression.png)

## Configuración de condiciones de recorrido {#configure-journey}

Ahora que ha activado y configurado los ajustes de audiencia, puede seguir configurando el resto de las condiciones de su recorrido. En este caso de uso, deseará agregar un nodo **Optimizer** después del nodo **Leer audiencia**, seguido de un nodo **Action**.

Después de configurar los nodos restantes, seleccione **Publicar** para completar la creación del recorrido.

![El botón de publicación está resaltado.](/help/connections/assets/multi-entity-targeting/select-publish.png)

El recorrido ahora se dirigirá a los perfiles de audiencia en función del **identificador suplementario**, en lugar del identificador principal. Con esta función, ahora puede segmentar varias entidades, como ID de suscripción, ID de cuenta o ID de pedido, y activarlas en el canal que desee.

## Próximos pasos {#next-steps}

Después de leer esta guía, ahora sabe cómo usar identificadores suplementarios de sus audiencias de Composición de audiencias federadas en Journey Optimizer recorrido. Para obtener más información sobre el uso de recorridos suplementarios, lea [usar identificadores suplementarios en la guía de recorridos](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/supplemental-identifier).

