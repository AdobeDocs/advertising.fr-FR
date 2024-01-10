---
title: Modification des planifications de publicité pour les emplacements
description: Découvrez comment modifier les plannings de publicité pour les publicités liées aux emplacements.
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: bc45e96cf091cba3872b20f6ea691e369b29982f
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# Modification des planifications de publicité pour les emplacements

## Modification des planifications de publicité pour un ou plusieurs emplacements

Vous pouvez modifier les dates de vol planifiées et la rotation des publicités associées à plusieurs emplacements à l’aide d’une [!DNL Microsoft Excel] feuille de calcul. Chaque publicité peut être active pendant plusieurs vols.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. Cochez la case en regard de chaque emplacement dont vous souhaitez télécharger les données publicitaires.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. Lorsque le fichier est disponible, cliquez sur **[!UICONTROL Download]** dans la notification située en haut de la page du navigateur pour télécharger un fichier de feuille de calcul (au format XLSX) selon la procédure normale de votre navigateur.

   ![Notification de téléchargement prêt](/help/dsp/assets/download-ready.png "Notification de téléchargement prêt")

1. Ouvrez le fichier téléchargé, modifiez les champs d’informations de vol pour chaque ligne d’annonce à inclure dans le vol, puis enregistrez le fichier mis à jour :

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** (par exemple [!UICONTROL Flight 1 Start Date] et [!UICONTROL Flight 1 End Date]) : les premières et dernières dates du vol. Utilisez le format AAAA-MM-JJ pour chaque date. Toutes les publicités avec des champs de date de vol vides sont traitées comme des publicités non participantes.

   * **[!UICONTROL Flight N Weight]** (par exemple [!UICONTROL Flight 1 Weight]) : comment faire pivoter les publicités pour un vol. Saisissez une valeur :

      * Pour faire pivoter uniformément les publicités d’un vol, saisissez `[!UICONTROL Even]`.

      * Pour faire pivoter inégalement les publicités d’un vol, indiquez le poids relatif de rotation de chaque publicité, sous forme de pourcentage (par exemple : `40` pour 40 %). Le poids total du vol doit être de 100.

1. Téléchargez le modèle de planification des publicités modifié :

   1. Cochez la case en regard de chaque emplacement approprié.

   1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**, puis spécifiez le fichier à télécharger.

## Modification de la planification des publicités pour un emplacement unique

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

Vous pouvez modifier les dates de vol planifiées et la rotation des publicités pour les publicités associées à un emplacement. Chaque publicité peut être active pendant plusieurs vols.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**.

1. En regard du nom de l’emplacement, cliquez sur  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

   1. Effectuez l’une des opérations suivantes :

      * Pour ajouter un vol, cliquez sur **[!UICONTROL Add Flight]**, puis spécifiez la date de début et la date de fin.

      * Pour ajouter un vol existant à une publicité, cliquez sur **[!UICONTROL +]** dans la ligne publicitaire de la colonne &quot;vol&quot;.

      * Pour supprimer un vol existant d’une publicité, cliquez sur **[!UICONTROL x]** dans la ligne publicitaire de la colonne &quot;vol&quot;.

      * (Lorsque plusieurs publicités ont le même vol) Pour faire pivoter les publicités de manière inégale, cliquez sur **[!UICONTROL Even Rotation]** dans les informations sur le vol, puis saisissez le poids relatif de rotation de chaque publicité, sous forme de pourcentage.

        Le poids total doit être égal à 100.

   1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Continue]**.

   1. Vérifiez les détails du vol, puis cliquez sur **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des emplacements](placement-about.md)
>* [Modifier un emplacement](placement-edit.md)
>* [Affichage du journal des modifications d’un emplacement](placement-change-log.md)
>* [Paramètres d’emplacement](placement-settings.md)
