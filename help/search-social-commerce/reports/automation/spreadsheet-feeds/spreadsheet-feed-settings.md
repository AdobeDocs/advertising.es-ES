---
title: Configuración de fuente de informe de hoja de cálculo
description: Obtenga información acerca de la configuración de las fuentes de hoja de cálculo.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Configuración de fuente de informe de hoja de cálculo

| Campo | Descripción |
|---|---|
| [!UICONTROL Feed Name] | Nombre de la fuente de la hoja de cálculo. |
| [!UICONTROL Report Template] | La plantilla de informe que especifica los datos de informe requeridos; seleccione la que utilizó para crear la plantilla [!DNL Excel]. Se muestran todas las plantillas de informe básicas.<br><br><b>Nota:</b> Si cambia la plantilla de informe utilizada para el informe o actualiza las columnas de la plantilla, debe crear y cargar una nueva plantilla [!DNL Excel]. |
| [!UICONTROL Excel Template] | La plantilla [!DNL Excel] con formato especial que creó en formato .XLSX, que se aplica a los datos especificados en la plantilla de informe. Especifique el archivo que desea cargar; para ello, especifique la ruta de acceso completa y el nombre del archivo, o bien haga clic en <b>[!UICONTROL Browse]</b> para ubicarlo en su dispositivo o red. |
| [!UICONTROL Back Fill From] | La fecha inicial en la que se actualizaron los datos existentes en la ficha [!UICONTROL RAW], representada por un número de días pasados. Escriba un valor de hasta 90 días; el valor predeterminado es de siete (7) días.<br><br>Por ejemplo, si el valor es 7 y hoy es 7 de marzo, los datos existentes en la ficha [!UICONTROL RAW] que comienzan por 1 de marzo se actualizarán (hasta la fecha de finalización especificada por el parámetro [!UICONTROL Back Fill Until]). Las filas de datos existentes para fechas anteriores al 1 de marzo no se eliminan, pero no se actualizan. |
| [!UICONTROL Back Fill Until] | La fecha de finalización en la que se actualizaron los datos existentes en la ficha [!UICONTROL RAW], representada por un número de días pasados. El valor predeterminado es un (1) día.<br><br>Por ejemplo, si este valor es 1 y hoy es 7 de marzo, los datos existentes en la ficha [!UICONTROL RAW] se actualizarán hasta el 6 de marzo (y a partir de la fecha de inicio especificada por el parámetro [!UICONTROL Back Fill From]). Si este valor es 1, el parámetro [!UICONTROL Back Fill Until] es 7 y hoy es 7 de marzo, los datos existentes en la ficha [!UICONTROL RAW] se actualizarán del 1 al 6 de marzo. En ambos ejemplos, las filas de datos existentes para las fechas posteriores al 6 de marzo no se eliminan, pero no se actualizan. |
| [!UICONTROL Email Recipients] | Direcciones de correo electrónico a las que se envían notificaciones cada vez que se actualiza el informe o cada vez que se ejecuta el informe cuando la plantilla incluye una programación. De forma predeterminada, se introduce la dirección de la cuenta de usuario. Para especificar varias direcciones, sepárelas con comas, espacios o líneas nuevas. |
| [!UICONTROL Schedule Time] | La hora a la que se actualizan las fuentes de hoja de cálculo: a las 08:00 o a cualquier hora entre las 10:00 y las 23:00 en el huso horario del anunciante. El valor predeterminado para las nuevas fuentes de hoja de cálculo es 10:00.<br><br><b>Nota:</b> Por motivos de rendimiento, no se pueden actualizar las fuentes de hojas de cálculo a las 09:00, cuando se generan otros informes. |
| [!UICONTROL Email Notification] | (Cuando se especifican destinatarios del correo electrónico) Qué se debe incluir en las notificaciones por correo electrónico a cualquier dirección especificada:<ul><li><i>Adjuntar fuente</i> — Para enviar una copia del informe completado en formato XLSX. Si el archivo tiene más de 10 MB, la notificación no incluye ningún archivo adjunto.</li><li><i>Solo notificación</i> (el valor predeterminado): para enviar solamente una notificación de la finalización o el error del informe, con un vínculo al informe.</li></ul> |

>[!MORELIKETHIS]
>
>* [Acerca de las fuentes de informes de hoja de cálculo](spreadsheet-feed-about.md)
>* [Crear una fuente de informes de hoja de cálculo](spreadsheet-feed-create.md)
>* [Crear una [!DNL Excel] plantilla para una fuente de informes de hoja de cálculo](spreadsheet-feed-create-excel-template.md)
>* [Editar la configuración de fuentes de informes de hoja de cálculo](spreadsheet-feed-edit.md)
>* [Ver o guardar un archivo de fuente de informes de hoja de cálculo](spreadsheet-feed-view-or-save.md)
>* [Actualizar manualmente las fuentes de informes de hoja de cálculo](spreadsheet-feed-refresh.md)
>* [Eliminar fuentes de informes de hoja de cálculo](spreadsheet-feed-delete.md)
