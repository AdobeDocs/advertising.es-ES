---
title: Configuración de cuentas de red de publicidad para la carga de datos
description: Obtenga información acerca de cómo configurar y administrar los detalles de cuenta para una cuenta de red de publicidad.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---

# Administración de cuentas de red de anuncios para cargas de datos

<!-- Edit all, including title and metadata -->

A continuación se indican instrucciones para administrar los detalles de cuenta de las cuentas de red de anuncios para las que se cargarán los datos de cuenta.

Para obtener detalles acerca de la funcionalidad disponible para cada red de anuncios, consulte &quot;[Inventario compatible](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

>[!NOTE]
>
>Para obtener instrucciones acerca de cómo administrar los detalles de cuenta de una cuenta de red de anuncios que Search, Social y Commerce sincroniza mediante la API de la red de anuncios, consulte &quot;[Administrar cuentas de red de anuncios mediante la conexión de API](../api-accounts/api-account-manage.md)&quot; en su lugar.

## Crear detalles de la cuenta {#create-account}

1. Haga clic en **[!UICONTROL Create Account]**.

1. Haga clic en el nombre de la red publicitaria y, a continuación, haga clic en **[!UICONTROL Next]**.

1. Especifique la [configuración de la cuenta](#account-settings):

   1. En la ficha **[!UICONTROL Account Details]**, edite los detalles de la cuenta.

   1. (Anunciantes con una integración de [[!DNL Adobe Analytics for Advertising]] (/help/integrations/analytics/overview.md)) Haga clic en la ficha **[!UICONTROL Set up Adobe Analytics]** y edite los grupos de informes [!DNL Analytics] que se utilizarán para el seguimiento y la creación de informes de la actividad de la campaña.

   1. (Opcional) En la ficha **[!UICONTROL Upload File]**, cargue los archivos de datos de la cuenta.

1. Haga clic en **[!UICONTROL Save]**.

## Editar detalles de la cuenta {#edit-account}

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Seleccione la cuenta de cualquiera de las siguientes maneras:

   * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

   * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

1. Editar la [configuración de la cuenta](#account-settings-upload):

   1. (Opcional) En la ficha **[!UICONTROL Account Details]**, edite los detalles de la cuenta.

   1. (Opcional; anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md)) Haga clic en la ficha **[!UICONTROL Set up Adobe Analytics]** y edite los [!DNL Analytics] grupos de informes que quiera usar para rastrear y generar informes sobre la actividad de la campaña.

   1. (Opcional) En la ficha **[!UICONTROL Upload File]**, cargue los archivos de datos de la cuenta.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Haga clic en **[!UICONTROL Save]**.

## Habilitar o deshabilitar las cuentas de red de publicidad {#enable-disable-account}

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Realice una de las acciones siguientes:

   * (Desde la vista [!UICONTROL Accounts]):

      * (Para habilitar la cuenta) Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Activate]** en la barra de herramientas de acciones en masa.

      * (Para deshabilitar la cuenta) Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Pause]** en la barra de herramientas de acciones en masa.

   * (Desde la configuración de la cuenta):

      1. Seleccione la cuenta de cualquiera de las siguientes maneras:

         * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

         * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

      1. En la ficha **[!UICONTROL Account Details]**, desactive **[!UICONTROL Account enabled]**.

      1. Haga clic en **[!UICONTROL Save]**.

## Configuración de cuenta {#account-settings-upload}

### Ficha [!UICONTROL Account Details]

**[!UICONTROL Account Name]:** Nombre que se mostrará para la cuenta en Search, Social y Commerce.

>[!NOTE]
>
>Si tiene una integración de Search, Social y Commerce-Adobe Analytics y cambia el nombre de la cuenta de búsqueda, notifique al equipo de cuenta de Adobe para que pueda actualizar la asignación.

**[!UICONTROL Network Account ID]:** Identificador de cuenta asignado por la red de publicidad. Este ID solo se utiliza para los informes. Search, Social y Commerce no se conectarán directamente a la cuenta de la red de publicidad.

**[!UICONTROL Currency]:** (solo lectura para cuentas existentes) La abreviatura de la moneda utilizada para la cuenta.

**[!UICONTROL Time Zone]:** (solo lectura para cuentas existentes) Zona horaria del anunciante.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social y Commerce permiten la captura automatizada de datos para un bloque de S3 especificado.

## Ficha [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (Anunciantes con una [[!DNL Adobe Analytics for Advertising] integración](/help/integrations/analytics/overview.md); opcional) Uno o más grupos de informes de Analytics a los que Search, Social y Commerce envían datos que se cargan para la red de anuncios, incluidas las clasificaciones de entidades y los datos de clics de la cuenta.

Para que los datos aparezcan en los grupos de informes, ya sea (a) la función de ID de AMO del lado del servidor debe estar configurada para la cuenta o (b) la configuración de nivel de anunciante a &quot;[!UICONTROL Enable Advertising reporting in Analytics]&quot; debe estar habilitada. Además, la cuenta del anunciante [!DNL Analytics] debe estar configurada para recibir datos de Search, Social y Commerce. Para obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

### Ficha [!UICONTROL Upload File]

(Opcional) Cargue archivos de datos para la cuenta.<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
