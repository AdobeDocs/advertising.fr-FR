---
title: Prévisualisation d’une expérience
description: Découvrez comment prévisualiser les contenus publicitaires dans une expérience publicitaire.
feature: Creative Experiences
exl-id: 2ac8f580-7d3d-4de6-ba14-5d72b30188d7
source-git-commit: a271589a2cb51ec50c37a52254fd8d1b535f279a
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Prévisualisation d’une expérience

Vous pouvez prévisualiser les contenus publicitaires avec une taille d’annonce spécifique que les visiteurs cibles verront pour une expérience, y compris tous les liens hypertexte. Pour les expériences avec le ciblage de l’arborescence de décision, vous pouvez prévisualiser un élément créatif unique, les éléments créatifs d’une branche particulière (type de cible) ou tous les éléments créatifs de l’expérience. Pour les expériences sans ciblage d’arbre de décision, vous pouvez prévisualiser une seule création. <!-- verify -->

* Lorsque vous prévisualisez tous les contenus publicitaires pour l’expérience ou une branche spécifique, tous les contenus publicitaires applicables s’affichent.

* Lorsque vous prévisualisez un seul contenu créatif et que plusieurs contenus créatifs correspondent aux critères, le contenu créatif affiché à chaque actualisation de l’aperçu est basé sur les paramètres de rotation des annonces publicitaires de l’expérience :

   * Pour la rotation algorithmique des publicités, le contenu créatif est sélectionné en fonction de l’objectif d’optimisation.

   * Pour la rotation d’annonces planifiées, le premier élément créatif du planning s’affiche. Vous pouvez continuer à actualiser l’aperçu pour continuer tout au long de la séquence.

   * Pour la rotation pondérée des annonces, le contenu publicitaire est sélectionné en fonction des poids spécifiés (par exemple, 80 % de chances que Creative A s’affiche et 20 % de chances que Creative B s’affiche) à chaque fois.

## Prévisualiser des contenus publicitaires dans une expérience avec le ciblage de l’arborescence de décision

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facultatif) [Personnaliser la vue](/help/creative/introduction/customize-data-views.md) pour inclure des expériences spécifiques.

1. Effectuez l’une des opérations suivantes :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Preview]**.

   * En mode Tableau, maintenez le curseur sur la ligne, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Preview]**.

1. Sélectionnez les contenus publicitaires à prévisualiser :

   * Pour prévisualiser un élément créatif unique :

      1. Cliquez sur **[!UICONTROL Creative]**.

      1. Sélectionnez la taille de l’annonce publicitaire.

      1. Dans la section [!UICONTROL Decision Tree Targeting] , sélectionnez la cible créative.

   * Pour prévisualiser les contenus publicitaires d’une branche spécifique :

      1. Cliquez sur **[!UICONTROL Particular branch]**.

      1. Sélectionnez la taille de l’annonce publicitaire.

     <!-- I don't see this as of 2/3:
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

      1. Sélectionnez la cible créative.

   * Pour prévisualiser tous les contenus publicitaires dans l’expérience, cliquez sur **[!UICONTROL Entire Tree]**.

     <!-- I don't see this as of 2/3:
     1. Click **[!UICONTROL Entire Tree]**.
     1. Select the ad size.
     1. Select whether to group the creatives by Rotation Type or Ad Size.
     -->

1. (Facultatif) Pour inclure le nom du contenu créatif, le type et la taille du contenu créatif, l’URL de la page de destination ou les URL de clics et les attributs flexibles sous chaque contenu créatif, sélectionnez **[!UICONTROL Display Creative Metadata]**.

1. Cliquez sur **[!UICONTROL Preview]**.

1. (Aperçu par contenu créatif uniquement ; facultatif) Dans la barre d’outils, cliquez sur **[!UICONTROL Refresh]** pour prévisualiser les éléments créatifs supplémentaires qui pourraient être affichés, en fonction des paramètres de rotation de l’annonce. <!-- I don't see this as of 2/3 -->

1. (Facultatif) Pour copier une URL de démonstration de l’expérience à partager avec d’autres personnes sans connexion à [!DNL Creative] :

   1. Dans l’angle supérieur droit de l’aperçu, cliquez sur ![Partager](/help/creative/assets/share.png "Partager").

   1. Dans la boîte de dialogue [!UICONTROL Share Demo URL], cliquez sur **[!UICONTROL Copy]** pour copier l’URL dans le presse-papiers afin de la partager avec une autre personne.

## Prévisualiser des contenus publicitaires dans une expérience sans ciblage d’arbre de décision

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. (Facultatif) [Personnaliser la vue](/help/creative/introduction/customize-data-views.md) pour inclure des expériences spécifiques.

1. Effectuez l’une des opérations suivantes :

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Preview]**.

   * En mode Tableau, maintenez le curseur sur la ligne, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Preview]**.

1. (Facultatif) Limitez la liste des contenus publicitaires en sélectionnant une taille de contenu publicitaire spécifique.

   Par défaut, les contenus publicitaires de toutes tailles sont répertoriés.

1. Cliquez sur le nom d’une balise d’annonce publicitaire pour développer la ligne et prévisualiser les contenus publicitaires.

1. (Facultatif) Pour accéder à la page de destination d’un élément créatif, cliquez sur l’élément créatif.

   <!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. (Facultatif) Pour copier une URL de démonstration de l’expérience à partager avec d’autres personnes sans connexion à [!DNL Creative] :

   1. Dans l’angle supérieur droit de l’aperçu, cliquez sur ![Partager](/help/creative/assets/share.png "Partager").

   1. Dans la boîte de dialogue [!UICONTROL Share Demo URL], cliquez sur **[!UICONTROL Copy]** pour copier l’URL dans le presse-papiers afin de la partager avec une autre personne.

>[!MORELIKETHIS]
>
>* [Création d’une expérience avec le ciblage d’arborescence de décision](experience-create-targeting.md)
>* [Création d’une expérience sans ciblage d’arborescence de décision](/help/creative/experiences/experience-create-no-targeting.md)
