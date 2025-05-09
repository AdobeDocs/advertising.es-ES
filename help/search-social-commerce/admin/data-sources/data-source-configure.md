---
title: Configurar una  [!DNL Google Analytics] vista como fuente de datos
description: Obtenga información sobre cómo configurar una fuente de datos desde una vista  [!DNL Google Analytics] .
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# Configurar una vista [!DNL Google Analytics] como origen de datos

*Solo administradores de agencias, administradores de cuentas de agencias, administradores de cuentas de Adobe y administradores*

Puede crear un origen de datos por cada cuenta, propiedad y combinación de vista de [!DNL Google Analytics].

Para integrar métricas de varias propiedades o de varias vistas para una sola propiedad, configure una fuente de datos independiente para cada una.

1. [Cumplir todos los requisitos previos para integrar la [!DNL Google Analytics] cuenta](data-source-prerequisites.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. En el cuadro de diálogo [!UICONTROL Deployment Prerequisites], active la casilla de verificación para confirmar que la dimensión personalizada necesaria &quot;ef_id&quot; está implementada en la cuenta de [!DNL Google Analytics] y, a continuación, haga clic en **[!UICONTROL Continue]**.

   Es posible que otros roles de su organización hayan cumplido algunos requisitos previos. Si tiene alguna pregunta sobre los requisitos previos, póngase en contacto con el equipo de cuenta de Adobe.

1. Escriba la [configuración del origen de datos](data-source-settings.md):

   1. En la sección **[!UICONTROL Connect to [!DNL Google Analytics]]**, haga lo siguiente.

      1. Escriba el identificador numérico de la cuenta [!DNL Google Analytics].

      1. Introduzca la dirección de correo electrónico que desea utilizar para acceder a los datos de este origen de datos. La dirección de correo electrónico debe estar registrada en una cuenta de [!DNL Google] y tener permisos de &quot;lectura y análisis&quot; para la cuenta de [!DNL Google Analytics]. Vea las [instrucciones para asignar permisos de usuario en [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para asegurarse de que solo las propiedades y vistas específicas de [!DNL Google Analytics] estén disponibles en Adobe Advertising, inicie sesión con una dirección de correo electrónico que solo tenga acceso a esas propiedades y vistas.

         >[!NOTE]
         >
         >Si posteriormente cambia la contraseña de esta cuenta de correo electrónico, se cierran todas las conexiones abiertas a la cuenta de correo electrónico. Para reanudar la sincronización de datos, vuelva a esta página y [vuelva a autenticar](data-source-reauthenticate.md).

      1. Seleccione la casilla de verificación para autorizar a Adobe Advertising a acceder a las métricas de la cuenta.

      1. Haga clic en **[!UICONTROL Authenticate]**.

   1. En la sección [!UICONTROL Account Details], especifique la propiedad y la vista de las métricas que desea importar. Además, especifique la dimensión personalizada que se rellena con el valor del parámetro de cadena de consulta &quot;ef_id&quot;.

   1. En la sección [!UICONTROL Import Metrics], especifique las métricas que desea incluir en las fuentes.

      No puede quitar [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] ni [!UICONTROL Session Duration], que se incluyen automáticamente. Puede añadir hasta 16 métricas válidas adicionales o métricas sin datos.

      >[!WARNING]
      >
      >[!DNL Google Analytics] permite hasta 10 métricas en una sola fuente de datos. Search, Social y Commerce pueden admitir hasta dos fuentes con un total de 20 métricas, pero el uso de una segunda fuente duplica las llamadas de API a [!DNL Google Analytics]. Si tiene muchas métricas, seleccione solo las que desee utilizar en los objetivos de optimización. Ver más sobre [cuotas y límites de llamadas para solicitudes de API a [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. En la sección [!UICONTROL Metric Tag], escriba el nombre de la etiqueta que anexará a cada métrica para el origen de datos.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Post]**.

   El origen de datos se denomina &quot;AccountName > PropertyName > ViewName&quot; y se activa automáticamente. Para pausar el origen de datos, consulte &quot;[Pausar una fuente desde un Source de datos](data-source-pause.md)&quot;.

   Las métricas están disponibles al día siguiente de la finalización de la sincronización diaria de datos, que comienza a las 05:00 en el huso horario del anunciante. Una vez que las métricas estén disponibles, se podrán ver en [[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md). Cada nueva métrica de conversión se denomina &quot;`ga:backEndMetricName_propertyID_viewID`&quot;, donde &quot;backEndMetricName&quot; es el nombre de métrica que usa la API. El nombre para mostrar de cada nueva métrica de conversión es &quot;`friendlyMetricName_ga:MetricTag`&quot;, donde &quot;friendlyMetricName&quot; es el nombre de métrica que aparece en [!DNL Google Analytics] y &quot;MetricTag&quot; es el [!UICONTROL Metric Tag] definido en la configuración del origen de datos.

   Puede añadir las métricas directamente a la administración de campañas y a las vistas de administración de portafolios, a los informes y a los objetivos de optimización.

>[!MORELIKETHIS]
>
>* [Acerca de la sincronización [!DNL Google Analytics] métricas de conversión](data-source-about.md)
>* [Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos](data-source-prerequisites.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [Volver a autenticar un [!DNL Google Analytics] origen de datos](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configuración de origen de datos](data-source-settings.md)
>* [Apéndice:  [!DNL Google Analytics] métricas disponibles](data-source-ga-metrics.md)
