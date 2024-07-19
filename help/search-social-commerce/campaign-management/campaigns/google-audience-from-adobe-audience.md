---
title: Crear  [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias
description: Aprenda a crear  [!DNL Google Ads] audiencias de coincidencia de cliente a partir de las audiencias de Adobe Analytics y Audience Manager existentes.
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de las audiencias de Adobe Analytics y Audience Manager

*[!DNL Google Ads]cuentas elegibles para la coincidencia de clientes solamente*

*Anunciantes con una integración de Adobe Advertising-Adobe Audience Manager o Adobe Advertising-Adobe Analytics solamente*

Los anunciantes de inclusión pueden crear [!DNL Google Ads] audiencias de coincidencia de clientes usando los ID de usuario de a) [!DNL Analytics] segmentos que se comparten con Adobe Experience Cloud y b) segmentos de Audience Manager que tienen Search, Social y Commerce como destino, incluidos [!DNL Analytics] segmentos publicados en Adobe Experience Cloud y los segmentos creados con la biblioteca de audiencias de Adobe Experience Cloud. Search, Social y Commerce devuelven automáticamente una URL de seguimiento [!DNL Google] a cada segmento de Audience Manager o [!DNL Analytics] para que [!DNL Google] pueda rastrear la audiencia.

Cada audiencia [!DNL Adobe] se puede usar para una sola audiencia [!DNL Google].

Cada nueva audiencia [!DNL Google] tiene el mismo nombre que la audiencia [!DNL Adobe] original. [!DNL Google] determina el tamaño de la audiencia que debe ser objetivo.

>[!TIP]
>
>Para la segmentación en tiempo real, utilice audiencias creadas por Audience Manager. Los segmentos creados en [!DNL Analytics] y sincronizados con Adobe Experience Cloud pueden tener poblaciones más pequeñas porque solo se sincronizan diariamente; es posible que un internauta que cumpla los requisitos para un segmento no se incluya en el segmento hasta el día siguiente. Los segmentos de [!DNL Analytics] tienen la fuente de datos &quot;grupo de informes - .&quot;

>[!NOTE]
>
>Search, Social y Commerce no almacenan los datos de clientes de sus segmentos de [!DNL Adobe] utilizados para crear o editar una audiencia de [!DNL Google].

1. Complete los requisitos previos según sea necesario:

   1. (Para crear audiencias de lista de remarketing con ID de usuario) Un usuario administrador de [!DNL Adobe] o administrador de cuentas debe seleccionar la configuración de nivel de anunciante para habilitar las audiencias de coincidencia de clientes.

   1. Implemente el [Servicio de identidad de Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html) versión 2.0 o superior.

   1. Implemente la siguiente etiqueta lo más alto posible en las páginas web del anunciante desde las que se debe realizar el seguimiento de la audiencia

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      donde `Advertising_Cloud_UserID` es el identificador numérico de usuario único asignado al anunciante.

      Ejemplo: `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. (Si aún no se ha completado) Un usuario autorizado debe configurar la cuenta del anunciante para [sincronizar con la cuenta de organización del anunciante en Adobe Experience Cloud](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. En los submenús, haga clic en **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. Seleccione la red publicitaria y el nombre de cuenta y, a continuación, haga clic en **[!UICONTROL Continue]**.

1. Especifique la información de la audiencia:

   1. En el menú **[!UICONTROL Data Source]**, seleccione **[!UICONTROL Adobe Audience]**.

   1. Seleccione el(la) [!UICONTROL Adobe Audience] en el que desea basar la audiencia [!DNL Google].

      >[!NOTE]
      >
      >Las audiencias de [!DNL Adobe] que ya se han usado para otra audiencia de [!DNL Google] no están disponibles.

      Si lo desea, puede buscar audiencias que contengan una cadena de texto específica con un mínimo de tres caracteres. Para cualquier audiencia que coincida, haga clic en **[!UICONTROL Include]** para seleccionarlo.

      Si selecciona varias audiencias de [!DNL Adobe], se crea una audiencia de [!DNL Google] independiente para cada una.

   1. Seleccione **[!UICONTROL Audience Type]** para crear: **[!UICONTROL Customer List_User ID]**.

      La cuenta del anunciante [!DNL Google Ads] debe ser [elegible para la coincidencia personalizada](https://support.google.com/adspolicy/answer/6299717) y se ha suscrito para el [remarketing de ID de usuario](https://support.google.com/google-ads/answer/9199250).

   1. Active la casilla de verificación para indicar que está de acuerdo con los términos de [!DNL Adobe] y las directivas de privacidad de red de anuncios.

   1. Especifique el número de **[!UICONTROL Membership Days]**, que es el número de días que la cookie de un usuario permanece en la audiencia.

      Utilice el periodo de tiempo durante el cual espera que el anuncio sea relevante para el usuario. Las listas de remarketing tienen una duración máxima de 540 días. Las listas de clientes no tienen una duración máxima; para indicar que la cookie nunca caduca, escriba 10000.

   1. Haga clic en **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] puede tardar hasta 24 horas en procesar el archivo.
>
>* Ver [[!DNL Google Ads] documentación sobre cómo funciona la coincidencia de clientes y las limitaciones](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Crear una audiencia de  [!DNL Google Ads] customer match a partir de una lista de correo electrónico de Adobe Campaign](google-audience-from-campaign-email-list.md)
>* [Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes](audience-from-customer-data-list.md)
>* [Administrar audiencias de remarketing dinámico](audience-dynamic-remarketing-manage.md)
