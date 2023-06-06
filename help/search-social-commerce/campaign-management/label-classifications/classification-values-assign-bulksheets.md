---
title: Asignar valores de clasificación a componentes de cuenta mediante hojas de edición masiva
description: Aprenda a utilizar hojas de edición masiva para asignar valores de clasificación a componentes de cuenta.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 7%

---

# Asignar valores de clasificación a componentes de cuenta mediante hojas de edición masiva

Puede asociar clasificaciones de etiquetas con valores para las siguientes entidades de búsqueda mediante hojas de edición por lotes: campaña, grupo de anuncios, palabra clave, anuncio, ubicación, grupo de productos a nivel de unidad y destino de búsqueda dinámica. Cada clasificación de etiquetas puede tener hasta 2000 valores.

Cada entidad puede tener un valor de etiqueta por clasificación. Por ejemplo, Shoes_Campaign puede tener un valor de Color de &quot;rojo&quot; y un valor Geo de &quot;Los Ángeles&quot;, pero no puede tener varios valores para Color o Geo.

Las entidades secundarias heredan los valores de etiquetas, por lo que no introduzca valores para entidades secundarias a menos que desee anular los valores heredados.

>[!NOTE]
>
>Las palabras clave y la copia de anuncio de algunas redes de anuncios y tipos de campañas son [no mutable](/help/search-social-commerce/campaign-management/faqs-campaigns.md), lo que significa que al editarlos se elimina la entidad existente y se crea una nueva. Cuando se elimina una entidad existente de este modo, la clasificación de etiquetas no se asigna a la nueva entidad.

1. [Descargar una hoja de edición masiva](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) que incluye las entidades a las que desea asignar valores de clasificación de etiquetas:

   * En el [!UICONTROL Rows and Columns] , expanda la pestaña [!UICONTROL Campaign] lista en la [!UICONTROL Bulksheet Columns] panel.

   * Expanda el [!UICONTROL Label Classification] lista.

   * Seleccione cada clasificación para la que desee incluir una columna en el archivo de hoja de edición masiva.

      Por ejemplo, si incluye las clasificaciones de etiquetas &quot;Color&quot; y &quot;Geo&quot;, la hoja de edición masiva incluirá las columnas &quot;Color&quot; y &quot;Geo&quot;.

1. Abra el archivo en un editor y añada valores de etiqueta a las columnas de clasificación de etiquetas de las entidades con las que desea asociarlos. La longitud máxima de cada valor es de 100 caracteres, y puede incluir caracteres ASCII y no ASCII.

   Consulte los valores de ejemplo en la siguiente sección.

   Además de agregar valores, también puede eliminar valores existentes eliminándolos de las filas relevantes. Para eliminar valores tanto de una entidad padre como de sus entidades hijo, a) incluya solo la fila de la entidad padre y elimine el valor de clasificación existente, o b) incluya tanto la entidad padre como sus entidades hijo y elimine el valor de clasificación existente de todas las filas padre y hijo.

1. [Cargue el archivo](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) para crear las asociaciones.

Los valores de etiqueta cargados son visibles en las vistas de entidad relevantes.

## Ejemplo de valores de clasificación de etiquetas para cargar en hojas de edición masiva

Este ejemplo incluye columnas para las clasificaciones de etiquetas &quot;Color&quot; y &quot;Geo&quot;. Para sus propias hojas de edición masiva, sustituya las columnas por sus propios nombres de clasificación de etiquetas.

| Cuenta | Campaign | Grupo de publicidad | Palabra clave | Anuncio | Ubicación | Etiquetas | Color | Geo |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 |  |  |  |  |  | Verde |  |
| Acct1 | C1 | AG1 |  |  |  |  |  |  |
| Acct1 | C1 | AG1 | K1 |  |  |  |  | RU |
| Acct1 | C1 | AG1 | K2 |  |  |  | Rojo | AU |
| Acct1 | C1 | AG1 | K3 |  |  |  | Azul | DE |
| Acct1 | C1 | AG1 |  | A1 |  |  |  |  |
| Acct1 | C1 | AG1 |  | A1 |  |  | Rojo |  |
| Acct1 | C1 | AG1 |  |  | P1 |  | Rojo | AU |
| Acct1 | C1 | AG1 |  |  | P2 |  | Azul | DE |

>[!MORELIKETHIS]
>
>* [Acerca de las clasificaciones de etiquetas](classification-about.md)
>* [Crear una clasificación de etiquetas](classification-create.md)
>* [Asignar valores de clasificación a componentes de cuenta desde las vistas de administración de campañas](classification-values-assign-campaign-management.md)
>* [Quitar valores de clasificación de etiquetas de componentes de cuenta](classification-values-remove.md)
>* [Eliminar valores de clasificación de etiquetas](classification-values-delete.md)
>* [Eliminar clasificaciones de etiquetas](classification-delete.md)

