---
title: Sintaxis de la lógica de segmento de audiencia
description: Haga referencia a la sintaxis que puede utilizar para definir la lógica de los segmentos de audiencia.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
source-git-commit: 97f5e8913afb2f71505512bf8e4ab5bf56c1d7f8
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Sintaxis de la lógica de segmento de audiencia

Cuando cree audiencias reutilizables, puede definir manualmente la lógica de segmentos mediante ID de segmento alfanuméricos (claves) y la siguiente sintaxis:

* () para indicar un grupo
* `||` para [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; para [!DNL AND]
* ! para [!DNL NOT] (excluir)

>[!NOTE]
>
>* Se incluyen todos los grupos de segmentos especificados a menos que estén precedidos por ! (lo que los excluye).
>* Puede [búsqueda del ID de segmento de una audiencia](reusable-audience-clipboard.md) de [!UICONTROL Audiences] > [!UICONTROL All audiences].

Por ejemplo, la lógica siguiente:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

significa (en inglés)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>En la configuración de colocación, puede utilizar audiencias guardadas como audiencias para dirigirse explícitamente o como audiencias independientes para excluir de la segmentación. Asegúrese de que la lógica del segmento refleje el propósito para el que utilizará la audiencia.

>[!MORELIKETHIS]
>
>* [Copiar la clave del segmento para una audiencia reutilizable en el portapapeles](reusable-audience-clipboard.md)
>* [Acerca de Audience Management](audience-about.md)
>* [Crear una audiencia reutilizable](reusable-audience-create.md)
>* [Configuración de audiencia](audience-settings.md)
>* [Proveedores de datos de terceros disponibles](third-party-data-providers.md)
