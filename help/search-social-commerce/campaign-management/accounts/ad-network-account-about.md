---
title: Acerca de las cuentas de red de publicidad
description: Obtenga información acerca de las cuentas de red de anuncios en Search, Social y Commerce.
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
source-git-commit: b2d578d0e15e647a57353dbfbde666b5e72d79f2
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 0%

---

# Acerca de las cuentas de red de publicidad

*Sólo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Search, Social y Commerce pueden realizar el seguimiento de cualquiera de las cuentas de un anunciante en las redes de publicidad admitidas. Para habilitar el seguimiento de una cuenta, debe crear un registro de cuenta correspondiente. Debe configurar los detalles de la cuenta para cualquier tipo de cuenta, independientemente de si Search, Social y Commerce se sincronizan con ella o optimizan las ofertas y los presupuestos en sus anuncios.

## Cuentas sincronizadas mediante API

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anteriormente [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex] y [!DNL Baidu] cuentas existentes*

Search, Social y Commerce se sincronizan (*se sincroniza*) con las cuentas de red de anuncios admitidas para que puedas rastrear tus anuncios, informar sobre ellos y visualizar su rendimiento. Para todas las redes de anuncios excepto [!DNL Yahoo! Display Network], si lo desea, puede administrar las campañas de su cuenta en Buscar, Social y Commerce; [!DNL Yahoo! Display Network], las campañas son de solo lectura. En todas las redes de anuncios, puede permitir que la capacidad de optimización optimice las ofertas de anuncios en cuentas administradas añadiéndolas a portafolios.

Para habilitar la sincronización de una cuenta, el registro de cuenta debe contener las credenciales de acceso de la cuenta y estar habilitado (activo).

Durante la sincronización, Search, Social y Commerce extraen las estructuras de campaña del anunciante y las entidades de campaña admitidas, incluidos la mayoría de sus atributos que se administran o registran en Search, Social y Commerce. No incluye datos de clics, ni ofertas y modificadores de oferta introducidos fuera de Search, Social y Commerce, que se recopilan por separado. Search, Social y Commerce se sincronizan automáticamente con las cuentas de red de anuncios una vez al día, y también siempre que detecta una nueva campaña en una de las redes de anuncios. Además, envía inmediatamente a la red de anuncios todos los cambios realizados en los datos de campaña desde Search, Social y Commerce. Si lo desea, puede solicitar una sincronización manual cuando sea necesario.

Para obtener más información sobre la creación y edición de campañas sincronizadas, consulte el capítulo sobre Campaign Management.

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
