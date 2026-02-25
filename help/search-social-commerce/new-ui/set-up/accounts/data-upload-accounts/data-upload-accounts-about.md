---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Acerca de la carga de datos de cuenta para informes y simulaciones

<!-- Move all related files into one page? -->

Si utiliza redes de publicidad en línea para las que Search, Social y Commerce no admiten la API, puede cargar contenido de la campaña y datos de coste, clics y conversión sin conexión en una cuenta para realizar simulaciones de informes y rendimiento. Los anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md) también pueden ver los datos de sus cuentas en Adobe Analytics.

Esta función está disponible para redes de anuncios que siguen la estructura de campaña estándar de tres niveles (campaña, grupo de anuncios o conjunto de anuncios y unidad de oferta (anuncio o palabra clave)). Para Adobe DSP, la función está disponible para paquetes y las ubicaciones asignadas a un paquete, pero no para campañas ni ubicaciones con un ritmo de nivel de ubicación.

La compatibilidad predeterminada está disponible para las siguientes redes: <!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

El rastreo de clics de Search, Social y Commerce y el seguimiento de conversiones de Adobe Advertising no son compatibles con esta función.

## Funcionalidad disponible en Search, Social y Commerce

* Seguimiento y creación de informes:

   * Componentes de campaña de solo lectura hasta el nivel de unidad de oferta en las vistas de administración de campañas.

   * Datos de rendimiento hasta el nivel de grupo de anuncios <!-- verify the entity level --> en las vistas de administración de campañas e informes personalizados. Los anunciantes con [!DNL Adobe Analytics for Advertising]) también obtienen datos de rendimiento hasta el nivel de grupo de anuncios <!-- verify the entity level --> dentro de los grupos de informes de Adobe Analytics especificados para el anunciante.&lt;!— Comprobar si los tipos de datos son limitados: ¿coste, clic, impresión de visualización, ingresos? —>

* Simulaciones de rendimiento al agregar las campañas a un portafolio.<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  Search, Social y Commerce no optimizan nada, ni siquiera colocan ofertas, para este tipo de campañas dentro de un portafolio.

## Flujo de trabajo para configurar cuentas sin conexión

<!-- subtitle wording? -->

1. [Configurar un registro de cuenta ficticia](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md).

1. Cree un archivo de datos para una sola cuenta <!--  in what file format? -->, incluido el estado en el nivel de día para campañas, grupos de anuncios y anuncios.

Los datos deben cumplir los requisitos de datos de la red de publicidad, por lo que los campos de datos de cada entidad pueden variar según la red de publicidad.

1. &#x200B;<!-- For all ad networks (excluding DSP), -->Cargue los datos iniciales de una sola cuenta de cualquiera de las siguientes maneras:

* Cargue un archivo manualmente desde el dispositivo o la red.

* Cargue los datos en una carpeta asignada por Search, Social y Commerce en un bloque de [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]).

  >[!PREREQUISITES]
  >
  >* Póngase en contacto con el equipo de su cuenta de Adobe para habilitar las cargas de datos de la cuenta para su cuenta de anunciante de Search, Social y Commerce. El equipo facilitará la creación de una carpeta específica de la organización en un bloque de [!DNL S3] y le informará cuando se haya completado.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* Recupere la ruta de almacenamiento en la nube [!DNL S3], el identificador de clave de acceso y la clave de acceso secreta de su cuenta. Se usan el mismo identificador de clave de acceso y clave de acceso secreta en todas las cuentas de carga de datos de la organización <!-- naming convention?-->.

1. Continúe cargando nuevos archivos de datos diariamente.

1. Una vez que hayas cargado datos durante 30 días, puedes, opcionalmente, añadir las campañas a <!--what type? how should we refer to them? --> portafolios y generar simulaciones.

Puede [ver un registro de cada carga de datos](upload-log.md) para ver su estado. Además, si inicia una carga pero esta no se ha realizado correctamente, recibirá una notificación de error a través de [Centro de notificaciones](/help/search-social-commerce/notifications/notification-about.md), según la configuración de las notificaciones.

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [Acerca de la carga de datos de cuenta para informes y simulaciones](data-upload-accounts-about.md)
>* [Cargar datos de cuenta en un  [!DNL Amazon] [!DNL S3] bloque](upload-data-from-s3-bucket.md)
>* [Cargar datos de cuenta manualmente](upload-data-manually.md)
>* [Ver un registro de los archivos de datos de cuenta cargados](upload-log.md)
>* [Administrar cuentas de red de anuncios para cargas de datos](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
