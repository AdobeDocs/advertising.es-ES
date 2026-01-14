---
title: Acerca de Adobe Advertising Creative
description: Más información sobre [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 0%

---

# Acerca de Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

Como parte de Adobe Advertising, Advertising Creative es una plataforma de autoservicio para automatizar experiencias publicitarias personalizadas en tiempo real y, opcionalmente, optimizar los anuncios en el nivel de elemento creativo.<!-- Verify -->: puede implementar las experiencias publicitarias como anuncios en cualquier DSP, incluido Adobe Advertising DSP.

## Bibliotecas creativas personalizadas de creativos reutilizables

Las bibliotecas de Creative le permiten administrar los elementos creativos que utilizará en las experiencias publicitarias. Puede crear varias bibliotecas, cada una con creativos y grupos creativos individuales (denominados *paquetes*, que adjuntará a las experiencias).

### [!DNL Adobe] integraciones de recursos

[!DNL Creative] está directamente integrado con Adobe Experience Manager, lo que le permite cargar fácilmente los recursos de imagen [!DNL Adobe] que el equipo de diseño crea y aprueba para los anuncios de imagen estándar.

## Experiencias basadas en reglas y sin segmentación

* **Experiencias segmentadas y basadas en reglas:** Cree historias con un modelo de árbol de decisiones basado en reglas, para desplegar una cadena coreográfica de anuncios que se personalizan en tiempo real según lo que sepa sobre su audiencia. Por ejemplo: las historias pueden cambiar según el comportamiento del cliente, la ubicación geográfica, la demografía, el redireccionamiento, la posición en el recorrido del cliente, etc.

* **Experiencias sin objetivo:** Programe y optimice los elementos de anuncio sin reducir la audiencia.

### Integraciones de datos de [!DNL Adobe]

Puede usar sus segmentos de audiencia propios de Adobe Audience Manager y Adobe Analytics, así como los segmentos de audiencia personalizados que cree en Advertising DSP y los píxeles de retargeting que cree con [!DNL Creative], como objetivos para determinados elementos creativos de una experiencia publicitaria. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Implementación de experiencias como anuncios

Una vez creada una experiencia, puede generar una etiqueta JavaScript o iframe para ella e implementarla como una publicidad de terceros en una campaña de Advertising DSP o en cualquier otra DSP.

### Optimización de los elementos publicitarios

Opcionalmente, puede permitir que [!DNL Creative] optimice los elementos de publicidad para cualquier experiencia en función del rendimiento, defina o no objetivos de audiencia específicos, mediante la rotación de publicidad optimizada y ponderada, que funciona con [!DNL Adobe AI].

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## Redireccionamiento de píxeles

Puede crear píxeles de retargeting para utilizarlos como objetivos para creativos dentro de una experiencia publicitaria. Los objetivos muestran anuncios únicamente a los usuarios con atributos especificados que visitaron anteriormente páginas web específicas.

## Seguimiento de impresión, clics y conversiones

[!DNL Creative] registra automáticamente todas las impresiones y clics de anuncios publicados desde una experiencia. También puede añadir direcciones URL de seguimiento de impresiones y clics de terceros a los creativos de las bibliotecas de Creative, así como direcciones URL de seguimiento personalizadas en una experiencia.

[!DNL Creative] también hace un seguimiento de las conversiones de los anuncios publicados creados a partir de sus experiencias publicitarias.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Informes de rendimiento

Puede ver informes de rendimiento detallados y de nivel de experiencia en Creativos > Experiencias.

También puede crear informes personalizados de Creative en Informes > Informes personalizados para monitorizar el rendimiento de nivel de experiencia en todas las experiencias. Si usas tus experiencias de [!DNL Creative] como anuncios en campañas de DSP, los datos de rendimiento de esos anuncios estarán disponibles en informes personalizados adicionales, al igual que los datos de los demás anuncios de DSP. <!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

Opcionalmente, puede enviar sus informes personalizados a [destinos de informe](/help/dsp/reports/report-destinations/report-destination-about.md) especificados.

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [Acerca de sus bibliotecas creativas](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Acerca de las experiencias en Advertising Creative](/help/creative/experiences/experience-about.md)
