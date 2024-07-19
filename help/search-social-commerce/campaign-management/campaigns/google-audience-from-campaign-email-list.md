---
title: Crear una audiencia de  [!DNL Google Ads] customer match a partir de una lista de correo electrónico de Adobe Campaign
description: Aprenda a crear una audiencia afín de clientes de  [!DNL Google Ads] a partir de una lista de correo electrónico de Adobe Campaign existente.
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# Crear una audiencia afín de clientes de [!DNL Google Ads] a partir de una lista de correo electrónico de Adobe Campaign

*[!DNL Google Ads]cuentas elegibles para la coincidencia de clientes solamente*

Puede crear una audiencia afín de clientes de [!DNL Google Ads] a partir de una lista de correo electrónico en Adobe Campaign configurando un vínculo de cuenta y un flujo de trabajo en [!DNL Campaign].

Para ello, necesita tener acceso a su instancia de [!DNL Campaign] y a un archivo XML que contenga el flujo de trabajo necesario, que le proporcionará el equipo de cuenta de Adobe. Las instrucciones pueden variar para las distintas versiones de [!DNL Campaign]. Si es necesario, el equipo de cuenta de Adobe puede ayudarle a configurar el flujo de trabajo en [!DNL Campaign].

1. Obtenga credenciales para una cuenta SFTP proporcionada por Advertising Search, Social y Commerce.

1. En [!DNL Campaign], configure el envío de la lista de correo electrónico a Advertising Search, Social y Commerce:

   1. Cree una [cuenta externa](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) para vincular la cuenta SFTP proporcionada por Search, Social y Commerce:

      1. En el menú de la izquierda, vaya a **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Haga clic en ![Crear cuenta](/help/search-social-commerce/assets/campaign-create-account.png "Crear cuenta").

      1. Introduzca una etiqueta para la cuenta y seleccione **[!UICONTROL SFTP]** como tipo de cuenta.

      1. Escriba la dirección URL y el número de puerto del servidor SFTP [!DNL Adobe], así como el nombre de carpeta, el nombre de usuario y la contraseña del anunciante.

      1. Haga clic en **[!UICONTROL Save]**.

   1. En [!DNL Campaign Client], instale el paquete de datos que incluye el flujo de trabajo necesario para enviar datos por correo electrónico:

      1. En la barra de menús, vaya a **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Seleccione **[!UICONTROL Install a package from a file]** y luego haga clic en **[!UICONTROL Next]**.

      1. Busque el archivo del paquete de datos (`AMO_Workflow.xml`) en el dispositivo o red y, a continuación, haga clic en **[!UICONTROL Next]**.

      1. Haga clic en **[!UICONTROL Start]** y espere a que se instale el flujo de trabajo.

   1. Edite el flujo de trabajo instalado para, opcionalmente, editar los filtros de la consulta de datos e identificar el nuevo nombre de audiencia y la cuenta SFTP externa:

      1. Vaya a **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** y abra el paquete.

      1. (Opcional) Edite cualquiera de los filtros de los datos:

         * En el flujo de trabajo, haga doble clic en la actividad de consulta (como ForkTransition 1).

         * Edite las expresiones de filtro.

         * Haga clic en **[!UICONTROL Finish]**.

      1. Asigne un nombre al segmento:

         * En el flujo de trabajo, haga doble clic en la actividad **[!UICONTROL Data extraction (File)]**.

         * En la ficha **[!UICONTROL Data extraction (File)]**, en el campo **[!UICONTROL File name]**, escriba el nombre del segmento con la extensión &quot;`.added`&quot; (como PaidSubscribers.added).

           El nombre del segmento no debe existir ya. El nombre del segmento distingue entre mayúsculas y minúsculas y debe constar de caracteres ASCII, pero no puede incluir guiones bajos (`_`).

           Sin embargo, si desea agregar el segmento a una cuenta de [!DNL Google Ad] específica, agregue el nombre del segmento con un guion bajo y el identificador de [!UICONTROL User SE Account ID] (ID de búsqueda, social y de Commerce para la cuenta de [!DNL Google Ads], no el identificador de cuenta de red):

           `_<User SE Account ID>`

           Ejemplo: Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >Esta es una excepción a la regla que prohíbe los guiones bajos en el nombre del archivo.

           De lo contrario, el segmento se agregará a todas las cuentas de [!DNL Google Ads] que Search, Social y Commerce están sincronizando para el anunciante.

         * Deje seleccionada la opción **[!UICONTROL Generate an outbound transition]**.

         * Haga clic en **[!UICONTROL Ok]**.

      1. Especifique la cuenta externa a la que desea enviar los datos:

         * En el flujo de trabajo, haga doble clic en la actividad **[!UICONTROL File Transfer]**.

         * En la ficha **[!UICONTROL File Transfer]**, en la sección **[!UICONTROL Remote server]**, seleccione la opción **[!UICONTROL Use an external account]**.

         * En el campo **[!UICONTROL External account]**, seleccione la etiqueta para la cuenta externa que creó en el paso 2.

         * En el campo **[!UICONTROL Server folder]**, seleccione el valor del campo [!UICONTROL Account] para la cuenta externa.

         * (Opcional) En la ficha **[!UICONTROL Schedule]**, especifique una programación diferente para la transferencia de archivos.

           De forma predeterminada, el flujo de trabajo se ejecuta a las 00:00 (medianoche), lo que garantiza que se procesen todos los registros. Para minimizar la latencia, programe el flujo de trabajo para que se ejecute antes de las 18:00.

         * Haga clic en **[!UICONTROL Ok]**.

Search, Social y Commerce comprueban el directorio cada 30 minutos (a las N:30 y N:59, en el huso horario del anunciante), mueven los archivos que encuentran a otra ubicación y, a continuación, crean automáticamente una audiencia a partir de los datos y la envían a Google a las 22:00 (22:00). Search, Social y Commerce siguen buscando actualizaciones (adiciones y restas) en la lista de correo electrónico cada 30 minutos y actualizan la audiencia en [!DNL Google Ads] según corresponda a las 22:00 todos los días.

>[!NOTE]
>
>* Si carga más de una versión de un archivo entre ciclos de procesamiento, se utiliza el archivo más reciente.
>
>* Search, Social y Commerce no almacenan los datos de clientes de sus listas de correo electrónico utilizadas para crear o editar una audiencia de [!DNL Google Ads].
>
>* [!DNL Google Ads] puede tardar un tiempo en procesar las actualizaciones para una audiencia.
>
>* Ver [[!DNL Google Ads] documentación sobre cómo funciona la coincidencia de clientes y las limitaciones](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Crear [!DNL Google Ads] audiencias de coincidencia de cliente a partir de [!DNL Adobe] audiencias](google-audience-from-adobe-audience.md)
>* [Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes](audience-from-customer-data-list.md)
>* [Administrar audiencias de remarketing dinámico](audience-dynamic-remarketing-manage.md)
