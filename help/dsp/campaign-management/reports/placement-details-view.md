---
title: Affichage des détails sur les sites, les publicités, la fréquence et le stock pour un emplacement
description: Découvrez comment afficher les sites, publicités, fréquence et données d’inventaire ciblés pour un emplacement.
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# Affichage des détails sur les sites, les publicités, la fréquence et le stock pour un emplacement

Pour chaque emplacement, vous pouvez [ouvrir un (affichage des détails [!UICONTROL Inspector])](placement-details-view.md), qui répertorie tous les sites, publicités et offres ciblés dans un emplacement. Il inclut également les données de fréquence pour l’emplacement. Vous pouvez éventuellement exporter les données de n’importe quel onglet.

![Inspecteur de placement](/help/dsp/assets/placement-inspector.png)

## Informations sur l&#39;emplacement [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** Tous les sites sur lesquels l’emplacement a eu des impressions.

  L’onglet [!UICONTROL Sites] comprend des fonctions de recherche et de filtrage, les mêmes options d’affichage des colonnes standard et personnalisées disponibles sur la page principale, ainsi qu’un bouton [!UICONTROL Exclude] dans chaque ligne afin que vous puissiez rapidement exclure un site de l’emplacement.

* **[!UICONTROL Ads]:** toutes les publicités de l’emplacement.

  L’onglet [!UICONTROL Ads] comprend des fonctions de recherche et de filtrage, les mêmes options d’affichage des colonnes standard et personnalisées disponibles sur la page principale et des boutons d’action rapide dans chaque ligne, tels que [!UICONTROL Pause] (afin que vous puissiez rapidement suspendre une publicité).

* **[!UICONTROL Frequency]:** Données pour chaque niveau de fréquence publicitaire de l’emplacement, notamment :
   * le niveau de fréquence des publicités (par exemple &quot;1&quot; pour toutes les instances où les utilisateurs ont vu une publicité une fois) ;
   * nombre estimé unique de périphériques/navigateurs ou de personnes (selon le [!UICONTROL Cross Device Level] spécifié pour la campagne) ayant reçu des impressions au niveau de fréquence spécifié
   * nombre estimé d’impressions au niveau de fréquence spécifié
   * la fréquence moyenne estimée pour le niveau de fréquence spécifié. Cette valeur est égale à (Impressions estimées)/(Uniques estimées).

* **[!UICONTROL Inventory]:** Informations sur toutes les offres ciblées par l’emplacement.

  L’onglet [!UICONTROL Inventory] permet de résoudre rapidement les problèmes en affichant des statistiques de performances, telles que [!UICONTROL Auctions], [!UICONTROL Bids] et [!UICONTROL Win Rate]. L’onglet comprend des fonctions de recherche et de filtrage, les mêmes options d’affichage des colonnes standard et personnalisées que celles disponibles sur la page principale, ainsi que des boutons d’action rapide dans chaque ligne, y compris [!UICONTROL Edit], [!UICONTROL View Report] et [[!UICONTROL Auction Insights] pour un dépannage supplémentaire](/help/dsp/inventory/private-deal-auction-insights.md).

## Ouvrez le [!UICONTROL Placement Inspector]

1. Ouvrez la vue des emplacements pour la campagne ou le package parent :

   * Afficher tous les emplacements dans la campagne parente :

      1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

      1. Cliquez sur le nom de la campagne.

      1. Cliquez sur l’onglet **[!UICONTROL Placements]** .

   * Afficher tous les emplacements dans le package parent :

      1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

      1. Cliquez sur le nom de la campagne.

      1. Cliquez sur l’onglet **[!UICONTROL Packages]** .

      1. Cliquez sur le nom du package parent.

1. Placez le curseur sur la ligne d’emplacement, cliquez sur **[!UICONTROL More]**, puis cliquez sur une option :

   * Pour afficher tous les sites ciblés par l’emplacement, cliquez sur **[!UICONTROL Sites]**.

   * Pour afficher toutes les publicités de l’emplacement, cliquez sur **[!UICONTROL Ads]**.

   * Pour afficher les données de fréquence de l’emplacement, cliquez sur **[!UICONTROL Frequency]**.

   * Pour afficher toutes les offres que le placement cible, cliquez sur **[!UICONTROL Inventory]**.

1. (Facultatif) [Modifiez le mode Colonne](campaign-data-views-manage.md#column-view-change) si nécessaire pour afficher les mesures requises.

1. (Facultatif) Pour exporter les données sur n’importe quel onglet, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") dans le coin supérieur droit, puis cliquez sur **[!UICONTROL Export]**.

   Les données sont enregistrées dans le dossier de téléchargement par défaut de votre navigateur sous la forme d’un rapport au format XLSM.

## Dépannage de l’inventaire

| Problème | Cause possible | Actions à entreprendre |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | L’éditeur n’a pas commencé à envoyer de requêtes d’offre. | Contactez l’éditeur pour activer l’opération. |
| | L’opération a été mal configurée, par exemple en saisissant un identifiant d’opération externe incorrect. | Confirmez les détails de l’opération et modifiez-la. |
| [!UICONTROL Auctions but no Bids] | Le ciblage de l’emplacement ne correspond pas aux requêtes d’offre entrantes pour l’opération. <br><br> Par exemple, un emplacement peut cibler une zone géographique qui n’est pas éligible à l’opération. | Modifiez les cibles d’emplacement selon les besoins afin d’éviter les non-correspondances de ciblage. |
| | L’emplacement ne comporte pas de publicité active avec le type de média requis pour l’opération. | Créez et joignez une publicité avec le type de média approprié à l’emplacement. |
| | Le placement n&#39;a pas le budget adéquat. | Augmentez le budget d’emplacement afin d’autoriser l’enchère sur les requêtes entrantes. |
| | Les dates de vol de placement ne chevauchent pas les dates de remise de l’impression pour l’opération. | Modifiez les dates de vol de l’emplacement selon les besoins. |
| [!UICONTROL Low Win Rate] | L’offre maximale de l’emplacement (plancher ou fixe) est inférieure au minimum requis par l’offre. | Augmentez le [!UICONTROL Max Bid] de l’emplacement selon les besoins. |
| | L’emplacement utilise des filtres avant offre qui limitent l’offre. | Réduisez les seuils des filtres pré-enchère pour autoriser plus d’offres. |
| | Le ciblage de l’audience pour l’emplacement est trop restrictif. | Vérifiez si les cibles d’audience spécifiées disposent de suffisamment d’utilisateurs actifs et développez l’audience si possible. |

>[!MORELIKETHIS]
>
>* [Types de rapports de performances dans les vues Campaign Management](campaign-reports-about.md)
>* [Gérer vos vues de données de campagne](campaign-data-views-manage.md)
