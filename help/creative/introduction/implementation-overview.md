---
title: Información general sobre la implementación del Adobe Advertising Creative
description: Obtenga información acerca del flujo de trabajo básico para implementar  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Información general sobre la implementación del Adobe Advertising Creative

*Beta cerrada*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

DSP El equipo de operaciones de [!DNL Creative] trabaja con cada anunciante para configurar sus experiencias creativas y creativas, ya sea implementando las experiencias publicitarias como anuncios dentro del equipo o proporcionando a su equipo las etiquetas de anuncios de terceros para que se implementen a sí mismos, y validando los datos iniciales de costo, clics y conversión.

De forma continua, el equipo de cuenta de Adobe, el equipo de la agencia o el anunciante (según los términos de la service level agreement) deben monitorizar cada experiencia y editarla según sea necesario para cumplir los objetivos del anunciante.

## Tareas de configuración iniciales para [!DNL Creative] campañas <!-- Experiences? "Campaigns" may be confusing now. -->

El equipo de implementación o su agencia trabajarán con usted para lo siguiente:

1. Defina sus objetivos de personalización (por ejemplo, si personalizará los anuncios para prospección o retargeting); todos los datos de origen, segundo y tercero disponibles, incluidos los recursos creativos, los segmentos de audiencia y los datos de CRM <!-- used how/where? -->; y su estrategia para lograr sus objetivos.

1. (Nuevas cuentas de anunciante) Configurar cuentas administrativas:

   1. Configure la cuenta del anunciante para [!DNL Creative]<!-- and/or DSP? --> y también cree una cuenta en Advertising Search.

      La configuración de la cuenta de [!DNL Creative] se realiza en Advertising DSP DSP, aunque el anunciante no sea un cliente de la cuenta de.

      Del mismo modo, incluso si el anunciante no es un cliente de [!DNL Search], la cuenta de [!DNL Search] se usa para crear etiquetas de seguimiento de conversión y configurar columnas de conversión en [!DNL Creative].

   1. (Si es necesario) Cree cuentas de usuario para que el anunciante vea y administre sus creativos y experiencias publicitarias y genere informes.

1. (Opcional) Si desea crear segmentos de audiencia de origen para incluirlos como destinatarios de sus creativos, cree las etiquetas de cualquiera de las siguientes maneras:

   * [Cree píxeles de retargeting](/help/creative/pixels/retargeting-pixel-manage.md) para redireccionar anuncios a visitantes con atributos específicos a páginas de aterrizaje o de conversión específicas y, a continuación, genere etiquetas para insertarlas en las páginas web relevantes.

   * DSP DSP (Anunciantes con la opción de) En la opción de, [cree segmentos de audiencia personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear a todos los visitantes en páginas de aterrizaje o páginas de conversión específicas y, a continuación, genere etiquetas para insertarlas en las páginas web relevantes.

   Ambos tipos de etiquetas son etiquetas de imagen, que muestran una imagen transparente (píxel) de 1 píxel x 1 píxel, que es invisible para los usuarios finales, en la página web en la que se añaden. Posteriormente, puede configurar elementos creativos en una experiencia de anuncio para que se dirijan a píxeles o segmentos de retargeting específicos, de modo que los elementos de anuncio relevantes se muestren solo a los usuarios que hayan visitado anteriormente páginas de sitio asociadas con el píxel o segmento.

   Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.

   **Nota:** También puede usar audiencias de origen de Adobe Audience Manager y Adobe Analytics como destinos creativos. Una vez que un visitante se califica para una audiencia compartida de [!DNL Analytics], la información se puede procesar en [!DNL Creative] en unas 24-48 horas. <!--Still true? And what about AAM and DSP? -->

1. Configure experiencias publicitarias en función de sus objetivos publicitarios:

   * **Flujo de trabajo de automatización:** El equipo de operaciones de [!DNL Creative] puede crear anuncios dinámicos para su organización mediante plantillas de anuncios y fuentes de datos.

     Para obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **Flujo de trabajo manual:** Configuración manual de experiencias publicitarias:

      1. Configure elementos creativos para utilizarlos en sus experiencias:

         * Para los creativos que [!DNL Creative] alojará, cárguelos.<!-- Add x-ref and reword if necessary to cover all cases -->

         * Para los creativos alojados en un servidor de publicidad de terceros compatible, [apunte a los archivos creativos](/help/creative/creative-libraries/creative-third-party-manage.md).

      1. (Opcional) [Agrupe los creativos en paquetes](/help/creative/creative-libraries/bundle-manage.md) que puede adjuntar a las experiencias en un solo paso.

      1. Los elementos creativos de la secuencia y los destinos de anuncio opcionales como [experiencias de anuncio](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done -->

     Los targets de anuncios pueden incluir píxeles de retargeting que crees en [!DNL Creative]; tus segmentos de audiencia en Adobe Experience Cloud (incluidos los de DSP, los de Audience Manager, los de  o los de [!DNL Analytics]); los targets geográficos o los déclencheur de datos específicos de la página web (como SKU=01234567890123 o Cart=empty).&lt;!— No veo segmentos de audiencia disponibles, y veo destinos de radio (que no funciona) pero no otros destinos geográficos — verifica todos estos. —>

1. Configure el seguimiento de conversión para sus experiencias publicitarias:


Configure el seguimiento de conversiones. Según la implementación, esto puede implicar agregar lo siguiente
etiquetas de seguimiento de conversión a las páginas web del anunciante o la configuración de un
lanzamiento de fuente para los datos de conversión que el anunciante ha recopilado por separado.


Puede generar etiquetas de seguimiento de conversión de Advertising Cloud en Advertising Cloud
Busque o en el Administrador dinámico de etiquetas de Adobe (anteriormente denominado Administrador dinámico de etiquetas).
Nota: Debe utilizar etiquetas de conversión de JavaScript, no de imagen.


Es posible que el departamento de TI del anunciante u otro grupo necesiten programar o recibir información
sobre, la implementación de etiquetas.


(Opcional) En Advertising Cloud Search, realice cada conversión (propiedad de transacción)
está disponible como un conjunto de columnas individual en las vistas de datos y los informes.


Se muestra una conversión (propiedad de transacción) en Advertising Cloud Search después de en
se ha rastreado al menos un evento de conversión.


Si no establece métricas específicas disponibles, se consolidan todas las conversiones
en una columna &quot;Conversiones&quot;.


Valide los datos de los que se realiza un seguimiento.


(Opcional) Configure la entrega de informes programados a direcciones de correo electrónico especificadas.


Para obtener instrucciones, consulte el capítulo de ayuda de &quot;Informes&quot;.


Configure campañas de publicidad en Advertising Cloud DSP DSP u otro servicio de campañas de publicidad, y proporcione a JavaScript.
o etiquetas iframe para las experiencias publicitarias al anunciante, que puede implementarlas como
DSP anuncios de terceros en la.


Monitorice el rendimiento de las experiencias de publicidad completadas, ya sea viendo predefinidas
detalles de rendimiento para experiencias individuales o creación de informes de rendimiento personalizados.


(Según sea necesario) Actualice las experiencias publicitarias en función del rendimiento y la mensajería actualizada.






>[!MORELIKETHIS]
>
>* [Acerca del Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Organización de la interfaz de usuario](/help/creative/introduction/ui.md)
