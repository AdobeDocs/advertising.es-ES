---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# ID de Adobe Advertising EF

## ID de Adobe Advertising EF

El EF ID es un token único que Adobe Advertising utiliza para asociar la actividad con un clic en línea o la exposición de un anuncio en el nivel de navegador o dispositivo individual. Los EF ID actúan principalmente como claves para enviar datos de [!DNL Analytics] y Customer Journey Analytics a Adobe Advertising para la creación de informes y la optimización de ofertas en Adobe Advertising.

Para [!DNL Analytics], el ID de EF se almacena en la dimensión [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=es) o [!DNL rVar] (reservada [!DNL eVar]) (ID de EF de Adobe Advertising).

Para Customer Journey Analytics, el identificador EF se almacena en la propiedad `trackingIdentities` del objeto `conversionDetails`, que forma parte de [el [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/es/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

### Formatos de ID de EF {#ef-id-formats}

Consulte los [formatos para elementos de dimensión de EF ID](https://experienceleague.adobe.com/es/docs/analytics/components/dimensions/amo-ef-id#dimension-items) en la &quot;Guía de componentes de Adobe Analytics&quot;.

>[!NOTE]
>
>Los ID de EF distinguen entre mayúsculas y minúsculas. Si una implementación de [!DNL Analytics] o Customer Journey Analytics obliga al seguimiento de URL a usar minúsculas, Adobe Advertising no reconocerá el EF ID. Esto afecta a las ofertas y los informes de Adobe Advertising, pero no afecta a los informes de Adobe Advertising en [!DNL Analytics] o Customer Journey Analytics.

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
