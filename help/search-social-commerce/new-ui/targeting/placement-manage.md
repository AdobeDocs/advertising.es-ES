---
title: Administrar ubicaciones
description: Obtenga información sobre cómo crear y administrar ubicaciones de Google Ads y ubicaciones negativas, y asignar restricciones a ubicaciones.
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
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: d3e38179ae119f35c184bee398edaaf456fab563
workflow-type: tm+mt
source-wordcount: '1390'
ht-degree: 0%
---
# Administrar ubicaciones

*característica de Beta*

*[!DNL Google Ads]solo cuentas*

Las ubicaciones son ubicaciones en la red de visualización en las que pueden aparecer los anuncios. La configuración de ubicación incluye los parámetros de oferta máxima y seguimiento opcional. La configuración del nivel de ubicación anula la configuración del grupo de anuncios o de la campaña. Las ubicaciones negativas impiden que se muestren anuncios en sitios específicos.

Una vez que [haga accesible una cuenta de red de anuncios a través de una conexión API](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md) y Search, Social y Commerce hayan sincronizado los datos de la cuenta con la red de anuncios, puede crear ubicaciones para grupos de anuncios en [tipos de campañas compatibles](/help/search-social-commerce/introduction/supported-inventory.md) dirigidos a la red de visualización. También puede editar y cambiar el estado de las ubicaciones y crear y eliminar ubicaciones negativas.

>[!NOTE]
>
>[!DNL Google Ads] no proporciona datos de rendimiento de nivel de anuncio para las ubicaciones.

## Acerca de la vista [!UICONTROL Placements] {#placement-view-about}

La vista [!UICONTROL Targeting] > [!UICONTROL Placements] incluye dos fichas para la cuenta de anunciante seleccionada:

* La pestaña [!UICONTROL Placements] enumera todas las ubicaciones que se pueden pujar en la vista filtrada.

* La ficha [!UICONTROL Negatives] enumera todas las ubicaciones negativas en la vista filtrada.

Para ver la página se requiere el permiso [!UICONTROL View Placements]. Para crear ubicaciones o ubicaciones negativas, editar ubicaciones, cambiar el estado de ubicación y eliminar ubicaciones o ubicaciones negativas se requiere el permiso [!UICONTROL Edit Placements].

### Acciones disponibles

* [Creación de ubicaciones](#placement-create)

* [Creación de ubicaciones negativas](#placement-negative-create)

* [Editar configuración de ubicación](#placement-edit)

* [Cambiar el estado de las ubicaciones y las ubicaciones negativas, o eliminarlas](#placement-status)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

* [Asignar restricciones a ubicaciones y anular la asignación de restricciones de ubicaciones](#placement-constraints)

* [Asignar clasificaciones de etiquetas a las ubicaciones](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)

## Creación de ubicaciones {#placement-create}

>[!TIP]
>
>Para crear un gran número de ubicaciones a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. En la ficha **[!UICONTROL Placements]**, haga clic en **[!UICONTROL Create Placement]**.

1. En el paso **[!UICONTROL Basic Settings]**, seleccione la red, la cuenta, la campaña y el grupo de publicidad.

1. Escriba la [configuración de ubicación](#placement-create-settings).

   Para crear varias ubicaciones, separe las direcciones URL del sitio web con comas.

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Revise la configuración. Para cambiar la configuración, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** en la sección correspondiente y cambie la configuración.

1. Haga clic en **[!UICONTROL Create]**.

## Creación de ubicaciones negativas {#placement-negative-create}

Puede crear ubicaciones negativas para una campaña o grupo de anuncios [!DNL Google Ads] que esté dirigida a la red de visualización.

>[!NOTE]
>
>También puede crear y editar ubicaciones negativas en la [configuración del grupo de anuncios](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md) y la [configuración de la campaña](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md).

>[!TIP]
>
>Para crear un gran número de ubicaciones negativas a la vez, use [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. En la ficha **[!UICONTROL Negatives]**, haga clic en **[!UICONTROL Create Negative]** y, a continuación, en **[!UICONTROL Campaign Negative]** o en **[!UICONTROL Ad Group Negative]**.

1. En el paso **[!UICONTROL Basic Settings]**, seleccione la red, la cuenta, la campaña y (para las ubicaciones negativas en el nivel de grupo de anuncios) el grupo de anuncios.

1. En el paso **[!UICONTROL Manage Websites]**, escriba las direcciones URL negativas del sitio web, como `www.example.com` o `example.com/shoes`.

   Separe las distintas direcciones URL con comas. Este formulario acepta direcciones URL del sitio web, no cadenas de tema o categoría.

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Revise la configuración. Para cambiar la configuración, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** en la sección correspondiente y cambie la configuración.

1. Haga clic en **[!UICONTROL Create]**.

## Editar configuración de ubicación {#placement-edit}

Puede editar el estado, la oferta, la dirección URL base y la plantilla de seguimiento de una o varias ubicaciones. No puede cambiar la dirección URL del sitio web de destino ni editar las ubicaciones eliminadas.

>[!TIP]
>
>Para editar una gran cantidad de datos de ubicación a la vez, usa [hojas de edición masiva de campañas](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. En la ficha **[!UICONTROL Placements]**, active la casilla de verificación situada junto a cada ubicación que desee editar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. En el panel **[!UICONTROL Edit Placements]**, edite la [configuración de ubicación](#placement-edit-settings).

   Para varias ubicaciones, los cambios se aplicarán a todas las ubicaciones seleccionadas. Puedes establecer pujas en un valor determinado o aumentarlas o reducirlas en un porcentaje o importe monetario determinados, con un límite. En el caso de las direcciones URL, puede reemplazar el valor existente, buscar y reemplazar texto, agregar un prefijo o anexar un sufijo.

   La edición de ofertas está desactivada cuando las ubicaciones seleccionadas utilizan varias monedas.

1. Haga clic en **[!UICONTROL Save]**.

## Cambiar el estado de las ubicaciones y las ubicaciones negativas {#placement-status}

Puedes pausar una colocación activa y pujable para desactivar las pujas en ella. Más tarde, puedes reanudar las pujas cambiando el estado de nuevo a activo.

También puede eliminar ubicaciones activas o en pausa, o negativas. Las ubicaciones eliminadas se eliminan de la red de anuncios. Siguen estando visibles cuando se incluyen en el filtro de datos, pero no se pueden cambiar.

### Activar o pausar ubicaciones

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. En la ficha **[!UICONTROL Placements]**, si lo desea, filtre la lista y, a continuación, active la casilla de verificación situada junto a cada ubicación cuyo estado desee cambiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. En la sección **[!UICONTROL Placement Details]**, cambie **[!UICONTROL Status]**:

   * Para activar las ubicaciones en pausa, seleccione **[!UICONTROL Active]**.

   * Para pausar las ubicaciones activas, seleccione **[!UICONTROL Paused]**.

1. Haga clic en **[!UICONTROL Save]**.

### Eliminar ubicaciones o ubicaciones negativas

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. En la ficha **[!UICONTROL Placements]** o **[!UICONTROL Negatives]**, si lo desea, filtre la lista y, a continuación, active la casilla de verificación situada junto a cada ubicación o ubicación negativa que desee eliminar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

## Administrar asignaciones de restricción para ubicaciones {#placement-constraints}

Puede asignar y eliminar restricciones de oferta para campañas, grupos de publicidad, palabras clave, ubicaciones, grupos de productos de nivel de unidad y destinos de búsqueda dinámica. Cada entidad solo puede tener una restricción.

Las restricciones las heredan las entidades secundarias, por lo que no es necesario asignar restricciones para entidades secundarias a menos que desee anular los valores heredados.

Al anular la asignación de una restricción, se elimina la asociación con los componentes de la cuenta y todos sus componentes secundarios, y los datos del informe de la restricción ya no están disponibles para dichos componentes. Al anular la asignación de una restricción, no se eliminan ni la restricción ni los propios componentes de la cuenta.

>[!NOTE]
>
>* Si posteriormente edita una palabra clave o la copia de anuncio para un anuncio no mutable (creando así una nueva palabra clave o anuncio), la restricción no se asigna a la nueva entidad.
>* Las restricciones activas restringen las ofertas solo para las unidades de oferta asignadas en portafolios optimizados de nivel de palabra clave heredados. Se ignoran para las unidades de oferta que están en portafolios activos, en portafolios híbridos o que no están en portafolios.

### Asignar una restricción a las ubicaciones {#placement-constraint-assign}

Puede asignar una sola restricción a una o varias ubicaciones.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. En la ficha **[!UICONTROL Placements]**, active la casilla de verificación situada junto a cada ubicación a la que va a asignar una única restricción.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Assign]>[!UICONTROL Bid Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

### Desasignar restricciones de ubicaciones {#placement-constraint-unassign}

Anular la asignación de una restricción no la elimina. Para eliminar una restricción, de modo que no esté disponible para uso futuro, consulte &quot;[Administrar restricciones para buscar unidades de oferta](/help/search-social-commerce/new-ui/goals/constraints-manage.md#constraint-change-status)&quot;.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Placements]**.

1. En la ficha **[!UICONTROL Placements]**, active la casilla de verificación situada junto a cada ubicación de la que anulará la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Unassign]>[!UICONTROL Bid Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

## Configuración de ubicación {#placement-settings}

### Configuración al crear ubicaciones {#placement-create-settings}

#### [!UICONTROL Basic Settings]

**[!UICONTROL Network]:** La red publicitaria. Solo se admite [!DNL Google Ads].

**[!UICONTROL Account]:** La cuenta de red de publicidad.

**[!UICONTROL Campaign]:** La campaña.

**[!UICONTROL Ad Group]:** El grupo de anuncios.

#### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** sitios en la red de visualización en los que puede aparecer su anuncio. Escriba una dirección URL de sitio web válida, como `www.example.com`, `example.com` o `example.com/shoes`. Separe las distintas direcciones URL con comas. La dirección URL no puede incluir el signo de interrogación (`?`).

Para excluir sitios web, [crea ubicaciones negativas](#placement-negative-create) desde la pestaña [!UICONTROL Targeting] > [!UICONTROL Placements] > [!UICONTROL Negatives] o usa la configuración de campañas y grupos de anuncios.

**[!UICONTROL Status]:** El estado de visualización de la ubicación: *[!UICONTROL Active]* (para habilitar la oferta) o *[!UICONTROL Paused]* (para deshabilitar la oferta).

#### [!UICONTROL Bids]

**[!UICONTROL Bid]:** (opcional) coste por clic (CPC) o coste por mil impresiones visibles (vCPM) para el anuncio basado en la ubicación, según la estrategia de oferta de campaña. Este valor anula la oferta de nivel de grupo de anuncios.

#### [!UICONTROL Tracking URLs]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

{{$include /help/_includes/base-url-google-note.md}}

{{$include /help/_includes/tracking-template-google.md}}

>[!NOTE]
>
>El formulario de creación de nueva interfaz de usuario requiere la dirección URL base y la plantilla de seguimiento, cuando se especifican, para comenzar con `http://` o `https://`.

### Configuración al editar ubicaciones {#placement-edit-settings}

El panel [!UICONTROL Edit Placements] admite la siguiente configuración para una o varias ubicaciones seleccionadas. No puede cambiar la dirección URL del sitio web de destino.

#### [!UICONTROL Placement Details]

**[!UICONTROL Status]:** *[!UICONTROL Active]* o *[!UICONTROL Paused]*.

#### [!UICONTROL Bid Details]

**[!UICONTROL Bid adjustment]:** Cómo cambiar la oferta:

* *[!UICONTROL Set to]:* Reemplazar la oferta existente con un valor especificado.

* *[!UICONTROL Increase]:* Aumentar la oferta existente en una cantidad o porcentaje especificados.

* *[!UICONTROL Decrease]:* Reducir la oferta existente en un porcentaje o cantidad especificados.

**[!UICONTROL Modifier type]:** (Para aumentos o disminuciones) Si el ajuste usa *[!UICONTROL Currency]* o *[!UICONTROL Percentage]*.

**[!UICONTROL Set value]:** La nueva puja o el importe de ajuste. El valor mínimo es 0,01.

**[!UICONTROL Max limit]:** (Para aumentos o disminuciones; opcional) El límite de la oferta ajustada. Para un aumento, esta es la oferta máxima; para una disminución, esta es la oferta mínima. El valor límite mínimo es 0,01.

La edición de ofertas está desactivada cuando las ubicaciones seleccionadas utilizan varias monedas.

#### [!UICONTROL Tracking Urls]

**[!UICONTROL Base Url]**, **[!UICONTROL Tracking Template]:** Para cada campo, seleccione cómo modificar el valor:

* *[!UICONTROL Set To]:* Reemplace el valor. Escriba una dirección URL de sitio web válida que comience por `http://` o `https://`.

* *[!UICONTROL Find/Replace]:* Reemplaza el texto especificado dentro del valor. Introduzca el texto que desea buscar y el texto de reemplazo.

* *[!UICONTROL Add Suffix]:* Anexe texto al valor. Introduzca el texto del sufijo.

* *[!UICONTROL Add Prefix]:* Agregue texto al principio del valor. Introduzca el texto del prefijo.

>[!NOTE]
>
>Todas las direcciones URL base nuevas deben ser direcciones URL válidas que comiencen por `http://` o `https://`.

>[!MORELIKETHIS]
>
>* [Administrar restricciones para buscar unidades de oferta](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [Administrar clasificaciones de etiquetas](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
