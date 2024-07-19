---
title: Seguimiento de conversión mediante una fuente de ID de EF
description: Obtenga información acerca del uso de una fuente de ID de EF para los datos de seguimiento de conversión.
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Seguimiento de conversión mediante una fuente de ID de EF

Con este método, Advertising Cloud recopila un valor `ef_id` cada vez que un usuario hace clic en el anuncio y lo llega a la página de aterrizaje, y el anunciante almacena el valor `ef_id` con los datos de conversión y lo envía en una fuente de datos.

## Resumen de implementación

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas [!DNL Adobe] y administrador de usuarios*

1. Utilice las opciones de seguimiento de cuenta o campaña &quot;[!UICONTROL EF Redirect]&quot;, el tipo de redirección &quot;[!UICONTROL Token]&quot; y &quot;[!UICONTROL Auto Upload]&quot; para generar automáticamente una dirección URL de destino o una dirección URL final con un token de Adobe Advertising (ef_id) para cada palabra clave (para el seguimiento a nivel de palabra clave) o anuncio (para el seguimiento a nivel de anuncio) en la cuenta o campaña.

   >[!NOTE]
   >* Este método no requiere que el anunciante utilice etiquetas de seguimiento de conversión de Adobe Advertising.
   >* Si cambia el tipo de redirección de una cuenta o campaña existente de [!UICONTROL Standard] a [!UICONTROL Token], o viceversa, debe volver a generar todas las direcciones URL de seguimiento aplicables.

   ef_id se rellena y se anexa a la dirección URL de la página de aterrizaje cuando el usuario final hace clic en el anuncio y se redirige a un servidor de Adobe Advertising. A continuación, se pasa ef_id al anunciante en la dirección URL de destino o en la dirección URL final del anuncio o la palabra clave. A continuación se muestra un ejemplo de una dirección URL de destino que se pasa al anunciante durante el redireccionamiento:

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. El anunciante extrae el ef_id de la redirección y lo almacena con los datos de conversión relevantes para incluirlos en el archivo de fuente. No modifique el ef_id ni cambie su mayúsculas y minúsculas.

1. (Opcional, pero recomendada) El anunciante puede crear un ID de transacción único para cada transacción y así incluirlo en el archivo de fuente.

1. El anunciante carga un archivo con los [datos de conversión necesarios](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) en la ubicación designada del servidor.

1. Los servicios técnicos analizan los datos de conversión de los archivos cargados y, a continuación, cargan los datos en el Adobe Advertising. A continuación, el Adobe Advertising realiza un seguimiento de los datos con palabras clave, anuncios y ubicaciones individuales y crea previsiones de ingresos para cada uno.

1. Los servicios técnicos validan los datos procesados con los datos de las fuentes y comprueban si hay [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de archivo para archivos de fuentes de conversión](feed-file-requirements.md)
>* [Requisitos de datos para fuentes de datos que usan EF ID](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
