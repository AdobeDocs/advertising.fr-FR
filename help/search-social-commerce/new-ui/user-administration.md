---
title: Administration des utilisateurs
description: Découvrez comment procéder .
feature: Search Introduction
source-git-commit: 5a4c608d8c8371c24cf220cc5eed9a39989dc850
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Administration des utilisateurs pour Search, Social et Commerce

Certains utilisateurs peuvent gérer l’accès à la nouvelle interface utilisateur de Search, Social et Commerce à l’aide de Adobe Admin Console, qui constitue l’emplacement central de la gestion de tous les droits Adobe et des utilisateurs. Les utilisateurs sont classés en tant qu’utilisateurs finaux ou administrateurs. Si vous êtes administrateur, l’équipe chargée de votre compte Adobe vous avertira. Si vous êtes administrateur, reportez-vous aux sections suivantes pour identifier vos autorisations et vos workflows de gestion des utilisateurs.<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## Types d’administrateurs concernés

Admin Console fournit plusieurs types d’administrateurs, mais seuls les types d’administrateurs et les autorisations suivants sont pertinents pour Search, Social et Commerce.

**Administrateur système :** super utilisateur pour l’organisation. Un administrateur système peut effectuer toutes les tâches administratives dans Admin Console pour l’organisation et peut déléguer des fonctionnalités administratives à d’autres utilisateurs (administrateurs de produit).&lt;!—, administrateurs de profils de produits et administrateurs de groupes d&#39;utilisateurs.  — Je pense que c&#39;est SEULEMENT DES ADMINISTRATEURS DE PRODUITS POUR NOUS ?  Vérifiez. —>

**Administrateur de produit :** gère l’accès à un produit [!DNL Adobe] spécifique (tel que Search, Social et Commerce) et les droits de leurs utilisateurs sur ce produit. Les administrateurs de produit peuvent créer des profils de produit pour le produit, créer (mais pas supprimer) des utilisateurs et des groupes d’utilisateurs, ajouter ou supprimer des utilisateurs et des groupes d’utilisateurs à partir des profils de produit, et ajouter ou supprimer d’autres administrateurs de produit du produit.

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## Profils de produit par défaut

Les profils de produit, qui sont similaires aux rôles, permettent aux utilisateurs d’accéder à des services spécifiques pour un produit spécifique.

La nouvelle interface utilisateur de Search, Social &amp; Commerce comporte les profils de produit par défaut suivants, qui fournissent différents sous-ensembles de fonctionnalités et de services. Vous ne pouvez pas modifier ni supprimer les profils de produit par défaut. Cependant, les administrateurs et administratrices système peuvent créer et gérer des profils de produit supplémentaires avec différents sous-ensembles d’autorisations, si nécessaire.

* **Optimisation de base :** ce profil fournit les fonctionnalités suivantes :

   * Objectifs : accès complet

   * Simulations : accès complet

   * Groupes Portfolio : accès complet

   * Portefeuilles : créez/modifiez l’accès aux paramètres du portefeuille pour la gestion des objectifs, des campagnes et des dépenses ; accès en lecture seule aux paramètres restants du portefeuille.

   * Campagnes : accès en lecture seule aux paramètres de la campagne (aucune fonctionnalité de création, de modification ou de suppression n’est disponible) ; accès complet aux affectations de contraintes et de portfolio<!-- Is that the correct wording? -->

   * Groupes publicitaires : accès en lecture seule aux paramètres des groupes publicitaires (aucune fonctionnalité de création, de modification ou de suppression n’est disponible) ; accès complet aux affectations de contraintes et de portefeuilles<!-- Is that the correct wording? -->

  Ce niveau d’accès est préférable pour les utilisateurs qui apprennent à utiliser Search, Social et Commerce.

* **Optimisation par des experts :** ce profil fournit les fonctionnalités suivantes :

   * Objectifs : accès complet

   * Simulations : accès complet

   * Groupes Portfolio : accès complet

   * Portefeuilles : accès complet

   * Campagnes : accès en lecture seule à la liste des campagnes (aucune fonctionnalité de création, de modification ou de suppression de campagne n’est encore disponible) ; accès complet aux affectations de contraintes et de portfolio<!-- Is that the correct wording? -->

   * Groupes publicitaires : accès en lecture seule à la liste des groupes publicitaires (aucune fonctionnalité de création, de modification ou de suppression de campagne n’est encore disponible) ; accès complet aux affectations de contraintes et de portfolio<!-- Is that the correct wording? -->

  Ce niveau d’accès est recommandé pour les utilisateurs experts de Search, Social et Commerce.

* **Lecture seule :** ce profil fournit les fonctionnalités suivantes :

   * Objectifs : accès en lecture seule

   * Simulations : accès en lecture seule

   * Groupes Portfolio : accès en lecture seule

   * Portfolios : accès en lecture seule

   * Campagnes : Accès en lecture seule

   * Groupes publicitaires : accès en lecture seule

* **Admin :** ce profil accorde un accès complet à toutes les fonctionnalités disponibles et permet aux utilisateurs de créer des instances clientes. N’attribuez ce droit à personne à moins d’avoir une justification commerciale adéquate.

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## Tâches pour les administrateurs

### Connectez-vous à Adobe Admin Console et ouvrez-le sur Search, Social et Commerce.

>[!PREREQUISITES]
>
>Vous devez disposer d&#39;un accès administrateur&lt;!— de quel genre ? Administrateur de produit, administrateur système, mais je suis sûr qu’il en va de même pour l’administrateur de profil de produit ou l’administrateur de groupe d’utilisateurs (il peut s’agir d’un groupe interne - cochez) -> pour Search, Social et Commerce.

1. Accédez à https://adminconsole.adobe.com/enterprise/.

1. (Si vous n’êtes pas connecté à Experience Cloud) Connectez-vous à Experience Cloud :

   1. Saisissez votre ID de [!DNL Adobe], puis cliquez sur **[!UICONTROL Continue]**.

   1. Sélectionnez **[!UICONTROL Personal Account] » ou **[!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. Sélectionnez l’organisation Experience Cloud applicable.

   1. Sous Produits et services, cliquez sur « [!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name] ».

   La page produit s’ouvre par défaut dans l’onglet [!UICONTROL Product profiles] pour Search, Social et Commerce. Les onglets supplémentaires incluent [!UICONTROL Users] et [!UICONTROL Product Admins].

### Workflow pour les administrateurs système

1. [Connectez-vous à Adobe Admin Console et ouvrez-le sur Search, Social et Commerce](#open-admin-console).

1. Déléguer la gestion des produits et des utilisateurs en [ajoutant des administrateurs de produit](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

<!-- what else? -->

### Workflow pour les administrateurs de produit

1. [Connectez-vous à Adobe Admin Console et ouvrez-le sur Search, Social et Commerce](#open-admin-console).

1. Au besoin, créez des utilisateurs finaux [individuellement](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) ou [en bloc](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html).

1. (Facultatif) Créez [groupes d’utilisateurs](https://helpx.adobe.com/enterprise/using/user-groups.html) pour chaque instance de produit et affectez des utilisateurs à chaque groupe d’utilisateurs.

   Si l’instance compte de nombreux utilisateurs, créez des groupes d’utilisateurs afin de vous assurer que les utilisateurs se voient attribuer les profils adéquats en fonction de leur niveau d’expertise. (Voir Étape 4 pour l’affectation de groupes d’utilisateurs aux profils de produit.) Vous pouvez créer des groupes d’utilisateurs en fonction du secteur d’activité, des besoins en matière d’accès des utilisateurs, de la date d’embauche des utilisateurs ou d’autres critères.

   >[!IMPORTANT]
   >
   >Les noms des groupes d’utilisateurs doivent indiquer clairement les droits qui doivent être attribués à ces groupes. Par exemple, si vous souhaitez créer un groupe d’utilisateurs avec des droits en « Lecture seule », incluez « Read Only » dans le nom du groupe d’utilisateurs, tel que « Acme_Uk_ReadOnly » ou « Acme_ReadOnly ».

1. (Facultatif) [Créer des profils de produit personnalisés](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) avec des jeux d’autorisations définis.

   Les profils personnalisés s’ajoutent aux quatre profils de produit par défaut déjà disponibles.

   Chaque profil de produit d’une organisation doit avoir un nom unique. Si votre organisation utilise plusieurs instances Search, Social et Commerce (par exemple, Acme_US et Acme_JP), vous ne pouvez pas dupliquer un nom de profil de produit dans plusieurs instances. **Bonne pratique :** utilisez la convention de nommage `<Name>_<Instance>,` telle que « Simulations_Only_JP ».

1. [Affectez manuellement ou en bloc chaque utilisateur ou groupe d’utilisateurs au profil de produit approprié](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html)

## Guide complet d’administration des utilisateurs et des liens supplémentaires

* Pour plus d’informations sur l’administration des utilisateurs à l’aide de Adobe Admin Console, consultez le « Guide d’administration d’Adobe Enterprise et Teams [ », y compris la ](https://helpx.adobe.com/enterprise/admin-guide.html)présentation d’Admin Console[.](https://helpx.adobe.com/fr/enterprise/using/admin-console.html)

* Admin Console : [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
