---
title: Afficher les données générées à partir des flux
description: Découvrez comment afficher les données générées à partir des flux de données d’inventaire.
exl-id: ee48f0f1-65fb-4d27-8f59-0108835d70e5
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/AG-bR4RcQZcDjJTLkrWhC4J3RcYb7kBRRiC3moSCxp0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 429
ht-degree: 0%

---

# Afficher les données générées à partir des flux

comptes *[!DNL Google Ads], [!DNL LY Ads] (actions de suppression uniquement), [!DNL Microsoft Advertising] et [!DNL Yandex] uniquement*

Lorsque vous propagez des données de flux sans les publier simultanément sur le réseau publicitaire, vous pouvez prévisualiser les données de l’une des manières suivantes. Vous pouvez ensuite [publier](propagated-data-post.md) de l’un des emplacements vers les réseaux publicitaires appropriés.

* Si vous avez utilisé l’option « [!UICONTROL Propagate and Preview] », affichez la feuille d’envoi groupé générée (nommée « `<feed file name>_<template name>` ») depuis la vue [!UICONTROL Bulksheets]. Aucune donnée n’est incluse dans les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads]. Cette option vous permet de [valider les landing pages](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) associées aux annonces et aux mots-clés avant de publier les données.

* Si vous avez utilisé l’option « [!UICONTROL Propagate only] », affichez les données générées dans une vue de hiérarchie de campagne à partir des onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

  Les vues de hiérarchie de la campagne affichent uniquement les données générées à partir du fichier de flux, et non les composants de compte existants. Une fois les données d’un composant et de tous ses sous-composants publiées sur le réseau publicitaire, elles ne sont plus répertoriées dans la vue hiérarchique de la campagne.

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

   1. (Facultatif) Pour afficher uniquement les composants de campagne créés pour un modèle spécifique :

      1. Cliquez sur le nom du modèle.

      1. Dans le menu [!UICONTROL Accounts] du volet de navigation de gauche, développez le nœud de réseau publicitaire et le nœud de compte de réseau publicitaire, puis cochez la case en regard du nom du modèle.

   1. Cliquez sur l’onglet **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** ou **[!UICONTROL Ads]** , selon les composants que vous souhaitez afficher.

      >[!NOTE]
      >
      >* À moins que vous n’affichiez des données pour un modèle spécifique, les onglets [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads] répertorient tous les groupes publicitaires, mots-clés et publicités créés à partir de tous les modèles et fichiers de flux. Les groupes de produits utilisés pour les annonces d’achats [!DNL Google Ads] sont répertoriés dans l’onglet [!UICONTROL Keywords] .
      >* Pour afficher uniquement les sous-composants d’une campagne spécifique, commencez par consulter l’onglet [!UICONTROL Campaigns] . De même, pour afficher uniquement les sous-composants d’un groupe publicitaire spécifique, commencez par afficher l’onglet [!UICONTROL Ad Groups] .

   1. (Facultatif) Pour afficher des informations supplémentaires, effectuez l’une des opérations suivantes :

      * Pour afficher les paramètres d’une campagne, d’un groupe publicitaire, d’un mot-clé ou d’une annonce, cliquez sur [icône Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Icône Afficher/modifier les paramètres") en regard du nom.

      * Pour afficher les sous-composants d’une campagne ou d’un groupe publicitaire, procédez comme suit :

         * Pour répertorier tous les groupes publicitaires d’une campagne, cliquez sur le nom de la campagne.

         * Pour répertorier tous les mots-clés ou cibles de produit dans un groupe publicitaire, cliquez sur le nom du groupe publicitaire.

         * Pour répertorier toutes les publicités d’un groupe publicitaire, cliquez sur le nom du groupe publicitaire, puis cliquez sur l’onglet [!UICONTROL Ads] .

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Modifier les données générées à partir des flux](propagated-data-edit.md)
>* [Publier les données de campagne générées à partir des flux sur les réseaux publicitaires](propagated-data-post.md)
>* [Arrêter un traitement de validation des données de flux de stock](stop-job.md)
>* [États des données générées à partir des flux](propagated-data-status.md)
