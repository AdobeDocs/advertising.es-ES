---
title: Volver a autenticar un [!DNL Google Analytics] fuente de datos
description: Obtenga información sobre cómo volver a autenticar un [!DNL Google Analytics] fuente de datos si cambia la contraseña asociada o si el certificado caduca.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Volver a autenticar un [!DNL Google Analytics] fuente de datos

*Administradores de agencia, Administradores de cuentas de agencia, Administradores de cuentas de Adobe y Solo administradores*

Si cambia la contraseña de la cuenta de correo electrónico utilizada para una fuente de datos o si la variable [!DNL OAuth] el certificado de la cuenta caduca, todas las conexiones abiertas a la cuenta de correo electrónico se cierran y debe volver a autenticarse para reanudar la sincronización de datos.

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Active la casilla de verificación situada junto al origen de datos que desea volver a autenticar.

1. En la barra de herramientas sobre la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Edite el [configuración de fuente de datos](data-source-settings.md):

   1. En el [!UICONTROL Connect to Google Analytics] , haga lo siguiente.

      1. (Si es necesario) Introduzca una nueva dirección de correo electrónico para acceder a los datos de esta fuente de datos. La dirección de correo electrónico debe estar registrada en un [!DNL Google] y tienen permisos de &quot;lectura y análisis&quot; para la cuenta de [!DNL Google Analytics] cuenta. Consulte la [instrucciones para asignar permisos de usuario en [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para asegurarse de que solo específico [!DNL Google Analytics] Las propiedades y vistas están disponibles en Search, Social y Commerce. Inicie sesión con una dirección de correo electrónico que solo tenga acceso a esas propiedades y vistas.
   1. Seleccione la casilla de verificación para autorizar a Search, Social y Commerce a acceder a las métricas de la cuenta.

   1. Haga clic **[!UICONTROL Re-Authenticate]**.


1. Haga clic **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Acerca de la sincronización [!DNL Google Analytics] métricas de conversión](data-source-about.md)
>* [Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos](data-source-prerequisites.md)
>* [Configurar un [!DNL Google Analytics] ver como fuente de datos](data-source-configure.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [[!DNL Google Analytics] configuración de fuente de datos](data-source-settings.md)
>* [Apéndice: disponible [!DNL Google Analytics] métricas](data-source-ga-metrics.md)

