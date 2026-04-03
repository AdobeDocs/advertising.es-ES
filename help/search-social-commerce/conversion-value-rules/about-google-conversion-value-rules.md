---
title: Acerca de  [!DNL Google Ads] reglas de valor de conversión
description: Aprenda a ver y administrar  [!DNL Google Ads] reglas de valor de conversión en Search, Social y Commerce.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Acerca de [!DNL Google Ads] reglas de valor de conversión

Search, Social y Commerce sincronizan automáticamente las [reglas de valor de conversión](https://support.google.com/google-ads/answer/10518330) de sus cuentas de [!DNL Google Ads]. Las reglas de valor de conversión permiten ajustar los valores de los eventos de conversión en función de la información del usuario, incluido el tipo de dispositivo, la ubicación y el segmento de audiencia. Puede utilizar reglas para pujas basadas en valores en campañas de búsqueda, visualización, compras y rendimiento máximo con Google Smart Bidding. Para las campañas con estrategias de oferta Maximizar conversiones y ROAS de Target, los algoritmos [!DNL Google Ads] empezarán a preferir las conversiones con un valor más alto.

Las reglas de valor de conversión a nivel de campaña anulan las reglas a nivel de cuenta. Cuando una conversión cumple varias reglas de valor de conversión, solo se aplica una de las reglas. Normalmente, se aplica la regla más específica, pero consulte la [[!DNL Google Ads] documentación sobre prioridades para los diferentes tipos de condiciones de regla](https://support.google.com/google-ads/answer/10520348).

## La vista y funcionalidad de [!UICONTROL Conversion Value Rules]

Todas las reglas creadas en la interfaz [!DNL Google Ads] se sincronizan en 24 horas y están disponibles en la vista [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules]. Algunas cuentas pueden administrar sus reglas de valor de conversión:

* En las cuentas para las que se realiza un seguimiento de las conversiones en el nivel de cuenta individual o de campaña, puede crear, editar y cambiar el estado de las reglas en los niveles de cuenta y de campaña.

  Las cuentas se pueden vincular a [!DNL Google Ads] cuentas de administrador, pero no pueden usar el seguimiento de conversiones entre cuentas (para el cual se realiza el seguimiento de las conversiones en todas las cuentas de la cuenta de administrador).

* En las cuentas que utilizan el seguimiento de conversión entre cuentas, las reglas de nivel de cuenta y de nivel de campaña se heredan de la cuenta del administrador y son de solo lectura.

## Reglas de valor de conversión con portafolios de Search, Social y Commerce

Cuando la cuenta del anunciante está configurada para cargar los objetivos de Search, Social y Commerce en [!DNL Google Ads], e incluye una campaña que usa una regla de valor de conversión en un portafolio con un objetivo, [!DNL Google Ads] aplica la regla de valor de conversión al valor de conversión original especificado en el objetivo. Como resultado, los datos de conversión de Buscar, Social y Commerce difieren de los datos de conversión de [!DNL Google Ads].

Por ejemplo, supongamos que el objetivo utiliza una única métrica de conversión &quot;Posibles clientes&quot; y proporciona a las conversiones desde dispositivos móviles un peso de 10 y a las conversiones desde dispositivos no móviles un peso de 10. Buscar, Social y Commerce cuenta un evento de cualquier tipo de dispositivo como una (1) conversión y acredita el valor de conversión como 10. Sin embargo, supongamos que una campaña de ese portafolio utiliza la regla de valor de conversión &quot;Si el dispositivo es móvil, multiplique por 2&quot;. Cuando se rastrea un evento de posibles clientes móvil para esa campaña, [!DNL Google Ads] también acredita el recuento de conversión como uno (1), pero el valor de conversión como (10 x 2) = 20.

Para obtener más información acerca de las reglas, incluidos los valores de conversión originales antes de que se aplicaran las reglas, vea el informe [reglas de valor de conversión en [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

>[!MORELIKETHIS]
>
>* [Crear una [!DNL Google Ads] regla de valor de conversión](create-google-conversion-value-rule.md)
>* [Editar una [!DNL Google Ads] regla de valor de conversión](edit-google-conversion-value-rule.md)
>* [Cambiar el estado de una [!DNL Google Ads] regla de valor de conversión](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] configuración de regla de valor de conversión](google-conversion-value-rule-settings.md)

