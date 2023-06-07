---
title: Seguimiento de conversión mediante una fuente de ID de EF
description: Obtenga información acerca del uso de una fuente de ID de EF para los datos de seguimiento de conversión.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Seguimiento de conversión mediante una fuente de ID de EF

Con este método, Advertising Cloud recopila un `ef_id` valor cada vez que un usuario hace clic en el anuncio y llega a la página de aterrizaje, y el anunciante almacena el `ef_id` con los datos de conversión y lo envía en una fuente de datos.

## Resumen de implementación

*Administrador de cuentas de agencia, [!DNL Adobe] administrador de cuentas y roles de usuario administrador solamente*

1. Utilice las opciones de cuenta o seguimiento de campaña &quot;[!UICONTROL EF Redirect],&quot; el tipo de redirección de &quot;[!UICONTROL Token],&quot; y &quot;[!UICONTROL Auto Upload]&quot; para generar automáticamente una URL de destino o una URL final con un token de publicidad de Adobe (ef_id) para cada palabra clave (para el seguimiento a nivel de palabra clave) o anuncio (para el seguimiento a nivel de anuncio) en la cuenta o campaña.

   >[!NOTE]
   >* Este método no requiere que el anunciante utilice etiquetas de seguimiento de conversión de publicidad de Adobe.
   >* Si cambia el tipo de redirección de una cuenta o campaña existente de [!UICONTROL Standard] hasta [!UICONTROL Token], o viceversa, debe volver a generar todas las URL de seguimiento aplicables.


   El ef_id se rellena y se anexa a la dirección URL de la página de aterrizaje cuando el usuario final hace clic en el anuncio y se redirige a un servidor de publicidad de Adobe. A continuación, se pasa ef_id al anunciante en la dirección URL de destino o en la dirección URL final del anuncio o la palabra clave. A continuación se muestra un ejemplo de una dirección URL de destino que se pasa al anunciante durante el redireccionamiento:

   http://pixel.everesttech.net/1180/cq?ev_sid=3&amp;ev_ln={keyword}&amp;ev_crx={creative}&amp;ev_mt={matchtype}&amp;ev_n={network}&amp;ev_ltx=&amp;ev_pl={placement}&amp;url=http%3A//www.example.com&amp;ef_id=D59Nu0u@BD0AAM1q:20110630172936:s

1. El anunciante extrae el ef_id de la redirección y lo almacena con los datos de conversión relevantes para incluirlos en el archivo de fuente. No modifique el ef_id ni cambie su mayúsculas y minúsculas.

1. (Opcional, pero recomendada) El anunciante puede crear un ID de transacción único para cada transacción y así incluirlo en el archivo de fuente.

1. El anunciante carga un archivo con la variable [datos de conversión necesarios](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) a la ubicación designada del servidor.

1. Los servicios técnicos analizan los datos de conversión de los archivos cargados y, a continuación, cargan los datos en la publicidad de Adobe. A continuación, Adobe Advertising realiza un seguimiento de los datos utilizando palabras clave, anuncios y ubicaciones para cada uno, y crea previsiones de ingresos para cada uno de ellos.

1. Los servicios técnicos validan los datos procesados con los datos de las fuentes y comprueban la existencia de cualquier [transacciones huérfanas](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Requisitos de archivo para archivos de fuentes de conversión](feed-file-requirements.md)
>* [Requisitos de datos para fuentes de datos que utilizan EF ID](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)


