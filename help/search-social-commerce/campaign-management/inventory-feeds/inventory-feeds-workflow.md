---
title: Automatización de la administración de anuncios mediante fuentes de inventario
description: Obtenga información sobre el flujo de trabajo para administrar automáticamente la estructura de cuentas y ofrecer anuncios dinámicos basados en los datos del inventario de productos o servicios.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Flujo de trabajo para administrar datos de campaña mediante fuentes de inventario

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Inicialmente, pruebe al menos un archivo de fuentes o una cuenta y, a continuación, podrá automatizar completamente el proceso o seguir controlándolo en cada paso:

1. (Opcional) Póngase en contacto con el equipo de su cuenta de Adobe para configurar un directorio FTP y depositar archivos de datos.

   Si utiliza el directorio FTP, el servicio de fuentes comprueba los archivos nuevos cada dos horas.

   De lo contrario, puede cargar archivos manualmente en la [!UICONTROL Advanced (ACM)] vista.

1. Establecer [parámetros para procesar datos de fuentes](feed-settings-manage.md#feed-data-settings).

   Si utiliza un FTP, no publique automáticamente los datos en las redes publicitarias inicialmente. Después de comprobar el resultado del primer archivo y estar satisfecho con los resultados, puede cambiar la configuración.

1. Cargue un archivo de datos en el directorio FTP, [cargar manualmente un archivo de datos](feed-files-manage.md) en el [!UICONTROL Advanced (ACM) view], o [habilitar el acceso a una cuenta de Google o Microsoft® merchant center](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Para cargar archivos manualmente, puede esperar hasta que cree una plantilla que utilice el archivo de datos.

1. (Opcional) Crear grupos de [modificadores](modifiers-manage.md) para usar como variables en varios campos de datos en plantillas de datos de fuentes.

1. [Cree una o más plantillas](ad-templates/ad-template-manage.md) que utilizan las columnas de datos para crear campañas, grupos de anuncios, palabras clave o copias de publicidad para una cuenta específica de la red de publicidad.

1. [Propagación de datos de fuentes mediante las plantillas](feed-data-propagate.md), que sustituye los nombres de columna de la plantilla por los datos del archivo o la cuenta. Según las opciones de plantilla, Buscar, Social y Comercio crea una nueva estructura de cuenta (campañas, grupos de anuncios y palabras clave) para los anuncios con la configuración predeterminada o asigna los anuncios a la estructura de cuenta existente.

1. (Opcional) [Previsualización de la salida](propagated-data-view.md) en el [!UICONTROL Advanced (ACM)] vistas y, opcionalmente, ver un resumen de los cambios de datos en la [!UICONTROL Propagations] pestaña.

1. [Publicar los datos](propagated-data-post.md) a las cuentas de red de publicidad relevantes.

1. (Si utiliza un FTP o una cuenta de un centro de comerciantes para cargar los datos, opcional) Después de validar el resultado del primer archivo de fuente, [editar los parámetros](feed-settings-manage.md#feed-data-settings) para propagar automáticamente los datos subsiguientes a través de las plantillas asociadas y publicarlos en las redes de publicidad relevantes.

1. (Cuando tenga nuevos archivos de datos) Si es necesario, cargue nuevos archivos, propague los datos a través de plantillas y publique los datos en la red de publicidad pertinente. Si lo desea, puede propagar y publicar los datos en un solo paso.

>[!MORELIKETHIS]
>
>* [Automatización de la administración de anuncios mediante fuentes de inventario](inventory-feeds-about.md)
>* [¿Cuándo las fuentes de inventario crean o eliminan componentes de cuenta?](when-are-components-created-deleted.md)

