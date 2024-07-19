---
title: Compatibilidad del Adobe Advertising con la Ley de Privacidad del Consumidor de California &#58; Compatibilidad de acceso y eliminación de datos del consumidor
description: Obtenga información sobre los tipos de solicitud de datos admitidos, los valores de configuración y campo requeridos, y ejemplos de solicitudes de acceso a la API que utilizan ID de productos heredados y campos de datos devueltos.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# Compatibilidad del Adobe Advertising con la Ley de Privacidad del Consumidor de California: Compatibilidad de acceso y eliminación de datos del consumidor

*Para [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; y DCO de Adobe Advertising*

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor legal para obtener asesoramiento sobre la Ley de Privacidad del Consumidor de California.

La Ley de Privacidad del Consumidor de California (CCPA) es la nueva ley de privacidad de California que entró en vigor el 1 de enero de 2020. La CCPA otorga a los residentes de California nuevos derechos con respecto a su información personal e impone responsabilidades de protección de datos a ciertas entidades que hacen negocios en California. La CCPA otorga a los consumidores el derecho de acceder a sus datos personales y suprimirlos, así como el derecho de exclusión de determinadas actividades que pueden considerarse &quot;vendedoras&quot; de información personal a terceros.

Como empresa, determinará los datos personales que Adobe Experience Cloud procesa y almacena en su nombre.

Como proveedor de servicio, Adobe Advertising proporciona asistencia a su empresa para que cumpla con las obligaciones que le impone CCPA y que son aplicables al uso de productos y servicios de Adobe Advertising, incluida la gestión de solicitudes de acceso y eliminación de información personal y la gestión de solicitudes de exclusión de la venta de información personal.

En este documento se describe cómo [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); y [!DNL Advertising DCO] — como proveedores de servicios — admiten los derechos de los consumidores para acceder y eliminar información personal mediante el Adobe [!DNL Experience Platform Privacy Service API] y [!DNL Privacy Service UI].

Para obtener información sobre cómo Advertising DSP admite el derecho del consumidor a no participar en la venta de información personal, consulte [Compatibilidad de Adobe Advertising con la Ley de Privacidad del Consumidor de California: Compatibilidad con la exclusión del consumidor](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

Para obtener más información sobre los servicios de privacidad de Adobe para la CCPA, consulte el [Centro de privacidad de Adobe](https://www.adobe.com/privacy/ccpa.html).

## Tipos de solicitud de datos admitidos para el Adobe Advertising

Adobe Experience Platform permite a las empresas completar las siguientes tareas:

* Acceda a los datos de nivel de cookie de un consumidor o a los datos de nivel de ID de dispositivo (para anuncios en aplicaciones móviles) en [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] o [!DNL DCO].
* Elimine los datos de nivel de cookie almacenados en [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] o [!DNL DCO] para los consumidores que usan un explorador; o elimine los datos de nivel de ID almacenados en [!DNL DSP] para los consumidores que usan aplicaciones en dispositivos móviles.
* Compruebe el estado de una o todas las solicitudes existentes.

## Configuración requerida para enviar solicitudes de Adobe Advertising

Para realizar solicitudes de acceso y eliminación de información personal del consumidor desde el Adobe Advertising, debe:

1. Implemente una biblioteca JavaScript para recuperar y eliminar las cookies del cliente. Se utiliza la misma biblioteca `AdobePrivacy.js` para todas las soluciones de Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Las solicitudes a algunas soluciones de Experience Cloud no requieren la biblioteca JavaScript, pero las solicitudes a Adobe Advertising sí la requieren.

   Debe implementar la biblioteca en la página web desde la que los clientes pueden enviar solicitudes de acceso y eliminación, como el portal de privacidad de la compañía. La biblioteca le ayuda a recuperar las cookies de Adobe (id. de área de nombres: `gsurferID`) para que pueda enviar estas identidades como parte de las solicitudes de acceso y eliminación a través de [!DNL Adobe Experience Platform Privacy Service API].

   Cuando el cliente solicita eliminar datos personales, la biblioteca también elimina la cookie del cliente del explorador del cliente.

   >[!NOTE]
   >
   >La eliminación de datos personales es diferente a la exclusión, lo que detiene el direccionamiento de un usuario final con segmentos de audiencia. Sin embargo, cuando un consumidor solicita eliminar datos personales de [!DNL Creative], [!DNL DSP] o [!DNL DCO], la biblioteca también envía una solicitud al Adobe Advertising para excluir al cliente de la segmentación de segmentos. Para los anunciantes con [!DNL Search, Social, & Commerce], le recomendamos que proporcione a sus clientes un vínculo a [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), que explica cómo excluirse de la segmentación de segmentos de audiencia.

1. Identifique su ID de organización de Experience Cloud y asegúrese de que esté vinculado a sus cuentas de Adobe Advertising.

   Un ID de organización de Experience Cloud es una cadena alfanumérica de 24 caracteres anexada a &quot;@AdobeOrg&quot;. A la mayoría de los clientes de Experience Cloud se les ha asignado un ID de organización. Si el equipo de marketing o el administrador interno del sistema [!DNL Adobe] no conocen el identificador de la organización o no están seguros de si se ha proporcionado, póngase en contacto con el equipo de cuenta de Adobe. Necesitará el identificador de organización para enviar solicitudes a la API de privacidad mediante el área de nombres `imsOrgID`.

   >[!IMPORTANT]
   >
   >Póngase en contacto con el representante del Adobe Advertising de su compañía para confirmar que todas las cuentas de Adobe Advertising de su organización, incluidas las cuentas de [!DNL DSP] o anunciantes, las cuentas de [!DNL Search, Social, & Commerce] y las cuentas de [!DNL Creative] o [!DNL DCO], están vinculadas a su ID de organización de Experience Cloud.

1. Use la [API de Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitudes automatizadas) o la [IU de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=es) (para solicitudes ad hoc) para enviar solicitudes de acceso y eliminación de información personal al Adobe Advertising en representación de los consumidores, y para comprobar el estado de las solicitudes existentes.

   Para que los anunciantes que tengan una aplicación móvil interactúen con los clientes e inicien campañas con [!DNL DSP], debe descargar los SDK móviles preparados para la privacidad para Experience Cloud. Los SDK móviles permiten a las empresas establecer indicadores de estado de exclusión, recuperar el ID de dispositivo del consumidor (ID de área de nombres: `deviceID`) y enviar solicitudes a la API de Privacy Service. Su aplicación móvil requerirá una versión 4.15.0 o superior del SDK.

   Cuando envía una solicitud de acceso de consumidor, la API de Privacy Service devuelve la información de un consumidor en función de la cookie especificada o el ID de dispositivo, que debe devolver al consumidor.

   Cuando envía una solicitud de eliminación de consumidor, el ID de cookie o el ID de dispositivo y todos los datos de costes, clics e ingresos asociados con la cookie se eliminan del servidor.

   >[!NOTE]
   >
   >Si su empresa tiene varios ID de organización de Experience Cloud, debe enviar solicitudes de API independientes para cada uno. Sin embargo, puede realizar una solicitud de API a varias subsoluciones de Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP] y [!DNL DCO]), con una cuenta por subsolución.

Todos estos pasos son necesarios para recibir asistencia del Adobe Advertising. Para obtener más información acerca de estas y otras tareas relacionadas que necesita realizar con Adobe Experience Platform Privacy Service y dónde encontrar los elementos necesarios, vea [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Valores de campo requeridos en solicitudes JSON de Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*su ID de organización Experience Cloud*>

&quot;usuarios&quot;:

* `"key":` &lt;*suele ser el nombre del cliente*>

* `"action":` `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (que indica el espacio de cookie [!DNL adCloud])

   * `"value":` &lt;*el valor real del ID de cookie del cliente recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que es el producto [!DNL Adobe] que se aplica a la solicitud)

* `"regulation": **ccpa**` (que es la norma de privacidad que se aplica a la solicitud)

## Ejemplo de solicitud enviada por un consumidor con un ID de usuario de Adobe Advertising recuperado de AdobePrivacy.js

```
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
```

## Campos de datos que se devuelven para las solicitudes de acceso

A continuación se muestra un ejemplo de una respuesta de acceso a información personal para el Adobe Advertising.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
