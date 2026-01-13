---
title: Control de acceso en la composición de audiencia federada
description: Obtenga información sobre cómo administrar el acceso a datos para usuarios en la Composición de audiencias federada.
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 65a69bf857ec1a0701534693600a8c6340179838
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 80%

---

# Control de acceso en la composición de audiencia federada

Puede utilizar el control de acceso para proporcionar acceso basado en funciones a los entornos limitados y a la Composición de audiencia federada.

## Administración del acceso a zonas protegidas {#access-sandboxes}

Al comprar la Composición de público federado de Adobe Experience Platform, se crea un perfil de producto para cada zona protegida activa en ese momento. Este perfil de producto se crea en Admin Console, en la tarjeta de producto **Adobe Experience Platform** y sigue la convención de nomenclatura siguiente: `ACP_FAC - <<SandboxName>> - admin.` para acceder a la Composición de público federado para una zona protegida específica, los usuarios deben agregarse al perfil de producto creado para esa zona protegida.

Por ejemplo, si se activa una nueva zona protegida denominada «fac-test», se crea un perfil «ACP_FAC - fac-test - admin» de producto correspondiente. Para acceder a la composición de público federado con esta zona protegida, los usuarios deben añadirse a este perfil de producto.

## Administración del acceso a la Composición de público federado

Puede administrar el acceso asignando los permisos necesarios para acceder a diferentes aspectos de la composición de audiencias federada. Estos permisos se asignan mediante funciones a usuarios que necesitan acceso a **Federated Audience Composition**.

>[!NOTE]
>
>Solo los administradores pueden asignar permisos a otros usuarios.

1. Vaya al menú **[!UICONTROL Permisos]**.
1. En el menú **[!UICONTROL Funciones]**, seleccione la **[!UICONTROL Función]** que desee actualizar.

   ![](assets/access_fda_1.png)

1. Seleccione **[!UICONTROL Editar]** para modificar los permisos de su función.

   ![](assets/access_fda_2.png)

1. Añada los permisos necesarios para el usuario. Puede añadir los siguientes permisos para acceder a la composición de público federado:

   | Permiso | Descripción |
   | ---------- | ----------- |
   | Administrar datos federados | Utilice este permiso para administrar todos los aspectos de la composición de público federado. Este permiso incluye Administrar base de datos federada, Administrar esquema federado, Administrar modelo de datos federado y Administrar composiciones federadas. |
   | Administrar base de datos federada | Utilice este permiso para añadir, ver, actualizar y eliminar sus conexiones a bases de datos federadas. |
   | Ver base de datos federada | Utilice este permiso para ver sus conexiones a bases de datos federadas. |
   | Administrar esquema federado | Utilice este permiso para crear, ver, actualizar, eliminar y actualizar esquemas. |
   | Ver datos de esquema federado | Utilice este permiso para ver la pestaña de datos dentro de la sección del esquema. |
   | Ver esquema federado | Utilice este permiso para ver las tablas del esquema. |
   | Administrar modelo de datos federado | Utilice este permiso para crear, ver, actualizar y eliminar modelos de datos. |
   | Ver modelo de datos federado | Utilice este permiso para ver los modelos de datos. |
   | Ver seguimiento de auditoría de federación | Utilice este permiso para ver el seguimiento de auditoría de la composición de público federado. |
   | Administrar composiciones federadas | Use este permiso para crear, ver, actualizar y eliminar composiciones federadas. |
   | Ver composiciones federadas | Utilice este permiso para ver composiciones federadas. |

   ![](assets/permissions.png)

1. Cuando haya realizado los cambios necesarios, haga clic en **[!UICONTROL Guardar]**.

Los permisos de los usuarios que ya se hayan asignado a esta función se actualizarán automáticamente y tendrán acceso a la Composición de público federado.

Para asignar esta función a nuevos usuarios:

1. Vaya a la pestaña **[!UICONTROL Usuarios]** en el panel de control Función y seleccione **[!UICONTROL Añadir usuarios]**.

   ![](assets/access_fda_4.png)

1. Introduzca el nombre o la dirección de correo electrónico del usuario o selecciónelo en la lista disponible. Cuando haya terminado, seleccione **[!UICONTROL Guardar]**.

De forma alternativa, puede asignar una de las funciones preexistentes a los usuarios, según los permisos que necesiten. Para obtener más información sobre cómo asignar funciones preexistentes a un usuario, lea la [guía sobre la administración de usuarios para un perfil de producto](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/ui/users).

| Nombre de la función | Permisos |
| --------- | ----------- |
| Administradores de datos de FAC | <ul><li>Administrar composiciones federadas</li><li>Ver bases de datos federadas</li><li>Ver esquemas federados</li><li>Ver datos de esquema federado</li><li>Ver modelos de datos federados</li></ul> |
| Administradores de composición de FAC | <ul><li>Administrar composiciones federadas</li></ul> |
| Administradores de FAC | <ul><li>Administrar datos federados</li></ul> |

El usuario recibirá un correo electrónico con instrucciones para acceder a su instancia. Si el usuario no estaba ya creado, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).

## Administración del acceso a composiciones específicas

Puede administrar el acceso a una composición específica aplicando etiquetas de acceso.

Para obtener más información sobre cómo aplicar etiquetas de acceso a una composición, lea la [sección](/help/compositions/home.md#access-labels) de la guía de composiciones sobre aplicar etiquetas de acceso.
