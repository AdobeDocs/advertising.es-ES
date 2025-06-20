---
title: Información general sobre la implementación de Adobe Advertising Creative
description: Obtenga información acerca del flujo de trabajo básico para implementar  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Información general sobre la implementación de Adobe Advertising Creative

*Beta cerrada*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

El equipo de operaciones de [!DNL Creative] trabaja con cada anunciante para configurar sus experiencias creativas y creativas, ya sea implementando las experiencias publicitarias como anuncios dentro de su DSP o proporcionando a su equipo las etiquetas de anuncios de terceros para que las implemente por sí mismo, y validando los datos iniciales de costo, clics y conversión.

De forma continua, el equipo de cuenta de Adobe, el equipo de la agencia o el anunciante (según los términos de la service level agreement) deben monitorizar cada experiencia y editarla según sea necesario para cumplir los objetivos del anunciante.

## Tareas de configuración iniciales para [!DNL Creative] experiencias

El equipo de implementación o su agencia trabajarán con usted para lo siguiente:

1. Defina sus objetivos de personalización (por ejemplo, si personalizará los anuncios para prospección o retargeting); todos los datos de origen, segundo y tercero disponibles, incluidos los activos creativos y los segmentos de audiencia; y su estrategia para lograr sus objetivos.<!-- and CRM data? used how/where? -->

1. (Nuevas cuentas de anunciante) Configurar cuentas administrativas:

   1. Configure la cuenta del anunciante para [!DNL Creative] y también cree una cuenta en Advertising Search, Social y Commerce.

      La configuración de la cuenta de [!DNL Creative] se realiza en Advertising DSP, incluso si el anunciante no utiliza el resto de DSP.

      Del mismo modo, incluso si el anunciante no es un cliente de [!DNL Search, Social, & Commerce], la cuenta de [!DNL Search, Social, & Commerce] se usa para crear etiquetas de seguimiento de conversión y configurar columnas de conversión en [!DNL Creative].

   1. (Si es necesario) Cree cuentas de usuario para que el anunciante vea y administre sus creativos y experiencias publicitarias y genere informes.

1. (Opcional) Si desea crear segmentos de audiencia de origen para incluirlos como destinatarios de sus creativos, cree las etiquetas de cualquiera de las siguientes maneras:

   * [Cree píxeles de retargeting](/help/creative/pixels/retargeting-pixel-manage.md) para redireccionar anuncios a visitantes con atributos específicos a páginas de aterrizaje o de conversión específicas y, a continuación, genere etiquetas para insertarlas en las páginas web relevantes.

   * (Anunciantes con DSP) En DSP, [cree segmentos de audiencia personalizados](/help/dsp/audiences/custom-segment-create.md) para rastrear a todos los visitantes en páginas de aterrizaje o páginas de conversión específicas y, a continuación, genere etiquetas para insertarlas en las páginas web relevantes.

   Ambos tipos de etiquetas son etiquetas de imagen, que muestran una imagen transparente (píxel) de 1 píxel x 1 píxel, que es invisible para los usuarios finales, en la página web en la que se añaden. Posteriormente, puede configurar elementos creativos en una experiencia de anuncio para que se dirijan a píxeles o segmentos de retargeting específicos, de modo que los elementos de anuncio relevantes se muestren solo a los usuarios que hayan visitado anteriormente páginas de sitio asociadas con el píxel o segmento.

   Es posible que el departamento de TI del anunciante u otro grupo tengan que programar la implementación de etiquetas o recibir información al respecto.

   **Nota:** También puede usar audiencias de origen de Adobe Audience Manager y Adobe Analytics como destinos creativos. Una vez que un visitante se califica para una audiencia compartida de [!DNL Analytics], la información se puede procesar en [!DNL Creative] en unas 24-48 horas. <!--Are times still true? -->

1. Configure la jerarquía de campañas dentro de los DSP en los que implementará las experiencias publicitarias. Use objetivos compatibles con los objetivos de las experiencias publicitarias que implementará en las campañas.

   El comportamiento de direccionamiento jerárquico puede variar según DSP. Advertising DSP aplica una segmentación a nivel de anuncio sobre la segmentación a nivel de ubicación (no en su lugar). Por ejemplo, si una ubicación se dirige a usuarios de Australia y un anuncio a usuarios de Japón, el anuncio se dirigirá a la rama &quot;Todos los demás&quot; para la experiencia. Asegúrese de pensar en toda la estructura de la campaña.

1. Configure experiencias publicitarias en función de sus objetivos publicitarios:

   * **Flujo de trabajo de automatización:** El equipo de operaciones de [!DNL Creative] puede crear anuncios dinámicos para su organización mediante plantillas de anuncios y fuentes de datos.

     Para obtener más información, póngase en contacto con el equipo de cuenta de Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **Flujo de trabajo manual:** Configuración manual de experiencias publicitarias:

      1. [Configure elementos creativos estándar para usarlos en sus experiencias](/help/creative/creative-libraries/creative-add-standard.md):

         * Para los creativos que [!DNL Creative] alojará, cárguelos. Esto puede incluir recursos de imagen en una cuenta de Adobe Experience Manager.

         * Para los creativos alojados en un servidor de publicidad de terceros admitido, apunte a los archivos creativos.

      1. (Opcional) [Agrupe los creativos en paquetes](/help/creative/creative-libraries/bundle-manage.md) que puede adjuntar a las experiencias segmentadas en un solo paso.

      1. Configurar [experiencias publicitarias](/help/creative/experiences/experience-about.md):

         * Para [experiencias de anuncios segmentadas](/help/creative/experiences/experience-create-targeting.md), los elementos creativos de secuencia y los destinos de anuncios opcionales.

           Los targets de anuncios pueden incluir píxeles de retargeting que crees en [!DNL Creative]; tus segmentos de audiencia en Adobe Experience Cloud (incluidos DSP, Audience Manager o [!DNL Analytics]); tus targets geográficos o déclencheur de datos específicos en la página web (como SKU=01234567890123 o Cart=empty).

         * Para [experiencias de publicidad sin objetivo](/help/creative/experiences/experience-create-no-targeting.md), cree una configuración de experiencia general.

           Los targets de anuncios pueden incluir píxeles de retargeting que crees en [!DNL Creative]; tus segmentos de audiencia en Adobe Experience Cloud (incluidos DSP, Audience Manager o [!DNL Analytics]); tus targets geográficos o déclencheur de datos específicos en la página web (como SKU=01234567890123 o Cart=empty).













1. Configure el seguimiento de conversión para sus experiencias publicitarias:


Configure el seguimiento de conversiones. Según la implementación, esto puede implicar agregar lo siguiente
etiquetas de seguimiento de conversión a las páginas web del anunciante o la configuración de un
lanzamiento de fuente para los datos de conversión que el anunciante ha recopilado por separado.


Puede generar etiquetas de seguimiento de conversión de Adobe Advertising en Advertising Search, Social y Commerce, o en el Administrador dinámico de etiquetas de Adobe (anteriormente denominado Administrador dinámico de etiquetas).
Nota: Debe utilizar etiquetas de conversión de JavaScript, no de imagen.


Es posible que el departamento de TI del anunciante u otro grupo necesiten programar o recibir información
sobre, la implementación de etiquetas.


(Opcional) En Buscar, Social y Commerce, realice cada conversión (propiedad de transacción)
está disponible como un conjunto de columnas individual en las vistas de datos y los informes.


Una conversión (propiedad de transacción) aparece en Buscar, Social y Commerce después de en
se ha rastreado al menos un evento de conversión.


Si no establece métricas específicas disponibles, se consolidan todas las conversiones
en una columna &quot;Conversiones&quot;.


Valide los datos de los que se realiza un seguimiento.


(Opcional) Configure la entrega de informes programados a direcciones de correo electrónico especificadas.


Para obtener instrucciones, consulte el capítulo de ayuda de &quot;Informes&quot;.


Configure campañas de publicidad en Advertising DSP u otro DSP y proporcione JavaScript
o etiquetas iframe para las experiencias publicitarias al anunciante, que puede implementarlas como
anuncios de terceros en DSP.


Monitorice el rendimiento de las experiencias de publicidad completadas, ya sea viendo predefinidas
detalles de rendimiento para experiencias individuales o creación de informes de rendimiento personalizados.


(Según sea necesario) Actualice las experiencias publicitarias en función del rendimiento y la mensajería actualizada.






>[!MORELIKETHIS]
>
>* [Acerca de Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Organización de la interfaz de usuario](/help/creative/introduction/ui.md)
