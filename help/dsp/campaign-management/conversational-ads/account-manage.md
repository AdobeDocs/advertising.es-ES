---
title: Administrar cuentas de anuncios conversacionales de [!DNL ChatGPT Ads]
description: Aprenda a crear y administrar cuentas para [!DNL ChatGPT Ads] anuncios de tarjetas de chat, una función beta que coloca anuncios dentro de las conversaciones del asistente de IA.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%
---
# Administrar cuentas de anuncios conversacionales de [!DNL ChatGPT Ads]

*característica de Beta*

A través de la integración de Adobe DSP con [!DNL OpenAI Ads], puede ejecutar [!DNL ChatGPT Ads] anuncios de tarjetas de chat, que aparecen dentro de [!DNL ChatGPT] conversaciones. Para esta función, DSP crea una cuenta de publicidad conversacional y compra contenido en nombre de la organización. No podrás acceder a la cuenta de publicidad desde ads.openai.com. Utilice esta característica para probar los medios de IA sin establecer una relación directa con [!DNL ChatGPT Ads].

Administrará sus cuentas de anuncios conversacionales de [!DNL ChatGPT Ads], incluidas sus campañas, grupos de anuncios y anuncios, por separado de sus campañas normales de DSP, que tienen una estructura diferente. También [verás datos de rendimiento de [!DNL ChatGPT Ads] campañas, grupos de anuncios y anuncios](campaign-manage.md#campaign-views-about) por separado de tus campañas de DSP.

## Idoneidad

Lo siguiente determina la idoneidad para esta función:

* **Clientes existentes de [!DNL Search, Social, & Commerce]:** Si tu anunciante ya usa [!DNL Search, Social, & Commerce], [crea y administra sus [!DNL ChatGPT Ads] campañas en Search, Social y Commerce](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md) en lugar de en DSP.

* **Industrias restringidas:** Los anunciantes de categorías restringidas (por ejemplo, finanzas o atención médica) no pueden crear campañas o cuentas de anuncios conversacionales.

Si el anunciante seleccionado no cumple los requisitos, las pestañas [!UICONTROL Accounts] y [!UICONTROL Campaigns] indican el motivo. Puede cambiar a otro anunciante con el selector de anunciante.

Para utilizar la función, póngase en contacto con el equipo de su cuenta de Adobe para iniciar el proceso de incorporación.

## Factura

Se le factura por el uso de [!DNL ChatGPT Ads] al final del mes con sus otras facturas, usando la divisa de facturación y la zona horaria de facturación de su cuenta de DSP (independientemente de la [divisa y la zona horaria utilizadas para la [!DNL ChatGPT Ads] cuenta](#account-settings)). Si tiene alguna pregunta sobre facturación, póngase en contacto con el equipo de su cuenta de Adobe.

## La vista [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] {#accounts-view}

La ficha [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] enumera las cuentas de [!DNL OpenAI] del anunciante seleccionado. La información de cada cuenta incluye:

**[!UICONTROL Status]:** Indica si la cuenta está mostrando actualmente anuncios: *Activo* o *En pausa*. No puede cambiar el estado de una cuenta; póngase en contacto con el equipo de cuenta de Adobe si desea pausar o reactivar una cuenta.

**[!UICONTROL Review status]:** El estado de revisión [!DNL OpenAI]: *En revisión*, *Aprobado* o *Desaprobado*. Mantenga el cursor sobre el estado por el motivo, si hay alguno disponible.

**[!UICONTROL Active campaigns]:** Número de campañas activas actualmente en la cuenta.

**[!UICONTROL Cost]:** Gasto total de la cuenta.

### Acciones disponibles

* [Ver límites de cuenta](#account-limits)

<!-- * [Refresh information about your accounts](#refresh) -- Add topic below. -->

* [Crear una cuenta](#account-create)

* [Editar una cuenta](#account-edit)

* [Actualizar la lista de cuentas](#account-refresh)

* [Vuelva al menú principal de DSP](#return-to-menu)

## Administrar cuentas

### Ver límites de cuenta {#account-limits}

Un límite de cuenta limita el gasto total de una cuenta en un intervalo de fechas específico. Puede ver los límites de una cuenta, pero solo su equipo de cuenta de Adobe puede crearlos, editarlos o eliminarlos.

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En la vista **[!UICONTROL Accounts]**, mantenga el cursor sobre la fila de la cuenta y haga clic en **[!UICONTROL ...]>[!UICONTROL View account limit]**.

La página [!UICONTROL Account limits] enumera cada límite de la cuenta:

**[!UICONTROL Name]:** El nombre del límite.

**[!UICONTROL Amount]:** Límite total de gasto para el período límite.

**[!UICONTROL Period]:** Intervalo de fecha al que se aplica el límite.

**[!UICONTROL Status]:** *Activo*, *Próximo* o *Completado*.

**[!UICONTROL Spent]:** Cantidad gastada hasta el momento dentro del período límite.

>[!NOTE]
>
>No puede editar ni eliminar los límites completados y los períodos de límite de la misma cuenta no se pueden superponer.

### Crear una cuenta de anuncio conversacional [!DNL ChatGPT Ads] {#account-create}

Para crear más de dos cuentas de [!DNL ChatGPT Ads] para un anunciante, comuníquese con el equipo de cuenta de Adobe.

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. Realice una de las siguientes acciones:

   * (Solo su primera cuenta) En la pantalla de bienvenida, haga clic en **[!UICONTROL Create an Account]**.

   * En la vista **[!UICONTROL Accounts]**, seleccione un anunciante y haga clic en **[!UICONTROL Create Account]**.

1. Especifique la [configuración de la cuenta](#account-settings).

1. Seleccione la casilla de verificación **[!UICONTROL I agree to the Terms and Conditions]**.

1. Haga clic en **[!UICONTROL Create account]**.

Las cuentas nuevas se crean en estado pausado mientras [!DNL OpenAI] las revisa. DSP activa la cuenta una vez que se aprueba.

### Editar una cuenta de publicidad conversacional de [!DNL ChatGPT Ads] {#account-edit}

Puede editar el nombre comercial legal y el sitio web de una cuenta una vez que la haya creado.

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En la vista **[!UICONTROL Accounts]**, mantenga el cursor sobre la fila de la cuenta y haga clic en **[!UICONTROL ...]>[!UICONTROL Edit account]**.

1. Editar **[!UICONTROL Legal Business Name]** y/o **[!UICONTROL Advertiser Website]**. Para obtener más información sobre los campos, consulte &quot;[Configuración de la cuenta](#account-settings)&quot;.

1. Haga clic en **[!UICONTROL Save changes]**.

>[!IMPORTANT]
>
>Guardar cambios reinicia la revisión de [!DNL OpenAI] de la cuenta. La cuenta no volverá a mostrar anuncios hasta que se vuelva a aprobar la cuenta.

### Actualizar la lista de cuentas {#account-refresh}

Volver a mostrar la lista de cuentas cuando otros usuarios hayan realizado cambios o adiciones.

1. En el menú principal, haga clic en **[!UICONTROL Conversational Ads Beta]**.

1. En la vista **[!UICONTROL Accounts]**, haga clic en **[!UICONTROL Refresh]** en la lista de cuentas.

### Vuelva al menú principal de DSP {#return-to-menu}

* Encima del menú principal, haga clic en **[!UICONTROL Back to DSP]**.

### [!DNL ChatGPT Ads] configuración de cuenta de publicidad conversacional {#account-settings}

**[!UICONTROL Legal Business Name]:** El nombre comercial registrado de la organización.

**[!UICONTROL Advertiser Website]:** Dirección URL del sitio web del anunciante, que comienza por `http://` o `https://`.

**[!UICONTROL Country]:** El país en el que la organización está registrada legalmente (no el país en el que publicará anuncios). Debe ser el mismo que el país utilizado para el contrato DSP de la organización. No puede cambiar este valor después de guardar la cuenta.

**[!UICONTROL Currency]:** (solo lectura) La divisa que el equipo de cuenta de Adobe configura para la cuenta de [!DNL ChatGPT Ads]. Puede ser diferente a la moneda de su cuenta de DSP, que se puede ver en cualquier otra parte de DSP. **Nota:** Independientemente de este valor, todas las facturas de uso estarán en la *divisa de facturación* usada para la cuenta de DSP.

**[!UICONTROL Timezone]:** (solo lectura) Zona horaria que el equipo de la cuenta de Adobe configura para la cuenta de [!DNL ChatGPT Ads]. Puede no coincidir con la zona horaria de la cuenta de DSP, que puede verse en cualquier otra parte de DSP. **Nota:** Independientemente de este valor, todas las facturas de uso representarán la *zona horaria de facturación* usada para la cuenta de DSP.

**[!UICONTROL Favicon]:** Un archivo de imagen para usar como favicon del sitio web para la cuenta.<!-- How is this used within this context? --> El explorador muestra el icono de favoritos en varios lugares, como la barra de direcciones, la pestaña o los marcadores. El archivo debe estar en formato JPG, PNG o WEBP y tener un mínimo de 256 x 256 píxeles.

Para cargar un icono, haga clic en **[!UICONTROL Upload favicon]** y, a continuación, busque y seleccione un archivo en su dispositivo o red.

**[!UICONTROL I agree to the Terms and Conditions]:** Una casilla de verificación para indicar que está de acuerdo con todos los términos legales. Active la casilla de verificación para crear una cuenta o actualizar la configuración de la cuenta.

>[!MORELIKETHIS]
>
>* [Administrar campañas de anuncios conversacionales](campaign-manage.md)
