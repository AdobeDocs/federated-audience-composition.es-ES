---
audience: end-user
title: Creación de composiciones
description: Aprenda a crear composiciones
exl-id: 7b9acfc0-99b6-4f83-b774-3652c811868c
source-git-commit: 5972479c87a757eb09ce74535e26427f5410f254
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 0%

---

# Organización de actividades de composición {#activities}

Una vez creada una composición, puede empezar a organizar las diferentes tareas que va a realizar. Para ello, se proporciona un lienzo visual, que le permite crear el diagrama de composición de audiencia. Dentro de este diagrama, puede añadir varias actividades y conectarlas en un orden secuencial.

## Añadir actividades {#add}

En esta fase de la configuración, el diagrama se muestra con un icono de inicio, que representa el principio de la composición. Para agregar su primera actividad, haga clic en el botón **+** conectado al icono de inicio.

Aparecerá una lista de actividades que se pueden agregar al diagrama. Las actividades disponibles dependen de su posición dentro del diagrama de composición. Por ejemplo, al agregar la primera actividad, puede iniciar la composición dirigiéndose a una audiencia, dividiendo la ruta de la composición, configurando un planificador para retrasar la ejecución de la composición o estableciendo una actividad **Wait** para retrasar la ejecución de la composición. Por otro lado, después de una actividad **Generar audiencia**, puede refinar el segmento con actividades de segmentación u organizar el proceso de composición con actividades de control de flujo.

Una vez que se ha agregado una actividad al diagrama, aparece un panel derecho que le permite configurar la actividad recién agregada con ajustes específicos. Encontrará información detallada sobre cómo configurar cada actividad en [esta sección](activities/about-activities.md).

![](assets/composition-create-add.png)

Repita este proceso para agregar tantas actividades como desee según las tareas que desee que realice la composición. Tenga en cuenta que también puede insertar una nueva actividad entre dos actividades. Para ello, haga clic en el botón **+** en la transición entre las actividades, seleccione la actividad deseada y configúrela en el panel derecho.

>[!TIP]
>
>Tiene la opción de personalizar el nombre de las transiciones entre cada actividad. Para ello, seleccione la transición y cambie su etiqueta en el panel derecho.

## La barra de herramientas de lienzo {#toolbar}

La barra de herramientas situada en la esquina superior derecha del lienzo proporciona opciones para manipular fácilmente las actividades y navegar en el lienzo.

![](assets/canvas-toolbar.png)

Las acciones disponibles son:

* **[!UICONTROL Selección múltiple]**: seleccione varias actividades para eliminarlas todas a la vez o cópielas y péguelas. Consulte [esta sección](#copy).
* **[!UICONTROL Rotar]**: cambie el lienzo verticalmente.
* **[!UICONTROL Ajustar a pantalla]**: adapta el nivel de zoom del lienzo a la pantalla.
* **[!UICONTROL Alejar]** / **[!UICONTROL Acercar]**: Aleja o en el lienzo.
* **[!UICONTROL Mostrar mapa]**: abre una instantánea del lienzo en el que se muestra que se encuentra.

## Administrar actividades {#manage}

Al agregar actividades, los botones de acción están disponibles en el panel de propiedades, lo que le permite realizar varias operaciones.

![](assets/activity-actions.png)

Puede hacer lo siguiente:

* **[!UICONTROL Eliminar]** la actividad del lienzo.
* **[!UICONTROL Deshabilitar]/[!UICONTROL Habilitar]** la actividad. Cuando se ejecuta la composición, las actividades desactivadas y las siguientes actividades en la misma ruta no se ejecutan y la composición se detiene.
* **[!UICONTROL Pausar]/[!UICONTROL Reanudar]** la actividad. Cuando se ejecuta la composición, esta se pausa en la actividad pausada. No se ejecutan la tarea correspondiente ni todas las que la siguen en la misma ruta.
* **[!UICONTROL Copie]** la actividad para pegarla en otra ubicación de la composición. Para ello, haga clic en el botón **+** de una transición y seleccione **[!UICONTROL Pegar actividad X]**. <!-- cannot copy multiple activities ? cannot paste in another composition?-->
* Configure **[!UICONTROL Opciones de ejecución]** para la actividad seleccionada. Expanda la sección siguiente para obtener más información sobre las opciones disponibles.

  +++Opciones de ejecución disponibles

  La sección **[!UICONTROL Properties]** le permite configurar opciones genéricas con respecto a la ejecución de la actividad:

   * **[!UICONTROL Ejecución]**: defina la acción que se va a llevar a cabo cuando se inicie.
   * **[!UICONTROL Duración máxima de la ejecución]**: especifique una duración como &quot;30 s&quot; o &quot;1h&quot;. Si la actividad no termina después de que haya transcurrido la duración especificada, se activa una alerta. Esto no afecta al funcionamiento de la composición.
   * **[!UICONTROL Zona horaria]**: seleccione la zona horaria de la actividad. La Composición de audiencia federada permite administrar las diferencias horarias entre varios países en la misma instancia. La configuración aplicada se configura cuando se crea la instancia.
   * **[!UICONTROL Afinidad]**: fuerza la ejecución de la actividad de composición en un equipo concreto. Para ello, debe especificar una o varias afinidades para la actividad en cuestión.
   * **[!UICONTROL Comportamiento]**: defina el procedimiento a seguir si se utilizan tareas asincrónicas.

  La sección **[!UICONTROL Administración de errores]** le permite especificar la acción que se debe llevar a cabo si la actividad encuentra un error.

  La sección **[!UICONTROL Secuencia de comandos de inicialización]** le permite inicializar variables o modificar propiedades de actividad. Haga clic en el botón **[!UICONTROL Editar código]** y escriba el fragmento de código que desea ejecutar. Se llama al script cuando se ejecuta la actividad.

  +++

* Acceda a los **registros y tareas** de la actividad.
