---
title: (Nouvelle interface utilisateur) Administration des utilisateurs
description: Découvrez comment gérer l’accès des utilisateurs et utilisatrices.
feature: Search Introduction
source-git-commit: c198b5ea2f8ef125b1a5d25616158d57950ce3b0
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Administration des utilisateurs pour Search, Social et Commerce

Certains utilisateurs peuvent gérer l’accès à la nouvelle interface utilisateur de Search, Social et Commerce à l’aide de [Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/using/admin-console.html), qui est l’emplacement central de la gestion de tous les droits Adobe et de la gestion des utilisateurs. Les utilisateurs sont classés en tant qu’utilisateurs finaux ou administrateurs. Si vous êtes administrateur, l’équipe chargée de votre compte Adobe vous avertira. Si vous êtes administrateur, reportez-vous aux sections suivantes pour identifier vos autorisations et workflows de gestion des utilisateurs.

## Types d’administrateurs

Admin Console propose plusieurs types d’administrateurs. Les types d’administrateurs et les autorisations suivants sont requis pour Search, Social et Commerce. Vous pouvez ajouter d’autres types si vous souhaitez déléguer des tâches de gestion des utilisateurs.

**Administrateur système :** superutilisateur qui gère tous les produits de l’organisation, y compris toutes les instances clientes de l’organisation. (Les instances client sont les mêmes que les comptes publicitaires hérités, avec une ou plusieurs instances par ID d’organisation). Un administrateur système peut effectuer toutes les tâches administratives dans Admin Console pour l’organisation et peut déléguer des fonctionnalités administratives à d’autres utilisateurs pour n’importe quel produit de l’organisation.

**Administrateur de produit :** gère l’accès à un produit [!DNL Adobe] spécifique (tel que Search, Social et Commerce) et les droits d’utilisation de ce produit. Les administrateurs de produit peuvent créer des profils de produit pour le produit, créer (mais pas supprimer) des utilisateurs et des groupes d’utilisateurs pour le produit, ajouter ou supprimer des utilisateurs et des groupes d’utilisateurs des profils de produit et ajouter ou supprimer d’autres administrateurs de produit du produit.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Profils de produit par défaut

Les profils de produit, qui sont similaires aux rôles, permettent aux utilisateurs d’accéder à des services spécifiques pour un produit spécifique.

La nouvelle interface utilisateur de Search, Social &amp; Commerce comporte les profils de produit par défaut suivants, qui fournissent différents sous-ensembles de fonctionnalités et de services. Vous ne pouvez pas modifier les autorisations de produit pour les profils de produit par défaut ni supprimer les profils de produit par défaut. Cependant, les administrateurs de produit, les administrateurs de profil de produit et les administrateurs système peuvent créer et gérer des profils de produit supplémentaires avec différents sous-ensembles d’autorisations disponibles, si nécessaire.

* **[!UICONTROL Basic Optimization]:** ce profil offre les fonctionnalités suivantes :

   * [!UICONTROL Objectives] : accès complet

   * [!UICONTROL Simulations] : accès complet

   * [!UICONTROL Portfolio Groups] : accès complet

   * [!UICONTROL Portfolios] : créer/modifier l’accès aux paramètres du portefeuille pour les [!UICONTROL Objectives] [!UICONTROL Campaigns], [!UICONTROL Management] et Dépenses ; accès en lecture seule aux paramètres restants du portefeuille.

   * [!UICONTROL Campaigns] : accès en lecture seule aux paramètres de la campagne (aucune fonctionnalité de création, de modification ou de suppression n&#39;est disponible) ; accès complet aux affectations de contraintes et de portfolio

   * [!UICONTROL Ad Groups] : accès en lecture seule aux paramètres du groupe publicitaire (aucune fonctionnalité de création, de modification ou de suppression n&#39;est disponible) ; accès complet aux affectations de contraintes et de portfolio

  Ce niveau d’accès est préférable pour les utilisateurs qui apprennent à utiliser Search, Social et Commerce.

* **[!UICONTROL Expert Optimization]:** ce profil offre les fonctionnalités suivantes :

   * [!UICONTROL Objectives] : accès complet

   * [!UICONTROL Simulations] : accès complet

   * [!UICONTROL Portfolio Groups] : accès complet

   * [!UICONTROL Portfolios] : accès complet

   * [!UICONTROL Campaigns] : accès en lecture seule à la liste des campagnes (aucune fonctionnalité de création, de modification ou de suppression de campagne n&#39;est encore disponible) ; accès complet aux affectations de contraintes et de portefeuilles

   * [!UICONTROL Ad Groups] : accès en lecture seule à la liste des groupes publicitaires (aucune fonctionnalité de création, de modification ou de suppression de campagne n’est encore disponible) ; accès complet aux affectations de contraintes et de portefeuilles

  Ce niveau d’accès est recommandé pour les utilisateurs experts de Search, Social et Commerce.

* **[!UICONTROL Read-Only]:** ce profil offre les fonctionnalités suivantes :

   * [!UICONTROL Objectives] : accès en lecture seule

   * [!UICONTROL Simulations] : accès en lecture seule

   * [!UICONTROL Portfolio Groups] : accès en lecture seule

   * [!UICONTROL Portfolios] : accès en lecture seule

   * [!UICONTROL Campaigns] : accès en lecture seule

   * [!UICONTROL Ad Groups] : accès en lecture seule

* **[!UICONTROL Admin]:** ce profil accorde un accès complet à toutes les fonctionnalités disponibles et permet aux utilisateurs de créer de nouvelles instances client (le même que les comptes publicitaires hérités, avec une ou plusieurs instances par ID d’organisation). N’attribuez ce droit à personne à moins d’avoir une justification commerciale adéquate.

## Tâches pour les administrateurs

### Connectez-vous à Adobe Admin Console et ouvrez-le sur Search, Social et Commerce.

>[!PREREQUISITES]
>
>Vous devez disposer d’un type d’accès administrateur à Search, Social et Commerce pour vous connecter à Admin Console.

1. Accédez à https://adminconsole.adobe.com/enterprise/.

1. (Si vous n’êtes pas connecté à Experience Cloud) Connectez-vous à Experience Cloud :

   1. Saisissez votre ID de [!DNL Adobe], puis cliquez sur **[!UICONTROL Continue]**.

   1. Sélectionnez **[!UICONTROL Personal Account] » ou &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Sélectionnez l’organisation Experience Cloud applicable.

      Admin Console s’ouvre sur l’onglet [!UICONTROL Overview] .

   1. Sous [!UICONTROL Product & services], cliquez sur « [!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name] ».

      La page produit s’ouvre sur l’onglet [!UICONTROL Product profiles] pour Search, Social et Commerce. Les onglets supplémentaires incluent [!UICONTROL Users] et [!UICONTROL Product Admins].

### Workflow pour les administrateurs système

Suivez ce workflow pour chaque instance cliente de Search, Social et Commerce.

1. [Connectez-vous à Adobe Admin Console et ouvrez-le sur Search, Social et Commerce](#open-admin-console).

1. (Facultatif) [Ajoutez un autre administrateur système](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) comme sauvegarde.

1. Déléguer la gestion des produits et des utilisateurs en [ajoutant des administrateurs de produit](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

### Workflow pour les administrateurs de produit

Suivez ce workflow pour chaque instance cliente de Search, Social et Commerce.

1. [Connectez-vous à Adobe Admin Console et ouvrez-le sur Search, Social et Commerce](#open-admin-console).

1. Au besoin, créez des utilisateurs finaux [individuellement](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) ou [en bloc](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. (Facultatif) Créez des [groupes d’utilisateurs](https://helpx.adobe.com/enterprise/using/user-groups.html) pour l’instance et affectez des utilisateurs à chaque groupe d’utilisateurs.

   Si l’instance compte de nombreux utilisateurs, créez des groupes d’utilisateurs afin de vous assurer que les utilisateurs se voient attribuer les profils adéquats en fonction de leur niveau d’expertise. (Voir Étape 4 pour l’affectation de groupes d’utilisateurs aux profils de produit.) Vous pouvez créer des groupes d’utilisateurs en fonction du secteur d’activité, des besoins en matière d’accès des utilisateurs, de la date d’embauche des utilisateurs ou d’autres critères.

   >[!IMPORTANT]
   >
   >Les noms des groupes d’utilisateurs doivent indiquer clairement les droits qui doivent être attribués à ces groupes. Par exemple, si vous souhaitez créer un groupe d’utilisateurs avec des droits en « Lecture seule », incluez « Read Only » dans le nom du groupe d’utilisateurs, tel que « Acme_Uk_ReadOnly » ou « Acme_ReadOnly ».

1. (Facultatif) [Créer des profils de produit personnalisés](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) avec des jeux d’autorisations définis.

   Les profils personnalisés s’ajoutent aux quatre profils de produit par défaut déjà disponibles.

   Chaque profil de produit d’une organisation doit avoir un nom unique. Si votre organisation utilise plusieurs instances Search, Social et Commerce (par exemple, Acme_US et Acme_JP), vous ne pouvez pas dupliquer un nom de profil de produit dans plusieurs instances. **Bonne pratique :** utilisez la convention de nommage `<Name>_<Instance>,` telle que « Simulations_Only_JP ».

   **Attention :** les autorisations de produit sont très granulaires. Soyez prudent lorsque vous configurez des profils de produit personnalisés ou vous pouvez omettre les fonctionnalités que vous souhaitez inclure.

1. [Affectez manuellement ou en bloc chaque utilisateur ou groupe d’utilisateurs au profil de produit approprié](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html)

## Guide complet d’administration des utilisateurs et des liens supplémentaires

* Pour plus d’informations sur l’administration des utilisateurs à l’aide de Adobe Admin Console, consultez le « Guide d’administration d’Adobe Enterprise et Teams [ », y compris la ](https://helpx.adobe.com/enterprise/admin-guide.html)présentation d’Admin Console[.](https://helpx.adobe.com/fr/enterprise/using/admin-console.html)

* Admin Console : [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
