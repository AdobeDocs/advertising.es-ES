---
title: Especificación creativa de HTML5
description: Consulte la especificación creativa de HTML5 para Advertising Creative.
feature: Creative Standard Creatives
exl-id: 06d29442-d688-4fb8-ad6f-cba0a897fde0
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Especificación creativa de HTML5 para Advertising Creative

Este documento describe los requisitos y la compatibilidad con la API para los creativos de HTML5 en [!DNL Creative]. La API permite el desarrollo de creativos de HTML5 cuyos atributos se pueden configurar en el momento de la entrega creativa.

## Ámbito

[!DNL Creative] admite titulares de HTML5 con elementos multimedia no enriquecidos que aparecen dentro de los bordes definidos de una página. Puede utilizar los siguientes tipos de HTML5 creativos:

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML5:** admite hasta 5 direcciones URL de páginas de aterrizaje que se pueden configurar durante la creación creativa y el tráfico.

* **HTML5 flexible:** admite hasta 5 direcciones URL de páginas de aterrizaje que se pueden configurar durante la creación y el tráfico creativos, y también permite modificar los atributos creativos durante la creación y el tráfico creativos.

## Requisitos

### Requisitos de carpeta y compresión

* El elemento creativo debe estar empaquetado en un archivo ZIP (formato .ZIP). Los archivos ZIP anidados no son compatibles, por lo que no incluya una carpeta comprimida dentro de la carpeta comprimida externa.

* El archivo ZIP debe contener al menos un archivo HTML (el archivo de visualización principal de HTML) que incluya una referencia a la biblioteca de JavaScript [!DNL Creative]. El archivo HTML principal puede estar en la carpeta raíz o en una subcarpeta.

* Al archivo HTML principal se le puede asignar cualquier nombre, siempre que no incluya caracteres especiales, aunque se recomienda `index.html`.

* Todos los recursos de soporte necesarios para procesar el elemento creativo final deben encontrarse en la misma carpeta que el archivo de visualización de HTML o en subcarpetas de la carpeta principal.

* No incluya en el creativo ningún archivo al que el creativo no haga referencia.

### Inclusión del archivo JavaScript de Advertising Creative

El archivo HTML principal (y ningún otro archivo) debe contener una referencia al archivo JavaScript `AMOLibrary.js`. Llame al archivo en la primera línea de la sección `<head>` con la siguiente dirección:

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

Este archivo contiene funciones para garantizar que la prueba local de eventos de salida se realice sin problemas.

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### Requisitos creativos de HTML5

#### Compatibilidad con URL de pulsaciones en HTML estático5

##### `amo.registerClick(clkVar, clkUrl)`

Registra las direcciones URL de pulsación y el parámetro asociado utilizado para hacer referencia a cada dirección URL (conocido como `clickTag`). Esta API informa al servidor de publicidad [!DNL Creative] sobre dónde agregar el rastreo de clics. Puede utilizar esta API para registrar hasta cinco variables de etiqueta de clic, cada una con la dirección URL de la página de aterrizaje correspondiente.

>[!NOTE]
>
>Las direcciones URL estáticas que incluya en el creativo de HTML5 se utilizan únicamente con fines de prueba local y se sobrescribirán. Al cargar un elemento creativo de HTML5, se define la página de aterrizaje predeterminada para cada variable `clickTag`. Al asignar un elemento creativo de HTML5 cargado a una experiencia publicitaria, puede, opcionalmente, anular la página de aterrizaje predeterminada para cada variable de `clickTag` y [!DNL Creative] agrega el rastreo de clics a las direcciones URL cuando guarda la experiencia.

###### Parámetros

* `clkVar`: nombre de la variable de clic (normalmente &quot;clickTag&quot;), entre comillas dobles.

* `clkUrl`: la dirección URL de la página de aterrizaje para esta variable de clic, entre comillas dobles.

###### Uso

Llame a `amo.registerClick()` en la sección `<head>` del archivo principal de HTML.

###### Ejemplo

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Déclencheur el evento de salida, que redirige al usuario a la página de aterrizaje configurada para `clickTag`. Durante las pruebas locales, esta función advierte a los desarrolladores de si la URL que se pasa a la función se ha registrado.

###### Parámetros

* `clkTag`: nombre de la variable de clic que se usa para asignar la dirección URL de la página de aterrizaje mediante la función `amo.registerClick()`, entre comillas simples.

* `event` — (Opcional) El objeto de evento &quot;clic&quot; de JavaScript. Registra las coordenadas de los clics, que se pueden utilizar para analizar el rendimiento creativo.

###### Uso

Llame a `amo.onAdClick()` en la sección `<body>` del archivo principal de HTML.

###### Ejemplos

`amo.onAdClick('clickTag')` O `amo.onAdClick('clickTag',clickEvt)`

### Requisitos creativos flexibles de HTML5

#### Compatibilidad con URL de pulsaciones en HTML5 flexible

##### `amo.registerClick(clkVar, clkUrl)`

Registra las direcciones URL de pulsación y el parámetro asociado utilizado para hacer referencia a cada dirección URL (conocido como `clickTag`). Esta API informa al servidor de publicidad [!DNL Creative] sobre dónde agregar el rastreo de clics. Puede utilizar esta API para registrar hasta cinco variables de etiqueta de clic, cada una con la dirección URL de la página de aterrizaje correspondiente.

>[!NOTE]
>
>Las direcciones URL estáticas que incluya en el creativo de HTML5 se utilizan únicamente con fines de prueba local y se sobrescribirán. Al cargar un elemento creativo de HTML5, se define la página de aterrizaje predeterminada para cada variable `clickTag`. Al asignar un elemento creativo de HTML5 cargado a una experiencia publicitaria, puede, opcionalmente, anular la página de aterrizaje predeterminada para cada variable de `clickTag` y [!DNL Creative] agrega el rastreo de clics a las direcciones URL cuando guarda la experiencia.

###### Parámetros

* `clkVar`: nombre de la variable de clic (normalmente &quot;clickTag&quot;), entre comillas dobles.

* `clkUrl`: la dirección URL de la página de aterrizaje para esta variable de clic, entre comillas dobles.

###### Uso

Llame a `amo.registerClick()` en la sección `<head>` del archivo principal de HTML.

###### Ejemplo

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Déclencheur el evento de salida, que redirige al usuario a la página de aterrizaje configurada para `clickTag`. Durante las pruebas locales, esta función advierte a los desarrolladores de si la URL que se pasa a la función se ha registrado.

###### Parámetros

* `clkTag`: nombre de la variable de clic que se usa para asignar la dirección URL de la página de aterrizaje mediante la función `amo.registerClick()`, entre comillas simples.

* `event` — (Opcional) El objeto de evento &quot;clic&quot; de JavaScript. Registra las coordenadas de los clics, que se pueden utilizar para analizar el rendimiento creativo.

###### Uso

Llame a `amo.onAdClick()` en la sección `<body>` del archivo principal de HTML.

###### Ejemplos

`amo.onAdClick('clickTag')` O `amo.onAdClick('clickTag',clickEvt)`

#### Compatibilidad con atributos creativos en HTML5 flexible

##### `amo.registerAttribute(key, type, value)`

Define los atributos de los elementos creativos que se pueden cambiar en el momento de la creación creativa o de la experiencia. Puede definir hasta 20 atributos creativos que se pueden configurar en el momento de la creación creativa o de la experiencia.

>[!NOTE]
>
>Los valores definidos en este método se utilizan únicamente para el desarrollo local y no se utilizan en el servicio de anuncios en directo.

###### Parámetros

* `key`: el nombre alfanumérico del atributo. Debe comenzar con un carácter alfabético.

* `type`: el tipo de atributo (`TEXT` o `IMAGE`).

* `value`: valor del atributo para pruebas. Para atributos de tipo `IMAGE`, el valor debe ser la ruta relativa al archivo de imagen.

###### Uso

Llame a `amo.registerAttribute()` para registrar un atributo, tipo y valor creativo durante la prueba en modo local. Los archivos de imagen utilizados como valores de muestra deben empaquetarse en el archivo ZIP junto con el paquete cargado.

##### `amo.attributes`

Un objeto JSON para consultar los nombres y valores de las variables de atributos creativos. Las claves de objeto son los nombres de atributo y los valores son los valores de dichos atributos.

En el modo de prueba local, los pares clave-valor son los pares registrados por la API `amo.registerAttribute`. Para la producción, los nombres y valores de las variables de los atributos creativos deben configurarse en el momento de la creación y el tráfico creativos.

### Requisitos de contenido de Creative

La mayoría de los intercambios de pantallas disponibles en Advertising DSP tienen los siguientes requisitos creativos:

* Un borde sólido debe rodear todas las imágenes de publicidad.

* No se permiten anuncios expansivos.

* La página de aterrizaje debe abrirse en una nueva ventana.

* El dominio de la página de aterrizaje y sus subdominios no pueden tener más de 35 caracteres. **Nota:** Las direcciones URL de la página de aterrizaje final se definen en DSP y no en los propios recursos de HTML5.

* Cualquier renuncia a la oferta de un anuncio debe incluirse en el propio anuncio y no solo en la página de aterrizaje.

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## Contenido de ejemplo como objeto y matriz JSON

### Contenido de ejemplo como objeto JSON

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### Contenido de ejemplo como matriz JSON

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## Ejemplo de creatividad de HTML5

### Ejemplo de estructura de carpetas (después de la descompresión)

* index.html

* /assets (carpeta)

   * bg.jpg (imagen de JPG, PNG, SVG o GIF)

### Archivo HTML de ejemplo (index.html) para creativos HTML5 simples

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### Ejemplo de archivo de HTML (index.html) para creativos estáticos de HTML5

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [Agregar elementos creativos estándar a una biblioteca creativa](/help/creative/creative-libraries/creative-add-standard.md)
