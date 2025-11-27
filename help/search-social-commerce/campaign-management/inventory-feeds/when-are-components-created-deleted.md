---
title: ¿Cuándo las fuentes de inventario crean o eliminan componentes de cuenta?
description: Descubra qué situaciones crean y eliminan componentes de cuenta al publicar fuentes de inventario.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# ¿Cuándo las fuentes de inventario crean o eliminan componentes de cuenta?

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (solo acciones de eliminación) y [!DNL Yandex] cuentas solamente*

Cuando se propaga un archivo de fuente de inventario a través de una plantilla, los componentes de cuenta se crean y eliminan de la siguiente manera.

>[!NOTE]
>
>Los anuncios duplicados nunca se crean dentro de un grupo de anuncios.

| Escenario | Ejemplo | Acción |
|----|----|----|
| Los datos de fuente incluyen un nuevo valor para una columna que se utiliza en el nombre de una campaña, el nombre de un grupo de anuncios, una palabra clave o un grupo de productos. | Archivos anteriores:<br>Campaign=Hats<br>Campaign=Gloves<br><br>Nuevo archivo:<br>Campaign=Shoes | Se crea una nueva campaña, grupo de anuncios, palabra clave o grupo de productos si no existe en la red de anuncios. |
| Los datos de la fuente contienen un nuevo valor para una columna que se utiliza en un anuncio. | Archivo anterior: Un anuncio incluido price=20<br><br>Nuevo archivo: Para el mismo anuncio, price=10 | Cuando se cambia la copia de anuncio de [!DNL Microsoft Advertising] anuncios de texto expandidos, [!DNL Yahoo! Japan ads] o [!DNL Yandex], se elimina el anuncio existente y se crea uno nuevo.<br><br>Cuando se cambia la copia de anuncio para otros tipos de anuncio o cuando se usa la columna aplicable para un parámetro de anuncio de [!DNL Google Ads] ({param1} o {param2}) en un anuncio, se actualiza el anuncio existente. |
| La configuración de la plantilla para la campaña, el grupo de anuncios, la palabra clave o el grupo de productos ha cambiado desde la última propagación. | Configuración anterior:Keyword=[Palabra clave]<br><br>Nueva configuración: Palabra clave=&lt;Color>[Palabra clave] | Se crea una nueva campaña, grupo de anuncios, palabra clave o grupo de productos si no existe en la red de anuncios. |
| La configuración de la plantilla para un anuncio ha cambiado desde la última propagación. | Configuración anterior: Descripción del anuncio=&quot;Comprar [categoría] ahora&quot;.<br><br>Nueva configuración: Descripción del anuncio=&quot;Comprar [marca] ahora&quot;. | Cuando se cambia la copia de anuncio de [!DNL Microsoft Advertising] anuncios de texto expandidos, [!DNL Yahoo! Japan ads] o [!DNL Yandex], se elimina el anuncio existente y se crea uno nuevo.<br><br>Cuando se cambia la copia de anuncio para otros tipos de anuncio o cuando el cambio refleja un cambio en la columna utilizada para un único parámetro de anuncio de [!DNL Google Ads] ({param1} o {param2}) en un anuncio, se actualiza el anuncio existente. |
| Los nuevos datos de fuente no incluyen una fila para una campaña o grupo de anuncios existente. | n/a | Las campañas y grupos de anuncios existentes permanecen tal cual. |
| Los nuevos datos de fuente no incluyen una fila para un grupo de anuncios, anuncio, palabra clave o grupo de productos existente. | n/a | El grupo de anuncios, el anuncio, la palabra clave o el grupo de productos existentes permanecen tal cual, se pausan o se eliminan, según la [configuración de datos de fuentes](feed-settings-manage.md#feed-data-settings). |
| Los nuevos datos de fuente de un grupo de productos principal existente no incluyen filas para sus grupos de productos secundarios existentes. | n/a | El grupo de productos principal existente permanece tal cual o se elimina, según la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). <b>Nota:</b> Si la configuración de los datos de fuente está configurada para poner en pausa los elementos de línea que faltan, el grupo de productos principal se eliminará porque no se pueden poner en pausa los grupos de productos. |
| Los nuevos datos de fuente incluyen una fila para un grupo de anuncios, anuncio, palabra clave o grupo de productos que era a) en datos anteriores, pero b) se omitió desde entonces y se pausó según la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). | n/a | El grupo de anuncios, el anuncio, la palabra clave o el grupo de productos existentes se reactivan, sin perder ningún historial o puntuación de calidad. |
| Los nuevos datos de fuente incluyen una fila para un grupo de anuncios, anuncio, palabra clave o grupo de productos que era a) en datos anteriores, pero b) se omitió desde entonces y se eliminó según la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). | n/a | Se crea un nuevo grupo de anuncios, anuncio, palabra clave o grupo de productos. |
| Ha deshabilitado la opción de nivel de campaña o de grupo de anuncios para &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot;. | La lista de palabras clave negativas incluye &quot;cupé&quot; y &quot;coche deportivo&quot;.<br><br>El grupo de anuncios ya incluye la palabra clave negativa &quot;SUV&quot;. | Las palabras clave negativas existentes que no estén en la lista permanecen tal cual. |
| Ha habilitado la opción de nivel de campaña o de grupo de anuncios en &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot;, y existen palabras clave negativas que no están en la lista. | La lista de palabras clave negativas incluye &quot;cupé&quot; y &quot;coche deportivo&quot;.<br><br>El grupo de anuncios ya incluye la palabra clave negativa &quot;SUV&quot;. | Cualquier palabra clave negativa no especificada creada previamente con la plantilla se eliminará cuando se propague un archivo de fuente a través de la plantilla. Sin embargo, cualquier palabra clave negativa no especificada creada con otros medios (como en hojas de edición masiva simples, las vistas [!UICONTROL Campaigns] o en el editor de anuncios de la red de anuncios) permanece tal cual. |
| Se produce la fecha de finalización programada de los componentes de un archivo de fuente registrado. | n/a | Las campañas existentes se mantienen tal cual. Los grupos de anuncios, los anuncios y las palabras clave existentes permanecen tal cual, se pausan o se eliminan, según la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). |
| El nivel de stock de un elemento cae por debajo del mínimo especificado en la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). | Archivo anterior: stock=10<br><br>Nuevo archivo: stock=0 | Las campañas existentes se mantienen tal cual. Los grupos de anuncios, anuncios, palabras clave y grupos de productos existentes se pausarán o eliminarán, según la [configuración de datos de fuente](feed-settings-manage.md#feed-data-settings). |
| El nivel de existencias de un elemento se remonta a un mínimo especificado en la [configuración de datos de fuentes](feed-settings-manage.md#feed-data-settings). | Archivo anterior: stock=0<br><br> Nuevo archivo: stock=10 | Cuando los anuncios, palabras clave o grupos de productos existentes están en pausa, se reactivan, sin perder ningún historial o puntuación de calidad. Cuando no existen anuncios, palabras clave o grupos de productos (por ejemplo, si se eliminaron anteriormente porque el nivel de stock estaba por debajo del mínimo), se crean nuevos anuncios. |

>[!MORELIKETHIS]
>
>* [Acerca de la automatización de la administración de anuncios mediante fuentes de inventario](inventory-feeds-about.md)
