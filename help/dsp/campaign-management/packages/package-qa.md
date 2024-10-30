---
title: Vérification et modification des paramètres du module à l’aide de feuilles d’envoi groupées
description: Découvrez comment vérifier et modifier les paramètres de module clés en bloc à l’aide de feuilles de calcul.
feature: DSP Packages
exl-id: bf52de27-db48-40e2-bb55-a2c27a1924ad
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Vérification et modification des paramètres du module à l’aide de feuilles d’envoi groupées

Vous pouvez télécharger les paramètres d’un ou de plusieurs modules au format XLSX ([!DNL Microsoft Excel] tableur) pour révision. La feuille de calcul comprend un onglet séparé avec les informations de vol.

Pour mettre à jour plusieurs paramètres à la fois, vous pouvez effectuer l’une des opérations suivantes :

* Apportez des modifications pour sélectionner des champs, enregistrer le fichier et charger à nouveau le fichier de feuille d’envoi groupé modifié dans DSP.

* Pour apporter des modifications à des packages supplémentaires et aux paramètres d’un emplacement ou d’une publicité, téléchargez un modèle de feuille d’envoi vierge contenant des onglets pour chaque type de composant de campagne, saisissez ou collez des paramètres nouveaux ou mis à jour dans le fichier de modèle, puis chargez le fichier pour apporter les modifications. Pour plus d’informations, voir &quot;[Vérification et modification des paramètres des composants de campagne à l’aide de feuilles d’envoi groupées](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

Les champs modifiables incluent la plupart des paramètres qui sont normalement modifiables.

>[!TIP]
>
>Pour modifier rapidement d’autres champs pour un ou plusieurs modules, voir &quot;[Modifier des modules](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Paramètres de téléchargement pour tous les modules d’un Campaign

Lorsque vous téléchargez les paramètres de tous les packages d’une campagne, la feuille de calcul comprend des onglets distincts pour les paramètres du package et pour les informations de vol. Vous pouvez éventuellement inclure des paramètres pour les emplacements et les annonces associés aux forfaits ; Des onglets supplémentaires sont inclus pour les paramètres de placement et d’annonce.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans l’angle supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download QA sheet]**.

1. Dans la boîte de dialogue [!UICONTROL QA Sheet Download], désélectionnez les composants de campagne dont vous souhaitez exclure les paramètres du fichier téléchargé, puis cliquez sur **[!UICONTROL Download]**.

Par défaut, les paramètres de tous les emplacements et annonces associés aux packages sont sélectionnés.

Un message de notification indique à quel moment le fichier peut être téléchargé.

1. Pour télécharger le fichier, effectuez l’une des opérations suivantes :

   * Dans le message de notification, cliquez sur **[!UICONTROL Download].**

   * Dans la droite de la barre de menus supérieure, cliquez sur ![Tâches](/help/dsp/assets/downloads.png). Cliquez sur **[!UICONTROL Download]** en regard de la tâche.

     Le fichier est enregistré dans le dossier Téléchargements du navigateur. Voir &quot;[Colonnes de placement dans les feuilles de calcul téléchargées/téléchargées](#qa-sheet-columns)&quot; pour obtenir la liste des colonnes incluses.

>[!NOTE]
>
>Vous ne pouvez pas modifier ni recharger les feuilles d’assurance qualité au niveau de la campagne. Pour apporter des modifications aux paramètres du composant de campagne dans ces fichiers, téléchargez un modèle de feuille d’envoi groupé distinct, saisissez ou collez des lignes de la feuille d’assurance qualité dans le modèle de feuille d’envoi groupé, enregistrez le fichier, puis chargez la feuille d’envoi groupée renseignée. Pour plus d’informations, voir &quot;[Vérification et modification des paramètres des composants de campagne à l’aide de feuilles d’envoi groupées](/help/dsp/campaign-management/campaign-components-review-edit.md)&quot;.

## Paramètres de téléchargement d’un ou de plusieurs modules

Lorsque vous téléchargez des paramètres pour des modules spécifiques, le fichier de feuille d’envoi groupé comprend des onglets distincts pour les paramètres du module et pour les informations de contrôle, et le fichier est modifiable.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Packages]**.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   Un message de notification indique à quel moment le fichier de feuille d’envoi groupé peut être téléchargé.

1. Pour télécharger la feuille d’envoi groupé, effectuez l’une des opérations suivantes :

   * Dans le message de notification, cliquez sur **[!UICONTROL Download].**

   * À droite de la barre de menu supérieure, cliquez sur ![Tâches](/help/dsp/assets/downloads.png). Cliquez sur **[!UICONTROL Download]** en regard de la tâche.

     Le fichier est enregistré dans le dossier Téléchargements du navigateur. Voir &quot;[Colonnes de placement dans les feuilles de calcul téléchargées/téléchargées](#qa-sheet-columns)&quot; pour obtenir la liste des colonnes incluses.

<!-- I don't think I need this here

## Download a Bulksheet Template {#download-template}

You can optionally download a blank bulksheet template that includes tabs for each type of campaign component. You can later add rows to any tab on the template and [upload the edited file](##upload-bulksheet-package) to make changes. 

1. Click the name of the campaign.

1.  In the upper right, click **[!UICONTROL ...]** > **[!UICONTROL Download Bulksheet]**.

   The file is saved to the browser's Downloads folder. See "[Placement Columns in Downloaded/Uploaded Spreadsheets](#qa-sheet-columns)" for a list of the included columns.

-->

## Chargement d’une feuille de support avec les paramètres de module {#upload-bulksheet-package}

Vous pouvez charger les paramètres de vos modules, y compris les emplacements et les publicités associés aux modules, dans un fichier de feuille d’envoi groupé.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Bulksheet]**.

1. Dans la boîte de dialogue [!UICONTROL Upload Bulksheet] :

   1. Faites glisser un fichier dans la zone ou cliquez dans la zone pour sélectionner un fichier sur votre périphérique ou votre réseau.

   1. Cliquez sur **[!UICONTROL Upload]**.

1. (Facultatif) Pour vérifier que les mises à jour ont été traitées, cliquez sur ![Tâches](/help/dsp/assets/downloads.png) à droite de la barre de menu supérieure.

## Colonnes de paramètre de package dans les feuilles de calcul téléchargées/chargées{#qa-sheet-columns-packages}

>[!TIP]
>
> Dans une feuille de calcul téléchargée, toutes les colonnes modifiables sont surlignées en bleu.

### Onglet [!UICONTROL Package]

| Section | Colonne | Description | Modifiable ? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic details] | [!UICONTROL Package ID] | Identifiant numérique du package. | — |
| [!UICONTROL Basic details] | [!UICONTROL Package Name] | Nom du module. | Oui |
| [!UICONTROL Basic details] | [!UICONTROL Status] | État du package : *[!UICONTROL active]* ou *[!UICONTROL inactive]*. | Oui |
| [!UICONTROL Basic details] | [!UICONTROL Description] | Description facultative du package. | Oui |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - CPM] | Taux de frais tiers statique à suivre en tant que coût non facturable pour 1 000 impressions, le cas échéant. | Oui |
| [!UICONTROL Basic details] | [!UICONTROL 3rd-party fees - description] | Une description facultative du taux de frais tiers, le cas échéant. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Start Date] | Date de début du package. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package End Date] | Date de fin du package. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pacing Level] | À quel niveau pour accélérer et plafonner les emplacements dans le package : *[!UICONTROL Package]* ou *[!UICONTROL Placement]*. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | Le budget du package. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | L’intervalle budgétaire : &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Limite d’intervalle budgétaire facultative. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | L’intervalle pour la limite d’intervalle de budget facultative : &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | L’objectif du paquet. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | La valeur cible de l’objectif. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Modules avec les objectifs d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; uniquement) [Objectif personnalisé](/help/dsp/optimization/custom-goal.md) qui inclut les recettes ou les événements de conversion utilisés pour calculer la mesure CPA ou ROAS. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Facultatif ; modules avec les objectifs d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; uniquement) L’événement de conversion final ou le montant d’événement/vente de recettes à utiliser pour calculer le retour sur dépenses publicitaires ou le coût par acquisition. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Modules avec objectifs d’optimisation personnalisés uniquement) L’objectif du module, qui permet de déterminer comment optimiser le module : *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* ou *[!UICONTROL Other]* . | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package id for learning carryover] | (Modules avec objectifs d’optimisation personnalisés uniquement) Identifiant du module pour un autre module dont les données historiques sont utilisées comme entrée pour l’optimisation du module. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Linked Package Name for learning carryover] | (Modules avec objectifs d’optimisation personnalisés uniquement) Autre module dont les données historiques sont utilisées comme entrée pour optimiser le module. | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Pace on] | Indique si le package se déplace vers *[!UICONTROL budget]* ou *[!UICONTROL primary_goal]* (pour les impressions). | — |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Amount] | (Lorsque vous placez le module sur des impressions) Le nombre cible d’impressions pendant l’intervalle de temps spécifié. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Primary Goal Interval] | (Lorsque vous placez le module sur des impressions) Intervalle de temps pour le nombre cible d’impressions. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Flight Pacing] | La stratégie de fréquence des vols pour le package : *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* ou *[!UICONTROL aggressive frontload]*. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Intraday Pacing] | La stratégie de traitement intrajournalier du package : *[!UICONTROL Even]* ou *[!UICONTROL ASAP]*. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap] | Limite de fréquence principale du package pendant le [!UICONTROL Frequency Cap Interval] spécifié. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval] | Intervalle de la limite de fréquence principale : *[!UICONTROL Day]*, *[!UICONTROL Week]* ou *[!UICONTROL Month]*. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Frequency Cap Interval Value] | Nombre de semaines, jours, heures ou minutes pour lesquelles s’applique le [!UICONTROL Frequency Cap] principal. Par exemple, si la limite principale est de 12 impressions par mois, alors la valeur ici est `12`. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap] | Limite de fréquence secondaire du package pendant le [!UICONTROL Secondary Frequency Cap Interval] spécifié | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval] | Type d’intervalle pour la limite de fréquence secondaire : *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* ou *[!UICONTROL Minute]*. Le nombre applicable de semaines, jours, heures ou minutes est indiqué par le [!UICONTROL Secondary Frequency Cap Interval Value]. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Secondary Frequency Cap Interval Value] | Nombre de semaines, jours, heures ou minutes pour lesquelles s’applique le [!UICONTROL Secondary Frequency Cap]. Par exemple, si la limite secondaire est de trois impressions par six heures, alors la valeur ici est `6`. | Oui |
| [!UICONTROL Custom Flights] | [!UICONTROL Activate Custom Flights] | Que vous créiez ou non des vols de fréquence variable pour le package *T* (true) ou *F* (false). Une fois que vous avez activé le vol personnalisé et enregistré le package, vous ne pouvez pas désactiver le vol personnalisé ni modifier la date de début du package. | — |
| [!UICONTROL Custom Flights] | [!UICONTROL Automatic Budget Rollover] | (Disponible uniquement lorsque l’option [!UICONTROL Activate Custom Flighting] est activée) Indique s’il faut ajouter automatiquement le budget restant du vol précédent au budget existant pour le prochain vol : *T* (true) ou *F* (false). | Oui |
| [!UICONTROL Error] | [!UICONTROL Error] | Toutes les erreurs pertinentes. | — |

### Onglet [!UICONTROL Package_Flights] {#qa-sheet-columns-package-flights}

| Section | Colonne | Description | Modifiable ? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | Identifiant numérique du package. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | Identifiant numérique du vol. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | La première date du vol. | Oui |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | Date finale du vol. | Oui |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | La cible dépense l&#39;objectif pour le vol. | Oui |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Packages existants sans l’option &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; activée) Montant du budget potentiellement non dépensé à ajouter au prochain vol. | Oui |

>[!MORELIKETHIS]
>
>* [Vérification et modification des paramètres des composants Campaign à l’aide de feuilles de support](/help/dsp/campaign-management/campaign-components-review-edit.md)
>* [Modifier les kits](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
