---
title: Flujo de trabajo para anuncios dinámicos
description: Obtenga información sobre el flujo de trabajo para administrar anuncios dinámicos.
feature: Creative Dynamic Creatives
source-git-commit: e08a3c841e733840058f85a7ecc67571631314b3
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Flujo de trabajo para anuncios dinámicos

1. [Cree una plantilla de anuncio](/help/creative/ad-templates/ad-template-manage.md) para sus anuncios dinámicos basados en los recursos disponibles

1. Configure los elementos de publicidad:

   * (Para anuncios HTML5 estáticos únicos) Recopile y [cargue los recursos de imagen](/help/creative/feeds/asset-manage.md) para sus anuncios.

   * (Para anuncios dinámicos de HTML5) Cree catálogos de los elementos publicitarios:

      1. Cree un archivo de fuente en formato de hoja de cálculo de Excel (XLSX) de Microsoft, con una fila para cada variación de anuncio. Incluya un nombre de imagen o una referencia a un Adobe Experience Manager en cada fila. Recopile por separado los recursos de imagen asociados.

      1. [Cargar el archivo de fuente y los recursos de imagen](/help/creative/feeds/asset-manage.md).

      1. [Cree una plantilla de fuente](/help/creative/feeds/feed-template-manage.md) para asignar los campos del archivo de fuente (hoja de cálculo) a los campos del servidor de Advertising Creative.

      1. [Cree un catálogo](/help/creative/feeds/catalog-manage.md#feed-catalog-create) a partir de un archivo de fuentes especificado y una plantilla de fuentes especificada y, a continuación, [procese el catálogo](/help/creative/feeds/catalog-manage.md#feed-catalog-process) para ver las variaciones de anuncios que se pueden crear a partir de él.

         Cada archivo de fuente solo se puede utilizar para un catálogo.

         Puede [rastrear el estado de los trabajos de procesamiento del catálogo](/help/creative/feeds/job-status-track.md) en la ficha [!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status].

1. [Crear elementos creativos dinámicos](/help/creative/creative-libraries/creative-add-dynamic.md) para una biblioteca creativa. Para los anuncios dinámicos de HTML5, utilice una plantilla de anuncio y catálogos especificados.

1. [Crear paquetes de anuncios dinámicos](/help/creative/creative-libraries/bundle-manage.md) que puede adjuntar todos a la vez a una experiencia de anuncio.

1. Cree experiencias de publicidad dinámica con [con ](/help/creative/experiences/experience-create-targeting.md) o [segmentación](/help/creative/experiences/experience-create-no-targeting.md) y [asígneles paquetes a sus experiencias de publicidad dinámica](/help/creative/experiences/experience-assign-creative-bundles.md).

1. [Genere e implemente etiquetas de experiencia de anuncio](/help/creative/experiences/experience-tag-export.md) para ejecutarlas como anuncios en su DSP.

   Para utilizar una experiencia de anuncio como anuncio en Adobe Advertising DSP, cargue la etiqueta de experiencia de anuncio en una campaña de Advertising DSP. Para utilizar una experiencia publicitaria como anuncio en un DSP diferente, implemente la etiqueta de experiencia publicitaria en ese DSP.
