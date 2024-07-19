---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Campo Tipo de redirección en la configuración de cuenta y campaña

**[!UICONTROL Redirect Type]:** (solo para [!UICONTROL EF Redirect]) Método para redirigir a los usuarios finales a la dirección URL final o a la dirección URL de destino. La opción seleccionada se aplica a todos los anuncios, palabras clave y ubicaciones de la cuenta o campaña. La configuración predeterminada de nivel de cuenta se hereda de la configuración de seguimiento del anunciante y la configuración predeterminada de nivel de campaña se hereda de la configuración de la cuenta.

* *[!UICONTROL Standard]:* Para redirigir al usuario final a la dirección URL especificada.

* *[!UICONTROL Token]:* Para redirigir al usuario final a la dirección URL y registrar también el identificador de búsqueda, social y Commerce para el clic (`ef_id`) como parámetro de cadena de consulta, que se usa como token. Elija esta opción si desea realizar un informe de las transacciones sin conexión, si desea que Search, Social y Commerce intercambien datos con Adobe Analytics o si desea realizar un seguimiento de todas las conversiones que se producen en [!DNL Apple Safari] exploradores.

**Notas:**

* Si cambia de [!UICONTROL Standard] a [!UICONTROL Token], o viceversa, debe volver a generar las direcciones URL de seguimiento para la cuenta.
* Puede anular la configuración de nivel de cuenta en el nivel de campaña.
