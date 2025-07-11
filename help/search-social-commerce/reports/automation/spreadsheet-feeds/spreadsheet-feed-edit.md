---
title: Editar configuración de fuente de informes de hoja de cálculo
description: Obtenga información sobre cómo editar la configuración de las fuentes de hojas de cálculo.
exl-id: 8ca36006-4038-404b-aaf9-66dc3e9ddcf6
feature: Search Reports
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---

# Editar configuración de fuente de informes de hoja de cálculo

*Solo para informes básicos e informes de precisión de modelo*

Puede cambiar la plantilla de informe, la plantilla [!DNL Microsoft Excel] y otros parámetros que se utilizarán para una fuente de hoja de cálculo.

>[!NOTE]
>
> Si edita las columnas de la plantilla de informe o utiliza una plantilla de informe nueva o actualizada, debe actualizar la plantilla [!DNL Excel] en consecuencia y volver a cargarla.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Spreadsheet Feeds]**.

1. (Opcional) Para actualizar la plantilla de informe o la plantilla [!DNL Excel] utilizada para la fuente de hoja de cálculo:

   * (Opcional) Para usar una plantilla de informe diferente o actualizada para la fuente, [cree una nueva [!DNL Excel] plantilla para la plantilla de informe](spreadsheet-feed-create-excel-template.md).

     En el siguiente paso, tendrá que cargar la plantilla de informe y el nuevo archivo [!DNL Excel].

   * (Opcional) Para agregar simplemente columnas personalizadas a la plantilla [!DNL Excel], inserte las columnas a la derecha de las columnas de la plantilla de informe y, a continuación, guarde el archivo como una hoja de cálculo [!DNL Excel] en formato .XLSX. Tendrá que cargar el nuevo archivo de [!DNL Excel] en el siguiente paso.

1. Cambie la configuración de la fuente de hoja de cálculo:

   * En el menú principal, haga clic en **[!UICONTROL Reports]>[!UICONTROL Spreadsheet Feeds]**.

   * Junto al nombre de la fuente de la hoja de cálculo, haga clic en ![Botón Ver/editar configuración](/help/search-social-commerce/assets/settings.png "Botón Ver/editar configuración").

   * En el cuadro de diálogo [!UICONTROL Edit Spreadsheet Feed], cambie la [configuración de fuente de hoja de cálculo](spreadsheet-feed-settings.md).

   * Haga clic en **[!UICONTROL Submit]**.

   * (Opcional) Una vez que [!UICONTROL Update Status] de la fuente sea *[!UICONTROL Finished]*, haga clic en **[!UICONTROL XLSX]** junto a la fuente y, a continuación, abra o guarde el archivo según el procedimiento normal del explorador.

     >[!NOTE]
     >
     > Si la plantilla de informe asociada con la fuente se elimina posteriormente, también se eliminará la fuente.

     Las fuentes de hoja de cálculo se actualizan automáticamente a las 08:00 todos los días en el huso horario del anunciante. Si la plantilla de informe incluye direcciones de cualquier destinatario de correo electrónico, esas direcciones recibirán notificaciones cuando se actualice la hoja de cálculo.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de informes de hoja de cálculo](spreadsheet-feed-about.md)
>* [Crear una fuente de informes de hoja de cálculo](spreadsheet-feed-create.md)
>* [Crear una [!DNL Excel] plantilla para una fuente de informes de hoja de cálculo](spreadsheet-feed-create-excel-template.md)
>* [Editar la configuración de fuentes de informes de hoja de cálculo](spreadsheet-feed-edit.md)
>* [Configuración de fuente de informes de hoja de cálculo](spreadsheet-feed-settings.md)
>* [Ver o guardar un archivo de fuente de informes de hoja de cálculo](spreadsheet-feed-view-or-save.md)
>* [Actualizar manualmente las fuentes de informes de hoja de cálculo](spreadsheet-feed-refresh.md)
