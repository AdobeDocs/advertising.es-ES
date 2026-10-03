---
title: Implementar [!DNL Microsoft Advertising] conversiones mejoradas para conversiones sin conexión
description: Obtenga información acerca del flujo de trabajo para configurar [!DNL Microsoft Advertising] conversiones mejoradas para conversiones sin conexión.
feature: Search Campaign Management, Conversions
exl-id: 44937db7-9e80-4a5d-85c7-5bd5febc3b96
TQID: 'https://experienceleague.adobe.com/GLFczqDqV8HE5hUZt8ORAlQMNy4OqQTtMdaHoYoN10U'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
    internal-label: Conversions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%
---
# Implementar [!DNL Microsoft Advertising] conversiones mejoradas para conversiones sin conexión

*[!DNL Microsoft Advertising]solo cuentas*

[[!DNL Microsoft Advertising] conversiones mejoradas](https://help.ads.microsoft.com/#apex/ads/en/60178) le permiten asignar usuarios a conversiones sin conexión mediante sus datos de conversión de origen. Utilice conversiones mejoradas en entornos en los que los ID de clic no están disponibles, como para rastrear las ventas por teléfono o correo electrónico resultantes de los posibles clientes del sitio web.

En Buscar, Social y Commerce, puede:

* Vea sus conversiones mejoradas existentes para conversiones sin conexión.

  Search, Social y Commerce sincronizan sus conversiones mejoradas existentes diariamente a las 05:00 en el huso horario del anunciante.

* Cargue datos de conversión de origen y sin conexión para asignarlos a sus objetivos de conversión mejorados existentes.

* Incluya sus conversiones mejoradas como métricas dentro de los informes y como métricas ponderadas dentro de los objetivos de optimización.

Para utilizar esta función, complete los siguientes pasos.

1. Siga todos los requisitos previos de la ayuda de [!DNL Microsoft Advertising] sobre &quot;[conversiones mejoradas](https://help.ads.microsoft.com/#apex/ads/en/60178)&quot;.

1. [Configurar un objetivo de conversión mejorado en [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178).

1. Siempre que sea necesario, cargue datos de origen, incluidas direcciones de correo electrónico con hash o números de teléfono, para atribuirlos a la conversión de una cuenta especificada. Puede completar este paso en [Search, Social y Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) o en [!DNL Microsoft Advertising].

   * En Search, Social y Commerce, puede descargar una plantilla en formato [!DNL Microsoft Excel], escribir los datos de conversión y guardar el archivo localmente y, a continuación, cargar el archivo editado.

     Todos los datos cargados se sincronizan en tiempo real con [!DNL Microsoft Advertising].

   * Para obtener más información sobre cómo cargar datos en [!DNL Microsoft Advertising], consulte la sección &quot;Configurar conversiones mejoradas para conversiones sin conexión&quot; en la ayuda de [!DNL Microsoft Advertising] sobre &quot;[conversiones mejoradas](https://help.ads.microsoft.com/#apex/ads/en/60178)&quot;.

>[!MORELIKETHIS]
>
>* [Cargar datos de conversión sin conexión para conversiones mejoradas](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
