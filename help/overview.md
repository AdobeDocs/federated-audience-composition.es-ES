---
title: Resumen de composición de audiencia federada
description: Obtenga información acerca de la composición de audiencias federada de Adobe y cómo utilizarla en servicios descendentes como Adobe Experience Platform y Adobe Journey Optimizer
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 51%

---

# Resumen de composición de audiencia federada

La composición de audiencias federada permite crear y enriquecer audiencias de sus almacenes de datos de terceros e importarlas a Adobe Experience Platform. Esto ofrece una solución fácil y potente para conectar su almacén de datos empresarial directamente dentro de servicios descendentes como Adobe Real-Time Customer Data Platform o Adobe Journey Optimizer, y realizar consultas en las tablas de su almacén de datos. Como resultado, puede acceder a los datos de los clientes almacenados en los almacenes de datos y en las plataformas de almacenamiento en la nube como Amazon Redshift y Azure Synapse Analytics.

## Competencias {#rn-capabilities}

La composición de público federado amplía el valor de Real-Time CDP y Journey Optimizer gracias al enfoque integral sobre la organización y activación del público:

* **Amplíe el acceso a los conjuntos de datos esenciales basados en almacenes para crear audiencias de alto valor**: puede usar los almacenes de datos existentes como el sistema principal de registro y, al mismo tiempo, aprovechar las mejores aplicaciones de su clase para potenciar las experiencias de los clientes.

* **Compatibilidad completa con casos de uso de participación de potencia**: La composición de audiencias federada, emparejada con Real-Time CDP o Journey Optimizer, admite experiencias personalizadas iniciadas por la marca con audiencias federadas y ofrece experiencias en el momento activadas por eventos en tiempo real, combinadas con atributos de persona para satisfacer los requisitos de casos de uso entre equipos.

* **Minimizar el movimiento y la duplicación de datos**: puede crear audiencias a partir de conjuntos de datos que residen en almacenes de datos empresariales sin copiar los datos subyacentes para administrar perfiles y audiencias de marketing procesables.

* **Utilizar un solo sistema para flujos de trabajo impulsados por experiencias**: puede depurar audiencias introducidas y federadas en Adobe Experience Platform y coordinar las experiencias salientes en todos los canales.

* **Compatibilidad con varias ediciones**: Los clientes de B2C y B2B CDP pueden aprovechar la Composición de audiencias federada para crear audiencias basadas en personas al integrar datos de almacenes de datos empresariales admitidos. Además, pueden enriquecer las audiencias basadas en personas de Experience Platform existentes incorporando atributos relevantes disponibles en el almacén de datos empresarial, mejorando sus perfiles de audiencia para una participación más personalizada y dirigida.

## Casos de uso {#use-cases}

La composición de público federado admite **tres** categorías de casos de uso: creación de públicos, enriquecimiento de públicos y enriquecimiento del perfil del cliente.

* **Creación de audiencias**: puede crear audiencias a partir de un almacén de datos y federarlas en Experience Platform para usarlas en Real-Time CDP o Journey Optimizer mediante una interfaz de usuario de arrastrar y soltar fácil de usar para expertos en marketing. Como resultado, puede realizar consultas en los almacenes de datos sin copiar datos subyacentes confidenciales ni duplicar datos existentes.
   * **Ejemplo:** cree un público de compradores anteriores de alto valor usando datos de transacciones históricas en el almacén, sin copiar esas transacciones en Experience Platform.

* **Enriquecimiento de la audiencia**: puede agregar más detalles a las audiencias existentes en Experience Platform usando conjuntos de datos adicionales de sus almacenes de datos y superponiendo las audiencias con esta información, todo sin copiar los datos subyacentes en Experience Platform. Con el enriquecimiento de públicos, puede ofrecer una personalización mejorada con el público enriquecido.
   * **Ejemplo:** enriquezca el público de Experience Platform compuesto por usuarios que abandonan el carro de compras con el público de la composición de público federado compuesto por compradores anteriores de alto valor para presentar una oferta personalizada.

* **Enriquecimiento del perfil**: puede seleccionar atributos de cliente individuales de su almacén de datos para mejorar los perfiles de Experience Platform. Con los datos federados agregados a estos perfiles, puede potenciar las experiencias en el momento que se activan mediante señales de clientes entrantes.
   * **Ejemplo:** enriquezca un perfil de Experience Platform con información del público federado. Ahora puede dirigirse a los visitantes del sitio que pertenecen al público federado de compradores anteriores de alto valor con una oferta específica que se activa en función de su comportamiento en el sitio.

![diagrama](assets/overview/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

Para obtener más información sobre los casos de uso de la composición de público federado, lea el [documento técnico de la composición de público federado](https://business.adobe.com/resources/sdk/flexibly-access-enterprise-data-with-federated-audience-composition.html).

## Pasos clave {#gs-steps}

La composición de público federado de Adobe le permite crear y actualizar los públicos de Adobe Experience Platform directamente desde la base de datos, sin ningún proceso de ingesta.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

1. **Crear una conexión**: reúna datos de varias fuentes y combínelos en un conjunto de datos unificado. Para obtener más información sobre cómo conectar aplicaciones de Adobe Experience Platform a su almacén de datos empresarial, bases de datos compatibles y configurar su conexión, lea la [descripción general de las conexiones](./connections/home.md).

2. **Modelar los datos**: Diseñe y cree esquemas y modelos de datos que definan la estructura, las relaciones y las restricciones de los datos. Para obtener más información sobre esquemas, lea la [descripción general del esquema](./data-modelling/schemas.md). Para obtener más información sobre los modelos de datos, lea la [descripción general del modelo de datos](./data-modelling/models.md).

3. **Transforme sus datos**: Aplique técnicas de manipulación de datos para modificar el formato, la estructura o los valores de los elementos de datos y hacerlos compatibles o adecuados para aplicaciones o análisis específicos.

4. **Componga su audiencia**: Cree, organice y cree audiencias. Para obtener más información sobre cómo componer audiencias, lea la [descripción general de la composición](./compositions/home.md). También puede actualizar o reutilizar los públicos existentes a través de Audience Portal y Destinations de Adobe Experience Platform. Obtenga más información en [esta página](./connections/destinations.md)

>[!NOTE]
>
>Después de ejecutar la composición, el público resultante se guarda en Adobe Experience Platform como público externo y estará disponible en Adobe Real-Time Customer Data Platform o Adobe Journey Optimizer. Se puede acceder desde el menú **Públicos**. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Gobernanza, privacidad y seguridad {#governance-privacy-security}

### Solicitudes de privacidad {#gov-privacy-requests}

Una vez creada una composición, los públicos resultantes se guardan en Adobe Experience Platform.

A continuación, puede realizar solicitudes de privacidad para acceder a los datos de perfil correspondientes a estos públicos o eliminarlos mediante Adobe Experience Platform **Privacy Service**, que proporciona una [interfaz de usuario](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=es){target="_blank"} y la [API RESTful](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/api/overview){target="_blank"} que le ayuda a administrar las solicitudes de datos de los clientes.

>[!NOTE]
>
>Para obtener más información sobre Privacy Service, consulte la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=es){target="_blank"}.

Puede crear y administrar solicitudes individuales para acceder a datos de los clientes y eliminarlos de la Composición de público federado de Adobe. Los pasos para enviar las **solicitudes de acceso** y **las solicitudes de eliminación** se detallan en la [documentación del perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/profile/privacy){target="_blank"}.

### Pista de auditoría {#gov-audit-trail}

La capacidad pista de auditoría proporciona un registro detallado y cronológico de todas las acciones y eventos que se han realizado en su entorno en tiempo real. Para obtener más información sobre la pista de auditoría, lea la [descripción general de la pista de auditoría](./admin/audit-trail.md).

## Más información {#learn}

<!-- Workflow + Workflow activities-->

Obtenga más información para acceder a la composición de público federado, y sus mecanismos de protección y limitaciones en [esta página](./start/access-prerequisites.md).

Para obtener respuestas a las preguntas más frecuentes, lea las [Preguntas frecuentes sobre la composición de audiencias federadas](./faq.md).

>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Configuración de ejecución"
>abstract="En esta sección puede configurar opciones relacionadas con la ejecución del flujo de trabajo, como el número de días que se conserva el historial de maquetación."

>[!CONTEXTUALHELP]
>id="dc_orchestration_query_enrichment_noneditable"
>title="Actividad no editable"
>abstract="Cuando una actividad de **Consulta** o **Enriquecimiento** se configura con datos adicionales en la consola, los datos de enriquecimiento se tienen en cuenta y pasan a la transición de salida, pero no se pueden editar."

<!-- Create a link -->

>[!CONTEXTUALHELP]
>id="dc_federated_database_create_link"
>title="Crear un vínculo"
>abstract="Defina la configuración del vínculo."


<!-- incremental query IDs -->

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery"
>title="Consulta incremental"
>abstract="La actividad **Consulta incremental** le permite consultar la base de datos utilizando el Modeler de consulta. Cada vez que se ejecuta esta actividad, se excluyen los resultados de las ejecuciones anteriores. Esto permite buscar solo elementos nuevos."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_history"
>title="Historial de consultas incrementales"
>abstract="Historial de consultas incrementales"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalquery_processeddata"
>title="Datos procesados de consulta incremental"
>abstract="Datos procesados de consulta incremental"

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_standard"
>title="Historial de consultas incrementales"
>abstract="La consulta incremental permite ejecutar la misma consulta varias veces al excluir los resultados de ejecuciones anteriores para cada nueva ejecución."

>[!CONTEXTUALHELP]
>id="dc_orchestration_incrementalmode_custom"
>title="Historial de consultas incrementales"
>abstract="La consulta incremental le permite ejecutar la misma consulta varias veces solo teniendo en cuenta los resultados donde el campo de fecha es posterior o igual a la última fecha de ejecución de la actividad de consulta incremental."

>[!CONTEXTUALHELP]
>id="dc_orchestration_build_audience_dimension"
>title="Seleccionar la dimensión de segmentación"
>abstract="La dimensión de segmentación permite definir la población a la que se dirige la operación: destinatarios, beneficiarios de contratos, operadores, suscriptores, etc. De forma predeterminada, en el caso de los correos electrónicos y SMS, el destinatario se selecciona en la tabla integrada Destinatarios. Para las notificaciones push, la dimensión de destino predeterminada son las aplicaciones del suscriptor."

