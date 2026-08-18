---
title: Metadatos de C2PA en Creative Studio
description: Descubra cómo los metadatos de C2PA se adjuntan automáticamente al contenido generado o editado con IA generativa en Creative Studio.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d335c890ccc3ff8b2d391881660a71d10fcba53a
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# Metadatos de C2PA en [!UICONTROL Creative Studio]

[!UICONTROL Creative Studio] adjunta automáticamente metadatos de C2PA al contenido que se genera o edita con IA generativa, de modo que la procedencia del contenido del anuncio se registre como metadatos duraderos e invisibles. Los metadatos siguen el estándar de la [Coalición para la procedencia y autenticidad del contenido](https://c2pa.org/) (C2PA).

## Tipos de contenido y su ámbito {#cc-content-types}

| Tipo de contenido | Compatible? | Servicio de IA que genera el contenido | Modelo que genera la credencial |
| --- | --- | --- | --- |
| Imágenes | Sí. Los metadatos de C2PA se adjuntan cuando las imágenes se generan o editan con IA generativa y se conservan mediante las operaciones de recorte y cambio de tamaño realizadas por el asistente de IA. | [!DNL Adobe Firefly C2PA] | [!DNL Gemini Flash] |

## Acciones que adjuntan metadatos de C2PA

La siguiente tabla resume cuándo se adjuntan los metadatos de C2PA, en función de la acción de imagen realizada en el asistente de IA [!UICONTROL Creative Studio].

| Acción | Descripción | ¿Metadatos de C2PA adjuntos? | Ejemplo de caso de uso |
| --- | --- | --- | --- |
| **Generar una imagen** | Crear una nueva imagen con un mensaje de texto | Siempre, porque la imagen se genera mediante IA generativa. | Se utiliza un mensaje de texto para generar una nueva imagen de fondo o un logotipo para una plantilla de anuncio.<br><br>Utiliza un mensaje de texto para reemplazar la imagen predeterminada de un concepto de anuncio con un recurso cargado de su biblioteca.<br><br>Utiliza un mensaje de texto para generar variaciones de una imagen de fondo en una plantilla de anuncio. |

## ¿Qué sucede a medida que se mueve el contenido? {#cc-content-moves}

La cadena de procedencia completa se conserva cuando un usuario descarga un archivo de imagen o se envía para que se publique en un anuncio.

## ¿Qué incluyen los metadatos de C2PA?

Para cada generación o modificación de GenAI, se incluyen los siguientes metadatos de C2PA. Si un recurso se altera varias veces, cada operación aparece en los metadatos de C2PA.

* Nombre y versión del sistema de IA utilizado ([!DNL Adobe Firefly C2PA])
* Modelo de IA utilizado ([!DNL Gemini Flash])
* Uso: Si se generó o editó mediante GenAI
* Fecha y hora de creación o modificación del contenido con las herramientas de IA generativa
* Identificador único (que puede utilizarse para distinguir cada uso de IA generativa)

## ¿Cómo puedo ver los metadatos de C2PA de una imagen?

Para ver el historial completo de recursos de una imagen,

* Abra el archivo de imagen en una herramienta de inspección de autenticidad de contenido, como https://contentauthenticity.adobe.com/inspect o https://verify.contentauthenticity.org/.

* Vea los metadatos de la imagen.

* Vea el código de imagen con la herramienta de inspección de código del explorador (generalmente denominada [!DNL Inspect]).

![Ejemplo de metadatos de C2PA para una imagen](/help/creative/assets/cs-content-credentials-example.png "Metadatos de C2PA para una imagen")

## Recursos adicionales

* [[!DNL Adobe] directrices de usuario de IA generativas](https://www.adobe.com/es/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

>[!MORELIKETHIS]
>
>* [Acerca de Creative Studio](/help/creative/creative-studio/creative-studio-about.md)
