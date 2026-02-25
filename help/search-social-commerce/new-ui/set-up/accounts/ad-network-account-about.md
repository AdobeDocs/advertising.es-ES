---
title: (Nueva IU) Acerca de las cuentas de red de publicidad
description: Obtenga información acerca de las cuentas de red de anuncios en la nueva IU de Search, Social y Commerce.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# (Nueva IU) Acerca de las cuentas de red de publicidad

Search, Social y Commerce pueden realizar el seguimiento de cualquiera de las cuentas de un anunciante en las redes de publicidad admitidas. Para habilitar el seguimiento de una cuenta, debe crear un registro de cuenta correspondiente. Debe configurar los detalles de la cuenta para cualquier tipo de cuenta, independientemente de si Search, Social y Commerce se sincronizan con ella o optimizan las ofertas y los presupuestos en sus anuncios.

## Cuentas sincronizadas mediante API

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anteriormente [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] y [!DNL Baidu] cuentas existentes*

Search, Social y Commerce se sincronizan (*se sincroniza*) con las cuentas de red de anuncios admitidas para que puedas rastrear tus anuncios, informar sobre ellos y visualizar su rendimiento. Para todas las redes de anuncios excepto [!DNL Yahoo! Display Network], si lo desea, puede administrar las campañas de su cuenta en Buscar, Social y Commerce; [!DNL Yahoo! Display Network], las campañas son de solo lectura. Para todas las redes de anuncios, puede permitir que la capacidad de optimización optimice las ofertas, los presupuestos de campaña y los objetivos de estrategia de oferta de campaña para las campañas en cuentas administradas, agregando las campañas a los portafolios.

Para habilitar la sincronización de una cuenta, el registro de cuenta debe contener las credenciales de acceso de la cuenta y estar habilitado (activo).

Durante la sincronización, Search, Social y Commerce extraen las estructuras de campaña del anunciante y las entidades de campaña admitidas, incluidos la mayoría de sus atributos que se administran o registran en Search, Social y Commerce. No incluye datos de clics, ni ofertas y modificadores de oferta introducidos fuera de Search, Social y Commerce, que se recopilan por separado. Search, Social y Commerce se sincronizan automáticamente con las cuentas de red de anuncios una vez al día, y también siempre que detecta una nueva campaña en una de las redes de anuncios. Además, envía inmediatamente a la red de anuncios todos los cambios realizados en los datos de campaña desde Search, Social y Commerce. Si lo desea, puede solicitar una sincronización manual cuando sea necesario.

Para obtener más información sobre la creación y edición de campañas sincronizadas, consulte el capítulo sobre administración de campañas.

## Cuentas para las que se cargan datos manualmente

En el caso de las redes de anuncios en línea para las que Search, Social y Commerce no admiten la API, puede cargar contenido de campañas y datos de coste, clics y conversiones sin conexión en una cuenta para realizar simulaciones de informes y rendimiento. Search, Social y Commerce no sincronizan los datos con la red de anuncios, no proporcionan ofertas automatizadas ni ofrecen ningún tipo de optimización, pero le permiten optimizar las perspectivas entre canales e identificar oportunidades para la optimización manual.

## Cuentas solo de seguimiento basadas en plantillas

*Disponible solo para cuentas de [!DNL Naver] existentes*

Las campañas de seguimiento le permiten realizar un seguimiento de los anuncios que compra directamente en la red de publicidad, crear informes al respecto y visualizar el rendimiento. Search, Social y Commerce no sincronizan los datos con la red de anuncios, no proporcionan pujas automatizadas ni ofrecen ningún tipo de optimización o simulación.

Para permitir que Search, Social y Commerce atribuyan conversiones a clics, configure opciones de seguimiento en el registro de cuenta y habilite el registro de cuenta. A continuación, puede usar hojas de edición masiva para generar direcciones URL de seguimiento para sus anuncios y palabras clave, y agregar manualmente las direcciones URL de seguimiento dentro del administrador de anuncios [!DNL Naver].

No puede configurar nuevas cuentas de [!DNL Naver] en Search, Social y Commerce. Ver más información sobre [!DNL Naver] campañas de solo seguimiento, ver &quot;[Implementar [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)&quot;.

>[!MORELIKETHIS]
>
>* [Administrar cuentas de red de anuncios mediante conexión API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [Administrar cuentas de red de anuncios para cargas de datos](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [Administrar [!DNL Naver] cuentas solo para seguimiento](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [Implementar [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [Administrar cuentas de centros comerciales](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
