---
title: Convertir los identificadores de usuario de  [!DNL Tealium]  a identificadores universales
description: DSP Obtenga información sobre cómo habilitar la ingesta de segmentos de origen de  [!DNL Tealium]  por parte de los usuarios.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# Convertir los identificadores de usuario de [!DNL Tealium] a identificadores universales

*característica de Beta*

DSP Utilice la integración de la con la plataforma de datos del cliente [!DNL Tealium] para convertir las direcciones de correo electrónico con hash de origen de su organización en ID universales para la publicidad de destino. El proceso utiliza el conector de la manguera de seguridad [!DNL Amazon Web Services] (AWS). DSP Siga estos pasos para compartir datos de Tealium con el usuario de la aplicación de la manera más:

1. (Para convertir direcciones de correo electrónico en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure el seguimiento para habilitar [!DNL Analytics] la medición](#analytics-tracking).

1. DSP [Crear un origen de audiencia en la dirección de correo electrónico &#x200B;](#source-create).

1. [Preparar y compartir datos de asignación de segmentos](#map-data).

1. [Cree conectores en [!DNL Tealium] para compartir datos de segmentos](#tealium-connector).

1. [Duplique el conector existente en [!DNL Tealium] para seguir compartiendo segmentos](#duplicate-connector).

1. [Compare el número de identificadores universales con el número de direcciones de correo electrónico con hash](#compare-id-count).

## Paso 1: Configurar el seguimiento para la medición de [!DNL Analytics] {#analytics-tracking}

*Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para convertir direcciones de correo electrónico a [!DNL RampIDs] o [!DNL ID5] ID, debe hacer lo siguiente:

1. (Si aún no lo ha hecho) Complete todos los [requisitos previos para implementar [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y asegúrese de que el [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se estén rellenando en las direcciones URL de seguimiento.

1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

   * **Para [!DNL RampIDs]:** Debe implementar una etiqueta de JavaScript adicional en sus páginas web para que coincida con las conversiones de los identificadores en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones. Póngase en contacto con el equipo de cuenta de Adobe, que le dará instrucciones para registrarse para una etiqueta [!DNL LiveRamp] [!DNL LaunchPad] desde [!DNL LiveRamp] soluciones de tráfico de autenticación. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, el equipo de cuenta de Adobe generará y proporcionará una etiqueta única para que su organización la implemente en sus páginas web.

## DSP Paso 2: Creación de una fuente de audiencia en el {#source-create}

1. DSP [Cree una fuente de audiencia](source-manage.md) para importar audiencias a su cuenta de o a una cuenta de anunciante. Puede elegir convertir sus identificadores de usuario a cualquiera de los [formatos de ID universales disponibles](source-about.md).

   La configuración de origen incluirá una clave de origen generada automáticamente, que utilizará para preparar los datos de asignación de segmentos.

1. Después de crear el origen de audiencia, comparta la clave de código fuente con el usuario [!DNL Tealium].

## Paso 3: Preparar y compartir datos de asignación de segmentos {#map-data}

El anunciante debe preparar y compartir datos de asignación de segmentos.

1. El anunciante debe preparar los datos dentro de [!DNL Tealium]:

   1. Use el hash de los ID de correo electrónico para la audiencia del anunciante mediante el algoritmo SHA-256.

   1. Asigne la columna que contiene los ID de correo electrónico con hash al atributo del tipo de ID de visitante.

   1. Cree la audiencia con el atributo `Tealium_visitor_id`. Aplique el enriquecimiento adecuado para almacenar en déclencheur la audiencia. Consulte la [[!DNL Tealium] documentación sobre los atributos de ID de visitante](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. El anunciante debe proporcionar datos de asignación de segmentos al equipo de cuenta de Adobe DSP para crear los segmentos en la cuenta de. Utilice los siguientes nombres y valores de columna en un archivo de valores separados por comas:

   * **Clave de segmento externo:** La clave de segmento externa, que especificará más adelante en la configuración de acción del conector en [!DNL Tealium]. La convención de nombres recomendada es &quot;`<DSP source key>_<Tealium segment name>`&quot;, como &quot;57bf424dc10_coffee-drinkers&quot;. DSP DSP Para la clave de origen de la, utilice [!UICONTROL Source Key] de la configuración de origen de audiencia de la lista de distribución.

   * **Nombre del segmento:** El nombre del segmento.

   * **Descripción del segmento:** El propósito o la regla del segmento, o ambos.

   * **Id. principal:** Mantener en blanco

   * **CPM de vídeo:** 0

   * **Mostrar CPM:** 0

   * **Ventana del segmento:** El tiempo de vida del segmento.

## Paso 4: Crear conectores en [!DNL Tealium] para compartir datos de segmentos {#tealium-connector}

Para cada segmento que desee compartir, cree un conector independiente para cada acción que almacene en déclencheur los cambios de datos. Por ejemplo, para compartir dos segmentos con dos déclencheur cada uno, cree cuatro conectores.

1. El equipo de cuenta de Adobe proporciona al anunciante las credenciales del conector de la manguera de seguridad de AWS.

1. En [!DNL Tealium], [agregue un conector](https://docs.tealium.com/server-side/connectors/add/) con las siguientes opciones:

   1. Seleccione el conector [!DNL AWS Firehose].

   1. En la configuración de origen:

      1. Seleccione el segmento de audiencia que desea compartir.

      1. Configurar un déclencheur:

         * Para el primer conector del segmento, seleccione el déclencheur `Joined Audience`. DSP Esto garantiza que los datos se compartan con los usuarios cada vez que se unen a un segmento.

         * Para el segundo conector del segmento, seleccione el déclencheur `Left Audience`. DSP Este conector se utiliza para gestionar todas las exclusiones y los usuarios que dejan el segmento en el espacio de trabajo de los usuarios de la red de la red de la red de área de trabajo

   1. En los ajustes de configuración, especifique el conector de la manguera de AWS. DSP Si aún no ha añadido el conector del manguito de fuego para la, agregue un conector del manguito de fuego con la siguiente información:

      * **Nombre:** El nombre del conector.

      * **Clave de acceso:** Clave de acceso proporcionada por el equipo de cuenta de Adobe.

      * **Clave secreta:** Clave secreta proporcionada por el equipo de cuenta de Adobe.

      * **Región:** este de Virginia del Norte (us-east-1)

   1. En la configuración de la acción, haga lo siguiente:

      1. Cree una acción &quot;Enviar datos del cliente al flujo de entrega (avanzado)&quot; para agregar datos al segmento, utilizando la siguiente información:

         * **Nombre de acción:** El nombre de la acción.

         * **Tipo de acción:** Enviar datos del cliente al flujo de entrega (avanzado)

         * **Flujo de entrega:** Tealium_CDP_Connector

         * **Datos del mensaje:** Haga lo siguiente:

            1. Elija un atributo para el segmento:

               * Para el atributo Hash_Email, asigne un nombre al mensaje personalizado `hashed_email`.

               * Para el atributo Cookies, asigne un nombre al mensaje personalizado `cookies`.

            1. En la opción para crear un campo personalizado, en el campo [!DNL Source Key], escriba el [!UICONTROL External Segment Key] que se incluyó en los [datos de asignación de segmentos](#map-data) en el procedimiento anterior.

               DSP utilizará esta clave para rellenar el segmento.

            1. (Recomendado) Cree una acción de actualización para mantener el segmento fresco.

## Paso 5: Duplique el conector existente en [!DNL Tealium] para seguir compartiendo segmentos {#duplicate-connector}

Solo puede tener un conector por segmento y un segmento por conector.

1. En [!DNL Tealium], duplique el segmento para el que desea crear otro segmento y cambie el nombre del nuevo segmento.

1. En [!DNL Tealium], duplique [el conector que creó](#tealium-connector) en el procedimiento anterior y cambie el nombre del nuevo conector de &quot;`<original name>-copy`&quot; al nuevo nombre del segmento.

## Paso 6: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

DSP Los segmentos deben estar disponibles en un plazo de 24 horas para su uso en el mercado de la. DSP Una vez que reciba los datos del segmento, el recuento de audiencias debería ser visible en un plazo de nueve (9) horas.

Compruebe en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia de [!UICONTROL Audiences] > [!UICONTROL All Audiences] o en la configuración de ubicación) que el segmento se está rellenando y compare el número de ID universales con el número de direcciones de correo electrónico con hash originales. Para obtener información sobre las tasas de traducción de ID aceptables y por qué los recuentos de segmentos pueden variar, consulte &quot;[Variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances)&quot;.

Los segmentos se actualizan cada 24 horas. Sin embargo, la inclusión en un segmento caduca después de 30 días de forma predeterminada o después de un periodo de caducidad especificado por el cliente. Actualice sus segmentos reinsertándolos desde [!DNL Tealium] antes de la caducidad. Para solicitar una caducidad de segmento personalizada, póngase en contacto con el equipo de cuenta de Adobe.

## Resolución de problemas

Para solucionar problemas de tasa de traducción y recuento de usuarios, consulte &quot;[Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)&quot;.

Para solucionar problemas con el procedimiento de conversión, póngase en contacto con el equipo de la cuenta de Adobe o con `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Compatibilidad con la activación de identificadores universales](/help/dsp/audiences/universal-ids.md)
>* [Acerca de la administración de audiencias](/help/dsp/audiences/audience-about.md)
