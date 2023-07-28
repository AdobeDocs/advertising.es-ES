---
title: Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes
description: Obtenga información sobre cómo crear y editar [!DNL Google Ads] y [!DNL Microsoft® Advertising] audiencias de coincidencia de clientes de sus listas de datos de clientes.
exl-id: 734d8cb1-3915-410f-a0cc-0669d6575eab
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# Administrar [!DNL Google Ads] y [!DNL Microsoft® Advertising] audiencias de coincidencia de clientes que usan listas de datos de clientes

Puede crear [!DNL Google Ads] y [!DNL Microsoft® Advertising] audiencias de coincidencia de clientes de sus listas de datos de clientes. También puede actualizar cualquier [!DNL Google Ads] o [!DNL Microsoft® Advertising] audiencia de coincidencia de clientes excepto para [!DNL Google Ads] audiencias creadas a partir de un [!DNL Adobe] audiencia.

## Crear una audiencia afín de clientes a partir de una lista de datos de clientes

*[!DNL Google Ads]y [!DNL Microsoft® Advertising] cuentas elegibles solo para la confrontación con clientes*

Puede crear un [!DNL Google Ads] o [!DNL Microsoft® Advertising] lista basada en datos de cliente a partir de un archivo de datos que genere desde su sistema de administración de la relación con los clientes (CRM).

Para [!DNL Microsoft® Advertising] cuentas, el archivo puede incluir direcciones de correo electrónico. Para [!DNL Google Ads] En el caso de las cuentas de, el archivo puede incluir direcciones de correo electrónico, direcciones de correo o números de teléfono; ID de usuario o ID de dispositivo móvil de su CRM.

>[!NOTE]
>
>Search, Social y Commerce no almacenan ninguno de los datos de clientes que carga o del [!DNL Adobe] segmentos utilizados para crear o editar un [!DNL Google Ads] o [!DNL Microsoft® Advertising] audiencia.

1. Genere un archivo con los datos del cliente en el formato requerido.

   El nombre y los apellidos, las direcciones de correo electrónico y los números de teléfono deben tener un cifrado hash con el algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Para [!DNL Google Ads] audiencias, consulte las [!DNL Google Ads] documentación sobre &quot;[Directrices de formato para cargar datos con hash](https://support.google.com/google-ads/answer/7476159)&quot; para obtener una lista de los campos y requisitos de información de contacto permitidos. Para [!DNL Microsoft® Advertising] audiencias, consulte las [!DNL Microsoft® Advertising] documentación sobre [preparación de listas de coincidencia de clientes](https://help.ads.microsoft.com/#apex/ads/en/56921. Si lo desea, puede descargar un [!DNL Microsoft® Excel] plantilla para información de contacto.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Especifique la información de la audiencia:

   1. En el [!UICONTROL Data Source] menú, seleccione **[!UICONTROL Customer List]**.

   1. Introduzca el **[!UICONTROL Audience Name]**.

   1. Cargue el archivo:

      1. Seleccione el [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]*, o *[!UICONTROL Mobile Device IDs]*.

         La opción ID de usuario solo está disponible para [!DNL Google Ads] anunciantes en los EE. UU. que han elegido participar en [segmentos de ID de usuario](https://support.google.com/google-ads/answer/9199250)

      1. (Solo listas de ID de dispositivos móviles) Seleccione la variable **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* o *[!UICONTROL iOS]*) e introduzca la **[!UICONTROL App ID]**.

         El ID de aplicación es un identificador único que el sistema operativo del dispositivo móvil utiliza para permitir que la aplicación se conecte a Google Play o a Apple App Store:

         * ([!DNL Android™] apps) El [!DNL Android™] nombre del paquete en [!DNL Google Play], identificado por &quot;`id=<package_name>`.&quot;

           Por ejemplo, en https://play.google.com/store/apps/details?id=com.example.game, el nombre del paquete es com.example.game.

         * ([!DNL iOS] apps) El ID de aplicación dentro de la [!DNL iTunes App Store], identificado por &quot;`<idNNNNNNNNN>`&quot; al final de la dirección URL. También está disponible en el [!DNL iOS Developer Console].

           Por ejemplo, en https://itunes.apple.com/us/app/id284882215, el ID es id284882215.

         Su equipo de desarrollo tiene acceso a [!UICONTROL App ID] para la plataforma correspondiente.

      1. En el [!UICONTROL Select File] , haga clic en **[!UICONTROL Choose File]** y seleccione el archivo en la red o dispositivo.

      1. Active la casilla de verificación para indicar que está de acuerdo con los términos del [!DNL Adobe] y políticas de privacidad de la red publicitaria.

      1. Haga clic **[!UICONTROL Upload File]**.

   1. Especifique el número de **[!UICONTROL Membership Days]**, que es el número de días que la cookie de un usuario permanece en la audiencia.

   Utilice el periodo de tiempo durante el cual espera que el anuncio sea relevante para el usuario. Las listas de clientes no caducan a menos que escriba un valor.

1. Haga clic **[!UICONTROL Post]**.

>[!NOTE]
>
>* La red de anuncios puede tardar hasta 24 horas en procesar el archivo.
>* Consulte [[!DNL Google Ads] documentación sobre cómo funciona la coincidencia de clientes y limitaciones](https://support.google.com/displayvideo/answer/9539301).

## Edición de una audiencia afín de clientes mediante una lista de datos de clientes

Puede actualizar cualquier [!DNL Google Ads] o [!DNL Microsoft® Advertising] audiencia de coincidencia de clientes excepto para [!DNL Google Ads] audiencias creadas a partir de un [!DNL Adobe] audiencia. Puede cargar datos para agregar, eliminar o reemplazar todos los datos existentes de la audiencia.

Los datos deben ser del mismo tipo que la lista de clientes original (direcciones de correo electrónico, direcciones de correo electrónico, números de teléfono, ID de usuario o ID de dispositivo móvil para una aplicación específica en un sistema operativo móvil específico).

1. Genere un archivo con los datos del cliente en el formato requerido para el tipo de datos existente.

El nombre y los apellidos, las direcciones de correo electrónico y los números de teléfono deben tener un cifrado hash con el algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Para [!DNL Google Ads] audiencias, consulte las [!DNL Google Ads] documentación sobre &quot;[Directrices de formato para cargar datos con hash](https://support.google.com/google-ads/answer/7476159)&quot; para obtener una lista de los campos y requisitos de información de contacto permitidos. Para [!DNL Microsoft® Advertising] audiencias, consulte las [!DNL Microsoft® Advertising] documentación sobre [preparación de listas de coincidencia de clientes](https://help.ads.microsoft.com/#apex/ads/en/56921. Si lo desea, puede descargar un [!DNL Microsoft® Excel] plantilla para información de contacto.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Seleccione la casilla de verificación situada junto a la audiencia que desea editar.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png).

1. Seleccione la acción: *[!UICONTROL Add]* (para añadir los datos cargados a los datos existentes, a menos que ya exista), *[!UICONTROL Delete]* (para eliminar los datos cargados de los datos existentes, cuando ya existen), o *[!UICONTROL Replace]* (para eliminar todos los datos existentes y sustituirlos por los datos cargados).

1. Cargue el archivo:

   1. En el [!UICONTROL Select File] , haga clic en **[!UICONTROL Choose File]** y seleccione el archivo en la red o dispositivo.

   1. Active la casilla de verificación para indicar que está de acuerdo con los términos del [!DNL Adobe] y políticas de privacidad de la red publicitaria.

   1. Haga clic **[!UICONTROL Upload File]**.

1. Haga clic **[!UICONTROL Post]**.

>[!NOTE]
>
>La red de anuncios puede tardar un tiempo en procesar las actualizaciones para una audiencia.

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Crear [!DNL Google Ads] audiencias de coincidencia de cliente de [!DNL Adobe] audiencias](google-audience-from-adobe-audience.md)
>* [Crear un [!DNL Google Ads] audiencia de customer match de una lista de correo electrónico de Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Administración de audiencias de remarketing dinámico](audience-dynamic-remarketing-manage.md)
