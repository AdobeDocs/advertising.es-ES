---
title: Administrar [!DNL Google Ads] destinos de búsqueda dinámica
description: Obtenga información sobre cómo crear y administrar [!DNL Google Ads] destinos de búsqueda dinámica.
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/MsSy-p-WSroc3FyiHx6kvcTohEaWOqJCzqbl91mNwK0'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f907f445c70ce64368dfa7e77d4cd1900ecc7113
workflow-type: tm+mt
source-wordcount: '1504'
ht-degree: 0%
---
# Administrar [!DNL Google Ads] destinos de búsqueda dinámica

*[!DNL Google Ads]solo cuentas*

Puede crear, editar y cambiar el estado de los destinos de búsqueda dinámica de [!DNL Google Ads] campañas que usan la red de búsqueda.

## ¿Qué son los destinos de búsqueda dinámica?

Los objetivos de búsqueda dinámica definen si la red de anuncios utiliza todas las páginas del sitio web o un subconjunto de ellas para segmentar los anuncios de búsqueda dinámica. Configure los objetivos de búsqueda dinámica en el nivel de grupo de anuncios; se aplican a todos los anuncios de búsqueda dinámica en el mismo grupo de anuncios.

Según la configuración de la campaña, los destinos de búsqueda dinámica pueden ser obligatorios u opcionales:

* Debe crear destinos de búsqueda dinámica cuando no especifique un dominio de sitio web ni un idioma en la sección &quot;[!UICONTROL DSA Options]&quot; de la campaña.

* Si lo desea, puede crear destinos de búsqueda dinámica cuando especifique un dominio de sitio web y un idioma en la sección &quot;[!UICONTROL DSA Options]&quot; de la campaña.

  [!DNL Google Ads] muestra automáticamente sus anuncios dinámicos de búsqueda en función del contenido de un sitio web especificado con esta configuración.

Para realizar el mejor seguimiento del rendimiento, configure la campaña con un grupo de anuncios por cada destino de búsqueda dinámica e incluya un grupo de anuncios que se ajuste a todos los criterios.

Para obtener más información sobre [!DNL Google Ads] anuncios dinámicos de búsqueda, consulte https://support.google.com/google-ads/answer/2471185.

## La vista [!UICONTROL Auto Targets] {#auto-target-view-about}

La vista [!UICONTROL Targeting] > [!UICONTROL Auto Targets] enumera todos los destinos de búsqueda dinámica en la vista filtrada de la cuenta de anunciante seleccionada. También puede administrar sus destinos de búsqueda dinámica.

Para ver los datos se requiere el permiso [!UICONTROL View Auto Targets]. Para crear destinos y editar sus ofertas o estados se requiere el permiso [!UICONTROL Edit Auto Targets].

### Acciones disponibles

* [Crear un destino de búsqueda dinámica](#auto-target-create)

* [Editar la configuración de los destinos de búsqueda dinámica](#auto-target-edit)

* [Cambiar el estado de los destinos de búsqueda dinámica o eliminarlos](#auto-target-status)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

* [Asignar restricciones](#constraint-assign) a los destinos de búsqueda dinámica y [quitar restricciones](#constraint-unassign) de los destinos de búsqueda dinámica

* [Asignar clasificaciones de etiquetas](#classification-values-assign) a destinos de búsqueda dinámica y [quitar clasificaciones de etiquetas](#classification-values-remove) de destinos de búsqueda dinámica

>[!NOTE]
>
>Puede crear y editar grandes cantidades de datos de destino (incluidas asignaciones de etiquetas y restricciones) de una sola vez cargando [archivos de hojas de edición masiva](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md) y publicándolos en la red publicitaria.

## Crear un destino de búsqueda dinámica [!DNL Google Ads] {#auto-target-create}

Puede crear objetivos de búsqueda dinámica para definir páginas en sus sitios web (es decir, los dominios utilizados en las URL de visualización de sus anuncios) cuyo contenido se utilice para segmentar los anuncios de búsqueda dinámica en el mismo grupo de anuncios.

Puede segmentar todas las páginas indexadas o especificar hasta tres criterios.

>[!NOTE]
>
>Para realizar el mejor seguimiento del rendimiento, cree un destinatario con la opción [!UICONTROL All] solo para un grupo de anuncios por campaña.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Create Auto Target]**.

1. En **[!UICONTROL Basic Settings]**, seleccione la red de anuncios, la cuenta, la campaña y el grupo de anuncios.

1. Especifique los [ajustes de destino de búsqueda dinámica](#auto-target-create-settings) restantes.

1. Haga clic en **[!UICONTROL Review and Save]**.

1. Revise la configuración. Para cambiar la configuración, haga clic en ![Editar](/help/search-social-commerce/assets/edit-new.png "Editar") **[!UICONTROL Edit]** en la sección correspondiente y cambie la configuración.

1. Haga clic en **[!UICONTROL Create]**.

## Editar la configuración de destino de búsqueda dinámica [!DNL Google Ads] {#auto-target-edit}

Puede editar el estado o la oferta máxima de uno o más destinos de búsqueda dinámica. No puede cambiar los criterios a los que se dirige.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada fila que desee editar.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

1. En el panel **[!UICONTROL Edit Auto Targets]**, edite el [estado y la configuración de la oferta](#auto-target-edit-settings).

   Los cambios se aplicarán a todos los destinos seleccionados. La configuración que no cambie conserva sus valores existentes.

   Cuando los destinos seleccionados utilizan varias divisas, la edición de ofertas está desactivada. Aún puede cambiar su estado.

1. Haga clic en **[!UICONTROL Save]**.

También puede editar una oferta de un solo destino directamente en la tabla de datos haciendo clic en su valor de oferta.

## Cambiar el estado de [!DNL Google Ads] destinos de búsqueda dinámica o eliminarlos {#auto-target-status}

Puede pausar un destino de búsqueda dinámica activo para que deje de utilizarlo para los anuncios de búsqueda dinámica en el mismo grupo de anuncios. Posteriormente, puede reanudar el uso del destino cambiando su estado de nuevo a activo. También puede eliminar destinos de búsqueda dinámica.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. (Opcional) Filtre la lista para incluir destinos de búsqueda dinámica específicos.

1. Realice una de las acciones siguientes:

   * Para cambiar el estado de un destino, haga clic en su valor en la columna **[!UICONTROL Status]** y seleccione **[!UICONTROL Active]** o **[!UICONTROL Paused]**.

   * Para cambiar el estado de varios destinos, active la casilla de verificación situada junto a cada destino, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas, seleccione **[!UICONTROL Status]** en el panel **[!UICONTROL Edit Auto Targets]** y, a continuación, haga clic en **[!UICONTROL Save]**.

   * Para eliminar uno o más destinos, active la casilla de verificación situada junto a cada destino, haga clic en **[!UICONTROL ...]>[!UICONTROL Delete]** en la barra de herramientas de acciones masivas y, a continuación, haga clic en **[!UICONTROL Confirm]** en el mensaje de confirmación.

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

## Administrar asignaciones de restricción para destinos de búsqueda dinámica {#constraints}

### Asignar una restricción a los destinos de búsqueda dinámica {#constraint-assign}

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino de búsqueda dinámica al que desee asignar una única restricción.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Bid Constraint]**.

1. Seleccione la restricción.

1. Haga clic en **[!UICONTROL Assign Now]**.

### Eliminar restricciones de los destinos de búsqueda dinámica seleccionados {#constraint-unassign}

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino de búsqueda dinámica del que anulará la asignación de restricciones.

1. En la barra de herramientas de acciones masivas, haga clic en **-[!UICONTROL Unassign]** > **[!UICONTROL Bid Constraint]**.

1. Haga clic en **[!UICONTROL Confirm]**.

## Administrar valores de clasificación para destinos de búsqueda dinámica {#classification-values}

### Asignar valores de clasificación a destinos de búsqueda dinámica {#classification-values-assign}

>[!NOTE]
>
>Las entidades secundarias heredan los valores de las etiquetas, por lo que no introduzca valores para los destinos de búsqueda dinámica a menos que desee anular los valores heredados.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino de búsqueda dinámica al que desee asignar un valor de etiqueta.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Para cada valor de clasificación aplicable, haga lo siguiente:

   1. En la columna **[!UICONTROL Classifications]**, especifique la clasificación:

      * Para utilizar una clasificación existente, haga clic en el nombre de la clasificación para expandirla.

      * Para crear una clasificación, haga clic en [!UICONTROL +] en el encabezado de la columna. En el campo de entrada, escriba el nombre de la clasificación y haga clic en ![Guardar](/help/search-social-commerce/assets/save-checkmark.png "Guardar") para guardar la clasificación inmediatamente. Para utilizar la nueva clasificación, haga clic en el nombre de la clasificación para expandirla.

        El nombre debe contener [caracteres ASCII 32-126](https://www.asciitable.com/) y la longitud máxima es de 27 caracteres de un solo byte.

   1. En la columna **[!UICONTROL Value Name]**, especifique el valor de la clasificación seleccionada:

      * Para utilizar un valor existente, seleccione el valor.

      * Para crear un valor, haga clic en [!UICONTROL +] en el encabezado de la columna. En el campo de entrada, escriba el valor y, a continuación, haga clic en ![Guardar](/help/search-social-commerce/assets/save-checkmark.png "Guardar") para guardar inmediatamente el valor y seleccionarlo de forma predeterminada.

        La longitud máxima es de 100 caracteres y puede incluir caracteres ASCII y no ASCII.

1. Haga clic en **+[!UICONTROL Assign Now]**.

### Quitar valores de clasificación de etiquetas de destinos de búsqueda dinámica {#classification-values-remove}

Al eliminar un valor de clasificación, se elimina la asociación con el componente de cuenta y todos sus componentes secundarios. Los datos del informe para el valor de clasificación ya no están disponibles para esos componentes. Al eliminar un valor de clasificación, no se elimina el valor ni los componentes de la cuenta.

1. En el menú principal, haga clic en **[!UICONTROL Targeting]>[!UICONTROL Auto Targets]**.

1. Seleccione la casilla de verificación situada junto a cada destino de búsqueda dinámica desde la que desea quitar un valor de etiqueta.

   Para obtener sugerencias sobre cómo seleccionar varias filas, consulte &quot;[Seleccionar varias filas](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Seleccione la casilla de verificación situada junto a cada valor de clasificación que desee eliminar de las entidades seleccionadas.

   Para seleccionar todos los valores asignados, haga clic en **[!UICONTROL Select All]**. Para anular la selección de todos los valores asignados, haga clic en **[!UICONTROL Deselect All]**.

1. Haga clic en **[!UICONTROL Unassign Selected]**.

## [!DNL Google Ads] configuración de destino de búsqueda dinámica {#dynamic-search-target-settings}

### Configuración disponible durante la creación {#auto-target-create-settings}

#### [!UICONTROL Auto Target Details]

**Segmentación automática:** Las páginas indizadas cuyo contenido se usa para segmentar los anuncios dinámicos de búsqueda en el grupo de anuncios:

* *[!UICONTROL All]* (valor predeterminado): segmenta todas las páginas indizadas.

* *[!UICONTROL Specific]:* Páginas de destino que coinciden con hasta tres criterios. Seleccione un criterio e introduzca su valor. Para agregar otro criterio, haga clic en **[!UICONTROL And]**. Los criterios se combinan con AND, por lo que una página debe coincidir con todos los criterios especificados. Haga clic en **[!UICONTROL Reset]** para borrar los criterios.

  * *[!UICONTROL Category]:* La categoría de contenido [!DNL Google Ads] de la página es igual al valor especificado. Introduzca un valor.

  * *[!UICONTROL URL]:* La dirección URL de la página contiene el valor especificado, como `shoes.example.com`. Introduzca una URL válida.

  * *[!UICONTROL Page Title]:* El título de la página contiene el texto especificado. Introduzca un valor.

  * *[!UICONTROL Page Content]:* El contenido de la página contiene el texto especificado. Introduzca un valor.

No se puede cambiar el criterio de destino después de crearlo.

**[!UICONTROL Status]:** El estado del destino:

* *[!UICONTROL Active]* (valor predeterminado): habilita la oferta.

* *[!UICONTROL Paused]:* deshabilita las pujas.

**[!UICONTROL Bid]:** El costo por clic (CPC) máximo para el destino. Este valor anula la oferta de nivel de grupo de anuncios. El campo es opcional; cuando se introduce una oferta, el valor mínimo es 0,01 en la divisa de la cuenta.

>[!NOTE]
>
>Si el objetivo está en un portafolio optimizado, la oferta CPC especificada se aplica por un día. Después, la capacidad de optimización coloca las ofertas según sus propios cálculos.

### Configuración disponible durante la edición {#auto-target-edit-settings}

#### [!UICONTROL Auto Target Details]

**[!UICONTROL Status]:** Seleccione **[!UICONTROL Active]** o **[!UICONTROL Paused]**.

#### [!UICONTROL Bid details]

La edición de ofertas está desactivada cuando los destinos seleccionados utilizan varias monedas.

**[!UICONTROL Bid adjustment]:** Cómo cambiar las pujas máximas:

* *[!UICONTROL Set to]:* Reemplazar cada oferta por la cantidad de [!UICONTROL Set value].

* *[!UICONTROL Increase]:* Aumentar cada oferta por la cantidad o porcentaje en [!UICONTROL Set value].

* *[!UICONTROL Decrease]:* Reducir cada oferta en la cantidad o porcentaje de [!UICONTROL Set value].

**[!UICONTROL Modifier type]:** (Para [!UICONTROL Increase] y [!UICONTROL Decrease]) Seleccione **[!UICONTROL Currency]** o **[!UICONTROL Percentage]**.

**[!UICONTROL Set value]:** La nueva oferta, o la cantidad o porcentaje por el cual cambiar cada oferta. El valor mínimo es 0,01.

**[!UICONTROL Max limit]:** (opcional; para [!UICONTROL Increase] y [!UICONTROL Decrease]) Un límite en la divisa de la cuenta. Para un aumento, esta es la puja máxima resultante. Para una disminución, esta es la puja mínima resultante. Al introducir un límite, el valor mínimo es 0,01.

>[!MORELIKETHIS]
>
>* [(Nueva IU) Administrar restricciones para buscar unidades de oferta](/help/search-social-commerce/new-ui/goals/constraints-manage.md)
>* [(Nueva IU) Administrar clasificaciones de etiquetas](/help/search-social-commerce/new-ui/set-up/label-classifications-manage.md)
