---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---
# Plantilla de anuncio de texto: método de asignación de grupo de anuncios

**[!UICONTROL Map Method]:** (Cuándo [!UICONTROL Map Only] está habilitado para grupos de anuncios; todas las redes de anuncios excepto [!DNL Yandex]) Método mediante el cual se asignan las nuevas palabras clave y los anuncios a los grupos de anuncios existentes:

* *[!UICONTROL Contains Anywhere]:* Agrega datos a un grupo de anuncios existente cuyo nombre incluye la cadena especificada, si existe.

* *[!UICONTROL Contains Exactly]:* Agrega datos a un grupo de anuncios existente cuyo nombre incluye la cadena especificada, si existe.

* *[!UICONTROL Exactly Matches]* (predeterminado): Agrega datos a un grupo de anuncios existente con el mismo nombre, si existe.

Cuando no se encuentra ninguna coincidencia, se omiten todos los datos del grupo de anuncios. Si los datos del grupo de anuncios en la fuente no incluyen datos de campaña, el grupo de anuncios se asigna a un grupo de anuncios con el mismo nombre en cualquier campaña, si existe. Si se encuentran varias coincidencias de grupos de anuncios, las palabras clave y los anuncios se asignan a todos.
