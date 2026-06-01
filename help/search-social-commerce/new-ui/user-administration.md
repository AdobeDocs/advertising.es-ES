---
title: (Nueva IU) Administración de usuarios
description: Obtenga información sobre cómo administrar el acceso de los usuarios.
feature: Search Introduction
exl-id: bfc43692-cfb6-468f-90df-a808a21a0c23
TQID: 'https://experienceleague.adobe.com/b28N5zmqqdZ6Yvg2swGLWv260fWsMUgjK2eW1DDn-uo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 46dede0e36eaaba0893780af13562b3e7501c259
workflow-type: tm+mt
source-wordcount: 1082
ht-degree: 0%

---

# (Nueva IU) Administración de usuarios para Search, Social y Commerce

Algunos usuarios pueden administrar el acceso a la nueva interfaz de usuario de Search, Social y Commerce usando [Adobe Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html), que es la ubicación central para administrar todos los derechos y la administración de usuarios de Adobe. Los usuarios se clasifican como usuarios finales o administradores. El equipo de cuenta de Adobe le notificará si es administrador. Si es administrador, consulte las siguientes secciones para identificar los permisos y flujos de trabajo para administrar usuarios.

## Tipos de administradores

Admin Console proporciona varios tipos de administradores. Se requieren los siguientes tipos y permisos de administrador para Search, Social y Commerce. Puede agregar tipos adicionales si desea delegar tareas de administración de usuarios.

**Administrador del sistema:** superusuario que administra todos los productos de la organización, incluidas todas las instancias de cliente de la organización. (Las instancias de cliente son las mismas que las cuentas de anunciante heredadas, con una o más instancias por ID de organización). Un administrador del sistema puede realizar todas las tareas administrativas en Admin Console para la organización y puede delegar la funcionalidad administrativa a otros usuarios para cualquiera de los productos de la organización.

**Administrador de productos:** administra el acceso a un producto específico de [!DNL Adobe] (como Buscar, Social y Commerce) y las autorizaciones de usuario para ese producto. Los administradores de productos pueden crear perfiles de producto para el producto, crear (pero no eliminar) usuarios y grupos de usuarios para el producto, añadir o eliminar usuarios y grupos de usuarios de perfiles de producto y añadir o eliminar otros administradores de productos del producto.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Perfiles de producto predeterminados

Los perfiles de producto, que son similares a las funciones, otorgan a los usuarios servicios específicos para un producto específico.

La nueva interfaz de usuario para Search, Social y Commerce tiene los siguientes perfiles de producto predeterminados, que proporcionan diferentes subconjuntos de funciones y servicios. No puede editar los permisos de producto para los perfiles de producto predeterminados ni eliminar los perfiles de producto predeterminados. Sin embargo, los administradores de productos, administradores de perfiles de productos y administradores de sistemas pueden crear y administrar perfiles de productos adicionales con diferentes subconjuntos de permisos disponibles, según sea necesario.

* **[!UICONTROL Basic Optimization]:** Para usuarios que necesitan capacidades estándar de planificación y administración de portafolios con acceso a la configuración básica.

* **[!UICONTROL Expert Optimization]:** Para usuarios avanzados que necesitan acceso completo a la configuración del portafolio, incluidos controles avanzados de nivel experto. Incluye todos los permisos de planificación del rendimiento, objetivo, campaña, configuración y administración de informes.

* **[!UICONTROL Read-Only Optimization]:** Para usuarios que necesitan visibilidad en portafolios, simulaciones y campañas sin ninguna capacidad de edición o creación.

* **[!UICONTROL \[Optimization\] Admin]:** otorga acceso completo a todas las funciones disponibles y permite a los usuarios crear nuevas instancias de cliente (las mismas que las cuentas de anunciante heredadas, con una o más instancias por ID de organización). No asigne este derecho a nadie a menos que tenga una justificación comercial adecuada.

### Funcionalidad por perfil de producto

<!-- These don't correspond exactly to the GUI menu -->

Una marca de verificación (✓) indica que el permiso está incluido en el perfil del producto.

**Administración de Portfolio**

| Permiso | Básico | Experto | Solo lectura | Administrador |
|---|---|---|---|---|
| Ver portafolios | ✓ | ✓ | ✓ | ✓ |
| Ver configuración de Portfolio | ✓ | ✓ | ✓ | ✓ |
| Ver detalles de rendimiento de Portfolio | ✓ | ✓ | ✓ | ✓ |
| Ver grupos de Portfolio | ✓ | ✓ | ✓ | ✓ |
| Editar grupos de Portfolio | ✓ | ✓ | | ✓ |
| Editar la configuración básica de Portfolio | ✓ | | | |
| Editar la configuración de Expert Portfolio | | ✓ | | ✓ |

<!--
Noone has permissions as of 6/1; spelling [sic]:
| Edit Advance Portfolio Settings | | | | |
-->

**Administración de planificación de rendimiento**

| Permiso | Básico | Experto | Solo lectura | Administrador |
|---|---|---|---|---|
| Ver simulación | ✓ | ✓ | ✓ | ✓ |
| Crear simulación | ✓ | ✓ | | ✓ |
| Ver recomendaciones de gastos | | ✓ | | ✓ |
| Aplicar recomendaciones de gasto | | ✓ | | ✓ |

**Administración de objetivos**

| Permiso | Básico | Experto | Solo lectura | Administrador |
|---|---|---|---|---|
| Ver objetivo | ✓ | ✓ | ✓ | ✓ |
| Editar objetivo | ✓ | ✓ | | ✓ |
| Ver reglas de valor de conversión | ✓ | ✓ | ✓ | ✓ |
| Editar reglas de valor de conversión | | ✓ | | ✓ |
| Ver conversiones | | ✓ | | ✓ |
| Editar conversiones | | ✓ | | ✓ |
| Ver visibilidad de conversiones | | ✓ | | ✓ |

**Administración de campañas**

| Permiso | Básico | Experto | Solo lectura | Administrador |
|---|---|---|---|---|
| Ver campañas | ✓ | ✓ | ✓ | ✓ |
| Editar campañas | ✓ | ✓ | | ✓ |
| Ver grupos de anuncios | ✓ | ✓ | ✓ | ✓ |
| Editar grupos de publicidad | ✓ | ✓ | | ✓ |
| Vista de anuncios | ✓ | ✓ | ✓ | ✓ |
| Edición de anuncios | | ✓ | | ✓ |
| Vista de palabras clave | ✓ | ✓ | ✓ | ✓ |
| Vista de audiencias | ✓ | ✓ | ✓ | ✓ |
| Vista de destinos automáticos | ✓ | ✓ | ✓ | ✓ |
| Vista de creativos | ✓ | ✓ | ✓ | ✓ |
| Vista de extensiones | ✓ | ✓ | ✓ | ✓ |
| Vista de clasificaciones de etiquetas | ✓ | ✓ | ✓ | ✓ |
| Vista de ubicaciones | ✓ | ✓ | ✓ | ✓ |
| Vista de recomendaciones | ✓ | ✓ | ✓ | ✓ |
| Ver hojas de edición masiva | | ✓ | | ✓ |
| Editar hojas de edición masiva | ✓ | ✓ | ✓ | ✓ |

**Administración de informes**

| Permiso | Básico | Experto | Solo lectura | Administrador |
|---|---|---|---|---|
| Ver registros de historial | ✓ | ✓ | ✓ | ✓ |
| Ver informes programados | ✓ | ✓ | ✓ | ✓ |
| Editar informes programados | | ✓ | | ✓ |

**Administración de instalación**

| Permiso | Básico | Experto | Solo lectura | Administrador |
|---|---|---|---|---|
| Ver cuenta | ✓ | ✓ | ✓ | ✓ |
| Editar cuenta | | ✓ | | ✓ |
| Ver cuentas MCC | ✓ | ✓ | ✓ | ✓ |
| Editar cuentas MCC | | ✓ | | ✓ |

## Tareas para administradores

### Inicie sesión en Adobe Admin Console y ábralo en Search, Social y Commerce

>[!PREREQUISITES]
>
>Debe tener algún tipo de acceso de administrador a Search, Social y Commerce para iniciar sesión en Admin Console.

1. Vaya a https://adminconsole.adobe.com/enterprise/.

1. (Si no ha iniciado sesión en CX Enterprise) Inicie sesión en CX Enterprise:

   1. Escriba su ID de [!DNL Adobe] y haga clic en **[!UICONTROL Continue]**.

   1. Seleccione **[!UICONTROL Personal Account]&quot; o &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Seleccione la organización empresarial de CX aplicable.

      Admin Console abre la ficha [!UICONTROL Overview].

   1. En [!UICONTROL Product & services], haga clic en &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

      La página del producto se abre en la ficha [!UICONTROL Product profiles] para Buscar, Social y Commerce. Las fichas adicionales incluyen [!UICONTROL Users] y [!UICONTROL Product Admins].

### Flujo de trabajo para administradores del sistema

Siga este flujo de trabajo para cada instancia de cliente de Search, Social y Commerce.

1. [Inicie sesión en Adobe Admin Console y ábralo en Search, Social y Commerce](#open-admin-console).

1. (Opcional) [Agregue otro administrador del sistema](https://helpx.adobe.com/es/enterprise/using/admin-roles.html#enterprise) como copia de seguridad.

1. Delegar la administración de productos y usuarios agregando administradores de productos[&#128279;](https://helpx.adobe.com/es/enterprise/using/admin-roles.html#enterprise).

### Flujo de trabajo para administradores de productos

Siga este flujo de trabajo para cada instancia de cliente de Search, Social y Commerce.

1. [Inicie sesión en Adobe Admin Console y ábralo en Search, Social y Commerce](#open-admin-console).

1. Si es necesario, cree usuarios finales [individualmente](https://helpx.adobe.com/es/enterprise/using/manage-users-individually.html) o [de forma masiva](https://helpx.adobe.com/es/enterprise/using/bulk-upload-users.html).

1. (Opcional) Cree [grupos de usuarios](https://helpx.adobe.com/es/enterprise/using/user-groups.html) para la instancia y asigne usuarios a cada grupo de usuarios.

   Si la instancia tiene muchos usuarios, cree grupos de usuarios para asegurarse de que se asignan los perfiles adecuados a los usuarios en función de su nivel de experiencia. (Consulte el paso 4 para asignar grupos de usuarios a perfiles de producto). Puede crear grupos de usuarios en función de la línea de negocio, las necesidades de acceso de los usuarios, la fecha de contratación de los usuarios u otros criterios.

   >[!IMPORTANT]
   >
   >Los nombres de los grupos de usuarios deben comunicar claramente los derechos que se deben asignar al grupo de usuarios. Por ejemplo, si desea crear un grupo de usuarios con derechos de &quot;Solo lectura&quot;, incluya &quot;Solo lectura&quot; en el nombre del grupo de usuarios, como &quot;Acme_Uk_ReadOnly&quot; o &quot;Acme_ReadOnly&quot;.

1. (Opcional) [Cree perfiles de producto personalizados](https://helpx.adobe.com/es/enterprise/using/manage-product-profiles.html) con conjuntos de permisos definidos.

   Los perfiles personalizados se añaden a los cuatro perfiles de producto predeterminados que ya están disponibles.

   Cada perfil de producto de una organización debe tener un nombre único. Si su organización utiliza varias instancias de Search, Social y Commerce (por ejemplo, Acme_US y Acme_JP), no puede duplicar un nombre de perfil de producto en varias instancias. **Práctica recomendada:** Use la convención de nomenclatura `<Name>_<Instance>,` como &quot;Simulations_Only_JP&quot;.

   **Precaución:** Los permisos del producto son muy granulares. Tenga cuidado al configurar perfiles de producto personalizados o puede omitir la funcionalidad que desea incluir.

1. [Asigne cada usuario o grupo de usuarios al perfil de producto correspondiente](https://helpx.adobe.com/es/enterprise/using/manage-product-profiles.html) de forma manual o en lotes.

## Guía de administración del usuario completa y vínculos adicionales

* Para obtener más información acerca de la administración de usuarios mediante Adobe Admin Console, consulte &quot;[Guía de administración de Adobe Enterprise &amp; Teams](https://helpx.adobe.com/es/enterprise/admin-guide.html)&quot;, incluida la [descripción general de Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html).

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
