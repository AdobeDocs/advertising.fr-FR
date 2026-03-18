---
title: Implémenter  [!DNL Google Ads]  publicités de recherche dynamiques
description: Découvrez le processus de configuration  [!DNL Google Ads]  publicités de recherche dynamique.
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: 79b4294df79fcc16916a01ac2d1a57f0b968d368
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Implémenter [!DNL Google Ads] publicités de recherche dynamiques

*[!DNL Google Ads]les campagnes de recherche uniquement avec un suivi de niveau création ou de niveau mot-clé et création uniquement*

Les annonces de recherche dynamique utilisent le contenu de votre site web plutôt que des mots-clés pour décider quand afficher vos annonces. Vous pouvez définir les pages de vos sites web dont le contenu est utilisé pour cibler vos annonces de recherche dynamique en configurant des cibles de recherche dynamique distinctes pour le groupe d’annonces ou en choisissant un paramètre au niveau de la campagne pour cibler vos annonces à l’aide du contenu de votre site web.

Vous pouvez configurer les annonces de recherches dynamiques individuellement ou à l’aide de feuilles d’envoi groupé. Les instructions suivantes incluent des liens vers la création d’entités individuelles.

## Étapes de configuration [!DNL Google Ads] publicités de recherche dynamique

1. [Créez une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour les annonces de recherches dynamiques :

   1. Définissez d’abord le budget de la campagne sur 10 % des dépenses quotidiennes de votre campagne de recherche.

      Vous pourrez ensuite augmenter le budget une fois que les publicités auront prouvé leur valeur.

   1. (Si vous [!DNL Google Ads] afficher vos annonces de recherche dynamique en fonction du contenu de votre site web) Spécifiez le domaine racine et la langue du domaine dans la section [!UICONTROL DSA Options] des paramètres de la campagne.

      >[!NOTE]
      >
      >Votre domaine doit être indexé par l’index de recherche organique [!DNL Google Ads] à cibler. En outre, si le domaine contient des pages dans plusieurs langues et que vous souhaitez cibler toutes les pages, créez une campagne distincte pour chaque langue.

      Si vous n’utilisez pas le domaine de votre site web pour cibler vos publicités, créez des cibles de recherche dynamique (voir Étape 4) pour chaque groupe publicitaire. Vous pouvez créer les cibles [individuellement](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) ou à l’aide de [ feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Assurez-vous que la campagne cible le canal de recherche et uniquement le réseau de recherche [!DNL Google Ads] (et non le réseau d’affichage). Ces paramètres sont disponibles à partir de l’onglet [!UICONTROL Networks and Devices] .

   1. (Facultatif) Excluez les mots-clés de l’onglet [!UICONTROL Negatives] .

   1. (Facultatif) Configurez un modèle de suivi au niveau de la campagne, qui remplace le modèle de suivi au niveau du compte, mais peut être remplacé aux niveaux inférieurs.

      (Annonceurs avec Adobe Analytics sans suivi côté serveur) Lorsque vous souhaitez inclure le suivi du flux inverse de Search, Social et Commerce à Analytics, ajoutez le code de suivi AMO ID aux paramètres d’ajout au niveau du compte, ce qui ajoute le code à l’URL finale. Voir « [Adobe Advertising IDs utilisés par  [!DNL Analytics]](/help/integrations/analytics/ids.md). »

1. [Créez un groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) au sein de la campagne, en procédant comme suit :

   1. Définissez la [!UICONTROL Ad Group Type] sur **[!UICONTROL Search Dynamic].**

   1. Définissez l’enchère par défaut pour toutes les publicités.

      Vous pouvez remplacer l’enchère par défaut pour des cibles de recherche dynamique individuelles, si vous les configurez.

   1. (Facultatif) Configurez un modèle de suivi au niveau du groupe publicitaire , qui remplace tous les modèles de suivi aux niveaux supérieurs, mais peut être remplacé au niveau de l’annonce.

      Si vous avez ajouté le suivi Adobe Analytics au niveau de la campagne et souhaitez l’inclure pour le groupe publicitaire, ajoutez-le ici. Voir l’étape 1e.

1. [Créez chaque annonce publicitaire de recherche dynamique](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) dans le groupe d’annonces.

   [!DNL Google Ads] génère dynamiquement le titre, l’URL d’affichage et l’URL de la page de destination pour chaque publicité. Vous pouvez éventuellement ajouter des redirections et un suivi au modèle de suivi au niveau des annonces, ce qui remplace les modèles de suivi aux niveaux supérieurs.
Si vous souhaitez remplacer un suivi Adobe Analytics à des niveaux supérieurs par un suivi au niveau des annonces, ajoutez-le ici. Voir les étapes 1e et 2c.

1. (Obligatoire si vous n’incluez pas le domaine racine et la langue du domaine dans la section Options DSA des paramètres de la campagne, facultatif dans le cas contraire) Créez [cibles de recherche dynamique](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) pour le groupe publicitaire. Vous pouvez également remplacer l&#39;offre au niveau du groupe publicitaire par des offres au niveau de la cible.

   Les cibles définissent si le réseau publicitaire utilise l’ensemble ou un sous-ensemble des pages de votre site web pour cibler vos publicités de recherche dynamique. Pour suivre au mieux les performances, configurez votre campagne avec un groupe publicitaire par cible de recherche dynamique et incluez un groupe publicitaire qui cible tous les critères.

1. Si nécessaire, [modifiez les paramètres de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour ajuster le budget de la campagne et affiner le trafic en excluant des mots-clés supplémentaires de la campagne.
