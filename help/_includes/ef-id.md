---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---
# ID de Adobe Advertising EF

El EF ID es un token único que Adobe Advertising utiliza para asociar la actividad con un clic en línea o la exposición de un anuncio en el nivel de navegador o dispositivo individual. Los EF ID actúan principalmente como claves para enviar datos de [!DNL Analytics] y Customer Journey Analytics a Adobe Advertising para la creación de informes y la optimización de ofertas en Adobe Advertising.

Para [!DNL Analytics], el ID de EF se almacena en la dimensión [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (reservada [!DNL eVar]) (ID de EF de Adobe Advertising).

Para Customer Journey Analytics, el identificador EF se almacena en la propiedad `trackingIdentities` del objeto `conversionDetails`, que forma parte de [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension].
