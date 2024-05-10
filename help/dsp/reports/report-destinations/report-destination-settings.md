---
title: Configuración de destino del informe
description: Consulte los detalles necesarios para los destinos de informe, por tipo de destino.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Configuración de destino del informe

Los detalles necesarios para los destinos de informe que no son de correo electrónico varían según el tipo de destino.

>[!NOTE]
>
> También puede enviar los informes personalizados a los destinatarios de correo electrónico, que no requieren un destino de informe guardado. Puede especificar destinatarios de correo electrónico, en lugar de destinos guardados, dentro de la configuración del informe.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Un nombre para ayudarle a identificar el destino.

**[!UICONTROL S3 Bucket URL]:** La ruta completa a la carpeta en el [!DNL Amazon Simple Storage Service] (S3) bloque en el que se carga el informe. Ejemplo: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** La ID de la clave de acceso a ([!DNL Amazon S3]) cubo (proporcionado por [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** La clave de acceso secreta de ([!DNL Amazon S3]) cubo (proporcionado por [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Un nombre para ayudarle a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** Número de puerto que se va a utilizar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** Contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** Ruta del servidor en el que se cargan los archivos.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Un nombre para ayudarle a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** Número de puerto que se va a utilizar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** Contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** Ruta del servidor en el que se cargan los archivos.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Un nombre para ayudarle a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** Número de puerto que se va a utilizar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** Contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** Ruta del servidor en el que se cargan los archivos.

>[!MORELIKETHIS]
>
>* [Acerca de [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Crear un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Editar una [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Eliminar un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
