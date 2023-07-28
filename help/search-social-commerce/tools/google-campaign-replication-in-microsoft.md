---
title: Répliquer [!DNL Google Ads] campagnes dans [!DNL Microsoft® Advertising]
description: Découvrez comment exporter vos campagnes synchronisées dans une [!DNL Google Ads] compte directement dans une synchronisation [!DNL Microsoft® Advertising] compte .
exl-id: 1bb0d915-bf33-4c50-88a5-268d4de5ccff
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '962'
ht-degree: 0%

---

# Répliquer [!DNL Google Ads] campagnes dans [!DNL Microsoft® Advertising]

Vous pouvez exporter vos campagnes synchronisées dans une [!DNL Google Ads] compte directement dans une synchronisation [!DNL Microsoft® Advertising] compte en tant que campagnes CPC (eCPC) améliorées. Les offres existantes et les budgets de campagne sont mis à l’échelle. Le suivi Recherche, Social et Commerce existant n’est pas importé.

Vous pouvez répliquer les types de campagnes suivants et leur structure de campagne :

* [!DNL Google Ads] rechercher et afficher des campagnes dans [!DNL Microsoft® Advertising] rechercher et afficher des campagnes.

* [!DNL Google Display Network] campagnes, y compris des images publicitaires, dans [!DNL Microsoft® Advertising] campagnes d’audience sur Microsoft® Audience Network.

  Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achat, répliquez d’abord vos [!DNL Google Merchant Center] offres de produits à [!DNL Microsoft® Merchant Center]. Lorsque vous répliquez les campagnes, sélectionnez la variable [!DNL Microsoft® Merchant Center] stockez dans les options d’importation pour lier le magasin à vos campagnes d’audience basées sur le flux.

* [!DNL Google Ads] campagnes de performances maximales, y compris les annonces d’inventaire local, en [!DNL Microsoft® Advertising] campagnes d’achats dynamiques.

Vous pouvez choisir de mettre à jour les campagnes une fois, tous les jours, toutes les semaines ou tous les mois, ou selon les [!DNL Microsoft® Advertising]Le planning est recommandé. Vous pouvez éventuellement configurer des notifications à chaque exécution d’une tâche d’importation ou en cas d’erreurs ou de modifications. Une fois que vous avez importé vos campagnes dans [!DNL Microsoft® Advertising], vous pouvez vérifier l’état de votre tâche d’importation, consulter les logs d’erreur, exécuter manuellement une tâche d’importation et modifier, mettre en pause, activer ou supprimer votre planning d’importation.

Toutes les informations sur les campagnes ne sont pas répliquées et vous devrez peut-être ajouter des informations à votre [!DNL Microsoft® Advertising] campagnes. Pour plus d’informations sur les données importées, voir [!DNL Microsoft® Advertising] help sur &quot;[Éléments importés depuis [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; Comme le suivi de recherche, de Social et de Commerce n’est pas importé, vous devez également ajouter le suivi dans la variable [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), ou [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) paramètres.

## Répliquer [!DNL Google Ads] campagnes

>[!NOTE]
>
>Si vous souhaitez répliquer des campagnes d’affichage basées sur des flux d’achat, commencez par [répliquez votre [!DNL Google Merchant Center] offres de produits dans [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). Lorsque vous répliquez les campagnes, sélectionnez la variable [!DNL Microsoft® Merchant Center] stockez dans les options d’importation pour lier le magasin à vos campagnes d’audience basées sur le flux.

Voir [de ce qui est importé d’ [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Dans le menu principal Rechercher, Social et commerce, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cliquez sur **[!UICONTROL +Import]**.

1. Spécifiez la variable [paramètres d’importation](#campaign-import-settings):

   1. Dans le **[!UICONTROL Select accounts]** section :

      1. Sélectionnez les comptes source et de destination.

      1. Cliquez sur **[!UICONTROL Get Credential Id from MSA]**.

      1. Connectez-vous à la destination [!DNL Microsoft Advertising] , copiez l’identifiant d’identification affiché, puis collez la valeur dans la variable **[!UICONTROL Credential ID]** champ .

   1. Dans le **[!UICONTROL Select campaigns & ad groups]** , indiquez les campagnes et les groupes publicitaires à importer.

   1. Dans le **[!UICONTROL Customize your import]** , spécifiez les types d’éléments à importer.

   1. Dans le **[!UICONTROL Set schedule]** , indiquez quand exécuter la tâche d’importation.

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Ajoutez le suivi Rechercher, Social et Commerce dans la variable [account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [groupe publicitaire](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md), ou [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) paramètres.

## Modification des paramètres de planification d’une tâche d’importation de campagne

Voir [de ce qui est importé d’ [!DNL Google Ads] campagnes](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cochez la case en regard de la tâche d’importation, puis cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Dans le **[!UICONTROL Set schedule]** , spécifiez la variable [paramètres de planification](#campaign-import-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Affichage des traitements d&#39;import de campagne

Vous pouvez répertorier toutes les tâches d’importation, y compris la source [!DNL Google Ads] compte, cible [!DNL Microsoft® Advertising] compte, l’heure ou le planning de l’importation et l’utilisateur qui a créé la tâche. Lorsque vous exécutez plusieurs fois une tâche d’importation, y compris lors d’imports régulièrement programmés, chaque occurrence est répertoriée comme une tâche distincte.

* Effectuez l’une des opérations suivantes :

   * Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     Par défaut, la vue s’ouvre sur la [!UICONTROL List of Import Jobs] .

   * Dans la [[!UICONTROL Import Logs] tab](#campaign-import-log), cliquez sur le **[!UICONTROL List of Import Jobs]** .

## Exécution d’une tâche d’importation de campagne

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cochez la case en regard de la tâche d’importation.

1. Cliquez sur ![Exécuter maintenant](/help/search-social-commerce/assets/run.png "Exécuter maintenant").

## Afficher les journaux des tâches d’importation de campagne {#campaign-import-log}

Vous pouvez répertorier toutes les tâches d’importation terminées ou ayant échoué, y compris l’heure de début, la source [!DNL Google Ads] compte, cible [!DNL Microsoft® Advertising] compte, utilisateur ayant créé la tâche, nombre d’opérations réussies et ayant échoué et adresses électroniques ayant reçu des notifications pour chaque tâche. Vous pouvez afficher plus de détails sur les modifications apportées à la cible. [!DNL Microsoft® Advertising] compte qui s’est produit pour chaque tâche, y compris le nombre d’éléments ajoutés, synchronisés, supprimés et qui ont généré des erreurs pour chaque niveau d’entité (campagne ou mot-clé, par exemple) dans le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. Cliquez sur le bouton **[!UICONTROL Import Logs]** .

1. (Facultatif) Pour afficher les détails d’une tâche d’importation, cliquez sur la valeur de la variable [!UICONTROL Summary] colonne .

## Paramètres des tâches d&#39;import de campagne {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** Synchronisé [!DNL Google Ads] compte à partir duquel les données de campagne sont exportées.

**[!UICONTROL Credential ID]:** Un identifiant qui [!DNL Microsoft® Advertising] utilise pour représenter votre [!DNL Google Ads] informations d’identification.

Génération automatique de [!DNL Microsoft® Advertising] les informations d’identification pour l’importation ne sont pas disponibles en raison de [!DNL Microsoft® Advertising] limites. Contactez l’assistance technique d’Adobe ou votre équipe de compte d’Adobe. Ils généreront les informations d’identification et vous donneront l’identifiant.

**[!UICONTROL Target Microsoft® Ads account]:** Synchronisé [!DNL Microsoft® Advertising] compte dans lequel les données de campagne sont importées.

### [!UICONTROL Select campaigns & ad groups]

**\[Données à importer\] :** Indiquez les données à importer :

* *[!UICONTROL Import all new and existing campaigns]:* Pour importer des données pour toutes les campagnes qui existent déjà et les campagnes qui n’existent pas dans [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* Pour sélectionner des campagnes et des groupes publicitaires spécifiques.

   * Pour développer une campagne dans ses groupes publicitaires enfants, cliquez sur **[!UICONTROL >]** après le nom de la campagne.

   * Pour sélectionner une campagne ou un groupe publicitaire, sélectionnez l’élément afin qu’une coche s’affiche.

   * Pour supprimer une campagne ou un groupe publicitaire :

      * Dans le [!UICONTROL Campaigns] ou [!UICONTROL Adgroups] , désélectionnez la campagne ou le groupe publicitaire pour que la coche disparaisse.

      * Dans le [!UICONTROL Selected] colonne, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** Permet de spécifier les options d&#39;import, d&#39;offres et de budgets, ainsi que d&#39;autres options.

**[!UICONTROL What to import]:** Définit les éléments à importer. Les options d’importation de catégories d’éléments sont sélectionnées par défaut, tous les types d’éléments étant sélectionnés. Pour inclure uniquement des types d’éléments spécifiques, cliquez sur **[!UICONTROL Show advanced options]** et modifiez les types d’éléments à inclure.

**[!UICONTROL Bids and budgets]:** Définit les paramètres d’offre et de budget à importer, mettre à jour et personnaliser.

**[!UICONTROL Other options]:** Définit comment gérer les URL de page d’entrée importées, les modèles de suivi et d’autres options de campagne, de publicité et de ciblage.

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** Nom de la tâche d’importation.

**[!UICONTROL When]:** Quand importer les campagnes spécifiées : *Auto* (pour laisser [!DNL Microsoft® Advertising] définir un planning pour optimiser vos campagnes), *[!UICONTROL Now]* (pour exécuter la tâche lorsque vous publiez les paramètres de la tâche), *[!UICONTROL Once]* à une heure spécifiée, *[!UICONTROL Daily]* à une heure spécifiée, *[!UICONTROL Weekly]* à une heure spécifiée ; ou *[!UICONTROL Monthly]* à une heure spécifiée.

**[!UICONTROL Receive email notifications]:** Si et à quel moment envoyer des notifications par e-mail sur des tâches d’importation aux adresses e-mail dans le champ Envoyer les rapports à .

**[!UICONTROL Send reports to]:** Adresses électroniques pour recevoir des notifications sur les traitements d’importation. Séparez plusieurs adresses par des virgules (`,`).
