---
title: Modification des planifications de publicité pour les emplacements
description: Découvrez comment modifier les plannings de publicité pour les publicités liées aux emplacements.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Modification des planifications de publicité pour les emplacements

## Modification des planifications de publicité pour un ou plusieurs emplacements

Vous pouvez modifier les dates de vol planifiées et la rotation des publicités pour les publicités jointes à plusieurs emplacements à l’aide d’une feuille de calcul [!DNL Microsoft Excel]. Chaque publicité peut être active pendant plusieurs vols.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez télécharger les données publicitaires.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Lorsque le fichier est disponible, cliquez sur **[!UICONTROL Download]** dans la notification située en haut de la page du navigateur pour télécharger un fichier de feuille de calcul (au format XLSX) selon la procédure normale de votre navigateur.

   ![Notification prête pour le téléchargement](/help/dsp/assets/download-ready.png "Notification prête pour le téléchargement")

1. Ouvrez le fichier téléchargé, modifiez les champs d’informations de vol pour chaque ligne d’annonce à inclure dans le vol, puis enregistrez le fichier mis à jour :

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (par exemple [!UICONTROL Flight 1 Start Date] et [!UICONTROL Flight 1 End Date]) : les premières et dernières dates du vol. Utilisez le format AAAA-MM-JJ pour chaque date. Toutes les publicités avec des champs de date de vol vides sont traitées comme des publicités non participantes.

   * **[!UICONTROL Flight N Weight]** (par exemple [!UICONTROL Flight 1 Weight]) : comment faire pivoter les publicités pour un vol. Saisissez une valeur :

      * Pour faire pivoter uniformément les publicités d&#39;un vol, saisissez `[!UICONTROL Even]`.

      * Pour faire pivoter inégalement les publicités d’un vol, indiquez le poids relatif de rotation de chaque publicité, sous forme de pourcentage (par exemple, `40` pour 40 %). Le poids total du vol doit être de 100.

1. Téléchargez le modèle de planification des publicités modifié :

   1. Cochez la case en regard de chaque emplacement approprié.

   1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**, puis spécifiez le fichier à télécharger.

## Modification de la planification des publicités pour un emplacement unique

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

Vous pouvez modifier les dates de vol planifiées et la rotation des publicités pour les publicités associées à un emplacement. Chaque publicité peut être active pendant plusieurs vols.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

1. Effectuez l’une des opérations suivantes :

   * Pour ajouter un vol, cliquez sur **[!UICONTROL Add Flight]**, puis spécifiez la date de début et la date de fin.

   * Pour ajouter un vol existant à une publicité, cliquez sur **[!UICONTROL +]** dans la ligne de publicité pour la colonne de vol.

   * Pour supprimer un vol existant d’une publicité, cliquez sur **[!UICONTROL x]** dans la ligne de publicité pour la colonne de contrôle.

      * (Lorsque plusieurs publicités ont le même vol) Pour faire pivoter les publicités de manière inégale, cliquez sur **[!UICONTROL Even Rotation]** dans les informations sur le vol, puis saisissez le poids relatif de rotation de chaque publicité, sous forme de pourcentage.

        Le poids total doit être égal à 100.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Continue]**.

1. Vérifiez les détails du vol, puis cliquez sur **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Modifier des emplacements](placement-edit.md)
>* [Afficher le journal des modifications d’un emplacement](placement-change-log.md)
>* [Paramètres de placement](placement-settings.md)
