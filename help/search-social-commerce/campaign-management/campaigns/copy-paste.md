---
title: Créer et modifier des données de campagne en bloc à l’aide du copier-coller
description: Découvrez comment gérer les données de campagne en bloc à l’aide de la fonctionnalité de copier-coller.
exl-id: 2ae1b02f-46ac-4ea8-aa9f-9e26ccaf63d0
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# Créer et modifier des données de campagne en bloc à l’aide du copier-coller

Comptes *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex] et [!DNL Baidu] existants uniquement*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads] vues*

Vous pouvez copier jusqu’à 10 000 lignes des vues [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads], puis les coller dans [!DNL Microsoft Excel] ou un autre éditeur pour modifier les champs n’ayant pas d’ID. Vous pouvez ensuite copier les lignes [!DNL Excel] et les coller à nouveau dans la vue sous forme de données séparées par des tabulations pour y apporter les modifications. Cette fonction utilise le presse-papiers de votre ordinateur.

Vous pouvez utiliser cette fonctionnalité pour modifier des objets Campaign existants (avec des champs d’identifiant) et pour créer de nouveaux objets Campaign sans champs d’identifiant.

## Copier les lignes de données

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] * [!UICONTROL Keywords] * [!UICONTROL Ads]\]**

1. Cochez la case en regard de chaque ligne à copier.

   Vous pouvez copier jusqu’à 10 000 lignes.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus"), puis sur **[!UICONTROL Copy]**.

   Vous pouvez également utiliser la commande de clavier « copier » de vos systèmes d’exploitation, par exemple **[!DNL Ctrl+C]** pour [!DNL Microsoft Windows] ou **[!DNL Command-C]** pour [!DNL Apple Mac].

1. Dans la boîte de dialogue [!UICONTROL Copy to Clipboard], cliquez sur **[!UICONTROL Continue]**. Lorsque les données sont prêtes à être copiées, cliquez sur **[!UICONTROL Copy]**.

1. Collez les lignes dans [!DNL Excel] ou un autre éditeur.

## Modifier et créer des lignes de données

1. Modifiez les données en fonction des exigences suivantes :

   * Les données collées doivent inclure une ligne d’en-tête et les valeurs d’objet de campagne nécessaires. Consultez les colonnes de la feuille d’envoi groupé requises pour [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo ! Réseau Display](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo ! Japon](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md) et [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). L&#39;ordre des colonnes importe peu.

      * Pour les objets existants que vous souhaitez modifier, vous devez inclure toutes les colonnes d’identifiant pertinentes, les noms d’entité et l’attribut à modifier. Ne modifiez pas l’ID numérique de l’objet.

      * Pour les nouveaux objets Campaign, incluez tous les noms et attributs d’entité pertinents, mais n’incluez pas les identifiants d’objet (qui sont générés automatiquement). Par exemple, si vous créez une annonce, laissez le champ [!UICONTROL Ad ID] vide. Le réseau publicitaire crée automatiquement un identifiant lorsque vous publiez l’objet .

   * La valeur de toute colonne non obligatoire peut être nulle (vide), mais chaque ligne doit comporter le même nombre de valeurs séparées par des tabulations.

1. Enregistrez les données en tant que valeurs séparées par des tabulations.

## Coller des lignes de données dans les vues de gestion de campagne

>[!NOTE]
>
>Si les lignes collées contiennent des données identiques à celles des entités existantes ou qui dupliquent une entité existante, les données en double sont ignorées.

1. Dans [!DNL Excel] ou un autre éditeur, copiez les lignes pertinentes séparées par des tabulations.

1. Dans le menu principal Search, Social et Commerce, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Ouvrez la vue dans laquelle coller les données (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] * [!UICONTROL Keywords] * [!UICONTROL Ads]\]**).

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus"), puis sur **[!UICONTROL Paste]**.

   Vous pouvez également utiliser la commande de clavier « coller » de vos systèmes d’exploitation, par exemple **[!DNL Ctrl+V]** pour [!DNL Microsoft Windows] ou **[!DNL Command-V]** pour [!DNL Apple Mac].

1. Collez les données dans la zone de saisie, puis cliquez sur **[!UICONTROL Process]**.

1. (Facultatif) Saisissez des détails supplémentaires :

   * (Si **[!UICONTROL Additional Details]** est compressé) Cliquez sur ![Ouvrir](/help/search-social-commerce/assets/chevron-up.png "Ouvrir") pour développer les détails.

   * Saisissez un **[!UICONTROL Job Name]** facultatif et/ou un **[!UICONTROL Job Description]** facultatif.

1. Cliquez sur **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l&#39;aide de feuilles d&#39;envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Modifier les paramètres directement dans une ligne](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Gérer les campagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Gérer les groupes publicitaires](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Gérer les mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Gérer les publicités](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)
