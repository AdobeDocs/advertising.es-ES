---
source-git-commit: 37c408f320fd95fb4f84e65ae73e5e67799e218b
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---
# Estado de Portfolio

<!-- used in multiple procedures -->

* *Borrador:* Al portafolio le falta un objetivo o al menos una campaña activa asignada. Este estado se establece automáticamente y cambia automáticamente a *inactivo* cuando asigna la configuración que falta y guarda los cambios.

* *Inactivo:* Search, Social y Commerce recopilan datos de costos, clics e impresiones de las campañas relevantes para generar informes.

* *Activo:* (portafolios existentes con toda la configuración requerida; requiere al menos una campaña activa con al menos una unidad de oferta activa) Search, Social y Commerce recopila datos de costo/clic/impresión y datos de ingresos para las campañas relevantes, y también modela los datos. Active un portafolio inactivo para empezar a modelar datos o reduzca un portafolio optimizado al estado activo para detener la optimización.

* *Optimizado:* (portafolios existentes con todas las configuraciones requeridas; requiere al menos una campaña activa con al menos una unidad de oferta activa) Search, Social y Commerce recopila datos de costo/clic/impresión y datos de ingresos para las campañas relevantes, modela los datos para determinar las estrategias de optimización y optimiza el portafolio según se requiera para el tipo de portafolio y las estrategias de oferta de campaña. Cambiar el estado a optimizado también se denomina inicio del portafolio. Se pueden optimizar las siguientes opciones: ofertas para palabras clave y anuncios, valores de ajuste de oferta (cuando está habilitado), presupuestos de campaña (cuando está habilitado) y objetivos de estrategia de oferta. No puede cambiar el estado a &quot;optimizado&quot; a menos que el portafolio contenga al menos una campaña activa con al menos un anuncio activo y una palabra clave/ubicación. **Nota:** Si elimina todas las campañas de un portafolio optimizado o las elimina, el estado del portafolio cambiará automáticamente a &quot;inactivo&quot;.
