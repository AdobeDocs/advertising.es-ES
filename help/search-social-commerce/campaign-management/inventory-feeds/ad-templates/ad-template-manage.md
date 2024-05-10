---
title: Administrar plantillas de publicidad para fuentes de inventario
description: Obtenga información acerca de la administración de plantillas de publicidad a través de las cuales se pueden procesar los datos de inventario para administrar la estructura de cuentas y enviar anuncios dinámicos.
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: 0a858fb9437439d2755f1a9679b0849c614293b7
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Administrar plantillas de publicidad para fuentes de inventario

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Antes o después de cargar los datos, puede crear plantillas de publicidad específicas para motores de búsqueda a través de las cuales se pueden procesar los datos. Puede crear plantillas para anuncios de texto y anuncios de texto expandidos/extendidos, [!DNL Google Ads] y [!DNL Microsoft® Advertising] anuncios de búsqueda adaptables, y para [!DNL Google Ads] y [!DNL Microsoft® Advertising] anuncios de compras.

Puede asociar cada plantilla con un archivo de fuente, [!DNL Google Merchant Center] cuenta, o [!DNL Microsoft® Merchant Center] y puede asociar varias plantillas con el mismo archivo de fuente o cuenta. Una plantilla de anuncio puede incluir variables que se sustituyen por columnas de datos reales de un archivo cargado o una cuenta. En la mayoría de los casos, las variables también pueden incluir [un grupo de modificadores](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) puede configurar en Search, Social y Commerce para crear varios anuncios, palabras clave, campañas o grupos de anuncios para cada fila aplicable del archivo de datos. Las opciones de plantilla le permiten crear una nueva estructura de cuentas (campañas, grupos de anuncios, palabras clave) para los anuncios o asignar los anuncios a la estructura de cuentas existente.

Además de crear nuevas plantillas desde cero, también puede crear nuevas plantillas clonando las existentes y editando las existentes.

Una vez creada una plantilla y asociada a un archivo de fuente de datos o a una cuenta de centro de comerciantes, se pueden propagar los datos del archivo a través de la plantilla para crear datos de campaña y estructura de cuentas. Opcionalmente, se puede crear un archivo de hoja de edición por lotes para su revisión o para su publicación inmediata en la red de anuncios.

Cualquier plantilla se puede activar, pausar o eliminar. Los datos de fuente se pueden propagar automáticamente solo a través de plantillas activas. Sin embargo, se pueden propagar manualmente los datos mediante una plantilla en pausa.

## Crear, clonar o editar una plantilla de fuente

Cree plantillas independientes para anuncios de texto y expandidos/extendidos, anuncios de búsqueda interactivos, [!DNL Google Ads] anuncios de compra y [!DNL Microsoft® Advertising] anuncios de compras.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre a la [!UICONTROL Templates] pestaña.

1. Realice una de las siguientes acciones:

   * Para crear una plantilla desde cero, haga clic en **[!UICONTROL Create/Clone]** en la barra de herramientas situada encima de la tabla de datos y, a continuación, seleccione la red de publicidad aplicable.

   * Para clonar una plantilla existente:

      1. Seleccione la casilla de verificación situada junto a la plantilla que desee copiar.

      1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Create/Clone]** y, a continuación, seleccione la red publicitaria aplicable.

   * (Para editar una plantilla existente) Junto al nombre de la plantilla, haga clic en ![Ver/editar configuración](/help/search-social-commerce/assets/settings.png "Ver/editar configuración").

1. Especifique la configuración para [plantilla de anuncio de texto](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] plantilla de anuncio de compra](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md), o [[!DNL Microsoft® Advertising] plantilla de anuncio de compra](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. En la parte superior de la ventana de configuración de la plantilla, especifique el nombre de la plantilla y la cuenta aplicable.

      Cuando clone una plantilla existente, cambie el nombre de la nueva plantilla para que los anuncios creados a partir de la nueva plantilla no se asocien a los anuncios creados a partir de la plantilla de origen.

   1. (Opcional) En la columna de la izquierda, especifique el archivo de fuente del producto o la cuenta del centro de comerciantes cuyos datos se propagarán a través de la plantilla:

      * (Para archivos de fuentes de productos) Para seleccionar un archivo cargado anteriormente, haga clic en ![Flecha hacia abajo](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flecha hacia abajo") y seleccione un archivo de la lista de archivos de fuente disponibles. Para cargar un nuevo archivo, especifique el archivo introduciendo la ruta de acceso completa y el nombre del archivo o haciendo clic en **[!UICONTROL Browse]** para localizar el archivo en el dispositivo o la red y, a continuación, haga clic en **[!UICONTROL Upload]**.

      * (Para una cuenta de centro de comerciante sincronizada) Seleccione el nombre de la cuenta.

      Se muestran las columnas del archivo o la cuenta seleccionados.

   1. En el **[!UICONTROL Account Structure]** pestaña, especifique la configuración de la estructura de la cuenta.

   1. (Solo anuncios de texto) Haga clic en **[!UICONTROL Keywords]** y especifique la configuración de la palabra clave.

   1. (Solo anuncios de búsqueda de texto y adaptables) Haga clic en el **[!UICONTROL Ads]** y realice una de las acciones siguientes:

      >[!NOTE]
      >
      >* Puede incluir hasta cuatro plantillas de variación de anuncio por plantilla de anuncio de texto estándar, cinco plantillas de variación de anuncio por plantilla de anuncio de texto expandido/ampliado y tres plantillas de variación de anuncio por plantilla de anuncio de búsqueda adaptable.
      >* Cada grupo de anuncios puede incluir hasta tres anuncios de búsqueda adaptables habilitados.
      >* No puede editar las variaciones de anuncios de texto estándar existentes y las plantillas existentes ya no generan anuncios de texto estándar.
      >* Si cambia una plantilla de variación de anuncio, los anuncios existentes se pueden eliminar y se pueden crear nuevos anuncios al propagar datos a través de la plantilla, [según el tipo de anuncio y la red de publicidad](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * Para agregar una variación de anuncio, haga lo siguiente:

         1. Clic **[!UICONTROL Add Ad Variation]** para crear un anuncio de texto, **[!UICONTROL Add ETA Variation]** para crear un anuncio de texto expandido/extendido, o **[!UICONTROL Add RSA Variation]** para crear un anuncio de texto adaptable.

            Una vez especificado el tipo de anuncio, solo puede crear ese tipo de anuncio con la plantilla.

         1. Especifique la configuración del anuncio.

            Para anuncios de búsqueda adaptables, puede incluir de 3 a 15 titulares y de 2 a 4 descripciones.

         1. (Opcional) Para rellenar previamente todos los campos alternativos y copiar con texto de los campos originales y copiar, active la casilla de verificación situada junto a **[!UICONTROL Prefill]**.

         1. (Opcional) Para añadir otro conjunto de copias de anuncio a un anuncio, que se puede utilizar si alguna de las líneas del anuncio original supera la longitud máxima una vez que algún parámetro dinámico se haya sustituido por datos durante la propagación, haga clic en **[!UICONTROL Add Alternate]** y, a continuación, agregue los valores alternativos.

            >[!NOTE]
            >
            >* Si la variable [!UICONTROL Prefill] está seleccionada, los campos alternativos se rellenan previamente con los campos originales y puede editarlos según sea necesario.
            >* Solo los campos de copia de anuncio que superen la longitud máxima se sustituyen por el valor alternativo. Por ejemplo, si solo un titular o título original es demasiado largo, la variación de anuncio generada utiliza el titular o título alternativo y las descripciones originales. Por lo tanto, asegúrese de que la copia de anuncio alternativa tenga sentido cuando se combine con la copia de anuncio original.
            >* Si la copia de anuncio original cumple los requisitos de longitud del motor de búsqueda, se descarta la copia de anuncio alternativa.
            >* Puede especificar hasta cuatro alternativas para cada campo de copia de anuncio.

         * Para editar una variación de anuncio, haga lo siguiente:

            1. Edite la configuración del anuncio.

               Para anuncios de búsqueda adaptables, puede incluir de 3 a 15 titulares y de 2 a 4 descripciones.

            1. (Opcional) Para rellenar previamente todos los campos alternativos y copiar con texto de los campos originales y copiar, active la casilla de verificación situada junto a **[!UICONTROL Prefill]**.

            1. (Opcional) Para añadir otro conjunto de copias de anuncio a un anuncio, que se puede utilizar si alguna de las líneas del anuncio original supera la longitud máxima una vez que algún parámetro dinámico se haya sustituido por datos durante la propagación, haga clic en **[!UICONTROL Add Alternate]** y, a continuación, agregue los valores alternativos.

               >[!NOTE]
               >
               >* Si la variable [!UICONTROL Prefill] está seleccionada, los campos alternativos se rellenan previamente con los campos originales y puede editarlos según sea necesario.
               >* Solo los campos de copia de anuncio que superen la longitud máxima se sustituyen por el valor alternativo. Por ejemplo, si solo un titular o título original es demasiado largo, la variación de anuncio generada utiliza el titular o título alternativo y las descripciones originales. Por lo tanto, asegúrese de que la copia de anuncio alternativa tenga sentido cuando se combine con la copia de anuncio original.
               >* Si la copia de anuncio original cumple los requisitos de longitud del motor de búsqueda, se descarta la copia de anuncio alternativa.
               >* Puede especificar hasta cuatro alternativas para cada campo de copia de anuncio.

         * Para quitar una variación de anuncio, haga clic en **[!UICONTROL Remove ETA Variation]** (para anuncios de texto expandidos/extendidos) o **[!UICONTROL Remove RSA Variation]** (para anuncios de búsqueda adaptables) junto a la variación de anuncio, según corresponda.

   1. (Solo plantillas de compra) Haga clic en **[!UICONTROL Product Groups]** y, a continuación, especifique información sobre los grupos de productos a los que desea dirigirse.

   1. (Opcional) Haga clic en **[!UICONTROL Feed Filters]** y, a continuación, especifique qué filas del archivo de fuente se van a propagar.

   1. (Opcional) Haga clic en **[!UICONTROL Label Classifications tab]** y luego especifique los valores de clasificación de etiquetas que desea asignar a los diferentes componentes de campaña creados:

      1. Haga clic en la casilla de verificación situada junto a **[!DNL \[Component\] Label Classifications]**.

      1. Para cada clasificación de etiquetas que asignar al componente, haga lo siguiente:

         1. Clic **[!UICONTROL Add Label Classification]**.

         1. Seleccione la clasificación de etiquetas y, a continuación, seleccione un valor existente o introduzca un nuevo valor.

1. Guarde la plantilla:

   * Para guardar la plantilla, haga clic en **[!UICONTROL Save]** y haga clic en **[!UICONTROL Save]** otra vez.

   * Para guardar la plantilla y propagar el archivo de datos especificado por ella, haga clic en **[!UICONTROL Save]** y haga clic en **[!UICONTROL Save & Propagate]**.

## Cambiar el estado de las plantillas de fuentes

Puede activar cualquier plantilla de fuente de datos en pausa o pausar cualquier plantilla de fuente de datos activa.

>[!NOTE]
>
>Puede propagar datos manualmente a través de una plantilla en pausa, pero los datos no se propagan automáticamente a través de ella.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre a la [!UICONTROL Templates] pestaña.

1. Seleccione la casilla de verificación situada junto a cada plantilla cuyo estado desee cambiar.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Change Status]** y haga clic en **[!UICONTROL Activate]** o **[!UICONTROL Pause]**.

## Eliminar plantillas de fuentes

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre a la [!UICONTROL Templates] pestaña.

1. Active la casilla de verificación situada junto a cada plantilla que desee eliminar.

1. En la barra de herramientas sobre la tabla de datos, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [Automatización de la administración de anuncios mediante fuentes de inventario](../inventory-feeds-about.md)
>* [Configuración de anuncios de texto y plantillas de anuncios de búsqueda adaptables](template-text-rsa.md)
>* [[!DNL Google Ads] configuración de plantilla de anuncio de compras](template-google-shopping.md)
>* [[!DNL Microsoft® Advertising] configuración de plantilla de anuncio de compras](template-microsoft-shopping.md)
>* [Propagación de datos de fuentes mediante plantillas](../feed-data-propagate.md)
