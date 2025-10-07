---
title: Campos disponibles para archivos de fuentes de publicidad dinámica
description: Obtenga información acerca de los campos que puede incluir en los archivos de fuente que utiliza para crear anuncios dinámicos.
feature: Creative Dynamic Ads
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Apéndice: Campos disponibles para archivos de fuentes de publicidad dinámica

Los siguientes campos de fuente están disponibles en el backend de Advertising Creative. Puede cargar un [archivo de fuente](/help/creative/feeds/asset-manage.md) que usa nombres de campo específicos de su organización. Sin embargo, para poder crear un [catálogo](/help/creative/feeds/catalog-manage.md) a partir del archivo de fuente, debe asignar cada campo del archivo de fuente a uno de los siguientes campos de la [plantilla de fuente](/help/creative/feeds/feed-template-manage.md) que usará para crear el catálogo.

El único campo que debe tener un equivalente en el archivo de fuente es `PART_NUM`.

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| Nombre de campo | Tipo de datos | ¿Requerido? |
|------------|-----------|-----------|
| NÚM_PARTE | varchar(64) | SÍ |
| PRODUCT_NAME | texto | NO |
| PRODUCT_URL | texto | NO |
| PRECIO | decimal(10,2) | NO |
| DISCOUNT_PRICE | decimal(10,2) | NO |
| IMAGEN | varchar(1024) | NO |
| IMAGE_HEIGHT | int | NO |
| IMAGE_WIDTH | int | NO |
| IMAGE_1 | varchar(1024) | NO |
| IMAGE_2 | varchar(1024) | NO |
| IMAGE_3 | varchar(1024) | NO |
| IMAGE_4 | varchar(1024) | NO |
| IMAGE_5 | varchar(1024) | NO |
| IMAGE_6 | varchar(1024) | NO |
| IMAGE_7 | varchar(1024) | NO |
| IMAGE_8 | varchar(1024) | NO |
| IMAGE_9 | varchar(1024) | NO |
| IMAGE_10 | varchar(1024) | NO |
| TEXT_1 | texto | NO |
| TEXT_2 | texto | NO |
| TEXT_3 | texto | NO |
| TEXT_4 | texto | NO |
| TEXT_5 | texto | NO |
| TEXT_6 | texto | NO |
| TEXT_7 | texto | NO |
| TEXT_8 | texto | NO |
| TEXT_9 | texto | NO |
| TEXT_10 | texto | NO |
| TEXT_11 | texto | NO |
| TEXT_12 | texto | NO |
| TEXT_13 | texto | NO |
| TEXT_14 | texto | NO |
| TEXT_15 | texto | NO |
| ADDITIONAL_PRICE_1 | decimal(10,2) | NO |
| ADDITIONAL_PRICE_2 | decimal(10,2) | NO |
| ADDITIONAL_PRICE_3 | decimal(10,2) | NO |
| AD_SIZE | varchar(32) | NO |
| CLASIFICAR | int | NO |
| PAÍS | texto | NO |
| ESTADO | texto | NO |
| CIUDAD | texto | NO |
| ZIP | texto | NO |
| DMA | texto | NO |
| PROFILE_FILTER_1 | texto | NO |
| PROFILE_FILTER_2 | texto | NO |
| PROFILE_FILTER_3 | texto | NO |
| PROFILE_FILTER_4 | texto | NO |
| PROFILE_FILTER_5 | texto | NO |
| DATAPASS_FILTER_1 | texto | NO |
| DATAPASS_FILTER_2 | texto | NO |
| DATAPASS_FILTER_3 | texto | NO |
| DATAPASS_FILTER_4 | texto | NO |
| DATAPASS_FILTER_5 | texto | NO |
| AUDIENCE_SEGMENT | texto | NO |
| IDIOMA | texto | NO |
| CREATIVE_ATTRIBUTE_1 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_2 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_3 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_4 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_5 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_6 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_7 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_8 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_9 | varchar(256) | NO |
| CREATIVE_ATTRIBUTE_10 | varchar(256) | NO |
| IS_DEFAULT | enum | NO |

>[!MORELIKETHIS]
>
>* [Flujos de trabajo para anuncios dinámicos](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Administrar archivos de recursos](/help/creative/feeds/asset-manage.md)
>* [Administrar plantillas de fuentes](/help/creative/feeds/feed-template-manage.md)
>* [Administrar catálogos](/help/creative/feeds/catalog-manage.md)
