---
title: Compatibilidad con la activación de ID universales
description: Obtenga información acerca de la compatibilidad para importar segmentos de ID universales, crear segmentos personalizados para rastrear ID universales y convertir otros identificadores de usuario en segmentos de origen a ID universales para una segmentación sin cookies.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Compatibilidad con la activación de ID universales

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*característica de Beta*

DSP DSP La compatibilidad con ID universales y basados en personas para la segmentación sin cookies de un solo dispositivo (no entre dispositivos) en los formatos digitales admitidos por la aplicación de la.

* DSP Puede enviar manualmente su [[!DNL LiveRamp] [!DNL RampIDs]] autenticado directamente a mediante el panel de [!DNL LiveRamp] [!DNL Connect] a la dirección de correo electrónico de su cuenta de correo electrónico. Consulte &quot;[Importar manualmente segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)&quot;.

* DSP Puede ingerir segmentos de origen compuestos de ID de correo electrónico con hash creados dentro de su plataforma de datos del cliente (CDP) y convertirlos en [!DNL LiveRamp] ID de [!DNL RampIDs] y [!DNL Unified ID 2.0 (UID2.0)]. Para obtener más información acerca de las plataformas de datos de clientes compatibles, las características disponibles para cada tipo de identificador universal compatible y los flujos de trabajo relacionados, consulte &quot;[Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)&quot;.

* Puede crear segmentos personalizados que hagan un seguimiento de los usuarios asociados con los ID universales ID5 que están expuestos a anuncios de dispositivos de escritorio y móviles y que visitan páginas web específicas. ID5 utiliza un modelo probabilístico para asignar un ID derivado de varias señales de usuario y señales de explorador. Para obtener instrucciones, consulte &quot;[Crear e implementar un segmento personalizado](/help/dsp/audiences/custom-segment-create.md)&quot;.

* Los segmentos de terceros de algunos proveedores pueden incluir automáticamente ID universales, además de los usuarios rastreados mediante cookies o ID de dispositivo. Por ejemplo, los segmentos de [!DNL Eyeota] pueden incluir automáticamente ID5, y los segmentos de [!DNL Lotame] pueden incluir ID2.0. Los detalles del segmento incluyen el tamaño de cada tipo. Se aplica la tarifa de uso habitual para cada segmento, que se indica junto al nombre del segmento; no se cobran tarifas adicionales por los ID5.

## Creación de informes por tipo de ID universal

* **Informes personalizados:** Los datos de costo, impresión, clics, conversión y frecuencia por tipo de identificador universal están disponibles en los informes personalizados.

* **[!DNL Analytics]informes:** Los anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) que hayan implementado todos los pasos necesarios pueden ver las conversiones de visualización por tipo de identificador universal en [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Para la atribución de conversión adecuada, asegúrate de que las URL de pulsaciones de tus anuncios incluyan tanto el [EF ID como el AMO ID](/help/integrations/analytics/ids.md).

* **Detalles del segmento:** Para todos los tipos de segmento, los detalles del segmento incluyen el tamaño de audiencia por tipo de identificador universal y por el tipo de dispositivo rastreado mediante cookies o ID de dispositivo.

## Cómo segmentar una audiencia de ID universal en sus ubicaciones

>[!NOTE]
>
>No puede cambiar los tipos de ID de destino en una ubicación activa. Si es necesario, puede duplicar una ubicación activa y cambiar los tipos de ID de destino en la nueva ubicación.

En una ubicación nueva, programada o en pausa, haga lo siguiente:

1. En la sección [!UICONTROL Geo-Targeting], especifique las áreas geográficas de destino. Cada socio de ID universal permite la segmentación de usuarios solamente en áreas geográficas específicas y solo los tipos de ID elegibles están disponibles en la configuración de [!UICONTROL Targeting].

1. En la sección [!UICONTROL Audience Targeting], haga lo siguiente:

   1. En la configuración [!UICONTROL Included Audiences], seleccione el segmento para el cual los datos de usuario se convirtieron en ID universales.

      Si lo desea, puede incluir segmentos adicionales.

   1. En la configuración de [!UICONTROL Targeting]:

      1. Seleccione el tipo de ID universal de destino.

         La configuración incluye las opciones &quot;[!UICONTROL Legacy IDs]&quot; y &quot;[!UICONTROL Universal ID]&quot;, que pueden incluir las subopciones &quot;[!UICONTROL ID5]&quot;, &quot;[!UICONTROL RampID]&quot; y &quot;[!UICONTROL Unified ID2.0]&quot;.&quot; Los destinos geográficos seleccionados determinan las subopciones disponibles.

         Puede seleccionar &quot;[!UICONTROL Legacy IDs]&quot; y &quot;[!UICONTROL Universal ID]&quot;, pero solo puede seleccionar un tipo de identificador universal por ubicación. Al seleccionar ID heredados e ID universales, se da preferencia de oferta a los ID universales.

      1. (Si es necesario) Acepte el contrato de términos de servicio para el uso de ID universales.

         DSP Para poder convertir datos a un nuevo tipo de ID, un usuario de la cuenta de la cuenta de la cuenta de la cuenta de la cuenta de debe aceptar los términos del contrato de servicio de. Los términos deben aceptarse solo una vez por tipo de ID, por cuenta.

Consulte &quot;[Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)&quot;.

## Prácticas recomendadas para pruebas y validación de datos

Siga estas prácticas recomendadas para segmentos basados en [!DNL RampID] y en ID5, para los que está disponible la medición de Adobe Analytics.

* Unas 24 horas después de activar un segmento, compruebe el recuento de ID convertidos para el segmento en [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Si el recuento de ID es inesperado, póngase en contacto con el equipo de cuenta de Adobe.

  Consulte &quot;[Variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot; para obtener más información sobre cómo pueden variar los recuentos de segmentos.

* No cambie los paquetes y las ubicaciones existentes. Sin embargo, si no tiene ningún presupuesto incremental para probar los ID universales, reduzca los presupuestos originales para financiar las pruebas.

* Copie los paquetes y las ubicaciones originales, ajuste los presupuestos según el tamaño de la prueba, cambie las audiencias para que utilicen segmentos basados en [!DNL RampID] (para usuarios autenticados) o segmentos basados en ID5 (para usuarios no autenticados) y compruebe que los nuevos paquetes y ubicaciones gastan sus presupuestos completos.

   * Para comparar el rendimiento de los segmentos basados en ID universales con el de las ubicaciones dirigidas a otros identificadores de audiencia, como, por ejemplo, cookies o ID de publicidad móvil, cree una campaña con una ubicación basada en ID universal y una ubicación basada en ID heredados.

     Para una prueba de retargeting completa, establezca como objetivo RampID para usuarios autenticados e ID5s para usuarios no autenticados.

     Obtener el mejor rendimiento no debería ser la comparación principal. En su lugar, determine qué ID se adaptan bien, lo que podría informar la optimización y las asignaciones presupuestarias más adelante. El objetivo a largo plazo es compensar las impresiones perdidas y el tráfico del sitio cuando las cookies están en desuso.

   * Para comparar el alcance total del explorador, establezca como objetivo segmentos universales basados en ID y segmentos heredados basados en ID en la misma ubicación. Utilice la misma configuración de campaña que el caso de uso anterior, excepto que no es necesario dividir el presupuesto de la campaña.

     La preferencia de oferta se da a los ID universales, pero los ID heredados reciben ofertas cuando los ID universales no están disponibles. Asegúrese de comparar el alcance en distintos navegadores (incluidos Chrome, Safari y Mozilla).

     >[!NOTE]
     >
     >La restricción de frecuencia se aplica a un ID individual. Cuando un usuario tiene varios tipos de ID, es posible que llegue a ese usuario más de lo esperado.

* Recuerde que el alcance de los segmentos de audiencia autenticados es naturalmente menor que el alcance de los segmentos basados en cookies y que el uso de opciones de segmentación adicionales reduce aún más el alcance. Sea prudente a la hora de utilizar la segmentación granular, especialmente uniendo varios objetivos con instrucciones Y.

## Variaciones de datos entre ID de correo electrónico e ID universales {#universal-ids-data-variances}

### Niveles de variación aceptables

La tasa de traducción de las direcciones de correo electrónico con hash a los identificadores universales debe ser superior al 90%; la tasa de traducción de [!DNL RampIDs] en particular debe ser del 95% si todas las direcciones de correo electrónico con hash son únicas. Por ejemplo, si envía 100 direcciones de correo electrónico con hash desde la plataforma de datos del cliente, deben traducirse al menos a 95 [!DNL RampIDs] o más de 90 tipos más de ID universales. Una tasa de traducción más baja puede indicar un problema. Consulte &quot;[Causas de variación](#universal-ids-data-variances-causes&quot; para obtener posibles explicaciones.

Para [!DNL RampIDs], póngase en contacto con el equipo de la cuenta de Adobe para obtener más información si las tasas de traducción son inferiores al 70 %.

### Causas de variación {#universal-ids-data-variances-causes}

* ID de correo electrónico con hash traducidos a ID5:

  El modelo probabilístico tiene una varianza de error de +/- 5 %. Esto significa que puede sobrestimar o subestimar el recuento de audiencias en un 5 %.

* ID de correo electrónico con hash traducidos a [!DNL RampIDs]:

   * DSP Cuando varios perfiles utilizan el mismo ID de correo electrónico, el recuento de segmentos de puede ser inferior al recuento de perfiles de la plataforma de datos del cliente. Por ejemplo, en Adobe Photoshop puede crear una cuenta de empresa y una cuenta personal con un solo ID de correo electrónico. Pero si ambos perfiles pertenecen a la misma persona, los perfiles se asignan a un ID de correo electrónico y, en consecuencia, a un [!DNL RampID].

   * Un(a) [!DNL RampID] se puede actualizar a un nuevo valor. Si [!DNL LiveRamp] no reconoce un ID de correo electrónico o no puede asignarlo a un [!DNL RampID] existente en su base de datos, asigna un nuevo [!DNL RampID] al ID de correo electrónico. En el futuro, cuando puedan asignar el ID de correo electrónico a otro [!DNL RampID] o puedan recopilar más información sobre el mismo ID de correo electrónico, actualizarán [!DNL RampID] a un nuevo valor. [!DNL LiveRamp] se refiere a esta acción como una actualización de un [!DNL RampID] &quot;derivado&quot; a un [!DNL RampID] &quot;mantenido&quot;. DSP DSP Sin embargo, no se obtienen asignaciones entre [!DNL RampIDs] derivadas y mantenidas, por lo que no se puede quitar la versión anterior de RampID del segmento de la. En este caso, el recuento de segmentos puede ser mayor que el recuento de perfiles.

     Ejemplo: Un usuario inicia sesión en el sitio web de [!DNL Adobe] y visita la página de Photoshop. Si [!DNL LiveRamp] no tiene información existente sobre el ID de correo electrónico, entonces le asignan un [!DNL RampID] derivado, por ejemplo, D123. Quince días después, el usuario visita la misma página, pero [!DNL LiveRamp] ha actualizado [!DNL RampID] durante esos 15 días y ha reasignado [!DNL RampID] a M123. A pesar de que el segmento &quot;Photoshop DSP Enthusiast&quot; de la plataforma de datos del cliente solo tiene un ID de correo electrónico para el usuario, el segmento de la tiene dos RampID: D123 y M123.

## Resolución de problemas

Si no ve los recuentos de usuarios o si los tamaños de audiencia son bajos, compruebe lo siguiente:

* Si usa anuncios de [!DNL Flashtalking] o [!DNL Google Campaign Manager 360], asegúrese de que las direcciones URL de pulsaciones de sus anuncios se adjunten con las macros correctas. Ver las macros de [[!DNL Flashtalking] anuncios](/help/integrations/analytics/macros-flashtalking.md) y [[!DNL Google Campaign Manager 360] anuncios](/help/integrations/analytics/macros-google-campaign-manager.md).

* Asegúrese de que el código correcto y universal de ID específico del socio esté implementado en el sitio web para que coincida con los eventos en el sitio y la exposición de anuncios. Trabaje con su representante de [!DNL LiveRamp] o [!DNL ID5] según sea necesario.

* DSP (Para los identificadores de [!DNL RampIDs] y [!DNL UID 2.0]) Asegúrese de que la fuente de datos de [está configurada correctamente](/help/dsp/audiences/sources/source-manage.md#source-settings) y de que los recuentos de usuarios se rellenan para los segmentos de audiencia generados.

* Si su alcance es menor de lo esperado, compruebe que la lógica del segmento de audiencia no sea demasiado granular.

* Asegúrese de que la configuración de la campaña, el paquete y la ubicación sea correcta.<!-- wording-->

Si no puede resolver el problema, póngase en contacto con el equipo de cuenta de Adobe.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](/help/dsp/audiences/sources/source-manage.md)
>* [Crear e implementar un segmento personalizado](/help/dsp/audiences/custom-segment-create.md)
>* [Importar segmentos autenticados manualmente desde [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
>* [Configuración de ubicación](/help/dsp/campaign-management/placements/placement-settings.md)
