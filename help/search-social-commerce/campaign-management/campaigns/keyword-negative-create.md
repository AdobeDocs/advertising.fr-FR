---
title: Créer des mots-clés négatifs
description: Découvrez comment créer des mots-clés négatifs pour les campagnes de recherche et les groupes publicitaires.
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# Créer des mots-clés négatifs

Comptes *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] et [!DNL Baidu] existants uniquement*

Vous pouvez créer des mots-clés négatifs pour un groupe publicitaire ou une campagne de recherche qui cible la recherche ou le réseau d’affichage/natif. Les mots-clés négatifs ne déclenchent pas de publicités.

>[!NOTE]
>Vous pouvez également créer et modifier des mots-clés négatifs dans les [paramètres du groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) et [paramètres de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>Pour créer plusieurs mots-clés négatifs à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer"), puis sur **[!UICONTROL Campaign]** pour créer des mots-clés négatifs au niveau de la campagne ou sur **[!UICONTROL Ad Group]** pour créer des mots-clés négatifs au niveau du groupe publicitaire.

1. Sélectionnez le réseau publicitaire, le compte, la campagne et (le cas échéant) le groupe publicitaire, puis cliquez sur **[!UICONTROL Continue]**.

1. Saisissez les mots-clés négatifs. Utilisez la syntaxe suivante, sans signe moins (`-`) :

   * Correspondance large négative : `keyword` (non prise en charge par [!DNL Microsoft Advertising])

   * Correspondance de l’expression négative : `"keyword"`

   * Correspondance exacte négative : `[keyword]`

   Séparez plusieurs valeurs par des virgules ou saisissez-les sur des lignes distinctes. Vous pouvez saisir ou coller jusqu’à 2 000 mots-clés négatifs en une seule opération. Consultez également les exigences et restrictions suivantes :

   * Longueur maximale des caractères : [!DNL Baidu] : 30 octets simples ou 15 octets doubles ; [!DNL Microsoft Advertising] : 100 octets simples ou 50 octets doubles ; [!DNL Google Ads] et [!DNL Yahoo! Japan Ads] : 80 octets simples ou 40 octets doubles.

   * [!DNL Baidu] n’autorise qu’un seul type de correspondance par mot-clé par groupe publicitaire. Par exemple, le groupe publicitaire 1 ne peut pas inclure à la fois `"keyword"` et `[keyword]`.

   * [!DNL Google Ads] : chaque mot-clé ne peut pas comporter plus de 10 mots et ne peut contenir que des lettres, des chiffres et les caractères spéciaux suivants : espace `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex] : chaque mot-clé peut contenir un maximum de sept mots, à l’exclusion des mots vides. Chaque [!DNL Yandex ad group] peut inclure un maximum de 200 mots-clés.

1. Cliquez sur **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [À propos des mots-clés](keyword-about.md)
>* [Gérer les mots-clés pouvant faire l’objet d’une offre](keyword-manage.md)
>* [Modifier le statut des mots-clés et des mots-clés négatifs](keyword-status-edit.md)
