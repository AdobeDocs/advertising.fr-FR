---
title: (Nouvelle interface utilisateur) Gestion des comptes réseau et
description: Découvrez comment configurer et gérer les détails du compte dans la nouvelle interface utilisateur pour un réseau publicitaire synchronisé via l’API du réseau publicitaire.
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '2129'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gérer les comptes réseau publicitaire via une connexion API

<!-- Besides just logging into an account, do you have to make any other choices once you're logged in (such as to give speciic permissions to SSC?  And what about oAuth tokens -- do we still use them? -->

*Fonction Beta*

<!-- Move out info about Naver into a separate page -->

Vous trouverez ci-dessous des instructions pour gérer les comptes de réseau publicitaire qui se synchronisent avec Search, Social et Commerce à l’aide de l’API du réseau publicitaire.

<!-- Move out info about Naver into a separate page -->

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [&#x200B; Inventaire pris en charge &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md).

## Créer un compte réseau publicitaire {#create-account}

Pour activer la synchronisation d’un compte, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et les options de suivi, ainsi que le statut *activé*.

>[!NOTE]
>
>Pour créer un compte sur le réseau publicitaire, accédez au site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Cliquez sur **[!UICONTROL Create Account]**.

1. Cliquez sur le nom du réseau publicitaire, puis sur **[!UICONTROL Next]**.

1. (Tous les réseaux publicitaires, à l’exception de [!DNL Yandex]) Connectez-vous au réseau publicitaire à l’aide des informations d’identification de l’annonceur. Sélectionnez l’option « Suivi des comptes pour ce compte ». Ensuite, en haut à droite, cliquez sur **[!UICONTROL Next]**.

1. Spécifiez les [paramètres du compte](#account-settings-api) :

   1. Dans l’onglet **[!UICONTROL Select Accounts]** , spécifiez les paramètres généraux du compte. Pour les comptes [!DNL Yandex], spécifiez les informations d’identification du compte.

   1. Cliquez sur l’onglet **[!UICONTROL Setup Tracking]** et renseignez les paramètres de tracking.

   1. (Annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md)) Cliquez sur l’onglet **[!UICONTROL Set up Adobe Analytics]** et sélectionnez toutes les suites de rapports [!DNL Analytics] à utiliser pour le suivi et les rapports d’activité de campagne.

1. Cliquez sur **[!UICONTROL Save]**.

   Les données récentes de coût et de clic pour toutes les campagnes du compte sont mises à jour toutes les heures dans Search, Social et Commerce. Par défaut, les données sont disponibles pour les 5 à 10 derniers jours, selon le réseau publicitaire. Cependant, si nécessaire, l’équipe de lancement du projet peut récupérer les données des 60 derniers jours au maximum.

## Modifier les détails du compte réseau publicitaire {#edit-account}

Pour réauthentifier les paramètres du compte afin d’actualiser les autorisations de connexion ou de mise à jour, activez ou désactivez l’activité sur un compte, modifiez les paramètres de suivi par défaut sur un compte ou modifiez les suites de rapports [!DNL Analytics] à utiliser pour le suivi et les rapports, puis modifiez les détails du compte.

>[!NOTE]
>
>Pour modifier un compte réel sur le réseau publicitaire, accédez au site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Sélectionnez le compte de l’une des manières suivantes :

   * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

   * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

1. Modifiez les [paramètres du compte](#account-settings-api) :

   1. (Facultatif) Dans l’onglet **[!UICONTROL Account Details]** , modifiez les détails du compte.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Setup Tracking]** et modifiez les paramètres de suivi.

   1. (Facultatif ; annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md)) Cliquez sur l’onglet **[!UICONTROL Set up Adobe Analytics]** et modifiez les suites de rapports [!DNL Analytics] à utiliser pour le suivi et les rapports d’activité de campagne.

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. Cliquez sur **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social et Commerce doivent synchroniser les nouvelles données de compte avec celles du réseau publicitaire. Cela se produit automatiquement une fois par jour, ou plus souvent lorsque Search, Social et Commerce détecte des modifications sur le réseau publicitaire.

## Réauthentifier un compte réseau publicitaire {#reauthenticate}

Pour actualiser la connexion au réseau publicitaire ou mettre à jour les autorisations pour le compte, réauthentifiez le compte.

1. (Si vous êtes connecté à un autre compte pour le même réseau publicitaire dans la même application de navigateur) Déconnectez-vous de tout compte autre que celui de l’annonceur.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

<!-- For Bing and Yandex, the right-click menu includes "Re authenticate." Clarify why just those types -->

1. Sélectionnez le compte de l’une des manières suivantes :

   * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

   * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

1. Dans l’onglet **[!UICONTROL Account Details]** , cliquez sur **[!UICONTROL Re authenticate]** et connectez-vous au réseau publicitaire à l’aide des informations d’identification de l’annonceur.

1. Cliquez sur **[!UICONTROL Save]**.

## Activer ou désactiver les comptes réseau publicitaires {#enable-disable-account}

Lorsque vous activez un compte de réseau publicitaire, Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’il est pris en charge) et diffuse des enchères automatisées et/ou des budgets de campagne pour les campagnes des portfolios. Lorsque vous désactivez un compte de réseau publicitaire, Search, Social et Commerce arrête toute activité sur le compte. Les données collectées alors que le compte était actif sont toujours stockées, mais les vues et rapports de gestion de campagne n’incluent pas les données de la période au cours de laquelle le compte est désactivé. Vous pourrez par la suite réactiver le compte pour reprendre l’activité avec le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Effectuez l’une des opérations suivantes :

   * (Vue [!UICONTROL Accounts]) :

      * (Pour activer le compte) Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Activate]** dans la barre d’outils des actions en bloc.

      * (Pour désactiver le compte) Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Pause]** dans la barre d’outils des actions en bloc.

   * (Dans les paramètres du compte) :

      1. Sélectionnez le compte de l’une des manières suivantes :

         * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

         * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

      1. Dans l’onglet **[!UICONTROL Account Details]** , désactivez **[!UICONTROL Account enabled]**.

      1. Cliquez sur **[!UICONTROL Save]**.

## Paramètres du compte réseau publicitaire {#account-settings-api}

Les paramètres du compte varient selon le réseau publicitaire. Il se peut que vous ne voyiez pas tous les paramètres ci-dessous.

<!-- When you're creating new accounts only; not sure that you'll have anything to do here once you've authenticated

### Authenticate tab

-->

### Onglet [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** nom à afficher pour le compte dans Search, Social et Commerce.

>[!NOTE]
>
>Si vous disposez d’une intégration Search, Social et Commerce-Adobe Analytics et que vous modifiez le nom du compte de recherche, demandez à l’équipe chargée de votre compte Adobe de mettre à jour le mappage.

**[!DNL [Ad Network] Accounts]:** (visible lorsque vous créez un compte) Compte du réseau publicitaire à synchroniser.

**[Informations de connexion]:** (comptes Yandex uniquement) Informations d’identification du compte à utiliser :

* **[!UICONTROL Login]:** nom ou ID de connexion permettant d’activer l’accès API au compte.

* **[!UICONTROL Password]:** mot de passe du compte.

* **[!UICONTROL Access Key]:** clé d’accès du compte de développeur à utiliser.

* **[!UICONTROL Application ID]:** jeton de développement à utiliser pour le compte. Le même jeton est utilisé pour tous les comptes [!DNL Yandex].

* **[!UICONTROL Purse Campaign ID]:** (comptes [!DNL Yandex] dont le paramètre Compte partagé est désactivé uniquement ; facultatif) Identifiant numérique de la campagne utilisé pour payer toutes les campagnes publicitaires du compte.

* **[!UICONTROL Finance Token]:** (comptes [!DNL Yandex] avec le paramètre Compte partagé désactivé uniquement ; facultatif) Jeton de développement à utiliser pour les appels API liés à la finance, comme pour réaffecter de l’argent du portefeuille entre les campagnes de l’annonceur, si nécessaire pour l’optimisation du portefeuille.

**[!UICONTROL Network Account ID]:** (Tous les réseaux publicitaires, à l’exception de [!DNL Yandex] ID de compte attribué par le réseau publicitaire.

>[!NOTE]
>
>Les comptes Ad Network Manager ne sont pas pris en charge ici. Pour identifier un compte Manager pour [!DNL Microsoft Advertising], utilisez respectivement le champ ID de compte de Principal ou Compte MCC . Pour [configurer les informations d’identification d’un compte  [!DNL Google Ads]  responsable](/help/search-social-commerce/admin/manager-accounts.md), accédez à [!UICONTROL Admin] \> [!UICONTROL Manager Accounts].

**[!UICONTROL Currency]:** (Lecture seule) Abréviation de la devise utilisée pour le compte. Cette valeur est automatiquement renseignée avec la devise configurée pour le compte sur le réseau publicitaire une fois l’enregistrement enregistré.

**[!UICONTROL Time Zone]:** Fuseau horaire de l’annonceur. Cette valeur est automatiquement renseignée avec le fuseau horaire configuré pour le compte Search, Social et Commerce de l’annonceur une fois l’enregistrement enregistré.

**[!UICONTROL Login]:** (Lecture seule) Compte utilisateur utilisé pour se connecter au compte.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled] :** Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’il est pris en charge) et diffuse des enchères automatisées et/ou des budgets de campagne pour les campagnes des portfolios.

## onglet [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** permet d’activer ou non le suivi à l’aide du service de suivi des conversions d’Adobe Advertising. Cette méthode génère des identifiants de suivi des clics uniques et redirige les utilisateurs vers le serveur Adobe Advertising à des fins de suivi avant de les envoyer à la page de destination du client. Cette méthode comporte des options de tracking par défaut que vous pouvez éventuellement personnaliser. Vous pouvez également spécifier des paramètres à ajouter à chaque URL.

Pour activer cette fonctionnalité, activez **[Activer le suivi]**.

>[!NOTE]
>
>* Si vous modifiez ce paramètre, vous devez régénérer les URL de tracking pour le compte.
>* Les options de tracking au niveau de la campagne remplacent les paramètres au niveau du compte.

**[!UICONTROL Tracking Type]:** (lorsque le suivi Search, Social et Commerce est activé) Méthode de redirection des utilisateurs finaux vers l’URL finale ou l’URL de destination. L’option sélectionnée s’applique à toutes les unités d’enchères du compte ou de la campagne. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur et le paramètre par défaut au niveau de la campagne est hérité des paramètres du compte.

* *[!UICONTROL Standard]:* pour simplement rediriger l’utilisateur final vers l’URL spécifiée.

* *[!UICONTROL Token]:* pour rediriger l’utilisateur final vers l’URL et enregistrer également l’ID Search, Social et Commerce pour le clic (`ef_id`) en tant que paramètre de chaîne de requête, utilisé comme jeton. Choisissez cette option si vous souhaitez signaler des transactions hors ligne, que Search, Social et Commerce échangent des données avec Adobe Analytics ou que vous souhaitez suivre toutes les conversions qui se produisent dans les navigateurs [!DNL Apple Safari].

>[!NOTE]
>
>* Si vous passez de [!UICONTROL Standard] à [!UICONTROL Token], ou vice versa, vous devez régénérer les URL de tracking pour le compte.
>* Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.

**[!UICONTROL Auto Update]:** (lorsque le suivi Search, Social et Commerce est activé) Standardise vos URL de suivi à des fins de compatibilité entre les navigateurs et les serveurs. Search, Social et Commerce télécharge automatiquement les éléments suivants sur le réseau publicitaire lors de la synchronisation suivante : (a) paramètres de tracking Search, Social et Commerce pour les modèles de tracking et les mêmes paramètres ajoutés aux URL finales ou (b) nouvelles URL de destination incorporées avec le code de tracking Search, Social et Commerce. Pour les annonceurs et annonceuses disposant d’une intégration [Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) et d’une configuration d’AMO ID côté serveur (s_kwcid), le chargement inclut également les paramètres [AMO ID](/help/integrations/analytics/ids.md#amo-id) pour vos comptes [!DNL Google Ads] et [!DNL Microsoft Advertising]. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur. Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.

Les URL de tracking ne sont mises à jour quotidiennement que pour les entités désynchronisées (c’est-à-dire les nouvelles entités ajoutées et les entités existantes dont les propriétés ont été modifiées). Par conséquent, si vous modifiez ce paramètre de désactivé à activé pour un annonceur/compte/campagne existant, les URL de suivi ne sont pas mises à jour pour les entités existantes qui sont déjà synchronisées. Pour ajouter le tracking aux URL des entités existantes non synchronisées, contactez l’équipe de votre compte Adobe et demandez un processus de synchronisation manuel unique. Le processus de chargement automatique gérera les modifications futures.

**[!UICONTROL URL Encoding]:** (lorsque le suivi Search, Social et Commerce est activé ; comptes avec URL de destination uniquement) Encode l’URL de base dans la barre d’adresse du navigateur de l’utilisateur final (par exemple, `%3D` au lieu de `=`) :

**[!UICONTROL Tracking Level]:** (lorsque le suivi Search, Social et Commerce est activé ; disponible au niveau du compte et de la campagne ; non applicable aux réseaux publicitaires activés pour le suivi parallèle). Niveau auquel les clics et le chiffre d’affaires doivent être suivis en ajoutant une redirection (le cas échéant) et en ajoutant des paramètres aux URL pertinentes :

* *[!UICONTROL Keyword]:* pour suivre les données uniquement au niveau du mot-clé. Non disponible pour [!DNL Yandex].

* *[!UICONTROL Ad]:* pour effectuer le suivi des données uniquement au niveau de l’annonce publicitaire. Non disponible pour [!DNL Naver].

* *[!UICONTROL Keyword and Ad]:* pour effectuer le suivi des données au niveau des mots-clés et des annonces. Non disponible pour [!DNL Naver] et [!DNL Yandex].

**[!UICONTROL Landing Page Suffix]** (comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement ; facultatif) tous les paramètres à ajouter à la fin des URL finales pour effectuer le suivi des informations ; inclure tous les paramètres que votre entreprise doit effectuer le suivi.

Exemple : `param1=value1&param2=value2`

Les comptes qui utilisent le suivi des clics d’Adobe Advertising doivent inclure l’identifiant des clics du réseau publicitaire (`msclkid` par [!DNL Microsoft Advertising] ; `gclid` pour Google) dans le suffixe . Les comptes disposant d’une intégration Adobe Analytics doivent utiliser le paramètre AMO ID (en commençant par `s_kwcid`). Si le compte dispose d’une implémentation d’AMO ID côté serveur, le paramètre est ajouté automatiquement lorsqu’un utilisateur clique sur une publicité ; sinon, vous devez l’ajouter manuellement ici. Consultez les sections [Formats de suffixes requis pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et [Formats de suffixes requis pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Ce champ n&#39;est pas mis à jour par le paramètre de tracking [!UICONTROL Auto Update].
>* Les suffixes d’URL finaux aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent est nécessaire pour les composants de compte individuels. Pour configurer un suffixe au niveau du groupe publicitaire ou à un niveau inférieur, utilisez l’éditeur du réseau publicitaire.

**URL de suivi du compte** : (comptes [!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Yahoo! Japan Ads] uniquement ; facultatif) modèle de suivi par défaut pour le compte, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de la page de destination et incorpore également l’URL finale/de la page de destination dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

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

## onglet [!UICONTROL Setup Analytics]

**[!UICONTROL Adobe Analytics Report Suite]:** (annonceurs avec une [[!DNL Adobe Analytics for Advertising] intégration](/help/integrations/analytics/overview.md); facultatif) Une ou plusieurs suites de rapports Analytics auxquelles Search, Social et Commerce envoient les données qu’ils collectent du réseau publicitaire, y compris les classifications d’entité et les données de clic pour le compte. Cette fonctionnalité est disponible uniquement pour les réseaux publicitaires pris en charge.

Pour que les données apparaissent dans les suites de rapports, (a) la fonction d’identifiant AMO côté serveur doit être configurée pour le compte ou (b) le paramètre au niveau de l’annonceur sur « [!UICONTROL Enable Advertising reporting in Analytics] » doit être activé. En outre, le compte [!DNL Analytics] de l’annonceur doit être configuré pour recevoir des données de Search, Social et Commerce. Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À propos des comptes de réseau publicitaire](../ad-network-account-about.md)
>* [Gérer les comptes de centre commercial](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
>* [Mettre à jour le code de suivi s_kwcid pour un  [!DNL Google Ads] compte](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
