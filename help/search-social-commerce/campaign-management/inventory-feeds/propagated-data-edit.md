---
title: Modification des données générées à partir de flux
description: Découvrez comment modifier les données générées à partir de flux de données d’inventaire.
exl-id: d43b593d-758d-4561-9cda-33b235099cc6
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Modification des données générées à partir de flux

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Lorsque vous propagez des données de flux sans les publier simultanément sur le réseau publicitaire, vous pouvez modifier les données de l’une des façons suivantes. Vous pouvez, par la suite, [publier des données](propagated-data-post.md) de n’importe quel emplacement vers les réseaux publicitaires appropriés :

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate and Preview]&quot;, vous pouvez modifier le fichier de feuille d’envoi groupé généré (appelé &quot;`<feed file name>_<template name>`&quot;) en le téléchargeant depuis la vue [!UICONTROL Bulksheets], en modifiant le fichier et en le chargeant à nouveau. Aucune donnée n’est incluse dans les onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate only]&quot;, vous pouvez modifier les données générées pour les composants ayant le statut [[!UICONTROL New]](propagated-data-status.md) dans une vue de hiérarchie de campagne à partir des onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads].

  Les vues de hiérarchie de campagne affichent uniquement les données générées à partir du fichier de flux, et non les composants de compte existants. Une fois que les données d’un composant et que tous ses sous-composants sont publiés sur le réseau publicitaire, ils ne sont plus répertoriés dans la hiérarchie de la campagne.

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

   1. (Facultatif) Pour afficher uniquement les composants de campagne créés pour un modèle spécifique :

      1. Cliquez sur le nom du modèle.

      1. Dans le menu [!UICONTROL Accounts] du volet de navigation de gauche, développez le noeud réseau publicitaire et le noeud de compte réseau publicitaire, puis cochez la case en regard du nom du modèle.

   1. Cliquez sur l’onglet **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** ou **[!UICONTROL Ads]** en fonction des composants que vous souhaitez afficher.

      >[!NOTE]
      >
      >* À moins que vous n’affichiez les données d’un modèle spécifique, les onglets [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads] répertorient tous les groupes publicitaires, mots-clés et annonces créés à partir de tous les modèles et fichiers de flux. Les groupes de produits utilisés pour les [!DNL Google Ads] publicités commerciales sont répertoriés dans l’onglet [!UICONTROL Keywords] .
      >* Pour afficher uniquement les sous-composants d’une campagne spécifique, commencez par afficher l’onglet [!UICONTROL Campaigns]. De même, pour afficher uniquement les sous-composants d’un groupe publicitaire spécifique, commencez par afficher l’onglet [!UICONTROL Ad Groups].

   1. (Facultatif ; pour modifier des groupes publicitaires, des mots-clés ou des publicités uniquement) Filtrez la liste pour inclure uniquement les sous-composants d’une campagne ou d’un groupe publicitaire spécifique :

      * Pour répertorier tous les groupes publicitaires d’une campagne, cliquez sur le nom de la campagne.

      * Pour répertorier tous les mots-clés d’un groupe publicitaire, cliquez sur le nom du groupe publicitaire.

      * Pour répertorier toutes les publicités comme dans un groupe publicitaire, cliquez sur le nom du groupe publicitaire, puis sur l’onglet [!UICONTROL Ads] .

   1. Cliquez sur [Icône Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Icône Afficher/modifier les paramètres") en regard de la campagne, du groupe publicitaire, du mot-clé ou du nom de la publicité.

   1. Modifiez les paramètres, puis cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Affichage des données générées à partir de flux](propagated-data-view.md)
>* [Données de campagne de publication générées à partir de flux vers les réseaux publicitaires](propagated-data-post.md)
>* [Arrêter une tâche de publication pour les données de flux d’inventaire](stop-job.md)
>* [États des données générées à partir de flux](propagated-data-status.md)
