---
title: Automatización de la administración de anuncios mediante fuentes de inventario
description: Obtenga información acerca de la administración avanzada de campañas, que le permite administrar automáticamente la estructura de cuentas y enviar anuncios dinámicos basados en los datos sobre el inventario de productos o servicios.
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 0%

---

# Automatización de la administración de anuncios mediante fuentes de inventario

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

La vista [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] para la administración avanzada de campañas le permite crear y actualizar automáticamente la estructura de cuentas de red de anuncios y enviar anuncios dinámicos basados en los datos sobre su inventario de productos o servicios. Puede cargar nuevos archivos con datos de productos diariamente o con la frecuencia que desee, o bien vincular directamente a una cuenta de [!DNL Google] o [!DNL Microsoft] del centro de comerciantes. Utilice esta función para lo siguiente:

* Cree nuevas campañas a partir de fuentes de datos ordenadas.

* Actualice de forma dinámica el texto y los anuncios adaptables de búsqueda, los [!DNL Google Ads] anuncios de compras o los [!DNL Microsoft Advertising] anuncios de compras cada vez que se procesen nuevos datos, utilizando variables dinámicas para elementos de datos modificables (como el precio o la cantidad). Cada vez que cambia los datos, se eliminan los anuncios existentes y se crean nuevos.

* Ponga en pausa o elimine automáticamente los grupos de anuncios, las palabras clave y los anuncios cuando el stock caiga por debajo de un nivel específico, según una fecha de finalización especificada o cuando se omita un componente existente de los datos de fuente.

Para configurar los anuncios, cree plantillas de fuentes de inventario que contengan variables (marcadores de posición) y, a continuación, sustituya las variables por columnas de datos reales de un archivo cargado o una cuenta de [Google o Microsoft Merchant Center sincronizada](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Las variables también pueden incluir grupos de modificadores configurados en un archivo o filas individuales del archivo para crear varios anuncios, palabras clave, campañas o grupos de anuncios para cada fila aplicable del archivo de datos. Por ejemplo, si utiliza una variable de grupo de modificadores en un titular de anuncio y el grupo de modificadores incluye dos modificadores (&quot;barato&quot; y &quot;con descuento&quot;), se crean dos anuncios independientes para cada producto, uno para cada modificador. Para los anuncios dinámicos de búsqueda [!DNL Google Ads] y [!DNL Microsoft Advertising], también puede incluir valores para los personalizadores de anuncios.

| [!UICONTROL Ad Variation] sección de plantilla | Modificadores en Search, Social y Commerce | Contenido de fuente | Anuncios resultantes |
|----|----|----|----|
| Título: Compre \{<i>Product Category</i>\} de gama alta &lt;<i>CheapList</i>>.<br><br>Descripción 1: Gran inventario de \{<i>Nombre de producto</i>\}.<br><br>Descripción 2: disponible con un descuento de \{<i>Porcentaje de descuento</i>\}%. | Valores del grupo de modificadores &quot;CheapList&quot;:<br><br>&quot;for cheap&quot;<br><br>&quot;at a discount&quot; | Categoría del producto,Nombre del producto,Porcentaje de descuento<br>electrónica,iPods,10<br><br>ropa,Camisas,15<br><br><b>Nota:</b> Puede separar los valores mediante comas o tabulaciones. | <u>Compre productos electrónicos de alta gama a precios económicos.</u><br>Gran inventario de tabletas. Disponible con un 10% de descuento.<br><br><u>Compre productos electrónicos de alta gama con descuento.</u><br>Gran inventario de tabletas. Disponible con un 10% de descuento.<br><br><u>Compra ropa de alta gama a buen precio.</u><br>Enorme inventario de camisas. Disponible con un 15% de descuento.<br><br><u>Compra ropa de alta gama con descuento.</u><br>Enorme inventario de camisas. Disponible con un 15% de descuento. |

Una vez generados los anuncios, puede revisarlos opcionalmente y luego publicarlos en la red de anuncios.

>[!NOTE]
>Para crear o editar datos de campaña de forma masiva mediante archivos de hoja de cálculo, consulte &quot;[Acerca de la administración de datos de campaña mediante hojas de cálculo en lotes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)&quot;.

## Flujo de trabajo para administrar datos de campaña mediante fuentes de inventario

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Inicialmente, pruebe al menos un archivo de fuentes o una cuenta y, a continuación, podrá automatizar completamente el proceso o seguir controlándolo en cada paso:

1. (Opcional) Póngase en contacto con el equipo de su cuenta de Adobe para configurar un directorio FTP y depositar archivos de datos.

   Si utiliza el directorio FTP, el servicio de fuentes comprueba los archivos nuevos cada dos horas.

   De lo contrario, puede cargar manualmente los archivos en la vista [!UICONTROL Advanced (ACM)].

1. Establezca [parámetros para procesar datos de fuentes](feed-settings-manage.md#feed-data-settings).

   Si utiliza un FTP, no publique automáticamente los datos en las redes publicitarias inicialmente. Después de comprobar el resultado del primer archivo y estar satisfecho con los resultados, puede cambiar la configuración.

1. Cargue un archivo de datos en el directorio FTP, [cargue manualmente un archivo de datos](feed-files-manage.md) en [!UICONTROL Advanced (ACM) view] o [habilite el acceso a una cuenta de Google o de Microsoft Merchant Center](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md).

Para cargar archivos manualmente, puede esperar hasta que cree una plantilla que utilice el archivo de datos.

1. (Opcional) Cree grupos de [modificadores](modifiers-manage.md) para usarlos como variables en varios campos de datos en plantillas de datos de fuentes.

1. [Cree una o más plantillas](ad-templates/ad-template-manage.md) que utilicen las columnas de datos para crear campañas, grupos de anuncios, palabras clave o copias de anuncios para una cuenta específica de la red de anuncios.

1. [Propague los datos de las fuentes a través de las plantillas](feed-data-propagate.md), que sustituyen los nombres de columna de la plantilla por los datos del archivo o la cuenta. Según las opciones de plantilla, Buscar, Social y Commerce crean una nueva estructura de cuentas (campañas, grupos de anuncios y palabras clave) para los anuncios con la configuración predeterminada o asignan los anuncios a la estructura de cuentas existente.

1. (Opcional) [Obtenga una vista previa del resultado](propagated-data-view.md) en las vistas [!UICONTROL Advanced (ACM)] y, opcionalmente, vea un resumen de los cambios de datos en la ficha [!UICONTROL Propagations].

1. [Publicar los datos](propagated-data-post.md) en las cuentas de red de anuncios relevantes.

1. (Si usa un FTP o una cuenta de un centro de comerciantes para cargar los datos; opcional) Después de validar el resultado del primer archivo de fuente, [edite los parámetros](feed-settings-manage.md#feed-data-settings) para propagar automáticamente los datos subsiguientes a través de las plantillas asociadas y publicarlos en las redes de publicidad relevantes.

1. (Cuando tenga nuevos archivos de datos) Si es necesario, cargue nuevos archivos, propague los datos a través de plantillas y publique los datos en la red de publicidad pertinente. Si lo desea, puede propagar y publicar los datos en un solo paso.

>[!MORELIKETHIS]
>
>* [¿Cuándo crean o eliminan las fuentes de inventario los componentes de la cuenta?](when-are-components-created-deleted.md)
