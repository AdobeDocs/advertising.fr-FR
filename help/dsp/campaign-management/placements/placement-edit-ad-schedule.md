---
title: Modifier les plannings de publicités pour les emplacements
description: Découvrez comment modifier les plannings de publicités pour les publicités jointes aux emplacements.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: 18c68edec80a80d236df138c05fba8d857c9ed9e
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Modifier les plannings de publicités pour les emplacements

## Modifier les plannings de publicités pour un ou plusieurs emplacements

Vous pouvez modifier les dates de vol planifiées et la rotation des annonces associées à plusieurs emplacements à l’aide d’une feuille de calcul [!DNL Microsoft Excel]. Chaque annonce peut être active pendant plusieurs vols.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez télécharger les données publicitaires.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Lorsque le fichier est disponible, cliquez sur **[!UICONTROL Download]** dans la notification située en haut de la page du navigateur pour télécharger un fichier de feuille de calcul (au format XLSX) conformément à la procédure habituelle de votre navigateur.

   ![Télécharger la notification prête](/help/dsp/assets/download-ready.png "Télécharger la notification prête")

1. Ouvrez le fichier téléchargé, modifiez les champs d’informations de vol pour chaque ligne d’annonce à inclure dans le vol et enregistrez le fichier mis à jour :

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (par exemple [!UICONTROL Flight 1 Start Date] et [!UICONTROL Flight 1 End Date]) : les première et dernière dates du vol. Utilisez le format AAAA-MM-JJ pour chaque date. Toutes les annonces dont les champs de date de vol sont vides sont traitées comme des annonces ne participant pas au programme.

   * **[!UICONTROL Flight N Weight]** (par exemple, [!UICONTROL Flight 1 Weight]) : rotation des publicités pour un vol. Saisissez une valeur :

      * Pour faire pivoter uniformément les publicités pour un vol, saisissez `[!UICONTROL Even]`.

      * Pour faire pivoter les publicités d’un vol de manière inégale, entrez le poids relatif de rotation de chaque publicité, sous la forme d’un pourcentage (par exemple, `40` pour 40 %). Le poids total du vol doit être égal à 100.

1. Chargez le modèle de planning publicitaire modifié :

   1. Cochez la case en regard de chaque emplacement applicable.

   1. Dans la barre d’outils d’actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**, puis spécifiez le fichier à charger.

## Modifier le planning publicitaire pour un emplacement unique

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

Vous pouvez modifier les dates de vol planifiées et la rotation des annonces associées à un emplacement. Chaque annonce peut être active pendant plusieurs vols.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Ads]** > **[!UICONTROL Ad schedule]**.

1. Effectuez l’une des opérations suivantes :

   * Pour ajouter un vol, cliquez sur **[!UICONTROL Add Flight]**, puis spécifiez la date de début et la date de fin.

   * Pour ajouter un vol existant à une publicité, cliquez sur **[!UICONTROL +]** dans la ligne de publicité de la colonne de vol.

   * Pour supprimer un vol existant d’une publicité, cliquez sur **[!UICONTROL x]** dans la ligne de publicité de la colonne de vol.

      * (Lorsque plusieurs publicités présentent le même vol) Pour faire pivoter les publicités de manière inégale, cliquez sur **[!UICONTROL Even Rotation]** dans les informations de vol, puis entrez le poids relatif de rotation de chaque publicité, sous la forme d’un pourcentage.

        Le poids total doit être égal à 100.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Continue]**.

1. Vérifiez les détails du vol, puis cliquez sur **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Modifier les emplacements](placement-edit.md)
>* [Afficher le journal des modifications pour un emplacement](placement-change-log.md)
>* [Paramètres d’emplacement](placement-settings.md)
