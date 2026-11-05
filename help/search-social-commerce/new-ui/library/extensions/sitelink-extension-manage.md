---
title: Administrar extensiones de vínculos de sitios compartidos
description: Obtenga información sobre cómo crear, editar y eliminar extensiones de vínculos de sitios compartidos.
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
source-wordcount: '1127'
ht-degree: 0%
---
# Administrar extensiones de vínculos de sitios compartidos

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo cuentas*

Un vínculo de sitio es un vínculo de texto adicional en una lista de anuncios de texto. Use vínculos de sitio para llevar a los usuarios directamente a páginas específicas del sitio. La red de anuncios determina qué vínculos de sitios se muestran en función de su relevancia para el anuncio.

Si lo desea, puede incluir texto descriptivo para cada vínculo a sitios. La red de anuncios también puede mostrar una copia de los anuncios existentes en la cuenta cuando sea muy relevante para el vínculo de sitio. [!DNL Google Ads] puede mostrar de 2 a 6 vínculos de sitios en un anuncio para escritorio y hasta cuatro en un anuncio para móviles. [!DNL Microsoft Advertising] puede mostrar dos, cuatro o seis vínculos de sitio con descripciones o de 4 a 6 sin descripciones.

Crea texto y configuración de vínculos de sitios compartidos en el nivel de cuenta para una [cuenta de red de anuncios sincronizada](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Los vínculos de sitio de la biblioteca no se utilizan con anuncios hasta que se asocian con entidades de cuenta.

## Acerca de las vistas [!UICONTROL Sitelinks] y [!UICONTROL Associations] {#sitelink-view-about}

En **[!UICONTROL Library]>[!UICONTROL Extensions]**, la ficha **[!UICONTROL Sitelinks]** muestra los vínculos de sitios compartidos a nivel de cuenta. La pestaña **[!UICONTROL Associations]** enumera las asociaciones entre extensiones y entidades de cuenta.

Para ver estas fichas se requiere el permiso [!UICONTROL View Extensions]. La creación, edición y eliminación de vínculos de sitio, así como la creación o eliminación de asociaciones, requieren el permiso [!UICONTROL Edit Extensions].

Consulte la ayuda de red de anuncios para obtener la cantidad máxima de extensiones por [cuenta de Google Ads](https://support.google.com/google-ads/answer/6372658) y por [cuenta de Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/52001).

### Acciones disponibles

* [Crear un vínculo de sitio compartido](#sitelink-create)

* [Editar configuración de vínculos de sitios compartidos](#sitelink-edit)

* [Eliminar vínculos de sitios compartidos](#sitelink-delete)

* [Asociar vínculos de sitios compartidos con cuentas, campañas y grupos de anuncios](ad-extension-association-manage.md#sitelink-associate)

* [Eliminar asociaciones de extensión](ad-extension-association-manage.md#association-delete)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

## Crear un vínculo de sitio compartido {#sitelink-create}

1. En el menú principal, haga clic en **[!UICONTROL Library]>[!UICONTROL Extensions]** y luego haga clic en la ficha **[!UICONTROL Sitelinks]**.

1. Haga clic en **[!UICONTROL Create Sitelink]**.

1. En **[!UICONTROL Basic Settings]**, seleccione la red publicitaria y la cuenta.

1. Escriba la [configuración de vínculos de sitios compartidos](#shared-sitelink-settings).

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Revise la configuración. Para cambiar una configuración, haga clic en **[!UICONTROL Edit]** en la sección correspondiente.

1. Haga clic en **[!UICONTROL Create]**.

Después de crear el vínculo del sitio, [asócielo a una cuenta, campaña o grupo de anuncios](ad-extension-association-manage.md#sitelink-associate).

## Editar configuración de vínculos de sitios compartidos {#sitelink-edit}

Puede editar un vínculo de sitio compartido a la vez. No puede cambiar su fecha de inicio después de crearla.

1. En el menú principal, haga clic en **[!UICONTROL Library]>[!UICONTROL Extensions]** y luego haga clic en la ficha **[!UICONTROL Sitelinks]**.

1. Seleccione la casilla de verificación situada junto a un vínculo de sitio.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. Edite la [configuración de vínculos de sitios compartidos](#shared-sitelink-settings).

1. Haga clic en **[!UICONTROL Review and Save]**, revise la configuración y haga clic en **[!UICONTROL Update]**.

También puede editar **[!UICONTROL Base URL]** o **[!UICONTROL Tracking Template]** de un enlace de sitio directamente en la tabla de datos haciendo clic en su valor.

## Eliminar vínculos de sitios compartidos {#sitelink-delete}

1. En el menú principal, haga clic en **[!UICONTROL Library]>[!UICONTROL Extensions]** y luego haga clic en la ficha **[!UICONTROL Sitelinks]**.

1. Seleccione la casilla de verificación situada junto a cada vínculo de sitio compartido que desee eliminar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

Para quitar una asociación sin eliminar el vínculo de sitio compartido de la biblioteca, [elimine la asociación](ad-extension-association-manage.md#association-delete).

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

## Configuración de vínculos de sitios compartidos {#shared-sitelink-settings}

Para ver las políticas y los motivos adicionales de desaprobación de vínculos de sitios, consulte los [requisitos de vínculos de sitios de Google Ads](https://support.google.com/adspolicy/answer/1054210) y los [requisitos de vínculos de sitios de Microsoft Advertising](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** El texto que aparecerá para el vínculo. Puede incluir hasta 25 caracteres de un solo byte o 12 de doble byte. El texto del vínculo debe ser único dentro de la cuenta o la campaña.

>[!NOTE]
>
>([!DNL Google Ads]) El texto existente de 35 caracteres se muestra en anuncios en escritorios y tabletas, pero no en dispositivos móviles.

**[!UICONTROL Status]:** Estado de visualización del vínculo de sitio: **[!UICONTROL Active]** o **[!UICONTROL Deleted]** para los vínculos de sitio existentes. Los nuevos vínculos de sitio están activos de forma predeterminada.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Texto adicional que la red de publicidad puede mostrar debajo del texto del vínculo. Para incluir una descripción, introduzca ambos campos. Cada una puede incluir hasta 35 caracteres de un solo byte o 17 de doble byte.

**[!UICONTROL Start Date]:** (opcional; solo creación) La primera fecha en la que se puede mostrar el vínculo de sitio. El valor predeterminado es el día actual. Para especificar una fecha futura, escríbala en formato MM/DD/AAAA o utilice el selector de fechas. La fecha de inicio es de solo lectura para los vínculos de sitio existentes.

**[!UICONTROL End Date]:** (opcional) la última fecha en la que se puede mostrar el vínculo de sitio. De forma predeterminada, el vínculo del sitio puede mostrarse indefinidamente. Para especificar una fecha de finalización, indíquela en formato MM/DD/AAAA o utilice el selector de fechas.

**[!UICONTROL Mobile Preference]:** (opcional) permite que la red intente mostrar la extensión a usuarios de dispositivos móviles en lugar de a usuarios de equipos de escritorio o tabletas. De forma predeterminada, esta opción no está habilitada y la extensión puede aparecer en cualquier tipo de dispositivo. La red no garantiza que muestre la extensión en el tipo de dispositivo preferido.

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]:** (opcional) La dirección URL de seguimiento, incluidas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, con la dirección URL de la página de aterrizaje final incrustada en un parámetro. Por ejemplo, `https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`.

En esta vista, los valores especificados para [!UICONTROL Base URL] y [!UICONTROL Tracking Template] deben comenzar por `http://` o `https://` y no pueden contener espacios.

* Si la configuración de la campaña incluye **[!UICONTROL EF Redirect]** y **[!UICONTROL Auto Upload]**, Search, Social y Commerce añadirán automáticamente como prefijo su propio código de redirección y seguimiento al guardar el registro.

* Para ver los parámetros que incrustan la dirección URL final, consulte la [documentación de Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/56799) o los parámetros &quot;Solo plantilla de seguimiento&quot; en la [documentación de Google Ads ValueTrack](https://support.google.com/google-ads/answer/6305348).

* Puede incluir parámetros de URL y parámetros personalizados de nivel de campaña, separados por el símbolo et (`&`), y redirecciones y seguimiento de terceros.

* La plantilla de seguimiento en el nivel más granular anula las plantillas en los niveles superiores.

>[!NOTE]
>
>* En el caso de las cuentas con direcciones URL finales, la dirección URL base puede contener redirecciones dentro del dominio o subdominio de la página de aterrizaje, pero no fuera de este. La red de anuncios extrae el dominio para crear la dirección URL de visualización.
>* ([!DNL Google Ads]) Cada vínculo de sitio de una campaña o grupo de anuncios debe tener una página de aterrizaje única con un contenido único de aproximadamente el 80 %. No utilice vínculos a varios anclajes en la misma página como páginas de aterrizaje de vínculos de sitio independientes.
>* ([!DNL Google Ads]) Al actualizar una plantilla de seguimiento en el nivel de vínculo de sitio o palabra clave, se vuelven a enviar los anuncios relevantes para su revisión. Al actualizarla en el nivel de cuenta, campaña o grupo de publicidad, no se vuelven a enviar los anuncios.
>* ([!DNL Microsoft Advertising]) Puede actualizar las plantillas de seguimiento en cualquier nivel sin volver a enviar los anuncios para su aprobación.
>* ([!DNL Google Ads]) Evite las macros, que no sustituyen los clics de fuentes que habilitan el seguimiento paralelo. Si se requieren macros, el equipo de cuenta de Adobe trabaja con Asistencia al cliente o con el equipo de implementación para agregarlas.

## Datos de rendimiento para vínculos de sitios {#sitelink-performance}

Los mapas de Search, Social y Commerce hacen clic en una extensión de anuncio y muestran las conversiones resultantes a la palabra clave asociada con el anuncio en el que aparece la extensión. Los datos de clics y costes de nivel de extensión no están disponibles en Search, Social y Commerce.

En [!UICONTROL Transaction Report], un valor [!UICONTROL Link Type] de `sl:<Sitelink text>`, como `sl:See Current Offers`, identifica una transacción a partir de un vínculo de sitio en lugar del anuncio en sí. Consulte &quot;[Informe de transacciones](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)&quot;.

Puede ver los datos de costes y clics en el nivel de extensión en la interfaz de la red de publicidad.

>[!MORELIKETHIS]
>
>* [Administrar extensiones de llamadas compartidas de Google Ads](callout-extension-manage.md)
>* [Administrar asociaciones de extensiones de publicidad](ad-extension-association-manage.md)
