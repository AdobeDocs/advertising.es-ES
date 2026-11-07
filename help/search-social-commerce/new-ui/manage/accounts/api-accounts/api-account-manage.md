---
title: (Nueva IU) Administrar las cuentas de red de publicidad
description: Obtenga información sobre cómo configurar y administrar los detalles de la cuenta en la nueva interfaz de usuario para una red de publicidad sincronizada mediante la API de red de publicidad.
feature: Search Campaign Management
exl-id: a50b2943-7568-401c-be5b-ff6f62629488
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: b568da9300e9adb8d189811c3c8b52516dfcef6f
workflow-type: tm+mt
source-wordcount: '3132'
ht-degree: 0%
---
# (Nueva IU) Administrar las cuentas de red de publicidad a través de la conexión API

Estas instrucciones explican cómo administrar las cuentas de red de publicidad que Search, Social y Commerce sincroniza mediante API, incluida la autenticación, la actualización de la conexión y las comprobaciones de estado.

Para crear, editar o volver a autenticar cuentas, debe tener permiso para editar cuentas.

Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Acerca de la vista [!UICONTROL Accounts] {#account-view-about}

La vista [!UICONTROL Manage] > [!UICONTROL Accounts] enumera todas las cuentas de red de anuncios en la vista filtrada para la cuenta de anunciante seleccionada. Haga clic en un nombre de cuenta para abrir la vista [!UICONTROL Campaigns] filtrada para esa cuenta.

### Autenticación de cuenta y estado de acceso {#authentication-status}

Los detalles de autenticación y acceso varían según la red de anuncios y la información disponible para la cuenta. Una cuenta habilitada o autenticada correctamente puede seguir teniendo permisos que faltan.

Las siguientes columnas muestran el estado de la cuenta, la autenticación y los detalles de acceso:

* **[!UICONTROL Status]:** Estado operativo de la cuenta, que es independiente de su autenticación y permisos. Una cuenta habilitada puede sincronizar datos con la red de anuncios y utilizar las funciones de optimización y administración de cuentas admitidas. Una cuenta deshabilitada detiene la actividad en Search, Social y Commerce. La visualización del estado de la cuenta usa un indicador verde para **[!UICONTROL Enabled]**, un indicador rojo para **[!UICONTROL Disabled]** y un indicador ámbar para **[!UICONTROL Pending]**. Puede [habilitar o deshabilitar cuentas](#enable-disable-account) desde la vista o la configuración de la cuenta.

* **[!UICONTROL Authenticated]:** Indica si la cuenta está autenticada:

  * **[!UICONTROL Yes]:** La cuenta está autenticada.

  * **[!UICONTROL No]:** La cuenta no está autenticada. Cuando haya un error de autenticación disponible, mantenga el cursor sobre el icono de advertencia rojo para ver el error.

  * **[!UICONTROL Not Applicable]:** La autenticación no se aplica porque se cargan datos para la cuenta en lugar de conectarse a través de una API.

  * **[!UICONTROL Expiring in N days]**, **[!UICONTROL Expiring today]** o **[!UICONTROL Expired]:** Una advertencia de caducidad de token reemplaza a **[!UICONTROL Yes]** cuando la información de caducidad está disponible y el token caduca en 14 días o menos, o bien ya ha caducado. Haga clic en el icono de advertencia para ver los detalles de acceso de la cuenta y [volver a autenticar](#reauthenticate).

* **[!UICONTROL Manager Account for Cross-Account Conversions]:** (solo cuentas de [!DNL Google Ads]) Identificador de la cuenta de administrador asociada que se usa para las cargas de conversión entre cuentas. Cuando hay un error disponible en la cuenta del administrador, aparece un icono de advertencia junto al ID. Para ver el error, mantenga el cursor sobre el icono. Las credenciales de la cuenta de administrador son independientes de las credenciales de la cuenta de red de publicidad. Para agregar o actualizar las credenciales de la cuenta del administrador, use **[!UICONTROL Setup]** > **[!UICONTROL Manager Accounts]**. Consulte &quot;[Administrar cuentas de administrador](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)&quot;.

* **[!UICONTROL Access Level]:** El nivel de acceso a la cuenta notificado, como **[!UICONTROL Full]**, **[!UICONTROL Limited]** o **[!UICONTROL None]**, o **[!UICONTROL Not Applicable]** cuando no hay disponible ningún valor de nivel de acceso.

  Cuando falten permisos, haga clic en el icono de advertencia para ver los detalles de acceso de la cuenta. La sección **[!UICONTROL Access]** enumera los permisos como **[!UICONTROL Granted]** o **[!UICONTROL Missing]**. Cuando los detalles de impacto están disponibles, la sección **[!UICONTROL Not working]** enumera la funcionalidad afectada. Para [volver a autenticar](#reauthenticate) y actualizar los permisos, haga clic en **[!UICONTROL Update Access]**.

### Acciones disponibles

Las acciones disponibles dependen de los permisos y del tipo de cuenta.

* [Crear y agregar detalles de cuenta de red](#create-account)

* [Editar los detalles de la cuenta de red del anuncio](#edit-account)

* [Volver a autenticar una cuenta de red de publicidad](#reauthenticate)

* [Habilitar o deshabilitar las cuentas de red de publicidad](#enable-disable-account)

* [Sincronizar datos de cuenta con la red de publicidad](sync-api-accounts.md)

* [Ver un gráfico de rendimiento en la vista [!UICONTROL Accounts]](#account-performance-graph)

* [Administrar informes de vista de datos desde la vista [!UICONTROL Accounts]](#account-reports)

## Crear y agregar detalles de cuenta de red {#create-account}

Para habilitar la sincronización de una cuenta, debe crear un registro de cuenta correspondiente que contenga las credenciales de acceso a la cuenta y las opciones de seguimiento y con el estado *habilitado*.

>[!NOTE]
>
>Para crear una cuenta real en la red de anuncios, vaya al sitio web de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Haga clic en **[!UICONTROL Create Account]**.

1. Haga clic en el nombre de la red publicitaria para abrir la configuración de la cuenta.

1. (Todas las redes de anuncios excepto [!DNL ChatGPT Ads] y [!DNL Yandex]) En la ficha **[!UICONTROL Authenticate]**, complete el inicio de sesión en la ventana emergente con las credenciales del anunciante y conceda acceso a la cuenta solicitada.

   La pantalla de configuración se actualiza automáticamente y muestra **[!UICONTROL Authentication Successful]** cuando la autenticación se realiza correctamente. Si necesita volver a abrir la ventana de inicio de sesión, haga clic en **[!UICONTROL Open login again]**. Si el explorador bloquea la ventana, edite la configuración del explorador para permitir ventanas emergentes para el sitio.

   Para [!DNL Meta Ads], una advertencia identifica los permisos que faltan y su impacto. Una autenticación correcta no significa necesariamente que se hayan concedido todos los permisos solicitados.

   Haga clic en **[!UICONTROL Next]** para continuar.

1. Especifique la [configuración de la cuenta](#account-settings-api) en cada ficha disponible. Para las cuentas autenticadas en una ventana emergente, seleccione la cuenta que desea sincronizar de **[!UICONTROL Linked Ad Accounts]** en la ficha **[!UICONTROL Select Accounts]**.

1. Haga clic en **[!UICONTROL Save]**.

   Los datos recientes de coste y clics de todas las campañas de la cuenta se actualizan cada hora en Search, Social y Commerce. De forma predeterminada, los datos están disponibles durante los últimos 5 a 10 días, según la red de publicidad. Sin embargo, si es necesario, el equipo de inicio del proyecto puede recuperar los datos durante los últimos 60 días.

## Editar los detalles de la cuenta de red del anuncio {#edit-account}

Para habilitar o deshabilitar la actividad en una cuenta, cambiar los parámetros de seguimiento predeterminados en una cuenta o cambiar los grupos de informes [!DNL Analytics] que se usan para el seguimiento y la creación de informes, edite los detalles de la cuenta. Para actualizar la conexión o los permisos de actualización, puede [volver a autenticar la cuenta](#reauthenticate) desde la configuración de la cuenta o desde la vista [!UICONTROL Accounts].

>[!NOTE]
>
>Para editar una cuenta real en la red de anuncios, vaya al sitio web de la red de anuncios.

1. En el menú principal, haga clic en **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Seleccione la cuenta de cualquiera de las siguientes maneras:

   * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

   * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

1. Edite la [configuración de la cuenta](#account-settings-api) en las fichas disponibles.

1. Haga clic en **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social y Commerce deben sincronizar los datos de la nueva cuenta con la de la red de anuncios. Esto sucede automáticamente una vez al día, o con mayor frecuencia cuando Search, Social y Commerce detectan cambios en la red de anuncios.

## Volver a autenticar una cuenta de red de publicidad {#reauthenticate}

*Para cuentas que utilizan autenticación emergente; no aplicable a [!DNL ChatGPT Ads] o [!DNL Yandex] cuentas*

Para actualizar la conexión de red de publicidad o los permisos de actualización de la cuenta, vuelva a autenticar la cuenta.

1. (Si ha iniciado sesión en otra cuenta para la misma red de anuncios en la misma aplicación de explorador) Cierre sesión en cualquier cuenta que no sea la del anunciante.

1. En el menú principal, haga clic en **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Abra la autenticación de una de las siguientes maneras:

   * (Cuando el valor **[!UICONTROL Authenticated]** de la cuenta sea **[!UICONTROL No]**) Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Re authenticate]**, cuando esté disponible.

   * (Cuando se muestre una advertencia de caducidad de token) Haga clic en el icono de advertencia de la columna **[!UICONTROL Authenticated]** y, a continuación, haga clic en **[!UICONTROL Reauthenticate]**.

   * (Cuando faltan permisos) Haga clic en el icono de advertencia de la columna **[!UICONTROL Access Level]** y, a continuación, haga clic en **[!UICONTROL Update Access]**.

   * (En la configuración de la cuenta) Seleccione la casilla de verificación situada junto al nombre de la cuenta y haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas, o mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**. En la ficha **[!UICONTROL Account Details]**, en **[!UICONTROL Account Authentication]**, haga clic en **[!UICONTROL Re authenticate]**.

1. Complete el inicio de sesión en la ventana emergente utilizando las credenciales del anunciante y conceda el acceso a la cuenta solicitada.

   El nuevo token de acceso se guarda automáticamente cuando la reautenticación se realiza correctamente. Si también cambia otras configuraciones de cuenta, haga clic en **[!UICONTROL Save]** para guardar los cambios.

   Para [!DNL Meta Ads], un mensaje de información identifica los permisos que faltan después de la reautenticación correcta. Para identificar la funcionalidad afectada, revise [detalles de acceso](#authentication-status).

## Habilitar o deshabilitar las cuentas de red de publicidad {#enable-disable-account}

Al habilitar una cuenta de red de publicidad, Search, Social y Commerce sincronizan los datos de campaña con la cuenta (cuando es compatible) y envían ofertas automatizadas o presupuestos de campaña para las campañas en portafolios. Cuando deshabilita una cuenta de red de publicidad, Search, Social y Commerce detienen toda la actividad en la cuenta. Los datos recopilados mientras la cuenta estaba activa se siguen almacenando, pero las vistas e informes de administración de campañas no incluyen datos del período de tiempo en el que la cuenta está deshabilitada. Más tarde puede volver a habilitar la cuenta para reanudar la actividad con la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Realice una de las acciones siguientes:

   * (Desde la vista [!UICONTROL Accounts]):

     * (Para habilitar la cuenta) Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Enable]** en la barra de herramientas de acciones en masa.

     * (Para deshabilitar la cuenta) Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Disable]** en la barra de herramientas de acciones en masa.

   * (Desde la configuración de la cuenta):

     1. Seleccione la cuenta de cualquiera de las siguientes maneras:

        * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

        * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

     1. En la ficha **[!UICONTROL Account Details]**, active **[!UICONTROL Account Enabled]** para habilitar la cuenta o desactívela para deshabilitarla.

     1. Haga clic en **[!UICONTROL Save]**.

## Ver un gráfico de rendimiento en la vista [!UICONTROL Accounts] {#account-performance-graph}

Abra y configure un gráfico de rendimiento con hasta tres métricas calculadas en total entre cuentas en la vista filtrada para el intervalo de fechas y la moneda especificados.

### Ver un gráfico de rendimiento

1. En el menú principal, haga clic en **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Especifique el intervalo de fechas y aplique los filtros necesarios para las cuentas cuyo rendimiento desee ver.

1. Sobre la tabla de datos, haga clic en ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

1. (Opcional) Use **[!UICONTROL Currency]** y **[!UICONTROL Metrics]** para especificar la moneda y hasta tres métricas que se incluirán en el gráfico.

### Ocultar un gráfico de rendimiento visible

* Sobre la tabla de datos, haga clic en ![Gráficos](/help/search-social-commerce/assets/charts.png "Gráficos").

## Administrar informes de vista de datos desde la vista [!UICONTROL Accounts] {#account-reports}

Genere un informe que incluya las filas de datos de una o varias cuentas en la vista [!UICONTROL Accounts] y, a continuación, descargue el informe como un archivo de hoja de cálculo de Microsoft Excel (formato XLSX). El informe incluye las columnas visibles en la vista para el intervalo de fechas especificado.

Puede eliminar los informes completados y los que no se hayan generado correctamente.

### Generación de un informe con las filas de datos filtradas

1. En el menú principal, haga clic en **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Especifique el intervalo de fechas y aplique los filtros para los datos que desee descargar.

1. Especifique las cuentas cuyos datos desee descargar:

   * Para descargar datos de cuentas específicas, active las casillas de verificación situadas junto a las cuentas.

   * Para descargar datos de todas las cuentas en la vista filtrada, deje todas las casillas de verificación desactivadas.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En el cuadro de diálogo [!UICONTROL Grid Reports], mantenga el valor predeterminado **[!UICONTROL Report Name]** o escriba otro nombre y, a continuación, haga clic en **[!UICONTROL Generate]**.

   El informe se agrega a la lista **[!UICONTROL Recently Generated]**.

1. (Opcional) Para descargar el archivo una vez que se haya completado, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Descargar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista **[!UICONTROL Recently Generated]** del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Eliminación de un informe

1. En el menú principal, haga clic en **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista **[!UICONTROL Recently Generated]** del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar") junto al nombre de un informe completado o uno que no se haya generado.

1. Confirme la eliminación.

## Configuración de cuenta de red de anuncios {#account-settings-api}

La configuración de la cuenta varía según la red de anuncios. Es posible que no vea todas las configuraciones a continuación.

### Ficha [!UICONTROL Authenticate]

(Visible mientras crea una cuenta que utiliza la autenticación emergente) Conéctese a la red de publicidad con las credenciales del anunciante. La pestaña muestra el estado de la conexión e incluye **[!UICONTROL Open login again]** para volver a abrir la ventana emergente de inicio de sesión.

### Ficha [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Nombre que se mostrará para la cuenta en Search, Social y Commerce.

>[!NOTE]
>
>Si tiene una integración de Search, Social y Commerce-Adobe Analytics y cambia el nombre de la cuenta de búsqueda, pida al equipo de cuenta de Adobe que actualice la asignación.

**[!UICONTROL Linked Ad Accounts]:** (visible mientras crea una cuenta que usa autenticación emergente) La cuenta de red de anuncios que se va a sincronizar. Elija entre las cuentas de publicidad vinculadas a su inicio de sesión en la red.

**[Detalles de inicio de sesión]:** ([!DNL Yandex] cuentas solamente) Las credenciales de la cuenta que se van a usar:

* **[!UICONTROL Login]:** El nombre o ID de inicio de sesión para habilitar el acceso de API a la cuenta.

* **[!UICONTROL Password]:** Contraseña de la cuenta.

* **[!UICONTROL Access Key]:** Clave de acceso para la cuenta de desarrollador que se va a usar.

* **[!UICONTROL Application ID]:** El token de desarrollador que se va a usar para la cuenta. Se utiliza el mismo token para todas las cuentas de [!DNL Yandex].

* **[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] cuentas con la configuración Cuenta compartida deshabilitada solamente; opcional) Identificador numérico de la campaña usado para pagar todas las campañas publicitarias de la cuenta.

* **[!UICONTROL Finance Token]:** ([!DNL Yandex] cuentas con la configuración Cuenta compartida deshabilitada solamente; opcional) El token de desarrollador para llamadas de API relacionadas con las finanzas, como la reasignación de dinero entre campañas de anunciantes para la optimización del portafolio.

**[!UICONTROL Currency]:** (solo lectura) La abreviatura de la moneda utilizada para la cuenta. Este valor se rellena automáticamente con la moneda configurada para la cuenta en la red de publicidad una vez guardado el registro.

**[!UICONTROL Time Zone]:** Zona horaria del anunciante. Este valor se rellena automáticamente con la zona horaria configurada para la cuenta de Search, Social y Commerce del anunciante una vez guardado el registro.

**[!UICONTROL Login]:** (solo lectura) Cuenta de usuario utilizada para iniciar sesión en la cuenta.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social y Commerce sincronizan los datos de campaña con la cuenta (cuando es compatible) y envían ofertas automatizadas o presupuestos de campaña para campañas en portafolios.

**[!UICONTROL Account Authentication]> [!UICONTROL Re authenticate]:** (visible mientras edita una cuenta que usa autenticación emergente) Actualiza la conexión o actualiza los permisos de la cuenta. El nuevo token de acceso se guarda automáticamente cuando la reautenticación se realiza correctamente.

## Ficha [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** Si se habilita o no el seguimiento mediante el servicio de seguimiento de conversión de Adobe Advertising. Este método genera ID únicos de seguimiento de clics y redirige a los usuarios al servidor de Adobe Advertising con fines de seguimiento antes de enviarlos a la página de aterrizaje del cliente. Este método tiene opciones de seguimiento predeterminadas que se pueden personalizar de forma opcional y también se pueden especificar parámetros para anexar a cada dirección URL.

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

**[!UICONTROL Auto Update]:** (cuando el seguimiento de Search, Social y Commerce está habilitado) Estandariza las direcciones URL de seguimiento para comprobar la compatibilidad entre exploradores y servidores. Search, Social y Commerce cargan automáticamente lo siguiente en la red de anuncios durante la siguiente sincronización: (a) parámetros de seguimiento de Search, Social y Commerce para plantillas de seguimiento y los mismos parámetros añadidos a las direcciones URL finales o (b) nuevas direcciones URL de destino incrustadas con el código de seguimiento de Search, Social y Commerce. Para anunciantes con una [integración Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=es) y una configuración de ID de AMO del lado del servidor (s_kwcid), la carga también incluye [parámetros de ID de AMO](/help/integrations/analytics/ids.md#amo-id) para sus cuentas de [!DNL Google Ads] y [!DNL Microsoft Advertising]. La configuración predeterminada en el nivel de cuenta se hereda de la configuración de seguimiento del anunciante. Puede anular la configuración de nivel de cuenta en el nivel de campaña.

Las direcciones URL de seguimiento se actualizan a diario solo para las entidades que no están sincronizadas (es decir, las nuevas entidades que se añadieron y las entidades existentes cuyas propiedades han cambiado). Por lo tanto, si cambia esta configuración de deshabilitada a habilitada para un anunciante, cuenta o campaña existente, las direcciones URL de seguimiento no se actualizan para las entidades existentes que ya están sincronizadas. Para agregar el seguimiento a las direcciones URL de entidades sincronizadas existentes, póngase en contacto con el equipo de cuenta de Adobe y solicite un proceso de sincronización manual único. El proceso de carga automática gestiona los cambios futuros.

**[!UICONTROL URL Encoding]:** (cuando el seguimiento de Search, Social y Commerce está habilitado; solo cuentas con direcciones URL de destino) Codifica la dirección URL base en la barra de direcciones del explorador del usuario final (como `%3D` en lugar de `=`):

**[!UICONTROL Tracking Level]:** (cuando el seguimiento de Search, Social y Commerce está habilitado; disponible en los niveles de cuenta y campaña; no aplicable a las redes de anuncios habilitadas para el seguimiento paralelo) Nivel en el que se rastrean los clics y los ingresos agregando una redirección y adjuntando parámetros a las direcciones URL relevantes:

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

**URL de seguimiento de cuenta**: ([!DNL Google Ads], [!DNL LY Ads] y [!DNL Microsoft Advertising] cuentas solamente; opcional) La plantilla de seguimiento predeterminada de la cuenta, que especifica todas las redirecciones de dominios de aterrizaje y parámetros de seguimiento, e incrusta también la dirección URL final de la página de aterrizaje en un parámetro. Ejemplo: `{lpurl}?source={network}&id=5` o `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` para incluir una redirección.

* Para incrustar la dirección URL final:

  * ([!DNL Google Ads] y [!DNL Microsoft Advertising] solamente) Para obtener una lista de parámetros que indiquen las direcciones URL finales en las plantillas de seguimiento, vea la ([!DNL Microsoft Advertising] solamente) [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/3/en/56799) o ([!DNL Google Ads] solamente) los parámetros &quot;Solo plantilla de seguimiento&quot; en la sección &quot;Parámetros disponibles [!DNL ValueTrack]&quot; en la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/6305348).

  * ([!DNL LY Ads] solamente) Use el parámetro `!{lpurl}` para indicar la dirección URL de la página de aterrizaje.

* Si lo desea, puede incluir parámetros de URL y cualquier parámetro personalizado definido para la campaña, separados por el símbolo &quot;et&quot; (&amp;), como `{lpurl}?matchtype={matchtype}&device={device}`.

* Si lo desea, puede añadir redirecciones y seguimiento de terceros.

* Cuando la configuración de la campaña incluye &quot;[!UICONTROL EF Redirect]&quot; y &quot;[!UICONTROL Auto Upload]&quot;, Search, Social y Commerce añadirán automáticamente como prefijo su propio código de redirección y seguimiento al guardar el registro.

>[!NOTE]
>
>* Para [!DNL Google Ads], evite utilizar macros que no sustituyan los clics de fuentes que habilitan el seguimiento paralelo. Si el anunciante debe utilizar macros, el equipo de cuenta de Adobe colabora con el servicio de atención al cliente o con el equipo de implementación para agregarlas.
>* La plantilla de seguimiento en el nivel más granular anula los valores en todos los niveles superiores. Por ejemplo, si tanto la configuración de la cuenta como la configuración de la palabra clave incluyen un valor, se aplica el valor de la palabra clave.
>* Si actualiza una plantilla de seguimiento en el nivel de anuncio, vínculo de sitio o palabra clave, los anuncios relevantes se vuelven a enviar para su revisión. Puede actualizar las plantillas de seguimiento en los niveles de cuenta, campaña o grupo de publicidad sin volver a enviar los anuncios para su aprobación.

## Ficha [!UICONTROL Set up Adobe Analytics]

Esta configuración está disponible para anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md).

**[!UICONTROL Adobe Analytics Report Suite]:** (opcional) uno o más grupos de informes de Analytics a los que Search, Social y Commerce envían los datos que recopila de la red de publicidad, incluidas las clasificaciones de entidades y los datos de clics de la cuenta. Esta característica solo está disponible para las redes de publicidad admitidas.<!-- What are the repercussions of changing the suites? Timing of updated data? -->

Para que los datos aparezcan en los grupos de informes, ya sea (a) la función de ID de AMO del lado del servidor debe estar configurada para la cuenta o (b) la configuración de nivel de anunciante a &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; debe estar habilitada. Además, la cuenta del anunciante [!DNL Analytics] debe estar configurada para recibir datos de Search, Social y Commerce. Para obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

**[!UICONTROL Adobe Analytics Conversion Reporting]: [!UICONTROL Enable conversion reporting in Adobe Analytics]:** ([!DNL Meta Ads] cuentas; opcional) Anexa el parámetro de seguimiento [AMO ID (s_kwcid)](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md) a todos los anuncios de la campaña. El parámetro permite a Adobe Analytics asociar conversiones con campañas de Meta Ads en el grupo de informes especificado, junto con las clasificaciones de entidades y los datos de clics.

>[!MORELIKETHIS]
>
>* [Acerca de las cuentas de red de anuncios](../ad-network-account-about.md)
>* [Administrar cuentas de centros comerciales](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)
>* [Actualizar el código de seguimiento s_kwcid para una [!DNL Google Ads] cuenta](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
