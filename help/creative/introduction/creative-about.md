---
title: Acerca de Adobe Advertising Creative
description: Más información sobre [!DNL Creative].
feature: Creative Introduction
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Acerca de Adobe Advertising Creative 2.0

*Beta cerrada*

<!-- verify all and rewrite to include new stuff -->

Como parte de Adobe Advertising, Advertising Creative es una plataforma de autoservicio para automatizar experiencias publicitarias personalizadas en tiempo real y, opcionalmente, optimizar los anuncios en el nivel de elemento creativo.

## Bibliotecas creativas personalizadas de creativos reutilizables

Las bibliotecas de Creative le permiten administrar los elementos creativos que utilizará en las experiencias publicitarias. Puede crear varias bibliotecas, cada una con creativos y grupos creativos individuales (llamados *paquetes*). Agregará paquetes creativos a las experiencias publicitarias.

## Experiencias basadas en reglas

Con [!DNL Creative], puedes crear historias usando un modelo de árbol de decisiones basado en reglas: desplegando una cadena coreográfica de anuncios que se personalizan en tiempo real en función de lo que sabes sobre tu audiencia y que siguen a tus clientes incluso cuando se mudan a diferentes sitios web<!-- verify if that's true without Adobe CDP -->. Por ejemplo: las historias pueden cambiar según el comportamiento del cliente, la ubicación geográfica, la demografía, el redireccionamiento, la posición en el recorrido del cliente, etc.

### Implementación de experiencias como anuncios

Una vez creada una experiencia, puede generar una etiqueta JavaScript o iframe para la experiencia e implementarla como un anuncio de terceros en Advertising DSP o en cualquier otro DSP.<!-- Add any more info about integration with DSP? -->

<!-- Maybe add a subsection "Audience targeting options" with info about types of creative-level REtargeting and placement-level targeting within your DSP.  Need to clarify if any placement-level targeting might contradict/override creative-level targeting, or if they're completely different.

Advertiser should be able to target all segments which are available in DSP for targeting
-->

### Optimización de los elementos publicitarios

Opcionalmente, puede permitir que [!DNL Creative] optimice los elementos de publicidad para cualquier experiencia en función del rendimiento, defina o no objetivos de audiencia específicos, mediante la rotación de publicidad optimizada y ponderada, que funciona con Adobe Sensei.

## Redireccionamiento de píxeles

Puede crear píxeles de retargeting para utilizarlos como objetivos para creativos dentro de una experiencia publicitaria. Los objetivos muestran anuncios únicamente a los usuarios con atributos especificados que visitaron anteriormente páginas web específicas.

## Seguimiento de impresión, clics y conversiones

[!DNL Creative] registra automáticamente todas las impresiones y clics de anuncios publicados desde una experiencia. También puede añadir direcciones URL de seguimiento de impresiones y clics de terceros a los creativos de las bibliotecas de Creative, así como direcciones URL de seguimiento personalizadas en una experiencia.

[!DNL Creative] también hace un seguimiento de las conversiones de los anuncios publicados creados a partir de sus experiencias publicitarias.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optoinal?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Informes de rendimiento

Puede ver informes de rendimiento detallados y de nivel de experiencia en Creativos > Experiencias.

También puede crear informes personalizados de Creative en Informes > Informes personalizados para monitorizar el rendimiento de nivel de experiencia en todas las experiencias. Si usas tus experiencias de [!DNL Creative] como anuncios en campañas de DSP, los datos de rendimiento de esos anuncios estarán disponibles en informes personalizados adicionales, al igual que los datos de los demás anuncios de DSP. <!-- Verify that [!DNL Creative] users have access to ALL other reports, and if I can completely duplicate the report help for both help sets. -->

Opcionalmente, puede enviar sus informes personalizados a [destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md) especificados.

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Acerca de sus bibliotecas creativas](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Acerca de las experiencias en Advertising Creative](/help/creative/experiences/experience-about.md)
