---
title: Crear una meta personalizada
description: Crear una meta personalizada
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Crear una meta personalizada

Puede crear objetivos personalizados como *objetivos* dentro [!DNL Advertising Search, Social, & Commerce].

DSP Para crear un objetivo personalizado, la cuenta de la debe estar vinculada a un [!DNL Search, Social, & Commerce] cuenta con el mismo ID de organización de Adobe Experience Cloud, desde el [!DNL Search, Social, & Commerce] configuración de cliente. DSP Si la cuenta de la cuenta de la cuenta no está vinculada a un [!DNL Search, Social, & Commerce] cuenta, póngase en contacto con el equipo de cuenta de Adobe.

>[!TIP]
>
>Consulte la [prácticas recomendadas para crear objetivos personalizados](custom-goal-best-practices.md) para obtener sugerencias sobre cómo configurar los objetivos personalizados.

1. Iniciar sesión en [!DNL Advertising Search, Social, & Commerce] at (usuarios de Norteamérica) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) o (todos los demás usuarios) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Asegúrese de que se ha realizado el seguimiento de las métricas que desea incluir en el objetivo, que están disponibles en el producto e incluyen un nombre para mostrar:
   1. En el menú principal, haga clic en **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. Busque la métrica y asegúrese de que **[!UICONTROL Show in UI and Reports]** está habilitado para la métrica.
   1. Si la métrica no tiene un valor en **[!UICONTROL Display Name]** , haga clic en la celda, escriba el nombre para mostrar y haga clic en **[!UICONTROL Apply].**
1. Crear el objetivo personalizado como *objetivo*:
   1. En el menú principal, haga clic en **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. En la barra de herramientas, haga clic en **[!UICONTROL Create objective].**
   1. Introduzca la configuración del objetivo:
      1. En el **[!UICONTROL Change Objective Name]** , introduzca el nombre del objetivo.

         El nombre del objetivo se mostrará en la variable [!UICONTROL Custom Goals] DSP en la configuración del paquete de.

      1. Asocie propiedades al objetivo:

         >[!NOTE]
         >
         > Todas las métricas de conversión rastreadas para el anunciante se enumeran de forma predeterminada en la variable [!UICONTROL Available Properties] lista.

         * Para importar un archivo CSV con métricas de conversión y sus ponderaciones, haga clic en **[!UICONTROL Import]** y busque el archivo que desea importar.

           Las métricas de conversión importadas ya deben existir para el anunciante; los nombres no distinguen entre mayúsculas y minúsculas.

           Las métricas de conversión importadas reemplazan cualquier propiedad existente especificada.

         * Para especificar manualmente la primera métrica de conversión con la ponderación predeterminada (1), seleccione una de las métricas de conversión rastreadas para el anunciante.

         * Para agregar manualmente otra métrica de conversión con la ponderación predeterminada (1), haga clic en **[!UICONTROL +]** .

           >[!TIP]
           >
           > Para buscar una métrica en la lista, introduzca una cadena desde cualquier lugar dentro del nombre de la métrica.

         * Para agregar manualmente varias métricas de conversión, haga clic en **[!UICONTROL Add Multiple Properties].** Para cada métrica de conversión que desee agregar, haga clic en el nombre de la métrica en la [!UICONTROL Available Properties] y arrástrela a la columna [!UICONTROL Added Properties] columna. Cuando termine de agregar métricas, haga clic en **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* Para buscar una métrica en la lista, introduzca una cadena desde cualquier lugar dentro del nombre de la métrica en el campo de entrada.
           >* Para filtrar la lista y excluir las métricas que se excluyen en los informes, seleccione la opción **[!UICONTROL Hide properties excluded from reports].**

         * (Cuando el objetivo contenga varias métricas de conversión) Para cambiar el peso de una métrica en relación con las demás métricas del objetivo, introduzca valores en la variable **[!UICONTROL Weight]** campo(s).

      1. Al final de la configuración, haga clic en **[!UICONTROL Save]**.

DSP Una vez creado un objetivo, puede asignarlo a un paquete de como un objetivo personalizado cuando el objetivo de optimización sea &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; o &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>Para obtener un rendimiento óptimo, las métricas combinadas en el objetivo personalizado (objetivo) deben sumar al menos diez conversiones al día. Si no es así, se recomienda añadir al objetivo métricas de conversión compatibles adicionales, como páginas de productos o inicios de aplicaciones. Consulte [Prácticas recomendadas para crear una meta personalizada](custom-goal-best-practices.md) para obtener directrices.

>[!MORELIKETHIS]
>
>* [Acerca de los objetivos personalizados](custom-goal-about.md)
>* [Prácticas recomendadas para crear una meta personalizada](custom-goal-best-practices.md)
>* [Objetivos de optimización y cómo utilizarlos](optimization-goals.md)
>* [Configuración de paquetes](/help/dsp/campaign-management/packages/package-settings.md)
> * [DSP Optimización de las campañas con la](optimization-how-dsp-optimizes-campaigns.md)
