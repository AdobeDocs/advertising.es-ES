---
title: Implementar  [!DNL Google Ads] conversiones mejoradas para clientes potenciales
description: Obtenga información acerca del flujo de trabajo para configurar  [!DNL Google Ads] conversiones mejoradas para posibles clientes.
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
source-git-commit: 56161ece4ba9c01cddb86e16796150c391f1a811
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---

# Implementar [!DNL Google Ads] conversiones mejoradas para posibles clientes

*[!DNL Google Ads]solo cuentas*

[[!DNL Google Ads] las conversiones mejoradas para posibles clientes](https://support.google.com/google-ads/answer/9888656) le permiten asignar usuarios a conversiones sin conexión mediante los datos de conversión de origen. Utilice conversiones mejoradas para posibles clientes en entornos en los que los ID de clic no están disponibles, como para rastrear ventas por teléfono o correo electrónico resultantes de posibles clientes en sitios web.

En Buscar, Social y Commerce, puede:

* Vea las conversiones mejoradas existentes para posibles clientes.

  Search, Social y Commerce sincronizan sus conversiones mejoradas existentes para posibles clientes diariamente a las 05:00 en el huso horario del anunciante.

* Cree conversiones mejoradas para posibles clientes.

* Cargue datos de conversión de origen y sin conexión para asignarlos a sus conversiones mejoradas para posibles clientes.

* Incluya sus conversiones mejoradas para posibles clientes como métricas dentro de los informes y como métricas ponderadas dentro de los objetivos de optimización.

Para utilizar esta función, complete los siguientes pasos. Los pasos para crear etiquetas de seguimiento de conversión y para crear acciones de conversión se pueden invertir de forma opcional.

1. En [!DNL Google Ads], adherirse a las conversiones mejoradas para posibles clientes:

   1. Abra la configuración de conversión de la cuenta.

   1. Seleccione la opción para mejorar las conversiones de los posibles clientes y aceptar los términos de servicio.

   1. Seleccione si desea usar una etiqueta [!DNL Google] o [!DNL Google Tag Manager] para crear la etiqueta de conversión.


1. Configure e implemente una etiqueta [!DNL Google] para la acción de conversión.

   Para obtener instrucciones, consulte la ayuda de [!DNL Google Ads] para crear etiquetas para las conversiones mejoradas de posibles clientes [mediante una [!DNL Google] etiqueta](https://support.google.com/google-ads/answer/11021502) o [mediante [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292).

1. Cree una acción de conversión para la conversión mejorada de posibles clientes en [Search, Social y Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) o en [Google Ads](https://support.google.com/google-ads/answer/12216226).

   Para el **tipo de conversión,** seleccione *Importar conversión* o *Importar.*

1. Siempre que sea necesario, cargue datos de origen, incluidas direcciones de correo electrónico con hash o números de teléfono, para atribuirlos a la conversión de una cuenta especificada. Puede completar este paso desde [Search, Social y Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) o desde [!DNL Google Data Manager].

   * En Search, Social y Commerce, puede descargar una plantilla en formato [!DNL Microsoft Excel], escribir los datos de conversión y guardar el archivo localmente y, a continuación, cargar el archivo editado. La plantilla incluye columnas para indicar si se dio el consentimiento del usuario para cargar datos en [!DNL Google] con fines publicitarios y de personalización de anuncios.

     Todos los datos cargados se sincronizan en tiempo real con [!DNL Google Ads].

   * Para obtener más información sobre cómo cargar datos mediante [!DNL Google Data Manager], consulte &quot;[Acerca del administrador de datos](https://support.google.com/google-ads/answer/14639041)&quot;.

>[!MORELIKETHIS]
>
>* [Crear una acción de conversión para una  [!DNL Google Ads] conversión mejorada para posibles clientes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Cargar datos de conversión sin conexión para conversiones mejoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
