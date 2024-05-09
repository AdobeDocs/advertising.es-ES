---
title: 'Compatibilidad del Adobe Advertising con la Ley de Privacidad del Consumidor de California : Compatibilidad con la exclusión de la venta del consumidor'
description: Obtenga información acerca de la compatibilidad para capturar solicitudes de exclusión de venta de consumidores.
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%

---

# Compatibilidad de Adobe Advertising con la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión de la venta del consumidor

*Para el Demand Side Platform DSP de Adobe Advertising ()*

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor legal para obtener asesoramiento sobre la Ley de Privacidad del Consumidor de California.

La Ley de Privacidad del Consumidor de California (CCPA) es la nueva ley de privacidad de California que entró en vigor el 1 de enero de 2020. La CCPA otorga a los residentes de California nuevos derechos con respecto a su información personal e impone responsabilidades de protección de datos a ciertas entidades que hacen negocios en California. La CCPA otorga a los consumidores el derecho de acceder a sus datos y eliminarlos, así como el derecho de exclusión de determinadas actividades que pueden considerarse &quot;vendedoras&quot; de información personal a terceros.

Como empresa, determinará los datos personales que Adobe Experience Cloud procesa y almacena en su nombre.

Como proveedor de servicio, Adobe Advertising proporciona asistencia a su empresa para que cumpla con las obligaciones que le impone CCPA y que son aplicables al uso de los productos y servicios de Adobe Advertising, incluida la administración de las solicitudes de los consumidores de acceso y eliminación de información personal y la administración de las solicitudes de los consumidores de exclusión de la venta de información personal.

En este documento se describe cómo Adobe Advertising Demand Side Platform DSP (), como proveedor de servicios, respalda el derecho del consumidor a excluirse de la &quot;venta&quot; de &quot;información personal&quot;, ya que cada término se define en la CCPA. Incluye información sobre cómo comunicar las solicitudes de exclusión de venta al Adobe Advertising y cómo recuperar informes de las solicitudes de exclusión de venta de su organización.

Para obtener información acerca de cómo [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; y [!DNL Advertising DCO] para respaldar los derechos de acceso y eliminación de información personal de los consumidores, consulte [Compatibilidad del Adobe Advertising con la Ley de Privacidad del Consumidor de California: Compatibilidad de acceso y eliminación de datos del consumidor](/help/privacy/ccpa/ccpa-access-delete.md).

Para obtener más información sobre los servicios de privacidad de Adobe de la CCPA, consulte la [Centro de privacidad de Adobe](https://www.adobe.com/privacy/ccpa.html).

## Comunicación de solicitudes de exclusión de la venta de consumidores al Adobe Advertising

Puede comunicar las solicitudes de exclusión de venta de los consumidores mediante lo siguiente:

* DSP un segmento de exclusión de CCPA creado en Advertising
* la API de Adobe Experience Platform Privacy Service

### Método 1: Comunicar las solicitudes de exclusión de la venta de la CCPA mediante una [!UICONTROL CCPA Opt-Out-of-Sale] DSP Segmento en Advertising

>[!NOTE]
>
>Los usuarios permanecen indefinidamente en los segmentos de exclusión de la venta de la CCPA.

1. DSP Inicie sesión en la cuenta del anunciante en Advertising en [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Cree un segmento de exclusión de CCPA e implemente el píxel del segmento para capturar las solicitudes de exclusión](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Método 2: Comunicar las solicitudes de exclusión de la venta de la CCPA mediante la API de Adobe Experience Platform Privacy Service

*Anunciantes asignados solo a un ID de organización de Adobe Experience Cloud*

1. Implemente una biblioteca JavaScript para recuperar las cookies del cliente. La misma biblioteca, `AdobePrivacy.js`, se utiliza para todas las soluciones de Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Las solicitudes a algunas soluciones de Adobe Experience Cloud no requieren la biblioteca JavaScript, pero las solicitudes a la Adobe Advertising sí la requieren.

   Debe implementar la biblioteca en la página web desde la que los clientes pueden enviar solicitudes de exclusión de venta, como el portal de privacidad de la compañía. La biblioteca de ayuda a recuperar las cookies de Adobe (ID de área de nombres: `gsurferID`) para que pueda enviar estas identidades como parte de solicitudes de exclusión de venta a través de la API de Adobe Experience Platform Privacy Service.

1. Identifique su ID de organización de Experience Cloud y asegúrese de que esté vinculado a sus cuentas de Adobe Advertising.

   Un ID de organización de Experience Cloud es una cadena alfanumérica de 24 caracteres anexada a &quot;@AdobeOrg&quot;. A la mayoría de los clientes de Experience Cloud se les ha asignado un ID de organización. Si el equipo de marketing o el administrador interno del sistema de Adobe no conocen el ID de la organización o no están seguros de si se ha proporcionado, póngase en contacto con el equipo de cuenta de Adobe. Necesitará el ID de organización para enviar solicitudes a la API de privacidad mediante `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Póngase en contacto con el representante de Adobe Advertising de su compañía para confirmar que todas las cuentas de Adobe Advertising de su organización, incluidas [!DNL DSP] cuentas o anunciantes, [!DNL Search, Social, & Commerce] cuentas, y [!DNL Creative] o [!DNL DCO] cuentas: están vinculadas a su ID de organización de Experience Cloud.

1. Utilice la API de Adobe Experience Platform Privacy Service para lo siguiente [enviar solicitudes de exclusión de venta](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) para dar su Adobe Advertising en nombre de los consumidores y para comprobar el estado de las solicitudes existentes.

   Consulte el apéndice siguiente para ver un ejemplo de solicitud de exclusión de la venta.

   >[!NOTE]
   >
   >Si su empresa tiene varios ID de organización de Experience Cloud, debe enviar solicitudes de API independientes para cada uno. Sin embargo, puede realizar una solicitud de API a varias subsoluciones de Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], y [!DNL DCO]), con una cuenta por subsolución.

Todos estos pasos son necesarios para recibir asistencia del Adobe Advertising. Para obtener más información sobre estas y otras tareas relacionadas que debe realizar con Adobe Experience Platform Privacy Service y dónde encontrar los elementos necesarios, consulte [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Recuperación de informes de consumidores que han enviado solicitudes de exclusión de venta

El Adobe Advertising de genera informes mensuales de los ID que los clientes han enviado para solicitudes de exclusión de venta de la cuenta. Cada informe está disponible como archivo de texto separado por tabulaciones comprimido en formato GZIP. DSP Los datos consolidan las solicitudes capturadas mediante segmentos de exclusión de la venta de la CCPA que se crearon en Advertising y cualquier envío realizado mediante la API de Privacy Service. Los ID de usuario capturados en los segmentos de exclusión de la venta de la CCPA se identifican por segmento y por anunciante. Los informes se generan el primer día de cada mes del mes anterior. Por ejemplo, la lista de usuarios mensual de para junio está disponible el 1 de julio.

DSP DSP Puede recuperar vínculos a los informes mensuales creados en los tres meses anteriores, ya sea desde Advertising o mediante Advertising [!DNL Trafficking API]. Cada vínculo es válido durante siete días, pero se actualiza cada vez que un cliente intenta recuperar uno.

### DSP Método 1: Recuperación de informes de exclusión de la venta de consumidores dentro de Advertising

1. DSP Inicie sesión en la cuenta del anunciante en Advertising en [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Recuperación de los informes](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### DSP Método 2: Recuperación de informes de exclusión de la venta de consumidores mediante el servicio de publicidad de la aplicación de la publicidad de la aplicación de la [!DNL Trafficking API]

Esta función está disponible para las organizaciones que utilizan [!DNL Trafficking API]. Consulte la documentación de [!DNL Trafficking API] para obtener más información.<!-- Add link to API doc once it's published. -->

Si su organización no utiliza el [!DNL Trafficking API] Si desea obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

## Apéndice: Ejemplo [!UICONTROL CCPA Opt-Out-of-Sale] Solicitud de usuarios de API de Privacy Service

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "adCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

donde:

* `"namespace": "adCloud"` indica el `adCloud` espacio de cookies, y el valor correspondiente es el ID de cookie del cliente recuperado de `AdobePrivacy.js`
* `"include": ["adCloud"]` indica que la solicitud se aplica al Adobe Advertising
