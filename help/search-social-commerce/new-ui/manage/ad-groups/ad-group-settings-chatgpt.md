---
title: '[!DNL ChatGPT] paramètres du groupe publicitaire'
description: Référencez les paramètres pour [!DNL ChatGPT] groupes publicitaires.
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
source-git-commit: 52c1132246ea0cc48b6102e6d6f15be1ded32f09
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%
---
# [!DNL ChatGPT] paramètres du groupe publicitaire

*Les publicités dans [!DNL ChatGPT] sont une fonctionnalité pilote de[!DNL OpenAI]*

## Onglet [!UICONTROL Basic Settings]

*Nouveaux groupes publicitaires uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne. Vous ne pouvez pas modifier la campagne après avoir créé le groupe publicitaire.

## Onglet [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Group name]:** nom de groupe publicitaire unique dans la campagne et contenant au moins trois caractères.

**[!UICONTROL Status]:** Statut d’affichage du groupe publicitaire : *[!UICONTROL Active]* ou *[!UICONTROL Paused]*. La valeur par défaut pour les nouveaux groupes publicitaires est *[!UICONTROL Active]*.

**[!UICONTROL Bid strategy]:** (campagnes avec l’objectif [!UICONTROL Clicks] ou [!UICONTROL Conversions]) Comment enchérir sur des annonces du groupe publicitaire :

* *[!UICONTROL Autobid]:* (valeur par défaut pour les nouveaux groupes publicitaires) [!DNL OpenAI] ajuste automatiquement les enchères afin d’obtenir le plus de clics ou de conversions possibles, selon l’objectif de la campagne, à partir de votre budget. Vous ne saisissez pas de montant d&#39;enchère. Cette option est disponible pour les budgets de campagne quotidiens et de durée de vie.

* *[!UICONTROL Target CPC]:* (campagnes avec l’objectif [!UICONTROL Clicks]) Enchères vers un coût moyen par clic. Saisissez l’objectif dans le champ [!UICONTROL Target CPC].

* *[!UICONTROL Target CPA]:* (campagnes avec l’objectif [!UICONTROL Conversions]) Enchères vers un objectif de coût moyen par conversion. Saisissez l’objectif dans le champ [!UICONTROL Target CPA].

* *[!UICONTROL Manual: Max bid]:* (groupes d&#39;annonces existants enchéris manuellement uniquement) Conserve l&#39;enchère maximum existante sous la forme d&#39;un montant en lecture seule. Vous pouvez conserver cette stratégie ou passer à [!UICONTROL Autobid] ou à la stratégie cible pour l’objectif de la campagne. Cette option n&#39;est pas disponible pour les nouveaux groupes publicitaires ou lors de la modification de groupes publicitaires qui utilisent déjà les enchères automatiques ou les enchères cibles.

Les groupes d’annonces existants ajoutés manuellement ne sont pas automatiquement modifiés en une autre stratégie. La modification d’un montant cible ou d’un paramètre non lié ne modifie pas une stratégie d’enchères cible existante.

**[!UICONTROL Target CPC]:** (groupes publicitaires avec la stratégie d’enchères [!UICONTROL Target CPC] ; obligatoire) Coût moyen par clic que vous souhaitez atteindre, dans la devise du compte. Saisissez un montant positif. Il s&#39;agit d&#39;un objectif de coût moyen et non d&#39;une enchère maximum.

**[!UICONTROL Target CPA]:** (groupes publicitaires avec la stratégie d’enchères [!UICONTROL Target CPA] ; obligatoire) Coût moyen par conversion que vous souhaitez atteindre, dans la devise du compte. Saisissez un montant positif. Il s&#39;agit d&#39;un objectif de coût moyen et non d&#39;une enchère maximum.

**[!UICONTROL Maximum CPC bid]:** (campagnes avec l’objectif [!UICONTROL Clicks] ; groupes d’annonces existants enchéris manuellement uniquement ; lecture seule) Montant maximal existant que vous paierez pour chaque clic.

**[!UICONTROL Conversion-optimized bid cap]:** (campagnes avec l’objectif [!UICONTROL Conversions] ; groupes d’annonces existants enchéris manuellement uniquement ; lecture seule) Montant maximal existant que vous êtes prêt à enchérir pour une conversion. [!DNL OpenAI] utilise le taux de conversion prévu pour convertir cette valeur en enchère par impression.

**[!UICONTROL Maximum CPM bid]:** (Campagnes avec l’objectif [!UICONTROL Reach]) Montant maximal que vous paierez pour mille impressions, dans la devise du compte. Entrez une valeur comprise entre 0,01 et 5 000. Les campagnes Reach ne disposent pas des options [!UICONTROL Bid strategy].

**[!UICONTROL Context hints (optional)]:** Description des conversations, sujets ou mots-clés pour lesquels vos produits ou services peuvent être pertinents. Séparez les indications par des virgules ou des sauts de ligne. Vos indications peuvent être utilisées pour guider la correspondance, mais ne sont pas des règles de ciblage de correspondance exacte. Consultez l’aide de [[!DNL ChatGPT Ads] pour savoir comment écrire des indications contextuelles efficaces](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints).

**[!UICONTROL Landing Page Suffix]:** (facultatif) tout paramètre à ajouter à la fin des URL de page de destination pour effectuer le suivi des informations. Exemple : `param1=value1&param2=value2`.

>[!MORELIKETHIS]
>
>* [Gérer les groupes publicitaires](ad-group-manage.md)
