---
title: Dupliquer un package
description: Découvrez comment dupliquer un package.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Dupliquer un package

Dupliquez un package pour créer un package avec des paramètres similaires. Vous pouvez :

* Dupliquez le kit dans l&#39;annonceur et la campagne d&#39;origine ou dans des kits différents.
* Vous pouvez éventuellement dupliquer les emplacements dans le module.
* (Pour les modules dupliqués dans les campagnes d’origine) Vous pouvez éventuellement dupliquer les publicités d’origine et les pixels d’événement de niveau emplacement.
* Modifier les dates de vol du nouveau package

Pour obtenir la liste des paramètres d’emplacement qui ne sont pas dupliqués, voir &quot;[What&#39;s Not Duplicated](#package-not-duplicated)&quot;.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne pour ouvrir la vue [!UICONTROL Packages].

1. En regard du nom du package, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Spécifiez les nouveaux paramètres de module :

   1. Saisissez le nouveau nom du package.

   1. (Facultatif) Modifiez les paramètres par défaut.

      Par défaut :

      * Le nouveau kit est affecté à l’annonceur et à la campagne d’origine.

      * Le nouveau package devient actif le jour en cours.<!-- and the flight continues for NN  days. -->

      * Les emplacements dans le package d’origine sont copiés dans le nouveau package.

      * Les publicités et les pixels d’événement de niveau placement ne sont pas copiés dans le nouveau module.

1. Cliquez sur **[!UICONTROL Submit]**.

## Éléments non dupliqués {#package-not-duplicated}

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
>* [À propos de la gestion de modules](package-about.md)
>* [Créer un module](package-create.md)
>* [Modifier un module](package-edit.md)
>* [Afficher le journal des modifications d’un package](package-change-log.md)
>* [Paramètres du module](package-settings.md)
