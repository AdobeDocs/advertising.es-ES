---
title: Administración de anuncios
description: Obtenga información sobre cómo crear y administrar anuncios, incluidos los tipos de anuncios disponibles.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6a479ae0bb30d609b16a343efcec296137b9ab43
workflow-type: tm+mt
source-wordcount: 1733
ht-degree: 0%

---

# Administración de anuncios

*característica de Beta*

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] y solo [!DNL Baidu] cuentas existentes*

Un anuncio pertenece a un grupo de anuncios y contiene el contenido que se muestra a los usuarios, como el titular, la descripción, la imagen u otros elementos creativos, según la red de anuncios y el tipo de anuncio.

Una vez que [hagas accesible una cuenta de red de anuncios a través de una conexión API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) y Search, Social y Commerce hayan sincronizado los datos de la cuenta con la red de anuncios, puedes crear anuncios para un [tipo de campaña compatible](/help/search-social-commerce/introduction/supported-inventory.md). También puede editar y cambiar el estado de las publicidades.

Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Acerca de la vista [!UICONTROL Ads] {#ad-view-about}

La vista [!UICONTROL Manage] > [!UICONTROL Ads] enumera todos los anuncios de la vista filtrada de la cuenta de anunciante seleccionada.

### Acciones disponibles

* [Crear un anuncio](#ad-create)

* [Cambiar el nombre de un anuncio desde la fila](#ad-rename)

* [Editar configuración de publicidad](#ad-edit)

* [Cambiar el estado de un anuncio o eliminarlo](#ad-status)

* [Administrar informes de vista de datos desde la vista [!UICONTROL Ads]](#ad-reports)

## Tipos de publicidad disponibles {#ad-types}

Puede crear y administrar tipos de anuncios admitidos para grupos de anuncios dentro de una cuenta sincronizada de red de anuncios:

* **Anuncios de texto o anuncios de texto expandidos** para un grupo de anuncios en una campaña dirigida a la red de búsqueda. Los anuncios de texto pueden incluir parámetros de seguimiento opcionales que anulan los parámetros de nivel de grupo de anuncios o de campaña. Según la red de anuncios, puede crear anuncios de texto expandidos/extendidos o anuncios de texto estándar.

* **anuncios de audiencia** nativos y entre dispositivos para [!DNL Microsoft Advertising] campañas en [!DNL Microsoft Audience Network]. Tiene dos opciones para los anuncios de audiencia, según la configuración de la campaña:

  * Si la campaña está vinculada a una tienda de centro comercial, permita que la red de publicidad genere automáticamente anuncios basados en fuentes para la campaña, utilizando la información de producto de la tienda. No es necesario crear anuncios basados en fuentes para la campaña, pero debe crear grupos de anuncios con segmentación de usuarios.

  * Si la campaña no está vinculada a una cuenta de un centro comercial, cree anuncios de audiencia basados en imágenes utilizando el formato de anuncio interactivo, que incluye varios recursos de texto e imagen. La red de anuncios organiza los anuncios mediante las combinaciones más eficaces de elementos publicitarios y los muestra en sitios como [!DNL MSN], [!DNL Outlook.com] y [!DNL Microsoft Edge].

* **Anuncios de solo llamada** para [!DNL Google Ads] campañas en la red de búsqueda. Los anuncios de solo llamada son anuncios de texto que incluyen un número de teléfono. Opcionalmente, puede usar un número de reenvío asignado por [!DNL Google Ads] para el sistema de informes de llamadas avanzado.

  >[!NOTE]
  >
  >Actualmente no se pueden crear ni editar anuncios de solo llamada. Puede ver, cambiar el estado de o eliminar un anuncio de solo llamada existente.

* **Anuncios dinámicos de búsqueda expandidos** (ahora denominados solo &quot;anuncios dinámicos de búsqueda&quot; en las redes de anuncios) para [!DNL Google Ads] y [!DNL Microsoft Advertising] grupos de anuncios dinámicos de búsqueda en campañas de búsqueda. Los anuncios dinámicos de búsqueda utilizan contenido del sitio web, en lugar de palabras clave, para decidir cuándo mostrar los anuncios. La red de anuncios genera dinámicamente el titular, elige la dirección URL de la página de aterrizaje y la dirección URL de visualización y genera automáticamente la dirección URL final.

  Para obtener más información sobre los anuncios dinámicos de búsqueda, consulte la [[!DNL Google Ads] documentación](https://support.google.com/google-ads/answer/2471185) y la [[!DNL Microsoft Advertising] documentación](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Anuncios multimedia** para [!DNL Microsoft Advertising] campañas de búsqueda. Los anuncios multimedia son anuncios de imágenes de gran tamaño que se muestran en posiciones principales y laterales destacadas, y solo se muestra un anuncio multimedia por página. Pueden incluir varios recursos de texto e imagen, como anuncios interactivos, y la red de publicidad organiza los anuncios utilizando las combinaciones más efectivas de elementos publicitarios. Los anuncios multimedia no reemplazan las ubicaciones de anuncios de texto.

* Líneas de promoción para **[!DNL Microsoft Advertising]anuncios de productos (compras)** en la red de compras. Los anuncios de compra utilizan productos de la fuente de productos [!DNL Microsoft Merchant Center] existente, en lugar de palabras clave, para decidir cómo y dónde mostrar los anuncios. La copia de anuncio y las direcciones URL de la página de aterrizaje se generan automáticamente a partir de la información del producto en la fuente, pero también puede configurar líneas de promoción para incluirlas en el grupo de anuncios.

  Para obtener más información sobre los anuncios de productos, consulte la [documentación de Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* **Anuncios de búsqueda adaptables** para [!DNL Google Ads] y [!DNL Microsoft Advertising] campañas en la red de búsqueda. La red de anuncios organiza dinámicamente anuncios de búsqueda adaptables basados en texto a partir de un conjunto de títulos y descripciones de anuncios, favoreciendo combinaciones que funcionan bien juntas. El anuncio incluye hasta tres titulares, dos descripciones y una URL personalizable desde la URL base y los campos opcionales ruta1 y ruta2. Si lo desea, puede anclar títulos de anuncios y descripciones a posiciones específicas.

  >[!NOTE]
  >
  >[!DNL Google Ads] no proporciona datos fuera de sus editores nativos sobre las combinaciones de texto que se mostraron como anuncios. Para obtener más información sobre cómo generar informes para cada combinación de texto, consulte la [documentación de Google Ads](https://support.google.com/google-ads/answer/7684791).

### Datos de rendimiento de nivel de anuncios

Los datos de nivel de anuncio están disponibles para la mayoría de los tipos de anuncio.

Sin embargo, no está disponible para [!DNL Google Ads] publicidad de búsqueda dinámica (DSA), rendimiento máximo, compras inteligentes y [!DNL YouTube] campañas. Se esperan discrepancias entre el total de datos de nivel de anuncio de una campaña y el total de datos de la campaña.

| Red de publicidad/Campaña/Tipo de publicidad | Disponibilidad de datos |
|---|---|
| [!DNL Google Ads] anuncio de búsqueda dinámica (DSA) | Campaña y grupo de publicidad |
| [!DNL Google Ads] rendimiento máximo | Campaign |
| [!DNL Google Ads] compras, compras inteligentes | Campaña y grupo de publicidad |
| [!DNL Google Ads] [!DNL YouTube] | Campaña y grupo de publicidad |

## Crear un anuncio {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* No es necesario crear anuncios de productos para campañas de compra; la red de publicidad los crea automáticamente. Sin embargo, para [!DNL Microsoft Advertising] campañas de compras puede definir líneas de promoción para incluirlas en los anuncios.
>* No puede crear [!DNL Google Ads] anuncios de solo llamada.

>[!TIP]
>
>Para crear un gran número de anuncios a la vez, usa [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Haga clic en **[!UICONTROL Create Ads]**.

1. En el paso **[!UICONTROL Basic Settings]**, seleccione la red, la cuenta, la campaña, el grupo de anuncios y el tipo de anuncio.

   Para obtener más información sobre los tipos de anuncios disponibles, consulte &quot;[Tipos de anuncios disponibles](#ad-types)&quot;.

1. Especifique la configuración restante para un [anuncio de texto Baidu](ad-settings-baidu-text.md), [anuncio de búsqueda dinámica expandido de Google Ads](ad-settings-google-dsa.md) (llamado solo &quot;anuncio de búsqueda dinámica&quot; en Google Ads), [anuncio de búsqueda interactiva de Google Ads](ad-settings-google-rsa.md), [anuncio de búsqueda dinámica expandida de Microsoft Advertising](ad-settings-microsoft-dsa.md), [anuncio multimedia de Microsoft Advertising](ad-settings-microsoft-multimedia.md), [anuncio de producto de Microsoft Advertising](ad-settings-microsoft-product.md), [anuncio interactivo de Microsoft Advertising (audiencia)](ad-settings-microsoft-responsive.md), [anuncio de búsqueda interactivo de Microsoft](ad-settings-microsoft-rsa.md) o [Yandex configuración de ad](ad-settings-yandex-text.md).

   >[!NOTE]
   >
   >(Campañas con seguimiento de conversión de Adobe Advertising) Si la configuración de la cuenta o de la campaña especifica solo seguimiento en el nivel de palabra clave, Search, Social y Commerce no generan seguimiento de anuncios.

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haz clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** y cambia la configuración del anuncio.

1. Haga clic en **[!UICONTROL Create]**.

1. &#x200B;<!-- Add link to where to generate this once available to users-->(Compras de anuncios en campañas con seguimiento de conversión de Adobe Advertising; opcional) Para rastrear clics en el anuncio, agregue manualmente una URL de seguimiento a la configuración de la cuenta, la campaña o el grupo de productos.

## Cambiar nombre de anuncio {#ad-rename}

Cambie rápidamente el nombre de un anuncio sin abrir la configuración completa del anuncio.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Mantenga el cursor sobre la fila del anuncio y haga clic en **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Edite el nombre y haga clic en **[!UICONTROL Apply]**.

## Editar configuración de publicidad {#ad-edit}

>[!NOTE]
>
>* Los siguientes tipos de anuncio son *mutables*, lo que significa que puede cambiar la copia o la imagen del anuncio y conservar el mismo ID: todos los tipos de anuncio de [!DNL Google Ads] excepto los anuncios de búsqueda dinámica y [!DNL Microsoft Advertising] los anuncios de texto expandido.
>* Todos los demás anuncios admitidos son *no mutables*, lo que significa que al cambiar la copia o imagen del anuncio se eliminará el anuncio existente y se creará uno nuevo. El rendimiento del nuevo anuncio puede ser volátil durante un par de semanas, mientras que Search, Social y Commerce recopilan datos suficientes para la optimización.
>* No puede editar el contenido de un anuncio de producto, excepto la línea de promoción de [!DNL Microsoft Advertising] anuncios de productos. Sin embargo, puede pausar o eliminar un anuncio.
>* No puede editar [!DNL Google Ads] anuncios de solo llamada. Sin embargo, puede pausar o eliminar una.
>* Solo se puede editar un anuncio a la vez.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Seleccione la casilla de verificación situada junto al anuncio.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. Edite la configuración restante para un [anuncio de texto Baidu](ad-settings-baidu-text.md), [anuncio de búsqueda dinámica expandido de Google Ads](ad-settings-google-dsa.md) (ahora solo llamado &quot;anuncio de búsqueda dinámica&quot; en Google Ads), [anuncio de búsqueda interactiva de Google Ads](ad-settings-google-rsa.md), [anuncio de búsqueda dinámica expandida de Microsoft Advertising](ad-settings-microsoft-dsa.md), [anuncio multimedia de Microsoft Advertising](ad-settings-microsoft-multimedia.md), [anuncio de producto de Microsoft Advertising](ad-settings-microsoft-product.md), [anuncio interactivo de Microsoft Advertising (audiencia)](ad-settings-microsoft-responsive.md), [anuncio de búsqueda interactivo de Microsoft](ad-settings-microsoft-rsa.md) o [Yandex configuración de anuncio de texto &#x200B;](ad-settings-yandex-text.md).

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haz clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** y cambia la configuración del anuncio.

1. Haga clic en **[!UICONTROL Update]**.

## Cambiar el estado de un anuncio {#ad-status}

Cambiar rápidamente el estado de un anuncio sin abrir la configuración completa del anuncio.

Puede pausar cualquier anuncio activo en una red de publicidad compatible para deshabilitar las pujas en ella. Más tarde, puedes reanudar las pujas cambiando el estado de nuevo a activo.

También puede eliminar cualquier anuncio activo o en pausa. Los anuncios eliminados se eliminan de la red de anuncios. Siguen estando visibles cuando se incluyen en el filtro de datos, pero no se pueden cambiar.

### Activación o pausa de un anuncio

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Seleccione la casilla de verificación de la fila de publicidad.

1. En la barra de herramientas de acciones masivas, cambie el estado:

   * Para activar un anuncio en pausa, haga clic en **[!UICONTROL Activate]**.

   * Para pausar un anuncio activo, haga clic en **[!UICONTROL Pause]**.

### Eliminar un anuncio

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Seleccione la casilla de verificación de la fila de publicidad.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Administrar informes de vista de datos desde la vista [!UICONTROL Ads] {#ad-reports}

Genere un informe que incluya las filas de datos de uno o más anuncios de la vista [!UICONTROL Ads] y, a continuación, descargue el informe como archivo de hoja de cálculo de Microsoft Excel (formato XLXS). El informe incluye todas las columnas visibles en la vista.

Puede eliminar cualquier informe generado.

Consulte también &quot;[(IU heredada) Descargar datos de una vista de administración de campañas](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)&quot; y &quot;[(IU heredada) Eliminar un informe de datos de rendimiento o un archivo de hoja de edición masiva del menú [!UICONTROL Downloads]](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md).&quot;

### Generación de un informe con las filas de datos filtradas

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Especifique los anuncios cuyos datos desea descargar:

   * Para descargar datos de anuncios específicos, active las casillas de verificación situadas junto a los anuncios.

   * Para descargar los datos de todos los anuncios, no es necesario seleccionar ninguna casilla de verificación. Todos los anuncios se incluyen de forma predeterminada.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la configuración de [!UICONTROL Grid Reports], escriba un nombre de informe único y haga clic en **[!UICONTROL Generate]**.

   De forma predeterminada, el nombre del archivo es &quot;ad_YYYYMMDD_NNNN&quot;, donde &quot;NNNN&quot; es el número de trabajo secuencial (como &quot;ad_20250402_1326).

   El archivo se agrega a la lista [!UICONTROL Recently Generated].

1. (Opcional) Para descargar el archivo una vez que se haya completado, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Descargar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Eliminar un informe completado

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe") **[!UICONTROL Reports]**.

1. En la lista [!UICONTROL Recently Generated] del cuadro de diálogo [!UICONTROL Grid Reports], haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar") junto al nombre de archivo.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] configuración de anuncios de texto](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] configuración de anuncios dinámicos de búsqueda expandida](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] configuración del anuncio de búsqueda adaptable](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] configuración de anuncios dinámicos de búsqueda expandida](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] configuración de anuncios multimedia](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] configuración de anuncios de productos](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] configuración de anuncio adaptable (audiencia)](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] configuración del anuncio de búsqueda adaptable](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] configuración de anuncios de texto](ad-settings-yandex-text.md)
