---
title: Carga de datos de conversión sin conexión para conversiones mejoradas
description: Aprenda a cargar datos de conversión sin conexión de origen para asignarlos a  [!DNL Google Ads] conversiones mejoradas para posibles clientes.
feature: Conversions
source-git-commit: c3cb1549adeb7b621c1b426c53da9bb09eddcbdc
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Carga de datos de conversión sin conexión para conversiones mejoradas

*[!DNL Google Ads]solo cuentas*

<!-- Tweak metadata title/description and heading -->

Puede cargar los datos de conversión sin conexión de origen, incluidas las direcciones de correo electrónico con hash y los números de teléfono, para asignarlos a las [[!DNL Google Ads] conversiones mejoradas de posibles clientes existentes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md). Todos los datos cargados se sincronizan en tiempo real con [!DNL Google Ads].

## Cargar datos para [!DNL Google Ads] conversiones mejoradas para posibles clientes

1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** y luego haga clic en la ficha **[!UICONTROL Upload]**.

1. Seleccione la red de publicidad y, a continuación, la cuenta.

1. (Opcional) Para descargar una plantilla con todos los [campos de datos necesarios](#enhanced-conversions-leads-data) en formato [!DNL Microsoft Excel], haga clic en **[!UICONTROL View Template]** y, a continuación, descargue el archivo según el procedimiento normal del explorador.

   Puede editar el archivo para incluir los datos, guardar los cambios y cargar el archivo en el siguiente paso.

1. Haga clic en **[!UICONTROL Choose File]** y, a continuación, seleccione un archivo para cargar desde el dispositivo o la red.

## Datos necesarios para los archivos cargados {#enhanced-conversions-leads-data}

### Datos encima de la tabla

`Parameters:TimeZone=insert_timezone`

Introduzca la zona horaria de la cuenta en esta ubicación o en la columna &quot;[!UICONTROL Conversion Time]&quot; para cada fila. Use a) el [formato de id. de zona horaria admitido](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b) el desplazamiento GMT, tal como indican + o - y la diferencia horaria de 4 dígitos (como -0500 en Nueva York).

### Columnas y valores de tabla

| Columna | Descripción |
| ------ | ----------- |
| Correo electrónico | La dirección de correo electrónico del usuario, que debe tener un cifrado hash con el algoritmo SHA-256. Cada fila debe incluir un valor de correo electrónico o un valor de número de teléfono. |
| Número de teléfono | Número de teléfono del usuario, que debe tener un cifrado hash con el algoritmo SHA-256. Debe incluir un código de país y puede contener guiones y otros símbolos. Cada fila debe incluir un valor de correo electrónico o un valor de número de teléfono. |
| Nombre de conversión | (Obligatorio) El nombre de la acción de conversión. |
| Tiempo de conversión | (Obligatorio) Hora a la que se produjo el evento de conversión en un [formato de hora admitido](https://support.google.com/google-ads/answer/7014069#prepare_data). Si no incluye el identificador de zona horaria de la cuenta en la línea `Parameters:TimeZone=insert_timezone` sobre la tabla de datos, incluya la zona horaria de cada fila usando a) el [formato de identificador de zona horaria admitido](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) o b) el desplazamiento GMT, tal como se indica con + o - y la diferencia horaria de 4 dígitos (como -0500 en Nueva York). |
| Valor de conversión | (Obligatorio) El valor de conversión numérico. |
| Divisa de conversión | El código de divisa del evento de conversión. |
| Añadir datos de usuario | (Aplicable a los datos pertenecientes a usuarios del Espacio Económico Europeo (EEE) o del Reino Unido (Reino Unido)) Indica si se dio el consentimiento del usuario para enviar datos de usuario a [!DNL Google] con fines de personalización de anuncios. Los valores pueden incluir `Granted`, `Denied` o \[null\] (que se envía a [!DNL Google Ads] como `Unspecified`). **Nota:** [!DNL Google Ads] actualmente no aplica el consentimiento para las conversiones mejoradas para los posibles clientes, pero es posible que lo haga en el futuro. |
| Ad Personalization | (Aplicable a los datos pertenecientes a usuarios del Espacio Económico Europeo (EEE) o del Reino Unido (Reino Unido)) Indica si se dio el consentimiento del usuario para enviar datos de usuario a [!DNL Google] con fines publicitarios. Los valores pueden incluir `Granted`, `Denied` o \[null\] (que se envía a [!DNL Google Ads] como `Unspecified`). **Nota:** [!DNL Google Ads] actualmente no aplica el consentimiento para las conversiones mejoradas para los posibles clientes, pero es posible que lo haga en el futuro. |

>[!MORELIKETHIS]
>
>* [Crear una acción de conversión para una  [!DNL Google Ads] conversión mejorada para posibles clientes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Implementar [!DNL Google Ads] conversiones mejoradas para posibles clientes](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Cargar métricas de conversión de búsqueda, medios sociales y seguimiento de Commerce a [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
