---
title: Acerca de sus bibliotecas creativas
description: Obtenga información sobre cómo administrar los elementos creativos para sus experiencias publicitarias.
feature: Creative Libraries, Creative Standard Creatives, Creative Dynamic Creatives
exl-id: 77dc6528-a455-4406-98b6-15e7ce529370
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '1059'
ht-degree: 0%

---

# Acerca de sus bibliotecas creativas

*Característica beta cerrada*

Las bibliotecas creativas le permiten administrar los elementos creativos que utilizará en las experiencias publicitarias. Puede crear varias bibliotecas, cada una con un conjunto de elementos creativos y *paquetes creativos*, que son grupos de elementos creativos que puede agregar a una experiencia como una sola unidad.

Las bibliotecas pueden incluir lo siguiente:

* **Creativos individuales:** Puede incluir creativos individuales directamente dentro de las experiencias publicitarias que no tengan objetivos de usuario definidos. También puede usar sus elementos creativos para crear paquetes, que puede incluir en [experiencias publicitarias](/help/creative/experiences/experience-about.md) de destino.

   * **Creativos estándar:** Puede cargar y administrar creativos en [varios formatos](#creative-creative-formats). Para cada elemento creativo, debe especificar el idioma predeterminado para cada anuncio con el que asocia el elemento creativo, la página de aterrizaje predeterminada que se abre cuando un usuario hace clic en un anuncio que incluye el elemento creativo y las etiquetas opcionales que se utilizarán como filtros en varias vistas de [!DNL Creative].

   * **Creativos dinámicos:** (solo clientes existentes de Adobe Advertising DCO) Los usuarios administradores pueden crear creativos generados dinámicamente asignando variables dinámicas en una plantilla de anuncio a los valores de un archivo de fuente. Todos los usuarios pueden obtener una vista previa de los anuncios dinámicos existentes, duplicarlos y eliminarlos.

* **Paquetes creativos:** Agrupe los elementos creativos en paquetes para usarlos en varias experiencias con objetivos de usuario definidos. Puede crear *paquetes estándar* que consten de anuncios estándar y *paquetes dinámicos* que consten de anuncios generados dinámicamente.

## Formatos de Creative compatibles {#creative-creative-formats}

### Formatos para creativos estándar

Puede agregar y administrar los siguientes tipos creativos en los [tamaños creativos admitidos](creative-sizes.md).

>[!IMPORTANT]
>
>Incluso si tiene intención de utilizar HTML5, Flexible HTML5 o creativos de terceros para sus experiencias publicitarias, también debe añadir creativos de imagen para cada tamaño creativo que utilice.
>
>Cada experiencia requiere un creativo de imagen predeterminado para cada tamaño creativo asignado a la experiencia. Los elementos creativos de imagen predeterminados se utilizan cuando un explorador no está habilitado para JavaScript o cuando el servidor de publicidad no puede personalizar el anuncio debido a retrasos.

#### HTML flexible5

Los creativos flexibles de HTML5 son creativos de HTML5 con todas sus imágenes y otros atributos como etiquetas estándar de HTML, que se pueden editar directamente en [!DNL Creative], ya sea en una biblioteca creativa o en una experiencia individual (lo que crea una variación del creativo original). Los creativos flexibles de HTML5 utilizan el estándar del Interactive Advertising Bureau (IAB) Technology Laboratory para un [catálogo de productos](https://flexibleads.iabtechlab.com/), para el cual los tamaños de formato de anuncio son flexibles (en lugar de fijos) y se basan en la relación de aspecto y el intervalo de tamaño del anuncio, y para el cual los anuncios mantienen su resolución en todos los dispositivos y sitios de editores.

Puede<!-- either --> cargar elementos creativos flexibles de HTML5 como archivos ZIP<!-- or use one of the [provided templates](flexible-html5-templates.md) as a starting point -->. Vea las [especificaciones para creativos flexibles de HTML5](html5-creative-specification.md).

<!-- Will flattening the view be possible later?
The card view, by default, includes a card for each base flexible HTML5 creative you've uploaded, with the number of creative variations [Delete old description? : an indicator of how many variations of the creative exist]. You can optionally flatten the card view to include separate cards for each base creative and each derivation. The table view is always flattened.


[Example default card view for a flexible creative with variations]()[]add image]
  
[Example card for a flexible creative with one variation]() [add image]

 -->

Si lo desea, puede cambiar los valores por defecto de los atributos especificados en un creativo flexible de HTML5. Posteriormente, puede especificar valores personalizados para los atributos dentro de una experiencia específica, lo que crea una variación del elemento creativo principal.

#### Creativos de HTML5

Puede cargar archivos creativos de HTML5 simples o estáticos, con todos los atributos e imágenes especificados, como archivos ZIP. No se puede editar ningún atributo ni añadir imágenes; en su lugar, cargue un nuevo archivo ZIP para añadir un nuevo elemento creativo. Vea las [especificaciones para creativos HTML5 simples y estáticos](html5-creative-specification.md).

#### Creativos de imagen

Puede incluir creativos de imagen en formato GIF, JPEG, JPG o PNG. Puede cargar <!--LATER:   images from your Adobe Experience Manager accounts or --> imágenes desde su dispositivo o red.

Cada experiencia publicitaria requiere un creativo de imagen predeterminado para cada tamaño creativo asignado a la experiencia.

#### Creativos de terceros

Introduzca las etiquetas de seguimiento de JavaScript para creativos alojados en servidores de publicidad de terceros. La secuencia de comandos varía según el servidor de publicidad; a continuación se muestra un ejemplo:

```
<SCRIPT language='JavaScript1.1' SRC="https://ad.doubleclick.net/ddm/adj/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"></SCRIPT> <NOSCRIPT> <A HREF="https://ad.doubleclick.net/ddm/jump/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp]?"><IMG SRC="https://ad.doubleclick.net/ddm/ad/A123456.12345GDN.COM/B1234567.123456789;sz=300x250;ord=[timestamp];dc_lat=;dc_rdid=;tag_for_child_directed_treatment=?"BORDER=0 WIDTH=300 HEIGHT=250 ALT="Advertisement"></A></NOSCRIPT>
```

### Formato para anuncios dinámicos

Los usuarios administradores pueden generar de forma dinámica elementos creativos en formato HTML5 estático y HTML5 dinámico asignando variables dinámicas en una plantilla de anuncio a valores de un archivo de fuente. Los elementos creativos dinámicos pueden incluir elementos creativos de las experiencias heredadas de Adobe Advertising Dynamic Creative Optimization (DCO).

## Las vistas [!UICONTROL Creative Libraries]

Consulte &quot;[Personalizar las vistas de datos](/help/creative/introduction/customize-data-views.md)&quot; para obtener más información sobre cómo personalizar cada vista.

### Vista principal de [!UICONTROL Creative Libraries]

La vista principal [!UICONTROL Creative Libraries] muestra todas las bibliotecas creativas. Los datos de cada biblioteca incluyen el número de experiencias a las que se asignan los paquetes de la biblioteca, el número de paquetes, el número de creativos, el número de tamaños creativos, el número de destinos de idioma predeterminados, la fecha de creación y la fecha de la última modificación de cualquier elemento de la biblioteca. El modo de tabla también incluye una columna para el anunciante.

#### Acciones disponibles

* Creación de nuevas bibliotecas

* Para cada biblioteca creativa:

   * Editar el nombre de la biblioteca

   * Abra la biblioteca para ver los creativos y los paquetes asignados a la biblioteca

   * Eliminar la biblioteca

### Las vistas [!UICONTROL Creative Libraries] > [!UICONTROL Creatives]

#### [!UICONTROL Standard Ads]

La ficha [!UICONTROL Standard Ads] muestra todos los elementos creativos estándar que ha creado. Los datos de cada elemento creativo incluyen el tamaño, el tipo y la fecha de creación del elemento creativo. El modo de tabla también incluye columnas para el idioma predeterminado y la página de aterrizaje predeterminada.

##### Acciones disponibles

* [Añadir elementos creativos estándar a una biblioteca](creative-add-standard.md)

* [Edición de un elemento creativo estándar](creative-edit-standard.md)

* [Previsualización de un elemento creativo estándar](creative-preview.md)

* [Añada elementos creativos estándar a paquetes estándar y elimine elementos creativos estándar de un paquete estándar](creative-attach-detach-bundles.md)

* [Duplicar creativos estándar](creative-duplicate.md)

* [Descargar creativos estándar](creative-download.md)

* [Eliminar elementos creativos estándar](creative-delete.md)

<!-- Add in as separate actions?

add or remove labels, regenerate thumbnails for your creatives. When a creative has child creative variations, you can view the variations within the Card view.

-->

#### [!UICONTROL Dynamic Ads]

La pestaña [!UICONTROL Dynamic Ads] muestra todos los elementos creativos dinámicos que se crearon dinámicamente para sus catálogos creativos, excepto los elementos creativos dinámicos que [eliminó manualmente](creative-delete.md) de la pestaña [!UICONTROL Dynamic Ads]. Si [duplicó manualmente](creative-duplicate.md) cualquier elemento creativo dinámico desde la última vez que se procesó un catálogo, entonces la lista de elementos creativos para ese catálogo también incluye los elementos creativos duplicados.

Los datos de cada creativo incluyen el tipo de creativo, el tamaño de creativo, el número de catálogos a los que pertenece el creativo y la fecha de creación. El modo de tabla también incluye columnas para la plantilla a través de la cual se generó el creativo y el recuento de ofertas.

>[!NOTE]
>
>Cada vez que se procesa un catálogo, se actualizan los datos de los elementos creativos dinámicos existentes para ese catálogo.

##### Acciones disponibles

Actualmente, la capacidad de crear y editar elementos creativos dinámicos solo está disponible para el equipo de cuenta de Adobe. Sin embargo, todos los usuarios pueden:

* [Previsualizar elementos creativos dinámicos](creative-preview.md)

* [Agregue creativos dinámicos a paquetes dinámicos y elimine los creativos dinámicos de un paquete dinámico](creative-attach-detach-bundles.md)

* [Creativos dinámicos duplicados](creative-duplicate.md)

* [Eliminar elementos creativos dinámicos](creative-delete.md)

<!-- Later:  Dynamic creatives are generated automatically when you save a catalog, but can regenerate the catalog using the contents of an updated asset file [using the Run Now option]. -->

### La vista [!UICONTROL Creative Libraries] > [!UICONTROL Bundles]

La vista [!UICONTROL Bundles] muestra todos los contenedores de paquete estándar y dinámico. Puede ver los nombres creativos, los tamaños creativos y los idiomas de los creativos incluidos en cada paquete.

#### Acciones disponibles

* Añadir paquetes estándar y dinámicos a una biblioteca

* Enumere y previsualice los creativos en un paquete

* Editar un nombre de paquete

* Añada elementos creativos estándar a paquetes estándar y elimine elementos creativos estándar de un paquete estándar

* Paquetes duplicados

* Eliminar paquetes

>[!MORELIKETHIS]
>
>* [Administrar bibliotecas creativas](/help/creative/creative-libraries/creative-library-manage.md)
>* [Agregar elementos creativos estándar a una biblioteca creativa](creative-add-standard.md)
>* [Administrar paquetes creativos](bundle-manage.md)
>* [Personalizar las vistas de datos](/help/creative/introduction/customize-data-views.md)
