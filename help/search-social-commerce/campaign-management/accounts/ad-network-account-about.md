---
title: Acerca de las cuentas de red de publicidad
description: Obtenga información acerca de las cuentas de red de anuncios en Search, Social y Commerce.
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/90Dq2tehH-k2aY3Ij30aHF-XQGdvlPY346moWkg3xmk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 430
ht-degree: 0%

---

# Acerca de las cuentas de red de publicidad

*Solo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Search, Social y Commerce pueden realizar el seguimiento de cualquiera de las cuentas de un anunciante en las redes de publicidad admitidas. Para habilitar el seguimiento de una cuenta, debe crear un registro de cuenta correspondiente. Debe configurar los detalles de la cuenta para cualquier tipo de cuenta, independientemente de si Search, Social y Commerce se sincronizan con ella o optimizan las ofertas y los presupuestos en sus anuncios.

## Cuentas sincronizadas mediante API

*[!DNL Google Ads], [!DNL LY Ads] (anteriormente [!DNL Yahoo! Japan Ads]), [!DNL Microsoft Advertising] (anteriormente [!DNL Bing Ads]), [!DNL Yahoo DSP] (anteriormente [!DNL Yahoo! Display Network]), [!DNL Yandex] y [!DNL Baidu] cuentas existentes*

Search, Social y Commerce se sincronizan (*se sincroniza*) con las cuentas de red de anuncios admitidas para que puedas rastrear tus anuncios, informar sobre ellos y visualizar su rendimiento. Para todas las redes de anuncios excepto [!DNL Yahoo DSP], si lo desea, puede administrar las campañas de su cuenta en Buscar, Social y Commerce. [!DNL Yahoo DSP], las campañas son de solo lectura. Para todas las redes de anuncios, puede permitir que la capacidad de optimización optimice las ofertas, los presupuestos de campaña y los objetivos de estrategia de oferta de campaña para las campañas en cuentas administradas, agregando las campañas a los portafolios.

Para habilitar la sincronización de una cuenta, el registro de cuenta debe contener las credenciales de acceso de la cuenta y estar habilitado (activo).

Durante la sincronización, Search, Social y Commerce extraen las estructuras de campaña del anunciante y las entidades de campaña admitidas, incluidos la mayoría de sus atributos que se administran o registran en Search, Social y Commerce. No incluye datos de clics, ni ofertas y modificadores de oferta introducidos fuera de Search, Social y Commerce, que se recopilan por separado. Search, Social y Commerce se sincronizan automáticamente con las cuentas de red de anuncios una vez al día, y también siempre que detecta una nueva campaña en una de las redes de anuncios. Además, envía inmediatamente a la red de anuncios todos los cambios realizados en los datos de campaña desde Search, Social y Commerce. Si lo desea, puede solicitar una sincronización manual cuando sea necesario.

Para obtener más información sobre la creación y edición de campañas sincronizadas, consulte el capítulo sobre administración de campañas.

## Cuentas solo de seguimiento

*[!DNL Naver]cuentas*

Las campañas de seguimiento le permiten realizar un seguimiento de los anuncios que compra directamente en la red de publicidad, crear informes al respecto y visualizar el rendimiento. Search, Social y Commerce no sincronizan los datos con la red de anuncios, no realizan pujas por la cuenta ni proporcionan ningún tipo de optimización o simulación.

Para permitir que Search, Social y Commerce atribuyan conversiones a clics, configure opciones de seguimiento en el registro de cuenta y habilite el registro de cuenta. A continuación, puede usar hojas de edición masiva para generar direcciones URL de seguimiento para sus anuncios y palabras clave, y agregar manualmente las direcciones URL de seguimiento dentro del administrador de anuncios [!DNL Naver].

Ver más información sobre [!DNL Naver] campañas de solo seguimiento, ver &quot;[Implementar [!DNL Naver] cuentas de solo seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)&quot;.

>[!MORELIKETHIS]
>
>* [Administrar cuentas de red de anuncios](ad-network-account-manage.md)
>* [Administrar cuentas de centros comerciales](merchant-account-manage.md)
>* [Actualizar el código de seguimiento de ID de AMO para una [!DNL Google Ads] cuenta](update-amo-id-google.md)
