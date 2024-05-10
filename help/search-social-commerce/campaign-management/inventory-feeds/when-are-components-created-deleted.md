---
title: ¿Cuándo las fuentes de inventario crean o eliminan componentes de cuenta?
description: Descubra qué situaciones crean y eliminan componentes de cuenta al publicar fuentes de inventario.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# ¿Cuándo las fuentes de inventario crean o eliminan componentes de cuenta?

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] solo cuentas*

Cuando se propaga un archivo de fuente de inventario a través de una plantilla, los componentes de cuenta se crean y eliminan de la siguiente manera.

>[!NOTE]
>
>Los anuncios duplicados nunca se crean dentro de un grupo de anuncios.

| Escenario | Ejemplo | Acción |
|----|----|----|
| Los datos de fuente incluyen un nuevo valor para una columna que se utiliza en el nombre de una campaña, el nombre de un grupo de anuncios, una palabra clave o un grupo de productos. | Archivos anteriores:<br>Campaign=Hats<br>Campaign=Gloves<br><br>Nuevo archivo:<br>Campaign=Shoes | Se crea una nueva campaña, grupo de anuncios, palabra clave o grupo de productos si no existe en la red de anuncios. |
| Los datos de la fuente contienen un nuevo valor para una columna que se utiliza en un anuncio. | Archivo anterior: Un anuncio incluido precio=20<br><br>Nuevo archivo: Para el mismo anuncio, precio=10 | Cuando el anuncio se copie para [!DNL Microsoft Advertising] anuncios de texto expandidos, [!DNL Yahoo! Japan ads], o [!DNL Yandex] se cambia el anuncio existente, se elimina y se crea uno nuevo.<br><br>Cuando se cambia la copia de anuncio para otros tipos de anuncio o cuando se utiliza la columna aplicable para un anuncio. [!DNL Google Ads] parámetro de anuncio ({param1} o {param2}) en un anuncio, el anuncio existente se actualiza. |
| La configuración de la plantilla para la campaña, el grupo de anuncios, la palabra clave o el grupo de productos ha cambiado desde la última propagación. | Configuración anterior:Palabra clave=[Palabra clave]<br><br>Nueva configuración: Palabra clave=&lt;color>[Palabra clave] | Se crea una nueva campaña, grupo de anuncios, palabra clave o grupo de productos si no existe en la red de anuncios. |
| La configuración de la plantilla para un anuncio ha cambiado desde la última propagación. | Configuración anterior: Descripción del anuncio=&quot;Buy&quot; [categoría] ahora&quot;.<br><br>Nueva configuración: Descripción del anuncio=&quot;Comprar [marca] ahora&quot;. | Cuando el anuncio se copie para [!DNL Microsoft Advertising] anuncios de texto expandidos, [!DNL Yahoo! Japan ads], o [!DNL Yandex] se cambia el anuncio existente, se elimina y se crea uno nuevo.<br><br>Cuando se cambia la copia de anuncio para otros tipos de anuncio o cuando el cambio refleja un cambio en la columna utilizada para un único anuncio [!DNL Google Ads] parámetro de anuncio ({param1} o {param2}) en un anuncio, el anuncio existente se actualiza. |
| Los nuevos datos de fuente no incluyen una fila para una campaña o grupo de anuncios existente. | n/a | Las campañas y grupos de anuncios existentes permanecen tal cual. |
| Los nuevos datos de fuente no incluyen una fila para un grupo de anuncios, anuncio, palabra clave o grupo de productos existente. | n/a | El grupo de anuncios, el anuncio, la palabra clave o el grupo de productos existentes permanecen tal cual, se pausan o se eliminan, según el [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). |
| Los nuevos datos de fuente de un grupo de productos principal existente no incluyen filas para sus grupos de productos secundarios existentes. | n/a | El grupo de productos principal existente permanece tal cual o se elimina, según el [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). <b>Nota:</b> Si la configuración de los datos de fuente está configurada para poner en pausa los elementos de línea que faltan, el grupo de productos principal se eliminará porque no se pueden poner en pausa los grupos de productos. |
| Los nuevos datos de fuente incluyen una fila para un grupo de anuncios, anuncio, palabra clave o grupo de productos que era a) en datos anteriores, pero b) se omitió desde entonces y se pausó según el [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). | n/a | El grupo de anuncios, el anuncio, la palabra clave o el grupo de productos existentes se reactivan, sin perder ningún historial o puntuación de calidad. |
| Los nuevos datos de fuente incluyen una fila para un grupo de anuncios, anuncio, palabra clave o grupo de productos que era a) en datos anteriores, pero b) se omitió desde entonces y se eliminó según el [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). | n/a | Se crea un nuevo grupo de anuncios, anuncio, palabra clave o grupo de productos. |
| Ha desactivado la opción de nivel de campaña o de grupo de anuncios para &quot;[!UICONTROL Delete negative keywords when omitted from list].&quot; | La lista de palabras clave negativas incluye &quot;cupé&quot; y &quot;coche deportivo&quot;.<br><br>El grupo de anuncios ya incluye la palabra clave negativa &quot;SUV&quot;. | Las palabras clave negativas existentes que no estén en la lista permanecen tal cual. |
| Ha habilitado la opción de nivel de campaña o de grupo de anuncios para &quot;[!UICONTROL Delete negative keywords when omitted from list]Existen las palabras clave &quot;&quot; y negativas que no están en la lista. | La lista de palabras clave negativas incluye &quot;cupé&quot; y &quot;coche deportivo&quot;.<br><br>El grupo de anuncios ya incluye la palabra clave negativa &quot;SUV&quot;. | Cualquier palabra clave negativa no especificada creada previamente con la plantilla se eliminará cuando se propague un archivo de fuente a través de la plantilla. Sin embargo, cualquier palabra clave negativa no especificada creada con otros medios (como en hojas de edición masiva simples, la variable [!UICONTROL Campaigns] , o en el editor de anuncios de la red publicitaria) permanecen tal cual. | | Se produce la fecha de finalización programada de los componentes de un archivo de fuente registrado. | n/a | Las campañas existentes se mantienen tal cual. Los grupos de anuncios, los anuncios y las palabras clave existentes permanecen tal cual, se pausan o se eliminan, según el [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). |
| El nivel de stock de un artículo cae por debajo de un mínimo especificado en la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). | Archivo anterior: stock=10<br><br>Nuevo archivo: stock=0 | Las campañas existentes se mantienen tal cual. Los grupos de anuncios, anuncios, palabras clave y grupos de productos existentes se pausan o eliminan, según el [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). |
| El nivel de stock de un artículo se remonta a un mínimo especificado en la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). | Archivo anterior: stock=0<br><br> Nuevo archivo: stock=10 | Cuando los anuncios, palabras clave o grupos de productos existentes están en pausa, se reactivan, sin perder ningún historial o puntuación de calidad. Cuando no existen anuncios, palabras clave o grupos de productos (por ejemplo, si se eliminaron anteriormente porque el nivel de stock estaba por debajo del mínimo), se crean nuevos anuncios. |

>[!MORELIKETHIS]
>
>* [Automatización de la administración de anuncios mediante fuentes de inventario](inventory-feeds-about.md)
