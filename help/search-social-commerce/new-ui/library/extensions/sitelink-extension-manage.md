---
title: Gestion des extensions de lien de site partagées
description: Découvrez comment créer, modifier et supprimer des extensions de lien de site partagées.
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%
---
# Gestion des extensions de lien de site partagées

Comptes *[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

Un lien de site est un lien de texte supplémentaire dans une liste d’annonces publicitaires. Utilisez des liens de site pour diriger les utilisateurs directement vers des pages spécifiques de votre site. Le réseau publicitaire détermine les liens de site à afficher en fonction de leur pertinence par rapport à la publicité.

Vous pouvez éventuellement inclure un texte descriptif pour chaque lien du site. Le réseau publicitaire peut également afficher une copie des publicités existantes dans le compte lorsqu’elle est très pertinente pour le lien du site. [!DNL Google Ads] peut afficher 2 à 6 liens de site dans une publicité pour ordinateur de bureau et jusqu’à quatre dans une publicité pour appareil mobile. [!DNL Microsoft Advertising] peut afficher deux, quatre ou six liens de site avec des descriptions ou 4 à 6 sans description.

Vous créez du texte et des paramètres de lien de site partagés au niveau du compte pour un [compte réseau publicitaire synchronisé](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Les liens de site dans la bibliothèque ne sont pas utilisés avec les annonces tant que vous ne les associez pas aux entités de compte.

## À propos des vues [!UICONTROL Sitelinks] et [!UICONTROL Associations] {#sitelink-view-about}

Dans **[!UICONTROL Library]>[!UICONTROL Extensions]**, l’onglet **[!UICONTROL Sitelinks]** répertorie les liens de site partagés au niveau du compte. L’onglet **[!UICONTROL Associations]** répertorie les associations entre les extensions et les entités de compte.

L’affichage de ces onglets nécessite l’autorisation [!UICONTROL View Extensions] . La création, la modification et la suppression de liens de site, ainsi que la création ou la suppression d’associations, nécessitent l’autorisation [!UICONTROL Edit Extensions].

Consultez l’aide du réseau publicitaire pour connaître le nombre maximal d’extensions par compte Google Ads [&#128279;](https://support.google.com/google-ads/answer/6372658) et par compte Microsoft Advertising [&#128279;](https://help.ads.microsoft.com/#apex/3/en/52001).

### Actions disponibles

* [Créer un lien de site partagé](#sitelink-create)

* [Modifier les paramètres du lien de site partagé](#sitelink-edit)

* [Supprimer les liens de site partagés](#sitelink-delete)

* [Associer des liens de site partagés à des comptes, des campagnes et des groupes publicitaires](ad-extension-association-manage.md#sitelink-associate)

* [Suppression des associations d’extensions](ad-extension-association-manage.md#association-delete)

* [Copier toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard)

## Créer un lien de site partagé {#sitelink-create}

1. Dans le menu principal, cliquez sur **[!UICONTROL Library]>[!UICONTROL Extensions]**, puis sur l&#39;onglet **[!UICONTROL Sitelinks]**.

1. Cliquez sur **[!UICONTROL Create Sitelink]**.

1. Dans **[!UICONTROL Basic Settings]**, sélectionnez le réseau publicitaire et le compte.

1. Saisissez les [paramètres de lien du site partagé](#shared-sitelink-settings).

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres. Pour modifier un paramètre, cliquez sur **[!UICONTROL Edit]** dans la section appropriée.

1. Cliquez sur **[!UICONTROL Create]**.

Après avoir créé le lien du site, [&#x200B; l’associer à un compte, une campagne ou un groupe publicitaire](ad-extension-association-manage.md#sitelink-associate).

## Modifier les paramètres du lien de site partagé {#sitelink-edit}

Vous pouvez modifier un lien de site partagé à la fois. Vous ne pouvez pas modifier sa date de début après l’avoir créée.

1. Dans le menu principal, cliquez sur **[!UICONTROL Library]>[!UICONTROL Extensions]**, puis sur l&#39;onglet **[!UICONTROL Sitelinks]**.

1. Cochez la case en regard d’un lien de site.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les [paramètres de lien du site partagé](#shared-sitelink-settings).

1. Cliquez sur **[!UICONTROL Review and Save]**, vérifiez les paramètres, puis cliquez sur **[!UICONTROL Update]**.

Vous pouvez également modifier le **[!UICONTROL Base URL]** ou le **[!UICONTROL Tracking Template]** d&#39;un lien du site directement dans le tableau de données en cliquant sur sa valeur.

## Supprimer les liens de site partagés {#sitelink-delete}

1. Dans le menu principal, cliquez sur **[!UICONTROL Library]>[!UICONTROL Extensions]**, puis sur l&#39;onglet **[!UICONTROL Sitelinks]**.

1. Cochez la case en regard de chaque lien de site partagé à supprimer.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

Pour supprimer une association sans supprimer le lien de site partagé de la bibliothèque, [supprimez l’association](ad-extension-association-manage.md#association-delete) à la place.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

## Paramètres de lien de site partagé {#shared-sitelink-settings}

Pour d’autres politiques et raisons de désapprobation du lien du site, consultez les [exigences du lien du site Google Ads](https://support.google.com/adspolicy/answer/1054210) et [exigences du lien du site Microsoft Advertising](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** texte à afficher pour le lien. Il peut contenir jusqu’à 25 caractères codés sur un octet ou 12 caractères codés sur deux octets. Le texte du lien doit être unique dans le compte ou la campagne.

>[!NOTE]
>
>([!DNL Google Ads]) Le texte existant de 35 caractères est affiché dans les publicités sur les ordinateurs de bureau et les tablettes, mais pas sur les appareils mobiles.

**[!UICONTROL Status]:** statut d’affichage du lien du site : **[!UICONTROL Active]** ou **[!UICONTROL Deleted]** pour les liens de site existants. Les nouveaux liens de site sont actifs par défaut.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** texte supplémentaire que le réseau publicitaire peut afficher sous le texte du lien. Pour inclure une description, saisissez les deux champs. Chacun peut inclure jusqu’à 35 caractères codés sur un octet ou 17 caractères codés sur deux octets.

**[!UICONTROL Start Date]:** (facultatif ; création uniquement) Première date à laquelle le lien du site peut être affiché. La valeur par défaut est la date actuelle. Pour spécifier une date ultérieure, saisissez-la au format MM/JJ/AAAA ou utilisez le sélecteur de date. La date de début est en lecture seule pour les liens de site existants.

**[!UICONTROL End Date]:** (facultatif) Dernière date à laquelle le lien du site peut être affiché. Par défaut, le lien du site peut être affiché indéfiniment. Pour spécifier une date de fin, saisissez-la au format MM/JJ/AAAA ou utilisez le sélecteur de date.

**[!UICONTROL Mobile Preference]:** (facultatif) Permet au réseau d’essayer d’afficher l’extension aux utilisateurs d’appareils mobiles plutôt qu’aux utilisateurs d’ordinateurs de bureau ou de tablettes. Par défaut, cette option n’est pas activée et l’extension peut apparaître sur n’importe quel type d’appareil. Le réseau ne garantit pas qu’il affichera l’extension sur le type d’appareil préféré.

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]:** (facultatif) L’URL de suivi, y compris les redirections de domaine hors atterrissage et les paramètres de suivi, avec l’URL de page de destination finale incorporée dans un paramètre. Par exemple, `https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`.

Dans cette vue, les valeurs saisies pour [!UICONTROL Base URL] et [!UICONTROL Tracking Template] doivent commencer par `http://` ou `https://` et ne peuvent pas contenir d’espaces.

* Lorsque les paramètres de la campagne incluent **[!UICONTROL EF Redirect]** et **[!UICONTROL Auto Upload]**, Search, Social et Commerce ajoute automatiquement un préfixe à son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour les paramètres qui intègrent l’URL finale, consultez la documentation d’[Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/56799) ou les paramètres « Modèle de suivi uniquement » de la documentation ValueTrack des [publicités Google](https://support.google.com/google-ads/answer/6305348).

* Vous pouvez inclure des paramètres d’URL et des paramètres personnalisés au niveau de la campagne, séparés par des esperluettes (`&`), ainsi que des redirections et un suivi tiers.

* Le modèle de suivi au niveau le plus granulaire remplace les modèles aux niveaux supérieurs.

>[!NOTE]
>
>* Pour les comptes avec des URL finales, l’URL de base peut contenir des redirections dans le domaine ou le sous-domaine de la page de destination, mais pas en dehors du domaine de la page de destination. Le réseau publicitaire extrait le domaine pour créer l’URL d’affichage.
>* ([!DNL Google Ads]) Chaque lien de site d’une campagne ou d’un groupe publicitaire doit avoir une page de destination unique avec environ 80 % de contenu unique. N’utilisez pas de liens vers plusieurs ancres sur la même page en tant que pages de destination de lien de site distinctes.
>* ([!DNL Google Ads]) La mise à jour d’un modèle de suivi au niveau du lien du site ou du mot-clé renvoie les publicités pertinentes pour révision. La mise à jour au niveau du compte, de la campagne ou du groupe publicitaire ne renvoie pas les publicités.
>* ([!DNL Microsoft Advertising]) Vous pouvez mettre à jour les modèles de suivi à n’importe quel niveau sans avoir à soumettre à nouveau des annonces pour approbation.
>* ([!DNL Google Ads]) Évitez les macros qui ne remplacent pas les clics provenant de sources permettant le suivi parallèle. Si des macros sont requises, votre équipe de compte Adobe travaille avec le service clientèle ou l’équipe d’implémentation pour les ajouter.

## Données de performances des liens de sites {#sitelink-performance}

Search, Social et Commerce mappent les clics sur une extension d’annonce et les conversions résultantes au mot-clé associé à l’annonce dans laquelle l’extension apparaît. Les données relatives au coût et aux clics au niveau de l’extension ne sont pas disponibles dans Search, Social et Commerce.

Dans l’[!UICONTROL Transaction Report], une valeur [!UICONTROL Link Type] de `sl:<Sitelink text>`, telle que `sl:See Current Offers`, identifie une transaction à partir d’un lien de site plutôt que l’annonce elle-même. Voir « [Rapport de transaction](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md) ».

Vous pouvez afficher le coût au niveau de l’extension et cliquer sur les données dans l’interface du réseau publicitaire.

>[!MORELIKETHIS]
>
>* [Gérer les extensions de légende partagées Google Ads](callout-extension-manage.md)
>* [Gérer les associations d’extensions publicitaires](ad-extension-association-manage.md)
