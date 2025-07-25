---
title: Administrar vínculos de sitios compartidos
description: Obtenga información sobre cómo crear y administrar extensiones de vínculos de sitios compartidos.
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Administrar vínculos de sitios compartidos

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solamente*

Cree y administre vínculos de sitios compartidos de nivel de cuenta para cualquier cuenta sincronizada de [!DNL Google Ads] o [!DNL Microsoft Advertising] desde la biblioteca de [!UICONTROL Extensions] > [!UICONTROL Sitelinks].

## Crear un vínculo de sitio compartido

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Escriba la [configuración de vínculos de sitios compartidos](#shared-sitelink-settings).

1. Haga clic en **[!UICONTROL Post]**.

Una vez creado un vínculo de sitio, puede [asignarlo a una cuenta, campaña o grupo de anuncios](sitelink-extension-associate.md).

## Editar configuración de vínculos de sitios compartidos

Puede editar un vínculo de sitio compartido a la vez.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Seleccione la casilla de verificación situada junto al vínculo del sitio que desea editar.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite la [configuración de vínculos de sitios compartidos](#shared-sitelink-settings).

1. Haga clic en **[!UICONTROL Post]**.

## Eliminar vínculos de sitios compartidos

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Active la casilla de verificación situada junto a cada vínculo de sitio compartido que desee eliminar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas, haga clic en ![Más](/help/search-social-commerce/assets/more.png "Más") y seleccione **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Delete]**.

## Configuración de vínculos de sitios compartidos {#shared-sitelink-settings}

Para obtener directivas y motivos adicionales para la desaprobación de vínculos de sitios, consulte los requisitos de extensión de vínculos de sitios [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) y [[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** El texto que aparecerá para el vínculo. Puede incluir hasta 25 caracteres de un solo byte o 12 de doble byte. El texto del vínculo debe ser único dentro de la cuenta o la campaña.

>[!NOTE]
>
>([!DNL Google Ads]) El texto existente de 35 caracteres se muestra en anuncios en escritorios y tabletas, pero no en dispositivos móviles.

**[!UICONTROL Status]:** Estado de visualización del vínculo de sitio: *[!UICONTROL Active]* o *[!UICONTROL Deleted]* (solo vínculos de sitio existentes). El valor predeterminado para los nuevos vínculos de sitio es *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Texto adicional que el motor de búsqueda puede mostrar debajo del texto del vínculo. Para incluir una descripción, introduzca valores para ambos campos de descripción. Cada campo de descripción puede incluir hasta 35 caracteres de un solo byte o 17 de doble byte.

**[!UICONTROL Start Date]:** (Campañas con vínculos de sitio heredados existentes o sin vínculos de sitio solamente; opcional) La primera fecha en la que se puede mostrar el vínculo de sitio con anuncios en la campaña. El valor predeterminado para los nuevos vínculos de sitio es el día actual. Para especificar una fecha de inicio futura, introduzca una fecha con el formato MM/DD/AAAA o M/D/AAAA, o bien haga clic en   y seleccione una fecha.

**[!UICONTROL End Date]:** (opcional) la última fecha en la que se puede mostrar el vínculo del sitio con anuncios en la campaña. De forma predeterminada, el vínculo del sitio puede mostrarse indefinidamente. Para especificar una fecha de finalización, introduzca una fecha con el formato MM/DD/AAAA o M/D/AAAA, o bien haga clic en   y seleccione una fecha.

**[!UICONTROL Mobile Preference]:** (opcional) permite que la red intente mostrar la extensión del anuncio a usuarios de dispositivos móviles en lugar de a usuarios de equipos de escritorio o tabletas. De forma predeterminada, la opción no está habilitada y la extensión de anuncio aparece en cualquier tipo de dispositivo.

>[!NOTE]
>
>La red no garantiza que muestre la extensión de anuncio en el tipo de dispositivo preferido.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** Dirección URL de la página de aterrizaje a la que se llevan los usuarios del motor de búsqueda cuando hacen clic en el anuncio. Incluya cualquier parámetro que determine el contenido de la página. Si introduce un valor, anula la dirección URL base del anuncio.

Una vez guardado el registro, la dirección URL base incluye cualquier parámetro de datos anexados configurado para la campaña o cuenta.

>[!NOTE]
>
>* (Cuentas con direcciones URL finales) La dirección URL base puede contener redirecciones dentro del dominio o subdominio de la página de aterrizaje, pero no redirecciones fuera de este. La red de anuncios extrae el dominio de esta dirección URL y agrega cualquier ruta de visualización opcional para el anuncio a fin de crear la dirección URL de visualización para el anuncio.
>* ([!DNL Google Ads]) Cada vínculo de sitio de una campaña o grupo de anuncios debe tener una página de aterrizaje única y el contenido de cada página de aterrizaje de vínculo de sitio debe tener aproximadamente un 80 % de contenido único. Por ejemplo, no puede tener vínculos de sitio con vínculos a varios anclajes dentro de la misma página.
>* ([!DNL Google Ads]) Evite utilizar macros que no sustituyan los clics de fuentes que habilitan el seguimiento paralelo. Si el anunciante debe utilizar macros, el equipo de cuenta de Adobe debe trabajar con Asistencia al cliente o con el equipo de implementación para agregarlas.

**[!UICONTROL Tracking Template]:** (opcional): la plantilla de seguimiento o la dirección URL de seguimiento, que especifica todas las redirecciones de dominios de aterrizaje externo y los parámetros de seguimiento, y que también incrusta la dirección URL final de la página de aterrizaje/destino en un parámetro. Ejemplo: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir una redirección.

* Para el seguimiento de conversión de Adobe Advertising, que se aplica cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;Carga automática&quot;, Search, Social y Commerce prefieren automáticamente su propio código de seguimiento de clics al guardar el registro.

* Para ver los parámetros admitidos para incrustar la dirección URL final, consulte ([!DNL Microsoft Advertising] solamente) [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] solamente) los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección &quot;Parámetros disponibles [!DNL ValueTrack]&quot; en la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/6305348).

* Si lo desea, puede incluir parámetros de URL y cualquier parámetro personalizado definido para la campaña, separados por el símbolo &quot;et&quot; (&amp;), como `{lpurl}?matchtype={matchtype}&device={device}`.

* Si lo desea, puede añadir redirecciones y seguimiento de terceros.

>[!NOTE]
>
>* Cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce añadirán automáticamente como prefijo su propio código de redirección y seguimiento al guardar el registro.
>* La plantilla de seguimiento en el nivel más granular anula los valores en todos los niveles superiores. Por ejemplo, si tanto la configuración de la cuenta como la configuración de la palabra clave incluyen un valor, se aplica el valor de la palabra clave.
>* ([!DNL Google Ads]) Si actualiza una plantilla de seguimiento en el nivel de vínculo de sitio o palabra clave, los anuncios relevantes se vuelven a enviar para su revisión. Puede actualizar las plantillas de seguimiento en los niveles de cuenta, campaña o grupo de publicidad sin volver a enviar los anuncios para su aprobación.
>* ([!DNL Microsoft Advertising]) Puede actualizar las plantillas de seguimiento en cualquier nivel sin volver a enviar los anuncios para su aprobación.
>* Para [!DNL Google Ads], evite utilizar macros que no sustituyan los clics de fuentes que habilitan el seguimiento paralelo. Si el anunciante debe utilizar macros, el equipo de cuenta de Adobe debe trabajar con Asistencia al cliente o con el equipo de implementación para agregarlas.

>[!MORELIKETHIS]
>
>* [Acerca de las extensiones de enlaces de sitios](sitelink-extension-about.md)
>* [Asociar vínculos de sitios compartidos con cuentas, campañas y grupos de anuncios](sitelink-extension-associate.md)
