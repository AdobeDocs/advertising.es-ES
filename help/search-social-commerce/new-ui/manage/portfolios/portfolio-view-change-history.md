---
title: (Nueva IU) Ver el historial de cambios de un portafolio y el historial de cambios de ofertas
description: Obtenga información sobre cómo ver cambios de portafolios e historial de cambios de ofertas, cambiar intervalos de fechas, filtrar cambios de portafolios y generar, descargar y eliminar informes de historial en Adobe Advertising Search, Social y Commerce.
feature: Search Portfolios, Search Optimization
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
source-git-commit: e7e0221adbb72127a9e6d2354b6a235b233a4a76
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 0%
---
# (Nueva IU) Ver el historial de cambios de un portafolio y el historial de cambios de ofertas

*característica de Beta*

Puede ver un registro de los cambios realizados en el portafolio durante cualquier intervalo de fechas. Las acciones registradas incluyen la creación de la cartera, todos los cambios en la configuración de la cartera, todas las campañas asignadas o no asignadas a la cartera, todas las restricciones aplicadas o eliminadas de las unidades de oferta de la cartera, todas las restricciones de las unidades de oferta de la cartera que han caducado y otras acciones que afectan a la cartera.

El cuadro de diálogo [!UICONTROL Change History] incluye una ficha [!UICONTROL Portfolio Change History] para los cambios del portafolio y una ficha [!UICONTROL Portfolio Bid Change History] para el historial de ofertas. De forma predeterminada, ambas pestañas muestran los últimos 180 días, que finalizan ayer.

Puede filtrar los cambios del portafolio por categoría y cambiar el intervalo de fechas en cualquiera de las pestañas. También puede descargar los datos en un archivo de hoja de cálculo.

## Ver el historial de cambios de un portafolio {#portfolio-change-history}

La información de cada cambio incluye [!UICONTROL Change Date], [!UICONTROL Changed By], [!UICONTROL Change Type] y [!UICONTROL Description]. Los cambios se muestran de más recientes a más antiguos.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Mantenga el cursor sobre la fila del portafolio y haga clic en **[!UICONTROL ...]>[!UICONTROL Change History]**.

1. En el cuadro de diálogo [!UICONTROL Change History], vea la ficha **[!UICONTROL Portfolio Change History]**.

1. (Opcional) Cambie la información que se muestra:

   * Haga clic en ![Calendario](/help/search-social-commerce/assets/calendar-new.png "Calendario") para cambiar el intervalo de fechas del informe.

   * Haga clic en ![Filtro](/help/search-social-commerce/assets/filter-new.png "Filtro") para filtrar los datos por categoría: [!UICONTROL All], [!UICONTROL Objective], [!UICONTROL Campaign], [!UICONTROL Target], [!UICONTROL Constraints], [!UICONTROL Optimization Levers] o [!UICONTROL Others].

## Ver el historial de cambios de ofertas de un portafolio {#portfolio-bid-change-history}

1. [Abrir el historial de cambios de la cartera](#portfolio-change-history).

1. Haga clic en la ficha **[!UICONTROL Portfolio Bid Change History]**.

1. (Opcional) Haga clic en ![Calendario](/help/search-social-commerce/assets/calendar-new.png "Calendario") para cambiar el intervalo de fechas.

1. (Opcional) Haga clic en el encabezado de la columna de fecha para ordenar la lista por fecha en orden ascendente o descendente.

Para ver el historial de una unidad de oferta individual, [abra los detalles de la unidad de oferta desde los detalles de rendimiento de la cartera](portfolio-details.md#bid-unit-history). También puede [abrir el historial de unidades de oferta desde la vista [!UICONTROL Keywords]](/help/search-social-commerce/new-ui/manage/keywords/keyword-manage.md#bid-unit-history) cuando la columna [!UICONTROL Bid Unit ID] esté disponible.

## Administrar informes para historiales de cambios de portafolios

Puede descargar información adicional sobre el historial de cambios de un portafolio en un archivo en formato de libro de [!DNL Microsoft Excel] (archivo XLSX). El informe incluye el ID de cambio numérico, los valores antiguos y nuevos, el tipo de cambio (como &quot;añadido&quot; o &quot;modificado&quot;), el tipo de acción (como &quot;Presupuesto&quot; o &quot;Nombre de Portfolio&quot;) y el subtipo, cuando corresponde, la hora y el nombre de usuario.

También puede generar, descargar y eliminar informes desde la ficha [!UICONTROL Portfolio Bid Change History]. La configuración del informe se titula [!UICONTROL Portfolio History] para cambios de portafolio y [!UICONTROL Portfolio Bid History] para el historial de ofertas.

### Generación de un informe con las filas de datos filtradas

1. [Abra el historial de cambios del portafolio](#portfolio-change-history) y, a continuación, haga clic en la ficha cuyos datos desee descargar.

1. En la esquina superior derecha, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe").

1. En la configuración [!UICONTROL Portfolio History] o [!UICONTROL Portfolio Bid History], acepte el nombre de informe predeterminado o escriba uno único y, a continuación, haga clic en **[!UICONTROL Generate]**.

   De manera predeterminada, el nombre del informe incluye el tipo de historial y la fecha y hora en formato `YYYYMMDD_HHmm`, como &quot;portfolioChangeHistory_20260402_1326&quot;. Si el nombre ya existe, se agrega un sufijo numérico.

   El archivo se agrega a la lista [!UICONTROL Recently Generated].

1. (Opcional) Para descargar el archivo una vez que se haya completado, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Descargar un informe completado

1. [Abra el historial de cambios del portafolio](#portfolio-change-history) y, a continuación, haga clic en la ficha desde la que generó el informe.

1. En la esquina superior derecha, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe").

1. En la lista [!UICONTROL Recently Generated] de la configuración de [!UICONTROL Portfolio History] o [!UICONTROL Portfolio Bid History], haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") junto al nombre del archivo.

   El archivo se descarga según el procedimiento normal del explorador.

### Eliminar un informe completado

1. [Abra el historial de cambios del portafolio](#portfolio-change-history) y, a continuación, haga clic en la ficha desde la que generó el informe.

1. En la esquina superior derecha, haga clic en ![Descargar informe](/help/search-social-commerce/assets/download.png "Descargar informe").

1. En la lista [!UICONTROL Recently Generated] de la configuración [!UICONTROL Portfolio History] o [!UICONTROL Portfolio Bid History], haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar") junto al nombre de archivo.

>[!MORELIKETHIS]
>
>* [Crear un portafolio](portfolio-create.md)
>* [(nueva interfaz de usuario) Editar un portafolio](portfolio-edit.md)
>* [(Nueva IU) Ver detalles de rendimiento del portafolio](portfolio-details.md)
>* [(nueva interfaz de usuario) Descargar datos en la vista [!UICONTROL Portfolios]](portfolio-view-report.md)
>* [Acerca de los portafolios](portfolio-about.md)
