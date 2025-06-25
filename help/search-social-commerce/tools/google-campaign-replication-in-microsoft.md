---
title: Répliquer  [!DNL Google Ads]  campagnes dans  [!DNL Microsoft Advertising]
description: Découvrez comment exporter vos campagnes synchronisées dans un compte  [!DNL Google Ads]  directement dans un compte  [!DNL Microsoft Advertising] .
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Réplication des campagnes [!DNL Google Ads] dans [!DNL Microsoft Advertising]

Vous pouvez exporter vos campagnes synchronisées dans un compte [!DNL Google Ads] directement vers un compte [!DNL Microsoft Advertising] synchronisé en tant que campagnes CPC améliorées (eCPC). Les offres existantes et les budgets de campagne sont mis à l’échelle. Le suivi Search, Social et Commerce existant n’est pas importé.

Vous pouvez répliquer les types de campagne suivants et leur structure :

* [!DNL Google Ads] des campagnes de recherche et d’affichage dans [!DNL Microsoft Advertising] campagnes de recherche et d’affichage .

* [!DNL Google Display Network] des campagnes, y compris des images publicitaires, dans des campagnes d’audience [!DNL Microsoft Advertising] sur le réseau d’audiences Microsoft.

  Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achats, répliquez d’abord vos offres de produits [!DNL Google Merchant Center] sur [!DNL Microsoft Merchant Center]. Lorsque vous répliquez les campagnes, sélectionnez la boutique [!DNL Microsoft Merchant Center] dans les Options d’importation pour la lier à vos campagnes d’audience basées sur les flux.

* [!DNL Google Ads] les campagnes Performances Max , y compris les annonces d’inventaire local, en campagnes Performances Max [!DNL Microsoft Advertising] .

Vous pouvez choisir de mettre à jour les campagnes une fois, tous les jours, toutes les semaines ou tous les mois, ou selon le planning recommandé par [!DNL Microsoft Advertising]. Vous pouvez éventuellement configurer des notifications chaque fois qu’une tâche d’importation s’exécute ou que des erreurs ou des modifications se produisent. Une fois que vous avez importé vos campagnes dans [!DNL Microsoft Advertising], vous pouvez vérifier le statut de votre tâche d’importation, consulter les journaux d’erreur, exécuter manuellement une tâche d’importation et modifier, suspendre, activer ou supprimer votre planning d’importation.

Toutes les informations sur les campagnes ne sont pas répliquées, et vous devrez peut-être ajouter certaines informations à vos campagnes [!DNL Microsoft Advertising]. Pour plus d’informations sur les données importées, consultez [!DNL Microsoft Advertising]’aide dans la section « [ de quoi est importé  [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851) ». Étant donné que le suivi des recherches, des réseaux sociaux et de Commerce n’est pas importé, vous devez également ajouter le suivi dans les paramètres [compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ou [annonce](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Réplication des campagnes [!DNL Google Ads]

>[!NOTE]
>
>Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achats, commencez par [répliquer vos offres  [!DNL Google Merchant Center]  produits dans [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Lorsque vous répliquez les campagnes, sélectionnez le magasin de [!DNL Microsoft Merchant Center] dans les options d’importation pour le lier à vos campagnes d’audience basées sur les flux.

Voir [Qu’est-ce qui est importé des  [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Dans le menu principal Search, Social et Commerce, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cliquez sur **[!UICONTROL +Import]**.

1. Spécifiez les [paramètres d’importation](#campaign-import-settings) :

   1. Dans la section **[!UICONTROL Select accounts]** :

      1. Sélectionnez les comptes source et de destination.

      1. Cliquez sur **[!UICONTROL Get Credential Id from MSA]**.

      1. Connectez-vous au compte de [!DNL Microsoft Advertising] de destination, copiez l’identifiant d’identification affiché et collez la valeur dans le champ **[!UICONTROL Credential ID]** .

   1. Dans la section **[!UICONTROL Select campaigns & ad groups]** , spécifiez les campagnes et les groupes publicitaires à importer.

   1. Dans la section **[!UICONTROL Customize your import]** , indiquez les types d’éléments à importer.

   1. Dans la section **[!UICONTROL Set schedule]** , indiquez quand exécuter la tâche d’importation.

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Ajoutez le suivi Search, Social et Commerce dans les paramètres [compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) ou [annonce](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md).

## Modifier les paramètres de planning d’un traitement d’import de campagne

Voir [Qu’est-ce qui est importé des  [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cochez la case en regard de la tâche d’importation, puis cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Dans la section **[!UICONTROL Set schedule]**, spécifiez les [paramètres de planification](#campaign-import-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Affichage des traitements d’import de campagne

Vous pouvez répertorier toutes les tâches d’importation, y compris le compte de [!DNL Google Ads] source, le compte de [!DNL Microsoft Advertising] cible, l’heure ou la planification de l’importation et l’utilisateur ou l’utilisatrice qui a créé la tâche. Lorsque vous exécutez une tâche d’importation plusieurs fois, y compris lors d’importations planifiées régulièrement, chaque occurrence est répertoriée comme une tâche distincte.

* Effectuez l’une des opérations suivantes :

   * Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Par défaut, la vue s’ouvre sur l’onglet [!UICONTROL List of Import Jobs] .

   * Dans l’onglet [[!UICONTROL Import Logs] , cliquez ](#campaign-import-log) l’onglet **[!UICONTROL List of Import Jobs]** .

## Exécution d’un traitement d’import de campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cochez la case en regard de la tâche d’importation.

1. Cliquez sur ![Exécuter maintenant](/help/search-social-commerce/assets/run.png "Exécuter maintenant").

## Afficher les journaux de vos traitements d’import de campagne {#campaign-import-log}

Vous pouvez répertorier toutes les tâches d’importation terminées ou ayant échoué, y compris l’heure de début, le compte de [!DNL Google Ads] source, le compte de [!DNL Microsoft Advertising] cible, l’utilisateur ou l’utilisatrice qui a créé la tâche, le nombre d’opérations réussies et ayant échoué et les adresses e-mail qui ont reçu des notifications pour chaque tâche. Vous pouvez afficher des détails supplémentaires sur les modifications apportées au compte de [!DNL Microsoft Advertising] cible pour chaque traitement, y compris le nombre d’éléments ajoutés, synchronisés, supprimés et qui ont généré des erreurs pour chaque niveau d’entité (campagne ou mot-clé, par exemple) dans le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cliquez sur l’onglet **[!UICONTROL Import Logs]** .

1. (Facultatif) Pour afficher les détails d’une tâche d’importation, cliquez sur la valeur dans la colonne [!UICONTROL Summary].

## Paramètres des traitements d&#39;import Campaign {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** compte [!DNL Google Ads] synchronisé à partir duquel les données de campagne sont exportées.

**[!UICONTROL Credential ID]:** identifiant que [!DNL Microsoft Advertising] utilise pour représenter vos informations d’identification [!DNL Google Ads].

La génération automatique des informations d’identification [!DNL Microsoft Advertising] pour l’importation n’est pas disponible en raison de limitations [!DNL Microsoft Advertising]. Contactez l’équipe chargée de votre compte Adobe. Elle générera les informations d’identification et vous donnera l’identifiant.

**[!UICONTROL Target Microsoft Ads account]:** compte [!DNL Microsoft Advertising] synchronisé dans lequel les données de campagne sont importées.

### [!UICONTROL Select campaigns & ad groups]

**\[Données à importer\]:** Spécifiez les données à importer :

* *[!UICONTROL Import all new and existing campaigns]:* pour importer les données de toutes les campagnes qui existent déjà et de celles qui n’existent pas dans [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* pour sélectionner des campagnes et des groupes publicitaires spécifiques.

   * Pour développer une campagne en ses groupes d’annonces enfants, cliquez sur **[!UICONTROL >]** après le nom de la campagne.

   * Pour sélectionner une campagne ou un groupe publicitaire, sélectionnez l’élément afin qu’une coche s’affiche.

   * Pour supprimer une campagne ou un groupe publicitaire :

      * Dans la colonne [!UICONTROL Campaigns] ou [!UICONTROL Adgroups], désélectionnez la campagne ou le groupe publicitaire afin que la coche disparaisse.

      * Dans la colonne [!UICONTROL Selected], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** vous permet de spécifier les éléments à importer, les offres et les budgets, ainsi que d’autres options.

**[!UICONTROL What to import]:** définit les éléments à importer. Les options permettant d&#39;importer des catégories d&#39;articles sont sélectionnées par défaut, tous les types d&#39;articles étant sélectionnés. Pour inclure uniquement des types d’éléments spécifiques, cliquez sur **[!UICONTROL Show advanced options]** et modifiez les types d’éléments pour inclure.

**[!UICONTROL Bids and budgets]:** définit les paramètres d’offre et de budget à importer, mettre à jour et personnaliser.

**[!UICONTROL Other options]:** définit comment gérer les URL de page de destination importées, les modèles de suivi et d’autres options de campagne, d’annonce publicitaire et de ciblage.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** nom de la tâche d’importation.

**[!UICONTROL When]:** quand importer les campagnes spécifiées : *Auto* (pour [!DNL Microsoft Advertising] permettre de définir un planning afin d’optimiser au mieux vos campagnes), *[!UICONTROL Now]* (pour exécuter le traitement lorsque vous publiez les paramètres du traitement), *[!UICONTROL Once]* à une heure spécifiée, *[!UICONTROL Daily]* à une heure spécifiée, *[!UICONTROL Weekly]* à une heure spécifiée ou *[!UICONTROL Monthly]* à une heure spécifiée.

**[!UICONTROL Receive email notifications]:** si et quand envoyer des notifications par e-mail sur les traitements d’importation aux adresses e-mail dans le champ Envoyer les rapports à .

**[!UICONTROL Send reports to]:** Adresses e-mail auxquelles envoyer des notifications sur les traitements d’import. Séparez les adresses multiples par des virgules (`,`).
