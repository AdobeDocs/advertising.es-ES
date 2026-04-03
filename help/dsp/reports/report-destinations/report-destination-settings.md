---
title: Configuración de destino del informe
description: Consulte los detalles necesarios para los destinos de informe, por tipo de destino.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
TQID: https://experienceleague.adobe.com/VB5UY9vm147LQJMKKyGOlhZdNcq6mVDYTT0Ef4RcwVs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: cc3b7f3c-58f0-4ba4-b808-391002930fd4id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 0%

---

# Configuración de destino del informe

Los detalles necesarios para los destinos de informe que no son de correo electrónico varían según el tipo de destino.

>[!NOTE]
>
> También puede enviar los informes personalizados a los destinatarios de correo electrónico, que no requieren un destino de informe guardado. Puede especificar destinatarios de correo electrónico, en lugar de destinos guardados, dentro de la configuración del informe.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Un nombre que le ayudará a identificar el destino.

**[!UICONTROL S3 Bucket URL]:** Ruta de acceso completa a la carpeta en el bloque [!DNL Amazon Simple Storage Service] (S3) en el que se ha cargado el informe. Ejemplo: `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** Identificador de clave de acceso al bloque ([!DNL Amazon S3]) (proporcionado por [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** La clave de acceso secreta del contenedor ([!DNL Amazon S3]) (proporcionada por [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Un nombre que le ayudará a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** El número de puerto que se va a usar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** Contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** Ruta de acceso del servidor en el que se cargan los archivos.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Un nombre que le ayudará a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** El número de puerto que se va a usar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** Contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** Ruta de acceso del servidor en el que se cargan los archivos.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Un nombre que le ayudará a identificar el destino.

**[!UICONTROL Server]:** El nombre de host del servidor.

**[!UICONTROL Port]:** El número de puerto que se va a usar en el servidor. El valor predeterminado es *[!UICONTROL 21]*.

**[!UICONTROL Username]:** El nombre de usuario para iniciar sesión en el servidor.

**[!UICONTROL Password]:** Contraseña para iniciar sesión en el servidor.

**[!UICONTROL Path (Optional)]:** Ruta de acceso del servidor en el que se cargan los archivos.

>[!MORELIKETHIS]
>
>* [Acerca de los destinos del informe](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Crear un destino de informe](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Editar un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Eliminar un destino de informe](/help/dsp/reports/report-destinations/report-destination-delete.md)
