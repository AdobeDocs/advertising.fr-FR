---
title: Dupliquer un package
description: Découvrez comment dupliquer un package.
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
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

Voir &quot;[Ce qui n’est pas dupliqué](#package-not-duplicated)&quot; pour une liste de paramètres d’emplacement qui ne sont pas dupliqués.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne pour ouvrir la [!UICONTROL Packages] vue.

1. En regard du nom du module, cliquez sur  **[!UICONTROL ...]** > **[!UICONTROL Duplicate]**.

1. Spécifiez les nouveaux paramètres de module :

   1. Saisissez le nouveau nom du package.

   1. (Facultatif) Modifiez les paramètres par défaut.

      Par défaut :

      * Le nouveau kit est affecté à l’annonceur et à la campagne d’origine.

      * Le nouveau paquet devient principal aujourd&#39;hui.<!-- and the flight continues for NN  days. -->

      * Les emplacements dans le package d’origine sont copiés dans le nouveau package.

      * Les publicités et les pixels d’événement de niveau placement ne sont pas copiés dans le nouveau module.

1. Cliquez sur **[!UICONTROL Submit]**.

## Ce qui n’est pas dupliqué {#package-not-duplicated}

Tous les paramètres des emplacements d’origine sont dupliqués sauf :

* Paramètres d’expérience
* (Si vous modifiez les dates de vol) Planification publicitaire personnalisée
* (Si vous ne joignez pas de publicités) Pondération et planification des publicités personnalisées
* Emplacements par défaut pour les offres (PG) garanties par programmation et emplacements pour [!UICONTROL Simple Ad Serving] transactions
* (Si vous copiez des emplacements dans une autre campagne) :
   * Cibles géographiques
   * Pixels d’événement
   * Publicités
   * Niveau de placement [!DNL DoubleVerify Authentic Brand Safety] segments (qui remplacent les segments au niveau de l’annonceur)

>[!MORELIKETHIS]
>
>* [À propos de la gestion de modules](package-about.md)
>* [Création d’un module](package-create.md)
>* [Modification d’un module](package-edit.md)
>* [Affichage du journal des modifications d’un module](package-change-log.md)
>* [Paramètres du module](package-settings.md)

