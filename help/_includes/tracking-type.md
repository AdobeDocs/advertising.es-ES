---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---
# Campo Tipo de seguimiento en la configuración de cuenta y campaña

**[!UICONTROL Tracking Type]:** Método por el que se generan las direcciones URL:

* *[!UICONTROL EF Redirect]* (el valor predeterminado): Para clientes que desean utilizar el servicio de seguimiento de conversiones de Adobe Advertising. Este método genera ID únicos de seguimiento de clics y redirige a los usuarios al servidor de publicidad de Adobe con fines de seguimiento antes de enviarlos a la página de aterrizaje del cliente.

   Este método tiene opciones de seguimiento predeterminadas que se pueden personalizar de forma opcional y también se pueden especificar parámetros para anexar a cada dirección URL.

* *[!UICONTROL No EF Redirect]:* Para clientes que solo desean utilizar sus propios códigos de seguimiento de clics. Search, Social y Commerce no proporcionan ID de seguimiento de clics ni códigos de redirección. Para las cuentas con direcciones URL de destino, cada dirección URL de destino es la misma que la dirección URL base.

   **Notas:**

   * Solo los usuarios administrador de cuentas de agencia, administrador de cuentas de Adobe y administrador pueden cambiar este valor.
   * Si cambia el método de seguimiento, debe volver a generar las direcciones URL de seguimiento de la cuenta.
   * Las opciones de seguimiento a nivel de campaña anulan la configuración a nivel de cuenta.
