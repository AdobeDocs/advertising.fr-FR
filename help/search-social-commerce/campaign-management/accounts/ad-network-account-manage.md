---
title: Gestion des comptes de réseau publicitaire
description: Découvrez comment configurer et gérer les détails du compte pour un compte réseau publicitaire.
exl-id: 4038d03b-63e2-4953-89df-37f7b5f68652
feature: Search Campaign Management
source-git-commit: 68efad8ad3bc2985ac75a0f9437a2eafb194e4b6
workflow-type: tm+mt
source-wordcount: '2079'
ht-degree: 0%

---

# Gestion des comptes de réseau publicitaire

<!-- Probably need to change the page title. If I update the filename, get B. to create a redirect to the new URL. -->

Vous trouverez ci-dessous des instructions pour la création et la modification des détails d’un compte réseau, l’actualisation du jeton [!DNL oAuth] pour un compte et la désactivation des comptes.

<!-- Move out info about Naver?  Then change to the following:  Following are instructions for creating and editing account details for an ad network account that Search, Social, & Commerce will sync using the ad network's API; refreshing the [!DNL oAuth] token for an account; and disabling accounts. -->

<!-- Also update Description metadata to "Learn how to set up and manage account details for an ad network account synced via the ad network API." -->

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, voir &quot;[Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md)&quot;.

## Création de détails de compte réseau publicitaire {#create-account}

*Gestionnaire de compte de l’agence, gestionnaire de compte d’Adobe et rôles utilisateur administrateur uniquement*

Pour activer la synchronisation ou le suivi d’un compte, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et les options de suivi, avec l’état *actif*.

>[!NOTE]
>
>* La prise en charge n&#39;est pas disponible pour les nouveaux comptes [!DNL Baidu].
>* Pour créer un compte réel sur le réseau publicitaire, rendez-vous sur le site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Spécifiez les [paramètres du compte](#account-settings) :

   1. Cliquez sur le nom du réseau publicitaire, puis sur **[!UICONTROL Next]**.

   1. Dans la section **[!UICONTROL Account Details]**, saisissez les détails du compte.

      Pour les réseaux publicitaires qui utilisent le type d’autorisation de connexion &quot;[!UICONTROL oAuth]&quot;, autorisez Search, Social et Commerce à accéder au compte à l’aide du [protocole d’autorisation OAuth](https://oauth.net/2/) :

      1. Saisissez la valeur **[!UICONTROL Login]** du compte, éventuellement le mot de passe, puis cliquez sur **[!UICONTROL Authenticate]**.

         La bonne pratique consiste à utiliser la connexion pour l’accès de l’API au compte. Saisissez le mot de passe lorsque vous souhaitez le chiffrer et l’enregistrer, de sorte que l’équipe du compte d’Adobe puisse actualiser les jetons si nécessaire.

      1. (Si vous n’êtes pas connecté au compte de l’annonceur) Connectez-vous au compte publicitaire de l’annonceur. La bonne pratique consiste à utiliser les informations d’identification pour l’accès de l’API au compte.

      1. Dans l’écran de demande d’autorisation/d’accès, cliquez sur le bouton pour confirmer l’autorisation.

      1. Copiez la chaîne d’authentification dans la fenêtre contextuelle qui s’ouvre, puis collez-la dans le champ **[!UICONTROL oAuth Token]**.

      1. Indiquez les détails restants du compte.

   1. Cliquez sur **[!UICONTROL Set Account Tracking]** et saisissez les paramètres de suivi.

1. Cliquez sur **[!UICONTROL Post]**.

   Les données de coût et de clic récentes pour toutes les campagnes du compte sont disponibles dans Search, Social et Commerce en environ 24 heures. Par défaut, les données sont disponibles pendant les 5 à 10 derniers jours, selon le réseau publicitaire. Toutefois, si nécessaire, l’équipe de lancement du projet peut récupérer des données pendant les 60 derniers jours.

## Modifier les détails d’un compte réseau {#edit-account}

*Gestionnaire de compte de l’agence, gestionnaire de compte d’Adobe et rôles utilisateur administrateur uniquement*

Si les informations d’identification du compte changent, vous souhaitez modifier les paramètres de suivi par défaut d’un compte, ou activer ou désactiver l’activité sur un compte, puis modifier les détails du compte.

>[!NOTE]
>
>Pour modifier un compte réel sur le réseau publicitaire, rendez-vous sur le site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**.

1. Modifiez les [paramètres du compte](#account-settings) :

   1. (Facultatif) Modifiez les détails du compte.

   1. (Facultatif) Cliquez sur **[!UICONTROL Set Account Tracking]**, puis modifiez les paramètres de suivi.

1. Cliquez sur **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social et Commerce doivent synchroniser les nouvelles données de compte avec celles du réseau publicitaire. Cela se produit automatiquement une fois par jour, ou plus souvent lorsque Search, Social et Commerce détecte les modifications sur le réseau publicitaire.

## Actualisation des jetons d’accès oAuth pour les comptes de recherche {#refresh-oauth-tokens}

*Gestionnaire de compte de l’agence, gestionnaire de compte d’Adobe et rôles utilisateur administrateur uniquement*

Si Search, Social et Commerce accèdent au compte à l’aide du [protocole d’autorisation OAuth](https://oauth.net/2/) et que les informations d’identification du compte changent, ou si un accès supplémentaire est nécessaire pour prendre en charge les nouvelles fonctionnalités de Search, Social et Commerce, vous devez obtenir un nouveau jeton d’accès pour le compte.

Votre équipe de compte d’Adobe vous informera si de nouvelles fonctionnalités nécessitent un nouveau jeton.

1. (Si vous êtes connecté à un autre compte pour le même réseau publicitaire dans la même application de navigateur) Déconnectez-vous de tout compte autre que celui de l’annonceur.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**.

1. Obtenez un nouveau jeton d’accès :

   1. Cliquez sur **[!UICONTROL Get oAuth Token]**.

   1. (Si vous n’êtes pas connecté au compte de l’annonceur) Connectez-vous au compte publicitaire de l’annonceur. La bonne pratique consiste à utiliser les informations d’identification pour l’accès de l’API au compte.

   1. Dans l’écran de demande d’autorisation/d’accès, cliquez sur le bouton pour confirmer l’autorisation.

   1. Copiez la chaîne d’authentification dans la fenêtre contextuelle qui s’ouvre, puis collez-la dans le champ **[!UICONTROL oAuth Token]**.

1. Cliquez sur **[!UICONTROL Post]**.

## Activation ou désactivation de comptes réseau d’annonces {#enable-disable-account}

*Gestionnaire de compte de l’agence, gestionnaire de compte d’Adobe et rôles utilisateur administrateur uniquement*

Lorsque vous activez un compte de réseau publicitaire, Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’il est pris en charge) et envoie des offres automatisées et/ou des budgets de campagne pour les campagnes dans les portefeuilles. Lorsque vous désactivez un compte de réseau publicitaire, Search, Social et Commerce arrête toute activité sur le compte. Les données collectées pendant que le compte était actif sont toujours stockées, mais les vues et les rapports de gestion de campagne n’incluent pas les données de la période pendant laquelle le compte est désactivé. Vous pouvez par la suite réactiver le compte pour reprendre l’activité avec le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Effectuez l’une des opérations suivantes :

   * (Pour modifier l’état d’un compte unique) Placez le curseur sur le nom du compte, cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**. Remplacez **[!UICONTROL Status]** par *Enabled* ou *Disabled*, puis cliquez sur **[!UICONTROL Post]**.

   * (Pour modifier l’état d’un ou de plusieurs comptes) Procédez comme suit :

      1. Cochez la case en regard de chaque compte.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)&quot;.

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur l’icône ![Activer](/help/search-social-commerce/assets/activate.png "Icône Activer") pour activer le compte ou ![Icône Désactiver](/help/search-social-commerce/assets/disable.png "Icône Désactiver") pour désactiver le compte.

## Paramètres du compte réseau publicitaire {#account-settings}

>[!NOTE]
>
>Seuls le gestionnaire de compte d’agence, le gestionnaire de compte [!DNL Adobe] et les utilisateurs administrateurs peuvent configurer les paramètres du compte.

### Détails du compte

**[!UICONTROL SE Account ID]:** (Tous les comptes à l’exception des comptes [!DNL Naver] et [!DNL Yandex] ; modifiable uniquement pour les nouveaux comptes) ID de compte attribué par le réseau publicitaire.

>[!NOTE]
>
>Les comptes de gestionnaire de réseau publicitaire ne sont pas pris en charge ici. Pour identifier un compte de gestionnaire pour [!DNL Microsoft Advertising] ou [!DNL Yandex], utilisez respectivement le champ Identifiant de compte de Principal ou Compte MCC . Pour [ configurer les informations d’identification d’un  [!DNL Google Ads] compte de gestionnaire](/help/search-social-commerce/admin/manager-accounts.md), accédez à [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** nom à afficher pour le compte dans Search, Social et Commerce.

>[!NOTE]
>
>Si vous disposez d’une intégration Search, Social et Commerce-Adobe Analytics et que vous modifiez le nom du compte de recherche, informez votre équipe de compte d’Adobe afin qu’elle puisse mettre à jour le mappage.

**[!UICONTROL Login Details]: \[Type de connexion\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] uniquement) Indique s’il faut autoriser les connexions au compte à l’aide de :

* *[!UICONTROL oAuth]* (valeur par défaut) : pour utiliser le [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

* *[!UICONTROL Password]:* pour utiliser le mot de passe du client.

Pour les comptes [!DNL Microsoft Advertising], seules les connexions [!DNL oAuth] autorisées peuvent être utilisées.

**[!UICONTROL Login Details]: [!UICONTROL Login] :** (Tous les réseaux publicitaires à l’exception de [!DNL Naver]) Nom ou identifiant de connexion pour activer l’accès de l’API au compte.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token] :** ([!DNL Microsoft Advertising] [!DNL oAuth] avec activé et tous les autres réseaux, à l’exception de [!DNL Meta] et [!DNL Yandex]) Jeton du compte pour autoriser les connexions à l’aide du [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password] :** (Tous les réseaux publicitaires à l’exception de [!DNL Naver]) Mot de passe du compte. Pour les comptes activés par mot de passe sur [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] et [!DNL Yandex], ce champ est obligatoire. Pour les comptes [!DNL oAuth], ce champ est facultatif. Utilisez-le lorsque vous souhaitez chiffrer et enregistrer le mot de passe afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

**[!UICONTROL Login Details]: [!UICONTROL Access Key] :** ([!DNL Yandex] comptes uniquement) Clé d’accès du compte de développeur à utiliser.

**[!UICONTROL Currency]:** abréviation de la devise utilisée pour le compte. Ce champ est éditable pour les nouveaux comptes [!DNL Naver]. Pour tous les autres réseaux de recherche, la valeur est renseignée automatiquement avec la devise configurée pour le compte sur le réseau publicitaire une fois l’enregistrement enregistré.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] et [!DNL Microsoft Advertising] comptes uniquement ; facultatif) Tous les paramètres à ajouter à la fin des URL finales pour effectuer le suivi des informations ; incluez tous les paramètres dont votre entreprise doit effectuer le suivi.

Exemple : `param1=value1&param2=value2`

Les comptes qui utilisent le suivi des clics par Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`msclkid` pour [!DNL Microsoft Advertising] ; `gclid` pour Google) dans le suffixe . Les comptes avec une intégration Adobe Analytics doivent utiliser le paramètre AMO ID (commençant par `s_kwcid`). Si le compte dispose d’une mise en oeuvre AMO ID côté serveur, le paramètre est automatiquement ajouté lorsqu’un utilisateur clique sur une publicité. Dans le cas contraire, vous devez l’ajouter manuellement à cet emplacement. Voir les [ formats de suffixes requis pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et les [ formats de suffixes requis pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Ce champ n&#39;est pas mis à jour par le paramètre de suivi [!UICONTROL Auto Upload].
>* Les suffixes d’URL finaux aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur du réseau publicitaire.

**Fuseau horaire :** (Tous les réseaux publicitaires, à l’exception de [!DNL Baidu] et [!DNL Yahoo! Display Network]) Fuseau horaire de l’annonceur. Ce champ est modifiable et facultatif pour les nouveaux comptes [!DNL Naver]. Pour tous les autres réseaux de recherche, la valeur est automatiquement renseignée avec le fuseau horaire configuré pour le compte Search, Social et Commerce de l’annonceur une fois que vous avez enregistré l’enregistrement.

**État :** État du compte dans Search, Social, &amp; Commerce :

* *Activé :* La recherche, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’elle est prise en charge) et envoie des offres automatisées et/ou des budgets de campagne pour les campagnes dans les portefeuilles.
* *Désactivé :* la recherche, Social et Commerce arrêtent toutes les activités du compte. Les données collectées pendant que le compte était actif sont toujours stockées, mais les vues et les rapports de gestion de campagne n’incluent pas les données pour la période pendant laquelle le compte est suspendu. Vous pouvez réactiver ultérieurement le compte pour reprendre l’activité avec le compte.

**Modèle de suivi** - ([!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Yahoo! Japan Ads] comptes uniquement ; facultatif) Le modèle de suivi par défaut du compte, qui spécifie tous les paramètres de suivi et redirections de domaine hors entrée et incorpore également l’URL de la dernière page/d’entrée dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

* Pour incorporer l’URL finale :

   * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Pour obtenir une liste de paramètres permettant d’indiquer les URL finales dans les modèles de suivi, voir les paramètres ([!DNL Microsoft Advertising] uniquement) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou ([!DNL Google Ads] uniquement) &quot;Modèle de suivi uniquement&quot; dans la section &quot;Paramètres disponibles [!DNL ValueTrack]&quot; de la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] uniquement) Utilisez le paramètre `!{lpurl}` pour indiquer l’URL de la page d’entrée.

* Vous pouvez éventuellement inclure des paramètres d’URL et des paramètres personnalisés définis pour la campagne, séparés par des esperluettes (&amp;), tels que `{lpurl}?matchtype={matchtype}&device={device}`.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

* Lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload]&quot;, Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lors de l’enregistrement.

>[!NOTE]
>
>* Pour [!DNL Google Ads], évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit collaborer avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres du mot-clé incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Si vous mettez à jour un modèle de suivi au niveau de la publicité, du lien de site ou du mot-clé, les publicités pertinentes sont soumises à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans soumettre à nouveau vos publicités pour approbation.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] comptes uniquement) ID d’un compte d’agence/de gestion associé au compte.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] comptes uniquement ; facultatif) compte d’agence/de gestion associé au compte. Pour supprimer une association existante, sélectionnez &quot;[!UICONTROL No MCC Account]&quot;.

**[!UICONTROL Application ID]:** ([!DNL Yandex] comptes uniquement) Jeton de développeur à utiliser pour le compte. Le même jeton est utilisé pour tous les comptes [!DNL Yandex].

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] comptes avec le paramètre Compte partagé désactivé uniquement ; facultatif) identifiant numérique de la campagne utilisée pour payer toutes les campagnes publicitaires dans le compte.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] comptes avec le paramètre Compte partagé désactivé uniquement ; facultatif) Jeton de développeur à utiliser pour les appels API liés au financement, tels que la réallocation de l’argent du portefeuille entre les campagnes de l’annonceur, selon les besoins pour l’optimisation du portefeuille.

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

**[!UICONTROL Track Product Group]:** (Pour [!UICONTROL EF Redirect] uniquement) Non implémenté

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

* **Format S_kwcid :** (comptes [!DNL Google Ads] existants pour les annonceurs avec une intégration Adobe Advertising-Adobe Analytics et pour lesquels l’AMO ID (s_kwcid) n’a pas déjà été migré)

Ce compte utilise le format hérité du code de suivi AMO ID, ce qui permet à l’Adobe Advertising de partager les données relatives au compte avec Adobe Analytics. Le [dernier format](/help/integrations/analytics/ids.md#amo-id-formats) comprend des paramètres pour l’identifiant de campagne et l’identifiant du groupe publicitaire, qui sont nécessaires pour générer des rapports précis aux niveaux de campagne et de groupe publicitaire pour [!DNL Google Ads] les performances maximales des campagnes, des brouillons et des campagnes d’expérience dans Analytics :

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Si ce compte doit générer des rapports aux niveaux de la campagne et du groupe publicitaire, cliquez sur l’icône [!UICONTROL Edit] (crayon), puis sur **[!UICONTROL Migrate to new s_kwcid format]** pour passer au nouveau format. Pour les comptes qui n’incluent pas ces types de campagne, la migration vers le nouveau format est facultative, mais recommandée.

Pour obtenir des instructions complètes, voir &quot;[Mise à jour du code de suivi AMO ID pour un [!DNL Google Ads] compte](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)&quot;.

**Noms de suites de rapports :** (Pour une redirection EF avec jeton uniquement ; annonceurs avec une intégration Adobe Advertising-Adobe Analytics ; facultatif) Une ou plusieurs suites de rapports Analytics auxquelles Search, Social et Commerce envoie les données qu’il collecte à partir du réseau publicitaire, y compris les classifications d’entités et les données de clic pour le compte. Cette fonctionnalité est disponible uniquement pour les réseaux publicitaires pris en charge.

Pour que les données apparaissent dans les suites de rapports, soit (a) la fonction AMO ID côté serveur doit être configurée pour le compte, soit (b) le paramètre au niveau de l’annonceur sur &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; doit être activé. En outre, le compte Analytics de l’annonceur doit être configuré pour recevoir les données de Search, Social et Commerce. Pour plus d’informations, contactez votre équipe de compte d’Adobe.

>[!MORELIKETHIS]
>
>* [À propos des comptes réseau d’annonces](ad-network-account-about.md)
>* [Gérer les comptes de centre commercial](merchant-account-manage.md)
>* [Mettre à jour le code de suivi s_kwcid pour un  [!DNL Google Ads] compte](update-amo-id-google.md)
