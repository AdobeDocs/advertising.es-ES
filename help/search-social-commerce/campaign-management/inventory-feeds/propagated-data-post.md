---
title: Publicar datos de campaña generados a partir de fuentes en redes de publicidad
description: Obtenga información sobre cómo publicar datos generados a partir de fuentes de datos de inventario en redes de publicidad.
exl-id: 7d66c52b-f761-4be2-a1d9-2c63887d7cb7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 0%

---

# Publicar datos de campaña generados a partir de fuentes en redes de publicidad

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Puede publicar datos de campaña generados a partir de una fuente a medida que propaga los datos a través de las plantillas asociadas o como un proceso independiente. Una vez que publique los datos, los datos propagados existentes se eliminarán de las listas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads].

Para que la publicación se realice correctamente, todos los grupos de anuncios deben asignarse a campañas, todas las palabras clave y los anuncios deben asignarse a grupos de anuncios y debe incluirse toda la información necesaria sin que se incumplan los requisitos de longitud.

* Si utilizó la opción para &quot;[!UICONTROL Propagate and Preview]&quot;, [publique el archivo de hoja de edición masiva generado](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-post.md) (denominado &quot;`<feed file name>_<template name>`&quot;) desde la vista [!UICONTROL Bulksheets].

  Si anteriormente no [validó sus páginas de aterrizaje](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md), puede hacerlo antes de publicar el archivo.

* Si utilizó la opción para &quot;[!UICONTROL Propagate only]&quot;, puede publicar los datos generados para los componentes con el estado [[!UICONTROL New] &#x200B;](propagated-data-status.md) dentro de una vista de jerarquía de campaña desde la pestaña [!UICONTROL Templates].

  >[!NOTE]
  >
  >Los componentes activos o eliminados pueden incluir subcomponentes nuevos, que se pueden publicar si los datos son válidos.

  >[!TIP]
  >
  >Si anteriormente no validó sus páginas de aterrizaje y desea hacerlo, [propague los datos y obtenga una vista previa](feed-data-propagate.md) desde la vista [!UICONTROL Bulksheets] en lugar de publicarlos en la red publicitaria. A continuación, puede [validar las direcciones URL](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) antes de publicar manualmente el archivo en la red publicitaria.

   1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, que se abre en la ficha [!UICONTROL Templates].

   1. Seleccione la casilla de verificación situada junto a la plantilla.

   1. En la barra de herramientas, haga clic en **[!UICONTROL Post]**.

   1. En la configuración de envío, escriba o seleccione información en los campos y haga clic en **[!UICONTROL Post]**.

      * **[!UICONTROL Selection]:** Qué componentes de la cuenta se publican.

      * **[!UICONTROL Scheduling]:** Cuándo publicar el archivo:

         * *[!UICONTROL Post to search engine now]* (valor predeterminado): crea un archivo de hoja de edición masiva a partir de los datos de fuentes propagadas y comienza a publicarlo inmediatamente.

         * *[!UICONTROL Post to search engine on these start/end times (in America/Los_Angeles time)]:* Crea un archivo de hoja de edición masiva y lo publica más tarde. Especifique lo siguiente:

            * **[!UICONTROL Start Time]:** Una fecha y hora futuras en las que se debe publicar el archivo de hoja de edición masiva en la red publicitaria. De forma predeterminada, el archivo se envía a las 00:00 (12:00 a.m.) del día siguiente. **Nota:** Para archivos grandes que requieren un procesamiento más largo, los datos publicados no están disponibles inmediatamente en las vistas de administración de campañas ni en el administrador de anuncios de la red.

            * **[!UICONTROL End Time]:** Una fecha y hora futuras en las que se pueden pausar o eliminar los anuncios publicados según la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings) para &quot;[!UICONTROL When the Scheduled End Date is reached]&quot;. De forma predeterminada, la hora de finalización es 00:00 (12:00 a.m.) dentro de 30 días a partir de hoy. Seleccione **[!UICONTROL None]** para mantener los datos activos indefinidamente (o hasta que propague nuevos datos para la plantilla), o especifique una fecha y una hora.

              Para especificar una fecha, usa el formato DD/MM/AAAA o D/M/AAAA o haz clic en ![Calendario](/help/search-social-commerce/assets/calendar.png "Calendario") para abrir el calendario y [seleccionar una fecha](/help/search-social-commerce/common-tasks/navigation-editing-selection/calendar.md). Para cambiar una hora, introdúzcala en formato de 24 horas HH/MM o H/M o seleccione una hora (en intervalos de 30 minutos) de la lista.

         * **[!UICONTROL Preview in Bulksheet Management Area only, post later]:** Crea un archivo de hoja de cálculo en bloque que está disponible en la vista [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Bulksheets]. Si lo desea, puede publicar el archivo desde allí.

           Cuando el archivo de hoja de edición masiva resultante es superior a 2 MB, el archivo está en formato ZIP. No es necesario descomprimir el archivo para publicarlo.

      * **[!UICONTROL Generate Tracking URLs]:** Indica si se deben incluir las direcciones URL de seguimiento para las palabras clave y las variaciones de anuncios en el archivo de hoja de edición masiva: *[!UICONTROL Yes]* (predeterminado) o *[!UICONTROL No]*.

        Si selecciona *[!UICONTROL Yes]*, las direcciones URL se generan a partir de las direcciones URL base para las palabras clave y los anuncios según los parámetros [!UICONTROL Tracking Methods] de la [configuración de la cuenta](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) o, si está asignando datos a campañas existentes, según los parámetros [!UICONTROL Tracking Methods] de la [configuración de la campaña](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

        Si existen direcciones URL de seguimiento para los elementos relevantes, no se regeneran a menos que se necesiten nuevas (como si el tipo de coincidencia de palabra clave, el texto creativo o los parámetros de seguimiento de la cuenta han cambiado).

      * **[!UICONTROL Bulksheet Name]:** Nombre del archivo de hoja de edición masiva que se va a crear a partir de los datos de fuente propagados. El nombre predeterminado del archivo es `<feed file name_file extension>_<feed template name>_<creation date in the format YYYYMMDDHHMMSS>.txt`. Puede cambiar el nombre del archivo como desee, pero debe finalizar con una de las siguientes extensiones: `.tsv` (para valores separados por tabulaciones), `.txt` (para texto ASCII), `.csv` (para valores separados por comas) o `.zip` (para un archivo TSV comprimido). Para datos que incluyen caracteres internacionales, utilice el formato TSV o TXT.

        El archivo publicado estará disponible en la vista [!UICONTROL Bulksheets] durante 30 días, independientemente de si lo publica en la red publicitaria.

La columna &quot;[!UICONTROL Last Prop. Status]&quot; muestra el estado del trabajo para las plantillas aplicables.

Cuando se crea la hoja de edición masiva, aparece en la vista [!UICONTROL Bulksheets]. Cuando se publica el archivo, se envía una notificación por correo electrónico con un vínculo al archivo. Sin embargo, si no se pueden publicar todos o algunos de los datos, aparecerá un archivo de error en la vista [!UICONTROL Bulksheets] y se enviará una notificación por correo electrónico con un vínculo al archivo de error.

>[!NOTE]
>
>* Independientemente de la opción de programación seleccionada, los datos especificados se quitan de las listas [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] y [!UICONTROL Ads].
>* Las grandes cantidades de datos tardan más en procesarse. Puede seguir el progreso del archivo durante el proceso.
>* Todos los datos publicados están sujetos al proceso editorial de la red.
>* Antes de publicar un archivo de hoja de edición masiva, puede [cancelar la publicación](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-stop-job.md).

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](inventory-feeds-about.md)
>* [Ver datos generados a partir de fuentes](propagated-data-view.md)
>* [Editar datos generados a partir de fuentes](propagated-data-edit.md)
>* [Detener un trabajo de registro para los datos de fuente de inventario](stop-job.md)
>* [Estados de datos generados a partir de fuentes](propagated-data-status.md)
