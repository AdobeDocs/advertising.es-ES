---
title: Compatibilidad con la activación de ID universales
description: Obtenga más información sobre la compatibilidad para importar segmentos de ID universales, crear segmentos personalizados para realizar un seguimiento de ID universales y convertir otros identificadores de usuario en sus segmentos de origen a ID universales para direccionamiento sin cookies.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: ea50b94ebc6d27fda9c0bd9f61da16750fa58f83
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# Compatibilidad con la activación de ID universales

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta función*

DSP admite identificadores universales basados en personas para direccionamiento sin cookies, de un solo dispositivos (no de dispositivos cruzada) en formatos digitales compatibles con DSP.

* Puede enviar manualmente su [[!DNL LiveRamp] [!DNL RampIDs]] autenticado directamente a DSP utilizando el [!DNL LiveRamp] [!DNL Connect] panel. Consulte &quot;[T Importar segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)&quot;

* DSP puede ingerir sus segmentos de origen compuestos por ID de correo electrónico con hash creados dentro de su plataforma de datos del cliente (CDP) y convertir a ellos e [!DNL LiveRamp] [!DNL RampIDs] [!DNL Unified ID 2.0 (UID2.0)] ID. Para obtener más información sobre las plataformas de datos de clientes admitidas, las funciones disponibles para cada tipo de ID universal admitido y los flujos de trabajo relacionados, consulte &quot;[Acerca de los orígenes](/help/dsp/audiences/sources/source-about.md) de audiencia de origen&quot;.

* Puede crear segmentos personalizados que realicen un seguimiento de los usuarios asociados con ID universales ID5 que están expuestos a anuncios de dispositivos escritorio y móviles y que visita páginas web específicas. ID5 utiliza un modelo probabilístico para asignar un ID derivado de varias señales de usuario y señales explorador. Para obtener instrucciones, consulte &quot;[Crear e implementar un segmento](/help/dsp/audiences/custom-segment-create.md) personalizado&quot;.

* Los segmentos de terceros de algunos proveedores pueden incluir automáticamente ID universales además de usuarios rastreados por cookies o ID dispositivos. Por ejemplo, los segmentos de [!DNL Eyeota] pueden incluir automáticamente ID de ID5 y los segmentos de pueden incluir ID de [!DNL Lotame] UID2.0. Los detalles segmento incluyen el tamaño para cada tipo. Se aplica la tarifa de uso habitual para cada segmento, que se indica junto al nombre segmento; no se cobran tarifas adicionales por los ID ID5.

## Informes por tipo de ID universal

* **Informes personalizados** : los datos de costo, impresión, clics, Conversión y Frecuencia por tipo de ID universal están disponibles en los informes personalizados.

* **[!DNL Analytics]Informes:** Los anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) los que han implementado todos los pasos necesarios pueden ver las conversiones de vista pulsaciones por tipo de ID universal en [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Para obtener una Conversión atribución adecuada, asegúrese de que las URL de clics de sus anuncios incluyan tanto el EF ID como el [AMO ID.](/help/integrations/analytics/ids.md)

* **Detalles del segmento:** para todos los tipos de segmento, los detalles segmento incluyen el tamaño audiencia por tipo de ID universal y por el tipo de dispositivo rastreado por cookies o ID de dispositivos.

## Cómo Target una audiencia de ID universal en las ubicaciones

>[!NOTE]
>
>No puede cambiar los tipos de ID de destino en un ubicación activo. Si es necesario, puede duplicado un ubicación activo y cambiar los tipos de ID de destino en el nuevo ubicación.

En una ubicación nueva, programada o pausada, realice lo siguiente:

1. En la [!UICONTROL Geo-Targeting] sección, especifique las zonas geográficas a las que desea destino. Cada socio de ID universal permite usuario direccionamiento solo en áreas geográficas específicas, y solo los tipos de identificación elegibles están disponibles en la [!UICONTROL Targeting] configuración.

1. En la [!UICONTROL Audience Targeting] sección, haga lo siguiente:

   1. En la [!UICONTROL Included Audiences] configuración, seleccione la segmento para la cual usuario datos se convirtieron en ID universales.

      Puede incluir segmentos adicionales si lo desea.

   1. En la [!UICONTROL Targeting] configuración:

      1. Seleccione el tipo de ID universal que desea destino.

         El ajuste incluye las opciones &quot;[!UICONTROL Legacy IDs]&quot; y &quot;[!UICONTROL Universal ID],&quot; que pueden incluir las subopciones &quot;[!UICONTROL ID5],&quot;[!UICONTROL RampID] &quot;,&quot; y &quot;[!UICONTROL Unified ID2.0].&quot; Los objetivos geográficos seleccionados determinan las subopciones disponibles.

         Puede seleccionar tanto &quot;[!UICONTROL Legacy IDs]&quot; como &quot;[!UICONTROL Universal ID],&quot; pero solo puede seleccionar un tipo de ID universal por ubicación. Al seleccionar tanto los ID heredados como los ID universales, se otorga preferencia de oferta a los ID universales.

      1. (Si es necesario) Acepte las condiciones del contrato de servicio para el uso de ID universales.

         Para poder convertir datos a un nuevo tipo de ID, un usuario del DSP cuenta debe aceptar las condiciones del contrato de servicio. Los términos deben aceptarse solo una vez por tipo de ID y por cuenta.

Consulte &quot;[Ubicación Configuración](/help/dsp/campaign-management/placements/placement-settings.md)&quot;.

## Prácticas recomendadas para pruebas y validación de datos

Utilice las siguientes prácticas recomendadas para [!DNL RampID]los segmentos basados en --y los segmentos basados en ID5, para los que está disponible la medición Adobe Analytics.

* Aproximadamente 24 horas después de activar un segmento, verifique el recuento de ID convertidos para el segmento dentro de [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Si el recuento de ID es inesperado, póngase en contacto con su equipo de cuentas de Adobe Systems.

  Consulte &quot;[Causas de las variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot; para obtener más información sobre cómo pueden variar los recuentos de segmento.

* No cambie sus paquetes y ubicaciones existentes. Sin embargo, si no tiene ningún presupuesto adicional para prueba identificaciones universales, reduzca los presupuestos originales para financiar las pruebas.

* Copie sus paquetes y ubicaciones originales, ajuste los presupuestos en función del tamaño del prueba, cambie las audiencias para usar [!DNL RampID]segmentos basados en -(para usuarios autenticados) o segmentos basados en ID5 (para usuarios no autenticados) y verifique que los nuevos paquetes y ubicaciones gasten todos sus presupuestos.

   * Para comparar el rendimiento de los segmentos basados en ID universales con el rendimiento de las colocaciones direccionamiento otros identificadores audiencia, como cookies o ID de publicidad móvil, cree una campaña con una ubicación basada en ID universal independiente y una ubicación basada en ID heredados.

     Para un prueba de retargeting completo, destino tanto RampIDs para usuarios autenticados como ID5s para usuarios no autenticados.

     Obtener el mejor rendimiento no debería ser la comparación principal. En su lugar, determine qué ID se escalan bien, lo que podría servir de base para la optimización y las asignaciones presupuestarias más adelante. El objetivo a largo plazo es compensar las impresiones y tráfico del sitio perdidas cuando las cookies están en desuso.

   * Para comparar el alcance total de explorador, destino segmentos basados en ID universales y segmentos basados en ID heredados de la misma ubicación. Utilice la misma configuración de campaña que en el caso de uso anterior, excepto que no es necesario dividir el presupuesto campaña.

     Se da preferencia de oferta a los ID universales, pero los ID heredados reciben ofertas cuando los ID universales no están disponibles. Asegúrese de comparar el alcance en diferentes exploradores (incluidos Cromo, Safari y Mozilla).

     >[!NOTE]
     >
     >La limitación de frecuencia se aplica a un ID individual. Cuando una usuario tiene varios tipos de ID, es posible que alcance esa usuario más de lo esperado.

* Recuerde que el alcance de los segmentos de audiencia autenticados es naturalmente menor que el alcance de los segmentos basados en cookie, y que el uso de opciones de direccionamiento adicionales reduce aún más su alcance. Sea prudente al utilizar direccionamiento granulares, especialmente uniendo varios objetivos con instrucciones AND.

## Causas de las variaciones de datos entre los ID de correo electrónico y los ID universales {#universal-ids-data-variances}

* ID de correo electrónico con hash traducidos a ID ID5:

  El modelo probabilístico tiene un variación de error de +/- 5%. Esto significa que puede sobreestimar o subestimar el recuento de audiencia en un 5%.

* Los ID de correo electrónico con hash traducidos a [!DNL RampIDs]:

   * Cuando varios perfiles utilizan el mismo ID de correo electrónico, el recuento de DSP segmento puede ser inferior al recuento de perfil dentro de la plataforma de datos del cliente. Por ejemplo, en Adobe Photoshop puede crear una compañía cuenta y una cuenta personal utilizando un único ID correo electrónico. Pero si ambos perfiles pertenecen a la misma persona, entonces los perfiles se asignan a un ID correo electrónico y correspondientemente a uno [!DNL RampID].

   * A [!DNL RampID] se puede actualizar a un nuevo valor. Si [!DNL LiveRamp] no reconoce un ID de correo electrónico o no puede asignarlo a uno existente [!DNL RampID] en su base de datos, asigna un ID nuevo [!DNL RampID] al correo electrónico. En el futuro, cuando puedan asignar el ID de correo electrónico a otro [!DNL RampID] o puedan recopilar más información sobre el mismo ID de correo electrónico, actualizarán el [!DNL RampID] valor a un nuevo valor. [!DNL LiveRamp]se refiere a esta acción como la actualización de un &quot;derivado&quot; [!DNL RampID] a un &quot;mantenido&quot;. [!DNL RampID] Sin embargo, DSP no obtiene asignaciones entre derivadas y mantenidas [!DNL RampIDs] y, por lo tanto, no puede eliminar la versión anterior del RampID del DSP segmento. En este caso, el recuento de segmento puede ser mayor que el recuento de perfil.

     Ejemplo: un usuario inicia sesión en el [!DNL Adobe] sitio web y visita el Photoshop Página. Si [!DNL LiveRamp] no tiene ninguna información existente sobre el ID de correo electrónico, entonces le asignan un derivado [!DNL RampID], digamos D123. Quince días después, el usuario visita el mismo Página, pero [!DNL LiveRamp] ha actualizado el [!DNL RampID] durante esos 15 días y ha reasignado el [!DNL RampID] M123. Aunque el segmento &quot;Photoshop entusiasta&quot; de la plataforma de datos del cliente solo tiene un ID de correo electrónico para el usuario, el DSP segmento tiene dos RampID: D123 y M123.

## Resolución de problemas

Si no ves usuario recuentos, o si tus tallas de audiencia son bajas, comprueba lo siguiente:

* Si utiliza [!DNL Flashtalking] anuncios [!DNL Google Campaign Manager 360] , asegúrese de que las URL de clics de sus anuncios estén anexadas con las macros correctas. Consulte las macros de [[!DNL Flashtalking] anuncios](/help/integrations/analytics/macros-flashtalking.md) y [[!DNL Google Campaign Manager 360] publicidades](/help/integrations/analytics/macros-google-campaign-manager.md).

* Asegúrese de que se implemente el código correcto y universal socio específico del  en su sitio web para que coincida con los eventos in situ y las exposiciones anuncios. Trabaje con su representante o [!DNL ID5] con su [!DNL LiveRamp] representante según sea necesario.

* (Para [!DNL RampIDs] e [!DNL UID 2.0] ID) Asegúrese de que la [DSP fuente de datos esté configurada correctamente](/help/dsp/audiences/sources/source-manage.md#source-settings) y de que los recuentos de usuario estén completados para los segmentos de audiencia generados.

* Si su alcance es menor de lo que espera, compruebe que la lógica de segmento de audiencia no sea demasiado granular.

* Asegúrese de que la configuración de campaña, paquete y ubicación sean correctas.<!-- wording-->

Si no puede resolver el problema, póngase en contacto con su equipo de cuentas de Adobe Systems.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia propia](/help/dsp/audiences/sources/source-about.md)
>* [Administrar orígenes de audiencia para activar el Audiences de ID universal](/help/dsp/audiences/sources/source-manage.md)
>* [Crear e implementar un segmento personalizado](/help/dsp/audiences/custom-segment-create.md)
>* [Importar manualmente los segmentos autenticados de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Acerca de la gestión de público](/help/dsp/audiences/audience-about.md)
>* [Configuración de colocación](/help/dsp/campaign-management/placements/placement-settings.md)
