---
title: Acerca de las recomendaciones del editor y la compatibilidad con perspectivas
description: Obtenga información acerca de la compatibilidad para ver y administrar recomendaciones y perspectivas del editor.
feature: Search Recommendations
source-git-commit: cfd8790d6b8384509a77103b8082ed033106431a
workflow-type: tm+mt
source-wordcount: '1606'
ht-degree: 0%

---

# Acerca de las recomendaciones del editor y la compatibilidad con perspectivas

*[!DNL Google Ads]y [!DNL Microsoft Advertising] cuentas*

Las recomendaciones y perspectivas de [!DNL Google Ads] y [!DNL Microsoft Advertising] son sugerencias de la red de anuncios para ayudar a mejorar el rendimiento y la eficacia de sus campañas:

* Cada recomendación de [!DNL Google Ads] proporciona sugerencias personalizadas sobre diferentes aspectos del rendimiento de una campaña (desde agregar un recurso hasta aumentar el presupuesto) en función del historial de rendimiento de la cuenta, la configuración de la campaña y las tendencias de [!DNL Google Ads].

* Cada recomendación y insight de rendimiento de [!DNL Microsoft Advertising] sugiere cambios para optimizar el rendimiento de la campaña en función de los algoritmos de aprendizaje automático y las prácticas recomendadas.

## La vista [!UICONTROL Recommendations]

En (nueva interfaz de usuario) [!UICONTROL Dashboard] > [!UICONTROL Recommendations] y (IU heredada) [!UICONTROL Insights & Reports] > [!UICONTROL Recommendations & Publisher Insights], puede:

* Vea de un vistazo todas las recomendaciones admitidas de que no se han llevado a cabo para una cuenta. La información de cada entrada incluye el tipo de recomendación, la recomendación [!DNL Adobe], las métricas afectadas, la entidad afectada y un vínculo para obtener más detalles. Los incrementos previstos en las métricas se resaltan en verde.

  ![IU de Recommendations](/help/search-social-commerce/assets/recommendations-ui.png "IU de Recommendations")

  Los datos están disponibles en tiempo real al abrir la vista. Para actualizar los datos, haz clic en ![Actualizar](/help/search-social-commerce/assets/refresh.png "Actualizar") en la parte inferior izquierda de la página.

* Para las cuentas de [!DNL Microsoft Advertising], vea de un vistazo cada insight de rendimiento generado en los últimos 30 días para una cuenta de [!DNL Microsoft Advertising]. Las perspectivas proporcionan información similar a las recomendaciones, pero en un formato diferente. Cada insight incluye la fecha, una descripción del problema, la entidad afectada, la causa raíz (que puede incluir vínculos a más detalles) y la acción sugerida con un vínculo para abrir el editor [!DNL Microsoft Advertising], desde el cual puede actuar en insight específico.

* Vea los detalles de una recomendación y aplique o descarte directamente la recomendación.

* Ver un registro de cada recomendación que se aplicó a la cuenta.

## Tipos de recomendación admitidos para [!DNL Google Ads]

| Categoría de recomendación | Tipo de recomendación | Descripción |
| --- | --- | --- |
| [!UICONTROL Ads and extensions] (ahora denominado &quot;[!DNL Ads and assets]&quot; en [!DNL Google Ads]) | [!UICONTROL Call extension] | Añadir extensiones de llamada a una campaña |
| | [!UICONTROL Callout extension] | Añadir extensiones de llamadas a una campaña |
|  | [!UICONTROL Improve demand gen ad strength] | Sugerencias para mejorar la solidez de un anuncio para generar demanda |
| | [!UICONTROL Optimize ad rotation] | Utilizar rotaciones de anuncios optimizadas |
| | [!UICONTROL Responsive search ad] | Añadir un nuevo anuncio de búsqueda adaptable |
| | [!UICONTROL Responsive search ad asset] | Añadir recursos de anuncios de búsqueda adaptable a un anuncio |
| | [!UICONTROL Responsive search improve ad strength] | Sugerencias para mejorar la solidez de un anuncio para una búsqueda adaptable |
| | [!UICONTROL Sitelink extension] | Añadir extensiones de vínculos de sitios a una campaña |
| | [!UICONTROL Text ad] | Añadir un anuncio de texto nuevo |
| [!UICONTROL Automated campaigns] | [!UICONTROL DSA to performance max migration] | Migración de anuncios dinámicos de búsqueda a campañas Máximo rendimiento |
| | [!UICONTROL Dynamic image extension opt in] | Habilite las extensiones de imagen dinámica para la cuenta, lo cual permite al aprendizaje automático de [!DNL Google Ads] anexar automáticamente a su anuncio las imágenes más relevantes de la página de aterrizaje del anuncio |
| | [!UICONTROL Improve performance max ad strength] | Mejore la solidez del grupo de recursos de una campaña Máximo rendimiento para obtener una calificación &quot;Excelente&quot; |
| | [!UICONTROL Performance max final URL opt in] | Activar la expansión de URL final para las campañas Máximo rendimiento |
| | [!UICONTROL Performance max opt in] | Inclusión en campañas Máximo rendimiento |
| | [!UICONTROL Upgrade local campaign to performance max] | Actualización de una campaña local heredada a una campaña de rendimiento máximo |
| | [!UICONTROL Upgrade smart shopping campaign to performance max] | Actualización de una campaña de compras inteligentes heredada a una campaña de rendimiento máximo |
| [!UICONTROL Bidding and budget] | [!UICONTROL Campaign budget] | Presupuesto recomendado para una campaña actualmente limitada por el presupuesto |
| | [!UICONTROL Forecasting campaign budget] | Presupuesto recomendado para una campaña que se espera que esté limitada por el presupuesto en el futuro |
| | [!UICONTROL Forecasting set Target CPA] | Establezca un CPA objetivo para las campañas sin uno antes de un evento de temporada que se pronostique aumente el tráfico |
| | [!UICONTROL Forecasting set Target ROAS] | Aumentar el presupuesto antes de un evento estacional que se prevé que aumente el tráfico y cambiar la estrategia de oferta de [!UICONTROL Maximize Conversion Value] a [!UICONTROL Target ROAS] |
| | [!UICONTROL Marginal ROI campaign budget] | Ajustar el presupuesto de la campaña para aumentar el ROI |
| | [!UICONTROL Maximize clicks opt in] | Cambiar a la estrategia de oferta [!UICONTROL Maximize Clicks] |
| | [!UICONTROL Maximize conversion value opt in] | Cambio en la estrategia de oferta Maximizar valor de conversión |
| | [!UICONTROL Maximize conversions opt in] | Cambiar a la estrategia de oferta [!UICONTROL Maximize Conversions] |
| | [!UICONTROL Move unused budget] | Mover el presupuesto no utilizado a un presupuesto restringido |
| | [!UICONTROL Raise Target CPA bid too low] | Subir [!UICONTROL Target CPA] en una cantidad recomendada cuando sea demasiado bajo y haya pocas conversiones o ninguna |
| | [!UICONTROL Set Target CPA] | Establezca un CPA de destinatario para las campañas sin uno |
| | [!UICONTROL Set Target ROAS] | Establezca un ROAS de destinatario para campañas sin uno |
| | [!UICONTROL Target CPA opt in] | Cambiar a la estrategia de oferta [!UICONTROL Target CPA] |
| | [!UICONTROL Target CPA raising] | Subir [!UICONTROL Target CPA] en función de [!DNL Google Ads] predicciones, que se calculan a partir de conversiones anteriores |
| | [!UICONTROL Target ROAS lowering] | Reduzca [!UICONTROL Target ROAS] en función de [!DNL Google Ads] predicciones, que se calculan a partir de conversiones anteriores |
| | [!UICONTROL Target ROAS opt in] | Cambiar a la estrategia de oferta [!UICONTROL Target ROAS] |
| [!UICONTROL Keywords and targeting] | [!UICONTROL Display expansion opt in] | Amplíe el alcance actualizando una campaña para utilizar la expansión de visualización |
| | [!UICONTROL Keyword] | Añadir nuevas palabras clave |
|  | [!UICONTROL Refresh customer match list] | Actualice las listas de coincidencia de clientes para mostrar anuncios personalizados a clientes recientes |
| | [!UICONTROL Search partners opt in] | Ampliar el alcance con [!DNL Google] socios de búsqueda |
| | [!UICONTROL Use broad match keyword] | Utilice la búsqueda de coincidencias generales para las campañas basadas en conversiones con pujas totalmente automatizadas basadas en conversiones |

## Tipos de recomendación admitidos para [!DNL Microsoft Advertising]

| Categoría de recomendación | Tipo de recomendación | Descripción |
| --- | --- | --- |
| [!UICONTROL Ads and extensions] | [!UICONTROL Responsive search ad] | Añadir un nuevo anuncio de búsqueda adaptable |
| [!UICONTROL Bidding and budgets] | [!UICONTROL Campaign budget] | Corrección de campañas limitadas por el presupuesto |
| [!UICONTROL Keywords and targeting] | [!UICONTROL Keyword] | Añadir nuevas palabras clave de todas las fuentes |

## Vea las recomendaciones y perspectivas del editor {#recommendations-view}

>[!NOTE]
>
>Aunque las recomendaciones de red de anuncios y las perspectivas de rendimiento le ayudan a mejorar el rendimiento de la campaña, es posible que algunas no se alineen con sus objetivos más amplios. Como resultado, es mejor consultar con el equipo de cuenta de Adobe antes de implementar cualquier recomendación o insight.

### (Nueva IU) Vea las recomendaciones del editor

1. En el menú principal, haga clic en **[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**.

1. En la barra de herramientas, seleccione la red publicitaria y la cuenta.

   Para las cuentas de [!DNL Microsoft Advertising], la ficha [!UICONTROL Recommendations] se abre de manera predeterminada.

1. En la columna [!UICONTROL Actions] de la fila, haga clic en **[!UICONTROL View]**. Si la recomendación tiene recomendaciones secundarias, haga clic en **[!UICONTROL View]** junto a la recomendación secundaria.

   Opcionalmente, puede [aplicar o descartar](#recommendations-apply-dismiss) las recomendaciones de la red de anuncios.

### (IU heredada) Ver las recomendaciones del editor

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**.

1. En la parte superior derecha, seleccione la red publicitaria y la cuenta.

   Para las cuentas de [!DNL Microsoft Advertising], los [!UICONTROL Recommendations] de la cuenta se muestran de forma predeterminada.

1. En la columna [!UICONTROL Actions] de la fila, haga clic en **[!UICONTROL View]**. Si la recomendación tiene recomendaciones secundarias, haga clic en **[!UICONTROL View]** junto a la recomendación secundaria.

   Opcionalmente, puede [aplicar o descartar](#recommendations-apply-dismiss) las recomendaciones de la red de anuncios.

### (Nueva interfaz de usuario) Ver sus datos de rendimiento de [!DNL Microsoft Advertising]

1. En el menú principal, haga clic en **[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**.

1. En la barra de herramientas, seleccione la red publicitaria y la cuenta.

1. Haga clic en la ficha **[!UICONTROL Insights]** sobre la tabla de datos.

1. (Opcional) Cuando la columna [!UICONTROL Actions] de la fila incluya una o más acciones:

   * Para abrir el editor [!DNL Microsoft Advertising], desde el cual puede actuar en un insight individual, haga clic en **[!UICONTROL Click here]** junto a la acción.

   * (Perspectivas con varias acciones) Para ver el texto completo de todas las acciones de insight, haga clic en **[!UICONTROL Read More]**. Para abrir el editor [!DNL Microsoft Advertising], desde el cual puede actuar en un insight individual, haga clic en **[!UICONTROL Click here]** junto a la acción individual.

   Si no inició sesión en el editor [!DNL Microsoft Advertising], primero se le dirigirá a la pantalla de inicio de sesión.

### (IU heredada) Ver sus datos de rendimiento de [!DNL Microsoft Advertising]

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**.

1. En la parte superior derecha, seleccione la red publicitaria y la cuenta.

1. Haga clic en **[!UICONTROL Insights]** sobre la tabla de datos.

1. Cuando la columna [!UICONTROL Actions] de la fila incluya una acción, si lo desea, puede hacer clic en **[!UICONTROL Click here]** para abrir el editor [!DNL Microsoft Advertising], desde el cual podrá actuar en insight.

   Si no inició sesión en el editor [!DNL Microsoft Advertising], primero se le dirigirá a la pantalla de inicio de sesión.

## Aplicar o descartar una recomendación del editor {#recommendations-apply-dismiss}

Aplique una recomendación cuando se ajuste a sus objetivos comerciales y deséchela cuando no lo haga.

>[!NOTE]
>
>Aunque las recomendaciones le ayudan a mejorar el rendimiento de las campañas, es posible que algunas no se alineen con sus objetivos más amplios. Como resultado, es mejor consultar con el equipo de cuenta de Adobe antes de implementar cualquier recomendación.

### (Nueva IU) Aplicar o descartar una recomendación del editor

1. En el menú principal, haga clic en **[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**.

1. En la barra de herramientas, seleccione la red publicitaria y la cuenta.

   Para las cuentas de [!DNL Microsoft Advertising], la ficha [!UICONTROL Recommendations] se abre de manera predeterminada.

1. (Opcional) Filtre las recomendaciones por categoría y tipo.

1. En la columna [!UICONTROL Actions] de la fila insight o Recommendations, haga clic en **[!UICONTROL View]**.

1. (Recomendaciones con subrecomendaciones) Haga clic en **[!UICONTROL View]** junto a la subrecomendación.

1. (Opcional) Realice una de las siguientes acciones:

   * Para aplicar una recomendación, haga clic en **[!UICONTROL Apply]**.

     La aplicación de una recomendación puede tardar entre milisegundos y pocos segundos, según el tamaño de la recomendación.

   * Para descartar una recomendación, haga clic en **[!UICONTROL Dismiss]**.

### (IU heredada) Aplicar o descartar una recomendación del editor

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**.

1. En la parte superior derecha, seleccione la red publicitaria y la cuenta.

   Para las cuentas de [!DNL Microsoft Advertising], los [!UICONTROL Recommendations] de la cuenta se muestran de forma predeterminada.

1. (Opcional) Filtre las recomendaciones por categoría y tipo.

1. En la columna [!UICONTROL Actions] de la fila insight o Recommendations, haga clic en **[!UICONTROL View]**.

1. (Recomendaciones con subrecomendaciones) Haga clic en **[!UICONTROL View]** junto a la subrecomendación.

1. (Opcional) Realice una de las siguientes acciones:

   * Para aplicar una recomendación, haga clic en **[!UICONTROL Apply]**.

     La aplicación de una recomendación puede tardar entre milisegundos y pocos segundos, según el tamaño de la recomendación.

   * Para descartar una recomendación, haga clic en **[!UICONTROL Dismiss]**.

## Ver un registro de las recomendaciones del editor para una cuenta {#recommendations-log}

Puede ver un registro de cada recomendación que se aplicó. La información incluye la categoría de recomendación, el tipo de recomendación, las entidades afectadas, el usuario que aplicó la recomendación y la marca de tiempo.

Las recomendaciones descartadas no están disponibles en la red de anuncios.

### (Nueva IU) Ver un registro de las recomendaciones del editor para una cuenta

1. En el menú principal, haga clic en **[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**.

1. En la barra de herramientas, seleccione la red publicitaria y la cuenta.

1. En la esquina superior derecha, haga clic en ![Registros de recomendaciones](/help/search-social-commerce/assets/recommendations-log-view-new.png "Registros de recomendaciones").

### (IU heredada) Ver un registro de las recomendaciones del editor para una cuenta

1. En el menú principal, haga clic en **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**.

1. En la parte superior derecha, seleccione la red publicitaria y la cuenta.

1. En la esquina superior derecha, haga clic en ![Registros de recomendaciones](/help/search-social-commerce/assets/recommendations-log-view.png "Registros de recomendaciones").

## Prácticas recomendadas para usar recomendaciones de editores con portafolios

<!--
 Add info for MS once we have it ..." 

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts*
 
-->

## [!DNL Google Ads] recomendaciones

| Tipo de recomendación | Descripción | ¿Aplicar automáticamente Recommendations con portafolios de Search, Social y Commerce? | Comentarios |
|--- |--- |--- |--- |
| [!UICONTROL Ads] y extensiones (ahora denominados &quot;anuncios y recursos&quot; en [!DNL Google Ads]) | Recomendaciones para agregar o editar anuncios y recursos | Se puede aplicar automáticamente, pero los anunciantes deben revisar las recomendaciones manualmente. | Es necesario revisar las recomendaciones para garantizar que los anuncios de búsqueda interactivos estén alineados con los requisitos del anunciante. |
| [!UICONTROL Automated campaigns] | Recomendaciones para campañas automatizadas (campañas locales e inteligentes) | No disponible en Buscar, Social ni Commerce. | — |
| [!UICONTROL Bidding and budget] | Recomendaciones de oferta, presupuesto y objetivo para mejorar el rendimiento | No aplique automáticamente para campañas en portafolios optimizados. | Las recomendaciones actuales pueden ser unidimensionales para los fines que desee. Por ejemplo, [!DNL Google Ads] recomienda un aumento en la CPA de destino, sin preocuparse por el presupuesto, cuando los clics disminuyen para una campaña. |
| [!UICONTROL Keywords and targeting] | Limpieza de palabras clave y recomendaciones de audiencia | Se puede aplicar automáticamente, pero utilice la aplicación automática de forma selectiva. | Utilice la limpieza de palabras clave y la eliminación de redundancias entre campañas, pero evite una mayor automatización (como la creación automática de anuncios dinámicos de búsqueda o la expansión automática de audiencias). |
| [!UICONTROL Measurement] | Recomendaciones para el seguimiento de conversiones y la certificación | No disponible en Buscar, Social ni Commerce. | Estas recomendaciones pueden afectar al rendimiento. Consulte con su equipo de cuenta de Adobe para discutir los pros y los contras de cualquier recomendación antes de aplicarla. |
| [!UICONTROL Repairs] | Recomendaciones varias para mejorar los problemas de la cuenta | No disponible en Buscar, Social ni Commerce. | Revisar manualmente y periódicamente las recomendaciones de reparación en [!DNL Google Ads]. Este tipo de recomendación es una buena manera de identificar anuncios, problemas de fuentes, problemas de seguimiento, etc. no aprobados. |
| [!UICONTROL Other] | Recomendación de usar la aplicación móvil [!DNL Google Ads] | No disponible en Buscar, Social ni Commerce. | — |

<!--

>[!MORELIKETHIS]
>
>* [View your publisher recommendations and performance insights](recommendation-view.md)
>* [Apply or dismiss a publisher recommendation](recommendation-apply-dismiss.md)
>* [View the publisher recommendations log for an account](recommendation-view-log.md)
>* [Best practices for using publisher recommendations with portfolios](recommendation-best-practices.md)

-->
