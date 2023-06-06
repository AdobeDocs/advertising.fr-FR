---
title: Créer et modifier des données de campagne en bloc à l’aide de la fonction copier-coller
description: Découvrez comment gérer les données de campagne en bloc à l’aide de la fonction copier-coller.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 0%

---

# Créer et modifier des données de campagne en bloc à l’aide de la fonction copier-coller

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], et [!DNL Yandex] comptes uniquement*

*[!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] views*

Vous pouvez copier jusqu’à 10 000 lignes du [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords], et [!UICONTROL Ads] visualisez et collez-les dans [!DNL Microsoft Excel] ou un autre éditeur pour modifier des champs non ID. Vous pouvez ensuite copier la variable [!DNL Excel] lignes et collez-les sous forme de données séparées par des tabulations dans la vue pour effectuer les modifications. Cette fonctionnalité utilise le Presse-papiers de votre ordinateur.

Vous pouvez utiliser cette fonction pour modifier des objets de campagne existants (avec des champs d’identifiant) et créer de nouveaux objets de campagne sans champs d’identifiant.

## Copie de lignes de données

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**.

1. Cochez la case en regard de chaque ligne à copier.

   Vous pouvez copier jusqu’à 10 000 lignes.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus"), puis cliquez sur **[!UICONTROL Copy]**.

   Vous pouvez également utiliser la commande de clavier &quot;copy&quot; de votre système d’exploitation, telle que **[!DNL Ctrl+C]** pour [!DNL Microsoft Windows] ou **[!DNL Command-C]** pour [!DNL Apple Mac].

1. Dans le [!UICONTROL Copy to Clipboard] boîte de dialogue, cliquez sur **[!UICONTROL Continue]**. Lorsque les données sont prêtes à être copiées, cliquez sur **[!UICONTROL Copy]**.

1. Collez les lignes dans [!DNL Excel] ou un autre éditeur.

## Modifier et créer des lignes de données

1. Modifiez les données en fonction des exigences suivantes :

   * Les données collées doivent inclure une rangée d’en-tête et les valeurs d’objet de campagne nécessaires. voir les colonnes de la feuille de support pour [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Publicités Google](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [Publicité Microsoft](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo ! Réseau d’affichage](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md), [Yahoo ! Japon](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), et [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md). L&#39;ordre des colonnes n&#39;a pas d&#39;importance.

      * Pour les objets existants que vous souhaitez modifier, vous devez inclure toutes les colonnes d’ID, les noms d’entité et l’attribut à modifier. Ne modifiez pas l’identifiant numérique de l’objet.

      * Pour les nouveaux objets de campagne, incluez tous les noms et attributs d’entité pertinents, mais n’incluez pas d’ID d’objet (qui sont générés automatiquement). Par exemple, si vous créez une publicité, laissez le champ [!UICONTROL Ad ID] champ vide. Le réseau publicitaire crée automatiquement un identifiant lorsque vous publiez l’objet.
   * La valeur de toute colonne non requise peut être nulle (vide), mais chaque ligne doit comporter le même nombre de valeurs séparées par des tabulations.


1. Enregistrez les données en tant que valeurs séparées par des tabulations.

## Collez des lignes de données dans les vues de gestion de campagne.

>[!NOTE]
>
>Si les lignes collées contiennent des données identiques à celles des entités existantes ou qui dupliquent une entité existante, les données en double sont ignorées.

1. Dans [!DNL Excel] Pour tout autre éditeur, copiez les lignes appropriées séparées par des tabulations.

1. Dans le menu principal Rechercher, Social et commerce, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Ouvrez la vue dans laquelle coller les données (**[!UICONTROL Live]> \[[!UICONTROL Campaigns] \| [!UICONTROL Ad Groups] \| [!UICONTROL Keywords] \| [!UICONTROL Ads]\]**).

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus"), puis cliquez sur **[!UICONTROL Paste]**.

   Vous pouvez également utiliser la commande de clavier &quot;Coller&quot; de votre système d’exploitation, telle que **[!DNL Ctrl+V]** pour [!DNL Microsoft Windows] ou **[!DNL Command-V]** pour [!DNL Apple Mac].

1. Collez les données dans la zone de saisie, puis cliquez sur **[!UICONTROL Process]**.

1. (Facultatif) Saisissez des détails supplémentaires :

   * (Si **[!UICONTROL Additional Details]** est compressé) Cliquez sur ![Ouvrir](/help/search-social-commerce/assets/chevron-up.png "Ouvrir") pour développer les détails.

   * Saisissez un **[!UICONTROL Job Name]** et/ou facultatif **[!UICONTROL Job Description]**.

1. Cliquez sur **[!UICONTROL Post Now]**.


>[!MORELIKETHIS]
>
>* [A propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [Modifier les paramètres directement dans une ligne](/help/search-social-commerce/common-tasks/settings-edit-within-row.md)
>* [Gestion des campagnes](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)
>* [Gestion des groupes d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
>* [Gestion des mots-clés](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
>* [Gestion des publicités](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)

