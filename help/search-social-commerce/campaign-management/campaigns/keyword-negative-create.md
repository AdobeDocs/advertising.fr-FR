---
title: Créer des mots-clés négatifs
description: Découvrez comment créer des mots-clés négatifs pour les campagnes de recherche et les groupes publicitaires.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---

# Créer des mots-clés négatifs

*[!DNL Baidu], [!DNL Google Ads] et [!DNL Microsoft® Advertising], et [!DNL Yahoo! Japan Ads] comptes uniquement*

Vous pouvez créer des mots-clés négatifs pour un groupe publicitaire de recherche ou une campagne qui cible la recherche ou le réseau d’affichage/natif. Les mots-clés négatifs ne déclenchent pas de publicités.

>[!NOTE]
>Vous pouvez également créer et modifier des mots-clés négatifs dans la variable [paramètres du groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) et [paramètres de campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Pour créer plusieurs mots-clés négatifs à la fois, utilisez [feuilles d’envoi groupé de campagnes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer"), puis cliquez sur **[!UICONTROL Campaign]** pour créer des mots-clés négatifs au niveau de la campagne ou **[!UICONTROL Ad Group]** pour créer des mots-clés négatifs au niveau du groupe publicitaire.

1. Sélectionnez le réseau publicitaire, le compte, la campagne et (le cas échéant) le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Saisissez les mots-clés négatifs. Utilisez la syntaxe suivante, sans signe moins (`-`) :

   * Correspondance large négative : `keyword` (non pris en charge par [!DNL Microsoft® Advertising])

   * Correspondance d’expression négative : `"keyword"`

   * Correspondance exacte négative : `[keyword]`

   Séparez plusieurs valeurs par des virgules ou saisissez-les sur des lignes distinctes. Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés négatifs en une seule opération. Voir également les exigences et restrictions suivantes :

   * Longueur maximale des caractères : [!DNL Baidu]: 30 sur un ou 15 sur deux octets ; [!DNL Microsoft® Advertising]: 100 sur un ou 50 sur deux octets ; [!DNL Google Ads] et [!DNL Yahoo! Japan Ads]: 80 sur un ou 40 sur deux octets.

   * [!DNL Baidu] n’autorise qu’un seul type de correspondance par mot-clé par groupe publicitaire. Par exemple, le groupe d’annonces 1 ne peut pas inclure les deux `"keyword"` et `[keyword]`.

   * [!DNL Google Ads]: Chaque mot-clé ne peut pas contenir plus de 10 mots et ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : space `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]: Chaque mot-clé peut contenir, au maximum, sept mots, à l’exception des mots-clés &quot;stop&quot;. Chaque [!DNL Yandex ad group] peut contenir un maximum de 200 mots-clés.


1. Cliquez sur **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [A propos des mots-clés](keyword-about.md)
>* [Gestion des mots-clés pouvant faire l’objet d’un offre](keyword-manage.md)
>* [Modifier l’état des mots-clés et des mots-clés négatifs](keyword-status-edit.md)

