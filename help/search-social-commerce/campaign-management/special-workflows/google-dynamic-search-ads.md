---
title: Mise en oeuvre de  [!DNL Google Ads] publicités de recherche dynamique
description: Découvrez le processus de configuration des  [!DNL Google Ads] annonces de recherche dynamique.
exl-id: 69e5069f-3f82-4ee3-841a-0c1292677223
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Implémentation de [!DNL Google Ads] annonces de recherche dynamique

*[!DNL Google Ads]campagnes de recherche uniquement avec suivi au niveau de la création ou au niveau des mots-clés et de la création uniquement*

Les annonces de recherche dynamique utilisent le contenu de votre site web, plutôt que des mots-clés, pour décider quand afficher vos annonces. Vous pouvez définir les pages de vos sites web dont le contenu est utilisé pour cibler vos annonces de recherche dynamique en configurant des cibles de recherche dynamique distinctes pour le groupe publicitaire ou en choisissant un paramètre de niveau campagne pour cibler vos annonces à l’aide du contenu de votre site web.

Vous pouvez configurer des annonces de recherche dynamique soit individuellement, soit à l’aide de feuilles d’envoi groupé. Les instructions suivantes comprennent des liens vers la création d’entités individuelles.

## Étapes de configuration de [!DNL Google Ads] annonces de recherche dynamique

1. [Créez une campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour les annonces de recherche dynamique :

   1. Définissez d’abord le budget de la campagne sur 10 % des dépenses quotidiennes de la campagne de recherche.

      Vous pourrez augmenter le budget ultérieurement une fois que les publicités auront prouvé leur valeur.

   1. (Si vous souhaitez que [!DNL Google Ads] affiche vos annonces de recherche dynamique en fonction du contenu de votre site web) Indiquez le domaine racine et la langue du domaine dans la section [!UICONTROL DSA Options] des paramètres de campagne.

      >[!NOTE]
      >
      >Votre domaine doit être indexé par l’index de recherche organique [!DNL Google Ads] à cibler. En outre, si le domaine contient des pages dans plusieurs langues et que vous souhaitez tous les cibler, créez une campagne distincte pour chaque langue.

      Si vous n’utilisez pas le domaine de votre site web pour cibler vos publicités, créez des cibles de recherche dynamique (voir Étape 4) pour chaque groupe publicitaire. Vous pouvez créer les cibles [individuellement](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) ou en utilisant [des feuilles en vrac](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

   1. Assurez-vous que la campagne cible le canal de recherche et uniquement le réseau de recherche [!DNL Google Ads] (et non le réseau d’affichage). Ces paramètres sont disponibles à partir de l’onglet [!UICONTROL Networks and Devices].

   1. (Facultatif) Excluez les mots-clés de l’onglet [!UICONTROL Negatives].

   1. (Facultatif) Configurez un modèle de suivi au niveau de la campagne, qui remplace le modèle de suivi au niveau du compte, mais qui peut être remplacé aux niveaux inférieurs.

      (Publicitaires avec Adobe Analytics sans suivi côté serveur) Pour inclure le suivi du flux inverse de Search, Social et Commerce à Analytics, ajoutez le code de suivi AMO ID aux paramètres d’ajout au niveau du compte, qui ajoutent le code à l’URL finale. Voir &quot;[ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)&quot;.

1. [Créez un groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) au sein de la campagne, en procédant comme suit :

   1. Définissez le [!UICONTROL Ad Group Type] sur **[!UICONTROL Search Dynamic].**

   1. Définissez l’offre par défaut pour toutes les publicités.

      Si vous les configurez, vous pouvez remplacer l’offre par défaut pour des cibles de recherche dynamique individuelles.

   1. (Facultatif) Configurez un modèle de suivi au niveau du groupe d’annonces, qui remplace tout modèle de suivi à des niveaux supérieurs, mais qui peut être remplacé au niveau de l’annonce.

      Si vous avez ajouté le suivi Adobe Analytics au niveau de la campagne et que vous souhaitez l’inclure pour le groupe publicitaire, ajoutez-le ici. Voir Etape 1 e.

1. [Créez chaque publicité de recherche dynamique](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) dans le groupe publicitaire.

   [!DNL Google Ads] génère dynamiquement le titre, l’URL d’affichage et l’URL de la page d’entrée pour chaque publicité. Vous pouvez éventuellement ajouter des redirections et un suivi au modèle de suivi au niveau des annonces, qui remplace les modèles de suivi à des niveaux supérieurs.
Si vous souhaitez remplacer un suivi Adobe Analytics à des niveaux supérieurs par un suivi au niveau des publicités, ajoutez-le ici. Voir les étapes 1e et 2c.

1. (Obligatoire lorsque vous n’incluez pas le domaine racine et la langue du domaine dans la section Options DSA des paramètres de campagne ; facultatif dans le cas contraire) Créez des [cibles de recherche dynamique](/help/search-social-commerce/campaign-management/campaigns/dynamic-search-target-manage.md) pour le groupe d’annonces. Vous pouvez éventuellement remplacer l’offre au niveau du groupe publicitaire par des offres au niveau de la cible.

   Les cibles définissent si le réseau publicitaire utilise l’ensemble ou un sous-ensemble de pages de votre site web pour cibler vos annonces de recherche dynamique. Pour optimiser le suivi des performances, configurez votre campagne avec un groupe d’annonces par cible de recherche dynamique et incluez un groupe d’annonces qui cible tous les critères.

1. Au besoin, [modifiez les paramètres de campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) pour ajuster le budget de la campagne et affiner le trafic en excluant des mots-clés supplémentaires de la campagne.
