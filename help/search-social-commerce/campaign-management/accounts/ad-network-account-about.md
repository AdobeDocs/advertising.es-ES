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

*Solo funciones de administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador de usuarios*

Search, Social y Commerce pueden rastrear cualquiera de las cuentas de un anunciante en las redes de anuncios admitidas. Para habilitar el seguimiento de una cuenta, debe crear un registro de cuenta correspondiente. Debe configurar los detalles de la cuenta para cualquier tipo de cuenta, independientemente de si Search, Social y Commerce se sincroniza con ella o optimiza las ofertas y los presupuestos de sus anuncios.

## Cuentas sincronizadas mediante API

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anteriormente [!DNL Bing Ads]), [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads], [!DNL Yandex], y existentes [!DNL Baidu] cuentas*

Search, Social y Commerce se sincronizan con (*sincroniza*) con cuentas de red de anuncios admitidas para que pueda realizar el seguimiento de sus anuncios, informar sobre ellos y visualizar su rendimiento. Para todas las redes de publicidad excepto para [!DNL Yahoo! Display Network], puede administrar de forma opcional las campañas de su cuenta en Buscar, Social y Comercio; [!DNL Yahoo! Display Network], las campañas son de solo lectura. En todas las redes de anuncios, puede permitir que la capacidad de optimización optimice las ofertas de anuncios en cuentas administradas añadiéndolas a portafolios.

Para habilitar la sincronización de una cuenta, el registro de cuenta debe contener las credenciales de acceso de la cuenta y estar habilitado (activo).

Durante la sincronización, Search, Social y Commerce extrae las estructuras de campaña del anunciante y las entidades de campaña admitidas, incluidos la mayoría de sus atributos que se administran o registran en Search, Social y Commerce. No incluye datos de clics, ni ofertas y modificadores de oferta introducidos fuera de Search, Social y Commerce, que se recopilan por separado. Search, Social y Commerce se sincroniza automáticamente con sus cuentas de red de anuncios una vez al día, y también siempre que detecta una nueva campaña en una de sus redes de anuncios. Además, envía inmediatamente a la red de anuncios todos los cambios realizados en los datos de campaña desde Search, Social y Commerce. Si lo desea, puede solicitar una sincronización manual cuando sea necesario.

Para obtener más información sobre la creación y edición de campañas sincronizadas, consulte el capítulo sobre Campaign Management.

## Cuentas solo de seguimiento

*[!DNL Naver]Cuentas*

Las campañas de seguimiento le permiten realizar un seguimiento de los anuncios que compra directamente en la red de publicidad, crear informes al respecto y visualizar el rendimiento. Search, Social y Commerce no sincronizan los datos con la red de anuncios, no realizan pujas por la cuenta ni proporcionan ningún tipo de optimización o simulación.

Para permitir que Search, Social y Commerce atribuyan conversiones a clics, configure opciones de seguimiento en el registro de cuenta y habilite el registro de cuenta. A continuación, puede utilizar hojas de edición masiva para generar direcciones URL de seguimiento para sus anuncios y palabras clave, y añadir manualmente las direcciones URL de seguimiento dentro de la [!DNL Naver] administrador de anuncios.

Ver más información sobre [!DNL Naver] campañas solo de seguimiento, consulte &quot;[Implementación [!DNL Naver] cuentas solo de seguimiento](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md).&quot;

>[!MORELIKETHIS]
>
>* [Administrar las cuentas de red de publicidad](ad-network-account-manage.md)
>* [Administrar cuentas de centros de comerciantes](merchant-account-manage.md)
>* [Actualización del código de seguimiento de ID de AMO para un [!DNL Google Ads] account](update-amo-id-google.md)
