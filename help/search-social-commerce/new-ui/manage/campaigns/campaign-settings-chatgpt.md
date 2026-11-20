---
title: '[!DNL ChatGPT Ads] paramètres de la campagne'
description: Référencez les paramètres des campagnes [!DNL ChatGPT Ads].
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6aa2e40903fd8652c0ac744e3cd4f68c5e74fd48
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%
---
# [!DNL ChatGPT Ads] paramètres de la campagne

*Les publicités dans [!DNL ChatGPT] sont une fonctionnalité pilote de[!DNL OpenAI]*

## Onglet [!UICONTROL Basic Settings]

*Nouvelles campagnes uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte réseau publicitaire.

**[!UICONTROL Campaign Type]:** Où placer les annonces : la seule option est *[!UICONTROL Standard]* pour afficher les annonces dans [!DNL ChatGPT].

## Onglet [!UICONTROL Campaign Details]

**[!UICONTROL Campaign Name]:** Nom de campagne unique dans le compte.

**[!UICONTROL Status]:** Statut d’affichage de la campagne : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Active*.

**[!UICONTROL Objective]:** Objectif de la campagne : *[!UICONTROL Reach]*, *[!UICONTROL Clicks]* ou *[!UICONTROL Conversions]*. L’objectif détermine les [options d’enchères de groupe publicitaire disponibles](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-settings-chatgpt.md) : l’offre de CPC cible est prise en charge pour les clics et l’offre de CPA cible est prise en charge pour les conversions. Le CPC cible et les enchères du CPA cible ne sont pas disponibles pour les campagnes de portée.

**[!UICONTROL Billing event]:** (nouvelles campagnes avec l’objectif [!UICONTROL Conversions]) Si vous êtes facturé en fonction des clics ou des impressions. La valeur par défaut est clics. L’objectif détermine l’optimisation de la campagne ; l’événement de facturation détermine la manière dont vous êtes facturé. Vous ne pouvez pas modifier l’événement de facturation après avoir enregistré la campagne.

**[!UICONTROL Location Targets]:** Emplacements géographiques d&#39;utilisateurs pris en charge à inclure en tant que cibles. Par défaut, tous les emplacements pris en charge sont ciblés. Vous pouvez limiter les cibles afin d’inclure (mais pas d’exclure) les utilisateurs d’une combinaison d’emplacements.

* Pour cibler tous les emplacements, ne sélectionnez aucun emplacement.

* Pour inclure un emplacement et ses emplacements enfants, cliquez sur le cercle adjacent.

* Pour développer un emplacement dans ses sous-composants (tels que les régions, territoires ou villes), cliquez sur son nom.

* Pour rechercher un emplacement, saisissez ou collez au moins les trois premiers caractères de l’emplacement dans le champ de saisie.

**[!UICONTROL Budget Type]:** Le type de budget de campagne : *Budget quotidien* ou *Durée de vie*. Vous ne pouvez pas modifier le type de budget après avoir enregistré la campagne.

**[!UICONTROL Budget]:** Budget pour le type de campagne spécifié.

**[!UICONTROL Conversion events]:** (facultatif) tout événement de conversion existant configuré dans [!DNL ChatGPT Ads] pour être associé à la campagne. **Remarque :** Les données de performances des conversions suivies par [!DNL OpenAI] ne sont pas disponibles dans Search, Social et Commerce. Surveillez vos conversions suivies par [!DNL OpenAI] dans [!DNL ChatGPT Ads Manager].

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

>[!MORELIKETHIS]
>
>* [Gérer les campagnes](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
