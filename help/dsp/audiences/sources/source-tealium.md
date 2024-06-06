---
title: Conversión de ID de usuario [!DNL Tealium] a los ID universales
description: DSP Obtenga información sobre cómo habilitar la ingesta de datos en el sitio web de [!DNL Tealium] segmentos de origen.
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 729098f01fb9d076efb2b945be4011df9ab1c905
workflow-type: tm+mt
source-wordcount: '1109'
ht-degree: 0%

---

# Conversión de ID de usuario [!DNL Tealium] a los ID universales

*Función beta*

DSP Uso de la integración de la con [!DNL Tealium] plataforma de datos del cliente para convertir las direcciones de correo electrónico con hash de origen de su organización en ID universales para la publicidad de destino. El proceso utiliza el [!DNL Amazon Web Services] (AWS) conector de la manguera de incendios. DSP Siga estos pasos para compartir datos de Tealium con el usuario de la aplicación de la manera más:

1. (Para convertir direcciones de correo electrónico en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Configure el seguimiento para habilitar [!DNL Analytics] medida](#analytics-tracking).

1. [DSP Creación de una fuente de audiencia en la](#source-create).

1. [Preparación y uso compartido de datos de asignación de segmentos](#map-data).

1. [Creación de conectores en [!DNL Tealium] para compartir datos de segmentos](#tealium-connector).

1. [Duplique el conector existente en [!DNL Tealium] para seguir compartiendo segmentos](#duplicate-connector).

1. [Comparar el número de ID universales con el número de direcciones de correo electrónico con hash](#compare-id-count).

DSP Los segmentos deben estar disponibles en el plazo de 24 horas y se actualizan cada 24 horas.

## Paso 1: Configurar el seguimiento para [!DNL Analytics] medida {#analytics-tracking}

*Anunciantes con [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Para convertir direcciones de correo electrónico a [!DNL RampIDs] o [!DNL ID5] ID., debe hacer lo siguiente:

1. (Si aún no lo ha hecho) Completar todo [requisitos previos para la implementación [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) y asegúrese de que la variable [ID de AMO e ID de EF](/help/integrations/analytics/ids.md) se están rellenando en las direcciones URL de seguimiento.

1. Regístrese con el socio de ID universal e implemente un código universal específico en sus páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) a las visualizaciones de:

   * **Para [!DNL RampIDs]:** Debe implementar una etiqueta JavaScript adicional en las páginas web para que coincida con las conversiones de los ID en los navegadores web de escritorio y móviles (pero no en las aplicaciones móviles) para las visualizaciones. Póngase en contacto con el equipo de cuenta de Adobe, que le dará instrucciones para registrarse en [!DNL LiveRamp] [!DNL LaunchPad] etiqueta desde [!DNL LiveRamp] Soluciones de tráfico de autenticación. El registro es gratuito, pero debe firmar un acuerdo. Una vez que se registre, el equipo de cuenta de Adobe generará y proporcionará una etiqueta única para que su organización la implemente en sus páginas web.

## DSP Paso 2: Creación de una fuente de audiencia en el {#source-create}

1. [Crear una fuente de audiencia](source-manage.md) DSP para importar audiencias a su cuenta de o a una cuenta de anunciante de. Puede elegir convertir los identificadores de usuario a cualquiera de los siguientes [formatos de ID universales disponibles](source-about.md).

   La configuración de origen incluirá una clave de origen generada automáticamente, que utilizará para preparar los datos de asignación de segmentos.

1. Después de crear la fuente de audiencia, comparta la clave de código fuente con el [!DNL Tealium] usuario.

## Paso 3: Preparar y compartir datos de asignación de segmentos {#map-data}

1. El anunciante debe preparar y compartir datos de asignación de segmentos:

   1. El anunciante debe preparar los datos en [!DNL Tealium]:

      1. Use el hash de los ID de correo electrónico para la audiencia del anunciante mediante el algoritmo SHA-256.

      1. Asigne la columna que contiene los ID de correo electrónico con hash al atributo del tipo de ID de visitante.

      1. Cree la audiencia con `Tealium_visitor_id` atributo. Aplique el enriquecimiento adecuado para almacenar en déclencheur la audiencia. Consulte la [[!DNL Tealium] Documentación sobre los atributos de ID de visitante](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. El anunciante debe proporcionar datos de asignación de segmentos al equipo de cuenta de Adobe DSP para crear los segmentos en la cuenta de. Utilice los siguientes nombres y valores de columna en un archivo de valores separados por comas:

      * **Clave de segmento externo:** La clave del segmento externa, que especificará más adelante en la configuración de acción del conector en [!DNL Tealium]. La convención de nombres recomendada es &quot;`<DSP source key>_<Tealium segment name>`,&quot; como &quot;57bf424dc10_coffee-drinkers&quot;. DSP Para la clave de origen de la, utilice [!UICONTROL Source Key] DSP de la configuración de origen de audiencia de la.

      * **Nombre del segmento:** El nombre del segmento.

      * **Descripción del segmento:** El propósito o la regla del segmento, o ambos.

      * **Identificador principal:** Mantener en blanco

      * **CPM de vídeo:** 0

      * **Mostrar CPM:** 0

      * **Ventana de segmentos:** El tiempo de vida del segmento.

## Paso 4: Crear conectores en [!DNL Tealium] para compartir datos de segmentos {#tealium-connector}

Para cada segmento que desee compartir, cree un conector independiente para cada acción que almacene en déclencheur los cambios de datos. Por ejemplo, para compartir dos segmentos con dos déclencheur cada uno, cree cuatro conectores.

1. El equipo de cuenta de Adobe proporciona al anunciante las credenciales del conector de la manguera de seguridad de AWS.

1. Entrada [!DNL Tealium], [añadir un conector](https://docs.tealium.com/server-side/connectors/add/), utilizando las siguientes opciones:

   1. Seleccione el [!DNL AWS Firehose] conector.

   1. En la configuración de origen:

      1. Seleccione el segmento de audiencia que desea compartir.

      1. Configurar un déclencheur:

         * Para el primer conector del segmento, seleccione el déclencheur `Joined Audience`. DSP Esto garantiza que los datos se compartan con los usuarios cada vez que se unen a un segmento.

         * Para el segundo conector del segmento, seleccione el déclencheur `Left Audience`. DSP Este conector se utiliza para gestionar todas las exclusiones y los usuarios que dejan el segmento en el espacio de trabajo de los usuarios de la red de la red de la red de área de trabajo

   1. En los ajustes de configuración, especifique el conector de la manguera de AWS. DSP Si aún no ha añadido el conector del manguito de fuego para la, agregue un conector del manguito de fuego con la siguiente información:

      * **Nombre:** Nombre del conector.

      * **Clave de acceso:** La clave de acceso proporcionada por el equipo de cuenta de Adobe.

      * **Clave secreta:** La clave secreta proporcionada por el equipo de cuenta de Adobe.

      * **Región:** Virginia del Norte del Este de EE. UU. (us-east-1)

   1. En la configuración de la acción, haga lo siguiente:

      1. Cree una acción &quot;Enviar datos del cliente al flujo de entrega (avanzado)&quot; para agregar datos al segmento, utilizando la siguiente información:

         * **Nombre de la acción:** Nombre de la acción.

         * **Tipo de acción:** Envío de datos de clientes al flujo de entrega (avanzado)

         * **Flujo de envío:** Tealium_CDP_Connector

         * **Datos del mensaje:**  Haga lo siguiente:

            1. Elija un atributo para el segmento:

               * Para el atributo Hash_Email, asigne un nombre al mensaje personalizado `hashed_email`.

               * Para el atributo Cookies, asigne un nombre al mensaje personalizado `cookies`.

            1. En la opción para crear un campo personalizado, en la variable [!DNL Source Key] , introduzca la variable [!UICONTROL External Segment Key] que se incluyó en la [datos de asignación de segmentos](#map-data) en el procedimiento anterior.

               DSP utilizará esta clave para rellenar el segmento.

            1. (Recomendado) Cree una acción de actualización para mantener el segmento fresco.

## Paso 5: Duplicar el conector existente en [!DNL Tealium] para seguir compartiendo segmentos {#duplicate-connector}

Solo puede tener un conector por segmento y un segmento por conector.

1. Entrada [!DNL Tealium], duplique el segmento para el que desea crear otro segmento y cambie el nombre del nuevo segmento.

1. Entrada [!DNL Tealium], duplicado [el conector que ha creado](#tealium-connector) en el procedimiento anterior, y cambie el nombre del nuevo conector de &quot;`<original name>-copy`&quot; al nuevo nombre de segmento.

## Paso 6: Comparar el número de ID universales con el número de direcciones de correo electrónico con hash {#compare-id-count}

Una vez completados todos los pasos, consulte en la biblioteca de audiencias (que está disponible cuando crea o edita una audiencia desde ) [!UICONTROL Audiences] > [!UICONTROL All Audiences] o dentro de la configuración de ubicación) que el segmento se está rellenando en un plazo de 24 horas. Compare el número de ID universales con el número de direcciones de correo electrónico con hash originales.

La tasa de traducción de las direcciones de correo electrónico con hash a los ID universales debe ser superior al 90 %. Por ejemplo, si envía 100 direcciones de correo electrónico con hash desde la plataforma de datos del cliente, deben traducirse a más de 90 ID universales. Una tasa de traducción del 90 % o menos es un problema. Para obtener más información sobre cómo pueden variar los recuentos de segmentos, consulte[Causas de variaciones de datos entre ID de correo electrónico e ID universales](#universal-ids-data-variances).&quot;

Los segmentos se actualizan cada 24 horas. Sin embargo, la inclusión en un segmento caduca pasados 30 días para garantizar el cumplimiento de la privacidad, por lo que debe actualizar las audiencias reinsertándolas desde [!DNL Tealium] cada 30 días o menos.

Para obtener ayuda sobre la resolución de problemas, póngase en contacto con su equipo de cuenta de Adobe o `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de audiencia de origen](/help/dsp/audiences/sources/source-about.md)
>* [Administrar fuentes de audiencia para activar audiencias de ID universal](source-manage.md)
>* [Configuración de origen de audiencia](source-settings.md)
>* [Conversión de ID de usuario [!DNL Adobe Real-Time CDP] a los ID universales](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
