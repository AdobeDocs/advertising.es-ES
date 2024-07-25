---
title: Configuración de los planes de alcance de TV conectado
description: Consulte las descripciones de los ajustes de los planes de alcance de TV conectados.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 37b901093d7eff65d783e558f2e98c5d288a8286
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Configuración de los planes de alcance de TV conectado

| Parámetro | Descripción | ¿Requerido? |
| --- | --- | --- |
| Nombre | El nombre para identificar su plan. | Sí |
| Anunciante | Anunciante específico de la cuenta para la que se está creando el plan. | Sí |
| Tipo de medio | El tipo de medios que se incluirán en el plan.<br><br>Actualmente, solo está disponible [!UICONTROL Connected TV]. | Sí |
| Intervalo de fechas | Las fechas de inicio y finalización del plan.<br><br>La fecha de inicio no puede ser anterior a la fecha actual. El intervalo de fecha no puede ser superior a 90 días. | Sí |
| Tipo de meta | El tipo de objetivo (como [!UICONTROL Budget]) a tener en cuenta en el plan.<br><br>Actualmente, solo está disponible [!UICONTROL Budget]. | Sí |
| Valor de meta | El valor de objetivo de la previsión. Para obtener resultados de previsión más precisos, utilice un valor > 5000 USD. | Sí |
| Puja máxima | La cantidad máxima para pagar 1000 impresiones. Si se selecciona el tipo de medio [!UICONTROL Connected TV], escriba un valor de al menos 10 USD. | Sí |
| Límite de frecuencia | La cantidad de veces que se debe publicar un anuncio en un hogar único.<br><br>Cuando implemente un plan y deba crear varias ubicaciones, aplique la configuración de límite de frecuencia en el nivel de paquete, no en el nivel de ubicación, para garantizar una entrega adecuada. | Sí |
| Segmentación geográfica | Ubicaciones que se incluirán o excluirán como destinos. Las opciones incluyen países, ciudades, estados, áreas de mercado designadas (DMA) y códigos postales (que puede a) pegar como valores separados por comas para un país especificado o b) buscar por país y ciudad). | Sí |
| Segmentación de inventario | Orígenes de inventario que se deben incluir o excluir como destinos. Seleccione al menos una fuente o fuente. | Sí |
| Segmentación de sitios/aplicaciones | Sitios web y aplicaciones que se incluirán o excluirán como destinatarios. Escriba una dirección URL por línea y haga clic en **[!UICONTROL Include All]** o **[!UICONTROL Exclude All]** debajo del campo de entrada. | No |
| Segmentación de audiencia | Audiencias que se deben incluir o excluir como destinatarios. | No |
| Duración del anuncio | La duración de los anuncios que se deben tener en cuenta en el plan. | No |

>[!MORELIKETHIS]
>
>* DSP [Acerca de la herramienta Planificador de](planner-about.md)
>* [Crear un plan de alcance de TV conectado](planner-create.md)
>* [Duplicar un plan de alcance de TV conectado](planner-duplicate.md)
>* [Editar un plan de alcance de TV conectado](planner-edit.md)
>* [Exportar un plan de alcance de TV conectado](planner-export.md)
>* [Volver a generar la previsión para un plan de alcance de TV conectado](planner-forecast.md)
>* [Archivar un plan de alcance de TV conectado](planner-archive.md)
