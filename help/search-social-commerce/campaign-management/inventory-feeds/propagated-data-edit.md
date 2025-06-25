---
title: Modifier les données générées à partir des flux
description: Découvrez comment modifier les données générées à partir des flux de données d’inventaire.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Modifier les données générées à partir des flux

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Lorsque vous propagez des données de flux sans les publier simultanément sur le réseau publicitaire, vous pouvez modifier les données de l’une des manières suivantes. Vous pouvez ensuite [publier](propagated-data-post.md) de l’un des emplacements aux réseaux publicitaires appropriés :

* Si vous avez utilisé l’option « [!UICONTROL Propagate and Preview] », vous pouvez modifier le fichier de feuille d’envoi groupé généré (nommé « `<feed file name>_<template name>` ») en le téléchargeant à partir de la vue [!UICONTROL Bulksheets], en modifiant le fichier et en le chargeant à nouveau. Aucune donnée n’est incluse dans les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

* Si vous avez utilisé l’option « [!UICONTROL Propagate only] », vous pouvez modifier les données générées pour les composants avec le statut [[!UICONTROL New]](propagated-data-status.md) dans une vue de hiérarchie de campagne à partir des onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

  Les vues de hiérarchie de la campagne affichent uniquement les données générées à partir du fichier de flux, et non les composants de compte existants. Une fois les données d’un composant et de tous ses sous-composants publiées sur le réseau publicitaire, elles ne sont plus répertoriées dans la hiérarchie de la campagne.

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

   1. (Facultatif) Pour afficher uniquement les composants de campagne créés pour un modèle spécifique :

      1. Cliquez sur le nom du modèle.

      1. Dans le menu [!UICONTROL Accounts] du volet de navigation de gauche, développez le nœud de réseau publicitaire et le nœud de compte de réseau publicitaire, puis cochez la case en regard du nom du modèle.

   1. Cliquez sur l’onglet **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** ou **[!UICONTROL Ads]** , selon les composants que vous souhaitez afficher.

      >[!NOTE]
      >
      >* À moins que vous n’affichiez des données pour un modèle spécifique, les onglets [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads] répertorient tous les groupes publicitaires, mots-clés et publicités créés à partir de tous les modèles et fichiers de flux. Les groupes de produits utilisés pour les annonces d’achats [!DNL Google Ads] sont répertoriés dans l’onglet [!UICONTROL Keywords] .
      >* Pour afficher uniquement les sous-composants d’une campagne spécifique, commencez par consulter l’onglet [!UICONTROL Campaigns] . De même, pour afficher uniquement les sous-composants d’un groupe publicitaire spécifique, commencez par afficher l’onglet [!UICONTROL Ad Groups] .

   1. (Facultatif ; pour modifier uniquement des groupes publicitaires, des mots-clés ou des annonces) Filtrez la liste afin d’inclure uniquement les sous-composants d’une campagne ou d’un groupe publicitaire spécifique :

      * Pour répertorier tous les groupes publicitaires d’une campagne, cliquez sur le nom de la campagne.

      * Pour répertorier tous les mots-clés d’un groupe publicitaire, cliquez sur le nom du groupe publicitaire.

      * Pour répertorier toutes les publicités comme dans un groupe publicitaire, cliquez sur le nom du groupe publicitaire, puis cliquez sur l’onglet [!UICONTROL Ads] .

   1. Cliquez sur [icône Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Icône Afficher/modifier les paramètres") en regard de la campagne, du groupe publicitaire, du mot-clé ou du nom de l’annonce.

   1. Modifiez les paramètres, puis cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Afficher les données générées à partir des flux](propagated-data-view.md)
>* [Publier les données de campagne générées à partir des flux sur les réseaux publicitaires](propagated-data-post.md)
>* [Arrêter un traitement de validation des données de flux de stock](stop-job.md)
>* [États des données générées à partir des flux](propagated-data-status.md)
