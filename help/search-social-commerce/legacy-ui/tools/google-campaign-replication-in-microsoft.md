---
title: Répliquer [!DNL Google Ads] campagnes dans [!DNL Microsoft Advertising]
description: Découvrez comment exporter directement vos campagnes synchronisées dans un compte [!DNL Google Ads] vers un compte [!DNL Microsoft Advertising] synchronisé.
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
TQID: 'https://experienceleague.adobe.com/l0yaZq0hmQSXXeJon22Fm8HOWJ6JDOaZuGqwxVfdw-c'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9f383e89-9ec3-5629-8dc3-d5aa5ab0be32
    internal-label: Search Tools
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '981'
ht-degree: 0%
---
# Répliquer [!DNL Google Ads] campagnes dans [!DNL Microsoft Advertising]

>[!NOTE]
>
>Les instructions pour cette tâche dans la nouvelle interface utilisateur sont disponibles à l’adresse « (Nouvelle interface utilisateur) [Répliquer [!DNL Google Ads] les campagnes dans [!DNL Microsoft Advertising]](/help/search-social-commerce/manage/campaigns/google-campaign-replication-in-microsoft.md) ».

Vous pouvez exporter vos campagnes synchronisées dans un compte [!DNL Google Ads] directement vers un compte [!DNL Microsoft Advertising] synchronisé en tant que campagnes CPC améliorées (eCPC). Les offres existantes et les budgets de campagne sont mis à l’échelle. Le suivi Search, Social et Commerce existant n’est pas importé.

Vous pouvez répliquer les types de campagne suivants et leur structure :

* [!DNL Google Ads] rechercher et afficher des campagnes dans [!DNL Microsoft Advertising] rechercher et afficher des campagnes.

* [!DNL Google Display Network] campagnes, y compris des images publicitaires, dans [!DNL Microsoft Advertising] campagnes d’audience sur le réseau d’audiences Microsoft.

  Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achats, répliquez d’abord vos [!DNL Google Merchant Center] offres de produits vers [!DNL Microsoft Merchant Center]. Lorsque vous répliquez les campagnes, sélectionnez la boutique [!DNL Microsoft Merchant Center] dans les options d’importation pour la lier à vos campagnes d’audience basées sur les flux.

* [!DNL Google Ads] campagnes de performance max, y compris les annonces d’inventaire local, en [!DNL Microsoft Advertising] campagnes de performance max.

Vous pouvez choisir de mettre à jour les campagnes une fois, tous les jours, toutes les semaines ou tous les mois, ou selon le planning recommandé par [!DNL Microsoft Advertising]. Vous pouvez éventuellement configurer des notifications chaque fois qu’une tâche d’importation s’exécute ou que des erreurs ou des modifications se produisent. Une fois que vous avez importé vos campagnes dans [!DNL Microsoft Advertising], vous pouvez vérifier le statut de votre tâche d’importation, consulter les journaux d’erreur, exécuter manuellement une tâche d’importation et modifier, suspendre, activer ou supprimer votre planning d’importation.

Toutes les informations de campagne ne sont pas répliquées, et vous devrez peut-être ajouter certaines informations à vos campagnes [!DNL Microsoft Advertising]. Pour plus d&#39;informations sur les données importées, consultez l&#39;aide de [!DNL Microsoft Advertising] sur « [Ce qui est importé de [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851) ». Comme le suivi des moteurs de recherche, des réseaux sociaux et de Commerce n’est pas importé, vous devez également ajouter le suivi dans les paramètres [compte](/help/search-social-commerce/legacy-ui/campaign-management/accounts/ad-network-account-manage.md), [campagne](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/campaign-manage.md), [groupe publicitaire](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/ad-group-manage.md) ou [publicité](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/ad-manage.md).

## Répliquer [!DNL Google Ads] campagnes

>[!NOTE]
>
>Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achats, commencez par [répliquer vos [!DNL Google Merchant Center] offres de produits dans [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Lorsque vous répliquez les campagnes, sélectionnez le magasin [!DNL Microsoft Merchant Center] dans les options d’importation pour le lier à vos campagnes d’audience basées sur les flux.

Voir [ce qui est importé des [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Dans le menu principal Search, Social et Commerce, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cliquez sur **[!UICONTROL +Import]**.

1. Spécifiez les [paramètres d’importation](#campaign-import-settings) :

   1. Dans la section **[!UICONTROL Select accounts]** :

      1. Sélectionnez les comptes source et de destination.

      1. Cliquez sur **[!UICONTROL Get Credential Id from MSA]**.

      1. Connectez-vous au compte [!DNL Microsoft Advertising] de destination, copiez l’identifiant d’identification affiché et collez la valeur dans le champ **[!UICONTROL Credential ID]**.

   1. Dans la section **[!UICONTROL Select campaigns & ad groups]**, spécifiez les campagnes et les groupes publicitaires à importer.

   1. Dans la section **[!UICONTROL Customize your import]**, spécifiez les types d’éléments à importer.

   1. Dans la section **[!UICONTROL Set schedule]**, indiquez quand exécuter la tâche d’importation.

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Ajoutez le suivi Search, Social et Commerce dans les paramètres [compte](/help/search-social-commerce/legacy-ui/campaign-management/accounts/ad-network-account-manage.md), [campagne](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/campaign-manage.md), [groupe publicitaire](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/ad-group-manage.md) ou [publicité](/help/search-social-commerce/legacy-ui/campaign-management/campaigns/ad-manage.md).

## Modifier les paramètres de planning d’un traitement d’import de campagne

Voir [ce qui est importé des [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >.[!UICONTROL Import Campaigns]**

1. Cochez la case en regard de la tâche d’importation, puis cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Dans la section **[!UICONTROL Set schedule]**, spécifiez les [paramètres de planification](#campaign-import-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Affichage des traitements d’import de campagne

Vous pouvez répertorier toutes les tâches d’importation, y compris le compte [!DNL Google Ads] source, le compte [!DNL Microsoft Advertising] cible, l’heure ou le planning d’importation et l’utilisateur ou l’utilisatrice qui a créé la tâche. Lorsque vous exécutez une tâche d’importation plusieurs fois, y compris lors d’importations planifiées régulièrement, chaque occurrence est répertoriée comme une tâche distincte.

* Effectuez l’une des opérations suivantes :

  * Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >.[!UICONTROL Import Campaigns]**

    Par défaut, la vue s’ouvre sur l’onglet [!UICONTROL List of Import Jobs].

  * Dans l’onglet [[!UICONTROL Import Logs]](#campaign-import-log), cliquez sur l’onglet **[!UICONTROL List of Import Jobs]**.

## Exécution d’un traitement d’import de campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >.[!UICONTROL Import Campaigns]**

1. Cochez la case en regard de la tâche d’importation.

1. Cliquez sur ![Exécuter maintenant](/help/search-social-commerce/assets/run.png "Exécuter maintenant").

## Afficher les journaux de vos traitements d’import de campagne {#campaign-import-log}

Vous pouvez répertorier toutes les tâches d’importation terminées ou ayant échoué, y compris l’heure de début, le compte [!DNL Google Ads] source, le compte [!DNL Microsoft Advertising] cible, l’utilisateur ou l’utilisatrice qui a créé la tâche, le nombre d’opérations réussies et ayant échoué et les adresses e-mail qui ont reçu des notifications pour chaque tâche. Vous pouvez afficher des détails supplémentaires sur les modifications apportées au compte [!DNL Microsoft Advertising] de la cible pour chaque tâche, y compris le nombre d’éléments ajoutés, synchronisés, supprimés et qui ont généré des erreurs pour chaque niveau d’entité (campagne ou mot-clé, par exemple) dans le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >.[!UICONTROL Import Campaigns]**

1. Cliquez sur l’onglet **[!UICONTROL Import Logs]**.

1. (Facultatif) Pour afficher les détails d’une tâche d’importation, cliquez sur la valeur de la colonne [!UICONTROL Summary].

## Paramètres des traitements d&#39;import Campaign {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Compte [!DNL Google Ads] synchronisé à partir duquel les données de campagne sont exportées.

**[!UICONTROL Credential ID]:** Identifiant utilisé par [!DNL Microsoft Advertising] pour représenter vos informations d’identification [!DNL Google Ads].

La génération automatique des informations d&#39;identification [!DNL Microsoft Advertising] pour l&#39;importation n&#39;est pas disponible en raison des limitations [!DNL Microsoft Advertising]. Contactez l’équipe chargée de votre compte Adobe. Elle générera les informations d’identification et vous donnera l’identifiant.

**[!UICONTROL Target Microsoft Ads account]:** Compte [!DNL Microsoft Advertising] synchronisé dans lequel les données de campagne sont importées.

### [!UICONTROL Select campaigns & ad groups]

**\[Données à importer\]:** Spécifiez les données à importer :

* *[!UICONTROL Import all new and existing campaigns]:* Pour importer les données de toutes les campagnes qui existent déjà et de celles qui n’existent pas dans [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Pour sélectionner des campagnes et des groupes publicitaires spécifiques.

  * Pour développer une campagne dans ses groupes d’annonces enfants, cliquez sur **[!UICONTROL >]** après le nom de la campagne.

  * Pour sélectionner une campagne ou un groupe publicitaire, sélectionnez l’élément afin qu’une coche s’affiche.

  * Pour supprimer une campagne ou un groupe publicitaire :

    * Dans la colonne [!UICONTROL Campaigns] ou [!UICONTROL Adgroups], désélectionnez la campagne ou le groupe publicitaire afin que la coche disparaisse.

    * Dans la colonne [!UICONTROL Selected], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** vous permet de spécifier les éléments à importer, les offres et les budgets, ainsi que d&#39;autres options.

**[!UICONTROL What to import]:** définit les éléments à importer. Les options permettant d&#39;importer des catégories d&#39;articles sont sélectionnées par défaut, tous les types d&#39;articles étant sélectionnés. Pour inclure uniquement des types d’éléments spécifiques, cliquez sur **[!UICONTROL Show advanced options]** et modifiez les types d’éléments pour inclure.

**[!UICONTROL Bids and budgets]:** définit les paramètres d&#39;enchères et de budget à importer, mettre à jour et personnaliser.

**[!UICONTROL Other options]:** définit comment gérer les URL de page de destination importées, les modèles de suivi et d’autres options de campagne, d’annonce publicitaire et de ciblage.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Nom de la tâche d’importation.

**[!UICONTROL When]:** à quel moment importer les campagnes spécifiées : *Auto* (pour permettre à [!DNL Microsoft Advertising] de définir un planning afin d’optimiser au mieux vos campagnes), *[!UICONTROL Now]* (pour exécuter le traitement lorsque vous publiez les paramètres du traitement), *[!UICONTROL Once]* à un moment spécifié, *[!UICONTROL Daily]* à un moment spécifié, *[!UICONTROL Weekly]* à un moment spécifié ou *[!UICONTROL Monthly]* à un moment spécifié.

**[!UICONTROL Receive email notifications]:** si et quand envoyer des notifications par e-mail sur les traitements d’importation aux adresses e-mail dans le champ Envoyer les rapports à.

**[!UICONTROL Send reports to]:** adresses e-mail pour recevoir des notifications sur les traitements d’import. Séparez les adresses multiples par des virgules (`,`).
