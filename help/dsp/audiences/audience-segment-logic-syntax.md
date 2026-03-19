---
title: Syntaxe de la logique de segment d’audience
description: Référencez la syntaxe que vous pouvez utiliser pour définir la logique des segments d’audience.
feature: DSP Audiences
exl-id: fb73f35f-1f65-463b-b93c-90804a8d19a9
source-git-commit: c83ad42f7d703e66713c9a34cbc6c9b5acbbc981
workflow-type: tm+mt
source-wordcount: '141'
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
