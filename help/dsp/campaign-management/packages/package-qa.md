---
title: Vérification et modification des paramètres du module à l’aide de feuilles de calcul
description: Découvrez comment vérifier et modifier les paramètres de package clés à l’aide de feuilles de calcul.
feature: DSP Packages
source-git-commit: 230a169611aa3094365a877476f2e5e1c6b3cb9b
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 0%

---

# Vérification et modification des paramètres du module à l’aide de feuilles de calcul

Vous pouvez télécharger les paramètres d’un ou de plusieurs modules au format XLSX ([!DNL Microsoft Excel] tableur) pour révision. La feuille de calcul comprend un onglet séparé avec les informations de vol. Vous pouvez ensuite apporter des modifications à la sélection des champs dans les deux onglets et charger à nouveau les données dans DSP tous en même temps. Les champs modifiables incluent la plupart des paramètres qui sont normalement modifiables.

>[!TIP]
>
>Pour modifier d’autres champs pour un ou plusieurs modules, voir &quot;[Modifier des modules](/help/dsp/campaign-management/packages/package-edit.md)&quot;.

## Paramètres de téléchargement d’un ou de plusieurs modules

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Packages]**.

1. Cochez la case en regard de chaque module dont vous souhaitez télécharger les paramètres.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Download Edit in Excel Sheet]**.

Le fichier est automatiquement enregistré dans le dossier Téléchargement du navigateur. Voir &quot;[Colonnes de module dans les feuilles de calcul téléchargées/téléchargées](#qa-sheet-columns-packages)&quot; pour obtenir la liste des colonnes incluses.

## Paramètres de chargement pour un ou plusieurs modules

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Dans le sous-menu, cliquez sur **[!UICONTROL Packages]**.

1. Cochez la case en regard de chaque module dont vous souhaitez charger les paramètres.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Upload Edit in Excel Sheet]**.

1. Dans la boîte de dialogue [!UICONTROL Edit in Excel] :

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
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget] | Le budget package. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Budget Interval] | Intervalle de budget : &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap] | Limite facultative de l’intervalle de budget. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Interval Cap Period] | L’intervalle pour la limite d’intervalle de budget facultative : &lt;i[!UICONTROL >Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* ou *[!UICONTROL All Time]*. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Goal] | L’objectif du paquet. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Optimization Target] | La valeur cible de l’objectif. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Custom Goal Name] | (Modules avec les objectifs d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; uniquement) [Objectif personnalisé](/help/dsp/optimization/custom-goal.md) qui inclut les recettes ou les événements de conversion utilisés pour calculer la mesure CPA ou ROAS. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Conversion Metric Name] | (Facultatif ; modules avec les objectifs d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend]&quot; et &quot;[!UICONTROL Lowest Cost per Acquisition]&quot; uniquement) L’événement de conversion final ou le montant d’événement/vente de recettes à utiliser pour calculer le retour sur dépenses publicitaires ou le coût par acquisition. | Oui |
| [!UICONTROL Goals & Budget] | [!UICONTROL Package Goal Type] | (Modules avec objectifs d’optimisation personnalisés uniquement) L’objectif du module, qui permet de déterminer comment optimiser le module : *[!UICONTROL Prospecting]*, *[!UICONTROL Retargeting]* ou *[!UICONTROL Other]* . | — |
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

### Onglet [!UICONTROL Package_Flights]

| Section | Colonne | Description | Modifiable ? |
|---------|--------|-------------|-----------|
| [!UICONTROL Flight Details] | [!UICONTROL Package ID] | Identifiant numérique du package. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight ID] | Identifiant numérique du vol. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Start Date] | La première date du vol. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight End Date] | La date finale du vol. | — |
| [!UICONTROL Flight details] | [!UICONTROL Flight Budget] | La cible dépense l&#39;objectif pour le vol. | — |
| [!UICONTROL Flight details] | [!UICONTROL Rollover] | (Packages existants sans l’option &quot;[!UICONTROL Automatically rollover remaining flight budget to next flight]&quot; activée) Montant du budget potentiellement non dépensé à ajouter au prochain vol. | — |

>[!MORELIKETHIS]
>
>* [Modifier des modules](/help/dsp/campaign-management/packages/package-edit.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
