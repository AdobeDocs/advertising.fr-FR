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

Lorsque vous propagez des données de flux sans les publier simultanément sur le réseau publicitaire, vous pouvez modifier les données de l’une des façons suivantes. Vous pouvez éventuellement [post data](propagated-data-post.md) de chaque emplacement aux réseaux publicitaires appropriés :

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate and Preview],&quot; vous pouvez ensuite modifier le fichier de feuille d’envoi groupé généré (appelé &quot;`<feed file name>_<template name>`&quot;) en le téléchargeant à partir de la fonction [!UICONTROL Bulksheets] visualisez, modifiez le fichier, puis chargez-le à nouveau. Aucune donnée n’est incluse dans la variable [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets.

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate only],&quot; vous pouvez ensuite modifier les données générées pour les composants avec l’événement [[!UICONTROL New] status](propagated-data-status.md) dans une vue hiérarchique de campagne à partir de la vue [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets.

  Les vues de hiérarchie de campagne affichent uniquement les données générées à partir du fichier de flux, et non les composants de compte existants. Une fois que les données d’un composant et que tous ses sous-composants sont publiés sur le réseau publicitaire, ils ne sont plus répertoriés dans la hiérarchie de la campagne.

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, qui s’ouvre sur le [!UICONTROL Templates] .

   1. (Facultatif) Pour afficher uniquement les composants de campagne créés pour un modèle spécifique :

      1. Cliquez sur le nom du modèle.

      1. Dans le [!UICONTROL Accounts] dans le volet de navigation de gauche, développez le noeud ad network et le noeud ad network account , puis cochez la case en regard du nom du modèle.

   1. Cliquez sur le bouton **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]**, ou **[!UICONTROL Ads]** selon les composants que vous souhaitez afficher.

      >[!NOTE]
      >
      >* À moins d’afficher les données d’un modèle spécifique, la variable [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] les onglets répertorient tous les groupes publicitaires, mots-clés et annonces créés à partir de tous les modèles et fichiers de flux. Groupes de produits utilisés pour [!DNL Google Ads] les publicités commerciales sont répertoriées dans la [!UICONTROL Keywords] .
      >* Pour afficher uniquement les sous-composants d’une campagne spécifique, commencez par afficher la variable [!UICONTROL Campaigns] . De même, pour afficher uniquement les sous-composants d’un groupe publicitaire spécifique, commencez par afficher la variable [!UICONTROL Ad Groups] .

   1. (Facultatif ; pour modifier des groupes publicitaires, des mots-clés ou des publicités uniquement) Filtrez la liste pour inclure uniquement les sous-composants d’une campagne ou d’un groupe publicitaire spécifique :

      * Pour répertorier tous les groupes publicitaires d’une campagne, cliquez sur le nom de la campagne.

      * Pour répertorier tous les mots-clés d’un groupe publicitaire, cliquez sur le nom du groupe publicitaire.

      * Pour répertorier tous les sous-titres d’un groupe publicitaire, cliquez sur le nom du groupe publicitaire, puis sur le [!UICONTROL Ads] .

   1. Cliquez sur [Icône Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Icône Afficher/modifier les paramètres") en regard de la campagne, du groupe publicitaire, du mot-clé ou du nom de la publicité.

   1. Modifiez les paramètres, puis cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Affichage des données générées à partir de flux](propagated-data-view.md)
>* [Données de campagne de publication générées à partir de flux vers les réseaux publicitaires](propagated-data-post.md)
>* [Arrêt d’une tâche de publication pour les données de flux d’inventaire](stop-job.md)
>* [Statuts des données générées à partir de flux](propagated-data-status.md)
