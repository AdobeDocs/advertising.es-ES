---
source-git-commit: 56c27461cf0e1d7111de9d35d9e38fa980af4c52
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---
# Formatos de ID de EF

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
