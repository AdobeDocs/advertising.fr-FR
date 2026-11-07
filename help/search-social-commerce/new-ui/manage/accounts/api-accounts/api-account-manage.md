---
title: (Nouvelle interface utilisateur) Gestion des comptes réseau et
description: Découvrez comment configurer et gérer les détails du compte dans la nouvelle interface utilisateur pour un réseau publicitaire synchronisé via l’API du réseau publicitaire.
feature: Search Campaign Management
exl-id: a50b2943-7568-401c-be5b-ff6f62629488
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: b568da9300e9adb8d189811c3c8b52516dfcef6f
workflow-type: tm+mt
source-wordcount: '3141'
ht-degree: 0%
---
# (Nouvelle interface utilisateur) Gérer les comptes réseau publicitaire via une connexion API

Ces instructions expliquent comment gérer les comptes de réseau publicitaire qui se synchronisent avec Search, Social et Commerce par le biais de l’API, y compris l’authentification, l’actualisation de la connexion et les vérifications de statut.

Pour créer, modifier ou réauthentifier des comptes, vous devez disposer des autorisations nécessaires pour modifier les comptes.

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [&#x200B; Inventaire pris en charge &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md).

## À propos de la vue [!UICONTROL Accounts] {#account-view-about}

La vue [!UICONTROL Manage] > [!UICONTROL Accounts] répertorie tous les comptes de réseau publicitaire dans la vue filtrée pour le compte publicitaire sélectionné. Cliquez sur le nom d’un compte pour ouvrir la vue [!UICONTROL Campaigns] filtrée pour ce compte.

### Authentification du compte et statut d’accès {#authentication-status}

Les informations d’authentification et d’accès varient selon le réseau publicitaire et les informations disponibles pour le compte. Un compte activé ou authentifié avec succès peut toujours avoir des autorisations manquantes.

Les colonnes suivantes affichent le statut du compte, l’authentification et les détails d’accès :

* **[!UICONTROL Status]:** le statut opérationnel du compte, qui est distinct de son authentification et de ses autorisations. Un compte activé peut synchroniser les données avec le réseau publicitaire et utiliser les fonctionnalités de gestion et d’optimisation de compte prises en charge. Un compte désactivé arrête l’activité dans Search, Social et Commerce. L’affichage du statut du compte utilise un indicateur vert pour **[!UICONTROL Enabled]**, un indicateur rouge pour **[!UICONTROL Disabled]** et un indicateur orange pour **[!UICONTROL Pending]**. Vous pouvez [activer ou désactiver des comptes](#enable-disable-account) à partir de la vue ou des paramètres du compte.

* **[!UICONTROL Authenticated]:** si le compte est authentifié :

  * **[!UICONTROL Yes]:** Le compte est authentifié.

  * **[!UICONTROL No]:** Le compte n&#39;est pas authentifié. Lorsqu’une erreur d’authentification est disponible, placez le curseur sur l’icône d’avertissement rouge pour afficher l’erreur.

  * L’authentification **[!UICONTROL Not Applicable]:** ne s’applique pas, car vous chargez des données pour le compte plutôt que de vous connecter via une API.

  * **[!UICONTROL Expiring in N days]**, **[!UICONTROL Expiring today]** ou **[!UICONTROL Expired]:** un avertissement d’expiration de jeton remplace **[!UICONTROL Yes]** lorsque des informations d’expiration sont disponibles et que le jeton expire dans 14 jours ou moins ou a déjà expiré. Cliquez sur l’icône d’avertissement pour afficher les détails d’accès du compte et [réauthentifier](#reauthenticate).

* **[!UICONTROL Manager Account for Cross-Account Conversions]:** (comptes [!DNL Google Ads] uniquement) ID du compte Manager associé utilisé pour les chargements de conversions entre comptes. Lorsqu’une erreur est disponible pour le compte du responsable, une icône d’avertissement s’affiche en regard de l’ID. Pour afficher l’erreur, placez le curseur sur l’icône. Les informations d’identification du compte du responsable sont distinctes de celles du compte réseau publicitaire. Pour ajouter ou actualiser les informations d’identification du compte du responsable, utilisez **[!UICONTROL Setup]** > **[!UICONTROL Manager Accounts]**. Voir « [Gérer les comptes du responsable](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md) ».

* **[!UICONTROL Access Level]:** niveau d’accès du compte signalé, tel que **[!UICONTROL Full]**, **[!UICONTROL Limited]** ou **[!UICONTROL None]**, ou **[!UICONTROL Not Applicable]** lorsqu’aucune valeur de niveau d’accès n’est disponible.

  Lorsque des autorisations sont manquantes, cliquez sur l’icône d’avertissement pour afficher les détails d’accès au compte. La section **[!UICONTROL Access]** répertorie les autorisations sous la forme **[!UICONTROL Granted]** ou **[!UICONTROL Missing]**. Lorsque les détails de l’impact sont disponibles, la section **[!UICONTROL Not working]** répertorie les fonctionnalités affectées. Pour [réauthentifier](#reauthenticate) et mettre à jour les autorisations, cliquez sur **[!UICONTROL Update Access]**.

### Actions disponibles

Les actions disponibles dépendent de vos autorisations et du type de compte.

* [Créer un compte réseau publicitaire](#create-account)

* [Modifier les détails du compte réseau publicitaire](#edit-account)

* [Réauthentifier un compte réseau publicitaire](#reauthenticate)

* [Activer ou désactiver les comptes réseau publicitaires](#enable-disable-account)

* [Synchroniser les données de compte avec le réseau publicitaire](sync-api-accounts.md)

* [Afficher un graphique des performances dans la vue [!UICONTROL Accounts]](#account-performance-graph)

* [Gérer les rapports de vue de données à partir de la vue [!UICONTROL Accounts]](#account-reports)

## Créer un compte réseau publicitaire {#create-account}

Pour activer la synchronisation d’un compte, vous devez créer un enregistrement de compte correspondant contenant les informations d’identification d’accès au compte et les options de suivi, ainsi que le statut *activé*.

>[!NOTE]
>
>Pour créer un compte sur le réseau publicitaire, accédez au site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Cliquez sur **[!UICONTROL Create Account]**.

1. Cliquez sur le nom du réseau publicitaire pour ouvrir la configuration du compte.

1. (Tous les réseaux publicitaires, à l’exception de [!DNL ChatGPT Ads] et [!DNL Yandex]) Dans l’onglet **[!UICONTROL Authenticate]**, connectez-vous dans la fenêtre contextuelle à l’aide des informations d’identification de l’annonceur et accordez l’accès au compte demandé.

   L’écran de configuration se met à jour automatiquement et s’affiche **[!UICONTROL Authentication Successful]** lorsque l’authentification réussit. Si vous devez rouvrir la fenêtre de connexion, cliquez sur **[!UICONTROL Open login again]**. Si votre navigateur bloque la fenêtre, modifiez ses paramètres pour autoriser des fenêtres contextuelles pour le site.

   Par [!DNL Meta Ads], un avertissement identifie les autorisations manquantes et leur impact. Une authentification réussie ne signifie pas nécessairement que toutes les autorisations demandées ont été accordées.

   Cliquez sur **[!UICONTROL Next]** pour continuer.

1. Spécifiez les [paramètres du compte](#account-settings-api) dans chaque onglet disponible. Pour les comptes authentifiés dans une fenêtre contextuelle, sélectionnez le compte à synchroniser à partir de **[!UICONTROL Linked Ad Accounts]** dans l’onglet **[!UICONTROL Select Accounts]** .

1. Cliquez sur **[!UICONTROL Save]**.

   Les données récentes de coût et de clic pour toutes les campagnes du compte sont mises à jour toutes les heures dans Search, Social et Commerce. Par défaut, les données sont disponibles pour les 5 à 10 derniers jours, selon le réseau publicitaire. Cependant, si nécessaire, l’équipe de lancement du projet peut récupérer les données des 60 derniers jours au maximum.

## Modifier les détails du compte réseau publicitaire {#edit-account}

Pour activer ou désactiver l’activité sur un compte, modifier les paramètres de suivi par défaut sur un compte ou modifier les suites de rapports [!DNL Analytics] à utiliser pour le suivi et les rapports, modifiez les détails du compte. Pour actualiser les autorisations de connexion ou de mise à jour, vous pouvez [réauthentifier le compte](#reauthenticate) à partir des paramètres du compte ou de la vue [!UICONTROL Accounts].

>[!NOTE]
>
>Pour modifier un compte réel sur le réseau publicitaire, accédez au site web du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Sélectionnez le compte de l’une des manières suivantes :

   * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

   * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

1. Modifiez les [paramètres du compte](#account-settings-api) dans les onglets disponibles.

1. Cliquez sur **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >Search, Social et Commerce doivent synchroniser les nouvelles données de compte avec celles du réseau publicitaire. Cela se produit automatiquement une fois par jour, ou plus souvent lorsque Search, Social et Commerce détecte des modifications sur le réseau publicitaire.

## Réauthentifier un compte réseau publicitaire {#reauthenticate}

*Pour les comptes qui utilisent l’authentification par fenêtre contextuelle ; non applicable aux comptes [!DNL ChatGPT Ads] ou [!DNL Yandex]*

Pour actualiser la connexion au réseau publicitaire ou mettre à jour les autorisations pour le compte, réauthentifiez le compte.

1. (Si vous êtes connecté à un autre compte pour le même réseau publicitaire dans la même application de navigateur) Déconnectez-vous de tout compte autre que celui de l’annonceur.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Ouvrez l’authentification de l’une des façons suivantes :

   * (Lorsque la valeur de **[!UICONTROL Authenticated]** du compte est **[!UICONTROL No]**) Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Re authenticate]**, le cas échéant.

   * (Lorsqu’un avertissement d’expiration de jeton s’affiche) Cliquez sur l’icône d’avertissement dans la colonne **[!UICONTROL Authenticated]**, puis sur **[!UICONTROL Reauthenticate]**.

   * (Lorsque des autorisations sont manquantes) Cliquez sur l’icône d’avertissement dans la colonne **[!UICONTROL Access Level]**, puis sur **[!UICONTROL Update Access]**.

   * (Dans les paramètres du compte) Cochez la case en regard du nom du compte et cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse, ou maintenez le curseur sur le nom du compte, cliquez sur **...**, puis cliquez sur **[!UICONTROL Edit]**. Dans l’onglet **[!UICONTROL Account Details]**, dans **[!UICONTROL Account Authentication]**, cliquez sur **[!UICONTROL Re authenticate]**.

1. Ouvrez une session dans la fenêtre contextuelle à l’aide des informations d’identification de l’annonceur et accordez l’accès au compte demandé.

   Le nouveau jeton d’accès est enregistré automatiquement lorsque la réauthentification réussit. Si vous modifiez également d’autres paramètres du compte, cliquez sur **[!UICONTROL Save]** pour enregistrer ces modifications.

   Par [!DNL Meta Ads], un message d’information identifie les autorisations qui font toujours défaut après une réauthentification réussie. Pour identifier la fonctionnalité affectée, passez en revue les [détails d’accès](#authentication-status).

## Activer ou désactiver les comptes réseau publicitaires {#enable-disable-account}

Lorsque vous activez un compte de réseau publicitaire, Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’il est pris en charge) et diffuse des enchères automatisées et/ou des budgets de campagne pour les campagnes des portfolios. Lorsque vous désactivez un compte de réseau publicitaire, Search, Social et Commerce arrête toute activité sur le compte. Les données collectées alors que le compte était actif sont toujours stockées, mais les vues et rapports de gestion de campagne n’incluent pas les données de la période au cours de laquelle le compte est désactivé. Vous pourrez par la suite réactiver le compte pour reprendre l’activité avec le compte.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Effectuez l’une des opérations suivantes :

   * (Vue [!UICONTROL Accounts]) :

     * (Pour activer le compte) Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Enable]** dans la barre d’outils des actions en bloc.

     * (Pour désactiver le compte) Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Disable]** dans la barre d’outils des actions en bloc.

   * (Dans les paramètres du compte) :

     1. Sélectionnez le compte de l’une des manières suivantes :

        * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

        * Cochez la case en regard du nom du compte, puis cliquez sur **[!UICONTROL Edit]** dans la barre d’outils des actions en masse.

     1. Dans l’onglet **[!UICONTROL Account Details]** , activez **[!UICONTROL Account Enabled]** pour activer le compte ou désactivez-le pour désactiver le compte.

     1. Cliquez sur **[!UICONTROL Save]**.

## Afficher un graphique des performances dans la vue [!UICONTROL Accounts] {#account-performance-graph}

Ouvrez et configurez un graphique de performances avec jusqu’à trois mesures totalisées sur les comptes dans la vue filtrée pour la période et la devise spécifiées.

### Affichage d’un graphique de performances

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Spécifiez la période et appliquez des filtres pour les comptes dont vous souhaitez afficher les performances.

1. Au-dessus du tableau de données, cliquez sur ![Graphiques](/help/search-social-commerce/assets/charts.png "Graphiques").

1. (Facultatif) Utilisez **[!UICONTROL Currency]** et **[!UICONTROL Metrics]** pour spécifier la devise et jusqu’à trois mesures à inclure dans le graphique.

### Masquage d’un graphique de performances visible

* Au-dessus du tableau de données, cliquez sur ![Graphiques](/help/search-social-commerce/assets/charts.png "Graphiques").

## Gérer les rapports de vue de données à partir de la vue [!UICONTROL Accounts] {#account-reports}

Générez un rapport qui inclut les lignes de données d’un ou de plusieurs comptes dans la vue [!UICONTROL Accounts], puis téléchargez le rapport sous la forme d’un fichier de feuille de calcul Excel Microsoft (format XLSX). Le rapport inclut les colonnes visibles dans l’affichage pour la période spécifiée.

Vous pouvez supprimer les rapports terminés et ceux dont la génération a échoué.

### Générer un rapport avec les lignes de données filtrées

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Spécifiez la période et appliquez des filtres pour les données que vous souhaitez télécharger.

1. Indiquez les comptes dont vous souhaitez télécharger les données :

   * Pour télécharger des données pour des comptes spécifiques, cochez les cases en regard des comptes.

   * Pour télécharger des données pour tous les comptes dans la vue filtrée, laissez toutes les cases à cocher désactivées.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![&#x200B; Télécharger le rapport &#x200B;](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la boîte de dialogue [!UICONTROL Grid Reports], conservez le **[!UICONTROL Report Name]** par défaut ou saisissez un autre nom, puis cliquez sur **[!UICONTROL Generate]**.

   Le rapport est ajouté à la liste **[!UICONTROL Recently Generated]**.

1. (Facultatif) Pour télécharger le fichier une fois l’opération terminée, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Télécharger un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![&#x200B; Télécharger le rapport &#x200B;](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste **[!UICONTROL Recently Generated]** de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Suppression d’un rapport

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![&#x200B; Télécharger le rapport &#x200B;](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste **[!UICONTROL Recently Generated]** de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") en regard du nom d’un rapport terminé ou d’un rapport dont la génération a échoué.

1. Confirmez la suppression.

## Paramètres du compte réseau publicitaire {#account-settings-api}

Les paramètres du compte varient selon le réseau publicitaire. Il se peut que vous ne voyiez pas tous les paramètres ci-dessous.

### onglet [!UICONTROL Authenticate]

(Visible lorsque vous créez un compte qui utilise l’authentification par fenêtre contextuelle) Connectez-vous au réseau publicitaire à l’aide des informations d’identification de l’annonceur. L’onglet affiche le statut de la connexion et comprend des **[!UICONTROL Open login again]** pour rouvrir la fenêtre contextuelle de connexion.

### Onglet [!UICONTROL Select Accounts]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** nom à afficher pour le compte dans Search, Social et Commerce.

>[!NOTE]
>
>Si vous disposez d’une intégration Search, Social et Commerce-Adobe Analytics et que vous modifiez le nom du compte de recherche, demandez à l’équipe chargée de votre compte Adobe de mettre à jour le mappage.

**[!UICONTROL Linked Ad Accounts]:** (visible lorsque vous créez un compte qui utilise l’authentification par fenêtre contextuelle) Compte réseau publicitaire à synchroniser. Faites votre choix parmi les comptes publicitaires liés à votre connexion réseau.

**[Détails de connexion]:** (comptes [!DNL Yandex] uniquement) Informations d’identification du compte à utiliser :

* **[!UICONTROL Login]:** nom ou ID de connexion permettant d’activer l’accès API au compte.

* **[!UICONTROL Password]:** mot de passe du compte.

* **[!UICONTROL Access Key]:** clé d’accès du compte de développeur à utiliser.

* **[!UICONTROL Application ID]:** jeton de développement à utiliser pour le compte. Le même jeton est utilisé pour tous les comptes [!DNL Yandex].

* **[!UICONTROL Purse Campaign ID]:** (comptes [!DNL Yandex] dont le paramètre Compte partagé est désactivé uniquement ; facultatif) Identifiant numérique de la campagne utilisé pour payer toutes les campagnes publicitaires du compte.

* **[!UICONTROL Finance Token]:** (comptes [!DNL Yandex] avec le paramètre Compte partagé désactivé uniquement ; facultatif) Jeton de développement pour les appels API liés à la finance, tels que la réaffectation d’argent entre les campagnes de l’annonceur pour l’optimisation du portfolio.

**[!UICONTROL Currency]:** (Lecture seule) Abréviation de la devise utilisée pour le compte. Cette valeur est automatiquement renseignée avec la devise configurée pour le compte sur le réseau publicitaire une fois l’enregistrement enregistré.

**[!UICONTROL Time Zone]:** Fuseau horaire de l’annonceur. Cette valeur est automatiquement renseignée avec le fuseau horaire configuré pour le compte Search, Social et Commerce de l’annonceur une fois l’enregistrement enregistré.

**[!UICONTROL Login]:** (Lecture seule) Compte utilisateur utilisé pour se connecter au compte.

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled] :** Search, Social et Commerce synchronise les données de campagne avec le compte (lorsqu’il est pris en charge) et diffuse des enchères automatisées et/ou des budgets de campagne pour les campagnes des portfolios.

**[!UICONTROL Account Authentication]> [!UICONTROL Re authenticate]:** (visible lorsque vous modifiez un compte qui utilise l’authentification d’une fenêtre contextuelle) Actualise la connexion ou met à jour les autorisations du compte. Le nouveau jeton d’accès est enregistré automatiquement lorsque la réauthentification réussit.

## onglet [!UICONTROL Setup Tracking]

<!-- This should be the name of the whole left side of options -- they're all enabled/disabled depending on whether you enable our tracking -->

**[!UICONTROL Search, Social, & Commerce Tracking]:** permet d’activer ou non le suivi à l’aide du service de suivi des conversions d’Adobe Advertising. Cette méthode génère des identifiants de suivi des clics uniques et redirige les utilisateurs vers le serveur Adobe Advertising à des fins de suivi avant de les envoyer à la page de destination du client. Cette méthode comporte des options de tracking par défaut que vous pouvez éventuellement personnaliser. Vous pouvez également spécifier des paramètres à ajouter à chaque URL.

Pour activer cette fonctionnalité, activez **[Activer le suivi]**.

>[!NOTE]
>
>* Si vous modifiez ce paramètre, vous devez régénérer les URL de tracking pour le compte.
>* Les options de tracking au niveau de la campagne remplacent les paramètres au niveau du compte.

**[!UICONTROL Tracking Type]:** (lorsque le suivi Search, Social et Commerce est activé) Méthode de redirection des utilisateurs finaux vers l’URL finale ou l’URL de destination. L’option sélectionnée s’applique à toutes les unités d’enchères du compte ou de la campagne. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur et le paramètre par défaut au niveau de la campagne est hérité des paramètres du compte.

* *[!UICONTROL Standard]:* pour rediriger l’utilisateur final vers l’URL spécifiée.

* *[!UICONTROL Token]:* pour rediriger l’utilisateur final vers l’URL et enregistrer également l’ID Search, Social et Commerce pour le clic (`ef_id`) en tant que paramètre de chaîne de requête, utilisé comme jeton. Choisissez cette option si vous souhaitez signaler des transactions hors ligne, que Search, Social et Commerce échangent des données avec Adobe Analytics ou que vous souhaitez suivre toutes les conversions qui se produisent dans les navigateurs [!DNL Apple Safari].

>[!NOTE]
>
>* Si vous passez de [!UICONTROL Standard] à [!UICONTROL Token], ou vice versa, vous devez régénérer les URL de tracking pour le compte.
>* Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.

**[!UICONTROL Auto Update]:** (lorsque le suivi Search, Social et Commerce est activé) Standardise vos URL de suivi à des fins de compatibilité entre les navigateurs et les serveurs. Search, Social et Commerce télécharge automatiquement les éléments suivants sur le réseau publicitaire lors de la synchronisation suivante : (a) paramètres de tracking Search, Social et Commerce pour les modèles de tracking et les mêmes paramètres ajoutés aux URL finales ou (b) nouvelles URL de destination incorporées avec le code de tracking Search, Social et Commerce. Pour les annonceurs et annonceuses disposant d’une intégration [Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) et d’une configuration d’AMO ID côté serveur (s_kwcid), le chargement inclut également les paramètres [AMO ID](/help/integrations/analytics/ids.md#amo-id) pour vos comptes [!DNL Google Ads] et [!DNL Microsoft Advertising]. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur. Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.

Les URL de tracking ne sont mises à jour quotidiennement que pour les entités désynchronisées (c’est-à-dire les nouvelles entités ajoutées et les entités existantes dont les propriétés ont été modifiées). Par conséquent, si vous modifiez ce paramètre de désactivé à activé pour un annonceur/compte/campagne existant, les URL de suivi ne sont pas mises à jour pour les entités existantes qui sont déjà synchronisées. Pour ajouter le tracking aux URL des entités existantes non synchronisées, contactez l’équipe de votre compte Adobe et demandez un processus de synchronisation manuel unique. Le processus de chargement automatique gère les modifications futures.

**[!UICONTROL URL Encoding]:** (lorsque le suivi Search, Social et Commerce est activé ; comptes avec URL de destination uniquement) Encode l’URL de base dans la barre d’adresse du navigateur de l’utilisateur final (par exemple, `%3D` au lieu de `=`) :

**[!UICONTROL Tracking Level]:** (lorsque le suivi Search, Social et Commerce est activé ; disponible au niveau du compte et de la campagne ; non applicable aux réseaux publicitaires activés pour le suivi parallèle) Niveau auquel effectuer le suivi des clics et des recettes en ajoutant une redirection et des paramètres d’ajout aux URL appropriées :

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

**URL de suivi du compte** : (comptes [!DNL Google Ads], [!DNL LY Ads] et [!DNL Microsoft Advertising] uniquement ; facultatif) modèle de suivi par défaut pour le compte, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de la page de destination et incorpore également l’URL finale/de la page de destination dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

* Pour incorporer l’URL finale :

  * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) Pour obtenir une liste de paramètres indiquant les URL finales dans les modèles de tracking, reportez-vous à la [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ([!DNL Microsoft Advertising] uniquement) ou ([!DNL Google Ads] uniquement) aux paramètres « Modèle de tracking uniquement » dans la section Paramètres de [!DNL ValueTrack] disponibles dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

  * ([!DNL LY Ads] uniquement) Utilisez le `!{lpurl}` de paramètre pour indiquer l’URL de la page de destination.

* Vous pouvez éventuellement inclure des paramètres d’URL et tout paramètre personnalisé défini pour la campagne, séparés par des esperluettes (&amp;), tel que `{lpurl}?matchtype={matchtype}&device={device}`.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

* Lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

>[!NOTE]
>
>* Par [!DNL Google Ads], évitez d’utiliser des macros qui ne remplacent pas les clics provenant de sources permettant le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte Adobe travaille avec le service clientèle ou l’équipe d’implémentation pour les ajouter.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres des mots-clés incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Si vous mettez à jour un modèle de suivi au niveau de l’annonce, du lien du site ou du mot-clé, les annonces pertinentes sont envoyées à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans envoyer à nouveau vos publicités pour approbation.

## onglet [!UICONTROL Set up Adobe Analytics]

Ces paramètres sont disponibles pour les annonceurs qui disposent d’une [[!DNL Adobe Analytics for Advertising]  intégration &#x200B;](/help/integrations/analytics/overview.md).

**[!UICONTROL Adobe Analytics Report Suite]:** (facultatif) Une ou plusieurs suites de rapports Analytics auxquelles Search, Social et Commerce envoient les données qu’ils collectent sur le réseau publicitaire, y compris les classifications d’entités et les données de clics pour le compte. Cette fonctionnalité est disponible uniquement pour les réseaux publicitaires pris en charge.<!-- What are the repercussions of changing the suites? Timing of updated data? -->

Pour que les données apparaissent dans les suites de rapports, (a) la fonction d’identifiant AMO côté serveur doit être configurée pour le compte ou (b) le paramètre au niveau de l’annonceur sur « [!UICONTROL Enable Advertising reporting in Analytics] » doit être activé. En outre, le compte [!DNL Analytics] de l’annonceur doit être configuré pour recevoir des données de Search, Social et Commerce. Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

**[!UICONTROL Adobe Analytics Conversion Reporting]: [!UICONTROL Enable conversion reporting in Adobe Analytics]:** (comptes [!DNL Meta Ads] ; facultatif) Ajoute le paramètre de tracking [AMO ID (s_kwcid)](/help/search-social-commerce/tracking/amo-id-tracking-parameter.md) à toutes les publicités de la campagne. Le paramètre permet à Adobe Analytics d’associer des conversions à des campagnes Meta Ads dans la suite de rapports spécifiée, ainsi qu’aux classifications d’entités et aux données de clics.

>[!MORELIKETHIS]
>
>* [À propos des comptes de réseau publicitaire](../ad-network-account-about.md)
>* [Gérer les comptes de centre commercial](/help/search-social-commerce/new-ui/set-up/manager-account-manage.md)
>* [Mettre à jour le code de suivi s_kwcid pour un  [!DNL Google Ads] compte](/help/search-social-commerce/campaign-management/accounts/update-amo-id-google.md)
