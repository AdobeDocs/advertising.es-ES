---
title: Crear [!DNL Google Ads] audiencias de coincidencia de cliente de [!DNL Adobe] audiencias
description: Aprenda a crear [!DNL Google Ads] audiencias de coincidencia de clientes de las audiencias de Adobe Analytics y Audience Manager existentes.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# Crear [!DNL Google Ads] audiencias de customer match de audiencias de Adobe Analytics y audiencias de Audience Manager

*[!DNL Google Ads]cuentas elegibles solo para la confrontación con clientes*

*Anunciantes con una integración de Adobe Advertising-Adobe Audience Manager o Adobe Advertising-Adobe Analytics solamente*

Los anunciantes de inclusión pueden crear [!DNL Google Ads] audiencias de coincidencia de clientes con ID de usuario de a) [!DNL Analytics] segmentos que se comparten con Adobe Experience Cloud y b) segmentos de Audience Manager que tienen como destino Search, Social y Commerce, incluidos los siguientes [!DNL Analytics] los segmentos que se publican en Adobe Experience Cloud y los segmentos que se crean con la biblioteca de audiencias de Adobe Experience Cloud. Buscar, Social y Comercio inserta automáticamente un [!DNL Google] URL de seguimiento de vuelta a cada [!DNL Analytics] o segmento de Audience Manager para que [!DNL Google] puede realizar un seguimiento de la audiencia.

Cada [!DNL Adobe] La audiencia solo se puede usar para una [!DNL Google] audiencia.

Cada nuevo [!DNL Google] La audiencia tiene el mismo nombre que el original [!DNL Adobe] audiencia. [!DNL Google] determina el tamaño de la audiencia que debe tener el destinatario.

>[!TIP]
>
>Para la segmentación en tiempo real, utilice audiencias creadas por Audience Manager. Segmentos creados en [!DNL Analytics] y sincronizados con Adobe Experience Cloud pueden tener poblaciones más pequeñas porque solo se sincronizan diariamente; un internauta que cumpla los requisitos de un segmento puede no incluirse en el segmento hasta el día siguiente. Segmentos de [!DNL Analytics] tiene una fuente de datos de &quot;grupo de informes - .&quot;

>[!NOTE]
>
>Search, Social y Commerce no almacenan ninguno de los datos de clientes de su [!DNL Adobe] segmentos utilizados para crear o editar un [!DNL Google] audiencia.

1. Complete los requisitos previos según sea necesario:

   1. (Para crear audiencias de lista de remarketing de ID de usuario) Una [!DNL Adobe] el usuario administrador o el administrador de cuentas deben seleccionar la configuración de nivel de anunciante para habilitar las audiencias de coincidencia de clientes. La configuración difiere entre anunciantes con Audience Manager y anunciantes con [!DNL Analytics] solo.

   1. Implementación de [Servicio de identidad de Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en) versión 2.0 o superior.

   1. Implemente la siguiente etiqueta lo más alto posible en las páginas web del anunciante desde las que se debe realizar el seguimiento de la audiencia

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      donde `Advertising_Cloud_UserID` es el ID de usuario único asignado al anunciante. Ejemplo:  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Si no se ha completado aún) Un usuario autorizado debe configurar la cuenta del anunciante en [sincronizar con la cuenta de organización del anunciante en Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Especifique la información de la audiencia:

   1. En el **[!UICONTROL Data Source]** menú, seleccione **[!UICONTROL Adobe Audience]**.

   1. Seleccione el [!UICONTROL Adobe Audience] en la que se basará la variable [!DNL Google] audiencia.

      >[!NOTE]
      >
      >[!DNL Adobe] audiencias que ya se han utilizado para otra [!DNL Google] La audiencia no está disponible.

      Si lo desea, puede buscar audiencias que contengan una cadena de texto específica con un mínimo de tres caracteres. Para cualquier audiencia coincidente, haga clic en **[!UICONTROL Include]** para seleccionarlo.

      Si selecciona varios [!DNL Adobe] audiencias y, a continuación, una [!DNL Google] La audiencia se crea para cada uno.

   1. Seleccione el **[!UICONTROL Audience Type]** para crear: **[!UICONTROL Customer List_User ID]**.

      El nombre del anunciante [!DNL Google Ads] la cuenta debe ser [apto para coincidencia personalizada](https://support.google.com/adspolicy/answer/6299717) y se ha suscrito para [remarketing de ID de usuario](https://support.google.com/google-ads/answer/9199250).

   1. Active la casilla de verificación para indicar que está de acuerdo con los términos del [!DNL Adobe] y políticas de privacidad de la red publicitaria.

   1. Especifique el número de **[!UICONTROL Membership Days]**, que es el número de días que la cookie de un usuario permanece en la audiencia.

      Utilice el periodo de tiempo durante el cual espera que el anuncio sea relevante para el usuario. Las listas de remarketing tienen una duración máxima de 540 días. Las listas de clientes no tienen una duración máxima; para indicar que la cookie nunca caduca, escriba 10000.

   1. Haga clic **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] puede tardar hasta 24 horas en procesar el archivo.
>
>* Consulte [[!DNL Google Ads] documentación sobre cómo funciona la coincidencia de clientes y limitaciones](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Crear un [!DNL Google Ads] audiencia de customer match de una lista de correo electrónico de Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes](audience-from-customer-data-list.md)
>* [Administración de audiencias de remarketing dinámico](audience-dynamic-remarketing-manage.md)

