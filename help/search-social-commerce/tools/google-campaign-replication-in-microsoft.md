---
title: Répliquer [!DNL Google Ads] campagnes dans [!DNL Microsoft Advertising]
description: Découvrez comment exporter vos campagnes synchronisées dans un compte  [!DNL Google Ads] directement dans un compte  [!DNL Microsoft Advertising] synchronisé.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Répliquer les campagnes [!DNL Google Ads] dans [!DNL Microsoft Advertising]

Vous pouvez exporter vos campagnes synchronisées dans un compte [!DNL Google Ads] directement dans un compte [!DNL Microsoft Advertising] synchronisé sous la forme de campagnes CPC (eCPC) améliorées. Les offres existantes et les budgets de campagne sont mis à l’échelle. Le suivi Recherche, Social et Commerce existant n’est pas importé.

Vous pouvez répliquer les types de campagnes suivants et leur structure de campagne :

* [!DNL Google Ads] recherchez et affichez des campagnes dans [!DNL Microsoft Advertising] campagnes de recherche et d’affichage.

* [!DNL Google Display Network] campagnes, y compris des images publicitaires, dans [!DNL Microsoft Advertising] campagnes d’audience sur le réseau d’audience Microsoft.

  Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achat, répliquez d’abord vos offres de produits [!DNL Google Merchant Center] sur [!DNL Microsoft Merchant Center]. Lorsque vous répliquez les campagnes, sélectionnez le magasin [!DNL Microsoft Merchant Center] dans les Options d’importation pour lier le magasin à vos campagnes d’audience basées sur les flux.

* [!DNL Google Ads] campagnes de performances max, y compris les annonces d’inventaire local, dans [!DNL Microsoft Advertising] campagnes de performances max.

Vous pouvez choisir de mettre à jour les campagnes une fois, tous les jours, toutes les semaines ou tous les mois, ou selon la planification recommandée par [!DNL Microsoft Advertising]. Vous pouvez éventuellement configurer des notifications à chaque exécution d’une tâche d’importation ou en cas d’erreurs ou de modifications. Une fois que vous avez importé vos campagnes dans [!DNL Microsoft Advertising], vous pouvez vérifier l’état de votre tâche d’importation, consulter les journaux d’erreurs, exécuter manuellement une tâche d’importation et modifier, mettre en pause, activer ou supprimer votre planning d’importation.

Toutes les informations sur les campagnes ne sont pas répliquées et vous devrez peut-être ajouter des informations à vos campagnes [!DNL Microsoft Advertising]. Pour plus d&#39;informations sur les données importées, consultez l&#39;[!DNL Microsoft Advertising]&#39;aide sur &quot;[Ce qui est importé de [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851)&quot;. Comme le suivi de recherche, de Social et de Commerce n’est pas importé, vous devez également ajouter le suivi dans les paramètres [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ou [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Réplication des campagnes [!DNL Google Ads]

>[!NOTE]
>
>Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achat, commencez par [répliquer vos  [!DNL Google Merchant Center] offres de produits dans [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Lorsque vous répliquez les campagnes, sélectionnez le magasin [!DNL Microsoft Merchant Center] dans les options d’importation pour lier le magasin à vos campagnes d’audience basées sur les flux.

Voir [ce qui est importé de [!DNL Google Ads] campaigns](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Dans le menu principal Rechercher, Social et Commerce, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cliquez sur **[!UICONTROL +Import]**.

1. Spécifiez les [paramètres d&#39;import](#campaign-import-settings) :

   1. Dans la section **[!UICONTROL Select accounts]** :

      1. Sélectionnez les comptes source et de destination.

      1. Cliquez sur **[!UICONTROL Get Credential Id from MSA]**.

      1. Connectez-vous au compte [!DNL Microsoft Advertising] de destination, copiez l’identifiant d’identification affiché, puis collez la valeur dans le champ **[!UICONTROL Credential ID]** .

   1. Dans la section **[!UICONTROL Select campaigns & ad groups]** , spécifiez les campagnes et les groupes publicitaires à importer.

   1. Dans la section **[!UICONTROL Customize your import]** , spécifiez les types d’éléments à importer.

   1. Dans la section **[!UICONTROL Set schedule]** , indiquez quand exécuter la tâche d’importation.

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Ajoutez le suivi Search, Social et Commerce dans les paramètres [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ou [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Modification des paramètres de planification d’une tâche d’importation de campagne

Voir [ce qui est importé de [!DNL Google Ads] campaigns](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cochez la case en regard de la tâche d’importation, puis cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Dans la section **[!UICONTROL Set schedule]** , spécifiez les [paramètres de planification](#campaign-import-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Affichage des traitements d&#39;import de campagne

Vous pouvez répertorier toutes les tâches d’importation, y compris le compte source [!DNL Google Ads], le compte cible [!DNL Microsoft Advertising], l’heure ou le planning d’importation, ainsi que l’utilisateur qui a créé la tâche. Lorsque vous exécutez plusieurs fois une tâche d’importation, y compris lors d’imports régulièrement programmés, chaque occurrence est répertoriée comme une tâche distincte.

* Effectuez l’une des opérations suivantes :

   * Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Par défaut, la vue s’ouvre sur l’onglet [!UICONTROL List of Import Jobs].

   * Dans l’onglet [[!UICONTROL Import Logs] ](#campaign-import-log), cliquez sur l’onglet **[!UICONTROL List of Import Jobs]** .

## Exécution d’une tâche d’importation de campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cochez la case en regard de la tâche d’importation.

1. Cliquez sur ![Exécuter maintenant](/help/search-social-commerce/assets/run.png "Exécuter maintenant").

## Afficher les journaux des tâches d’importation de campagne {#campaign-import-log}

Vous pouvez répertorier toutes les tâches d’importation terminées ou ayant échoué, notamment l’heure de début, le compte source [!DNL Google Ads], le compte cible [!DNL Microsoft Advertising], l’utilisateur qui a créé la tâche, le nombre d’opérations réussies et en échec, ainsi que toutes les adresses électroniques qui ont reçu des notifications pour chaque tâche. Vous pouvez afficher plus de détails sur les modifications apportées au compte [!DNL Microsoft Advertising] cible pour chaque tâche, y compris le nombre d’éléments ajoutés, synchronisés, supprimés et qui ont généré des erreurs pour chaque niveau d’entité (campagne ou mot-clé, par exemple) dans le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cliquez sur l’onglet **[!UICONTROL Import Logs]** .

1. (Facultatif) Pour afficher les détails d’une tâche d’importation, cliquez sur la valeur dans la colonne [!UICONTROL Summary].

## Paramètres des tâches d&#39;import de campagne {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** compte [!DNL Google Ads] synchronisé à partir duquel les données de campagne sont exportées.

**[!UICONTROL Credential ID]:** ID utilisé par [!DNL Microsoft Advertising] pour représenter vos informations d’identification [!DNL Google Ads].

La génération automatique des informations d’identification [!DNL Microsoft Advertising] pour l’importation n’est pas disponible en raison des restrictions de [!DNL Microsoft Advertising]. Contactez votre équipe de compte d’Adobe, qui générera les informations d’identification et vous fournira l’identifiant.

**[!UICONTROL Target Microsoft Ads account]:** compte [!DNL Microsoft Advertising] synchronisé dans lequel les données de campagne sont importées.

### [!UICONTROL Select campaigns & ad groups]

**\[Données à importer\]:** Spécifiez les données à importer :

* *[!UICONTROL Import all new and existing campaigns]:* pour importer des données pour toutes les campagnes qui existent déjà et les campagnes qui n’existent pas dans [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* pour sélectionner des campagnes et des groupes publicitaires spécifiques.

   * Pour développer une campagne dans ses groupes d’annonces enfants, cliquez sur **[!UICONTROL >]** après le nom de la campagne.

   * Pour sélectionner une campagne ou un groupe publicitaire, sélectionnez l’élément afin qu’une coche s’affiche.

   * Pour supprimer une campagne ou un groupe publicitaire :

      * Dans la colonne [!UICONTROL Campaigns] ou [!UICONTROL Adgroups], désélectionnez la campagne ou le groupe publicitaire pour que la coche disparaisse.

      * Dans la colonne [!UICONTROL Selected], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Permet de spécifier les éléments à importer, les offres et les budgets, ainsi que d’autres options.

**[!UICONTROL What to import]:** Définit les éléments à importer. Les options d’importation de catégories d’éléments sont sélectionnées par défaut, tous les types d’éléments étant sélectionnés. Pour inclure uniquement des types d’éléments spécifiques, cliquez sur **[!UICONTROL Show advanced options]** et modifiez les types d’éléments à inclure.

**[!UICONTROL Bids and budgets]:** définit les paramètres d’offre et de budget à importer, mettre à jour et personnaliser.

**[!UICONTROL Other options]:** définit la gestion des URL de page d’entrée importées, des modèles de suivi et d’autres options de campagne, de publicité et de ciblage.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Nom de la tâche d’importation.

**[!UICONTROL When]:** à quel moment importer les campagnes spécifiées : *Auto* (pour permettre à [!DNL Microsoft Advertising] de définir une planification afin d’optimiser vos campagnes), *[!UICONTROL Now]* (pour exécuter la tâche lorsque vous publiez les paramètres de la tâche), *[!UICONTROL Once]* à un moment spécifié, *[!UICONTROL Daily]* à un moment spécifié, *[!UICONTROL Weekly]* à un moment spécifié ou *[!UICONTROL Monthly]* à un moment spécifié.

**[!UICONTROL Receive email notifications]:** si et à quel moment envoyer des notifications par e-mail sur les tâches d’importation aux adresses de messagerie dans le champ Envoyer les rapports à .

**[!UICONTROL Send reports to]:** Adresses électroniques pour recevoir des notifications sur les tâches d’importation. Séparez plusieurs adresses par des virgules (`,`).
