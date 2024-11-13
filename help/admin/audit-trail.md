---
audience: end-user
title: Pista de auditoría
description: Conozca cómo se registran las acciones y los eventos y cómo se puede acceder a ellos en la pista de auditoría
exl-id: 97142f54-53ce-4c2a-9d89-fdcb2a47b159
source-git-commit: 65052ffcd8c70817aa428bea7f8b6baa0a49a1b0
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 11%

---

# Pista de auditoría {#audit-trail}

>[!CONTEXTUALHELP]
>id="dc_audit_trail"
>title="Seguimiento de auditoría"
>abstract="La capacidad de seguimiento de auditoría proporciona un registro detallado y cronológico de todas las acciones y eventos que se han realizado en tiempo real en su entorno de composición de público federado de Adobe Experience Platform."

La capacidad Audit trail proporciona un registro detallado y cronológico de todas las acciones y eventos que se han realizado en su entorno en tiempo real

La función **[!UICONTROL Pista de auditoría]** registra constantemente en tiempo real un registro detallado de las acciones y eventos que tienen lugar en la instancia de Adobe Federated Composition. Ofrece un método cómodo para acceder a un registro cronológico de datos, y abordar consultas como: el estado de los flujos de trabajo, las personas más recientes para modificarlos o las actividades realizadas por los usuarios dentro de la instancia.

+++ Más información sobre las Entidades disponibles de pista de auditoría

* **Seguimiento de auditoría de esquemas de Source** le permite supervisar las actividades y las modificaciones recientes realizadas en los esquemas en la instancia de Composición de audiencias federada de Adobe.

  Para obtener información detallada sobre los esquemas, consulte esta [página](../customer/schemas.md).

* **Registro de auditoría de flujo de trabajo** le permite realizar un seguimiento de las actividades y los cambios recientes realizados en los flujos de trabajo, incluidos sus estados actuales, como:

   * Start
   * Pause
   * Stop
   * Restart
   * Limpieza igual al historial de purga de acciones
   * Simular, que es igual a la acción Iniciar en modo de simulación
   * Activación igual a la acción Ejecutar tareas pendientes ahora
   * Interrupción incondicional

  Para obtener más información sobre los flujos de trabajo, consulte esta [página](../compositions/gs-compositions.md).

* **Cuenta externa** le permite comprobar las modificaciones realizadas en las cuentas externas en la instancia de composición de audiencias de Adobe.

  Para obtener más información sobre la cuenta externa, consulte esta [página](../connections/federated-db.md).

+++

## Acceso a Pista de auditoría {#accessing-audit-trail}

Para acceder a la **[!UICONTROL pista de auditoría]** de su instancia:

1. En el menú **[!UICONTROL Datos federados]**, seleccione **[!UICONTROL Pista de auditoría]**.

1. La ventana **[!UICONTROL Pista de auditoría]** se abre con la lista de sus entidades. Composición de audiencia federada audita las acciones de creación, edición y eliminación para flujos de trabajo, opciones, envíos y esquemas.

   ![](assets/audit_trail.png)

1. La ventana **[!UICONTROL Entidad de auditoría]** le proporciona información más detallada sobre la entidad elegida, como:

   * **[!UICONTROL Tipo]** : flujo de trabajo, opciones, envíos o esquemas.
   * **[!UICONTROL Entidad]** : Nombre interno de sus actividades.
   * **[!UICONTROL Modificado por]** : Nombre de usuario de la última persona que modificó esta entidad por última vez.
   * **[!UICONTROL Acción]** : última acción realizada en esta entidad, ya sea Creada, Modificada o Eliminada.
   * **[!UICONTROL Fecha de modificación]** : Fecha de la última acción realizada en esta entidad.
