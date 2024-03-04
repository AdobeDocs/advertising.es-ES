---
title: Publicar datos de campaña generados a partir de fuentes en redes de publicidad
description: Obtenga información sobre cómo publicar datos generados a partir de fuentes de datos de inventario en redes de publicidad.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: 6b3c876f17d0e30dcce69048bb4041fc8cd29902
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Publicar datos de campaña generados a partir de fuentes en redes de publicidad

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Puede publicar datos de campaña generados a partir de una fuente a medida que propaga los datos a través de las plantillas asociadas o como un proceso independiente. Una vez que publique los datos, los datos propagados existentes se eliminarán del [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] listas.

Para que la publicación se realice correctamente, todos los grupos de anuncios deben asignarse a campañas, todas las palabras clave y los anuncios deben asignarse a grupos de anuncios y debe incluirse toda la información necesaria sin que se incumplan los requisitos de longitud.

* Si utilizó la opción para &quot;[!UICONTROL Propagate and Preview],&quot; entonces [publicar el archivo de hoja de edición masiva generado](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (denominado &quot;`<feed file name>_<template name>`&quot;) del [!UICONTROL Bulksheets] vista.

  Si no lo ha hecho anteriormente [validación de las páginas de aterrizaje](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), puede hacerlo antes de publicar el archivo.

* Si utilizó la opción para &quot;[!UICONTROL Propagate only],&quot; puede publicar los datos generados para los componentes con el [[!UICONTROL New] status](propagated-data-status.md) dentro de una vista de jerarquía de campañas desde el [!UICONTROL Templates] pestaña.

  >[!NOTE]
  >
  >Los componentes activos o eliminados pueden incluir subcomponentes nuevos, que se pueden publicar si los datos son válidos.

  >[!TIP]
  >
  >Si anteriormente no validó las páginas de aterrizaje y desea hacerlo, [propagar datos y previsualizarlos](feed-data-propagate.md) desde el [!UICONTROL Bulksheets] en lugar de publicarlo en la red de anuncios. Puede hacer lo siguiente [validación de las direcciones URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) antes de publicar manualmente el archivo en la red de publicidad.

   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre a la [!UICONTROL Templates] pestaña.

   1. Seleccione la casilla de verificación situada junto a la plantilla.

   1. En la barra de herramientas, haga clic en **[!UICONTROL Post]**.

   1. En la configuración de contabilización, introduzca o seleccione información en los campos y, a continuación, haga clic en **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Qué componentes de la cuenta se registran.

      * **[!UICONTROL Scheduling]:** Cuándo publicar el archivo:

         * *[!UICONTROL Post to search engine now]* (el valor predeterminado): crea un archivo de hoja de edición masiva a partir de los datos de fuente propagados y comienza a publicarlo inmediatamente.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Crea un archivo de hoja de edición masiva y lo publica más tarde. Especifique lo siguiente:

            * **[!UICONTROL Start Time]:** Una fecha y hora futuras en las que el archivo de hoja de edición masiva debe publicarse en la red publicitaria. De forma predeterminada, el archivo se envía a las 00:00 (12:00 a.m.) del día siguiente. **Nota:** Para los archivos grandes que requieren un procesamiento más largo, los datos publicados no están disponibles inmediatamente en las vistas de administración de campañas ni en el administrador de anuncios de la red.

            * **[!UICONTROL End Time]:** Una fecha y hora futuras en las que los anuncios publicados pueden pausarse o eliminarse en función de la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings) para &quot;[!UICONTROL When the Scheduled End Date is reached].&quot; De forma predeterminada, la hora de finalización es 00:00 (12:00 a.m.) dentro de 30 días a partir de hoy. Seleccionar **[!UICONTROL None]** para mantener los datos activos indefinidamente (o hasta que propague nuevos datos para la plantilla), o especifique una fecha y una hora.

              Para especificar una fecha, utilice el formato DD/MM/AAAA o D/M/AAAA o haga clic en [Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") para abrir el calendario y [seleccionar una fecha](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para cambiar una hora, introdúzcala en formato de 24 horas HH/MM o H/M o seleccione una hora (en intervalos de 30 minutos) de la lista.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Crea un archivo de hoja de edición masiva que está disponible en el [!UICONTROL Search] > [!UICONTROL Bulksheets] vista. Si lo desea, puede publicar el archivo desde allí.

           Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP. No es necesario descomprimir el archivo para publicarlo.

      * **[!UICONTROL Generate Tracking URLs]:** Si se incluyen direcciones URL de seguimiento para palabras clave y variaciones de anuncios en el archivo de hoja de edición masiva: *[!UICONTROL Yes]* (el valor predeterminado) o *[!UICONTROL No]*.

        Si selecciona *[!UICONTROL Yes]*, las direcciones URL se generan a partir de las direcciones URL base para las palabras clave y los anuncios según el [!UICONTROL Tracking Methods] Parámetros de en [configuración de cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) o, si está asignando datos a campañas existentes, a la variable [!UICONTROL Tracking Methods] parámetros en el [configuración de campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Si existen direcciones URL de seguimiento para los elementos relevantes, no se regeneran a menos que se necesiten nuevas (como si el tipo de coincidencia de palabra clave, el texto creativo o los parámetros de seguimiento de la cuenta han cambiado).

      * **[!UICONTROL Bulksheet Name]:** Nombre del archivo de hoja de edición masiva que se va a crear a partir de los datos de fuente propagados. El nombre predeterminado del archivo es `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Puede cambiar el nombre del archivo como desee, pero debe terminar con una de las siguientes extensiones de archivo: `.tsv` (para valores separados por tabulaciones), `.txt` (para texto ASCII), `.csv` (para valores separados por comas), o `.zip` (para un archivo TSV comprimido). Para datos que incluyen caracteres internacionales, utilice el formato TSV o TXT.

        El archivo publicado está disponible en el [!UICONTROL Bulksheets] visualizarlo durante 30 días, lo publique o no en la red de publicidad.

El &quot;[!UICONTROL Last Prop. Status]La columna &quot; muestra el estado del trabajo para las plantillas aplicables.

Cuando se crea la hoja de edición masiva, aparece en la [!UICONTROL Bulksheets] vista. Cuando se publica el archivo, se envía una notificación por correo electrónico con un vínculo al archivo. Sin embargo, si no se pueden publicar todos o algunos de los datos, aparece un archivo de error en la [!UICONTROL Bulksheets] y se envía una notificación por correo electrónico con un vínculo al archivo de error.

>[!NOTE]
>
>* Independientemente de la opción de programación seleccionada, los datos especificados se eliminan del [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], y [!UICONTROL Ads] listas.
>* Las grandes cantidades de datos tardan más en procesarse. Puede seguir el progreso del archivo durante el proceso.
>* Todos los datos publicados están sujetos al proceso editorial de la red.
>* Antes de publicar un archivo de hoja de edición por lotes, puede [cancelar el registro](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Ver datos generados a partir de fuentes](propagated-data-view.md)
>* [Editar datos generados a partir de fuentes](propagated-data-edit.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de los datos generados a partir de las fuentes](propagated-data-status.md)
