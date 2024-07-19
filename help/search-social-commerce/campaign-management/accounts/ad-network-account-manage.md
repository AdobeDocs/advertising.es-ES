---
title: Administrar las cuentas de red de publicidad
description: Obtenga información acerca de cómo configurar y administrar los detalles de cuenta para una cuenta de red de publicidad.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# Administrar las cuentas de red de publicidad

A continuación encontrará instrucciones para crear y editar los detalles de la cuenta de red de anuncios, actualizar el token [!DNL oAuth] de una cuenta y deshabilitar cuentas.

Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Crear y agregar detalles de cuenta de red {#create-account}

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Para habilitar la sincronización o el seguimiento de una cuenta, debe crear un registro de cuenta correspondiente que contenga las credenciales de acceso a la cuenta y las opciones de seguimiento y con el estado *activo*.

>[!NOTE]
>
>* La compatibilidad no está disponible para las nuevas cuentas de [!DNL Baidu].
>* Para crear una cuenta real en la red de anuncios, vaya al sitio web de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Especifique la [configuración de la cuenta](#account-settings):

   1. Haga clic en el nombre de la red publicitaria y, a continuación, haga clic en **[!UICONTROL Next]**.

   1. En la sección **[!UICONTROL Account Details]**, escriba los detalles de la cuenta.

      Para las redes de anuncios que utilizan el tipo de autorización de inicio de sesión &quot;[!UICONTROL oAuth]&quot;, permita que Search, Social y Commerce accedan a la cuenta mediante el [protocolo de autorización de OAuth](https://oauth.net/2/):

      1. Escriba el valor **[!UICONTROL Login]** de la cuenta; si lo desea, escriba la contraseña y haga clic en **[!UICONTROL Authenticate]**.

         La práctica recomendada es utilizar el inicio de sesión para acceder a la cuenta mediante API. Introduzca la contraseña cuando desee cifrarla y guardarla, de modo que el equipo de cuenta de Adobe pueda actualizar los tokens según sea necesario.

      1. (Si no ha iniciado sesión en la cuenta del anunciante) Inicie sesión en la cuenta publicitaria del anunciante. La práctica recomendada es utilizar las credenciales de para el acceso de la API a la cuenta.

      1. En la pantalla de solicitud de permiso/acceso, haga clic en el botón para confirmar el permiso.

      1. Copie la cadena de autenticación en la ventana emergente que se abre y péguela en el campo **[!UICONTROL oAuth Token]**.

      1. Especifique los detalles de la cuenta restante.

   1. Haga clic en **[!UICONTROL Set Account Tracking]** e introduzca la configuración de seguimiento.

1. Haga clic en **[!UICONTROL Post]**.

   Los datos recientes de coste y clics de todas las campañas de la cuenta están disponibles en Search, Social y Commerce en unas 24 horas. De forma predeterminada, los datos están disponibles durante los últimos 5 a 10 días, según la red de publicidad. Sin embargo, si es necesario, el equipo de inicio del proyecto puede recuperar los datos durante los últimos 60 días.

## Editar los detalles de la cuenta de red del anuncio {#edit-account}

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Si cambian las credenciales de la cuenta, desea cambiar los parámetros de seguimiento predeterminados en una cuenta o desea habilitar o deshabilitar la actividad en una cuenta y, a continuación, editar los detalles de la cuenta.

>[!NOTE]
>
>Para editar una cuenta real en la red de anuncios, vaya al sitio web de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenga el cursor sobre el nombre de la cuenta, haga clic en ![Más](/help/search-social-commerce/assets/more-filters.png "Más") y, a continuación, seleccione **[!UICONTROL Edit]**.

1. Editar la [configuración de la cuenta](#account-settings):

   1. (Opcional) Edite los detalles de la cuenta.

   1. (Opcional) Haga clic en **[!UICONTROL Set Account Tracking]** y edite la configuración de seguimiento.

1. Haga clic en **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social y Commerce deben sincronizar los datos de la nueva cuenta con la de la red de anuncios. Esto sucede automáticamente una vez al día, o con mayor frecuencia cuando Search, Social y Commerce detectan cambios en la red de anuncios.

## Actualizar tokens de acceso de oAuth para cuentas de búsqueda {#refresh-oauth-tokens}

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Si Search, Social y Commerce accede a la cuenta mediante el [protocolo de autorización de OAuth](https://oauth.net/2/) y las credenciales de la cuenta cambian, o si se requiere acceso adicional para admitir nuevas funciones en Search, Social y Commerce, debe obtener un nuevo token de acceso para la cuenta.

El equipo de cuenta de Adobe le informará si las nuevas funciones requieren un token nuevo.

1. (Si ha iniciado sesión en otra cuenta para la misma red de anuncios en la misma aplicación de explorador) Cierre sesión en cualquier cuenta que no sea la del anunciante.

1. En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Mantenga el cursor sobre el nombre de la cuenta, haga clic en ![Más](/help/search-social-commerce/assets/more-filters.png "Más") y, a continuación, seleccione **[!UICONTROL Edit]**.

1. Obtenga un nuevo token de acceso:

   1. Haga clic en **[!UICONTROL Get oAuth Token]**.

   1. (Si no ha iniciado sesión en la cuenta del anunciante) Inicie sesión en la cuenta publicitaria del anunciante. La práctica recomendada es utilizar las credenciales de para el acceso de la API a la cuenta.

   1. En la pantalla de solicitud de permiso/acceso, haga clic en el botón para confirmar el permiso.

   1. Copie la cadena de autenticación en la ventana emergente que se abre y péguela en el campo **[!UICONTROL oAuth Token]**.

1. Haga clic en **[!UICONTROL Post]**.

## Habilitar o deshabilitar las cuentas de red de publicidad {#enable-disable-account}

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Al habilitar una cuenta de red de publicidad, Search, Social y Commerce sincronizan los datos de campaña con la cuenta (cuando es compatible) y envían ofertas automatizadas o presupuestos de campaña para las campañas en portafolios. Al deshabilitar una cuenta de red de publicidad, Search, Social y Commerce detienen toda la actividad en la cuenta. Los datos recopilados mientras la cuenta estaba activa se siguen almacenando, pero las vistas e informes de administración de campañas no incluyen datos del período de tiempo en el que la cuenta está deshabilitada. Más tarde puede volver a habilitar la cuenta para reanudar la actividad con la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. En el submenú, haga clic en **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Realice una de las acciones siguientes:

   * (Para cambiar el estado de una sola cuenta) Mantenga el cursor sobre el nombre de la cuenta, haga clic en ![Más](/help/search-social-commerce/assets/more-filters.png "Más") y seleccione **[!UICONTROL Edit]**. Cambie **[!UICONTROL Status]** a *Habilitado* o *Deshabilitado* y, a continuación, haga clic en **[!UICONTROL Post]**.

   * (Para cambiar el estado de una o varias cuentas) Haga lo siguiente:

      1. Seleccione la casilla de verificación situada junto a cada cuenta.

         Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Activar icono](/help/search-social-commerce/assets/activate.png "Activar icono") para habilitar la cuenta o en ![Icono Deshabilitar](/help/search-social-commerce/assets/disable.png "Icono Deshabilitar") para deshabilitarla.

## Configuración de cuenta de red de anuncios {#account-settings}

>[!NOTE]
>
>Solo el administrador de cuentas de agencia, el administrador de cuentas [!DNL Adobe] y los usuarios administradores pueden configurar las opciones de la cuenta.

### Detalles de cuenta

**[!UICONTROL SE Account ID]:** (todas las cuentas excepto las cuentas de [!DNL Naver] y [!DNL Yandex]; editables solo para cuentas nuevas) Identificador de cuenta asignado por la red de publicidad.

>[!NOTE]
>
>Las cuentas de administrador de red de anuncios no son compatibles aquí. Para identificar una cuenta de administrador para [!DNL Microsoft Advertising] o [!DNL Yandex], use el campo Identificador de cuenta maestra o Cuenta MCC, respectivamente. Para [configurar credenciales para una [!DNL Google Ads] cuenta de administrador](/help/search-social-commerce/admin/manager-accounts.md), vaya a [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** Nombre que se mostrará para la cuenta en Search, Social y Commerce.

>[!NOTE]
>
>Si tiene una integración de Search, Social y Commerce-Adobe Analytics y cambia el nombre de la cuenta de búsqueda, notifique al equipo de cuenta de Adobe para que pueda actualizar la asignación.

**[!UICONTROL Login Details]: \[Tipo de inicio de sesión\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] solamente) Si se autorizan los inicios de sesión en la cuenta mediante:

* *[!UICONTROL oAuth]* (valor predeterminado): para usar el [[!DNL OAuth] protocolo de autorización](https://oauth.net/2/).

* *[!UICONTROL Password]:* Para usar la contraseña del cliente.

Para las cuentas de [!DNL Microsoft Advertising], solo se pueden usar los inicios de sesión autorizados por [!DNL oAuth].

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Todas las redes de publicidad excepto [!DNL Naver]) El nombre de inicio de sesión o ID para habilitar el acceso de API a la cuenta.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth] habilitadas y todas las demás redes excepto [!DNL Meta] y [!DNL Yandex]) El token de la cuenta para autorizar inicios de sesión mediante el [[!DNL OAuth] protocolo de autorización](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Todas las redes de publicidad excepto [!DNL Naver]) Contraseña de la cuenta. Este campo es obligatorio en las cuentas habilitadas para contraseña de [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] y [!DNL Yandex]. Para las cuentas habilitadas para [!DNL oAuth], este campo es opcional; utilícelo cuando desee cifrar y guardar la contraseña para que el administrador de cuentas pueda actualizar los tokens según sea necesario.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Yandex] cuentas solamente) Clave de acceso para la cuenta de desarrollador que se va a usar.

**[!UICONTROL Currency]:** La abreviatura de la moneda utilizada para la cuenta. Este campo es editable para las nuevas cuentas de [!DNL Naver]. Para todas las demás redes de búsqueda, el valor se rellena automáticamente con la moneda configurada para la cuenta en la red de publicidad una vez que se guarda el registro.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] y [!DNL Microsoft Advertising] solo cuentas; opcional) Cualquier parámetro que se anexe al final de las direcciones URL finales para realizar el seguimiento de la información; incluya todos los parámetros que su empresa debe seguir.

Ejemplo: `param1=value1&param2=value2`

Las cuentas que usan el rastreo de clics en el Adobe Advertising deben incluir el identificador de clic (`msclkid` para [!DNL Microsoft Advertising]; `gclid` para Google) de la red publicitaria en el sufijo. Las cuentas con una integración de Adobe Analytics deben usar el parámetro de ID de AMO (que comienza con `s_kwcid`). Si la cuenta tiene una implementación de AMO ID del lado del servidor, el parámetro se añade automáticamente cuando un usuario hace clic en un anuncio; de lo contrario, debe añadirlo aquí de forma manual. Vea los [formatos de sufijo necesarios para [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) y [formatos de sufijo necesarios para [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* La configuración de seguimiento [!UICONTROL Auto Upload] no actualiza este campo.
>* Los sufijos finales de URL en los niveles inferiores anulan el sufijo de nivel de cuenta. Para facilitar el mantenimiento, utilice únicamente el sufijo de nivel de cuenta a menos que sea necesario realizar un seguimiento diferente para los componentes de cuenta individuales. Para configurar un sufijo en el nivel de grupo de anuncios o inferior, utilice el editor de la red de anuncios.

**Zona horaria:** (todas las redes de anuncios excepto [!DNL Baidu] y [!DNL Yahoo! Display Network]) Zona horaria del anunciante. Este campo es editable y opcional para las nuevas cuentas de [!DNL Naver]. Para todas las demás redes de búsqueda, el valor se rellena automáticamente con la zona horaria configurada para la cuenta de Search, Social y Commerce del anunciante una vez guardado el registro.

**Estado:** El estado de la cuenta en Search, Social y Commerce:

* *Habilitado:* Search, Social y Commerce sincronizan los datos de campaña con la cuenta (cuando es compatible) y envían ofertas automatizadas o presupuestos de campaña para las campañas en portafolios.
* *Deshabilitado:* Search, Social y Commerce detienen toda actividad en la cuenta. Los datos recopilados mientras la cuenta estaba activa se siguen almacenando, pero las vistas e informes de administración de campañas no incluyen datos del período de tiempo en el que la cuenta se pone en pausa. Posteriormente, puede volver a activar la cuenta para reanudar la actividad con la cuenta.

**Plantilla de seguimiento** - ([!DNL Google Ads], [!DNL Microsoft Advertising] y [!DNL Yahoo! Japan Ads] cuentas solamente; opcional) La plantilla de seguimiento predeterminada para la cuenta, que especifica todas las redirecciones de dominio de aterrizaje externo y parámetros de seguimiento y también incrusta la dirección URL de la página final/de aterrizaje en un parámetro. Ejemplo: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir una redirección.

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

**[!UICONTROL Master Account ID]:** (solo cuentas de [!DNL Microsoft Advertising]) Identificador de una cuenta de agencia/administración asociada a la cuenta.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] cuentas solamente; opcional) Una cuenta de agencia/administración asociada a la cuenta. Para quitar una asociación existente, seleccione &quot;[!UICONTROL No MCC Account]&quot;.

**[!UICONTROL Application ID]:** (solo cuentas de [!DNL Yandex]) El token de desarrollador que se usará para la cuenta. Se utiliza el mismo token para todas las cuentas de [!DNL Yandex].

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] cuentas con la configuración Cuenta compartida deshabilitada solamente; opcional) Identificador numérico de la campaña usado para pagar todas las campañas publicitarias de la cuenta.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] cuentas con la configuración Cuenta compartida deshabilitada solamente; opcional) El token de desarrollador que se usará para las llamadas de API relacionadas con las finanzas, como para reasignar dinero de la cartera entre las campañas del anunciante según sea necesario para la optimización del portafolio.

### Seguimiento de cuentas

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (solo para [!UICONTROL EF Redirect]) No implementado

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **Formato S_kwcid** - (Cuentas existentes de [!DNL Google Ads] para anunciantes con una integración Adobe Advertising-Adobe Analytics y para los cuales el ID de AMO (s_kwcid) aún no se ha migrado)

Esta cuenta utiliza el formato heredado para el código de seguimiento de ID de AMO, que permite que Adobe Advertising comparta datos sobre la cuenta con Adobe Analytics. El [formato más reciente](/help/integrations/analytics/ids.md#amo-id-formats) incluye parámetros para el identificador de campaña y el identificador de grupo de anuncios, los cuales son necesarios para informar con precisión en los niveles de campaña y grupo de anuncios para las campañas Máximo rendimiento de [!DNL Google Ads], así como borradores y experimentos, y campañas en Analytics:

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Si esta cuenta necesita generar informes en los niveles de campaña y de grupo de publicidad, haga clic en el icono [!UICONTROL Edit] (lápiz) y luego en **[!UICONTROL Migrate to new s_kwcid format]** para cambiar al nuevo formato. Para las cuentas que no incluyen estos tipos de campaña, la migración al nuevo formato es opcional pero se recomienda.

Para obtener instrucciones completas, consulte &quot;[Actualizar el código de seguimiento de ID de AMO para una [!DNL Google Ads] cuenta](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)&quot;.

**Nombres de grupos de informes** - (Para redireccionamiento de EF solo con token; anunciantes con integración de Adobe Advertising-Adobe Analytics; opcional) Uno o más grupos de informes de Analytics a los que Search, Social y Commerce envían datos que recopila de la red de anuncios, incluidas las clasificaciones de entidades y los datos de clics de la cuenta. Esta función solo está disponible para las redes de publicidad admitidas.

Para que los datos aparezcan en los grupos de informes, ya sea (a) la función de ID de AMO del lado del servidor debe estar configurada para la cuenta o (b) la configuración de nivel de anunciante a &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; debe estar habilitada. Además, la cuenta de Analytics del anunciante debe configurarse para recibir datos de Search, Social y Commerce. Para obtener más información, póngase en contacto con el administrador de cuentas de Adobe.

>[!MORELIKETHIS]
>
>* [Acerca de las cuentas de red de anuncios](ad-network-account-about.md)
>* [Administrar cuentas de centros comerciales](merchant-account-manage.md)
>* [Actualizar el código de seguimiento s_kwcid para una [!DNL Google Ads] cuenta](update-amo-id-google.md)
