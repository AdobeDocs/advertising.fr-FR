---
title: Afficher les détails Sites, Ads, Frequency et Inventory pour un emplacement
description: Découvrez comment afficher les sites ciblés, les publicités, la fréquence et les données d’inventaire pour un emplacement.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 0f022babeab6c044949760cedc103323eb0cc950
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Afficher les détails Sites, Ads, Frequency et Inventory pour un emplacement

Pour chaque emplacement, vous pouvez [ouvrir un [!UICONTROL Inspector] (vue détaillée)](placement-details-view.md) qui répertorie tous les sites, annonces et offres ciblés dans un emplacement. Elle inclut également des données de fréquence pour l’emplacement. Vous pouvez éventuellement exporter les données de n’importe quel onglet.

![inspecteur d’emplacement](/help/dsp/assets/placement-inspector.png)

## Informations dans la [!UICONTROL Inspector] Emplacement {#placement-inspector}

* **[!UICONTROL Sites]:** tous les sites sur lesquels l&#39;emplacement a eu des impressions.

  L’onglet [!UICONTROL Sites] comprend des fonctionnalités de recherche et de filtrage, les mêmes options d’affichage des colonnes standard et personnalisées que celles disponibles sur la page principale, ainsi qu’un bouton [!UICONTROL Exclude] dans chaque ligne afin que vous puissiez rapidement exclure un site de l’emplacement.

* **[!UICONTROL Ads]:** toutes les annonces de l’emplacement.

  L’onglet [!UICONTROL Ads] comprend des fonctions de recherche et de filtrage, les mêmes options d’affichage des colonnes standard et personnalisées que celles disponibles sur la page principale, ainsi que des boutons d’action rapide dans chaque ligne, tels que [!UICONTROL View Ad Approvals].

* **[!UICONTROL Frequency]:** Données pour chaque niveau de fréquence publicitaire de l’emplacement, notamment :
   * le niveau de fréquence de la publicité (par exemple « 1 » pour toutes les instances dans lesquelles les utilisateurs ont vu une publicité une fois)
   * estimation du nombre unique d’appareils/navigateurs ou de personnes (en fonction du [!UICONTROL Cross Device Level] spécifié pour la campagne) qui ont reçu des impressions au niveau de fréquence spécifié
   * nombre estimé d’impressions au niveau de fréquence spécifié
   * fréquence moyenne estimée pour le niveau de fréquence spécifié. Cette valeur est égale à (Impressions estimées)/(Uniques estimées).

* **[!UICONTROL Inventory]:** Informations sur toutes les offres ciblées par l’emplacement.

  L’onglet [!UICONTROL Inventory] permet un dépannage rapide en affichant des statistiques de performances, telles que [!UICONTROL Auctions], [!UICONTROL Bids] et [!UICONTROL Win Rate]. L’onglet comprend des fonctionnalités de recherche et de filtrage, les mêmes options d’affichage des colonnes standard et personnalisées que celles disponibles sur la page principale, ainsi que des boutons d’action rapide dans chaque ligne, y compris des [!UICONTROL Edit], des [!UICONTROL View Report] et des [[!UICONTROL Auction Insights] pour un dépannage plus approfondi](/help/dsp/inventory/private-deal-auction-insights.md).

## Ouvrir le [!UICONTROL Placement Inspector] {#inspector-open}

1. Ouvrez la vue des emplacements pour la campagne ou le package parent :

   * Afficher tous les emplacements dans la campagne parent :

      1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

      1. Cliquez sur le nom de la campagne.

      1. Cliquez sur l’onglet **[!UICONTROL Placements]** .

   * Afficher tous les emplacements dans le package parent :

      1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

      1. Cliquez sur le nom de la campagne.

      1. Cliquez sur l’onglet **[!UICONTROL Packages]** .

      1. Cliquez sur le nom du package parent.

1. Placez le curseur sur la ligne d&#39;emplacement, puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Inspector]**.

1. (Facultatif) [Modifiez la vue Colonnes](campaign-data-views-manage.md#column-view-change) au besoin pour afficher les mesures requises.

1. (Facultatif) Pour exporter les données sur n’importe quel onglet, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") en haut à droite, puis cliquez sur **[!UICONTROL Export]**.

   Les données sont enregistrées dans le dossier de téléchargement par défaut de votre navigateur sous la forme d’un rapport au format XLSM.

## Suppression d’une publicité d’un emplacement du [!UICONTROL Placement Inspector] {#remove-ads-placement-inspector}

1. [Ouvrez le [!UICONTROL Placement Inspector]](#inspector-open).

1. Cliquez sur l’onglet **[!UICONTROL Ads]** .

1. En regard du nom de l’annonce publicitaire, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Detach]**.

## Dépannage de l’inventaire

| Problème | Cause possible | Mesures à prendre |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | L&#39;éditeur n&#39;a pas commencé à envoyer de demandes d&#39;enchères. | Contactez l’éditeur pour activer la transaction. |
| | L’opération a été configurée de manière incorrecte, par exemple en saisissant un ID d’opération externe incorrect. | Confirmez les détails de l’opération et modifiez l’opération. |
| [!UICONTROL Auctions but no Bids] | Le ciblage de l’emplacement ne correspond pas aux demandes d’enchères entrantes pour l’opération. <br><br> Par exemple, un emplacement peut cibler une zone géographique qui n’est pas éligible à l’offre. | Modifiez les cibles d&#39;emplacement selon les besoins pour éviter les incohérences de ciblage. |
| | L’emplacement ne comporte pas d’annonce active avec le type de média requis pour la transaction. | Créez et joignez une annonce publicitaire avec le type de média approprié à l’emplacement. |
| | L&#39;emplacement n&#39;a pas un budget suffisant. | Augmentez le budget de l’emplacement pour permettre les enchères sur les demandes entrantes. |
| | Les dates de vol d&#39;emplacement ne se chevauchent pas avec les dates de livraison d&#39;impression pour l&#39;affaire. | Modifiez les dates de vol de l’emplacement selon vos besoins. |
| [!UICONTROL Low Win Rate] | L&#39;enchère maximum du placement (plancher ou fixe) est inférieure au minimum requis par l&#39;opération. | Augmentez le [!UICONTROL Max Bid] de l’emplacement si nécessaire. |
| | L’emplacement utilise des filtres de pré-enchères qui limitent les enchères. | Abaissez les seuils des filtres de pré-enchères pour permettre plus d’enchères. |
| | Le ciblage de l’audience pour l’emplacement est trop restrictif. | Vérifiez si les cibles d’audience spécifiées comptent suffisamment d’utilisateurs actifs et développez l’audience si possible. |

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues de gestion de campagnes](campaign-reports-about.md)
>* [Gestion Des Vues De Données De Campaign](campaign-data-views-manage.md)
