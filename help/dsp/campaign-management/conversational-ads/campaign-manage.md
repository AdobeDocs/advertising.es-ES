---
title: Administrar [!DNL ChatGPT Ads] campañas de anuncios conversacionales
description: Aprenda a crear y administrar [!DNL ChatGPT Ads] campañas, grupos de anuncios y anuncios con tarjetas de chat, una función beta que coloca anuncios dentro de las conversaciones del asistente de IA.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 0%
---
# Administrar [!DNL ChatGPT Ads] campañas de anuncios conversacionales, grupos de anuncios y anuncios

*característica de Beta*

Administre [!DNL ChatGPT Ads] campañas, grupos de anuncios y anuncios de tarjetas de chat en una [cuenta de anuncios conversacionales](account-manage.md).

Se le factura por el uso de [!DNL ChatGPT Ads] al final del mes con el resto de sus facturas. Si tiene alguna pregunta sobre facturación, póngase en contacto con el equipo de su cuenta de Adobe.

## La vista [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] {#campaign-views-about}

La vista [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] incluye tres fichas: [!UICONTROL Campaigns], [!UICONTROL Ad Groups] y [!UICONTROL Ads]. Cada pestaña enumera las campañas, grupos de anuncios o publicidades de la cuenta seleccionada, junto con los datos de rendimiento del intervalo de fechas seleccionado. Los datos de rendimiento a nivel de campaña, grupo de anuncios y anuncio incluyen [!UICONTROL Impressions], [!UICONTROL Clicks], [!UICONTROL Spend], [!UICONTROL CTR], [!UICONTROL Avg CPC] y [!UICONTROL Avg CPM].

>[!NOTE]
>
>* Las organizaciones configuradas para ver los valores de impuestos en las vistas Informes no los verán para [!DNL ChatGPT Ads]. Calcule los valores de impuestos manualmente.

### Acciones disponibles

<!-- * [Refresh information about your campaigns](#refresh) -- Add topic below. -->

* [Crear](#campaign-create) o [editar](#campaign-edit) una campaña

* [Crear](#ad-group-create) o [editar](#ad-group-edit) un grupo de anuncios para una campaña existente

* [Crear](#ad-create) o [editar](#ad-edit) un anuncio para un grupo de anuncios existente

* [Activar o pausar una campaña, un grupo de publicidad o una publicidad](#pause-activate)

* [Archivar una campaña, un grupo de anuncios o una publicidad](#archive)

* [Explorar en profundidad desde campañas hasta grupos de publicidad y anuncios](#drill-down)

* [Actualizar la campaña, el grupo de anuncios o la lista de anuncios](#refresh)

## Campañas

### Crear una campaña de anuncios conversacionales de [!DNL ChatGPT Ads] {#campaign-create}

Al crear una campaña, puede crear su primer grupo de publicidad y su primer anuncio. Cada paso crea esa entidad en cuanto hace clic en **[!UICONTROL Next]**, por lo que no puede volver a un paso anterior; si necesita cambiar algo posteriormente, edítela una vez que se cierre el asistente.

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En el submenú, haga clic en la ficha **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, seleccione un anunciante y una cuenta de [!DNL ChatGPT Ads].

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]>[!UICONTROL Campaign]**.

1. Especifique la [configuración de campaña](#campaign-settings).

1. Haga clic en **[!UICONTROL Next]** para guardar la configuración de la campaña.

1. Realice una de las siguientes acciones:

   * Si no desea crear un grupo de anuncios para la campaña, haga clic en **[!UICONTROL Close]**.

     >[!TIP]
     >
     >Para crear un grupo de anuncios o un anuncio posterior, consulte &quot;[Crear un grupo de anuncios](#ad-group-create)&quot; o &quot;[Crear un anuncio](#ad-create)&quot;.&quot;

   * (Opcional) Crear un grupo de anuncios:

     1. Especifique la [configuración del grupo de anuncios](#ad-group-settings).

     1. Haga clic en **[!UICONTROL Next]** para guardar la configuración del grupo de anuncios.

     1. (Opcional) Si no desea crear un anuncio para la campaña, haga clic en **[!UICONTROL Close]**.

   * (Opcional después de crear un grupo de anuncios) Crear un anuncio:

     1. Especifique la [configuración del anuncio](#ad-settings).

     1. Haga clic en **[!UICONTROL Create ad]**.

### Editar la configuración de campañas de anuncios conversacionales de [!DNL ChatGPT Ads] {#campaign-edit}

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En el submenú de la izquierda, haga clic en **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, seleccione un anunciante y una cuenta de [!DNL ChatGPT Ads].

1. (Si es necesario) Sobre la tabla de datos, haga clic en la ficha **[!UICONTROL Campaigns]**.

1. Mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Edite cualquiera de las [configuraciones de campaña](#campaign-settings), [configuraciones de grupo de anuncios](#ad-group-settings) y [configuraciones de anuncios](#ad-settings).

1. Haga clic en **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] configuración de campaña de anuncios conversacionales {#campaign-settings}

**[!UICONTROL Campaign name]:** Un nombre único para la campaña. El nombre debe incluir al menos tres caracteres.

**[!UICONTROL Campaign type]:** (solo lectura) *Estándar* es el único tipo disponible.

**[!UICONTROL Objective]:** Métrica en la que se debe enfocar la campaña: *Alcanzar* o *Clics*. El objetivo determina el tipo de oferta para los grupos de publicidad de la campaña.

**[!UICONTROL Locations]:** (opcional) una o más ubicaciones específicas para el destino. Para segmentar todas las ubicaciones, deje esta configuración vacía. Para especificar una ubicación específica, escriba al menos dos letras que aparezcan en cualquier parte dentro del nombre y, a continuación, haga clic en el nombre dentro de los resultados de búsqueda.

**[!UICONTROL Budget type]:** *Presupuesto diario* o *Presupuesto de por vida*.

**[!UICONTROL Budget]:** El presupuesto para el tipo de presupuesto especificado. El valor debe ser mayor que cero (0).

**[!UICONTROL Start date]:** Fecha en la que comienza la campaña, en la zona horaria de la cuenta.

**[!UICONTROL Set an end date]:** (opcional) le permite especificar una fecha de finalización para la campaña. Cuando seleccione esta opción, especifique **[!UICONTROL End date]**.

## Grupos de anuncios

### Crear un grupo de anuncios [!DNL ChatGPT Ads] para una campaña existente {#ad-group-create}

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En el submenú, haga clic en la ficha **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, seleccione un anunciante y una cuenta de [!DNL ChatGPT Ads].

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]>[!UICONTROL Ad Group]**.

1. Especifique la [configuración del grupo de anuncios](#ad-group-settings), incluida la campaña principal.

1. Haga clic en **[!UICONTROL Create ad group]**.

## Editar un grupo de anuncios [!DNL ChatGPT Ads] {#ad-group-edit}

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En el submenú de la izquierda, haga clic en **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, seleccione un anunciante y una cuenta de [!DNL ChatGPT Ads].

1. Sobre la tabla de datos, haga clic en la ficha **[!UICONTROL Ad Groups]**.

1. Mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Editar la configuración de [grupo de anuncios](#ad-group-settings).

1. Haga clic en **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] configuración del grupo de anuncios {#ad-group-settings}

**[!UICONTROL Parent campaign]:** (Grupos de anuncios solo para campañas existentes) La campaña a la que pertenece el grupo de anuncios.

**[!UICONTROL Ad group name]:** Un nombre único para el grupo de anuncios. El nombre debe incluir al menos tres caracteres.

**[!UICONTROL Maximum CPC bid]** o **[!UICONTROL Maximum CPM bid]:** La cantidad máxima que pagarás por cada clic o por 1.000 impresiones. El valor debe ser mayor que cero (0). El objetivo de la campaña determina el campo de oferta: *Clics* campañas muestran **[!UICONTROL Maximum CPC bid]**, y *Alcanzar* campañas muestran **[!UICONTROL Maximum CPM bid]**.

>[!TIP]
>
>Las pujas más altas pueden ganar más subastas.

**[!UICONTROL Context hints]:** (opcional) una descripción de las conversaciones, temas o palabras clave para los que sus productos o servicios son relevantes. Estas sugerencias guían la coincidencia, pero no son reglas de segmentación de coincidencia exacta.

## Anuncios

### Crear un anuncio de tarjeta de chat [!DNL ChatGPT Ads] para un grupo de anuncios existente {#ad-create}

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En el submenú, haga clic en la ficha **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, seleccione un anunciante y una cuenta de [!DNL ChatGPT Ads].

1. En la esquina superior derecha, haga clic en **[!UICONTROL Create]>[!UICONTROL Ad]**.

1. Especifique la [configuración de publicidad](#ad-settings), incluida la campaña principal y el grupo de publicidad.

1. Haga clic en **[!UICONTROL Create ad]**.

## Editar un anuncio de tarjeta de chat [!DNL ChatGPT Ads] {#ad-edit}

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En el submenú de la izquierda, haga clic en **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, seleccione un anunciante y una cuenta de [!DNL ChatGPT Ads].

1. Sobre la tabla de datos, haga clic en la ficha **[!UICONTROL Ads]**.

1. Mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Editar la configuración de [ad](#ad-settings).

1. Haga clic en **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] configuración de anuncios de tarjetas de chat {#ad-settings}

**[!UICONTROL Parent campaign]** y **[!UICONTROL Parent ad group]:** (anuncios solo en grupos de anuncios existentes) La campaña y el grupo de anuncios al que pertenece el anuncio.

**[!UICONTROL Ad name]:** Un nombre único para el anuncio. El nombre debe incluir al menos tres caracteres.

**[!UICONTROL Ad URL (Link)]:** La dirección URL de la página de aterrizaje, que comienza por `http://` o `https://`.

**[!UICONTROL Title (headline)]:** El titular del anuncio. El título debe tener entre 3 y 50 caracteres. **Nota:** El título puede truncarse en algunos tipos de ubicación.

**[!UICONTROL Description]:** Texto del cuerpo del anuncio. La descripción debe tener entre 3 y 100 caracteres.

**[!UICONTROL Ad image]:** Una imagen JPG o PNG para incluir en el anuncio. Para cargar una imagen, haga clic en (anuncios nuevos) **[!UICONTROL Upload image (PNG/JPG)]** o **[!UICONTROL Change image]** y, a continuación, busque y seleccione un archivo en su dispositivo o red.

**[!UICONTROL Preview]:** Una vista previa del anuncio, basada en la configuración del anuncio.

## Activar o pausar una campaña, un grupo de anuncios o un anuncio de [!DNL ChatGPT Ads] {#pause-activate}

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En el submenú de la izquierda, haga clic en **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, seleccione un anunciante y una cuenta de [!DNL ChatGPT Ads].

1. En la ficha **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** o **[!UICONTROL Ads]**, busque la fila.

1. En la columna **[!UICONTROL Active]**, realice una de las siguientes acciones:

   * Para activar un elemento en pausa, active la opción (a la derecha).

   * Para pausar un elemento activo, desactive la opción (a la izquierda).

## Archivar una campaña, un grupo de anuncios o un anuncio de [!DNL ChatGPT Ads] {#archive}

El archivado elimina permanentemente la campaña, el grupo de anuncios o el anuncio de las vistas de [!UICONTROL Conversational Ads].

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En el submenú de la izquierda, haga clic en **[!UICONTROL Campaigns]**.

1. En la esquina superior derecha, seleccione un anunciante y una cuenta de [!DNL ChatGPT Ads].

1. En la ficha **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** o **[!UICONTROL Ads]**, mantenga el cursor sobre la fila y haga clic en **[!UICONTROL ...]>[!UICONTROL Archive]**.

## Explorar en profundidad desde [!DNL ChatGPT Ads] campañas hasta grupos de anuncios y anuncios {#drill-down}

* Haga clic en una fila de campaña para ver solamente sus grupos de anuncios en la ficha **[!UICONTROL Ad Groups]**, o haga clic en una fila de grupo de anuncios para ver solamente sus anuncios en la ficha **[!UICONTROL Ads]**.

Para quitar el filtro y ver todas las filas de la vista, haga clic en **X** en el filtro situado encima de la tabla de datos.

## Actualizar la campaña, el grupo de anuncios o la lista de anuncios {#refresh}

Volver a mostrar la lista de campañas, grupos de anuncios o anuncios cuando otros usuarios hayan realizado cambios o adiciones.

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En la vista **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** o **[!UICONTROL Ads]**, haga clic en **[!UICONTROL Refresh]** sobre la tabla de datos.

>[!MORELIKETHIS]
>
>* [Administrar cuentas de anuncios conversacionales](account-manage.md)
