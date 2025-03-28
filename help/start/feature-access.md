---
title: Acceso a la Composición de público federado
description: Obtenga información acerca de los permisos necesarios para la Composición de público federado
exl-id: 84138456-218b-4beb-ae7b-146213b03cc2
source-git-commit: 0f4bba9c749a6548da07d78136e914cc53314684
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 93%

---

# Acceso a la Composición de público federado {#feature-access}

## Administración del acceso a zonas protegidas {#access-sandboxes}

Al adquirir la Composición de audiencia federada de Adobe Experience Platform, se crea un perfil de producto para cada zona protegida activa en ese momento. Este perfil de producto se crea en Admin Console, en la tarjeta de producto **Adobe Experience Platform** y sigue la convención de nomenclatura siguiente: `ACP_FAC - <<SandboxName>> - admin.` para acceder a la Composición de público federado para una zona protegida específica, los usuarios deben agregarse al perfil de producto creado para esa zona protegida.

Por ejemplo, si se activa una nueva zona protegida denominada «fac-test», se crea un perfil «ACP_FAC - fac-test - admin» de producto correspondiente. Para acceder a la composición de público federado con esta zona protegida, los usuarios deben añadirse a este perfil de producto.

## Administración del acceso a la Composición de público federado

Para obtener acceso a la **Composición de público federado**, primero debe asegurarse de que el permiso **Administrar datos federados** se haya asignado a las funciones correspondientes. Estas funciones deben asignarse a los usuarios que necesiten acceder a la **Composición de público federado**.

Tenga en cuenta que solo los administradores tienen la capacidad de asignar permisos.

1. Vaya al menú **[!UICONTROL Permisos]**.

1. En el menú **[!UICONTROL Funciones]**, seleccione la **[!UICONTROL Función]** que desee actualizar.

   ![](assets/access_fda_1.png)

1. Haga clic en **[!UICONTROL Editar]** para modificar los permisos de la función.

   ![](assets/access_fda_2.png)

1. Añada el recurso **Datos federados** y, a continuación, seleccione **[!UICONTROL Administrar datos federados]** en el menú desplegable.

   ![](assets/access_fda_3.png)

1. Cuando haya realizado los cambios necesarios, haga clic en **[!UICONTROL Guardar]**.

Los permisos de los usuarios que ya se hayan asignado a esta función se actualizarán automáticamente y tendrán acceso a la Composición de público federado.

Para asignar esta función a nuevos usuarios:

1. Vaya a la pestaña **[!UICONTROL Usuarios]** en el panel Función y haga clic en **[!UICONTROL Añadir usuarios]**.

   ![](assets/access_fda_4.png)

1. Introduzca el nombre o la dirección de correo electrónico del usuario o selecciónelo en la lista disponible. Cuando haya terminado, haga clic en **[!UICONTROL Guardar]**.

El usuario recibirá un correo electrónico con instrucciones para acceder a su instancia. Si el usuario no se ha creado previamente, consulte [esta documentación](https://experienceleague.adobe.com/es/docs/experience-platform/access-control/abac/permissions-ui/users).
