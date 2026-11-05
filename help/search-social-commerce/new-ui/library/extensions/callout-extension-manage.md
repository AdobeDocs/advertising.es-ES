---
title: Administración de extensiones de llamadas compartidas de Google Ads
description: Obtenga información sobre cómo crear, editar y eliminar extensiones de llamadas compartidas de Google Ads.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%
---
# Administrar extensiones de llamada compartida [!DNL Google Ads]

*[!DNL Google Ads]solo cuentas*

Una extensión de llamada es un texto informativo sobre un producto, servicio o promoción que ofrece su sitio y que se muestra con un anuncio de texto. La red de anuncios puede mostrar 2-4 llamadas con un anuncio.

Usted crea texto de llamada y configuración compartidos a nivel de cuenta para una [cuenta sincronizada de Google Ads](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Las llamadas de la biblioteca no se utilizan con anuncios hasta que se asocian a una campaña o grupo de anuncios admitido en la red de búsqueda.

Para que tus anuncios puedan aparecer con llamadas, asigna al menos dos llamadas por campaña o grupo de anuncios. Las llamadas en el nivel de grupo de anuncios anulan las llamadas en el nivel de campaña.

## Acerca de las vistas [!UICONTROL Callouts] y [!UICONTROL Associations] {#callout-view-about}

En **[!UICONTROL Library]>[!UICONTROL Extensions]**, la ficha **[!UICONTROL Callouts]** enumera las llamadas compartidas de nivel de cuenta. La pestaña **[!UICONTROL Associations]** enumera las asociaciones entre extensiones y entidades de cuenta.

Para ver estas fichas se requiere el permiso [!UICONTROL View Extensions]. La creación, edición y eliminación de llamadas, así como la creación o eliminación de asociaciones, requieren el permiso [!UICONTROL Edit Extensions].

Consulte la [Documentación de Google Ads sobre los límites de la cuenta](https://support.google.com/google-ads/answer/6372658) para obtener la cantidad máxima de extensiones por cuenta.

### Acciones disponibles

* [Creación de una llamada compartida](#callout-create)

* [Editar configuración de llamada compartida](#callout-edit)

* [Eliminar llamadas compartidas](#callout-delete)

* [Asociar llamadas compartidas con campañas y grupos de anuncios](ad-extension-association-manage.md#callout-associate)

* [Eliminar asociaciones de extensión](ad-extension-association-manage.md#association-delete)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

## Creación de una llamada compartida {#callout-create}

1. En el menú principal, haga clic en **[!UICONTROL Library]>[!UICONTROL Extensions]** y luego haga clic en la ficha **[!UICONTROL Callouts]**.

1. Haga clic en **[!UICONTROL Create Callout]**.

1. En **[!UICONTROL Basic Settings]**, seleccione [!DNL Google Ads] y la cuenta.

1. Escriba la [configuración de llamada compartida](#shared-callout-settings).

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Revise la configuración. Para cambiar una configuración, haga clic en **[!UICONTROL Edit]** en la sección correspondiente.

1. Haga clic en **[!UICONTROL Create]**.

Después de crear la llamada, [asóciela a una campaña o a un grupo de anuncios](ad-extension-association-manage.md#callout-associate).

## Editar configuración de llamada compartida {#callout-edit}

Se puede editar una llamada compartida a la vez. No puede cambiar su fecha de inicio después de crearla.

1. En el menú principal, haga clic en **[!UICONTROL Library]>[!UICONTROL Extensions]** y luego haga clic en la ficha **[!UICONTROL Callouts]**.

1. Seleccione la casilla de verificación situada junto a una llamada.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. Editar la [configuración de llamada compartida](#shared-callout-settings).

1. Haga clic en **[!UICONTROL Review and Save]**, revise la configuración y haga clic en **[!UICONTROL Update]**.

## Eliminar llamadas compartidas {#callout-delete}

1. En el menú principal, haga clic en **[!UICONTROL Library]>[!UICONTROL Extensions]** y luego haga clic en la ficha **[!UICONTROL Callouts]**.

1. Seleccione la casilla de verificación situada junto a cada llamada compartida que desee eliminar.

   Para obtener información sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

Para quitar una asociación sin eliminar la llamada compartida de la biblioteca, [elimine la asociación](ad-extension-association-manage.md#association-delete).

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

## Configuración de llamadas compartidas {#shared-callout-settings}

Para obtener directivas y motivos adicionales para desaprobar llamadas, consulte los [requisitos de llamadas de Google Ads](https://support.google.com/adspolicy/answer/1054212).

**[!UICONTROL Callout Text]:** El texto que debe aparecer. Puede incluir hasta 25 caracteres de un solo byte o 12 de doble byte. No puede incluir signos de exclamación o puntuación al principio del texto.

**[!UICONTROL Start Date]:** (opcional; solo creación) Primera fecha en la que se puede mostrar la llamada. El valor predeterminado es el día actual. Para especificar una fecha futura, escríbala en formato MM/DD/AAAA o utilice el selector de fechas. La fecha de inicio es de solo lectura para los rótulos existentes.

**[!UICONTROL End Date]:** (opcional) la última fecha en la que se puede mostrar la llamada. De forma predeterminada, la llamada se puede mostrar indefinidamente. Para especificar una fecha de finalización, indíquela en formato MM/DD/AAAA o utilice el selector de fechas.

**[!UICONTROL Mobile Preference]:** (opcional) permite que [!DNL Google Ads] intente mostrar la extensión a usuarios de dispositivos móviles en lugar de a usuarios de equipos de escritorio o tabletas. De lo contrario, la extensión puede aparecer en cualquier tipo de dispositivo. [!DNL Google Ads] no garantiza que mostrará la extensión en el tipo de dispositivo preferido.

## Datos de rendimiento para llamadas {#callout-performance}

Los mapas de Search, Social y Commerce hacen clic en una extensión de anuncio y muestran las conversiones resultantes a la palabra clave asociada con el anuncio en el que aparece la extensión. Los datos de clics y costes de nivel de extensión no están disponibles en Search, Social y Commerce.

Puede ver los datos de costos y clics en el nivel de extensión en la interfaz [!DNL Google Ads].

>[!MORELIKETHIS]
>
>* [Administrar extensiones de vínculos de sitios compartidos](sitelink-extension-manage.md)
>* [Administrar asociaciones de extensiones de publicidad](ad-extension-association-manage.md)
