---
title: Crear un [!DNL Google Ads] audiencia de customer match de una lista de correo electrónico de Adobe Campaign
description: Obtenga información sobre cómo crear un [!DNL Google Ads] audiencia de customer match de una lista de correo electrónico de Adobe Campaign existente.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Crear un [!DNL Google Ads] audiencia de customer match de una lista de correo electrónico de Adobe Campaign

*[!DNL Google Ads]cuentas elegibles solo para la confrontación con clientes*

Puede crear un [!DNL Google Ads] audiencia afín de clientes de una lista de correo electrónico en Adobe Campaign configurando un vínculo de cuenta y un flujo de trabajo en [!DNL Campaign].

Para ello, debe acceder a su [!DNL Campaign] y un archivo XML que contiene el flujo de trabajo necesario, que le proporcionará su equipo de cuenta de Adobe. Las instrucciones pueden variar para diferentes versiones de [!DNL Campaign]. Si es necesario, su equipo de cuenta de Adobe puede ayudarle a configurar el flujo de trabajo en [!DNL Campaign].

1. Obtenga credenciales para una cuenta SFTP proporcionada por Advertising Search, Social y Commerce.

1. Entrada [!DNL Campaign], configure el envío de la lista de correo electrónico a Advertising Search, Social y Commerce:

   1. Crear un [cuenta externa](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) para vincular su cuenta SFTP proporcionada por Search, Social y Commerce:

      1. En el menú de la izquierda, vaya a **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Clic ![Crear cuenta](/help/search-social-commerce/assets/campaign-create-account.png "Crear cuenta").

      1. Introduzca una etiqueta para la cuenta y seleccione **[!UICONTROL SFTP]** como el tipo de cuenta.

      1. Introduzca la dirección URL y el número de puerto del [!DNL Adobe] Servidor SFTP y nombre de carpeta, nombre de usuario y contraseña del anunciante.

      1. Haga clic **[!UICONTROL Save]**.
   1. Entrada [!DNL Campaign Client], instale el paquete de datos que incluye el flujo de trabajo necesario para enviar datos de correo electrónico:

      1. En la barra de menús, vaya a **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Seleccionar **[!UICONTROL Install a package from a file]** y haga clic en **[!UICONTROL Next]**.

      1. Busque el archivo del paquete de datos (`AMO_Workflow.xml`) en el dispositivo o red y, a continuación, haga clic en **[!UICONTROL Next]**.

      1. Clic **[!UICONTROL Start]** y espere a que se instale el flujo de trabajo.
   1. Edite el flujo de trabajo instalado para, opcionalmente, editar los filtros de la consulta de datos e identificar el nuevo nombre de audiencia y la cuenta SFTP externa:

      1. Ir a **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** y abra el paquete.

      1. (Opcional) Edite cualquiera de los filtros de los datos:

         * En el flujo de trabajo, haga doble clic en la actividad de consulta (como ForkTransition 1).

         * Edite las expresiones de filtro.

         * Haga clic **[!UICONTROL Finish]**.
      1. Asigne un nombre al segmento:

         * En el flujo de trabajo, haga doble clic en la actividad **[!UICONTROL Data extraction (File)]**.

         * En el **[!UICONTROL Data extraction (File)]** , en la pestaña **[!UICONTROL File name]** , introduzca el nombre del segmento con la extensión &quot;`.added`&quot; (como PaidSubscribers.added).

            El nombre del segmento no debe existir ya. El nombre del segmento distingue entre mayúsculas y minúsculas y debe constar de caracteres ASCII, pero no puede incluir guiones bajos (`_`).

            Sin embargo, si desea agregar el segmento a un segmento específico [!DNL Google Ad] cuenta, y añada el nombre del segmento con un guion bajo y la etiqueta [!UICONTROL User SE Account ID] (ID de Search, Social y Commerce para [!DNL Google Ads] cuenta, no el identificador de cuenta de red):

            `_<User SE Account ID>`

            Ejemplo: Paid_Subscribers_1234.added

            >[!NOTE]
            >
            >Esta es una excepción a la regla que prohíbe los guiones bajos en el nombre del archivo.

            De lo contrario, el segmento se agregará a todo [!DNL Google Ads] cuentas que Search, Social y Commerce están sincronizando para el anunciante.

         * Deje la opción en **[!UICONTROL Generate an outbound transition]** seleccionados.

         * Haga clic **[!UICONTROL Ok]**.
      1. Especifique la cuenta externa a la que desea enviar los datos:

         * En el flujo de trabajo, haga doble clic en la actividad **[!UICONTROL File Transfer]**.

         * En el **[!UICONTROL File Transfer]** , en la pestaña **[!UICONTROL Remote server]** , seleccione la opción para **[!UICONTROL Use an external account]**.

         * En el **[!UICONTROL External account]** , seleccione la etiqueta para la cuenta externa creada en el paso 2.

         * En el **[!UICONTROL Server folder]** , seleccione el valor del campo [!UICONTROL Account] para la cuenta externa.

         * (Opcional) En el **[!UICONTROL Schedule]** pestaña, especifique una programación diferente para la transferencia de archivos.

            De forma predeterminada, el flujo de trabajo se ejecuta a las 00:00 (medianoche), lo que garantiza que se procesen todos los registros. Para minimizar la latencia, programe el flujo de trabajo para que se ejecute antes de las 18:00.

         * Haga clic **[!UICONTROL Ok]**.





Search, Social y Commerce comprueba el directorio cada 30 minutos (en NN:30 y NN:59 en el huso horario del anunciante), mueve los archivos que encuentra a otra ubicación y, a continuación, crea automáticamente una audiencia a partir de los datos y la envía a Google a las 22:00 (10 p. m.). Search, Social y Commerce siguen buscando actualizaciones (adiciones y restas) en la lista de correo electrónico cada 30 minutos y actualizan la audiencia en [!DNL Google Ads] en consecuencia a las 22:00 diariamente.

>[!NOTE]
>
>* Si carga más de una versión de un archivo entre ciclos de procesamiento, se utiliza el archivo más reciente.
>
>* Search, Social y Commerce no almacenan ninguno de los datos de clientes de las listas de correo electrónico utilizadas para crear o editar una [!DNL Google Ads] audiencia.
>
>* [!DNL Google Ads] puede tardar un tiempo en procesar las actualizaciones para una audiencia.
>
>* Consulte [[!DNL Google Ads] documentación sobre cómo funciona la coincidencia de clientes y limitaciones](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [Acerca de las audiencias](audience-about.md)
>* [Crear [!DNL Google Ads] audiencias de coincidencia de cliente de [!DNL Adobe] audiencias](google-audience-from-adobe-audience.md)
>* [Administrar audiencias de coincidencia de clientes mediante listas de datos de clientes](audience-from-customer-data-list.md)
>* [Administración de audiencias de remarketing dinámico](audience-dynamic-remarketing-manage.md)

