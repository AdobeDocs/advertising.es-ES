---
title: DSP "Flujo de trabajo para utilizar la integración de la con [!DNL Tealium]"
description: DSP "Aprenda a habilitar la ingesta de datos por parte de los [!DNL Tealium] segmentos de origen".
feature: DSP Audiences
source-git-commit: e7c967d66be9c8ca78a64d644c7e3a691f1e216a
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# DSP Flujo de trabajo para usar la integración de la con [!DNL Tealium]

Puede compartir los datos de origen de su organización desde el [!DNL Tealium] plataforma de datos del cliente con [!DNL Amazon Web Services] (AWS) conector de la manguera de incendios. DSP Hay cuatro pasos para compartir datos de Tealium con el usuario de la aplicación de la manera más:

1. [DSP Creación de una fuente de audiencia en la](#source-create).

1. [Preparación y uso compartido de datos de asignación de segmentos](#map-data).

1. [Creación de conectores en [!DNL Tealium] para compartir datos de segmentos](#tealium-connector).

1. [Duplique el conector existente en [!DNL Tealium] para seguir compartiendo segmentos](#duplicate-connector).

## DSP Paso 1: Creación de una fuente de audiencia en el {#source-create}

* [Crear una fuente de audiencia](source-create.md) DSP para importar audiencias a su cuenta de o de anunciante, y comparta la clave del código fuente con la cuenta de [!DNL Tealium] usuario.

## Paso 2: Preparar y compartir datos de asignación de segmentos {#map-data}

1. El anunciante debe preparar y compartir datos de asignación de segmentos:

   1. El anunciante debe preparar los datos en [!DNL Tealium]:

      1. Los ID de correo electrónico de la audiencia del anunciante deben tener un cifrado hash con el algoritmo SHA-256.

      1. La columna que contiene los ID de correo electrónico con hash debe asignarse al atributo del tipo de ID de visitante.

      1. La audiencia debe crearse con `Tealium_visitor_id` atributo. Se debe aplicar el enriquecimiento adecuado para almacenar en déclencheur la audiencia. Consulte la [[!DNL Tealium] Documentación sobre los atributos de ID de visitante](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. El anunciante debe proporcionar datos de asignación de segmentos al equipo de cuenta de Adobe DSP para crear los segmentos en la cuenta de. Utilice los siguientes nombres y valores de columna en un archivo de valores separados por comas:

      * **Clave de segmento externo:** La clave del segmento externa, que especificará más adelante en la configuración de acción del conector en [!DNL Tealium]. La convención de nombres recomendada es &quot;`<DSP source key>_<Tealium segment name>`,&quot; como &quot;57bf424dc10_coffee-drinkers&quot;.

      * **Nombre del segmento:** El nombre del segmento.

      * **Descripción del segmento:** El propósito o la regla del segmento, o ambos.

      * **Identificador principal:** Mantener en blanco

      * **CPM de vídeo:** 0

      * **Mostrar CPM:** 0

      * **Ventana de segmentos:** El tiempo de vida del segmento.

## Paso 3: Crear conectores en [!DNL Tealium] para compartir datos de segmentos {#tealium-connector}

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

            1. En la opción para crear un campo personalizado, en la variable [!DNL Source Key] , introduzca la variable [!UICONTROL External Segment Key] que se incluyó en los datos de asignación de segmentos en [Paso 2](#map-data).

               DSP utilizará esta clave para rellenar el segmento.

            1. (Recomendado) Cree una acción de actualización para mantener el segmento fresco.

## Paso 4: Duplicar el conector existente en [!DNL Tealium] para seguir compartiendo segmentos {#duplicate-connector}

Solo puede tener un conector por segmento y un segmento por conector.

1. Entrada [!DNL Tealium], duplique el segmento para el que desea crear otro segmento y cambie el nombre del nuevo segmento.

1. Entrada [!DNL Tealium], duplique el conector creado en [Paso 3](#tealium-connector)y cambie el nombre del nuevo conector desde &quot;`<original name>-copy`&quot; al nuevo nombre de segmento.

>[!MORELIKETHIS]
>
>* [Acerca de la activación de segmentos autenticados a partir de fuentes de audiencia](/help/dsp/audiences/sources/source-about.md)
>* [Crear una fuente de audiencia para activar audiencias de origen](source-create.md)
>* [Configuración de origen de audiencia](source-settings.md)
>* [DSP Flujo de trabajo para usar la integración de la con [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Acerca de Audience Management](/help/dsp/audiences/audience-about.md)
