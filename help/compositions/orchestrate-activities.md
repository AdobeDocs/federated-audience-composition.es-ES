---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
source-git-commit: 4b5173a2a0549d6535bccd07c94e521ecde8330b
workflow-type: tm+mt
source-wordcount: '1052'
ht-degree: 2%

---


# Organización de actividades de composición {#activities}

Una vez creada una composición, puede empezar a organizar las diferentes tareas que va a realizar. Para ello, se proporciona un lienzo visual, que le permite crear el diagrama de composición. Dentro de este diagrama, puede añadir varias actividades y conectarlas en un orden secuencial.

## Añadir actividades {#add}

En esta fase de la configuración, el diagrama se muestra con un icono de inicio que representa el principio del flujo de trabajo. Para añadir su primera actividad, haga clic en **+** botón conectado al icono de inicio.

Aparecerá una lista de actividades que se pueden agregar al diagrama. Las actividades disponibles dependen de su posición dentro del diagrama de composición. Por ejemplo, al añadir la primera actividad de, puede iniciar la composición dirigiéndose a una audiencia, dividiendo la ruta del flujo de trabajo o estableciendo un **Esperar** para retrasar la ejecución del flujo de trabajo. Por otro lado, después de un **Crear audiencia** actividad, puede refinar el segmento con actividades de segmentación, enviar una entrega a la audiencia con actividades de canal u organizar el proceso de composición con actividades de control de flujo.

Una vez que se ha agregado una actividad al diagrama, aparece un panel derecho que le permite configurar la actividad recién agregada con ajustes específicos. Encontrará información detallada sobre cómo configurar cada actividad en [esta sección](activities/about-activities.md).

Repita este proceso para agregar tantas actividades como desee según las tareas que desee que realice la composición. Tenga en cuenta que también puede insertar una nueva actividad entre dos actividades. Para ello, haga clic en el **+** en la transición entre las actividades, seleccione la actividad deseada y configúrela en el panel derecho.

Para quitar una actividad, selecciónela en el lienzo y haga clic en **Eliminar** en las propiedades de la actividad.

>[!TIP]
>
>Tiene la opción de personalizar el nombre de las transiciones entre cada actividad. Para ello, seleccione la transición y cambie su etiqueta en el panel derecho.

## La barra de herramientas {#toolbar}

La barra de herramientas situada en la esquina superior derecha del lienzo proporciona opciones para manipular fácilmente las actividades y navegar en el lienzo:

* **Modo de selección múltiple**: seleccione varias actividades para eliminarlas todas a la vez o cópielas y péguelas. Consulte [esta sección](#copy).
* **Rotar**: cambie el lienzo verticalmente.
* **Ajustar a pantalla**: adapte el nivel de zoom del lienzo a la pantalla.
* **Alejar** / **Ampliar**: Aleje o en el lienzo.
* **Mostrar mapa**: abre una instantánea del lienzo en el que se muestra que se encuentra.


## Administrar actividades {#manage}

Al agregar actividades, los botones de acción están disponibles en el panel de propiedades, lo que le permite realizar varias operaciones. Puede hacer lo siguiente:

* **Eliminar** la actividad del lienzo.
* **Deshabilitar/habilitar** la actividad. Cuando se ejecuta el flujo de trabajo, las actividades desactivadas y las siguientes actividades en la misma ruta no se ejecutan y el flujo de trabajo se detiene.
* **Copiar** la actividad. Consulte [esta sección](#copy).
* Acceda a los **Registros y tareas**.
* **Pausar/reanudar** la actividad. Cuando se ejecuta el flujo de trabajo, se detiene en la actividad pausada. No se ejecutan la tarea correspondiente ni todas las que la siguen en la misma ruta.

Varios **Segmentación** actividades, como **Combinar** o **Deduplicación**, le permite procesar la población restante e incluirla en una transición saliente adicional. Por ejemplo, si utiliza un **Split** actividad, el complemento está formado por la población que no coincide con ninguno de los subconjuntos definidos anteriormente. Para utilizar esta capacidad, active la variable **Generar complemento** opción.

## Copiar actividades {#copy}

Puede copiar actividades de flujo de trabajo y pegarlas en cualquier flujo de trabajo. El flujo de trabajo de destino puede estar en una pestaña diferente del explorador.

Para copiar actividades, tiene dos opciones:

* copie una actividad con el botón acción.

* copie varias actividades con el botón de la barra de herramientas.

Para pegar las actividades copiadas, haga clic en **+** en una transición y seleccione Pegar actividad X.

## Opciones de ejecución {#execution}

Todas las actividades permiten administrar sus opciones de ejecución. Seleccione una actividad y haga clic en **Opciones de ejecución** botón. Esto permite definir el modo de ejecución y el comportamiento de la actividad en caso de errores.

### Propiedades

El **Ejecución** permite definir la acción que se lleva a cabo cuando se inicia la tarea.

El **Duración máxima de la ejecución** permite especificar una duración como &quot;30 segundos&quot; o &quot;1h&quot;. Si la actividad no termina después de que haya transcurrido la duración especificada, se activa una alerta. Esto no afecta al funcionamiento del flujo de trabajo.

El **Zona horaria** Este campo permite seleccionar la zona horaria de la actividad. Adobe Campaign le permite administrar las diferencias horarias entre varios países en la misma instancia. La configuración aplicada se configura cuando se crea la instancia.

**La afinidad** Este campo permite forzar la ejecución de un flujo de trabajo o una actividad de flujo de trabajo en un equipo concreto. Para ello, debe especificar una o varias afinidades para el flujo de trabajo o actividad en cuestión.

El **Comportamiento** permite definir el procedimiento que se debe seguir si se utilizan tareas asincrónicas.

### Administración de errores

El **En caso de error** Este campo permite especificar la acción que se debe llevar a cabo si la actividad experimenta un error.

### Script de inicialización

El **Script de inicialización** permite inicializar variables o modificar propiedades de actividad. Haga clic en **Editar código** y escriba el fragmento de código que desea ejecutar. Se llama al script cuando se ejecuta la actividad. Consulte la sección relacionada con [variables de evento](../workflows/event-variables.md).

## Ejemplo {#example}

VIP A continuación, se muestra un ejemplo de flujo de trabajo diseñado para enviar un correo electrónico a todos los clientes (que no sean clientes de la red) con un correo electrónico que estén interesados en las máquinas de café.

Para ello, se han añadido las actividades siguientes:

* A **[!UICONTROL Tenedor]** actividad que divide el flujo de trabajo en tres rutas (una para cada conjunto de clientes),
* **[!UICONTROL Crear audiencia]** actividades para dirigirse a los tres conjuntos de clientes:

   * Clientes con un correo electrónico,
   * Clientes que pertenecen a la audiencia preexistente &quot;Interesado en las máquinas de café&quot;,
   * VIP Clientes que pertenecen a la audiencia preexistente de &quot;recompensa o&quot;.

* A **[!UICONTROL Combinar]** actividad que agrupa a clientes con un correo electrónico y a aquellos interesados en las máquinas de café,
* A **[!UICONTROL Combinar]** VIP actividad que excluye a los clientes de la,
* Un **[!UICONTROL Envío de correo electrónico]** actividad que envía un correo electrónico a los clientes resultantes.

Una vez completado el flujo de trabajo, añada. **[!UICONTROL Fin]** actividad al final del diagrama. Esta actividad le permite marcar visualmente el final de un flujo de trabajo y no tiene impacto funcional.

Después de diseñar correctamente el diagrama de flujo de trabajo, puede ejecutar el flujo de trabajo y realizar un seguimiento del progreso de sus distintas tareas. [Obtenga información sobre cómo iniciar un flujo de trabajo y monitorizar su ejecución](start-monitor-workflows.md)
