---
title: (Nueva IU) Cargar datos de conversión sin conexión para lograr conversiones mejoradas
description: Aprenda a cargar datos de conversión sin conexión de origen para asignarlos a  [!DNL Google Ads] conversiones mejoradas para posibles clientes y [!DNL Microsoft Advertising] conversiones mejoradas.
feature: Conversions
feature_v2: id: e6916c1b-e939-4e0b-99f5-768e83e1e99fid: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 903
ht-degree: 0%

---

# Carga de datos de conversión sin conexión para conversiones mejoradas

*[!DNL Google Ads]y [!DNL Microsoft Advertising] solo cuentas*

Puede cargar los datos de conversión sin conexión de origen, incluidas las direcciones de correo electrónico con hash y los números de teléfono, para asignarlos a las [[!DNL Google Ads] conversiones mejoradas para posibles clientes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) y [[!DNL Microsoft Advertising] conversiones mejoradas](https://help.ads.microsoft.com/#apex/ads/en/60178) existentes. Todos los datos cargados se sincronizan en tiempo real con la red de anuncios.

## (Nueva IU) Cargar datos para mejorar las conversiones

*característica de Beta*

1. En el menú principal, haga clic en **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Sobre la tabla de datos, haga clic en **[!UICONTROL Set up Conversion]**.

1. Especifique la configuración de carga de datos:

   1. En la ficha [!UICONTROL Basic Details]:

      1. Seleccione [!UICONTROL Setup Method] *[!UICONTROL Data Upload]*.

      1. Seleccione [!UICONTROL Platform]: *[!UICONTROL Google]* o *[!UICONTROL Microsoft]*.

      1. Haga clic en **[!UICONTROL Next]**.

   1. En la ficha [!UICONTROL Configure]:

      1. (Opcional) Para descargar una plantilla con todos los [campos de datos necesarios](#enhanced-conversions-leads-data) en formato [!DNL Microsoft Excel], haga clic en **[!UICONTROL Download Template]** y, a continuación, descargue el archivo según el procedimiento normal del explorador.

         Puede editar el archivo para incluir los datos, guardar los cambios y, a continuación, cargar el archivo en la cuenta de red de publicidad especificada.

      1. Seleccione la cuenta de red de publicidad a la que se cargarán los datos.

      1. En el cuadro [!UICONTROL Upload Conversion File], realice una de las acciones siguientes:

         * Arrastre un archivo al cuadro.

         * Haga clic en **[!UICONTROL Browse File]** y, a continuación, seleccione un archivo para cargar desde el dispositivo o la red.

   1. Haga clic en **[!UICONTROL Review and Save]** para revisar la configuración.

   1. Haga clic en **[!UICONTROL Upload]**.

## (IU heredada) Cargar datos para mejorar las conversiones

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]** y luego haga clic en la ficha **[!UICONTROL Upload]**.

1. Seleccione la red de publicidad y, a continuación, la cuenta.

1. (Opcional) Para descargar una plantilla con todos los [campos de datos necesarios](#enhanced-conversions-leads-data) en formato [!DNL Microsoft Excel], haga clic en **[!UICONTROL View Template]** y, a continuación, descargue el archivo según el procedimiento normal del explorador.

   Puede editar el archivo para incluir los datos, guardar los cambios y cargar el archivo en el siguiente paso.

1. Haga clic en **[!UICONTROL Choose File]** y, a continuación, seleccione un archivo para cargar desde el dispositivo o la red.

## Datos necesarios para los archivos cargados {#enhanced-conversions-leads-data}

### Datos encima de la tabla

`Parameters:TimeZone=insert_timezone`

Escriba la zona horaria de la cuenta en esta ubicación o en la columna &quot;[!UICONTROL Conversion Time]&quot; de cada fila. Use a\) ([!DNL [!DNL Google Ads] solamente]) el [formato de id. de zona horaria admitido](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b\) el desplazamiento GMT, tal como indican + o - y la diferencia horaria de 4 dígitos (como -0500 para Nueva York, +0100 para Berlín o +0000 para la hora del meridiano de Greenwich).

### Columnas y valores de tabla para [!DNL Google Ads]

| Columna | Descripción |
| ------ | ----------- |
| [!UICONTROL Email] | La dirección de correo electrónico del usuario, que debe tener un cifrado hash con el algoritmo SHA-256. Cada fila debe incluir un valor [!UICONTROL Email] o un valor [!UICONTROL Phone Number]. |
| [!UICONTROL Phone Number] | Número de teléfono del usuario, que debe tener un cifrado hash con el algoritmo SHA-256. Debe incluir un código de país y puede contener guiones y otros símbolos. Cada fila debe incluir un valor [!UICONTROL Email] o un valor [!UICONTROL Phone Number]. |
| [!UICONTROL Conversion Name] | (Obligatorio) El nombre de la acción de conversión. |
| [!UICONTROL Conversion Time] | (Obligatorio) Hora a la que se produjo el evento de conversión en un [formato de hora admitido](https://support.google.com/google-ads/answer/7014069#prepare_data). Si no incluye el identificador de zona horaria de la cuenta en la línea `Parameters:TimeZone=insert_timezone` situada encima de la tabla de datos, incluya la zona horaria de cada fila con a\) el [formato de identificador de zona horaria admitido](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b\) el desplazamiento GMT, indicado por + o - y la diferencia horaria de 4 dígitos (como -0500 para Nueva York, +0100 para Berlín o +0000 para la hora del meridiano de Greenwich). |
| [!UICONTROL Conversion Value] | (Obligatorio) El valor de conversión numérico. |
| [!UICONTROL Conversion Currency] | El código de divisa del evento de conversión. |
| [!UICONTROL Ad User Data] | (Aplicable a los datos pertenecientes a usuarios del Espacio Económico Europeo (EEE) o del Reino Unido (Reino Unido)) Indica si se dio el consentimiento del usuario para enviar datos de usuario a [!DNL Google] con fines de personalización de anuncios. Los valores pueden incluir `Granted`, `Denied` o \[null\] (que se envía a [!DNL Google Ads] como `Unspecified`). **Nota:** [!DNL Google Ads] actualmente no aplica el consentimiento para las conversiones mejoradas para los posibles clientes, pero es posible que lo haga en el futuro. |
| [!UICONTROL Ad Personalization] | (Aplicable a los datos pertenecientes a usuarios del Espacio Económico Europeo (EEE) o del Reino Unido (Reino Unido)) Indica si se dio el consentimiento del usuario para enviar datos de usuario a [!DNL Google] con fines publicitarios. Los valores pueden incluir `Granted`, `Denied` o \[null\] (que se envía a [!DNL Google Ads] como `Unspecified`). **Nota:** [!DNL Google Ads] actualmente no aplica el consentimiento para las conversiones mejoradas para los posibles clientes, pero es posible que lo haga en el futuro. |

### Columnas y valores de tabla para [!DNL Microsoft Advertising]

Para obtener más instrucciones para aplicar formato y aplicar hash a los datos, consulte la documentación de [!DNL Microsoft Ads] sobre [conversiones mejoradas](https://help.ads.microsoft.com/#apex/ads/60178).

| Columna | Descripción |
| ------ | ----------- |
| [!UICONTROL Email] | La dirección de correo electrónico del usuario, que debe tener un cifrado hash con el algoritmo SHA-256. Cada fila debe incluir un valor [!UICONTROL Email] o un valor [!UICONTROL Phone Number]. |
| [!UICONTROL Phone Number] | Número de teléfono del usuario, que debe tener un cifrado hash con el algoritmo SHA-256. Debe incluir un código de país y puede contener guiones y otros símbolos. Para mejorar las conversiones sin conexión, cada fila debe incluir un valor [!UICONTROL Email] o un valor [!UICONTROL Phone Number]. |
| [!UICONTROL Conversion Name] | (Obligatorio) El nombre de la acción de conversión. |
| [!UICONTROL Conversion Time] | (Obligatorio) La hora a la que se produjo el evento de conversión. Si no incluye el identificador de zona horaria de la cuenta en la línea `Parameters:TimeZone=insert_timezone` situada encima de la tabla de datos, incluya la zona horaria de cada fila con el desplazamiento GMT, tal y como indican + o - y la diferencia horaria de 4 dígitos (por ejemplo, -0500 en Nueva York, +0100 en Berlín o +0000 en la hora del meridiano de Greenwich). Para obtener una lista de zonas horarias de varias ciudades, consulte [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), pero asegúrese de usar el formato especificado aquí en lugar del formato de la lista de zonas horarias. |
| [!UICONTROL Conversion Value] | (Obligatorio) El valor de conversión numérico. |
| [!UICONTROL Conversion Currency] | El código de divisa del evento de conversión. |

>[!MORELIKETHIS]
>
>* [Implementar [!DNL Google Ads] conversiones mejoradas para posibles clientes](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implementar [!DNL Microsoft Advertising] conversiones sin conexión mejoradas](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [Crear una acción de conversión para una  [!DNL Google Ads] conversión mejorada para posibles clientes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Cargar métricas de conversión de búsqueda, medios sociales y seguimiento de Commerce a [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
