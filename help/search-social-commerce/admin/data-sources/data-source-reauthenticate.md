---
title: Volver a autenticar un origen de datos  [!DNL Google Analytics] s
description: Obtenga información sobre cómo volver a autenticar una fuente de datos  [!DNL Google Analytics] si cambia la contraseña asociada o si el certificado caduca.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Volver a autenticar un origen de datos de [!DNL Google Analytics]

*Solo administradores de agencias, administradores de cuentas de agencias, administradores de cuentas de Adobe y administradores*

Si cambia la contraseña de la cuenta de correo electrónico utilizada para un origen de datos o si caduca el certificado [!DNL OAuth] de la cuenta, todas las conexiones abiertas a la cuenta de correo electrónico se cerrarán y deberá volver a autenticarse para reanudar la sincronización de datos.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Active la casilla de verificación situada junto al origen de datos que desea volver a autenticar.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar").

1. Editar la [configuración de origen de datos](data-source-settings.md):

   1. En la sección [!UICONTROL Connect to Google Analytics], haga lo siguiente.

      1. (Si es necesario) Introduzca una nueva dirección de correo electrónico para acceder a los datos de esta fuente de datos. La dirección de correo electrónico debe estar registrada en una cuenta de [!DNL Google] y tener permisos de &quot;lectura y análisis&quot; para la cuenta de [!DNL Google Analytics]. Vea las [instrucciones para asignar permisos de usuario en [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Para asegurarse de que solo las propiedades y vistas específicas de [!DNL Google Analytics] estén disponibles en Search, Social y Commerce, inicie sesión con una dirección de correo electrónico que solo tenga acceso a esas propiedades y vistas.

   1. Seleccione la casilla de verificación para autorizar a Search, Social y Commerce a acceder a las métricas de la cuenta.

   1. Haga clic en **[!UICONTROL Re-Authenticate]**.

1. Haga clic en **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [Acerca de la sincronización [!DNL Google Analytics] métricas de conversión](data-source-about.md)
>* [Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos](data-source-prerequisites.md)
>* [Configurar una [!DNL Google Analytics] vista como fuente de datos](data-source-configure.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [[!DNL Google Analytics] configuración de origen de datos](data-source-settings.md)
>* [Apéndice:  [!DNL Google Analytics] métricas disponibles](data-source-ga-metrics.md)
