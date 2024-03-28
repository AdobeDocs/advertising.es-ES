---
title: Cumplimiento del Adobe Advertising del Reglamento General de Protección de Datos
description: Obtenga información sobre los tipos de solicitud de datos admitidos, los valores de configuración y campo requeridos, y ejemplos de solicitudes de acceso a la API que utilizan ID de productos heredados y campos de datos devueltos
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 80072930c0506a017a927ce53eaad900a2642e92
workflow-type: tm+mt
source-wordcount: '1002'
ht-degree: 0%

---

# Cumplimiento del Adobe Advertising del Reglamento General de Protección de Datos

*Para [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; y Adobe Advertising DCO*

>[!IMPORTANT]
>
>El contenido de este documento no constituye asesoramiento jurídico y no está pensado para sustituir el asesoramiento jurídico. Consulte con su asesor jurídico para obtener asesoramiento sobre el Reglamento General de Protección de Datos.

El Reglamento General de Protección de Datos (RGPD), una ley vigente desde el 25 de mayo de 2018, otorga a todos los individuos (sujetos de datos) dentro de las fronteras de la Unión Europea (UE) el control de sus datos personales y simplifica el entorno regulador de las empresas internacionales. Esta ley se aplica a todas las empresas (responsables del tratamiento de datos) que ofrecen bienes o servicios a personas que se encuentran dentro de los límites de la UE, supervisan o recopilan datos personales de personas de la UE en el momento en que se procesan sus datos personales, independientemente de la ubicación comercial del responsable del tratamiento de datos.

Adobe Experience Cloud actúa como encargado del tratamiento de datos de cualquier dato personal que reciba y almacene en nombre de sus clientes. Como responsable del tratamiento de datos, determinará qué datos personales Adobe Experience Cloud trata y almacena en su nombre.

Este documento describe cómo [!DNL Advertising Search, Social, & Commerce]; Advertising Creative DSP; Advertising (Demand Side Platform); y [!DNL Advertising DCO] admiten los derechos de acceso y eliminación de datos del RGPD de las partes interesadas mediante la API de Adobe Experience Platform Privacy Service y la IU de Privacy Service.

Para obtener más información sobre el significado del RGPD para su empresa, consulte [RGPD y su empresa](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Tipos de solicitud de datos admitidos para el Adobe Advertising

Adobe Experience Platform permite a las empresas completar las siguientes tareas:

* Acceder a los datos de un interesado en cuanto a cookies o a los datos en cuanto a ID de dispositivo (para anuncios en aplicaciones móviles) en [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], o [!DNL DCO].
* Eliminar datos de nivel de cookie almacenados en [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], o [!DNL DCO] para interesados que utilicen un explorador, o eliminar datos de nivel de ID almacenados en [!DNL DSP] para interesados que utilizan aplicaciones en dispositivos móviles.
* Compruebe el estado de una o todas las solicitudes existentes.

## Configuración requerida para enviar solicitudes de Adobe Advertising

Para realizar solicitudes de acceso y eliminación de datos para el Adobe Advertising, deberá:

1. Implemente una biblioteca JavaScript para recuperar y eliminar las cookies del interesado. La misma biblioteca, `AdobePrivacy.js`, se utiliza para todas las soluciones de Adobe Experience Cloud.

   >[!IMPORTANT]
   >
   >Las solicitudes a algunas soluciones de Experience Cloud no requieren la biblioteca JavaScript, pero las solicitudes a Adobe Advertising sí la requieren.

   Debe implementar la biblioteca en la página web desde la que los interesados pueden enviar solicitudes de acceso y eliminación, como el portal de privacidad de la empresa. La biblioteca le ayuda a recuperar [!DNL Adobe] cookies (ID de área de nombres: `gsurferID`) para que pueda enviar estas identidades como parte de las solicitudes de acceso y eliminación mediante la API de Adobe Experience Platform Privacy Service.

   Cuando el interesado solicita la eliminación de datos personales, la biblioteca también elimina la cookie del interesado del explorador del interesado.

   >[!NOTE]
   >
   >La eliminación de datos personales es diferente a la exclusión, que detiene el direccionamiento de un usuario final con segmentos de audiencia. Sin embargo, cuando un interesado pida eliminar datos personales de [!DNL Creative], [!DNL DSP], o [!DNL DCO]Además, la biblioteca también envía una solicitud al Adobe Advertising para que excluya al interesado de la segmentación de segmentos. Para anunciantes con [!DNL Search, Social, & Commerce], le recomendamos que proporcione a los interesados un vínculo a [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), que explica cómo excluirse de la segmentación de segmentos de audiencia.

1. Identifique su ID de organización de Experience Cloud y asegúrese de que esté vinculado a sus cuentas de Adobe Advertising.

   Un ID de organización de Experience Cloud es una cadena alfanumérica de 24 caracteres anexada a &quot;@AdobeOrg&quot;. A la mayoría de los clientes de Experience Cloud se les ha asignado un ID de organización. Si su equipo de marketing o [!DNL Adobe] el administrador del sistema no conoce su ID de organización o no está seguro de si se ha proporcionado, póngase en contacto con el Servicio de atención al cliente de Adobe en gdprsupport@adobe.com. Necesitará el ID de organización para enviar solicitudes a la API de privacidad mediante `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Póngase en contacto con el representante de Adobe Advertising de su compañía para confirmar que todas las cuentas de Adobe Advertising de su organización, incluidas [!DNL DSP] cuentas o anunciantes, [!DNL Search, Social, & Commerce] cuentas, y [!DNL Creative] o [!DNL DCO] cuentas: están vinculadas a su ID de organización de Experience Cloud.

1. Utilice cualquiera de las [API de Adobe Experience Platform Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (para solicitudes automatizadas) o la [IU de Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=es) (en el caso de solicitudes ad hoc) para enviar solicitudes de acceso y eliminación al Adobe Advertising por cuenta de los interesados, y para comprobar el estado de las solicitudes existentes.

   DSP Para que los anunciantes que tengan una aplicación móvil interactúen con los interesados y lancen campañas con, deberá descargar los SDK móviles preparados para la privacidad para Experience Cloud de, que están preparados para la aplicación. Los SDK móviles permiten a los controladores de datos establecer indicadores de estado de exclusión y recuperar el ID de dispositivo (ID de área de nombres: `deviceID`) y envíe solicitudes a la API de Privacy Service. Su aplicación móvil requerirá una versión 4.15.0 o superior del SDK.

   Al enviar la solicitud de acceso de un interesado, la API de Privacy Service devuelve la información de dicho interesado en función de la cookie o el ID de dispositivo especificados, que debe devolver al interesado.

   Al enviar la solicitud de eliminación de un interesado, se eliminan del servidor el ID de cookie o el ID de dispositivo y todos los datos de costes, clics e ingresos asociados con la cookie.

   >[!NOTE]
   >
   >Si su empresa tiene varios ID de organización de Experience Cloud, debe enviar solicitudes de API independientes para cada uno. Sin embargo, puede realizar una solicitud de API a varias subsoluciones de Adobe Advertising ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], y [!DNL DCO]), con una cuenta por subsolución.

Todos estos pasos son necesarios para el Adobe Advertising. Para obtener más información sobre estas y otras tareas relacionadas que debe realizar con Adobe Experience Platform Privacy Service y dónde encontrar los elementos que necesita, consulte &quot;[Introducción al Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).&quot;

## Valores de campo requeridos en solicitudes JSON de Adobe Advertising

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*su ID de organización de Experience Cloud*>

`"users":`

* `"key":` &lt;*normalmente, el nombre del interesado*>

* `"action":` o bien `**access**` o `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (lo que indica que [!DNL adcloud] cookie space)

   * `"value":` &lt;*el valor real de la ID de cookie del interesado recuperado de`AdobePrivacy.js`*>

* `"include": **adCloud**` (que es el [!DNL Adobe] producto que se aplica a la solicitud)

* `"regulation": **gdpr**` (que es la norma de privacidad que se aplica a la solicitud)

## Ejemplo de solicitud enviada por el sujeto de datos mediante un ID de usuario de Adobe Advertising recuperado de `AdobePrivacy.js`

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
    "regulation":"gdpr"
}
```

## Campos de datos que se devuelven para las solicitudes de acceso

A continuación se muestra un ejemplo de una respuesta de acceso para el Adobe Advertising.

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
