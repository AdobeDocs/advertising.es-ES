---
title: Administración de usuarios
description: Aprenda a .
feature: Search Introduction
source-git-commit: ab6acc0ac777edb625b91a29464ca00a4407dcf1
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# (Nueva IU) Administración de usuarios para Search, Social y Commerce

Algunos usuarios pueden administrar el acceso a la nueva interfaz de usuario de Search, Social y Commerce mediante Adobe Admin Console, que es la ubicación central para administrar todas las autorizaciones y la administración de usuarios de Adobe. Los usuarios se clasifican como usuarios finales o administradores. El equipo de cuenta de Adobe le avisará si es administrador. Si es administrador, consulte las siguientes secciones para identificar los permisos y flujos de trabajo para administrar usuarios.<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## Tipos relevantes de administradores

Admin Console proporciona varios tipos de administradores, pero solo los siguientes tipos y permisos de administradores son relevantes para Search, Social y Commerce.

**Administrador del sistema:** Superusuario de la organización. Un administrador del sistema puede realizar todas las tareas administrativas en Admin Console para la organización y puede delegar la funcionalidad administrativa a otros usuarios (administradores de productos).&lt;!—, administradores de perfil de producto y administradores de grupos de usuarios.  — Creo que es SOLO ADMINISTRADORES DE PRODUCTOS PARA NOSOTROS?  Verificar. —>

**Administrador de productos:** administra el acceso a un producto específico de [!DNL Adobe] (como Search, Social y Commerce) y las autorizaciones de sus usuarios para ese producto. Los administradores de productos pueden crear perfiles de producto para el producto, crear (pero no eliminar) usuarios y grupos de usuarios, añadir o eliminar usuarios y grupos de usuarios de perfiles de producto y añadir o eliminar otros administradores de productos del producto.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Perfiles de producto predeterminados

Los perfiles de producto, que son similares a las funciones, otorgan a los usuarios servicios específicos para un producto específico.

La nueva interfaz de usuario para Search, Social y Commerce tiene los siguientes perfiles de producto predeterminados, que proporcionan diferentes subconjuntos de funciones y servicios. No puede editar ni eliminar los perfiles de producto predeterminados. Sin embargo, los administradores del sistema pueden crear y administrar perfiles de producto adicionales con diferentes subconjuntos de permisos, según sea necesario.

* **Optimización básica:** Este perfil proporciona la siguiente funcionalidad:

   * Objetivos: Acceso completo

   * Simulations: Acceso completo

   * Grupos de Portfolio: acceso completo

   * Portafolios: crea o edita el acceso a la configuración del portafolio para Objetivos, Campañas y Administración de gastos; acceso de solo lectura al resto de la configuración del portafolio.

   * Campañas: acceso de solo lectura a la configuración de la campaña (no hay funciones de creación, edición o eliminación disponibles); acceso completo a las asignaciones de restricciones y portafolios<!-- Is that the correct wording? -->

   * Grupos de anuncios: acceso de solo lectura a la configuración del grupo de anuncios (no hay funciones de creación, edición o eliminación disponibles); acceso completo a las asignaciones de restricciones y portafolios<!-- Is that the correct wording? -->

  Este nivel de acceso es el preferido de los usuarios que aún aprenden a utilizar Search, Social y Commerce.

* **Optimización de expertos:** Este perfil proporciona la siguiente funcionalidad:

   * Objetivos: Acceso completo

   * Simulations: Acceso completo

   * Grupos de Portfolio: acceso completo

   * Portafolios: acceso completo

   * Campañas: acceso de solo lectura a la lista de campañas (aún no hay funciones de creación, edición o eliminación de campañas disponibles); acceso completo a las asignaciones de restricciones y portafolios<!-- Is that the correct wording? -->

   * Grupos de anuncios: acceso de solo lectura a la lista de grupos de anuncios (aún no hay funciones de creación, edición o eliminación de campañas disponibles); acceso completo a las asignaciones de restricciones y portafolios<!-- Is that the correct wording? -->

  Este nivel de acceso es recomendable para usuarios expertos de Search, Social y Commerce.

* **Solo lectura:** Este perfil proporciona la siguiente funcionalidad:

   * Objetivos: acceso de solo lectura

   * Simulations: Acceso de solo lectura

   * Grupos de Portfolio: acceso de solo lectura

   * Portafolios: acceso de solo lectura

   * Campaigns: Acceso de solo lectura

   * Grupos de anuncios: acceso de solo lectura

* **Administrador:** Este perfil concede acceso completo a todas las funcionalidades disponibles y permite a los usuarios crear nuevas instancias de cliente. No asigne este derecho a nadie a menos que tenga una justificación comercial adecuada.

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## Tareas para administradores

### Inicie sesión en Adobe Admin Console y ábralo en Search, Social y Commerce

>[!PREREQUISITES]
>
>Debe tener acceso de administrador&lt;!— ¿de qué tipo? Administrador de productos, administrador del sistema, pero seguro que también soy administrador de perfiles de producto o administrador de grupos de usuarios (podría ser un grupo interno — comprobar) —> para Buscar, Social y Commerce.

1. Vaya a https://adminconsole.adobe.com/enterprise/.

1. (Si no ha iniciado sesión en Experience Cloud) Inicie sesión en Experience Cloud:

   1. Escriba su ID de [!DNL Adobe] y haga clic en **[!UICONTROL Continue]**.

   1. Seleccione **[!UICONTROL Personal Account]&quot; o **[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Seleccione la organización de Experience Cloud aplicable.

   1. En Productos y servicios, haga clic en &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]&quot;.

   La página del producto se abre de forma predeterminada en la ficha [!UICONTROL Product profiles] para Buscar, Social y Commerce. Las fichas adicionales incluyen [!UICONTROL Users] y [!UICONTROL Product Admins].

### Flujo de trabajo para administradores del sistema

1. [Inicie sesión en Adobe Admin Console y ábralo en Search, Social y Commerce](#open-admin-console).

1. Delegar la administración de productos y usuarios agregando administradores de productos[.](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise)

<!-- what else? -->

### Flujo de trabajo para administradores de productos

1. [Inicie sesión en Adobe Admin Console y ábralo en Search, Social y Commerce](#open-admin-console).

1. Si es necesario, cree usuarios finales [individualmente](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) o [de forma masiva](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. (Opcional) Cree [grupos de usuarios](https://helpx.adobe.com/enterprise/using/user-groups.html) para cada instancia de producto y asigne usuarios a cada grupo de usuarios.

   Si la instancia tiene muchos usuarios, cree grupos de usuarios para asegurarse de que se asignan los perfiles adecuados a los usuarios en función de su nivel de experiencia. (Consulte el paso 4 para asignar grupos de usuarios a perfiles de producto). Puede crear grupos de usuarios en función de la línea de negocio, las necesidades de acceso de los usuarios, la fecha de contratación de los usuarios u otros criterios.

   >[!IMPORTANT]
   >
   >Los nombres de los grupos de usuarios deben comunicar claramente los derechos que se deben asignar al grupo de usuarios. Por ejemplo, si desea crear un grupo de usuarios con derechos de &quot;Solo lectura&quot;, incluya &quot;Solo lectura&quot; en el nombre del grupo de usuarios, como &quot;Acme_Uk_ReadOnly&quot; o &quot;Acme_ReadOnly&quot;.

1. (Opcional) [Cree perfiles de producto personalizados](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) con conjuntos de permisos definidos.

   Los perfiles personalizados se añaden a los cuatro perfiles de producto predeterminados que ya están disponibles.

   Cada perfil de producto de una organización debe tener un nombre único. Si su organización utiliza varias instancias de Search, Social y Commerce (por ejemplo, Acme_US y Acme_JP), no puede duplicar un nombre de perfil de producto en varias instancias. **Práctica recomendada:** Use la convención de nomenclatura &quot;<Name>_<Instance>,&quot; como &quot;Simulations_Only_JP&quot;.

1. [Asigne cada usuario o grupo de usuarios al perfil de producto correspondiente](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) de forma manual o en lotes.

## Guía de administración del usuario completa y vínculos adicionales

* Para obtener más información acerca de la administración de usuarios mediante Adobe Admin Console, consulte &quot;[Guía de administración de Adobe Enterprise &amp; Teams](https://helpx.adobe.com/enterprise/admin-guide.html)&quot;, incluida la [descripción general de Admin Console](https://helpx.adobe.com/es/enterprise/using/admin-console.html)

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
