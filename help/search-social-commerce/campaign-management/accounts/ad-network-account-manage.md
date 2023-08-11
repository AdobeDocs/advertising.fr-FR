---
title: Gestion des comptes de réseau publicitaire
description: Découvrez comment configurer et gérer les détails du compte pour un compte réseau publicitaire.
exl-id: fd8b38bd-24d0-488c-9e57-a516f5ae67ac
feature: Search Campaign Management
source-git-commit: ca9425333731ada692c68f08b20f070265eb3409
workflow-type: tm+mt
source-wordcount: '2086'
ht-degree: 0%

---

# Gestion des comptes de réseau publicitaire

Vous trouverez ci-dessous des instructions sur la création et la modification des détails d’un compte réseau, en actualisant la variable [!DNL oAuth] pour un compte et en désactivant les comptes.

## Création de détails de compte réseau publicitaire {#create-account}

*Rôles utilisateur du gestionnaire de compte de l’agence, du gestionnaire de compte d’Adobe et de l’administrateur uniquement*

Pour activer la synchronisation ou le suivi d’un compte, vous devez créer un enregistrement de compte correspondant contenant les options de suivi et les informations d’identification d’accès au compte, et avec l’état . *principal*. Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, voir &quot;[Inventaire pris en charge](/help/search-social-commerce/introduction/supported-inventory.md).&quot;

>[!NOTE]
>
>Pour créer un compte réel sur le réseau publicitaire, rendez-vous sur le site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Spécifiez la variable [paramètres du compte](#account-settings):

   1. Cliquez sur le nom du réseau publicitaire, puis sur **[!UICONTROL Next]**.

   1. Dans le **[!UICONTROL Account Details]** , saisissez les détails du compte.

      Pour les réseaux publicitaires qui utilisent le type d’autorisation de connexion &quot;[!UICONTROL oAuth],&quot; permettent à Search, Social et Commerce d’accéder au compte à l’aide de la variable [Protocole d’autorisation OAuth](https://oauth.net/2/):

      1. Saisissez le **[!UICONTROL Login]** pour le compte, saisissez éventuellement le mot de passe, puis cliquez sur **[!UICONTROL Authenticate]**.

         La bonne pratique consiste à utiliser la connexion pour l’accès de l’API au compte. Saisissez le mot de passe lorsque vous souhaitez le chiffrer et l’enregistrer, de sorte que l’équipe du compte d’Adobe puisse actualiser les jetons si nécessaire.

      1. (Si vous n’êtes pas connecté au compte de l’annonceur) Connectez-vous au compte publicitaire de l’annonceur. La bonne pratique consiste à utiliser les informations d’identification pour l’accès de l’API au compte.

      1. Dans l’écran de demande d’autorisation/d’accès, cliquez sur le bouton pour confirmer l’autorisation.

      1. Copiez la chaîne d’authentification dans la fenêtre contextuelle qui s’ouvre, puis collez-la dans le **[!UICONTROL oAuth Token]** champ .

      1. Indiquez les détails restants du compte.

   1. Cliquez sur **[!UICONTROL Set Account Tracking]**, puis saisissez les paramètres de suivi.

1. Cliquez sur **[!UICONTROL Post]**.

   Les données de coût et de clic récentes pour toutes les campagnes du compte sont disponibles dans Search, Social et Commerce en environ 24 heures. Par défaut, les données sont disponibles pendant les 5 à 10 derniers jours, selon le réseau publicitaire. Toutefois, si nécessaire, l’équipe de lancement du projet peut récupérer des données pendant les 60 derniers jours.

## Modifier les détails d’un compte réseau {#edit-account}

*Rôles utilisateur du gestionnaire de compte de l’agence, du gestionnaire de compte d’Adobe et de l’administrateur uniquement*

Si les informations d’identification du compte changent, vous souhaitez modifier les paramètres de suivi par défaut d’un compte, ou activer ou désactiver l’activité sur un compte, puis modifier les détails du compte.

>[!NOTE]
>
>Pour modifier un compte réel sur le réseau publicitaire, rendez-vous sur le site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, puis cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**.

1. Modifiez la variable [paramètres du compte](#account-settings):

   1. (Facultatif) Modifiez les détails du compte.

   1. (Facultatif) Cliquez sur **[!UICONTROL Set Account Tracking]** et modifiez les paramètres de suivi.

1. Cliquez sur **[!UICONTROL Post]**.

   >[!NOTE]
   >
   >Search, Social et Commerce doivent synchroniser les nouvelles données de compte avec celles du réseau publicitaire. Cela se produit automatiquement une fois par jour, ou plus souvent lorsque Search, Social et Commerce détecte les modifications sur le réseau publicitaire.

## Actualisation des jetons d’accès oAuth pour les comptes de recherche {#refresh-oauth-tokens}

*Rôles utilisateur du gestionnaire de compte de l’agence, du gestionnaire de compte d’Adobe et de l’administrateur uniquement*

Si Search, Social et Commerce accède au compte à l’aide de la variable [Protocole d’autorisation OAuth](https://oauth.net/2/) et les informations d’identification du compte changent, ou si un accès supplémentaire est nécessaire pour prendre en charge les nouvelles fonctionnalités de Search, Social et Commerce, vous devez obtenir un nouveau jeton d’accès pour le compte.

Votre équipe de compte d’Adobe vous informera si de nouvelles fonctionnalités nécessitent un nouveau jeton.

1. (Si vous êtes connecté à un autre compte pour le même réseau publicitaire dans la même application de navigateur) Déconnectez-vous de tout compte autre que celui de l’annonceur.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Placez le curseur sur le nom du compte, puis cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**.

1. Obtenez un nouveau jeton d’accès :

   1. Cliquez sur **[!UICONTROL Get oAuth Token]**.

   1. (Si vous n’êtes pas connecté au compte de l’annonceur) Connectez-vous au compte publicitaire de l’annonceur. La bonne pratique consiste à utiliser les informations d’identification pour l’accès de l’API au compte.

   1. Dans l’écran de demande d’autorisation/d’accès, cliquez sur le bouton pour confirmer l’autorisation.

   1. Copiez la chaîne d’authentification dans la fenêtre contextuelle qui s’ouvre, puis collez-la dans le **[!UICONTROL oAuth Token]** champ .

1. Cliquez sur **[!UICONTROL Post]**.

## Activation ou désactivation de comptes réseau d’annonces {#enable-disable-account}

*Rôles utilisateur du gestionnaire de compte de l’agence, du gestionnaire de compte d’Adobe et de l’administrateur uniquement*

Lorsque vous activez un compte de réseau publicitaire, Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’il est pris en charge) et envoie des offres automatisées et/ou des budgets de campagne pour les campagnes dans les portefeuilles. Lorsque vous désactivez un compte de réseau publicitaire, Search, Social et Commerce arrête toutes les activités du compte. Les données collectées pendant que le compte était principal sont toujours stockées, mais les vues et les rapports de gestion de campagne n’incluent pas les données de la période pendant laquelle le compte est désactivé. Vous pouvez par la suite réactiver le compte pour reprendre l’activité avec le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. Dans le sous-menu, cliquez sur **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. Effectuez l’une des opérations suivantes :

   * (Pour modifier l’état d’un compte unique) Placez le curseur sur le nom du compte, cliquez sur ![Plus](/help/search-social-commerce/assets/more-filters.png "Plus"), puis sélectionnez **[!UICONTROL Edit]**. Modifiez la variable **[!UICONTROL Status]** to *Activé* ou *Désactivé*, puis cliquez sur **[!UICONTROL Post]**.

   * (Pour modifier l’état d’un ou de plusieurs comptes) Procédez comme suit :

      1. Cochez la case en regard de chaque compte.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Icône Activer](/help/search-social-commerce/assets/activate.png "Icône Activer") pour activer le compte ou ![Icône Désactiver](/help/search-social-commerce/assets/disable.png "Icône Désactiver") pour désactiver le compte.

## Paramètres du compte réseau publicitaire {#account-settings}

>[!NOTE]
>
>Seul le gestionnaire de compte de l&#39;agence, [!DNL Adobe] le gestionnaire de compte et les utilisateurs administrateurs peuvent configurer les paramètres du compte.

### Détails du compte

**[!UICONTROL SE Account ID]:** (Tous les comptes sauf [!DNL Naver] et [!DNL Yandex] Comptes ; modifiable uniquement pour les nouveaux comptes) Identifiant de compte attribué par le réseau publicitaire.

>[!NOTE]
>
>Les comptes de gestionnaire de réseau publicitaire ne sont pas pris en charge ici. Pour identifier un compte de gestionnaire pour [!DNL Microsoft Advertising] ou [!DNL Yandex], utilisez respectivement le champ Identifiant de compte de Principal ou Compte MCC . À [configurer les informations d’identification d’un [!DNL Google Ads] compte manager](/help/search-social-commerce/admin/manager-accounts.md), accédez à [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Account Name]:** Nom à afficher pour le compte dans Search, Social et Commerce.

>[!NOTE]
>
>Si vous disposez d’une intégration Search, Social, &amp; Commerce-Adobe Analytics et que vous modifiez le nom du compte de recherche, informez votre équipe de compte d’Adobe afin qu’elle puisse mettre à jour le mappage.

**[!UICONTROL Login Details]: \[Type de connexion\]** - ([!DNL Microsoft Advertising]/[!DNL Microsoft Merchant Center] uniquement) Si vous souhaitez autoriser des connexions au compte à l’aide des éléments suivants :

* *[!UICONTROL oAuth]* (valeur par défaut) : pour utiliser la variable [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

* *[!UICONTROL Password]:* Pour utiliser le mot de passe du client.

Pour [!DNL Microsoft Advertising] comptes, uniquement [!DNL oAuth]-authorized logins peut être utilisé.

**[!UICONTROL Login Details]: [!UICONTROL Login]:** (Tous les réseaux publicitaires sauf [!DNL Naver]) Nom ou identifiant de connexion pour activer l’accès de l’API au compte.

**[!UICONTROL Login Details]: [!UICONTROL OAuth Token]:** ([!DNL Microsoft Advertising] [!DNL oAuth]-enabled et tous les autres réseaux, à l’exception de [!DNL Baidu], [!DNL Meta], et [!DNL Yandex]) Jeton du compte pour autoriser les connexions à l’aide de la variable [[!DNL OAuth] protocole d’autorisation](https://oauth.net/2/).

**[!UICONTROL Login Details]: [!UICONTROL Password]:** (Tous les réseaux publicitaires sauf [!DNL Naver]) Mot de passe du compte. Pour les comptes activés par mot de passe sur [!DNL Baidu], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], et [!DNL Yandex], ce champ est obligatoire. Pour [!DNL oAuth]comptes activés, ce champ est facultatif. Utilisez-le lorsque vous souhaitez chiffrer et enregistrer le mot de passe afin que le gestionnaire de compte puisse actualiser les jetons si nécessaire.

**[!UICONTROL Login Details]: [!UICONTROL Access Key]:** ([!DNL Baidu] et [!DNL Yandex] Comptes uniquement) La clé d’accès du compte développeur à utiliser.

**[!UICONTROL Currency]:** Abréviation de la devise utilisée pour le compte. Ce champ peut être modifié pour la nouvelle [!DNL Naver] comptes. Pour tous les autres réseaux de recherche, la valeur est renseignée automatiquement avec la devise configurée pour le compte sur le réseau publicitaire une fois l’enregistrement enregistré.

**[!UICONTROL Landing Page Suffix]** ([!DNL Google Ads] et [!DNL Microsoft Advertising] Comptes uniquement ; facultatif) Tout paramètre à ajouter à la fin des URL finales pour effectuer le suivi des informations ; incluez tous les paramètres dont votre entreprise doit effectuer le suivi.

Exemple : `param1=value1&param2=value2`

Les comptes qui utilisent le suivi des clics par Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`msclkid` pour [!DNL Microsoft Advertising]; `gclid` pour Google) dans le suffixe . Les comptes avec une intégration Adobe Analytics doivent utiliser le paramètre AMO ID (en commençant par `s_kwcid`). Si le compte dispose d’une mise en oeuvre AMO ID côté serveur, le paramètre est automatiquement ajouté lorsqu’un utilisateur clique sur une publicité. Dans le cas contraire, vous devez l’ajouter manuellement à cet emplacement. Voir [formats de suffixes requis pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et [formats de suffixes requis pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Ce champ n’est pas mis à jour par la variable [!UICONTROL Auto Upload] paramètre de suivi.
>* Les suffixes d’URL finaux aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur du réseau publicitaire.

**Fuseau horaire :** (Tous les réseaux publicitaires sauf [!DNL Baidu] et [!DNL Yahoo! Display Network]) Fuseau horaire de l’annonceur. Ce champ est modifiable et facultatif pour la nouvelle [!DNL Naver] comptes. Pour tous les autres réseaux de recherche, la valeur est automatiquement renseignée avec le fuseau horaire configuré pour le compte Search, Social, &amp; Commerce de l’annonceur une fois que vous avez enregistré l’enregistrement.

**État :** État du compte dans Search, Social et Commerce :

* *Activé :* Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’elles sont prises en charge) et envoie des offres automatisées et/ou des budgets de campagne pour les campagnes dans les portefeuilles.
* *Désactivé :* La recherche, Social et Commerce arrêtent toutes les activités du compte. Les données collectées pendant que le compte était principal sont toujours stockées, mais les vues et les rapports de gestion de campagne n’incluent pas les données pour la période pendant laquelle le compte est suspendu. Vous pouvez réactiver ultérieurement le compte pour reprendre l’activité avec le compte.

**Modèle de suivi** - ([!DNL Google Ads], [!DNL Microsoft Advertising], et [!DNL Yahoo! Japan Ads] Comptes uniquement ; facultatif) Le modèle de suivi par défaut du compte, qui spécifie tous les paramètres de suivi et redirections de domaine hors entrée et incorpore également l’URL de la page d’entrée/finale dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

* Pour incorporer l’URL finale :

   * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Pour obtenir une liste des paramètres permettant d’indiquer les URL finales dans les modèles de suivi, voir ([!DNL Microsoft Advertising] uniquement) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou ([!DNL Google Ads] uniquement) les paramètres &quot;Modèle de tracking uniquement&quot; dans la section &quot;Disponible&quot; [!DNL ValueTrack] Paramètres&quot; dans la variable [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

   * ([!DNL Yahoo! Japan Ads] uniquement) Utiliser le paramètre `!{lpurl}` pour indiquer l&#39;URL de la landing page.

* Vous pouvez éventuellement inclure des paramètres d’URL et des paramètres personnalisés définis pour la campagne, séparés par des esperluettes (&amp;), tels que `{lpurl}?matchtype={matchtype}&device={device}`.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

* Lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

>[!NOTE]
>
>* Pour [!DNL Google Ads], évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit collaborer avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres du mot-clé incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Si vous mettez à jour un modèle de suivi au niveau de la publicité, du lien de site ou du mot-clé, les publicités pertinentes sont soumises à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans soumettre à nouveau vos publicités pour approbation.

**[!UICONTROL Master Account ID]:** ([!DNL Microsoft Advertising] Comptes uniquement) L’identifiant d’un compte d’agence/de gestion associé au compte.

**[!UICONTROL MCC Account]:** ([!DNL Yandex] Comptes uniquement ; facultatif) un compte d’agence/de gestion associé au compte. Pour supprimer une association existante, sélectionnez &quot;[!UICONTROL No MCC Account].&quot;

**[!UICONTROL Application ID]:** ([!DNL Yandex] Comptes uniquement) Jeton de développeur à utiliser pour le compte. Le même jeton est utilisé pour tous les [!DNL Yandex] comptes.

**[!UICONTROL Purse Campaign ID]:** ([!DNL Yandex] comptes dont le paramètre Compte partagé est désactivé uniquement ; facultatif) identifiant numérique de la campagne qui sera utilisé pour payer toutes les campagnes publicitaires du compte.

**[!UICONTROL Finance Token]:** ([!DNL Yandex] comptes pour lesquels le paramètre Compte partagé est désactivé uniquement ; facultatif) Jeton de développeur à utiliser pour les appels d’API liés à la finance, comme la réaffectation de l’argent du portefeuille entre les campagnes de l’annonceur, selon les besoins pour l’optimisation de portefeuille.

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

* **Format S_kwcid** - (Existant [!DNL Google Ads] les comptes des annonceurs avec une intégration Adobe Advertising-Adobe Analytics et pour lesquels l’AMO ID (s_kwcid) n’a pas déjà été migré ;

Ce compte utilise le format hérité du code de suivi AMO ID, ce qui permet à l’Adobe Advertising de partager les données relatives au compte avec Adobe Analytics. La variable [dernier format](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md) comprend des paramètres pour l’identifiant de campagne et l’identifiant du groupe publicitaire, qui sont nécessaires pour générer des rapports précis aux niveaux de la campagne et du groupe publicitaire pour [!DNL Google Ads] performances max des campagnes et des campagnes de brouillons et d’expériences dans Analytics :

`s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

Si ce compte doit générer des rapports aux niveaux de la campagne et du groupe publicitaire, cliquez sur le bouton [!UICONTROL Edit] (crayon), puis **[!UICONTROL Migrate to new s_kwcid format]** pour changer le nouveau format. Pour les comptes qui n’incluent pas ces types de campagne, la migration vers le nouveau format est facultative, mais recommandée.

Pour obtenir des instructions complètes, voir &quot;[Mettre à jour le code de suivi AMO ID pour un [!DNL Google Ads] account](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md).&quot;

**Noms de suites de rapports** - (Pour la redirection EF avec jeton uniquement ; les annonceurs avec une intégration Adobe Advertising-Adobe Analytics ; facultatif) Une ou plusieurs suites de rapports Analytics auxquelles Search, Social et Commerce envoie les données qu’ils collectent depuis le réseau publicitaire, y compris les classifications d’entités et les données de clic pour le compte. Cette fonctionnalité est disponible uniquement pour les réseaux publicitaires pris en charge.

Pour que les données s’affichent dans les suites de rapports, soit (a) la fonction AMO ID côté serveur doit être configurée pour le compte, soit (b) le paramètre au niveau de l’annonceur sur &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; doit être activé. En outre, le compte Analytics de l’annonceur doit être configuré pour recevoir les données de Search, Social et Commerce. Pour plus d’informations, contactez votre gestionnaire de compte Adobe.

>[!MORELIKETHIS]
>
>* [A propos des comptes de réseau publicitaire](ad-network-account-about.md)
>* [Gestion des comptes de centre commercial](merchant-account-manage.md)
>* [Mettre à jour le code de suivi s_kwcid pour un [!DNL Google Ads] account](update-amo-id-google.md)
