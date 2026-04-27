---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer data access and delete support
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
TQID: https://experienceleague.adobe.com/g7Klc5k3qEPYDKIbTmsQcnklUPVvbN6qqhXaHCHvn3A
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d095671a-1355-40aa-8b5f-06c33c68080bid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1111
ht-degree: 0%

---

# Adobe Advertising support for the California Consumer Privacy Act: Consumer data access and delete support

*For [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; and Adobe Advertising DCO*

>[!IMPORTANT]
>
>The contents of this document are not legal advice and are not meant to substitute for legal advice. Consult with your legal counsel for advice concerning the California Consumer Privacy Act.

The California Consumer Privacy Act (CCPA) is California’s new privacy law, which is effective January 1, 2020. CCPA provides California residents new rights regarding their personal information and imposes data protection responsibilities on certain entities who conduct business in California. CCPA provides consumers with the right to access and delete their personal information as well as the right to opt out of certain activities that qualify as “selling” personal information to a third party.

As a business, you will determine the personal data that Adobe CX Enterprise processes and stores on your behalf.

As your service provider, Adobe Advertising provides support for your business to fulfill its obligations under CCPA that are applicable to the use of Adobe Advertising products and services, including managing requests to access and delete personal information and managing requests to opt out of the sale of personal information.

This document describes how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); and [!DNL Advertising DCO] — as service providers — support consumers&#39; rights to access and delete personal information using the Adobe [!DNL Experience Platform Privacy Service API] and [!DNL Privacy Service UI].

For information about how Advertising DSP supports the consumer right to opt-out of the sale of personal information, see [Adobe Advertising support for the California Consumer Privacy Act: Consumer opt-out of sale support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

For more information about the Adobe Privacy services for CCPA, see the [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Supported data request types for Adobe Advertising

Adobe Experience Platform provides the ability for businesses to complete the following tasks:

* Access a consumer&#39;s cookie-level data or device ID-level data (for ads in mobile apps) within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO].
* Delete cookie-level data stored within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for consumers using a browser; or delete ID-level data stored within [!DNL DSP] for consumers using apps on mobile devices.
* Check the status of one or all existing requests.

## Required setup to send requests for Adobe Advertising

To make requests to access and delete consumer personal information from Adobe Advertising, you must:

1. Deploy a JavaScript library to retrieve and remove your customer&#39;s cookies. The same library, `AdobePrivacy.js`, is used for all Adobe CX Enterprise solutions.

   >[!IMPORTANT]
   >
   >Requests to some CX Enterprise solutions don&#39;t require the JavaScript library, but requests to Adobe Advertising require it.

   You should deploy the library on the webpage from which your customers can submit access and delete requests, such as your company&#39;s privacy portal. The library helps you retrieve Adobe cookies (namespace ID: `gsurferID`) so that you can submit these identities as part of access and delete requests via the [!DNL Adobe Experience Platform Privacy Service API].

   When the customer asks to delete personal data, the library also deletes the customer&#39;s cookie from the customer&#39;s browser.

   >[!NOTE]
   >
   >Deleting personal data is different than opting out, which stops the targeting of an end user with audience segments. However, when a consumer asks to delete personal data from [!DNL Creative], [!DNL DSP], or [!DNL DCO], the library also sends a request to Adobe Advertising to opt out the customer from segment targeting. For advertisers with [!DNL Search, Social, & Commerce], we recommend that you provide your customers a link to [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), which explains how to opt out of audience segment targeting.

1. Identify your CX Enterprise organization ID and make sure that it&#39;s linked to your Adobe Advertising accounts.

   A CX Enterprise organization ID is a 24-character alphanumeric string appended with &quot;@AdobeOrg.&quot; Most CX Enterprise customers have been assigned an organization ID. If your marketing team or internal [!DNL Adobe] system administrator doesn&#39;t know your organization ID, or isn&#39;t sure if it&#39;s been provisioned, then contact your Adobe Account Team. You&#39;ll need the organization ID to submit requests to the Privacy API using the `imsOrgID` namespace.

   >[!IMPORTANT]
   >
   >Contact your company’s Adobe Advertising representative to confirm that all of your organization&#39;s Adobe Advertising accounts — including [!DNL DSP] accounts or advertisers, [!DNL Search, Social, & Commerce] accounts, and [!DNL Creative] or [!DNL DCO] accounts — are linked to your CX Enterprise organization ID.

1. Use either the [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (for automated requests) or the [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=es) (for ad-hoc requests) to submit requests to access and delete personal information to Adobe Advertising on behalf of consumers, and to check the status of existing requests.

   For advertisers who have a mobile app to interact with customers and launch campaigns with [!DNL DSP], you must download the Privacy-ready Mobile SDKs for CX Enterprise. The Mobile SDKs allow businesses to set opt-out status flags, retrieve the consumer&#39;s device ID (namespace ID: `deviceID`), and submit requests to the Privacy Service API. Your mobile app will require an SDK Version 4.15.0 or greater.

   When you submit a consumer access request, the Privacy Service API returns a consumer&#39;s information based on the specified cookie or device ID, which you then must return to the consumer.

   When you submit a consumer delete request, the cookie ID or device ID and all cost, click, and revenue data associated with the cookie are deleted from the server.

   >[!NOTE]
   >
   >If your business has multiple CX Enterprise organization IDs, then you must send separate API requests for each. You can, however make one API request to multiple Adobe Advertising sub-solutions ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], and [!DNL DCO]), with one account per sub-solution.

All steps are necessary to receive support from Adobe Advertising. For more information about these and other related tasks you need to perform using the Adobe Experience Platform Privacy Service, and where to find the necessary items, see [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Required field values in Adobe Advertising JSON requests

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*your CX Enterprise organization ID*>

&quot;users&quot;:

* `"key":` &lt;*usually the name of the customer*>

* `"action":` either `**access**` or `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (which indicates the [[!DNL AdCloud] cookie space](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix))

   * `"value":` &lt;*the actual customer’s cookie ID value as retrieved from`AdobePrivacy.js`*>

* `"include": **adCloud**` (which is the [[!DNL Adobe] product](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix) that applies to the request)

* `"regulation": **ccpa**` (which is the privacy regulation that applies to the request)

## Example of request submitted by a consumer using an Adobe Advertising user ID retrieved from AdobePrivacy.js

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

## Data fields that are returned for access requests

The following is an example of a personal information access response for Adobe Advertising.

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
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
