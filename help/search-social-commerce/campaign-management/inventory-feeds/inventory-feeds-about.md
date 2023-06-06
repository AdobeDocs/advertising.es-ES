---
title: Automatización de la administración de anuncios mediante fuentes de inventario
description: Obtenga información acerca de la administración avanzada de campañas, que le permite administrar automáticamente la estructura de cuentas y enviar anuncios dinámicos basados en los datos sobre el inventario de productos o servicios.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Automatización de la administración de anuncios mediante fuentes de inventario

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

El [!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] la vista para administración avanzada de campañas le permite crear y actualizar automáticamente la estructura de cuentas de red de publicidad y publicar anuncios dinámicos basados en los datos de su inventario de productos o servicios. Puede cargar nuevos archivos con datos de productos diariamente o con la frecuencia que desee, o vincular directamente a un [!DNL Google] o [!DNL Microsoft®] cuenta del centro de comerciantes. Utilice esta función para lo siguiente:

* Cree nuevas campañas a partir de fuentes de datos ordenadas.

* Actualizar dinámicamente el texto y los anuncios de búsqueda adaptables, [!DNL Google Ads] anuncios de compra, o [!DNL Microsoft® Advertising] anuncios de compra cada vez que se procesan nuevos datos, utilizando variables dinámicas para elementos de datos modificables (como el precio o la cantidad). Cada vez que cambia los datos, se eliminan los anuncios existentes y se crean nuevos.

* Ponga en pausa o elimine automáticamente los grupos de anuncios, las palabras clave y los anuncios cuando el stock caiga por debajo de un nivel específico, según una fecha de finalización especificada o cuando se omita un componente existente de los datos de fuente.

Para configurar los anuncios, cree plantillas de fuentes de inventario que contengan variables (marcadores de posición) y, a continuación, sustituya las variables por columnas de datos reales de un archivo cargado o un [Cuenta de Google o Microsoft® merchant center sincronizada](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Las variables también pueden incluir grupos de modificadores configurados en un archivo o filas individuales del archivo para crear varios anuncios, palabras clave, campañas o grupos de anuncios para cada fila aplicable del archivo de datos. Por ejemplo, si utiliza una variable de grupo de modificadores en un titular de anuncio y el grupo de modificadores incluye dos modificadores (&quot;barato&quot; y &quot;con descuento&quot;), se crean dos anuncios independientes para cada producto, uno para cada modificador. Para [!DNL Google Ads] y [!DNL Microsoft® Advertising] anuncios dinámicos de búsqueda, también puede incluir valores para personalizadores de anuncios.

| [!UICONTROL Ad Variation] Sección de plantilla | Modificadores en Search, Social y Commerce | Contenido de fuente | Anuncios resultantes |
|----|----|----|----|
| Título: Comprar \{ de gama alta<i>Categoría de productos</i>\} &lt;<i>CheapList</i>>.<br><br>Descripción 1: Enorme inventario de \{<i>Nombre del producto</i>\}.<br><br>Descripción 2: Disponible en \{<i>Porcentaje de descuento</i>\}% de descuento. | Valores del grupo de modificadores &quot;CheapList&quot;:<br><br>&quot;por poco dinero&quot;<br><br>&quot;con descuento&quot; | Categoría de producto, Nombre de producto, Porcentaje de descuento<br>electrónica,iPods,10<br><br>ropa,Camisas,15<br><br><b>Nota:</b> Puede separar los valores mediante comas o tabulaciones. | <u>Comprar productos electrónicos de alta gama a buen precio.</u><br>Gran inventario de tabletas. Disponible con un 10% de descuento.<br><br><u>Compre productos electrónicos de alta gama con descuento.</u><br>Gran inventario de tabletas. Disponible con un 10% de descuento.<br><br><u>Compra ropa de alta gama a buen precio.</u><br>Gran inventario de camisas. Disponible con un 15% de descuento.<br><br><u>Compra ropa de alta gama con descuento.</u><br>Gran inventario de camisas. Disponible con un 15% de descuento. |

Una vez generados los anuncios, puede revisarlos opcionalmente y luego publicarlos en la red de anuncios.

>[!NOTE]
>Para crear o editar datos de campaña de forma masiva mediante archivos de hoja de cálculo, consulte &quot;[Administración de datos de campaña mediante hojas de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot;

>[!MORELIKETHIS]
>
>* [Flujo de trabajo para administrar datos de campaña mediante fuentes de inventario](inventory-feeds-workflow.md)
>* [¿Cuándo las fuentes de inventario crean o eliminan componentes de cuenta?](when-are-components-created-deleted.md)

