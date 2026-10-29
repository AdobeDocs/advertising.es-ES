---
title: Administrar palabras clave
description: Aprenda a crear y administrar palabras clave pujables y negativas, y a asignar restricciones a palabras clave.
feature: Search Optimization, Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 3bb565d689b65ae66d6ea2094abccdff3c9e891d
workflow-type: tm+mt
source-wordcount: '1265'
ht-degree: 0%
---
# Administrar palabras clave

*característica de Beta*

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] y solo [!DNL Baidu] cuentas existentes*

Una palabra clave es una palabra o frase asociada con un anuncio. La configuración de palabras clave incluye el tipo de coincidencia de palabra clave, el número máximo de ofertas que se utilizarán cuando la palabra clave active el anuncio y, en algunas redes de anuncios, parámetros de seguimiento opcionales. La configuración del nivel de palabra clave anula la configuración del grupo de anuncios o de la campaña. Las palabras clave negativas impiden que se muestren anuncios para búsquedas coincidentes.

Una vez que [hagas accesible una cuenta de red de anuncios a través de una conexión API](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) y Search, Social y Commerce hayan sincronizado los datos de la cuenta con la red de anuncios, puedes crear palabras clave para buscar grupos de anuncios en [tipos de campañas compatibles](/help/search-social-commerce/introduction/supported-inventory.md). También puede editar y cambiar el estado de las palabras clave y crear y eliminar palabras clave negativas.

Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Acerca de la vista [!UICONTROL Keywords] {#keyword-view-about}

La vista [!UICONTROL Manage] > [!UICONTROL Keywords] incluye dos fichas para la cuenta de anunciante seleccionada:

* La pestaña [!UICONTROL Keywords] enumera todas las palabras clave que se pueden pujar en la vista filtrada.

* La ficha [!UICONTROL Negatives] enumera todas las palabras clave negativas en la vista filtrada.

### Acciones disponibles

* [Crear palabras clave](#keyword-create)

* [Creación de palabras clave negativas](#keyword-negative-create)

* [Editar configuración de palabras clave](#keyword-edit)

* [Cambiar el estado o eliminar palabras clave y palabras clave negativas](#keyword-status)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

* [Asignar restricciones a palabras clave y anular la asignación de restricciones de palabras clave](#keyword-constraints)

* [Asignar clasificaciones de etiquetas](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md) a palabras clave

## Crear palabras clave {#keyword-create}

>[!TIP]
>
>Para crear un gran número de palabras clave a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. En la ficha **[!UICONTROL Keywords]**, haga clic en **[!UICONTROL Create Keywords]**.

1. En el paso **[!UICONTROL Basic Settings]**, seleccione la red, la cuenta, la campaña y el grupo de publicidad.

1. Escriba [[!DNL Baidu] configuración de palabras clave](keyword-settings-baidu.md), [[!DNL Google Ads] configuración de palabras clave](keyword-settings-google.md), [[!DNL LY Ads] configuración de palabras clave](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] configuración de palabras clave](keyword-settings-microsoft.md) o [[!DNL Yandex] configuración de palabras clave](keyword-settings-yandex.md).

   Puede escribir o pegar hasta 2000 palabras clave en una operación. Separe varias palabras clave con comas o introdúzcalas en líneas independientes.

   >[!NOTE]
   >
   >Si la configuración de la cuenta o la campaña especifica solo seguimiento en el nivel de anuncio, Search, Social y Commerce no generan seguimiento para las palabras clave.

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** y cambie la configuración de la entidad o la palabra clave.

1. Haga clic en **[!UICONTROL Create]**.

## Editar configuración de palabras clave {#keyword-edit}

Al cambiar el texto de la palabra clave o el tipo de coincidencia, se puede eliminar la palabra clave existente y crear una nueva, según la red publicitaria. Consulte la configuración de palabras clave para su red de anuncios para obtener más información.

>[!TIP]
>
>Para editar una gran cantidad de datos de palabras clave a la vez, incluidas palabras clave en diferentes redes de anuncios, usa [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. En la ficha **[!UICONTROL Keywords]**, active la casilla de verificación situada junto a cada palabra clave que desee editar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. Edite [[!DNL Baidu] configuración de palabras clave](keyword-settings-baidu.md), [[!DNL Google Ads] configuración de palabras clave](keyword-settings-google.md), [[!DNL LY Ads] configuración de palabras clave](keyword-settings-yahoo-japan.md), [[!DNL Microsoft Advertising] configuración de palabras clave](keyword-settings-microsoft.md) o [[!DNL Yandex] configuración de palabras clave](keyword-settings-yandex.md).

   Para varias palabras clave, puede editar solo los campos que son comunes a todas las palabras clave seleccionadas y los cambios se aplican a todas las palabras clave seleccionadas. Para algunos campos alfanuméricos, puede cambiar los valores existentes a un valor especificado, reemplazar una cadena existente por una cadena especificada, agregar un prefijo o anexar un sufijo. Para algunos campos monetarios, puede cambiar los valores existentes a un valor especificado o aumentar o disminuir el importe en un porcentaje o importe monetario especificados, con un límite.

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haz clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** y cambia la configuración de la palabra clave.

1. Haga clic en **[!UICONTROL Update]**.

## Creación de palabras clave negativas {#keyword-negative-create}

*[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising] y solo [!DNL Baidu] cuentas existentes*

Puede crear palabras clave negativas para un grupo de anuncios de búsqueda o una campaña que esté dirigido a la red de búsqueda, de visualización o nativa.

>[!NOTE]
>
>También puede crear y editar palabras clave negativas en las [configuraciones del grupo de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) y [configuraciones de campaña](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>Para crear un gran número de palabras clave negativas a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. En la ficha **[!UICONTROL Negatives]**, haga clic en **[!UICONTROL Create Negatives]** y, a continuación, en **[!UICONTROL Campaign Negative Keyword]** o en **[!UICONTROL Ad Group Negative Keyword]**.

1. Seleccione la red, la cuenta, la campaña y (para palabras clave negativas en el nivel de grupo de anuncios) el grupo de anuncios.

1. Introduzca las palabras clave negativas. Utilice la siguiente sintaxis, sin un signo menos (`-`):

   * Coincidencia amplia negativa: `keyword` (no admitido por [!DNL Microsoft Advertising])

   * Coincidencia de frase negativa: `"keyword"`

   * Coincidencia exacta negativa: `[keyword]`

   Separe varios valores con comas o introdúzcalos en líneas independientes. Puede escribir o pegar hasta 2000 palabras clave negativas en una operación. Se aplican los siguientes requisitos y restricciones:

   * Longitudes máximas de caracteres: [!DNL Baidu]: 30 bytes simples o 15 bytes dobles; [!DNL Microsoft Advertising]: 100 bytes simples o 50 bytes dobles; [!DNL Google Ads] y [!DNL LY Ads]: 80 bytes simples o 40 bytes dobles.

   * [!DNL Baidu] solo permite un tipo de coincidencia por palabra clave y grupo de anuncios. Por ejemplo, el grupo de anuncios 1 no puede incluir `"keyword"` y `[keyword]`.

   * [!DNL Google Ads]: cada palabra clave no puede contener más de 10 palabras y solo puede incluir letras, dígitos y los siguientes caracteres especiales: espacio `# $ & _ - " [ ] ' + . / :`

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Si es necesario, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** y cambie la entidad o las palabras clave negativas.

1. Haga clic en **[!UICONTROL Create]**.

## Cambiar el estado de las palabras clave y las palabras clave negativas {#keyword-status}

Puede pausar una palabra clave de búsqueda activa que se pueda pujar para deshabilitar las pujas por ella. Más tarde, puedes reanudar las pujas cambiando el estado de nuevo a activo.

También puede eliminar palabras clave de búsqueda activas o en pausa, o palabras clave negativas. Las palabras clave eliminadas se eliminan de la red de anuncios. Siguen estando visibles cuando se incluyen en el filtro de datos, pero no se pueden cambiar.

### Activar o pausar palabras clave

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. En la ficha **[!UICONTROL Keywords]**, si lo desea, filtre la lista y, a continuación, active la casilla de verificación situada junto a cada palabra clave cuyo estado desee cambiar.

1. En la barra de herramientas de acciones masivas, cambie el estado:

   * Para activar palabras clave en pausa, haga clic en **[!UICONTROL Activate]**.

   * Para pausar palabras clave activas, haga clic en **[!UICONTROL Pause]**.

### Eliminar palabras clave o palabras clave negativas

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. En la ficha **[!UICONTROL Keywords]** o **[!UICONTROL Negatives]**, si lo desea, filtre la lista y, a continuación, active la casilla de verificación situada junto a cada palabra clave o palabra clave negativa que desee eliminar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

## Administrar asignaciones de restricción para palabras clave {#keyword-constraints}

Puede asignar y eliminar restricciones de oferta para campañas, grupos de publicidad, palabras clave, ubicaciones, grupos de productos de nivel de unidad y destinos de búsqueda dinámica. Cada entidad solo puede tener una restricción.

Las restricciones las heredan las entidades secundarias, por lo que no es necesario asignar restricciones para entidades secundarias a menos que desee anular los valores heredados.

Al anular la asignación de una restricción, se elimina la asociación con los componentes de la cuenta y todos sus componentes secundarios, y los datos del informe de la restricción ya no están disponibles para dichos componentes. Al anular la asignación de una restricción, no se eliminan ni la restricción ni los propios componentes de la cuenta.

>[!NOTE]
>
>* Si posteriormente edita una palabra clave o la copia de anuncio para un anuncio no mutable (creando así una nueva palabra clave o anuncio), la restricción no se asigna a la nueva entidad.
>* Las restricciones activas restringen las ofertas solo para las unidades de oferta asignadas en portafolios optimizados de nivel de palabra clave heredados. Se ignoran para las unidades de oferta que están en portafolios activos, en portafolios híbridos o que no están en portafolios.

### Asignar una restricción a palabras clave {#keyword-constraint-assign}

Puede asignar una sola restricción a una o varias palabras clave.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. En la ficha **[!UICONTROL Keywords]**, active la casilla de verificación situada junto a cada palabra clave a la que va a asignar una sola restricción.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

### Desasignar restricciones de palabras clave {#keyword-constraint-unassign}

Anular la asignación de una restricción no la elimina. Para eliminar una restricción, de modo que no esté disponible para uso futuro, consulte &quot;Eliminar restricciones para unidades de oferta de búsqueda&quot; en el capítulo Guía de optimización sobre &quot;Restricciones de oferta&quot;, que está disponible en Buscar, Social y Commerce.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Keywords]**.

1. En la ficha **[!UICONTROL Keywords]**, active la casilla de verificación situada junto a cada palabra clave de la que anulará la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] configuración de palabras clave](keyword-settings-baidu.md)
>* [[!DNL Google Ads] configuración de palabras clave](keyword-settings-google.md)
>* [[!DNL LY Ads] configuración de palabras clave](keyword-settings-yahoo-japan.md)
>* [[!DNL Microsoft Advertising] configuración de palabras clave](keyword-settings-microsoft.md)
>* [[!DNL Yandex] configuración de palabras clave](keyword-settings-yandex.md)
>* [Administrar restricciones para buscar unidades de oferta](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Administrar clasificaciones de etiquetas](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
