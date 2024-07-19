---
title: Administrar cuentas de comerciante
description: Obtenga información sobre cómo configurar y administrar los detalles de la cuenta de un centro de comerciantes.
exl-id: 7d940e45-ea49-470b-98d0-0196593228cb
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 0%

---

# Administrar cuentas de comerciante

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Search, Social y Commerce pueden descargar y mostrar datos de productos todos los días para cualquiera de las cuentas de Google Merchant Center o Microsoft Merchant Center de un anunciante. Además, Search, Social y Commerce pueden automatizar la creación de anuncios en función del contenido de la cuenta de comerciante. Para trabajar directamente con los datos del producto en Search, Social y Commerce, debe crear un registro de cuenta correspondiente que contenga las credenciales de acceso a la cuenta y con acceso *habilitado*.

>[!NOTE]
>
>No se puede quitar un registro de cuenta de comerciante. Puede deshabilitar el acceso a una cuenta cambiando el tipo de cuenta a *deshabilitada*.

## Crear detalles de cuenta de comerciante {#create-merchant-account}

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Para ver los datos del producto y generar plantillas de seguimiento para una cuenta de comerciante, y para crear anuncios basados en los datos, debe crear un registro de cuenta correspondiente que contenga las credenciales de acceso a la cuenta y con acceso a la cuenta *habilitada*.

>[!NOTE]
>
>Para crear una cuenta real en la red de comerciantes, vaya al sitio web de la red.

1. En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]**, que se abre en la ficha [!UICONTROL Accounts].

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Create Account]**.

1. Especifique la [configuración de la cuenta comercial](#merchant-account-settings):

   1. En el menú [!UICONTROL Product Source], seleccione el centro de comerciantes.

   <!--

   1. ([!DNL Meta Ads] accounts only) Log in to the [!DNL Meta Ads] account.

   And are there additional steps just for Meta? If so, create a separate procedure for it.
   
   -->

   1. (Necesario para cuentas de [!DNL Google Ads]; opcional para cuentas de [!DNL Microsoft Advertising]) Permitir que Search, Social y Commerce accedan a la cuenta mediante el [[!DNL OAuth] protocolo de autorización](https://oauth.net/2/):

      1. ([!DNL Microsoft Advertising] solo cuentas) Seleccione **[!UICONTROL oAuth]**.

      1. Haga clic en **[!UICONTROL Enable Connection]**.

      1. (Si no ha iniciado sesión en la cuenta del anunciante) Inicie sesión en la cuenta del anunciante. Una práctica recomendada es utilizar las credenciales para el acceso de la API de contenido a la cuenta del centro de comerciantes.

      1. En la pantalla de solicitud de acceso/permiso, haga clic en el botón para confirmar el permiso.

      1. Copie la cadena de autenticación en la ventana emergente que se abre y péguela en el campo **[!UICONTROL oAuth Token]**.

      1. Especifique el resto de configuraciones de la cuenta.

1. Haga clic en **[!UICONTROL Save]**.

   Los datos de atributos de todos los productos de la cuenta están disponibles en Search, Social y Commerce después del siguiente proceso de sincronización diario (sobre las 06:00 en la zona horaria local del usuario). A continuación, puede utilizar los datos del producto para automatizar la creación de anuncios mediante fuentes de inventario.

## Editar detalles de la cuenta de comerciante {#edit-merchant-account}

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Si las credenciales de la cuenta cambian o desea dejar de recuperar y utilizar datos de una cuenta de comerciante, edite los detalles de la cuenta.

>[!NOTE]
>
>Para editar una cuenta real en la red de comerciantes, vaya al sitio web de la red.

1. En el menú principal, haga clic en **[!UICONTROL Search]\> [!UICONTROL Campaigns] \>[!UICONTROL Products]**, que se abre en la ficha [!UICONTROL Accounts].

1. Junto al nombre de la cuenta, haga clic en ![Ver/editar configuración](/help/search-social-commerce/assets/settings.png "Ver/editar configuración").

1. Editar la [configuración de la cuenta de comerciante](#merchant-account-settings).

1. Haga clic en **[!UICONTROL Save]**.

>[!NOTE]
>
>Search, Social y Commerce deben sincronizar los datos de la nueva cuenta con la de la red de comerciantes. Esto sucede automáticamente una vez al día, aproximadamente a las 06:00 en la zona horaria local del usuario.

## Deshabilitar el acceso a una cuenta de comerciante {#disable-merchant-account}

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Al deshabilitar una cuenta de comerciante, Search, Social y Commerce no inician sesión en la cuenta y, por lo tanto, no recuperan los datos actualizados del producto. Los datos recopilados mientras la cuenta estaba habilitada se seguirán almacenando y los anuncios existentes creados con datos de productos no se actualizarán, pausarán ni eliminarán según la plantilla de fuente y la configuración de los datos de fuente.

1. En el menú principal, haga clic en **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Products]** , que se abre en la ficha [!UICONTROL Accounts].

1. Junto al nombre de la cuenta, haga clic en ![Ver/editar configuración](/help/search-social-commerce/assets/settings.png "Ver/editar configuración").

1. Cambie [!UICONTROL EF Account Type] a **[!UICONTROL Disabled]**.

1. Haga clic en **[!UICONTROL Save]**.

## Configuración de cuenta de comerciante {#merchant-account-settings}

>[!NOTE]
>
>Solo el administrador de cuentas de agencia, el administrador de cuentas [!DNL Adobe] y los roles de usuario administrador pueden establecer la configuración de la cuenta de comerciante.

**[!UICONTROL Product Source]:** La red de comerciantes. No puede cambiar el valor de una cuenta existente.

**[!UICONTROL OAuth Token]:** ([!DNL Google Merchant Center] cuentas solamente) El token de la cuenta para autorizar inicios de sesión mediante el [[!DNL OAuth] protocolo de autorización](https://oauth.net/2/).

**[!UICONTROL Auth Type]:** ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] solamente) Si se autorizarán los inicios de sesión en la cuenta mediante:

* *[!UICONTROL Client login]:* Para usar el inicio de sesión del cliente.

* *[!UICONTROL oAuth]* (valor predeterminado): para usar el [[!DNL OAuth] protocolo de autorización](https://oauth.net/2/).

**[!UICONTROL Access Key]:** ([!DNL Microsoft Merchant Center] solamente) La clave de acceso que debe usar la cuenta de desarrollador.

**[!UICONTROL Account Name]:** Nombre mostrado para la cuenta en Search, Social y Commerce.

**[!UICONTROL Login]:** El nombre o identificador de inicio de sesión de la cuenta.

**[!UICONTROL Password]:** Contraseña de la cuenta.

**[!UICONTROL Confirm Password]:** Contraseña de la cuenta.

**[!UICONTROL EF Account Type]:** Si Search, Social y Commerce tienen acceso a la cuenta:

* *[!UICONTROL Enabled]* (predeterminado): Search, Social y Commerce pueden iniciar sesión en la cuenta para recuperar los datos del producto.

* *[!UICONTROL Disabled]:* Search, Social y Commerce no inician sesión en la cuenta y, por lo tanto, no recuperan los datos actualizados del producto. Los datos recopilados mientras la cuenta estaba habilitada se seguirán almacenando y los anuncios existentes creados con datos de productos no se actualizarán, pausarán ni eliminarán según la plantilla de fuente y la configuración de los datos de fuente.

**[!UICONTROL Account ID]:** El identificador de la cuenta de comerciante. Si solo tiene una cuenta con la información de inicio de sesión especificada, este valor es opcional.

**[!UICONTROL Time Zone]:** Zona horaria del anunciante. Utilice la misma zona horaria configurada para la información de cuenta de Search, Social y Commerce del anunciante (que se establece al crear la cuenta). No puede cambiar el valor de una cuenta existente.

>[!MORELIKETHIS]
>
>* [Acerca de las cuentas de red de anuncios](ad-network-account-about.md)
>* [Administrar cuentas de red de anuncios](ad-network-account-manage.md)
