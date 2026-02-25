---
title: (Nueva IU) Administrar las cuentas de red de publicidad
description: Obtenga información sobre cómo configurar y administrar los detalles de la cuenta en la nueva interfaz de usuario para una red de publicidad sincronizada mediante la API de red de publicidad.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# (Nueva IU) Administrar las cuentas de red de publicidad a través de la conexión API

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*característica de Beta*

<!-- Move out info about Naver into a separate page -->

A continuación se indican instrucciones para administrar cuentas de red de anuncios que Search, Social y Commerce sincronizan mediante la API de la red de anuncios.

<!-- Move out info about Naver into a separate page -->

Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Crear y agregar detalles de cuenta de red {#create-account}

Para habilitar la sincronización de una cuenta, debe crear un registro de cuenta correspondiente que contenga las credenciales de acceso a la cuenta y las opciones de seguimiento y con el estado *habilitado*.

>[!NOTE]
>
>Para crear una cuenta real en la red de anuncios, vaya al sitio web de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Haga clic en **[!UICONTROL Create Account]**.

1. Haga clic en el nombre de la red publicitaria y, a continuación, haga clic en **[!UICONTROL Next]**.

1. (Todas las redes de anuncios excepto [!DNL Yandex]) Inicie sesión en la red de anuncios con las credenciales del anunciante. Seleccione la opción &quot;Seguimiento de cuentas para esta cuenta&quot;. A continuación, en la esquina superior derecha, haga clic en **[!UICONTROL Next]**.

1. Especifique la [configuración de la cuenta](#account-settings-api):

   1. En la ficha **[!UICONTROL Select Accounts]**, especifique la configuración general de la cuenta. Especifique las credenciales de la cuenta para [!DNL Yandex] cuentas.

   1. Haga clic en la ficha **[!UICONTROL Setup Tracking]** e introduzca la configuración de seguimiento.

   1. (Anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md)) Haga clic en la ficha **[!UICONTROL Set up Adobe Analytics]** y seleccione los [!DNL Analytics] grupos de informes que quiera usar para realizar el seguimiento y generar informes de la actividad de la campaña.

1. Haga clic en **[!UICONTROL Save]**.

   Los datos recientes de coste y clics de todas las campañas de la cuenta se actualizan cada hora en Search, Social y Commerce. De forma predeterminada, los datos están disponibles durante los últimos 5 a 10 días, según la red de publicidad. Sin embargo, si es necesario, el equipo de inicio del proyecto puede recuperar los datos durante los últimos 60 días.

## Editar los detalles de la cuenta de red del anuncio {#edit-account}

Para volver a autenticar la configuración de la cuenta a fin de actualizar la conexión o los permisos de actualización, habilite o deshabilite la actividad en una cuenta, cambie los parámetros de seguimiento predeterminados en una cuenta o cambie los grupos de informes [!DNL Analytics] que se utilizarán para el seguimiento y la creación de informes y, a continuación, edite los detalles de la cuenta.

>[!NOTE]
>
>Para editar una cuenta real en la red de anuncios, vaya al sitio web de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Seleccione la cuenta de cualquiera de las siguientes maneras:

   * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

   * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

1. Editar la [configuración de la cuenta](#account-settings-api):

   1. (Opcional) En la ficha **[!UICONTROL Account Details]**, edite los detalles de la cuenta.

   1. (Opcional) Haga clic en la ficha **[!UICONTROL Setup Tracking]** y edite la configuración de seguimiento.

   1. (Opcional; anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md)) Haga clic en la ficha **[!UICONTROL Set up Adobe Analytics]** y edite los [!DNL Analytics] grupos de informes que quiera usar para rastrear y generar informes sobre la actividad de la campaña.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Haga clic en **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social y Commerce deben sincronizar los datos de la nueva cuenta con la de la red de anuncios. Esto sucede automáticamente una vez al día, o con mayor frecuencia cuando Search, Social y Commerce detectan cambios en la red de anuncios.

## Volver a autenticar una cuenta de red de publicidad {#reauthenticate}

Para actualizar la conexión de red de publicidad o los permisos de actualización de la cuenta, vuelva a autenticar la cuenta.

1. (Si ha iniciado sesión en otra cuenta para la misma red de anuncios en la misma aplicación de explorador) Cierre sesión en cualquier cuenta que no sea la del anunciante.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. Seleccione la cuenta de cualquiera de las siguientes maneras:

   * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

   * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

1. En la ficha **[!UICONTROL Account Details]**, haga clic en **[!UICONTROL Re authenticate]** e inicie sesión en la red de publicidad con las credenciales del anunciante.

1. Haga clic en **[!UICONTROL Save]**.

## Habilitar o deshabilitar las cuentas de red de publicidad {#enable-disable-account}

Al habilitar una cuenta de red de publicidad, Search, Social y Commerce sincronizan los datos de campaña con la cuenta (cuando es compatible) y envían ofertas automatizadas o presupuestos de campaña para las campañas en portafolios. Cuando deshabilita una cuenta de red de publicidad, Search, Social y Commerce detienen toda la actividad en la cuenta. Los datos recopilados mientras la cuenta estaba activa se siguen almacenando, pero las vistas e informes de administración de campañas no incluyen datos del período de tiempo en el que la cuenta está deshabilitada. Más tarde puede volver a habilitar la cuenta para reanudar la actividad con la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Realice una de las acciones siguientes:

   * (Desde la vista [!UICONTROL Accounts]):

      * (Para habilitar la cuenta) Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Activate]** en la barra de herramientas de acciones en masa.

      * (Para deshabilitar la cuenta) Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Pause]** en la barra de herramientas de acciones en masa.

   * (Desde la configuración de la cuenta):

      1. Seleccione la cuenta de cualquiera de las siguientes maneras:

         * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

         * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

      1. En la ficha **[!UICONTROL Account Details]**, desactive **[!UICONTROL Account enabled]**.

      1. Haga clic en **[!UICONTROL Save]**.

## Configuración de cuenta de red de anuncios {#account-settings-api}

La configuración de la cuenta varía según la red de anuncios. Es posible que no vea todas las configuraciones a continuación.

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### Ficha [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Nombre que se mostrará para la cuenta en Search, Social y Commerce.

>[!NOTE]
>
>Si tiene una integración de Search, Social y Commerce-Adobe Analytics y cambia el nombre de la cuenta de búsqueda, pida al equipo de cuenta de Adobe que actualice la asignación.

**[!DNL [Cuentas de red de anuncios]]:** (visible mientras crea una cuenta) Cuenta de red de anuncios que se va a sincronizar.

**[Detalles de inicio de sesión]:** (solo cuentas de Yandex) Las credenciales de la cuenta que se deben usar:

* **[!UICONTROL Login]:** El nombre o ID de inicio de sesión para habilitar el acceso de API a la cuenta.

* **[!UICONTROL Password]:** Contraseña de la cuenta.

* **[!UICONTROL Access Key]:** Clave de acceso para la cuenta de desarrollador que se va a usar.

* **[!UICONTROL Application ID]:** El token de desarrollador que se va a usar para la cuenta. Se utiliza el mismo token para todas las cuentas de [!DNL Yandex].

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] cuentas con la configuración Cuenta compartida deshabilitada solamente; opcional) Identificador numérico de la campaña usado para pagar todas las campañas publicitarias de la cuenta.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] cuentas con la configuración Cuenta compartida deshabilitada solamente; opcional) El token de desarrollador que se usará para las llamadas de API relacionadas con las finanzas, como para reasignar dinero de la cartera entre las campañas del anunciante según sea necesario para la optimización del portafolio.

**[!UICONTROL Network Account ID]:** (Todas las redes de publicidad excepto [!DNL Yandex]: id. de cuenta asignado por la red de publicidad.

>[!NOTE]
>
>Las cuentas de administrador de red de anuncios no son compatibles aquí. Para identificar una cuenta de administrador para [!DNL Microsoft Advertising], use el campo Identificador de cuenta maestra o Cuenta MCC, respectivamente. Para [configurar credenciales para una [!DNL Google Ads] cuenta de administrador](/help/search-social-commerce/admin/manager-accounts.md), vaya a [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Currency]:** (solo lectura) La abreviatura de la moneda utilizada para la cuenta. Este valor se rellena automáticamente con la moneda configurada para la cuenta en la red de publicidad una vez guardado el registro.

**[!UICONTROL Time Zone]:** Zona horaria del anunciante. Este valor se rellena automáticamente con la zona horaria configurada para la cuenta de Search, Social y Commerce del anunciante una vez guardado el registro.

**[!UICONTROL Login]:** (solo lectura) Cuenta de usuario utilizada para iniciar sesión en la cuenta.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social y Commerce sincronizan los datos de campaña con la cuenta (cuando es compatible) y envían ofertas automatizadas o presupuestos de campaña para campañas en portafolios.

## Ficha [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Si se habilita o no el seguimiento, use el servicio de seguimiento de conversiones de Adobe Advertising. Este método genera ID únicos de seguimiento de clics y redirige a los usuarios al servidor de Adobe Advertising con fines de seguimiento antes de enviarlos a la página de aterrizaje del cliente. Este método tiene opciones de seguimiento predeterminadas que se pueden personalizar de forma opcional y también se pueden especificar parámetros para anexar a cada dirección URL.

Para habilitar esta característica, active **[Habilitar seguimiento]**.

>[!NOTE]
>
>* Si cambia esta configuración, debe volver a generar las direcciones URL de seguimiento de la cuenta.
>* Las opciones de seguimiento a nivel de campaña anulan la configuración a nivel de cuenta.

**[!UICONTROL Tracking Type]:** (cuando el seguimiento de Buscar, Social y Commerce está habilitado) Método para redirigir a los usuarios finales a la dirección URL final o a la dirección URL de destino. La opción seleccionada se aplica a todas las unidades de oferta de la cuenta o campaña. La configuración predeterminada de nivel de cuenta se hereda de la configuración de seguimiento del anunciante y la configuración predeterminada de nivel de campaña se hereda de la configuración de la cuenta.

* *[!UICONTROL Standard]:* Para redirigir al usuario final a la dirección URL especificada.

* *[!UICONTROL Token]:* Para redirigir al usuario final a la dirección URL y registrar también el identificador de búsqueda, social y Commerce para el clic (`ef_id`) como parámetro de cadena de consulta, que se usa como token. Elija esta opción si desea realizar un informe de las transacciones sin conexión, si desea que Search, Social y Commerce intercambien datos con Adobe Analytics o si desea realizar un seguimiento de todas las conversiones que se producen en [!DNL Apple Safari] exploradores.

>[!NOTE]
>
>* Si cambia de [!UICONTROL Standard] a [!UICONTROL Token], o viceversa, debe volver a generar las direcciones URL de seguimiento para la cuenta.
>* Puede anular la configuración de nivel de cuenta en el nivel de campaña.

**[!UICONTROL Auto Update]:** (cuando el seguimiento de Search, Social y Commerce está habilitado) Estandariza las direcciones URL de seguimiento para comprobar la compatibilidad entre exploradores y servidores. Search, Social y Commerce cargan automáticamente lo siguiente en la red de anuncios durante la siguiente sincronización: (a) parámetros de seguimiento de Search, Social y Commerce para plantillas de seguimiento y los mismos parámetros añadidos a las direcciones URL finales o (b) nuevas direcciones URL de destino incrustadas con el código de seguimiento de Search, Social y Commerce. Para anunciantes con una [integración Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) y una configuración de ID de AMO del lado del servidor (s_kwcid), la carga también incluye [parámetros de ID de AMO](/help/integrations/analytics/ids.md#amo-id) para sus cuentas de [!DNL Google Ads] y [!DNL Microsoft Advertising]. La configuración predeterminada en el nivel de cuenta se hereda de la configuración de seguimiento del anunciante. Puede anular la configuración de nivel de cuenta en el nivel de campaña.

Las direcciones URL de seguimiento se actualizan a diario solo para las entidades que no están sincronizadas (es decir, las nuevas entidades que se añadieron y las entidades existentes cuyas propiedades han cambiado). Por lo tanto, si cambia esta configuración de deshabilitada a habilitada para un anunciante, cuenta o campaña existente, las direcciones URL de seguimiento no se actualizan para las entidades existentes que ya están sincronizadas. Para agregar el seguimiento a las direcciones URL de entidades sincronizadas existentes, póngase en contacto con el equipo de cuenta de Adobe y solicite un proceso de sincronización manual único. El proceso de carga automática gestionará los cambios futuros.

**[!UICONTROL URL Encoding]:** (cuando el seguimiento de Search, Social y Commerce está habilitado; solo cuentas con direcciones URL de destino) Codifica la dirección URL base en la barra de direcciones del explorador del usuario final (como `%3D` en lugar de `=`):

**[!UICONTROL Tracking Level]:** (cuando el seguimiento de Search, Social y Commerce está habilitado; disponible en los niveles de cuenta y campaña; no aplicable a las redes de anuncios que están habilitadas para el seguimiento paralelo) Nivel en el que se debe realizar el seguimiento de los clics y los ingresos agregando una redirección (cuando corresponda) y anexando parámetros a las direcciones URL relevantes:

* *[!UICONTROL Keyword]:* Para realizar el seguimiento de los datos solamente en el nivel de palabra clave. No disponible para [!DNL Yandex].

* *[!UICONTROL Ad]:* Para realizar el seguimiento de los datos solamente en el nivel de anuncio. No disponible para [!DNL Naver].

* *[!UICONTROL Keyword and Ad]:* Para hacer un seguimiento de los datos en los niveles de palabra clave y anuncio. No disponible para [!DNL Naver] y [!DNL Yandex].

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] y [!DNL Microsoft Advertising] solo cuentas; opcional) Cualquier parámetro que se anexe al final de las direcciones URL finales para realizar el seguimiento de la información; incluya todos los parámetros que su empresa debe seguir.

Ejemplo: `param1=value1&param2=value2`

Las cuentas que usan el rastreo de clics de Adobe Advertising deben incluir el identificador de clics de la red de publicidad (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para Google) en el sufijo. Las cuentas con una integración de Adobe Analytics deben usar el parámetro de ID de AMO (que comienza con `s_kwcid`). Si la cuenta tiene una implementación de AMO ID del lado del servidor, el parámetro se añade automáticamente cuando un usuario hace clic en un anuncio; de lo contrario, debe añadirlo aquí de forma manual. Vea los [formatos de sufijo necesarios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y [formatos de sufijo necesarios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* La configuración de seguimiento [!UICONTROL Auto Update] no actualiza este campo.
>* Los sufijos finales de URL en los niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el editor de la red de anuncios.

**URL de seguimiento de cuenta**: ([!DNL Google Ads], [!DNL Microsoft Advertising] y [!DNL Yahoo! Japan Ads] cuentas solamente; opcional) La plantilla de seguimiento predeterminada de la cuenta, que especifica todas las redirecciones de dominios de aterrizaje y parámetros de seguimiento, e incrusta también la dirección URL final de la página de aterrizaje en un parámetro. Ejemplo: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir una redirección.

* Para incrustar la dirección URL final:

   * ([!DNL Google Ads] y [!DNL Microsoft Advertising] solamente) Para obtener una lista de parámetros que indiquen las direcciones URL finales en las plantillas de seguimiento, vea la ([!DNL Microsoft Advertising] solamente) [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] solamente) los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección &quot;Parámetros disponibles [!DNL ValueTrack]&quot; en la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] solamente) Use el parámetro `!{lpurl}` para indicar la dirección URL de la página de aterrizaje.

* Si lo desea, puede incluir parámetros de URL y cualquier parámetro personalizado definido para la campaña, separados por el símbolo &quot;et&quot; (&amp;), como `{lpurl}?matchtype={matchtype}&device={device}`.

* Si lo desea, puede añadir redirecciones y seguimiento de terceros.

* Cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce añadirán automáticamente como prefijo su propio código de redirección y seguimiento al guardar el registro.

>[!NOTE]
>
>* Para [!DNL Google Ads], evite utilizar macros que no sustituyan los clics de fuentes que habilitan el seguimiento paralelo. Si el anunciante debe utilizar macros, el equipo de cuenta de Adobe debe trabajar con Asistencia al cliente o con el equipo de implementación para agregarlas.
>* La plantilla de seguimiento en el nivel más granular anula los valores en todos los niveles superiores. Por ejemplo, si tanto la configuración de la cuenta como la configuración de la palabra clave incluyen un valor, se aplica el valor de la palabra clave.
>* Si actualiza una plantilla de seguimiento en el nivel de anuncio, vínculo de sitio o palabra clave, los anuncios relevantes se vuelven a enviar para su revisión. Puede actualizar las plantillas de seguimiento en los niveles de cuenta, campaña o grupo de publicidad sin volver a enviar los anuncios para su aprobación.

## Ficha [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md); opcional) Uno o más grupos de informes de Analytics a los que Search, Social y Commerce envían los datos que recopila de la red de anuncios, incluidas las clasificaciones de entidades y los datos de clics de la cuenta. Esta función solo está disponible para las redes de publicidad admitidas.

Para que los datos aparezcan en los grupos de informes, ya sea (a) la función de ID de AMO del lado del servidor debe estar configurada para la cuenta o (b) la configuración de nivel de anunciante a &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; debe estar habilitada. Además, la cuenta del anunciante [!DNL Analytics] debe estar configurada para recibir datos de Search, Social y Commerce. Para obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

>[!MORELIKETHIS]
>
>* [Acerca de las cuentas de red de anuncios](../ad-network-account-about.md)
>* [Administrar cuentas de centros comerciales](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [Actualizar el código de seguimiento s_kwcid para una [!DNL Google Ads] cuenta](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
