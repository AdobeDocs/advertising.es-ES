---
title: (Nueva IU) Acerca de los portafolios
description: Más información sobre los portafolios.
feature: Search Portfolios, Search Optimization
hide: true
exl-id: 8d023c22-a1dd-4608-8c72-0a61f055e7e5
source-git-commit: f7c63646b3eae20fd3413446789fe06ce583e23e
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# (Nueva IU) Acerca de los portafolios

*característica de Beta*

Puede administrar sus campañas de publicidad de forma colectiva mediante portafolios (similar a los portafolios de inversión). Un portafolio es un conjunto de campañas publicitarias o conjuntos de anuncios, incluidas sus palabras clave y anuncios asociados, que se optimizan para lograr un único objetivo comercial. Un objetivo puede incluir varias conversiones ponderadas y un único presupuesto o objetivo de rendimiento (como un presupuesto mensual o un objetivo de retorno de la inversión). Dado que las campañas/conjuntos de anuncios, las palabras clave y los anuncios individuales pueden tener un rendimiento diferente entre sí (por ejemplo, pueden gastar cantidades diferentes o lograr ROI diferentes), la capacidad de optimización utiliza modelos impulsados por IA para dirigir todo el catálogo de productos para lograr el objetivo de forma colectiva. Todas las campañas de un portafolio utilizan la misma moneda.

Algunas funciones de usuario pueden crear y configurar portafolios. Según el tipo de portafolio, la configuración del portafolio puede incluir el objetivo del portafolio, las campañas asignadas, la estrategia de gasto, cualquier restricción de oferta en el nivel de portafolio, y los parámetros de modelado y optimización. Cuando esté listo para que Search, Social y Commerce inicien la optimización de un portafolio, cambie el estado a &quot;optimizado&quot;.

Opcionalmente, puede agrupar portafolios en [grupos de portafolios](portfolio-group-manage.md) para poder ver los datos compuestos de todo el grupo.

Según su función, es posible que pueda generar simulaciones de rendimiento, que utilizan el modelado predictivo para identificar el punto de gasto óptimo y los informes detallados de precisión de la previsión.<!-- Mention this now? In addition, all users can use the Spend Recommendation Tool to identify the optimal budget distribution across portfolios. -->

## Compatibilidad de optimización por estrategia de oferta {#optimization-by-bid-strategy}

Las campañas pueden optimizarse según la campaña o la estrategia de oferta del grupo de anuncios.

>[!NOTE]
>
>Las &quot;pujas inteligentes&quot; y las &quot;pujas automatizadas&quot; suelen utilizarse indistintamente, pero no son lo mismo. Las pujas inteligentes solo hacen referencia a [!DNL Google Ads] y [!DNL Microsoft Advertising] estrategias de pujas automatizadas que utilizan pujas en tiempo de subasta, lo que significa que la red de anuncios optimiza las conversiones o los valores de conversión en el momento de cada subasta.

<!-- Add "Frequency of Bidding (or other actions, like adjusting campaign budget or bid adjustment values?) -->

| Estrategia de oferta | ¿Pujas inteligentes? | ¿Oferta a nivel de grupo de palabras clave/productos? | Nivel de soporte | Tipo de objetivo | Unidad de oferta | ¿Qué Establece Adobe? | ¿Qué establece la red de publicidad? |
|---|---|---|---|---|---|---|---|
| CPC manual (opción de solo [!DNL Google Ads]) | — | Sí | Crear, editar, optimizar | Objetivo de una o varias propiedades con cualquier valor de peso | Palabra clave + Tipo de coincidencia + Campaña | Palabra clave bid, campaign budget, valores de ajuste de oferta | n/a |
| ECPC (CPC mejorado) | Sí | Sí | Crear, editar, optimizar | Objetivo de una o varias propiedades con cualquier valor de peso | Palabra clave + Tipo de coincidencia + Campaña | Oferta por palabra clave, presupuesto de campaña | Ajusta las ofertas en tiempo real |
| Maximizar clics[^1] | — | — | Crear, editar, optimizar | Ninguno; solo optimiza los clics | Campaign | Presupuesto de campaña | Ajusta la oferta en tiempo real para maximizar los clics dentro del presupuesto |
| Maximizar conversiones<br>(con o sin TCPA) | Sí | — | Crear, editar, optimizar | Objetivo de una sola propiedad con una ponderación de 1 | Campaña o grupo de publicidad ([!DNL Google Ads])<br>Solo campaña ([!DNL Microsoft Advertising]) | Presupuesto de la campaña, CPA de destino cuando se establece<br>TCPA puede ser una estrategia de oferta independiente en [!DNL Microsoft Advertising]) | Ajusta la oferta en tiempo real para maximizar los pedidos/posibles clientes dentro del presupuesto y alcanzar el objetivo de la CPA cuando se establece el objetivo |
| Maximizar el valor de conversión<br>(con o sin TROAS) | Sí | — | Crear, editar, optimizar | Objetivo de varias propiedades con cualquier valor de peso o objetivo de una sola propiedad con un valor de peso mayor que 1 (para representar un valor monetario) | Campaña o grupo de publicidad ([!DNL Google Ads])<br>Solo campaña ([!DNL Microsoft Advertising]) | Presupuesto de la campaña, ROAS de destino cuando se establece<br>TROAS puede ser una estrategia de oferta independiente en [!DNL Microsoft Advertising]) | Ajusta las ofertas en tiempo real para maximizar los ingresos/beneficios dentro del presupuesto, cumpliendo el objetivo de ROAS cuando se establece el objetivo |
| Cuota de impresiones objetivo | — | — | Crear, editar | n/a | n/a | n/a: no se puede asignar a un portafolio | Ajusta las ofertas en tiempo real para alcanzar el objetivo de cuota de impresión |

[^1]: La configuración de la estrategia de oferta [!UICONTROL Maximize Clicks] en la red de anuncios no es la misma que el objetivo [!UICONTROL Maximize Clicks] de Search, Social y Commerce. Si la estrategia de oferta es [!UICONTROL Maximize Clicks], solo debe asignarla a un portafolio con optimización de nivel de campaña o de nivel de grupo de anuncios, no a un portafolios con optimización de nivel de palabra clave.

## Estados de Portfolio {#portfolio-status}

Un portafolio puede tener los siguientes estados:

<!-- **Link to include file for "Portfolio status"** -->

{{$include /help/_includes/search-portfolio-status.md}}

## La vista [!UICONTROL Portfolios]

La vista [!UICONTROL Portfolios] muestra sus portafolios existentes, con datos de rendimiento personalizables. Puede [personalizar las columnas dentro de la vista](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md) y filtrar los datos para incluir portafolios específicos [de la barra de herramientas](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) o del [encabezado de columna](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md).

<!-- No options yet to edit anything within the grid, view bid changes, add a portfolio to a portfolio group, edit the Target column, or import/export DOW targets. -->

### Acciones disponibles

<!-- Update with any new options -->

<!-- within row:
* [Rename a portfolio](portfolio-rename.md)

* [View the constraints for a portfolio](portfolio-view-constraint.md)

* [View the change history for a portfolio](portfolio-view-change-history.md)
-->

* [Crear un portafolio](portfolio-create.md)

* [Duplicación de un portafolio](portfolio-duplicate.md)

* [Editar configuración de portafolio](portfolio-edit.md)

* [Edición masiva de la configuración de portafolios mediante archivos de hojas de edición masiva](portfolio-bulksheets.md)

* [Ver detalles de rendimiento del portafolio](portfolio-details.md)

* [Descargar datos en la vista [!UICONTROL Portfolios]](portfolio-view-report.md)

>[!MORELIKETHIS]
>
>* [Crear un portafolio](portfolio-create.md)
>* [Duplicar un portafolio](portfolio-duplicate.md)
>* [Editar un portafolio](portfolio-edit.md)
>* [Administrar informes de vista de datos desde la vista [!UICONTROL Portfolios]](portfolio-view-report.md)
