---
title: Dupliquer une campagne
description: Découvrez comment dupliquer une campagne.
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Dupliquer une campagne

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Dupliquez une campagne pour créer une campagne avec des paramètres similaires. Vous pouvez :

* Dupliquez la campagne pour l’annonceur d’origine ou pour une autre campagne
* Vous pouvez éventuellement dupliquer les packages et emplacements d’origine
* Modifier les dates de vol de la nouvelle opération

Pour obtenir la liste des paramètres d’emplacement qui ne sont pas dupliqués, voir &quot;[What&#39;s Not Duplicated](#campaign-not-duplicated)&quot;.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. En regard du nom de la campagne, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Définissez les nouveaux paramètres de campagne :

   1. Saisissez le nouveau nom de l&#39;opération et la date de fin du vol.

   1. (Facultatif) Modifiez les paramètres par défaut.

      Par défaut, la nouvelle campagne est affectée à l’annonceur d’origine, son planning de vol commence le jour en cours et comprend les kits et emplacements d’origine.

1. Cliquez sur **[!UICONTROL Submit]**.

## Éléments non dupliqués {#campaign-not-duplicated}

Tous les paramètres des emplacements d’origine sont dupliqués sauf :

* Paramètres d’expérience
* (Si vous modifiez les dates de vol) Planification publicitaire personnalisée
* (Si vous ne joignez pas de publicités) Pondération et planification des publicités personnalisées
* Emplacements par défaut pour les offres et emplacements garantis par programmation pour les [!UICONTROL Simple Ad Serving] offres
* (Si vous copiez des emplacements dans une autre campagne) :
   * Cibles géographiques
   * Pixels d’événement
   * Publicités
   * Segments de niveau emplacement [!DNL DoubleVerify Authentic Brand Safety] (qui remplacent les segments au niveau de l’annonceur)

>[!MORELIKETHIS]
>
>* [À propos de Campaign Management](campaign-about.md)
>* [Créer une campagne](campaign-create.md)
>* [Modifier une campagne](campaign-edit.md)
>* [Afficher le journal des modifications d’une campagne](campaign-change-log.md)
>* [Paramètres de campagne](campaign-settings.md)
