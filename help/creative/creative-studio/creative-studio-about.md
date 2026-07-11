---
title: Acerca de Creative Studio en Advertising Creative
description: Aprenda a utilizar Creative Studio para crear contenido de publicidad asistida por IA en Adobe Advertising Creative.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 811
ht-degree: 0%

---

# Acerca de [!UICONTROL Creative Studio] en [!DNL Advertising Creative]

*característica de Beta*

[!UICONTROL Creative Studio] es un entorno asistido por IA en el que puede generar, cambiar el tamaño y refinar los anuncios en pantalla en múltiples formatos en una sola sesión. Interactúa con la IA a través de una interfaz de chat en lenguaje natural para generar y modificar el contenido del anuncio (no se requiere ningún trabajo de diseño manual para los campos de contenido).

## Información general de Workspace

[!UICONTROL Creative Studio] está organizado en tres fichas:

**[!UICONTROL Creatives]**: punto de partida para la creación de anuncios. Muestra los elementos creativos existentes generados a partir de Creative Studio, organizados en bibliotecas creativas contraíbles. Desde aquí puede generar anuncios en pantalla estándar a partir de plantillas, crear elementos creativos dinámicos a partir de los datos del catálogo y administrar los elementos creativos existentes (editar, generar variaciones de anuncios, previsualizar, duplicar, descargar, eliminar, realizar controles de calidad y revisar los registros de cambios). Consulte &quot;[Administrar anuncios estándar en Creative Studio](creative-studio-manage-standard-ads.md)&quot; y &quot;[Administrar anuncios dinámicos en Creative Studio](creative-studio-manage-dynamic-ads.md)&quot;.

**[!UICONTROL Templates]**: muestra todas las plantillas de anuncios de vídeo y visualización disponibles en su cuenta, con filtros por origen (Todas, Plantillas del sistema, Plantillas de usuario), estado y formato de anuncio. Puede obtener una vista previa, marcar como favorita, etiquetar, descargar y eliminar plantillas, o iniciar una sesión de generación de anuncios directamente desde una plantilla de anuncio en pantalla existente. Consulte &quot;[Administrar plantillas en Creative Studio](creative-studio-manage-templates.md)&quot;.

**[!UICONTROL Assets]**: almacena imágenes, vídeo y archivos de audio utilizados en las plantillas y disponibles para adjuntarlos a los mensajes de chat de IA durante las sesiones de generación de anuncios. Puede buscar, filtrar, cargar, descargar y eliminar recursos. Consulte [Administrar recursos en Creative Studio](creative-studio-manage-assets.md).

## Funcionalidades clave

* **Generación de contenido de IA:** Use **[!UICONTROL Ad Variations Generator]** para generar conceptos y variaciones de anuncios a través de una interfaz de chat en lenguaje natural. El asistente de IA puede generar titulares, subtitulares, CTA, copias de cuerpo y variaciones de imagen de fondo, y puede crear nuevas plantillas de tamaño en la misma sesión. Se pueden activar hasta 10 conceptos por sesión.

* **Compatibilidad con anuncios de vídeo y visualización:** Cree y administre plantillas de anuncios de visualización y plantillas de anuncios de vídeo. Al crear una plantilla, elija **[!UICONTROL Display Ad Template]** o **[!UICONTROL Video Ad Template]** para que coincida con el formato de su campaña.

* **Carga de plantillas de HTML5:** Importe plantillas de anuncios de HTML5 existentes cargándolas como archivos ZIP. El cuadro de diálogo **[!UICONTROL Import Templates]** le permite asignar un nombre de anunciante y plantilla antes de realizar la importación.

* **Compatibilidad con varios tamaños:** Cambiar el tamaño de los anuncios a dimensiones estándar IAB en un solo paso. La API ajusta automáticamente la ubicación y el tamaño del contenido para cada formato, y los controles de lienzo (ampliar/alejar, ajustar a la pantalla, reproducir animaciones) le ayudan a revisar cada tamaño.

* **Salidas alineadas con la marca:** Cuando se aplica el [perfil de marca](/help/creative/brands/brand-manage.md), la IA utiliza los logotipos, las paletas de color, las directrices de voz, los estándares de imagen y las directrices de canal de la marca para mantener el contenido generado dentro de la marca.

* **Acceso a la biblioteca de recursos:** Adjunte imágenes y otros recursos directamente a los mensajes de chat de IA seleccionando en la biblioteca de recursos, para que el contexto visual esté disponible durante la generación de contenido.

* **Integración de fuentes:** Para las campañas de publicidad dinámica, conecte un catálogo de productos o de contenido para generar anuncios a escala y, a continuación, utilice el agente de IA para filtrar, previsualizar y comprobar la calidad de las combinaciones de anuncios generadas por catálogo.

* **Organización de plantillas:** Marque las plantillas como favoritas, aplique etiquetas y filtre por estado, formato u origen para mantener organizada la biblioteca de plantillas.

## Flujos de trabajo de creación de anuncios

| Flujo de trabajo | Cuándo usar |
| --- | --- |
| [Generar anuncios estándar a partir de una plantilla](creative-studio-manage-standard-ads.md) | Seleccione una plantilla de visualización o de vídeo y utilice [!UICONTROL Ad Variations Generator] para crear variaciones de contenido generadas por IA. Es mejor cuando ya existe una plantilla y desea generar contenido asistido por IA. |
| [Administrar elementos creativos dinámicos](creative-studio-manage-dynamic-ads.md) | Conecte un catálogo de productos o de contenido a una plantilla, asigne campos de catálogo a elementos de plantilla y, a continuación, utilice el agente de IA para previsualizar y realizar un control de calidad de todas las combinaciones de anuncios generadas. Ideal para campañas a gran escala basadas en catálogos. |
| Crear una plantilla nueva | Comience desde un lienzo en blanco para crear una plantilla de visualización o vídeo. Es mejor cuando ninguna plantilla existente satisface sus necesidades. |
| Cargar plantillas de HTML5 | Importe una o más plantillas de publicidad de HTML5 empaquetadas como archivos ZIP. Es mejor cuando tiene creativos de HTML5 listos para la producción creados fuera de [!DNL Advertising Creative]. |

## Anuncios estándar y anuncios dinámicos

[!UICONTROL Creative Studio] admite dos modelos de contenido de anuncio que determinan el comportamiento del agente de IA:

**Anuncios estándar**: usted proporciona o genera todo el contenido de la publicidad. El agente de IA puede generar, modificar o reemplazar cualquier campo de contenido (titulares, CTA, imágenes, colores, copia de tono) dentro de las restricciones del diseño de la plantilla. Los anuncios estándar completados se guardan en una biblioteca creativa seleccionando un anunciante y una biblioteca, con una opción para adjuntarlos a paquetes. Los anuncios estándar son mejores para campañas de mensajería personalizadas.

**Anuncios dinámicos**: el contenido está dirigido por un catálogo de productos o de contenido. Un flujo de trabajo guiado de cuatro pasos le guiará a través de la selección de una plantilla, la asignación de campos de catálogo a elementos de plantilla y la configuración del conjunto de anuncios. Después de la configuración, el agente de IA cambia a un control de calidad y una función de vista previa: puede filtrar anuncios por campos de catálogo, marcar problemas de calidad (límites de caracteres, desbordamiento de contenido, imágenes rotas, conformidad) y analizar combinaciones en el catálogo, pero no puede modificar directamente el contenido procedente del catálogo. Para cambiar el contenido de un anuncio dinámico, actualice el catálogo de origen.

>[!MORELIKETHIS]
>
>* [Administrar anuncios estándar en Creative Studio](creative-studio-manage-standard-ads.md)
>* [Administrar elementos creativos dinámicos en Creative Studio](creative-studio-manage-dynamic-ads.md)
>* [Administrar plantillas en Creative Studio](creative-studio-manage-templates.md)
>* [Administrar recursos en Creative Studio](creative-studio-manage-assets.md)
>* [Administrar perfiles de marca en Advertising Creative](/help/creative/brands/brand-manage.md)
