---
title: (Nueva IU) Cambiar el estado de un portafolio
description: Obtenga información sobre cómo cambiar el estado de un portafolio o eliminar un portafolio inactivo.
feature: Search Portfolios, Search Optimization
hide: true
source-git-commit: 081453404883619e0a70bba080c857bf7e3136cc
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# (Nueva IU) Cambiar el estado de un portafolio

*característica de Beta*

El estado de un portafolio puede ser uno de los siguientes:

* **Inactiva:** La capacidad de optimización está recopilando datos de costos, clics e impresiones de las campañas relevantes para fines de informes, pero no está modelando los datos ni optimizando los presupuestos y las ofertas de las campañas.

* **Activo:** La capacidad de optimización está recopilando datos de costos, clics e impresiones, así como datos de ingresos para las campañas relevantes y está modelando los datos, pero no está optimizando los presupuestos ni las ofertas de las campañas. Active un portafolio inactivo para empezar a modelar datos o reduzca un portafolio optimizado al estado activo para detener la optimización.

* **Optimizada:** La capacidad de optimización está recopilando datos de costos, clics, impresiones e ingresos de las campañas relevantes, modelando los datos y optimizando los presupuestos y las ofertas de las campañas (cuando corresponda) en la fecha de inicio designada del portafolio. Cambiar el estado a optimizado también se denomina inicio del portafolio.

Para dejar de recopilar datos de costes, clics e impresiones y datos de ingresos de las campañas relevantes, elimine el portafolio. Al eliminar un portafolio, no estará disponible en Search, Social y Commerce.

Todos los cambios realizados en el estado del portafolio se registran en su historial de cambios.

## Optimizar, activar o desactivar un portafolio

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Mantenga el cursor sobre la fila del portafolio y haga clic en ![Editar](/help/search-social-commerce/assets/edit.png "Editar") junto al [!UICONTROL Portfolio Status].

1. Cambiar el estado:

   * Para activar una cartera inactiva u optimizada, seleccione **[!UICONTROL Active]**.

   * Para desactivar una cartera activa, seleccione **[!UICONTROL Inactive]**.

   * Para optimizar (iniciar) un portafolio activo, seleccione **[!UICONTROL Optimized]**.

     >[!NOTE]
     >
     >* Solo puede iniciar un portafolio si ya está activo y contiene al menos una campaña activa con al menos un anuncio activo y una palabra clave o ubicación.
     >* Antes de lanzar un portafolio, debe implementar etiquetas de seguimiento de conversión en las páginas web del anunciante.
     >* Antes de iniciar un portafolio, la práctica recomendada es realizar un análisis de línea de base.
     >* Si va a lanzar un nuevo portafolio, asegúrese de que la fecha de inicio sea hoy o más tarde.>* Evite cambiar el portafolio en la primera semana después del lanzamiento, aunque el rendimiento sea volátil.
     >* Una vez que Search, Social y Commerce empiecen a optimizar un portafolio, debe dejar que administre todos los cambios de oferta futuros (cuando corresponda). Search, Social y Commerce sobrescribirán los cambios que realice desde la red de publicidad.
     >* Después de lanzar un portafolio, puede establecer temporalmente ofertas manuales para cualquier campaña CPC del portafolio creando y publicando hojas de edición masiva de campañas. Cualquier cambio de oferta que resulte de los datos publicados es aplicable por un día. Después, Search, Social y Commerce reanudan el establecimiento de ofertas según su propia estrategia de optimización.

## Eliminar un portafolio inactivo

Solo puede eliminar portafolios inactivos. Si el portafolio está optimizado o activo, primero debe cambiar su estado a inactivo antes de tener la opción de eliminarlo.

1. En el menú principal, haga clic en **[!UICONTROL Manage]>[!UICONTROL Portfolios]**.

1. Realice una de las acciones siguientes:

   * Mantenga el cursor sobre la fila del portafolio y haga clic en **[!UICONTROL ...]>[!UICONTROL Delete]**.

   * Seleccione la casilla de verificación situada junto al portafolio. En la barra de herramientas de acciones masivas, haga clic en ![Eliminar](/help/search-social-commerce/assets/delete-new.png "Eliminar").

1. En el mensaje de confirmación, haga clic en **[!UICONTROL Confirm]**.

>[!MORELIKETHIS]
>
>* [Crear un portafolio](portfolio-create.md)
>* [(nueva interfaz de usuario) Editar un portafolio](portfolio-edit.md)
>* [Acerca de los portafolios](portfolio-about.md)
