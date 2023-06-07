---
title: Affichage des données générées à partir de flux
description: Découvrez comment afficher les données générées à partir de flux de données d’inventaire.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Affichage des données générées à partir de flux

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Lorsque vous propagez des données de flux sans les publier simultanément sur le réseau publicitaire, vous pouvez prévisualiser les données de l’une des manières suivantes. Si vous le souhaitez, [post data](propagated-data-post.md) de chaque emplacement aux réseaux publicitaires appropriés.

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate and Preview],&quot; puis afficher la feuille d’envoi groupé générée (nommée &quot;`<feed file name>_<template name>`&quot;) de la fonction [!UICONTROL Bulksheets] vue. Aucune donnée n’est incluse dans la variable [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets. Cette option vous permet de [valider les landing pages ;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-validate-landing-pages.md) associés aux publicités et aux mots-clés avant de publier les données.

* Si vous avez utilisé l’option pour &quot;[!UICONTROL Propagate only]&quot;, puis affichez les données générées dans une vue hiérarchique de campagne à partir de la variable [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] onglets.

   Les vues de hiérarchie de campagne affichent uniquement les données générées à partir du fichier de flux, et non les composants de compte existants. Une fois que les données d’un composant et tous ses sous-composants sont publiés sur le réseau publicitaire, ils ne sont plus répertoriés dans la vue de hiérarchie de campagne.

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**, qui s’ouvre sur le [!UICONTROL Templates] .

   1. (Facultatif) Pour afficher uniquement les composants de campagne créés pour un modèle spécifique :

      1. Cliquez sur le nom du modèle.

      1. Dans le [!UICONTROL Accounts] dans le volet de navigation de gauche, développez le noeud ad network et le noeud ad network account , puis cochez la case en regard du nom du modèle.
   1. Cliquez sur le bouton **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]**, **[!UICONTROL Keywords]** ou **[!UICONTROL Ads]** selon les composants que vous souhaitez afficher.

      >[!NOTE]
      >
      >* À moins d’afficher les données d’un modèle spécifique, la variable [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] les onglets répertorient tous les groupes publicitaires, mots-clés et annonces créés à partir de tous les modèles et fichiers de flux. Groupes de produits utilisés pour [!DNL Google Ads] les publicités commerciales sont répertoriées dans la [!UICONTROL Keywords] .
      >* Pour afficher uniquement les sous-composants d’une campagne spécifique, commencez par afficher la variable [!UICONTROL Campaigns] . De même, pour afficher uniquement les sous-composants d’un groupe publicitaire spécifique, commencez par afficher la variable [!UICONTROL Ad Groups] .


   1. (Facultatif) Pour afficher des informations supplémentaires, effectuez l’une des opérations suivantes :

      * Pour afficher les paramètres d’une campagne, d’un groupe publicitaire, d’un mot-clé ou d’une publicité, cliquez sur [Icône Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Icône Afficher/modifier les paramètres") en regard du nom.

      * Pour afficher les sous-composants d’une campagne ou d’un groupe publicitaire, procédez comme suit :

         * Pour répertorier tous les groupes publicitaires d’une campagne, cliquez sur le nom de la campagne.

         * Pour répertorier tous les mots-clés ou cibles de produits d’un groupe publicitaire, cliquez sur le nom du groupe publicitaire.

         * Pour répertorier toutes les publicités d’un groupe, cliquez sur le nom du groupe, puis sur le bouton [!UICONTROL Ads] .


>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Modification des données générées à partir de flux](propagated-data-edit.md)
>* [Données de campagne de publication générées à partir de flux vers les réseaux publicitaires](propagated-data-post.md)
>* [Arrêt d’une tâche de publication pour les données de flux d’inventaire](stop-job.md)
>* [Statuts des données générées à partir de flux](propagated-data-status.md)
