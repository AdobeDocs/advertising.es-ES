---
title: Carga de datos de cuenta sin conexión para informes y simulaciones
description: Aprenda a cargar datos de cuentas sin conexión manualmente o en un bloque de  [!DNL Amazon] [!DNL S3] para la compatibilidad con informes y simulaciones. Los archivos de registro realizan un seguimiento del progreso de los trabajos de carga.
source-git-commit: 8ba0f8fa6050a3e6ec93bcf08df2c0204191fc02
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# Carga de datos de cuenta sin conexión para informes y simulaciones

*Anunciantes habilitados para las cargas de datos de cuenta*

Cargue contenido de campañas y datos de coste, clics y conversión sin conexión de una cuenta sin compatibilidad con API para simulaciones de informes y rendimiento.

Puede realizar un seguimiento del progreso de los trabajos de carga mediante la característica [!UICONTROL Upload Logs]:

* Vea una lista de cada archivo cargado para la cuenta. La información sobre cada trabajo de carga de archivos incluye el nombre de archivo, el canal de carga (*[!UICONTROL Cloud Storage]* o *[!UICONTROL Drag & Drop]*), la fecha y el estado de sincronización, y los motivos de las cargas incompletas.

* Descargue un archivo con las entidades de cuenta y las métricas relacionadas que se cargaron para cualquier trabajo. Los archivos están en formato de valores separados por comas (CSV).

## Carga manual de datos de cuenta

Puede rellenar una cuenta con contenido de campaña y datos de coste, clics y conversión cargando manualmente los datos en un archivo.

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Realice una de las acciones siguientes:

   * (Desde la vista [!UICONTROL Accounts]):

      1. Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Upload]** en la barra de herramientas de acciones masivas.

      1. Arrastre un archivo al cuadro o haga clic en **[!UICONTROL Browse Files]** y elija un archivo de su dispositivo o red.

      1. Haga clic en **[!UICONTROL Upload Files]**.

   * (Desde la configuración de la cuenta):

      1. Seleccione la cuenta de cualquiera de las siguientes maneras:

         * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

         * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

      1. Haga clic en la ficha **[!UICONTROL Upload File]**.

      1. Arrastre un archivo al cuadro o haga clic en **[!UICONTROL Browse Files]** y elija un archivo de su dispositivo o red.

      1. Haga clic en **[!UICONTROL Save]**.

## Cargar datos de cuenta en un bloque de [!DNL Amazon] [!DNL S3] {#data-upload-s3}

Puede rellenar una cuenta con datos de coste, clics y contenido de campañas cargándolos en una carpeta asignada a Search, Social y Commerce en un bloque de [!DNL Amazon Web Services] (AWS) [!DNL Simple Storage Service] ([!DNL S3]).

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Póngase en contacto con el equipo de su cuenta de Adobe para habilitar las cargas de datos de la cuenta para su cuenta de anunciante de Search, Social y Commerce. El equipo facilitará la creación de una carpeta específica de la organización en un bloque de [!DNL S3] y le informará cuando se haya completado.<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* Recupere la ruta de almacenamiento en la nube [!DNL S3], el identificador de clave de acceso y la clave de acceso secreta de su cuenta. Se usan el mismo identificador de clave de acceso y clave de acceso secreta en todas las cuentas de carga de datos de la organización <!-- naming convention?-->.

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Realice una de las acciones siguientes:

   * (Desde la vista [!UICONTROL Accounts]):

      1. Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Upload]** en la barra de herramientas de acciones masivas.

      1. En el cuadro [!UICONTROL Cloud Storage Link], haga clic en **[!UICONTROL Go to the Link]**.

      1. Haga clic en **[!UICONTROL Show Access Key and Secret]**.

      1. Junto al campo [!UICONTROL Storage Link], haga clic en **[!UICONTROL Copy]** para copiar el vínculo en el portapapeles y guardarlo en un lugar seguro.

      1. Del mismo modo, copie y almacene de forma segura los valores [!UICONTROL Access Key] y [!UICONTROL Secret Key].

      1. Haga clic en **[!UICONTROL Done]**.

   * (Desde la configuración de la cuenta):

      1. Seleccione la cuenta de cualquiera de las siguientes maneras:

         * Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Edit]**.

         * Seleccione la casilla de verificación situada junto al nombre de la cuenta y, a continuación, haga clic en **[!UICONTROL Edit]** en la barra de herramientas de acciones masivas.

      1. Haga clic en la ficha **[!UICONTROL Upload File]**.

      1. En el cuadro [!UICONTROL Cloud Storage Link], haga clic en **[!UICONTROL Go to the Link]**.

      1. Haga clic en **[!UICONTROL Show Access Key and Secret]**.

      1. Junto al campo [!UICONTROL Storage Link], haga clic en **[!UICONTROL Copy]** para copiar el vínculo en el portapapeles y guardarlo en un lugar seguro.

      1. Del mismo modo, copie y almacene de forma segura los valores [!UICONTROL Access Key] y [!UICONTROL Secret Key].

      1. Haga clic en **[!UICONTROL Done]**.

      1. Haga clic en **[!UICONTROL Save]**.

1. (Una vez por organización) Configure su entorno local de AWS:

   1. Descargue e instale [!DNL AWS Command Line Interface] (AWS CLI) desde la siguiente ubicación: [https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html).

   1. Configure las credenciales de AWS:

      1. Cree un archivo de texto sin formato y asígnele el nombre `~/.aws/credentials` (sin extensión de archivo).

      1. Abra el archivo en cualquier editor de texto e introduzca el ID de clave de acceso y la clave de acceso secreta de la organización de la siguiente manera:

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. Descargue el informe de datos de cuenta de la red de publicidad y guárdelo.

1. En AWS CLI, ejecute el siguiente comando para cargar los datos de su cuenta en la ubicación de nube [!DNL S3].

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   Ejemplo: `aws s3 cp filename.txt s3://cloud-location/`

## Ver un registro de los archivos de datos de cuenta cargados

1. En el menú principal, haga clic en **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Mantenga el cursor sobre el nombre de la cuenta, haga clic en **...** y, a continuación, haga clic en **[!UICONTROL Upload Logs]**.

1. (Opcional) Para descargar los datos de un archivo cargado, haga clic en ![Descargar](/help/search-social-commerce/assets/download.png "Descargar") en la columna [!UICONTROL Download] y descargue el archivo según el procedimiento normal del explorador.

## Datos necesarios

Los datos deben cumplir los requisitos de datos de la red publicitaria. Los campos de datos de cada entidad pueden variar según la red publicitaria.
