---
title: Compatibilidad con la activación de ID universales
description: Obtenga información acerca de la compatibilidad para importar segmentos de ID universales, crear segmentos personalizados para rastrear ID universales y convertir otros identificadores de usuario en segmentos de origen a ID universales para una segmentación sin cookies.
feature: DSP Audiences
source-git-commit: 56489cd226d4a46fa3b1548492b4a9c6fd7e0528
workflow-type: tm+mt
source-wordcount: '1369'
ht-degree: 0%

---

# Compatibilidad con la activación de ID universales

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Función beta*

DSP DSP La compatibilidad con ID universales y basados en personas para la segmentación sin cookies de un solo dispositivo (no entre dispositivos) en los formatos digitales admitidos por la aplicación de la.

* Puede enviar manualmente su [[!DNL LiveRamp] [!DNL RampIDs]DSP ] directamente a los usuarios que utilizan el [!DNL LiveRamp] [!DNL Connect] panel. Consulte &quot;[Importar manualmente segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* DSP Puede ingerir segmentos de origen compuestos de ID de correo electrónico con hash creados dentro de su plataforma de datos del cliente (CDP) y convertirlos a [!DNL LiveRamp] [!DNL RampIDs] y [!DNL Unified ID 2.0 (UID2.0)] ID. Para obtener más información sobre las plataformas de datos de clientes compatibles, las funciones disponibles para cada tipo de ID universal compatible y los flujos de trabajo relacionados, consulte &quot;[Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md).&quot;

* Puede crear segmentos personalizados que hagan un seguimiento de los usuarios asociados con los ID universales ID5 que están expuestos a anuncios de dispositivos de escritorio y móviles y que visitan páginas web específicas. ID5 utiliza un modelo probabilístico para asignar un ID derivado de varias señales de usuario y señales de explorador. Para obtener instrucciones, consulte &quot;[Creación e implementación de un segmento personalizado](/help/dsp/audiences/custom-segment-create.md).&quot;

* Segmentos de terceros de [!DNL Eyeota] y algunos otros proveedores pueden incluir automáticamente ID5, además de los usuarios rastreados mediante cookies o ID de dispositivo. Los detalles del segmento incluyen el tamaño de cada tipo. Se aplica la tarifa de uso habitual para cada segmento, que se indica junto al nombre del segmento; no se cobran tarifas adicionales por los ID5.

<!-- Make above statement more generic when other ID types are available 

* Some third-party segment vendors have started including universal IDs in their segments, and you can use them in saved audiences and as placement targets without any extra steps or extra fees.
-->

## Creación de informes por tipo de ID universal

* **Informes personalizados:** Los datos de coste, impresión, clics, conversión y frecuencia por tipo de ID universal están disponibles en los informes personalizados.

* **[!DNL Analytics]informes:** Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) Los usuarios que hayan implementado todos los pasos necesarios pueden ver las conversiones de visualizaciones por tipo de ID universal en [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Para la atribución de conversión adecuada, asegúrese de que las direcciones URL de clics para sus anuncios incluyan tanto la [EF ID y el AMO ID](/help/integrations/analytics/ids.md).

* **Detalles del segmento:** Para todos los tipos de segmentos, los detalles del segmento incluyen el tamaño de la audiencia por tipo de ID universal y por el tipo de dispositivo rastreado mediante cookies o ID de dispositivo.

## Cómo segmentar una audiencia de ID universal en sus ubicaciones

>[!NOTE]
>
>No puede cambiar los tipos de ID de destino en una ubicación activa. Si es necesario, puede duplicar una ubicación activa y cambiar los tipos de ID de destino en la nueva ubicación.

En una ubicación nueva, programada o en pausa, haga lo siguiente:

1. En el [!UICONTROL Geo-Targeting] , especifique las áreas geográficas de destino. Cada socio de ID universal permite la segmentación de usuarios únicamente en áreas geográficas específicas y solo los tipos de ID aptos están disponibles en el [!UICONTROL Targeting] configuración.

1. En el [!UICONTROL Audience Targeting] , haga lo siguiente:

   1. En el [!UICONTROL Included Audiences] , seleccione el segmento para el que se convirtieron los datos de usuario en ID universales.

      Si lo desea, puede incluir segmentos adicionales.

   1. En el [!UICONTROL Targeting] configuración:

      1. Seleccione el tipo de ID universal de destino.

         La configuración incluye las opciones &quot;[!UICONTROL Legacy IDs]&quot; y &quot;[!UICONTROL Universal ID],&quot; que puede incluir las subopciones &quot;[!UICONTROL ID5],&quot; &quot;[!UICONTROL RampID],&quot; y &quot;[!UICONTROL Unified ID2.0].&quot; Las subopciones reales están determinadas por los destinos geográficos seleccionados.

         Puede seleccionar ambas opciones &quot;[!UICONTROL Legacy IDs]&quot; y &quot;[!UICONTROL Universal ID],&quot;, pero solo puede seleccionar un tipo de ID universal por ubicación. Al seleccionar ID heredados e ID universales, se da preferencia de oferta a los ID universales.

      1. (Si es necesario) Acepte el contrato de términos de servicio para el uso de ID universales.

         DSP Para poder convertir datos a un nuevo tipo de ID, un usuario de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de debe aceptar los términos del contrato de servicio de. Los términos deben aceptarse solo una vez por tipo de ID, por cuenta.

Consulte &quot;[Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Prácticas recomendadas para pruebas y validación de datos

Siga estas prácticas recomendadas para [!DNL RampID]Segmentos basados en y segmentos basados en ID5, para los que está disponible la medición de Adobe Analytics.

* Unas 24 horas después de activar un segmento, compruebe el recuento de ID convertidos para el segmento en [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Si el recuento de ID es inesperado, póngase en contacto con el equipo de cuenta de Adobe.

  Consulte &quot;[Causas de variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot; para obtener más información sobre cómo pueden variar los recuentos de segmentos.

* No cambie los paquetes y las ubicaciones existentes. Sin embargo, si no tiene un presupuesto incremental para probar los ID universales, reduzca los presupuestos originales para financiar las pruebas.

* Copie los paquetes y las ubicaciones originales, ajuste los presupuestos según el tamaño de la prueba y cambie las audiencias que desee utilizar [!DNL RampID]Segmentos basados en (para usuarios autenticados) o segmentos basados en ID5 (para usuarios no autenticados), y compruebe que los nuevos paquetes y ubicaciones gastan sus presupuestos completos.

   * Para comparar el rendimiento de los segmentos basados en ID universales con el de las ubicaciones dirigidas a otros identificadores de audiencia, como, por ejemplo, cookies o ID de publicidad móvil, cree una campaña con una ubicación basada en ID universal y una ubicación basada en ID heredados.

     Para una prueba de retargeting completa, establezca como objetivo RampID para usuarios autenticados e ID5s para usuarios no autenticados.

     Obtener el mejor rendimiento no debería ser la comparación principal. En su lugar, determine qué ID se adaptan bien, lo que podría informar la optimización y las asignaciones presupuestarias más adelante. El objetivo a largo plazo es compensar las impresiones perdidas y el tráfico del sitio cuando las cookies están en desuso.

   * Para comparar el alcance total del explorador, establezca como objetivo segmentos universales basados en ID y segmentos heredados basados en ID en la misma ubicación. Utilice la misma configuración de campaña que el caso de uso anterior, excepto que no es necesario dividir el presupuesto de la campaña.

     La preferencia de oferta se da a los ID universales, pero los ID heredados reciben ofertas cuando los ID universales no están disponibles. Asegúrese de comparar el alcance en distintos exploradores (incluidos Chrome, Safari y Mozilla).

     >[!NOTE]
     >
     >La restricción de frecuencia se aplica a un ID individual. Cuando un usuario tiene varios tipos de ID, es posible que esté llegando a ese usuario más de lo que esperaba.

* Recuerde que el alcance de los segmentos de audiencia autenticados es naturalmente menor que el alcance de los segmentos basados en cookies y que el uso de opciones de segmentación adicionales reduce aún más el alcance. Sea prudente a la hora de utilizar la segmentación granular, especialmente uniendo varios objetivos con instrucciones Y.

## Causas de variaciones de datos entre ID de correo electrónico e ID universales {#universal-ids-data-variances}

Existen dos razones para la variación de los ID de correo electrónico con hash traducidos a [!DNL RampIDs]:

* DSP Cuando varios perfiles utilizan el mismo ID de correo electrónico, el recuento de segmentos de puede ser inferior al recuento de perfiles de la plataforma de datos del cliente. Por ejemplo, en Adobe Photoshop puede crear una cuenta de empresa y una cuenta personal con un solo ID de correo electrónico. Pero si ambos perfiles pertenecen al mismo segmento, los perfiles se asignan a un ID de correo electrónico y, en consecuencia, a uno [!DNL RampID].

* A [!DNL RampID] se puede actualizar a un nuevo valor. If [!DNL LiveRamp] no reconoce un ID de correo electrónico o no puede asignarlo a un existente [!DNL RampID] en su base de datos, a continuación, asigna un nuevo [!DNL RampID] al ID de correo electrónico. En el futuro, cuándo podrán asignar el ID de correo electrónico a otro [!DNL RampID] o pueden recopilar más información sobre el mismo ID de correo electrónico, actualizan el [!DNL RampID] a un nuevo valor. [!DNL LiveRamp] hace referencia a esta acción como una actualización de un &quot;derivado&quot; [!DNL RampID] a un &quot;mantenido&quot; [!DNL RampID]. DSP Sin embargo, no se obtienen asignaciones entre las asignaciones derivadas y las mantenidas [!DNL RampIDs] DSP y, por lo tanto, no se puede eliminar la versión anterior de RampID del segmento de. En este caso, el recuento de segmentos puede ser mayor que el recuento de perfiles.

  Ejemplo: Un usuario inicia sesión en [!DNL Adobe] y visite la página de Photoshop. If [!DNL LiveRamp] no tiene información existente sobre el ID de correo electrónico y, a continuación, lo asignan a un derivado [!DNL RampID], diga D123. Quince días después, el usuario visita la misma página, pero [!DNL LiveRamp] ha actualizado el [!DNL RampID] durante esos 15 días y ha reasignado el [!DNL RampID] a M123. A pesar de que el segmento &quot;Photoshop DSP Enthusiast&quot; de la plataforma de datos del cliente solo tiene un ID de correo electrónico para el usuario, el segmento de la tiene dos RampID: D123 y M123.

## Resolución de problemas

Si no ve los recuentos de usuarios o los tamaños de audiencia son bajos, compruebe lo siguiente:

* Si utiliza [!DNL Flashtalking] o [!DNL Google Campaign Manager 360] anuncios y, a continuación, asegúrese de que las direcciones URL de pulsaciones de sus anuncios se adjuntan con las macros correctas. Consulte las macros de [[!DNL Flashtalking] anuncios](/help/integrations/analytics/macros-flashtalking.md) y [[!DNL Google Campaign Manager 360] anuncios](/help/integrations/analytics/macros-google-campaign-manager.md).

* Asegúrese de que el código correcto y universal de ID específico del socio esté implementado en el sitio web para que coincida con los eventos en el sitio y la exposición de anuncios. Trabaje con su [!DNL LiveRamp] o [!DNL ID5] representativo según sea necesario.

* (Para [!DNL RampIDs] y [!DNL UID 2.0] ID) Asegúrese de que sus [DSP La fuente de datos de la está configurada correctamente](/help/dsp/audiences/sources/source-settings.md)y que los recuentos de usuarios se rellenen para los segmentos de audiencia generados.

* Si su alcance es menor de lo esperado, compruebe que la lógica del segmento de audiencia no sea demasiado granular.

Si no puede resolver el problema, póngase en contacto con el equipo de cuenta de Adobe.

>[!MORELIKETHIS]
>
>* [Crear una fuente de audiencia para activar audiencias de ID universal](/help/dsp/audiences/sources/source-create.md)
>* [Conversión de ID de usuario [!DNL Adobe Real-Time CDP] a los ID universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Conversión de ID de usuario [!DNL Tealium] a los ID universales](/help/dsp/audiences/sources/source-tealium.md)
>* [Creación e implementación de un segmento personalizado](/help/dsp/audiences/custom-segment-create.md)
>* [Importar manualmente segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
