---
title: Requisitos previos para configurar un origen de datos  [!DNL Google Analytics]
description: Obtenga información acerca de los pasos que debe completar antes de configurar una fuente de datos de  [!DNL Google Analytics] .
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Requisitos previos para configurar un origen de datos de [!DNL Google Analytics]

Antes de configurar un origen de datos de [!DNL Google Analytics], debe establecer el parámetro de cadena de consulta &quot;ef_id&quot; de Search, Social y Commerce como clave principal para pasar datos de [!DNL Google Analytics] a Search, Social y Commerce. Configure la clave principal para cada combinación de cuenta y propiedad de [!DNL Google Analytics] para la que desee sincronizar datos. Es posible que otras personas de su organización necesiten completar estas tareas; consulte a continuación para obtener más información.

Si las direcciones URL de la página de aterrizaje para los anuncios o las palabras clave aún no incluyen redirecciones de Search, Social y Commerce, agréguelas primero.

## Requisito previo 1: Implementar un token de Search, Social y Commerce (parámetro de cadena de consulta &quot;ef_id&quot;) en las direcciones URL de la página de aterrizaje para todas las cuentas de publicidad aplicables

En cada clic de búsqueda de pago para las campañas relevantes, se debe generar un `ef_id` único que se debe anexar a la dirección URL de la página de aterrizaje como una cadena de consulta, como `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, donde `&ef_id=abcde:123456789:s` es el símbolo de anexado, la clave `ef_id` y el valor `ef_id`. Para incluir un ef_id, las cuentas y campañas de red de anuncios relevantes deben tener [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; y [!UICONTROL Redirect Type] &quot;[!UICONTROL Token]&quot;.&quot;

Para cuentas y campañas existentes, es probable que el ef_id ya esté implementado.

Si el ef_id no está incluido, pida ayuda a su equipo de cuenta de Adobe.

Una vez cumplidos todos los requisitos previos, `ef_id` se usa como clave principal para pasar datos de [!DNL Google Analytics] a Search, Social y Commerce.

## Requisito previo 2: capture el token de Search, Social y Commerce (parámetro de cadena de consulta &quot;ef_id&quot;) en una dimensión personalizada para cada propiedad [!DNL Google Analytics] relevante

Repita las tareas siguientes para cada combinación de cuenta y propiedad de [!DNL Google Analytics] para la que desee sincronizar datos. Consulte [[!DNL Google Analytics] documentación sobre la creación e implementación de dimensiones personalizadas](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) para obtener ayuda con estas tareas.

1. En [!DNL Google Analytics], cree una dimensión personalizada denominada &quot;`ef_id`&quot;. Establezca el ámbito de la dimensión en [!DNL User] y establezca la dimensión como activa.

   >[!NOTE]
   >
   >Este requisito previo requiere permiso de edición para las propiedades relevantes.

1. Actualice el código de seguimiento [!DNL Google Analytics] para capturar el valor del parámetro de cadena de consulta ef_id cuando esté presente en la dirección URL de la página de aterrizaje y almacenarlo en la dimensión personalizada ef_id.

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
>* [Configurar una [!DNL Google Analytics] vista como fuente de datos](data-source-configure.md)
>* [Editar una [!DNL Google Analytics] fuente de datos](data-source-edit.md)
>* [Pausar la sincronización de un origen de datos](data-source-pause.md)
>* [Volver a autenticar un [!DNL Google Analytics] origen de datos](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] configuración de origen de datos](data-source-settings.md)
>* [Apéndice:  [!DNL Google Analytics] métricas disponibles](data-source-ga-metrics.md)
