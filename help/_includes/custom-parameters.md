---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---
# Campo Parámetros personalizados en la configuración de campañas de GGL y MS, configuración de grupos de publicidad de MS y configuración de anuncios adaptables y multimedia de MS

**[!UICONTROL Custom Parameters]:** (Opcional; aplicable solo a campañas de audiencia para [!DNL Microsoft Advertising]) Pares de nombre y valor para hasta tres parámetros personalizados. La longitud máxima de los nombres es de 16 caracteres alfanuméricos; la longitud máxima de los valores es de 200 caracteres, incluidos los parámetros incrustados.

Puede incluir los nombres de parámetros personalizados en las plantillas de seguimiento de la entidad y sus entidades secundarias. Cuando un usuario hace clic en un anuncio relevante, la red de publicidad reemplaza el nombre del parámetro con el valor de parámetro definido. Por ejemplo, si crea un parámetro de cliente `{_color}=red` y la plantilla de seguimiento incluye `http://tracker.example.com/?color={_color}&u={lpurl}`, &quot;rojo&quot; se inserta en el parámetro de color cuando un usuario hace clic en un anuncio.

Parámetros personalizados en el grupo de anuncios o ([!DNL Microsoft Advertising] solo) los parámetros personalizados de nivel de anuncio anulan los parámetros personalizados de nivel de campaña con el mismo nombre.
