---
title: Gestion des comptes réseau et
description: Découvrez comment configurer et gérer les détails d’un compte réseau publicitaire.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: cb65108fcc60c11b901e3b43c292ad5a94192b9f
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# Gestion des comptes réseau et

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

Vous trouverez ci-dessous des instructions pour créer et modifier les détails du compte réseau publicitaire, actualiser le jeton [!DNL oAuth] pour un compte et désactiver les comptes.

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [&#x200B; Inventaire pris en charge &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md).

## Créer un compte réseau publicitaire {#create-account}

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Pour activer la synchronisation ou le suivi d’un compte, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et les options de suivi, ainsi que le statut *actif*.

>[!NOTE]
>
>* La prise en charge n’est pas disponible pour les nouveaux comptes [!DNL Baidu].
>* Pour créer un compte sur le réseau publicitaire, accédez au site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Spécifiez les [paramètres du compte](#account-settings) :

   1. Cliquez sur le nom du réseau publicitaire, puis sur **[!UICONTROL Next]**.

   1. Dans la section **[!UICONTROL Account Details]** , saisissez les détails du compte.

      Pour les réseaux publicitaires qui utilisent le type d’autorisation de connexion « [!UICONTROL oAuth] », autorisez Search, Social et Commerce à accéder au compte à l’aide du protocole d’autorisation [&#x200B; OAuth &#x200B;](https://oauth.net/2/) :

      1. Saisissez la valeur **[!UICONTROL Login]** du compte, éventuellement le mot de passe, puis cliquez sur **[!UICONTROL Authenticate]**.

         La bonne pratique consiste à utiliser la méthode de connexion pour accéder au compte via l’API. Saisissez le mot de passe lorsque vous souhaitez le chiffrer et l’enregistrer, de sorte que l’équipe du compte Adobe puisse actualiser les jetons si nécessaire.

      1. (Si vous n’êtes pas connecté au compte publicitaire de l’annonceur) Connectez-vous au compte publicitaire de l’annonceur. La bonne pratique consiste à utiliser les informations d’identification pour l’accès de l’API au compte .

      1. Dans l’écran de demande d’autorisation/accès , cliquez sur le bouton pour confirmer l’autorisation.

      1. Copiez la chaîne d’authentification dans la fenêtre pop-up qui s’ouvre et collez la chaîne dans le champ **[!UICONTROL oAuth Token]** .

      1. Spécifiez les détails du compte restant.

   1. Cliquez sur **[!UICONTROL Set Account Tracking]**, puis saisissez les paramètres de tracking.

1. Cliquez sur **[!UICONTROL Post]**.

   Les données récentes de coût et de clic pour toutes les campagnes du compte sont disponibles dans Search, Social et Commerce en 24 heures environ. Par défaut, les données sont disponibles pour les 5 à 10 derniers jours, selon le réseau publicitaire. Cependant, si nécessaire, l’équipe de lancement du projet peut récupérer les données des 60 derniers jours au maximum.

## Modifier les détails du compte réseau publicitaire {#edit-account}

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Si les informations d’identification du compte changent, vous pouvez modifier les paramètres de suivi par défaut sur un compte ou activer ou désactiver l’activité sur un compte, puis modifier les détails du compte.

>[!NOTE]
>
>Pour modifier un compte réel sur le réseau publicitaire, accédez au site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**.

1. Modifiez les [paramètres du compte](#account-settings) :

   1. (Facultatif) Modifiez les détails du compte.

   1. (Facultatif) Cliquez sur **[!UICONTROL Set Account Tracking]** et modifiez les paramètres de suivi.

1. Cliquez sur **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social et Commerce doivent synchroniser les nouvelles données de compte avec celles du réseau publicitaire. Cela se produit automatiquement une fois par jour, ou plus souvent lorsque Search, Social et Commerce détecte des modifications sur le réseau publicitaire.

## Actualiser les jetons d’accès oAuth pour les comptes de recherche {#refresh-oauth-tokens}

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Si Search, Social et Commerce accèdent au compte à l’aide du protocole d’autorisation [OAuth](https://oauth.net/2/) et que les informations d’identification du compte changent, ou si un accès supplémentaire est nécessaire pour prendre en charge de nouvelles fonctionnalités dans Search, Social et Commerce, vous devez obtenir un nouveau jeton d’accès pour le compte.

L’équipe chargée de votre compte Adobe vous informera si de nouvelles fonctionnalités nécessitent un nouveau jeton.

1. (Si vous êtes connecté à un autre compte pour le même réseau publicitaire dans la même application de navigateur) Déconnectez-vous de tout compte autre que celui de l’annonceur.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**.

1. Obtenir un nouveau jeton d’accès :

   1. Cliquez sur **[!UICONTROL Get oAuth Token]**.

   1. (Si vous n’êtes pas connecté au compte publicitaire de l’annonceur) Connectez-vous au compte publicitaire de l’annonceur. La bonne pratique consiste à utiliser les informations d’identification pour l’accès de l’API au compte .

   1. Dans l’écran de demande d’autorisation/accès , cliquez sur le bouton pour confirmer l’autorisation.

   1. Copiez la chaîne d’authentification dans la fenêtre pop-up qui s’ouvre et collez la chaîne dans le champ **[!UICONTROL oAuth Token]** .

1. Cliquez sur **[!UICONTROL Post]**.

## Activer ou désactiver les comptes réseau publicitaires {#enable-disable-account}

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte Adobe et d’utilisateur administrateur uniquement*

Lorsque vous activez un compte de réseau publicitaire, Search, Social et Commerce synchronise les données de la campagne avec le compte (lorsqu’il est pris en charge) et diffuse des enchères automatisées et/ou des budgets de campagne pour les campagnes des portfolios. Lorsque vous désactivez un compte de réseau publicitaire, Search, Social et Commerce arrête toute activité sur le compte. Les données collectées alors que le compte était actif sont toujours stockées, mais les vues et rapports de gestion de campagne n’incluent pas les données de la période au cours de laquelle le compte est désactivé. Vous pourrez par la suite réactiver le compte pour reprendre l’activité avec le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Effectuez l’une des opérations suivantes :

   * (Pour modifier le statut d’un seul compte) Placez le curseur sur le nom du compte, cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**. Remplacez le **[!UICONTROL Status]** par *Activé* ou *Désactivé*, puis cliquez sur **[!UICONTROL Post]**.

   * (Pour modifier le statut d’un ou de plusieurs comptes) Procédez comme suit :

      1. Cochez la case en regard de chaque compte.

         Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Icône Activer](/help/search-social-commerce/assets/activate.png "Icône Activer") pour activer le compte ou sur ![Icône Désactiver](/help/search-social-commerce/assets/disable.png "Icône Désactiver") pour le désactiver.

## Paramètres du compte réseau publicitaire {#account-settings}

>[!NOTE]
>
>Seuls le gestionnaire de compte d’agence, le gestionnaire de compte [!DNL Adobe] et les utilisateurs administrateurs peuvent configurer les paramètres du compte.

### Détails du compte

**[!UICONTROL SE Account ID]:** (tous les comptes, à l’exception des comptes [!DNL Naver] et [!DNL Yandex] ; modifiable uniquement pour les nouveaux comptes) Identifiant de compte attribué par le réseau publicitaire.

>[!NOTE]
>
>Les comptes Ad Network Manager ne sont pas pris en charge ici. Pour identifier un compte Manager pour [!DNL Microsoft Advertising] ou [!DNL Yandex], utilisez respectivement le champ ID de compte de Principal ou Compte MCC . Pour [configurer les informations d’identification d’un compte  [!DNL Google Ads]  responsable](/help/search-social-commerce/admin/manager-accounts.md), accédez à [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** nom à afficher pour le compte dans Search, Social et Commerce.

>[!NOTE]
>
>Si vous disposez d’une intégration Search, Social et Commerce-Adobe Analytics et que vous modifiez le nom du compte de recherche, contactez l’équipe chargée de votre compte Adobe pour qu’elle mette à jour le mappage.

**[!UICONTROL Login Details]: \[Type de connexion\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] uniquement) Autoriser ou non les connexions au compte à l’aide de :

* *[!UICONTROL oAuth]* (valeur par défaut) : pour utiliser le [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

* *[!UICONTROL Password]:* pour utiliser le mot de passe du client.

Pour les comptes [!DNL Microsoft Advertising], seules les connexions autorisées par le [!DNL oAuth] peuvent être utilisées.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (tous les réseaux publicitaires, à l’exception de [!DNL Naver]) nom ou ID de connexion permettant d’activer l’accès de l’API au compte.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] activé pour les [!DNL oAuth] et tous les autres réseaux à l’exception de [!DNL Meta] et [!DNL Yandex]) Jeton du compte pour autoriser les connexions à l’aide du [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Tous les réseaux publicitaires sauf [!DNL Naver]) Mot de passe du compte. Pour les comptes activés par mot de passe sur [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] et [!DNL Yandex], ce champ est obligatoire. Pour les comptes activés pour [!DNL oAuth], ce champ est facultatif ; utilisez-le lorsque vous souhaitez chiffrer et enregistrer le mot de passe afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** (comptes [!DNL Yandex] uniquement) Clé d’accès du compte de développeur à utiliser.

**[!UICONTROL Currency]:** abréviation de la devise utilisée pour le compte. Ce champ peut être modifié pour les nouveaux comptes [!DNL Naver]. Pour tous les autres réseaux de recherche, la valeur est automatiquement renseignée avec la devise configurée pour le compte sur le réseau publicitaire une fois que vous avez enregistré l’enregistrement.

**[!UICONTROL Landing Page Suffix]** (comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement ; facultatif) tous les paramètres à ajouter à la fin des URL finales pour effectuer le suivi des informations ; inclure tous les paramètres que votre entreprise doit effectuer le suivi.

Exemple : `param1=value1&param2=value2`

Les comptes qui utilisent le suivi des clics d’Adobe Advertising doivent inclure l’identifiant des clics du réseau publicitaire (`msclkid` par [!DNL Microsoft Advertising] ; `gclid` pour Google) dans le suffixe . Les comptes disposant d’une intégration Adobe Analytics doivent utiliser le paramètre AMO ID (en commençant par `s_kwcid`). Si le compte dispose d’une implémentation d’AMO ID côté serveur, le paramètre est ajouté automatiquement lorsqu’un utilisateur clique sur une publicité ; sinon, vous devez l’ajouter manuellement ici. Consultez les sections [Formats de suffixes requis pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et [Formats de suffixes requis pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Ce champ n&#39;est pas mis à jour par le paramètre de tracking [!UICONTROL Auto Upload].
>* Les suffixes d’URL finaux aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent est nécessaire pour les composants de compte individuels. Pour configurer un suffixe au niveau du groupe publicitaire ou à un niveau inférieur, utilisez l’éditeur du réseau publicitaire.

**Fuseau horaire :** (tous les réseaux publicitaires, à l’exception des [!DNL Baidu] et des [!DNL Yahoo! Display Network]) Fuseau horaire de l’annonceur. Ce champ est modifiable et facultatif pour les nouveaux comptes [!DNL Naver]. Pour tous les autres réseaux de recherche, la valeur est automatiquement renseignée avec le fuseau horaire configuré pour le compte Search, Social et Commerce de l’annonceur une fois l’enregistrement enregistré.

**Statut :** statut du compte dans Search, Social et Commerce :

* *Activé :* Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’il est pris en charge) et diffuse des enchères automatisées et/ou des budgets de campagne pour les campagnes des portfolios.
* *Désactivé :* la recherche, les réseaux sociaux et Commerce arrête toutes les activités sur le compte. Les données collectées alors que le compte était actif sont toujours stockées, mais les vues et rapports de gestion de campagne n’incluent pas les données de la période pendant laquelle le compte est en pause. Vous pourrez ensuite réactiver le compte pour reprendre l’activité avec le compte.

**Modèle de suivi** - (comptes [!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Yahoo! Japan Ads] uniquement ; facultatif) Modèle de suivi par défaut pour le compte, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors atterrissage et incorpore également l’URL finale/de la page de destination dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

* Pour incorporer l’URL finale :

   * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Pour obtenir une liste de paramètres indiquant les URL finales dans les modèles de tracking, reportez-vous à la [!DNL Microsoft Advertising]documentation[[!DNL Microsoft Advertising]  (](https://help.ads.microsoft.com/#apex/3/en/56799) uniquement) ou ([!DNL Google Ads] uniquement) aux paramètres « Modèle de tracking uniquement » dans la section Paramètres de [!DNL ValueTrack] disponibles dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] uniquement) Utilisez le `!{lpurl}` de paramètre pour indiquer l’URL de la page de destination.

* Vous pouvez éventuellement inclure des paramètres d’URL et tout paramètre personnalisé défini pour la campagne, séparés par des esperluettes (&amp;), tel que `{lpurl}?matchtype={matchtype}&device={device}`.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

* Lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

>[!NOTE]
>
>* Par [!DNL Google Ads], évitez d’utiliser des macros qui ne remplacent pas les clics provenant de sources permettant le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte Adobe doit collaborer avec le service clientèle ou l’équipe d’implémentation pour les ajouter.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres des mots-clés incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Si vous mettez à jour un modèle de suivi au niveau de l’annonce, du lien du site ou du mot-clé, les annonces pertinentes sont envoyées à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans envoyer à nouveau vos publicités pour approbation.

**[!UICONTROL Master Account ID]:** (comptes [!DNL Microsoft Advertising] uniquement) ID d’un compte d’agence/de gestion associé au compte.

**[!UICONTROL MCC Account]:** (comptes [!DNL Yandex] uniquement ; facultatif) Compte agence/de gestion associé au compte. Pour supprimer une association existante, sélectionnez « [!UICONTROL No MCC Account] ».

**[!UICONTROL Application ID]:** (comptes [!DNL Yandex] uniquement) Jeton de développement à utiliser pour le compte. Le même jeton est utilisé pour tous les comptes [!DNL Yandex].

**[!UICONTROL Purse Campaign ID]:** (comptes [!DNL Yandex] dont le paramètre Compte partagé est désactivé uniquement ; facultatif) Identifiant numérique de la campagne utilisé pour payer toutes les campagnes publicitaires du compte.

**[!UICONTROL Finance Token]:** (comptes [!DNL Yandex] avec le paramètre Compte partagé désactivé uniquement ; facultatif) Jeton de développement à utiliser pour les appels API liés à la finance, comme pour réaffecter de l’argent du portefeuille entre les campagnes de l’annonceur, si nécessaire pour l’optimisation du portefeuille.

### Suivi de compte

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

<!-- **[!UICONTROL Auto Upload]:** -->

{{$include /help/_includes/auto-upload.md}}

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Tracking Level]:** -->

{{$include /help/_includes/tracking-level.md}}

**[!UICONTROL Track Product Group]:** (pour les [!UICONTROL EF Redirect] uniquement) Non implémenté

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **Format S_kwcid :** (comptes [!DNL Google Ads] existants pour les annonceurs disposant d’une intégration Adobe Advertising-Adobe Analytics et pour lesquels l’AMO ID (s_kwcid) n’a pas déjà été migré)

Ce compte utilise le format hérité du code de suivi AMO ID, ce qui permet à Adobe Advertising de partager des données sur le compte avec Adobe Analytics. Le [dernier format](/help/integrations/analytics/ids.md#amo-id-formats) inclut des paramètres pour l’identifiant de campagne et l’identifiant de groupe publicitaire, qui sont nécessaires pour générer des rapports précis aux niveaux de la campagne et du groupe publicitaire pour [!DNL Google Ads] campagnes avec performances maximales et les campagnes sous forme de brouillons et d’expériences dans Analytics :

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Si ce compte doit créer des rapports au niveau de la campagne et du groupe publicitaire, cliquez sur l’icône [!UICONTROL Edit] (crayon), puis **[!UICONTROL Migrate to new s_kwcid format]** pour changer le nouveau format. Pour les comptes qui n’incluent pas ces types de campagne, la migration vers le nouveau format est facultative, mais recommandée.

Pour obtenir des instructions complètes, reportez-vous à « [&#x200B; Mettre à jour le code de suivi AMO ID pour un  [!DNL Google Ads]  compte &#x200B;](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md) ».

**Noms de suites de rapports :** (pour la redirection EF avec jeton uniquement ; annonceurs avec une intégration Adobe Advertising-Adobe Analytics ; facultatif) Une ou plusieurs suites de rapports Analytics auxquelles Search, Social et Commerce envoient les données qu’il collecte du réseau publicitaire, y compris les classifications d’entité et les données de clic pour le compte. Cette fonctionnalité est disponible uniquement pour les réseaux publicitaires pris en charge.

Pour que les données apparaissent dans les suites de rapports, (a) la fonction d’identifiant AMO côté serveur doit être configurée pour le compte ou (b) le paramètre au niveau de l’annonceur sur « [!UICONTROL Enable Advertising reporting in Analytics] » doit être activé. En outre, le compte Analytics de l’annonceur doit être configuré pour recevoir des données de Search, Social et Commerce. Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À propos des comptes de réseau publicitaire](ad-network-account-about.md)
>* [Gérer les comptes de centre commercial](merchant-account-manage.md)
>* [Mettre à jour le code de suivi s_kwcid pour un  [!DNL Google Ads] compte](update-amo-id-google.md)
