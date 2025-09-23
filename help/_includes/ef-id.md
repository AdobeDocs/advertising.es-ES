---
source-git-commit: 0cf325946fdc3852b8b94acb29678bf6c47227a0
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# ID de Adobe Advertising EF

## ID de Adobe Advertising EF

El EF ID es un token único que Adobe Advertising utiliza para asociar la actividad con un clic en línea o la exposición de un anuncio en el nivel de navegador o dispositivo individual. Los EF ID actúan principalmente como claves para enviar datos de [!DNL Analytics] y Customer Journey Analytics a Adobe Advertising para la creación de informes y la optimización de ofertas en Adobe Advertising.

Para [!DNL Analytics], el ID de EF se almacena en la dimensión [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (reservada [!DNL eVar]) (ID de EF de Adobe Advertising).

Para Customer Journey Analytics, el identificador EF se almacena en la propiedad `trackingIdentities` del objeto `conversionDetails`, que forma parte de [el [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension).

### Formatos de ID de EF {#ef-id-formats}

>[!NOTE]
>
>Los ID de EF distinguen entre mayúsculas y minúsculas. Si una implementación de [!DNL Analytics] o Customer Journey Analytics obliga al seguimiento de URL a usar minúsculas, Adobe Advertising no reconocerá el EF ID. Esto afecta a las ofertas y los informes de Adobe Advertising, pero no afecta a los informes de Adobe Advertising en [!DNL Analytics] o Customer Journey Analytics.

#### [!DNL Google Ads] anuncios de búsqueda

```
{gclid}:G:s
```

donde:

* `gclid` es [!DNL Google Click ID] (GCLID).
* `s` es el tipo de red (&quot;s&quot; para la búsqueda).

#### [!DNL Microsoft Advertising] anuncios de búsqueda

```
{msclkid}:G:s
```

donde:

* `msclkid` es el [!DNL Microsoft Click ID] (MSCLKID).
* `s` es el tipo de red (&quot;s&quot; para la búsqueda).

#### Mostrar anuncios y anuncios de búsqueda en otros motores de búsqueda

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

donde:

* &lt;*ID de visitante de Adobe Advertising*> es un ID único por visitante (como UhKVaAAABCkJ0mDt). También se denomina *ID de internauta*.

* &lt;*timestamp*> es la hora con formato AAAAMMDDHHMMSS (como 20190821192533 para el año 2019, mes 08, día 21, hora 19:25:33).

* &lt;*tipo de canal*> es el tipo de canal responsable del clic o la exposición:

   * `d` por hacer clic en un anuncio en pantalla de DSP (pulsación en pantalla)
   * `i` para una impresión de un anuncio en pantalla de DSP (visualización completa)
   * `s` para un clic en un anuncio de búsqueda (pulsación de búsqueda).

Ejemplo `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
