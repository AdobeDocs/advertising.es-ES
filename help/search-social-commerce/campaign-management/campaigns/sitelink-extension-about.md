---
title: Acerca de las extensiones sitelink
description: Obtenga información acerca de las extensiones de vínculos de sitios.
exl-id: c2d96440-62da-4b57-a98e-d7b94882d6c5
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Acerca de las extensiones sitelink

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solamente*

Un vínculo de sitio es un vínculo de texto adicional en una lista de anuncios de texto. Use vínculos de sitio para llevar a los usuarios directamente a páginas específicas del sitio. La red de anuncios determina qué vínculos de sitios se muestran con un anuncio, en función de la relevancia del vínculo de sitios para el anuncio. Si lo desea, puede incluir texto descriptivo para cada vínculo a sitios, que se puede incluir en el anuncio. La red de anuncios puede mostrar automáticamente la copia de anuncio de los anuncios existentes en la cuenta con el vínculo de sitio cuando la copia de anuncio sea muy relevante para el vínculo de sitio. [!DNL Google Ads] puede mostrar de 2 a 6 vínculos de sitios en un anuncio de escritorio y hasta cuatro vínculos de sitios en un anuncio móvil. [!DNL Microsoft Advertising] puede mostrar dos, cuatro o seis vínculos de sitio con descripciones o de 4 a 6 vínculos de sitio sin descripciones.

Puede crear texto y configuración de vínculos de sitios compartidos, incluidas las fechas durante las cuales los vínculos de sitios pueden aparecer con anuncios, en el nivel de cuenta.

## Las vistas [!UICONTROL Sitelinks] y [!UICONTROL Associations]

La biblioteca [!UICONTROL Extensions] > [!UICONTROL Sitelinks] en [!UICONTROL Campaigns] > [!UICONTROL Campaigns] enumera todos los vínculos de sitio de nivel de cuenta, y puede crear y administrar los vínculos de sitio compartidos desde allí. Consulte la ayuda de red de anuncios para obtener la cantidad máxima de extensiones de anuncios por [[!DNL Google Ads] cuenta](https://support.google.com/google-ads/answer/6372658) y por [[!DNL Microsoft Advertising] cuenta](https://help.ads.microsoft.com/#apex/3/en/52001). Los vínculos de sitio de la biblioteca no se usan con los anuncios hasta que se asignan a entidades de cuenta.

Desde la vista [!UICONTROL Extensions] > [!UICONTROL Associations], puede asignar cualquiera de los vínculos de sitio como posibles extensiones a todos los anuncios en el nivel de cuenta ([!DNL Google Ads] solamente), en el nivel de campaña o en el nivel de grupo de anuncios ([!DNL Google Ads] solamente).

## Datos de rendimiento para vínculos de sitios

Search, Social y Commerce asignan los clics a una extensión de anuncio y la conversión resultante a la palabra clave asociada con el anuncio en el que se incluye la extensión. No hay datos de coste o clics en el nivel de extensión disponibles en Buscar, Social y Commerce. Sin embargo, en [el [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md), puede saber si una transacción fue resultado de un vínculo de sitio (en lugar del anuncio en sí) cuando el valor de la columna Tipo de vínculo aparece como `sl:<Sitelink text>`, como sl:Ver ofertas actuales.

En [!DNL Google Ads] y [!DNL Microsoft Advertising], puede ver los datos de costos y clics en la ficha [!DNL Ad Extensions].

>[!MORELIKETHIS]
>
>* [Administrar extensiones de vínculos de sitios compartidos](sitelink-extension-manage.md)
>* [Asociar extensiones de vínculos de sitios compartidos con campañas o grupos de anuncios](sitelink-extension-associate.md)
