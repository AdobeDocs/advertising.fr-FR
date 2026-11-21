---
title: (Nouvelle interface utilisateur) Répliquer des campagnes Google Ads dans Microsoft Advertising
description: Découvrez comment exporter vos campagnes synchronisées dans un compte Google Ads directement vers un compte Microsoft Advertising synchronisé.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '987'
ht-degree: 0%
---
# (Nouvelle interface utilisateur) Répliquer [!DNL Google Ads] campagnes dans [!DNL Microsoft Advertising]

*Fonctionnalité Beta*

Vous pouvez exporter vos campagnes synchronisées dans un compte [!DNL Google Ads] directement vers un compte [!DNL Microsoft Advertising] synchronisé en tant que campagnes CPC améliorées (eCPC). Les offres existantes et les budgets de campagne sont mis à l’échelle. Le suivi Search, Social et Commerce existant n’est pas importé.

Vous pouvez répliquer les types de campagne suivants et leur structure :

* [!DNL Google Ads] rechercher et afficher des campagnes dans [!DNL Microsoft Advertising] rechercher et afficher des campagnes.

* [!DNL Google Display Network] campagnes, y compris des images publicitaires, dans [!DNL Microsoft Advertising] campagnes d’audience sur le réseau d’audiences Microsoft.

  Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achats, répliquez d’abord vos [!DNL Google Merchant Center] offres de produits vers [!DNL Microsoft Merchant Center]. Lorsque vous répliquez les campagnes, sélectionnez le magasin [!DNL Microsoft Merchant Center] dans les options d’importation pour le lier à vos campagnes d’audience basées sur les flux.

* [!DNL Google Ads] campagnes de performance max, y compris les annonces d’inventaire local, en [!DNL Microsoft Advertising] campagnes de performance max.

Vous pouvez choisir de mettre à jour les campagnes une fois ; tous les jours, toutes les semaines ou tous les mois ; ou selon le planning recommandé par [!DNL Microsoft Advertising]. Vous pouvez éventuellement configurer des notifications chaque fois qu’une tâche d’importation s’exécute ou que des erreurs ou des modifications se produisent. Une fois que vous avez importé vos campagnes dans [!DNL Microsoft Advertising], vous pouvez vérifier le statut de votre tâche d’importation, consulter les journaux d’erreur, exécuter manuellement une tâche d’importation et modifier, suspendre, activer ou supprimer votre planning d’importation.

Toutes les informations de campagne ne sont pas répliquées, et vous devrez peut-être ajouter certaines informations à vos campagnes [!DNL Microsoft Advertising]. Pour plus d&#39;informations sur les données importées, consultez l&#39;aide de [!DNL Microsoft Advertising] sur « [Ce qui est importé de [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851){target="_blank"} ». Comme le suivi des moteurs de recherche, des réseaux sociaux et de Commerce n’est pas importé, vous devez également ajouter le suivi dans les paramètres [compte](/help/search-social-commerce/legacy-ui/campaign-management/accounts/ad-network-account-manage.md), [campagne](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/campaign-manage.md), [groupe publicitaire](/help/search-social-commerce/manage/campaigns/campaign-manage.md) ou [publicité](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/ad-manage.md).

## Répliquer [!DNL Google Ads] campagnes

>[!NOTE]
>
>Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achats, commencez par [répliquer vos [!DNL Google Merchant Center] offres de produits dans [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870){target="_blank"}. Lorsque vous répliquez les campagnes, sélectionnez le magasin [!DNL Microsoft Merchant Center] dans les options d’importation pour le lier à vos campagnes d’audience basées sur les flux.

Voir [ce qui est importé des [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Au-dessus de la liste des campagnes, cliquez sur **[!UICONTROL Import Campaigns]**.

1. Cliquez sur **[!UICONTROL + Import Campaigns]**.

1. Spécifiez les [paramètres d&#39;importation](#campaign-import-settings).

1. Cliquez sur **[!UICONTROL Review and Save]** en haut à droite.

1. Vérifiez vos sélections dans le résumé et cliquez sur **[!UICONTROL Start Import]**.

1. (Facultatif) Ajoutez le suivi Search, Social et Commerce dans les paramètres [compte](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md), [campagne](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/campaign-manage.md), [groupe publicitaire](/help/search-social-commerce/manage/campaigns/campaign-manage.md) ou [publicité](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/ad-manage.md).

## Modifier les paramètres de planning d’un traitement d’import de campagne

Voir [ce qui est importé des [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Au-dessus de la liste des campagnes, cliquez sur **[!UICONTROL Import Campaigns]**.

1. Sous l&#39;onglet **[!UICONTROL List of Import Jobs]**, cliquez sur le nom de la tâche d&#39;importation, puis cliquez sur **[!UICONTROL Edit]**.

1. À l’étape **[!UICONTROL Set schedule]**, spécifiez les [paramètres de planification](#campaign-import-settings).

1. Cliquez sur **[!UICONTROL Save]**.

## Affichage des traitements d’import de campagne

Vous pouvez répertorier toutes les tâches d’importation, y compris le compte [!DNL Google Ads] source, le compte [!DNL Microsoft Advertising] cible, l’heure ou le planning d’importation et l’utilisateur ou l’utilisatrice qui a créé la tâche. Lorsque vous exécutez une tâche d’importation plusieurs fois, y compris lors d’importations planifiées régulièrement, chaque occurrence est répertoriée comme une tâche distincte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Au-dessus de la liste des campagnes, cliquez sur **[!UICONTROL Import Campaigns]**.

   Par défaut, la vue s’ouvre sur l’onglet **[!UICONTROL List of Import Jobs]**.

## Exécution d’un traitement d’import de campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Au-dessus de la liste des campagnes, cliquez sur **[!UICONTROL Import Campaigns]**.

1. Dans l&#39;onglet **[!UICONTROL List of Import Jobs]**, cochez la case en regard de la tâche d&#39;importation, puis cliquez sur **[!UICONTROL Run Now]**.

## Afficher les journaux de vos traitements d’import de campagne {#campaign-import-log}

Vous pouvez répertorier toutes les tâches d’importation terminées ou ayant échoué, y compris l’heure de début, le compte [!DNL Google Ads] source, le compte [!DNL Microsoft Advertising] cible, l’utilisateur ou l’utilisatrice qui a créé la tâche, le nombre d’opérations réussies et ayant échoué et les adresses e-mail qui ont reçu des notifications pour chaque tâche. Vous pouvez afficher des détails supplémentaires sur les modifications apportées au compte [!DNL Microsoft Advertising] de la cible pour chaque tâche, y compris le nombre d’éléments ajoutés, synchronisés, supprimés et qui ont généré des erreurs pour chaque niveau d’entité (campagne ou mot-clé, par exemple) dans le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Campaigns]**.

1. Au-dessus de la liste des campagnes, cliquez sur **[!UICONTROL Import Campaigns]**.

1. Cliquez sur l’onglet **[!UICONTROL Import Logs]**.

1. (Facultatif) Pour afficher les détails d’une tâche d’importation, cliquez sur la valeur de la colonne [!UICONTROL Summary].

## Paramètres des traitements d&#39;import Campaign {#campaign-import-settings}

### Onglet [!UICONTROL Select Accounts]

**[!UICONTROL Import Name]:** Nom permettant d’identifier la tâche d’importation.

**[!UICONTROL Source Google Ads account]:** Compte [!DNL Google Ads] synchronisé à partir duquel les données de campagne sont exportées.

**[!UICONTROL Target Microsoft Ads account]:** Compte [!DNL Microsoft Advertising] synchronisé dans lequel les données de campagne sont importées.

**[!UICONTROL Credential ID]:** Identifiant utilisé par [!DNL Microsoft Advertising] pour représenter vos informations d’identification [!DNL Google Ads]. La génération automatique des informations d&#39;identification [!DNL Microsoft Advertising] pour l&#39;importation n&#39;est pas disponible en raison des limitations [!DNL Microsoft Advertising]. Contactez l’équipe chargée de votre compte Adobe. Elle générera les informations d’identification et vous donnera l’identifiant.

### Onglet [!UICONTROL Select Campaigns & Ad Groups]

**\[Données à importer\]:** Données à importer :

* *[!UICONTROL Import all new and existing campaigns]:* Pour importer les données de toutes les campagnes qui existent déjà et de celles qui n’existent pas dans [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Pour sélectionner des campagnes et des groupes publicitaires spécifiques.

  * Pour développer une campagne dans ses groupes d’annonces enfants, cliquez sur **[!UICONTROL >]** après le nom de la campagne.

  * Pour sélectionner une campagne ou un groupe publicitaire, sélectionnez l’élément afin qu’une coche s’affiche.

  * Pour supprimer une campagne ou un groupe publicitaire, désélectionnez l’élément ou cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") dans la colonne [!UICONTROL Selection].

### Onglet [!UICONTROL Customize Your Import]

**[!UICONTROL Choose specific import options]:** vous permet de spécifier les éléments à importer, les offres et les budgets, ainsi que d&#39;autres options.

**[!UICONTROL What to import]:** définit les éléments à importer. Les options permettant d&#39;importer des catégories d&#39;articles sont sélectionnées par défaut, tous les types d&#39;articles étant sélectionnés. Pour inclure uniquement des types d’éléments spécifiques, cliquez sur **[!UICONTROL Show advanced options]** et modifiez les types d’éléments pour inclure. Vous pouvez également associer un ID de balise UET à une liste de remarketing ou à une audience qui n&#39;a pas encore été importée dans [!DNL Microsoft Advertising].

**[!UICONTROL Bids and budgets]:** définit les paramètres d&#39;enchères et de budget à importer, mettre à jour et personnaliser, y compris les options permettant d&#39;augmenter ou de réduire les enchères et les budgets d&#39;un pourcentage spécifié pour [!DNL Microsoft Advertising].

**[!UICONTROL Other options]:** définit comment gérer les URL de page de destination importées, les modèles de suivi et d’autres options de campagne, d’annonce et de ciblage, y compris les options permettant de rechercher et de remplacer du texte et d’insérer des suffixes.

### Onglet [!UICONTROL Set Schedule]

**[!UICONTROL When]:** à quel moment importer les campagnes spécifiées : *Auto* (pour permettre à [!DNL Microsoft Advertising] de définir un planning afin d’optimiser au mieux vos campagnes), *[!UICONTROL Now]* (pour exécuter le traitement lorsque vous publiez les paramètres du traitement), *[!UICONTROL Once]* à un moment spécifié, *[!UICONTROL Daily]* à un moment spécifié, *[!UICONTROL Weekly]* à un moment spécifié ou *[!UICONTROL Monthly]* à un moment spécifié.

**[!UICONTROL Receive email notifications]:** Si et quand envoyer des notifications par e-mail sur les traitements d’importation aux adresses dans le champ [!UICONTROL Send reports to] : *[!UICONTROL No emails]*, *[!UICONTROL Only if there are changes or errors]* (valeur par défaut), *[!UICONTROL Only if there are errors]* ou *[!UICONTROL Every time this import runs]*.

**[!UICONTROL Send reports to]:** adresses e-mail pour recevoir des notifications sur les traitements d’import. Séparez les adresses multiples par des virgules (`,`).

>[!MORELIKETHIS]
>
>* [Gestion des comptes de réseau publicitaire](/help/search-social-commerce/manage/accounts/api-accounts/api-account-manage.md)
