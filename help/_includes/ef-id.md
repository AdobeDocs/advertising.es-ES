---
source-git-commit: 8c36de7ffe73f86a4e78f11e38cd84fa59134833
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---
# ID de Adobe Advertising EF

## ID de Adobe Advertising EF

El EF ID es un token único que Adobe Advertising utiliza para asociar la actividad con un clic en línea o una exposición de publicidad. El EF ID se almacena en la dimensión [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) o [!DNL rVar] (reservado [!DNL eVar]) (Adobe Advertising EF ID) y rastrea cada clic o exposición de anuncio en el nivel de navegador o dispositivo individual. Los EF ID actúan principalmente como claves para enviar datos de [!DNL Analytics] a Adobe Advertising para la creación de informes y la optimización de ofertas en Adobe Advertising.

### Formato de ID de EF

>[!NOTE]
>
>Los ID de EF distinguen entre mayúsculas y minúsculas. Si una implementación de [!DNL Analytics] obliga al seguimiento de URL a usar minúsculas, Adobe Advertising no reconocerá el EF ID. Esto afecta las ofertas y los informes de Adobe Advertising, pero no afecta a los informes de Adobe Advertising dentro de [!DNL Analytics].

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
