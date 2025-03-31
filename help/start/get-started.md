---
title: Introducción a la composición de público federado de Experience Platform
description: Descubra qué es la composición de público federado de Adobe y cómo utilizarla en Adobe Experience Platform
exl-id: 43464aea-9c1d-4f1f-859f-82f209f350b7
source-git-commit: 97bda9d08eead79e6172e3b5bb746e7516bf6d85
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 95%

---

# Introducción a la composición de público federado {#gs-fac}

La Composición de público federado está disponible para los entornos [Adobe Real-Time Customer Data Platform](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/home){target="_blank"} ni [Adobe Journey Optimizer](https://experienceleague.adobe.com/es/docs/journey-optimizer/using/ajo-home){target="_blank"}. Le permite generar y enriquecer los públicos de los almacenes de datos de terceros e importarlos a Adobe Experience Platform. La composición de público federado ofrece una solución fácil y potente para conectar su almacén de datos empresariales directamente con Adobe Real-Time Customer Data Platform o Adobe Journey Optimizer y para realizar consultas en las tablas de su almacén de datos.

La composición de público federado de Adobe ayuda a los usuarios de las aplicaciones de Adobe Experience Platform a acceder a sus datos de clientes almacenados en sus almacenes de datos y plataformas de almacenamiento en la nube como Amazon Redshift, Azure Synapse Analytics y más. Los datos de clientes pueden almacenarse en varios almacenes de datos y ahora se puede acceder a ellos instantáneamente, sin necesidad de replicación. Las plataformas admitidas se enumeran en [esta página](../connections/federated-db.md#supported-db).

>[!INFO]
>
>Siga esta [guía paso a paso](https://experienceleague.adobe.com/es/docs/platform-learn/tutorial-comprehensive-technical/datacollection/module13/fac) para aprender a crear públicos mediante la Composición de público federado.

## Competencias {#rn-capabilities}

La composición de público federado amplía el valor de Real-Time CDP y Journey Optimizer gracias al enfoque integral sobre la organización y activación del público:

* Amplía el acceso a los conjuntos de datos críticos basados en almacenes para crear públicos de gran valor: utilice los almacenes de datos existentes como sistema principal de registro y aproveche las mejores aplicaciones para potenciar extraordinarias experiencias de cliente.

* Compatibilidad completa para potenciar los casos de uso de participación: la composición de público federado, junto con Real-Time CDP o Journey Optimizer, admite experiencias personalizadas iniciadas por la marca con públicos federados y ofrece experiencias activadas por eventos en tiempo real, en combinación con atributos de persona para satisfacer los requisitos de casos de uso entre equipos.

* Minimiza el movimiento y la duplicación de datos: cree públicos a partir de conjuntos de datos que residen en un almacén de datos empresariales sin copiar los datos subyacentes para administrar perfiles de marketing y públicos procesables.

* Utilización de un solo sistema para flujos de trabajo basados en experiencias: organice públicos federados e ingeridos en Adobe Experience Platform y coordine las experiencias de salida en todos los canales.

* Los clientes de B2C y B2B CDP ahora pueden aprovechar la Composición de audiencias federada para crear audiencias basadas en personas integrando datos de almacenes de datos empresariales admitidos. Además, pueden enriquecer las audiencias basadas en personas de AEP existentes incorporando atributos relevantes disponibles en el almacén de datos empresarial, mejorando sus perfiles de audiencia para una participación más personalizada y dirigida.

## Casos de uso {#rn-uc}

A través de una interfaz de usuario para expertos en marketing fácil de usar, puede crear reglas de segmentos que consulten su almacén de datos para obtener una lista de usuarios que cumplan los requisitos de un segmento específico necesario para campañas de marketing, acceder a públicos existentes en el almacén para su activación o enriquecer públicos de Adobe Experience Platform con puntos de datos adicionales que existan en el almacén.

En esta versión, hay dos casos de uso disponibles:

1. Creación de públicos: genere nuevos públicos a partir de conjuntos de datos empresariales sin tener que copiar los datos subyacentes y active esos públicos con destinos prediseñados.

1. Enriquecimiento de público: enriquezca los públicos existentes en Adobe Experience Platform utilizando datos de público compuestos que se hayan federado desde el almacén de datos empresariales. Estos datos no se mantendrán en los perfiles de clientes de Adobe Experience Platform.

![diagrama](assets/fac-use-cases.png){zoomable="yes"}{width="75%" align="center"}

## Pasos clave {#gs-steps}

La composición de público federado de Adobe le permite crear y actualizar los públicos de Adobe Experience Platform directamente desde la base de datos, sin ningún proceso de ingesta.

<!--![diagram](assets/steps-diagram.png){zoomable="yes"}{width="85%" align="center"}-->

Pasos clave:

1. **Integración de datos**: reúna datos de varias fuentes y combínelos en un conjunto de datos unificado. Obtenga más información acerca de cómo conectar las aplicaciones de Adobe Experience Platform y el almacén de datos empresariales; las bases de datos admitidas y cómo configurarlas se especifican en [esta sección](../connections/federated-db.md).

1. **Modelado de datos**: diseñe y cree modelos de datos y esquemas que definan la estructura, las relaciones y las restricciones de los datos. Obtenga más información acerca de los esquemas en [esta página](../customer/schemas.md). Obtenga más información acerca de la creación de vínculos para su modelo de datos en [esta página](../data-management/gs-models.md).

1. **Transformación de datos**: aplique técnicas de manipulación de datos para modificar el formato, la estructura o los valores de los elementos de datos y hacerlos compatibles o adecuados para aplicaciones o análisis específicos.

1. **Uso de datos**: cree, organice y genere públicos. Obtenga más información acerca de cómo componer públicos en [esta página](../compositions/gs-compositions.md). También puede actualizar o reutilizar los públicos existentes a través de Audience Portal y Destinations de Adobe Experience Platform. Obtenga más información en [esta página](../connections/destinations.md)

>[!NOTE]
>
>Después de ejecutar la composición, el público resultante se guarda en Adobe Experience Platform como público externo, estará disponible en Adobe Real-Time Customer Data Platform o Adobe Journey Optimizer. Se puede acceder desde el menú **Públicos**. [Más información](https://experienceleague.adobe.com/es/docs/experience-platform/segmentation/ui/audience-portal){target="_blank"}

## Gobernanza, privacidad y seguridad {#governance-privacy-security}

### Solicitudes de privacidad {#gov-privacy-requests}

Una vez creada una composición, los públicos resultantes se guardan en Adobe Experience Platform.

A continuación, puede realizar solicitudes de privacidad para acceder a los datos de perfil correspondientes a estos públicos o eliminarlos mediante Adobe Experience Platform **Privacy Service**, que proporciona una [interfaz de usuario](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=es){target="_blank"} y la [API RESTful](https://experienceleague.adobe.com/es/docs/experience-platform/privacy/api/overview){target="_blank"} para ayudarle a administrar las solicitudes de datos de los clientes.

>[!NOTE]
>
>Para obtener más información sobre Privacy Service, consulte la [documentación de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=es){target="_blank"}.

Puede crear y administrar solicitudes individuales para acceder a datos de los clientes y eliminarlos de la Composición de público federado de Adobe. Los pasos para enviar las **solicitudes de acceso** y **las solicitudes de eliminación** se detallan en la [documentación del perfil del cliente en tiempo real](https://experienceleague.adobe.com/es/docs/experience-platform/profile/privacy){target="_blank"}.

### Pista de auditoría {#gov-audit-trail}

La función de pista de auditoría proporciona un registro detallado y cronológico de todas las acciones y eventos que se han realizado en su entorno en tiempo real. [Más información](../admin/audit-trail.md)

## Más información {#learn}

<!-- Workflow + Workflow activities-->


Obtenga más información para acceder a la composición de público federado, y sus protecciones y limitaciones en [esta página](access-prerequisites.md).

También puede consultar las preguntas frecuentes en [esta página](faq.md).


>[!CONTEXTUALHELP]
>id="dc_workflow_settings_execution"
>title="Configuración de ejecución"
>abstract="En esta sección, puede configurar las opciones relacionadas con la ejecución del flujo de trabajo, como el número de días que se mantiene el historial de la composición."

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


<!-- save profile IDs-->

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile"
>title="Guardar perfil"
>abstract="Guardar perfil"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_aepschemalist"
>title="Guardar lista de esquemas de AEP de perfil"
>abstract="Guardar lista de esquemas de AEP de perfil"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepattribute"
>title="Guardar atributo de esquema de AEP de perfil"
>abstract="Guardar atributo de esquema de AEP de perfil"

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_primaryidentitynamespace"
>title="Seleccionar el campo de identificación principal"
>abstract="Campo de identificación principal que se utilizará para los perfiles."

>[!CONTEXTUALHELP]
>id="ddc_orchestration_saveprofile_selectdataset"
>title="Conjunto de datos de AEP"
>abstract="Seleccione el conjunto de datos de AEP que se utilizará para los perfiles."

>[!CONTEXTUALHELP]
>id="dc_orchestration_saveprofile_selectaepschema"
>title="Guardar perfil Seleccionar esquema de AEP"
>abstract="Seleccione el esquema de AEP que se utilizará para los perfiles."
