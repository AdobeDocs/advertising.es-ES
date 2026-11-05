---
title: (Nueva IU) Administrar fuentes de informes de hojas de cálculo
description: Obtenga información sobre cómo crear, configurar, actualizar, ver y eliminar fuentes de informes de hojas de cálculo que ofrecen datos de rendimiento diarios en una hoja de cálculo con formato personalizado.
feature: Search Reports
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
source-git-commit: b0691683d8b9a02169920645c4220c3737cb9bd9
workflow-type: tm+mt
source-wordcount: '1632'
ht-degree: 0%
---
# (Nueva IU) Administrar fuentes de informes de hojas de cálculo

*Solo para informes básicos e informes de precisión de modelo*

<!-- Update link to notifications once available -->

Las fuentes de hoja de cálculo proporcionan datos de rendimiento diarios para todos los informes básicos y de precisión de modelo en un formato de hoja de cálculo personalizado en XLSX [!DNL Microsoft Excel]. Puede configurar fuentes de hojas de cálculo utilizando [!DNL Excel] plantillas de hoja de cálculo con formato especial que cree a partir de plantillas de informe normales. Cada día, la hoja de cálculo se actualiza automáticamente a una hora especificada con nuevos datos sin procesar que se agregan diariamente. Los datos sin procesar rellenan cualquier columna y gráfico que haya incluido en la plantilla de hoja de cálculo. Una vez que haya disponible un archivo de fuente de hoja de cálculo, o si falla la generación del archivo, cada destinatario de correo electrónico especificado en la configuración de fuente de hoja de cálculo recibe una notificación, según la configuración de [notificación para los informes](/help/search-social-commerce/notifications/notification-about.md) establecida por el usuario.

Puede configurar la fuente para que se actualice hasta los últimos 90 días de datos, y todos los datos existentes anteriores se seguirán acumulando.

La vista [!UICONTROL Reports] > [!UICONTROL Spreadsheet Feeds] enumera todas las fuentes de hoja de cálculo que ha creado. Desde esta vista, puede crear, editar, actualizar manualmente o eliminar fuentes de hoja de cálculo, ver la configuración de la plantilla de informe asociada y copiar los datos de fila seleccionados.

## Acciones disponibles

* [Crear una  [!DNL Excel] plantilla para una fuente de informes de hoja de cálculo](#spreadsheet-feed-create-excel-template)

* [Crear una fuente de informes de hoja de cálculo](#spreadsheet-feed-create)

* [Editar configuración de fuente de informes de hoja de cálculo](#spreadsheet-feed-edit)

* [Ver la configuración de la plantilla de informe asociada](#spreadsheet-feed-view-template)

* [Ver o guardar un archivo de fuente de informes de hoja de cálculo](#spreadsheet-feed-view-or-save)

* [Actualizar manualmente fuentes de informes de hoja de cálculo](#spreadsheet-feed-refresh)

* [Eliminar fuentes de informes de hoja de cálculo](#spreadsheet-feed-delete)

* [Copiar todos los datos de las filas seleccionadas en el portapapeles](#copy-to-clipboard)

## Crear una plantilla [!DNL Excel] para una fuente de informes de hoja de cálculo {#spreadsheet-feed-create-excel-template}

Para crear fuentes de hoja de cálculo, primero debe crear [!DNL Microsoft Excel] plantillas de hoja de cálculo con formato especial usando [plantillas de informe](report-templates-manage.md) normales. Opcionalmente, puede personalizar la hoja de cálculo [!DNL Excel] para incluir columnas y gráficos adicionales.

1. En **[!UICONTROL Reports]>[!UICONTROL Reports]**, genere el tipo de informe deseado con una unidad [!UICONTROL Date Aggregation] de &quot;[!UICONTROL Daily]&quot; y con todos los demás parámetros de datos que desee, guardando el informe como plantilla.

   >[!NOTE]
   >
   > * Puede crear fuentes de hoja de cálculo para los informes [!UICONTROL Portfolio], [!UICONTROL Search Engine], [!UICONTROL Search Engine Account], [!UICONTROL Campaign], [!UICONTROL Ad Group], [!UICONTROL Ad Variation], [!UICONTROL Keyword] y [!UICONTROL Forecast Accuracy]. Si usa el [!UICONTROL Ad Group Report], limite el número de grupos de publicidad incluidos para obtener resultados más rápidos.
   > * No se utiliza la unidad [!UICONTROL Date Range] definida en la plantilla. Cuando configure la fuente de la hoja de cálculo más adelante, definirá las fechas en las que desea actualizar los datos.

1. Una vez generado el informe, vaya a **[!UICONTROL Reports]>[!UICONTROL Reports]** y exporte una versión TSV o XLS del resultado del informe a un archivo.

1. En [!DNL Excel], cree una plantilla personalizada para el informe:

   1. Abra el archivo de informe en [!DNL Excel].

   1. Prepare el libro:

      1. Elimine las filas superiores que muestran los parámetros del informe. Para archivos XLS, elimine también la fila &quot;[!UICONTROL Total]&quot;. Si lo desea, puede eliminar algunas de las filas de datos, pero mantenga a) la fila del encabezado de datos con todas las columnas en el orden original y b) al menos una fila de datos. No agregue manualmente ningún dato.

         >[!NOTE]
         >
         > La última columna debe incluir valores distintos de cero.

      1. Ordene los datos por fecha de inicio en orden ascendente (de la más antigua a la más reciente).

      1. Cambie el nombre de la ficha de hoja de cálculo de &quot;[!UICONTROL Sheet1]&quot; a &quot;[!UICONTROL RAW]&quot;.&quot;

         Este nombre de ficha específico permite actualizar los datos.

      1. (Opcional) Agregue columnas personalizadas a la derecha de las columnas de la plantilla del informe, según sea necesario.

   1. (Opcional) En una hoja de cálculo independiente, cree una tabla dinámica. Una vez finalizado, haga clic con el botón derecho en cualquier celda de la tabla dinámica y seleccione **[!UICONTROL Pivot Table Options]**, haga clic en la ficha **[!UICONTROL Data]** y, a continuación, seleccione **[!UICONTROL Refresh data when opening the file]**.

   1. Guarde el archivo como una hoja de cálculo de [!DNL Excel] en formato .XLSX.

## Crear una fuente de informes de hoja de cálculo {#spreadsheet-feed-create}

1. [Cree la  [!DNL Excel] plantilla para rellenar con los datos del informe](#spreadsheet-feed-create-excel-template).

1. Cree la fuente de la hoja de cálculo:

   1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   1. En la esquina superior derecha, haga clic en **[!UICONTROL Create Spreadsheet]**.

   1. En el cuadro de diálogo **[!UICONTROL Create Spreadsheet Feed]**, especifique la [configuración de fuente de hoja de cálculo](#spreadsheet-feed-settings).

   1. Haga clic en **[!UICONTROL Submit]**.

   1. (Opcional) Una vez que [!UICONTROL Update Status] de la fuente sea *[!UICONTROL Finished]*, haga clic en **[!UICONTROL XLSX]** junto a la fuente y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador.

      >[!NOTE]
      >
      >Si la plantilla de informe asociada con la fuente se elimina posteriormente, también se eliminará la fuente.

      Las fuentes de hoja de cálculo se actualizan automáticamente todos los días a las [!UICONTROL Schedule Time] configuradas. Las direcciones especificadas en la configuración [!UICONTROL Email Recipients] de la fuente reciben notificaciones cuando se actualiza la hoja de cálculo.

## Editar configuración de fuente de informes de hoja de cálculo {#spreadsheet-feed-edit}

>[!NOTE]
>
> Si edita las columnas de la plantilla de informe o utiliza una plantilla de informe nueva o actualizada, debe actualizar la plantilla [!DNL Excel] en consecuencia y volver a cargarla.

1. (Opcional) Para actualizar la plantilla de informe o la plantilla [!DNL Excel] utilizada para la fuente de hoja de cálculo:

   * (Opcional) Para usar una plantilla de informe diferente o actualizada para la fuente, [cree una nueva [!DNL Excel] plantilla para la plantilla de informe](#spreadsheet-feed-create-excel-template).

     Seleccionará la plantilla de informe y cargará el nuevo archivo [!DNL Excel] en los pasos siguientes.

   * (Opcional) Para agregar simplemente columnas personalizadas a la plantilla [!DNL Excel], inserte las columnas a la derecha de las columnas de la plantilla de informe y, a continuación, guarde el archivo como una hoja de cálculo [!DNL Excel] en formato .XLSX. Tendrá que cargar el nuevo archivo de [!DNL Excel] en el siguiente paso.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Cambie la configuración de la fuente de hoja de cálculo:

   1. Seleccione la casilla de verificación situada junto al nombre de la fuente de la hoja de cálculo.

   1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Edit]**.

   1. En el cuadro de diálogo **[!UICONTROL Edit Spreadsheet Feed]**, cambie la [configuración de fuente de hoja de cálculo](#spreadsheet-feed-settings).

   1. Haga clic en **[!UICONTROL Submit]**.

   1. (Opcional) Una vez que [!UICONTROL Update Status] de la fuente sea *[!UICONTROL Finished]*, haga clic en **[!UICONTROL XLSX]** junto a la fuente y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador.

   >[!NOTE]
   >
   > Si la plantilla de informe asociada con la fuente se elimina posteriormente, también se eliminará la fuente.

   Las fuentes de hoja de cálculo se actualizan automáticamente todos los días en el(la) [!UICONTROL Schedule Time] configurado(a) en el huso horario del anunciante. Las direcciones especificadas en la configuración [!UICONTROL Email Recipients] de la fuente reciben notificaciones cuando se actualiza la hoja de cálculo.

## Configuración de fuente de informe de hoja de cálculo {#spreadsheet-feed-settings}

| Campo | Descripción |
|---|---|
| [!UICONTROL Feed Name] | Nombre de la fuente de la hoja de cálculo, con un máximo de 120 caracteres. |
| [!UICONTROL Report Template] | La plantilla de informe que especifica los datos de informe requeridos; seleccione la que utilizó para crear la plantilla [!DNL Excel]. Se muestran todas las plantillas de informe básicas.<br><br><b>Nota:</b> Si cambia la plantilla de informe utilizada para el informe o actualiza las columnas de la plantilla, debe crear y cargar una nueva plantilla [!DNL Excel]. |
| [!UICONTROL Excel Template] | La plantilla [!DNL Excel] con formato especial que creó en formato .XLSX, que se aplica a los datos especificados en la plantilla de informe. Haga clic en <b>[!UICONTROL Choose file]</b> para localizar el archivo que desea cargar. |
| [!UICONTROL Back Fill From] | La fecha inicial en la que se actualizaron los datos existentes en la ficha [!UICONTROL RAW], representada por un número de días pasados. Escriba un valor comprendido entre 1 y 90 que sea mayor que [!UICONTROL Back Fill Until]; el valor predeterminado es de siete (7) días.<br><br>Por ejemplo, si el valor es 7 y hoy es 7 de marzo, los datos existentes en la ficha [!UICONTROL RAW] que comienzan por 1 de marzo se actualizarán (hasta la fecha de finalización especificada por el parámetro [!UICONTROL Back Fill Until]). Las filas de datos existentes para fechas anteriores al 1 de marzo no se eliminan, pero no se actualizan. |
| [!UICONTROL Back Fill Until] | La fecha de finalización en la que se actualizaron los datos existentes en la ficha [!UICONTROL RAW], representada por un número de días pasados. Escriba un valor comprendido entre 1 y 90 que sea menor que [!UICONTROL Back Fill From]. El valor predeterminado es un (1) día.<br><br>Por ejemplo, si este valor es 1 y hoy es 7 de marzo, los datos existentes en la ficha [!UICONTROL RAW] se actualizarán hasta el 6 de marzo (y a partir de la fecha de inicio especificada por el parámetro [!UICONTROL Back Fill From]). Si este valor es 1, el parámetro [!UICONTROL Back Fill From] es 7 y hoy es 7 de marzo, los datos existentes en la ficha [!UICONTROL RAW] se actualizarán del 1 al 6 de marzo. En ambos ejemplos, las filas de datos existentes para las fechas posteriores al 6 de marzo no se eliminan, pero no se actualizan. |
| [!UICONTROL Email Recipients] | Direcciones de correo electrónico a las que se envían notificaciones cada vez que se actualiza la fuente de la hoja de cálculo. De forma predeterminada, se introduce la dirección de la cuenta de usuario. Para especificar varias direcciones, sepárelas con comas, espacios o líneas nuevas. |
| [!UICONTROL Schedule Time] | Hora a la que se actualiza la fuente de la hoja de cálculo cada día en el huso horario del anunciante. Seleccione una hora de entre las opciones disponibles. El valor predeterminado para las nuevas fuentes de hoja de cálculo es 10:00. |
| [!UICONTROL Email Notification] | Qué se debe incluir en las notificaciones por correo electrónico a las direcciones especificadas:<ul><li><i>[!UICONTROL Attach Feed (Max 10MB)]</i> — Para enviar una copia del informe completado en formato XLSX. Si el archivo tiene más de 10 MB, la notificación no incluye ningún archivo adjunto.</li><li><i>[!UICONTROL Notification Only]</i> (valor predeterminado): para enviar solamente una notificación de la finalización o el error del informe, con un vínculo al informe.</li></ul> |

## Ver la configuración de la plantilla de informe asociada {#spreadsheet-feed-view-template}

El icono de engranaje **[!UICONTROL Template Settings]** abre un duplicado de la plantilla de informe asociada a la fuente. Al abrir el duplicado, no se guarda una plantilla nueva ni se cambia la plantilla asociada de la fuente.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Haga clic en el icono de engranaje **[!UICONTROL Template Settings]** junto al nombre de la plantilla de informe asociada.

1. Revise la configuración del informe.

1. Haga clic en **[!UICONTROL Cancel]** cuando haya terminado. Si se le solicita que descarte la instalación, haga clic en **[!UICONTROL Discard]**.

Para cambiar la plantilla de informe original, siga el [procedimiento de edición de plantillas de informe](report-templates-manage.md#template-edit). Para usar una plantilla diferente para la fuente, [edite la configuración de la fuente de la hoja de cálculo](#spreadsheet-feed-edit) y seleccione la plantilla.

## Ver o guardar un archivo de fuente de informes de hoja de cálculo {#spreadsheet-feed-view-or-save}

Puede ver cualquier fuente de hoja de cálculo generada o guardarla en un archivo. Los archivos de fuente de hoja de cálculo están en formato XLSX [!DNL Microsoft Excel].

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Haga clic en **[!UICONTROL XLSX]** junto a la fuente y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador.

## Actualizar manualmente fuentes de informes de hoja de cálculo {#spreadsheet-feed-refresh}

>[!NOTE]
>
>Las fuentes de hoja de cálculo se actualizan automáticamente todos los días en el(la) [!UICONTROL Schedule Time] configurado(a) en el huso horario del anunciante.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Active la casilla de verificación situada junto a cada fuente que desee actualizar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Run Spreadsheet]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

1. (Opcional) Una vez que [!UICONTROL Update Status] de una fuente sea *[!UICONTROL Finished]*, haga clic en **[!UICONTROL XLSX]** junto a la fuente y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador.

## Eliminar fuentes de informes de hoja de cálculo {#spreadsheet-feed-delete}

>[!NOTE]
>
>Si se elimina la plantilla de informe asociada a una fuente, esta se eliminará automáticamente.

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Active la casilla de verificación situada junto a cada fuente que desee eliminar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

## Copiar todos los datos de las filas seleccionadas en el portapapeles {#copy-to-clipboard}

Copie la información visible en las filas seleccionadas, según los filtros aplicados y las columnas visibles en la vista. La información se guarda como valores separados por tabulaciones (TSV).

1. En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

1. Active la casilla de verificación situada junto a cada fila cuyos datos desee copiar.

1. En la barra de herramientas de acciones masivas, haga clic en **[!UICONTROL Copy]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.
