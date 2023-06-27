---
title: Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos
description: Obtenga información acerca de los pasos que debe completar antes de configurar una [!DNL Google Analytics] fuente de datos.
role: User, Admin
exl-id: cbb2ad6d-8494-4fa4-928c-238b25bda3a6
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Requisitos previos para configurar una [!DNL Google Analytics] fuente de datos

Antes de configurar un [!DNL Google Analytics] fuente de datos, debe establecer el parámetro de cadena de consulta de búsqueda, social y comercial &quot;ef_id&quot; como clave principal desde la que pasar datos [!DNL Google Analytics] a Búsqueda, Social y Comercio. Configure la clave principal para cada [!DNL Google Analytics] combinación de cuenta y propiedad para la que desea sincronizar datos. Es posible que otras personas de su organización necesiten completar estas tareas; consulte a continuación para obtener más información.

Si las direcciones URL de la página de aterrizaje para los anuncios o las palabras clave aún no incluyen redirecciones de búsqueda, medios sociales y comercio, agréguelas primero.

## Requisito previo 1: Implementar un token de búsqueda, social y de comercio (parámetro de cadena de consulta &quot;ef_id&quot;) en las direcciones URL de la página de aterrizaje para todas las cuentas de publicidad aplicables

En cada búsqueda de pago, haga clic en para las campañas relevantes, una variable única `ef_id` debe generarse y anexarse a la dirección URL de la página de aterrizaje como una cadena de consulta, como `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, donde `&ef_id=abcde:123456789:s` es el símbolo de adición, `ef_id` clave, y `ef_id` valor. Para incluir un ef_id, las cuentas y campañas de red de publicidad relevantes deben tener el valor [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; y el [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

Para cuentas y campañas existentes, es probable que el ef_id ya esté implementado.

Si el ef_id no está incluido, pida ayuda a su equipo de cuenta de Adobe.

Cuando se hayan completado todos los requisitos previos, la variable `ef_id` se utiliza como clave principal para pasar datos de [!DNL Google Analytics] a Búsqueda, Social y Comercio.

## Requisito previo 2: Capture el token de búsqueda, social y de comercio (parámetro de cadena de consulta &quot;ef_id&quot;) en una dimensión personalizada para cada elemento relevante [!DNL Google Analytics] propiedad

Repita las siguientes tareas para cada uno [!DNL Google Analytics] combinación de cuenta y propiedad para la que desea sincronizar datos. Consulte [[!DNL Google Analytics] documentación sobre la creación e implementación de dimensiones personalizadas](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) para obtener ayuda con estas tareas.

1. Entrada [!DNL Google Analytics], cree una dimensión personalizada denominada &quot;`ef_id`&quot;. Establezca el ámbito de la dimensión en [!DNL User]y establezca la dimensión en activa.

   >[!NOTE]
   >
   >Este requisito previo requiere permiso de edición para las propiedades relevantes.

1. Actualice su [!DNL Google Analytics] código de seguimiento para capturar el valor del parámetro de cadena de consulta ef_id cuando está presente en la dirección URL de la página de aterrizaje y almacenarlo en la dimensión personalizada ef_id.

   >[!NOTE]
   >
   >El ef_id solo debe usarse en direcciones URL de páginas de aterrizaje.

   Por ejemplo, si la dirección URL de la página de aterrizaje es `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, el valor de la dimensión ef_id en [!DNL Google Analytics] es `abcde:123456789:s`.

   >[!NOTE]
   >
   >Este requisito previo debe completarlo un desarrollador cualificado.

>[!MORELIKETHIS]
>
>* [Acerca de la sincronización [!DNL Google Analytics] métricas de conversión](data-source-about.md)
>* [Configurar un [!DNL Google Analytics] ver como fuente de datos](data-source-configure.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [Volver a autenticar un [!DNL Google Analytics] fuente de datos](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configuración de fuente de datos](data-source-settings.md)
>* [Apéndice: disponible [!DNL Google Analytics] métricas](data-source-ga-metrics.md)
