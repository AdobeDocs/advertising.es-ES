---
title: Configurar un [!DNL Google Analytics] ver como fuente de datos
description: Obtenga información sobre cómo configurar una fuente de datos desde un [!DNL Google Analytics] vista.
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
feature: Search Admin, Search Data Sources
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# Configurar un [!DNL Google Analytics] ver como fuente de datos

*Administradores de agencia, Administradores de cuentas de agencia, Administradores de cuentas de Adobe y Solo administradores*

Puede crear una fuente de datos por [!DNL Google Analytics] combinación de cuenta, propiedad y vista.

Para integrar métricas de varias propiedades o de varias vistas para una sola propiedad, configure una fuente de datos independiente para cada una.

1. [Complete todos los requisitos previos para integrar [!DNL Google Analytics] account](data-source-prerequisites.md).

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Crear](/help/search-social-commerce/assets/add.png "Crear").

1. En el [!UICONTROL Deployment Prerequisites] , active la casilla de verificación para confirmar que la dimensión personalizada requerida &quot;ef_id&quot; está implementada en el [!DNL Google Analytics] y haga clic en **[!UICONTROL Continue]**.

   Es posible que otros roles de su organización hayan cumplido algunos requisitos previos. Si tiene preguntas sobre los requisitos previos, póngase en contacto con el equipo de cuenta de Adobe.

1. Introduzca el [configuración de fuente de datos](data-source-settings.md):

   1. En el **[!UICONTROL Connect to [!DNL Google Analytics]]** , haga lo siguiente.

      1. Introduzca el ID numérico para [!DNL Google Analytics] cuenta.

      1. Introduzca la dirección de correo electrónico que desea utilizar para acceder a los datos de este origen de datos. La dirección de correo electrónico debe estar registrada en un [!DNL Google] y tienen permisos de &quot;lectura y análisis&quot; para la cuenta de [!DNL Google Analytics] cuenta. Consulte la [instrucciones para asignar permisos de usuario en [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para asegurarse de que solo específico [!DNL Google Analytics] Las propiedades y vistas están disponibles en Adobe Advertising. Inicie sesión con una dirección de correo electrónico que solo tenga acceso a esas propiedades y vistas.

         >[!NOTE]
         >
         >Si posteriormente cambia la contraseña de esta cuenta de correo electrónico, se cierran todas las conexiones abiertas a la cuenta de correo electrónico. Para reanudar la sincronización de datos, vuelva a esta página y [volver a autenticar](data-source-reauthenticate.md).

      1. Seleccione la casilla de verificación para autorizar al Adobe Advertising a acceder a las métricas de la cuenta.

      1. Haga clic **[!UICONTROL Authenticate]**.

   1. En el [!UICONTROL Account Details] , especifique la propiedad y la vista de las métricas que desea importar. Además, especifique la dimensión personalizada que se rellena con el valor del parámetro de cadena de consulta &quot;ef_id&quot;.

   1. En el [!UICONTROL Import Metrics] , especifique las métricas que desea incluir en las fuentes.

      No se puede eliminar [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces], o [!UICONTROL Session Duration], que se incluyen automáticamente. Puede añadir hasta 16 métricas válidas adicionales o métricas sin datos.

      >[!WARNING]
      >
      >[!DNL Google Analytics] permite hasta 10 métricas en una sola fuente de datos. Search, Social y Commerce pueden admitir hasta dos fuentes con un total de 20 métricas, pero el uso de una segunda fuente duplica las llamadas de API a [!DNL Google Analytics]. Si tiene muchas métricas, seleccione solo las que desee utilizar en los objetivos de optimización. Ver más sobre [cuotas y límites de llamadas para solicitudes de API a [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. En el [!UICONTROL Metric Tag] , introduzca el nombre de la etiqueta que se anexará a cada métrica para la fuente de datos.

1. En la esquina superior derecha, haga clic en **[!UICONTROL Post]**.

   El origen de datos se denomina &quot;AccountName > PropertyName > ViewName&quot; y se activa automáticamente. Para pausar la fuente de datos, consulte[Pausar una fuente de datos](data-source-pause.md).&quot;

   Las métricas están disponibles al día siguiente de la finalización de la sincronización diaria de datos, que comienza a las 05:00 en el huso horario del anunciante. Una vez que las métricas están disponibles, son visibles en [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). Cada nueva métrica de conversión se denomina &quot;`ga:backEndMetricName_propertyID_viewID`,&quot; donde &quot;backEndMetricName&quot; es el nombre de métrica utilizado por la API. El nombre para mostrar de cada nueva métrica de conversión es &quot;`friendlyMetricName_ga:MetricTag`,&quot; donde &quot;friendlyMetricName&quot; es el nombre de la métrica que aparece en [!DNL Google Analytics] y &quot;MetricTag&quot; es el [!UICONTROL Metric Tag] definido en la configuración de la fuente de datos.

   Puede añadir las métricas directamente a la administración de campañas y a las vistas de administración de portafolios, a los informes y a los objetivos de optimización.

>[!MORELIKETHIS]
>
>* [Acerca de la sincronización [!DNL Google Analytics] métricas de conversión](data-source-about.md)
>* [Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos](data-source-prerequisites.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [Volver a autenticar un [!DNL Google Analytics] fuente de datos](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configuración de fuente de datos](data-source-settings.md)
>* [Apéndice: disponible [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
