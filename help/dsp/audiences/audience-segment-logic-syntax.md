---
title: Syntaxe de la logique de segment d’audience
description: Référencez la syntaxe que vous pouvez utiliser pour définir la logique des segments d’audience.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
TQID: https://experienceleague.adobe.com/FPci9npdKrFxwge6tw41Fhx4XAC9VqYFc-RZhLhILLo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 0%

---

# Syntaxe de la logique de segment d’audience

Lorsque vous créez des audiences réutilisables, vous pouvez définir manuellement la logique du segment à l’aide d’identifiants de segment alphanumériques (clés) et de la syntaxe suivante :

* () pour indiquer un groupe
* `||` pour [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; pour les [!DNL AND]
* ! par [!DNL NOT] (exclure)

>[!NOTE]
>
>* Tous les groupes de segments spécifiés sont inclus, sauf s’ils sont précédés de ! (ce qui les exclut).
>* Vous pouvez [trouver l’identifiant de segment pour une audience](reusable-audience-clipboard.md) à partir de [!UICONTROL Audiences] > [!UICONTROL All audiences].

Par exemple, la logique suivante :

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

signifie (en anglais brut)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>Dans les paramètres d’emplacement, vous pouvez utiliser les audiences enregistrées comme audiences à cibler explicitement ou comme audiences distinctes à exclure du ciblage. Assurez-vous que la logique de votre segment reflète l’objectif d’utilisation de l’audience.

>[!MORELIKETHIS]
>
>* [Copiez la clé de segment pour une audience réutilisable dans le presse-papiers](reusable-audience-clipboard.md)
>* [À propos de la gestion des audiences](audience-about.md)
>* [Créer une audience réutilisable](reusable-audience-create.md)
>* [Paramètres de l’audience](audience-settings.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
