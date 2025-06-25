---
title: Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes
description: Aprenda a crear y editar audiencias de coincidencia de clientes de  [!DNL Google Ads] y [!DNL Microsoft Advertising] a partir de sus listas de datos de clientes.
exl-id: 594a7ee0-4ac9-4970-b53e-d4624fd7b70c
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Administrar audiencias de coincidencia de clientes [!DNL Google Ads] y [!DNL Microsoft Advertising] mediante listas de datos de clientes

Puede crear audiencias de coincidencia de clientes de [!DNL Google Ads] y [!DNL Microsoft Advertising] a partir de sus listas de datos de clientes. También puede actualizar cualquier audiencia afín de clientes [!DNL Google Ads] o [!DNL Microsoft Advertising], excepto [!DNL Google Ads] audiencias creadas a partir de una audiencia [!DNL Adobe].

## Crear una audiencia afín de clientes a partir de una lista de datos de clientes

*[!DNL Google Ads]y [!DNL Microsoft Advertising] cuentas elegibles para la coincidencia de clientes solamente*

Puede crear una lista basada en datos de clientes de [!DNL Google Ads] o [!DNL Microsoft Advertising] a partir de un archivo de datos que genere desde el sistema de administración de la relación con los clientes (CRM).

Para cuentas de [!DNL Microsoft Advertising], el archivo puede incluir direcciones de correo electrónico. Para cuentas de [!DNL Google Ads], el archivo puede incluir direcciones de correo electrónico, direcciones de correo o números de teléfono; ID de usuario o ID de dispositivos móviles de su CRM.

>[!NOTE]
>
>Search, Social y Commerce no almacenan ninguno de los datos de clientes que subió o de los segmentos de [!DNL Adobe] utilizados para crear o editar una audiencia de [!DNL Google Ads] o [!DNL Microsoft Advertising].

1. Genere un archivo con los datos del cliente en el formato requerido.

   El nombre y los apellidos, las direcciones de correo electrónico y los números de teléfono deben tener un cifrado hash con el algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Para audiencias de [!DNL Google Ads], consulte la documentación de [!DNL Google Ads] en &quot;[Directrices de formato para cargar datos con hash](https://support.google.com/google-ads/answer/7476159)&quot; para obtener una lista de los campos y requisitos de información de contacto permitidos. Para audiencias de [!DNL Microsoft Advertising], consulte la documentación de [!DNL Microsoft Advertising] sobre [preparación de listas de coincidencia de clientes](https://help.ads.microsoft.com/#apex/ads/en/56921). Si lo desea, puede descargar una plantilla [!DNL Microsoft Excel] para obtener información de contacto.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Especifique la información de la audiencia:

   1. En el menú [!UICONTROL Data Source], seleccione **[!UICONTROL Customer List]**.

   1. Escriba **[!UICONTROL Audience Name]**.

   1. Cargue el archivo:

      1. Seleccione [!UICONTROL Data Upload Type]: *[!UICONTROL Emails, Phones, and/or Mailing Addresses]*, *[!UICONTROL User IDs]* o *[!UICONTROL Mobile Device IDs]*.

         La opción ID de usuario solo está disponible para [!DNL Google Ads] anunciantes de EE. UU. que hayan elegido [segmentos de ID de usuario](https://support.google.com/google-ads/answer/9199250)

      1. (Solo listas de ID de dispositivos móviles) Seleccione **[!UICONTROL OS Type]** (*[!UICONTROL Android™]* o *[!UICONTROL iOS]*) e introduzca **[!UICONTROL App ID]**.

         El ID de aplicación es un identificador único que el sistema operativo del dispositivo móvil utiliza para permitir que la aplicación se conecte a Google Play o a Apple App Store:

         * ([!DNL Android™] aplicaciones) El nombre del paquete [!DNL Android™] en [!DNL Google Play], identificado por &quot;`id=<package_name>`&quot;.

           Por ejemplo, en `https://play.google.com/store/apps/details?id=com.example.game`, el nombre del paquete es com.example.game.

         * ([!DNL iOS] aplicaciones) El id. de aplicación dentro de [!DNL iTunes App Store], identificado por &quot;`<idNNNNNNNNN>`&quot; al final de la dirección URL. También está disponible en el [!DNL iOS Developer Console].

           Por ejemplo, en `https://itunes.apple.com/us/app/id284882215`, el identificador es id284882215.

         Su equipo de desarrollo tiene acceso a [!UICONTROL App ID] para la plataforma correspondiente.

      1. En el campo [!UICONTROL Select File], haga clic en **[!UICONTROL Choose File]** y seleccione el archivo en su red o dispositivo.

      1. Active la casilla de verificación para indicar que está de acuerdo con los términos de [!DNL Adobe] y las directivas de privacidad de red de anuncios.

      1. (Anunciantes que crean audiencias de [!DNL Google Ads] que hacen negocios en el Espacio Económico Europeo (EEE) o en el Reino Unido (Reino Unido); opcional) Si ha recopilado el consentimiento de usuarios de EEE y Reino Unido para cargar sus datos con fines publicitarios, active la casilla de verificación situada junto a **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

      [!DNL Google Ads] ignora los datos de los usuarios del EEE y del Reino Unido con un estado de consentimiento no especificado. Esto puede provocar discrepancias en los datos y problemas de rendimiento.

      1. Haga clic en **[!UICONTROL Upload File]**.

   1. Especifique el número de **[!UICONTROL Membership Days]**, que es el número de días que la cookie de un usuario permanece en la audiencia.

   Utilice el periodo de tiempo durante el cual espera que el anuncio sea relevante para el usuario. Las listas de clientes no caducan a menos que escriba un valor.

1. Haga clic en **[!UICONTROL Post]**.

>[!NOTE]
>
>* La red de anuncios puede tardar hasta 24 horas en procesar el archivo.
>* Ver [[!DNL Google Ads] documentación sobre cómo funciona la coincidencia de clientes y las limitaciones](https://support.google.com/displayvideo/answer/9539301).

## Edición de una audiencia afín de clientes mediante una lista de datos de clientes

Puede actualizar cualquier audiencia de coincidencia de cliente [!DNL Google Ads] o [!DNL Microsoft Advertising], excepto [!DNL Google Ads] audiencias creadas a partir de una audiencia [!DNL Adobe]. Puede cargar datos para agregar, eliminar o reemplazar todos los datos existentes de la audiencia.

Los datos deben ser del mismo tipo que la lista de clientes original (direcciones de correo electrónico, direcciones de correo electrónico, números de teléfono, ID de usuario o ID de dispositivo móvil para una aplicación específica en un sistema operativo móvil específico).

1. Genere un archivo con los datos del cliente en el formato requerido para el tipo de datos existente.

El nombre y los apellidos, las direcciones de correo electrónico y los números de teléfono deben tener un cifrado hash con el algoritmo SHA-256. <!-- Our UI says all, but GGL docs say don't hash user IDs and device IDs. --> Para audiencias de [!DNL Google Ads], consulte la documentación de [!DNL Google Ads] en &quot;[Directrices de formato para cargar datos con hash](https://support.google.com/google-ads/answer/7476159)&quot; para obtener una lista de los campos y requisitos de información de contacto permitidos. Para audiencias de [!DNL Microsoft Advertising], consulte la documentación de [!DNL Microsoft Advertising] en [preparación de listas de coincidencia de clientes]&#x200B;(https://help.ads.microsoft.com/#apex/ads/en/56921. Si lo desea, puede descargar una plantilla [!DNL Microsoft Excel] para obtener información de contacto.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. Seleccione la casilla de verificación situada junto a la audiencia que desea editar.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png).

1. Seleccione la acción: *[!UICONTROL Add]* (para agregar los datos cargados a los datos existentes, a menos que ya existan), *[!UICONTROL Delete]* (para eliminar los datos cargados de los datos existentes, cuando ya existan), o *[!UICONTROL Replace]* (para eliminar todos los datos existentes y reemplazarlos con los datos cargados).

1. Cargue el archivo:

   1. En el campo [!UICONTROL Select File], haga clic en **[!UICONTROL Choose File]** y seleccione el archivo en su red o dispositivo.

   1. Active la casilla de verificación para indicar que está de acuerdo con los términos de [!DNL Adobe] y las directivas de privacidad de red de anuncios.

   1. Haga clic en **[!UICONTROL Upload File]**.

1. Haga clic en **[!UICONTROL Post]**.

>[!NOTE]
>
>La red de anuncios puede tardar un tiempo en procesar las actualizaciones para una audiencia.

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias](google-audience-from-adobe-audience.md)
>* [Crear una audiencia de  [!DNL Google Ads] customer match a partir de una lista de correo electrónico de Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Administrar audiencias de remarketing dinámico](audience-dynamic-remarketing-manage.md)
