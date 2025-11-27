---
title: Configuración de los planes de alcance de TV conectado
description: Consulte las descripciones de los ajustes de los planes de alcance de TV conectados.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Configuración de los planes de alcance de TV conectado

<!-- Move out of table for consistency at some point. -->

| Parámetro | Descripción | ¿Requerido? |
| --- | --- | --- |
| [!UICONTROL Name] | El nombre para identificar su plan. | Sí |
| [!UICONTROL Advertiser] | Anunciante específico de la cuenta para la que se está creando el plan. | Sí |
| [!UICONTROL Media Type] | El tipo de medios que se incluirán en el plan.<br><br>Actualmente, solo está disponible [!UICONTROL Connected TV]. | Sí |
| [!UICONTROL Date Range] | Las fechas de inicio y finalización del plan.<br><br>La fecha de inicio no puede ser anterior a la fecha actual. El intervalo de fecha no puede ser superior a 90 días. | Sí |
| [!UICONTROL Goal Type] | El tipo de objetivo (como [!UICONTROL Budget]) a tener en cuenta en el plan.<br><br>Actualmente, solo está disponible [!UICONTROL Budget]. | Sí |
| [!UICONTROL Goal Value] | El valor de objetivo de la previsión. Para obtener resultados de previsión más precisos, utilice un valor > 5000 USD. | Sí |
| [!UICONTROL Max Bid] | La cantidad máxima para pagar 1000 impresiones. Si se selecciona el tipo de medio [!UICONTROL Connected TV], escriba un valor de al menos 10 USD. | Sí |
| [!UICONTROL Frequency Cap] | La cantidad de veces que se debe publicar un anuncio en un hogar único.<br><br>Cuando implemente un plan y deba crear varias ubicaciones, aplique la configuración de límite de frecuencia en el nivel de paquete, no en el nivel de ubicación, para garantizar una entrega adecuada. | Sí |
| [!UICONTROL Geo-Targeting] | Ubicaciones que se incluirán o excluirán como destinos. Las opciones incluyen:<ul><li>Países, ciudades o estados: haga clic en la ficha **[!UICONTROL Country/State/City]**; seleccione si el área es un *País*, *Estado* o *Ciudad*; si lo desea, expanda cualquier ubicación para ver sus subcomponentes y, a continuación, haga clic en **[!UICONTROL Include]** o **[!UICONTROL Exclude]** junto a la ubicación.</li><li>Áreas de mercado designadas (DMA) en Estados Unidos: haga clic en la ficha **[!UICONTROL DMA]**; si lo desea, expanda cualquier estado para ver sus DMA y, a continuación, haga clic en **[!UICONTROL Include]** o **[!UICONTROL Exclude]** junto a la ubicación.</li><li>Códigos postales: puede:<ul><li>Haga clic en la ficha **[!UICONTROL Search postal code]**, seleccione el país, escriba el nombre completo de la ciudad o las letras que contiene el nombre de la ciudad y, a continuación, presione la tecla **[Escriba]**, haga clic en el nombre de ciudad correcto para ver todos los códigos postales de la ciudad, haga clic en el código postal correcto y, a continuación, haga clic en **[!UICONTROL Include]** o **[!UICONTROL Exclude]**.</li><li>Haga clic en la ficha **[!UICONTROL Paste postal code]**, seleccione el país, introduzca o pegue valores separados por comas y, a continuación, haga clic en **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**.</li></ul></li></ul> | Sí |
| [!UICONTROL Inventory Targeting] | Orígenes de inventario que se deben incluir o excluir como destinos. Seleccione al menos una fuente o fuente. | Sí |
| [!UICONTROL Site/App Targeting] | Sitios web y aplicaciones que se incluirán o excluirán como destinatarios. Escriba una dirección URL por línea y haga clic en **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]**. | No |
| [!UICONTROL Audience Targeting] | Audiencias que se deben incluir o excluir como destinatarios. | No |
| [!UICONTROL Ad duration] | La duración de los anuncios que se deben tener en cuenta en el plan. | No |

>[!MORELIKETHIS]
>
>* [Acerca de la herramienta de planificación de DSP](planner-about.md)
>* [Crear un plan de alcance de TV conectado](planner-create.md)
>* [Duplicar un plan de alcance de TV conectado](planner-duplicate.md)
>* [Editar un plan de alcance de TV conectado](planner-edit.md)
>* [Exportar un plan de alcance de TV conectado](planner-export.md)
>* [Volver a generar la previsión para un plan de alcance de TV conectado](planner-forecast.md)
>* [Archivar un plan de alcance de TV conectado](planner-archive.md)
