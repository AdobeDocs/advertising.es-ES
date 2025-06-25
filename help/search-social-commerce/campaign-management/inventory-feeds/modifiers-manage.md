---
title: Administrar modificadores
description: Obtenga información sobre cómo configurar y administrar modificadores para las plantillas de publicidad para las fuentes de datos de inventario.
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Administración de modificadores

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Los modificadores son adjetivos o adverbios que se pueden agregar o quitar de una frase sin cambiar la estructura básica de la oración. Puede crear grupos de modificadores para utilizarlos como variables en varios campos de datos en plantillas de datos de fuentes. Al incluir modificadores en los campos de estructura de cuenta (campaña y grupo de publicidad), palabras clave, direcciones URL base y anuncios, se crea un valor para cada modificador asociado. Por ejemplo, si utiliza una variable de grupo de modificadores en un titular de anuncio y el grupo de modificadores incluye tres modificadores (&quot;barato&quot;, &quot;descuento&quot; y &quot;asequible&quot;), se crean tres anuncios independientes para cada fila de datos de la fuente de datos, uno para cada modificador. Del mismo modo, si se incluye un grupo de modificadores con varios valores en la dirección URL base de un grupo de anuncios, se crea un conjunto de palabras clave para cada una de las direcciones URL base resultantes.

Cada grupo de modificadores puede incluir tantos modificadores como desee. Cada plantilla solo puede utilizar un grupo de modificadores.

## Creación de un grupo de modificadores

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Modifiers]**.

1. Sobre la lista de grupos de modificadores, haga clic en **[!UICONTROL Create]**.

1. Especifique la configuración del grupo de modificadores:

   **[!UICONTROL Name]:** Nombre del grupo de modificadores.

   **[!UICONTROL Modifiers]:** Los valores modificadores del grupo (uno por línea).

1. Haga clic en **[!UICONTROL Save]**.

## Editar un grupo de modificadores

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Modifiers]**.

1. En la lista de grupos de modificadores, pulse en el nombre del grupo de modificadores.

1. Edite la configuración del grupo de modificadores:

   **[!UICONTROL Name]:** Nombre del grupo de modificadores.

   **[!UICONTROL Modifiers]:** Los valores modificadores del grupo (uno por línea).

1. Haga clic en **[!UICONTROL Save]**.

## Eliminar grupos de modificadores

>[!IMPORTANT]
>
>Cuando elimine un grupo de modificadores, quite todas las variables de dicho grupo (indicadas como `<modifier_group_name>`) de los campos de las plantillas existentes. Si intenta propagar datos a través de una plantilla utilizando variables para modificadores que no existen, el trabajo falla1.

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. En la barra de herramientas situada encima de la tabla de datos, haga clic en **[!UICONTROL Modifiers]**.

1. Seleccione la casilla de verificación situada junto a cada grupo de modificadores que desee borrar.

1. Sobre la lista de grupos de modificadores, haga clic en **[!UICONTROL Delete]**.

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Yes]**.

1. (Si es necesario) [Elimine las referencias al modificador](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) de todas las plantillas aplicables.

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de inventario](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Administrar plantillas de anuncios](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
