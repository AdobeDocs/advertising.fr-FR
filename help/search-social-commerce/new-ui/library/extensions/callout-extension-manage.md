---
title: Gestion des extensions de légende partagées Google Ads
description: Découvrez comment créer, modifier et supprimer les extensions de légende partagée Google Ads.
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
source-wordcount: '685'
ht-degree: 0%
---
# Gestion des extensions de légende partagées [!DNL Google Ads]

Comptes *[!DNL Google Ads]uniquement*

Une extension de légende est du texte d’information sur un produit, un service ou une promotion que votre site offre, affiché avec une publicité textuelle. Le réseau publicitaire peut afficher 2 à 4 légendes avec une publicité.

Vous créez un texte de légende partagé et des paramètres au niveau du compte pour un [compte Google Ads synchronisé](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md). Les légendes de la bibliothèque ne sont pas utilisées avec les publicités tant que vous ne les associez pas à une campagne ou à un groupe publicitaire pris en charge sur le réseau de recherche.

Pour que vos publicités puissent s’afficher avec des légendes, attribuez au moins deux légendes par campagne ou groupe publicitaire. Les légendes au niveau du groupe publicitaire remplacent les légendes au niveau de la campagne.

## À propos des vues [!UICONTROL Callouts] et [!UICONTROL Associations] {#callout-view-about}

Dans **[!UICONTROL Library]>[!UICONTROL Extensions]**, l’onglet **[!UICONTROL Callouts]** répertorie les légendes partagées au niveau du compte. L’onglet **[!UICONTROL Associations]** répertorie les associations entre les extensions et les entités de compte.

L’affichage de ces onglets nécessite l’autorisation [!UICONTROL View Extensions] . La création, la modification et la suppression de légendes, ainsi que la création ou la suppression d&#39;associations, nécessitent l&#39;autorisation [!UICONTROL Edit Extensions].

Consultez la documentation de [Google Ads sur les limites de compte](https://support.google.com/google-ads/answer/6372658) pour connaître le nombre maximal d’extensions par compte.

### Actions disponibles

* [Créer une légende partagée](#callout-create)

* [Modifier les paramètres des légendes partagées](#callout-edit)

* [Supprimer les légendes partagées](#callout-delete)

* [Associer des légendes partagées à des campagnes et à des groupes publicitaires](ad-extension-association-manage.md#callout-associate)

* [Suppression des associations d’extensions](ad-extension-association-manage.md#association-delete)

* [Copier toutes les données des lignes sélectionnées dans le presse-papiers](#copy-to-clipboard)

## Créer une légende partagée {#callout-create}

1. Dans le menu principal, cliquez sur **[!UICONTROL Library]>[!UICONTROL Extensions]**, puis sur l&#39;onglet **[!UICONTROL Callouts]**.

1. Cliquez sur **[!UICONTROL Create Callout]**.

1. Dans **[!UICONTROL Basic Settings]**, sélectionnez [!DNL Google Ads] et le compte .

1. Saisissez les [paramètres de légende partagée](#shared-callout-settings).

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Vérifiez les paramètres. Pour modifier un paramètre, cliquez sur **[!UICONTROL Edit]** dans la section appropriée.

1. Cliquez sur **[!UICONTROL Create]**.

Après avoir créé la légende, [ l’associer à une campagne ou à un groupe publicitaire](ad-extension-association-manage.md#callout-associate).

## Modifier les paramètres des légendes partagées {#callout-edit}

Vous pouvez modifier une légende partagée à la fois. Vous ne pouvez pas modifier sa date de début après l’avoir créée.

1. Dans le menu principal, cliquez sur **[!UICONTROL Library]>[!UICONTROL Extensions]**, puis sur l&#39;onglet **[!UICONTROL Callouts]**.

1. Cochez la case en regard d’une légende.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les [paramètres des légendes partagées](#shared-callout-settings).

1. Cliquez sur **[!UICONTROL Review and Save]**, vérifiez les paramètres, puis cliquez sur **[!UICONTROL Update]**.

## Supprimer les légendes partagées {#callout-delete}

1. Dans le menu principal, cliquez sur **[!UICONTROL Library]>[!UICONTROL Extensions]**, puis sur l&#39;onglet **[!UICONTROL Callouts]**.

1. Cochez la case en regard de chaque légende partagée à supprimer.

   Pour plus d’informations sur la sélection de plusieurs lignes, voir « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

Pour supprimer une association sans supprimer la légende partagée de la bibliothèque, [supprimez l’association](ad-extension-association-manage.md#association-delete) à la place.

## Copier toutes les données des lignes sélectionnées dans le presse-papiers {#copy-to-clipboard}

Copiez les informations visibles dans les lignes sélectionnées, en fonction des filtres appliqués et des colonnes visibles dans la vue. Les informations sont enregistrées en tant que valeurs séparées par des tabulations (TSV).

1. Cochez la case en regard de chaque ligne dont vous souhaitez copier les données.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Copy]**.

## Paramètres des légendes partagées {#shared-callout-settings}

Pour d’autres politiques et raisons de désapprobation des légendes, consultez les [Exigences relatives aux légendes des publicités ](https://support.google.com/adspolicy/answer/1054212).

**[!UICONTROL Callout Text]:** Texte à afficher. Il peut contenir jusqu’à 25 caractères codés sur un octet ou 12 caractères codés sur deux octets. Il ne peut pas contenir de points d&#39;exclamation ou de ponctuation au début du texte.

**[!UICONTROL Start Date]:** (facultatif ; création uniquement) Première date à laquelle la légende peut être affichée. La valeur par défaut est la date actuelle. Pour spécifier une date ultérieure, saisissez-la au format MM/JJ/AAAA ou utilisez le sélecteur de date. La date de début est en lecture seule pour les légendes existantes.

**[!UICONTROL End Date]:** (facultatif) Dernière date à laquelle la légende peut être affichée. Par défaut, la légende peut être affichée indéfiniment. Pour spécifier une date de fin, saisissez-la au format MM/JJ/AAAA ou utilisez le sélecteur de date.

**[!UICONTROL Mobile Preference]:** (facultatif) [!DNL Google Ads] permet d’essayer d’afficher l’extension aux utilisateurs d’appareils mobiles plutôt qu’aux utilisateurs d’ordinateurs de bureau ou de tablettes. Sinon, l’extension peut apparaître sur n’importe quel type d’appareil. [!DNL Google Ads] ne garantit pas que l’extension s’affichera sur le type d’appareil préféré.

## Données de performances des légendes {#callout-performance}

Search, Social et Commerce mappent les clics sur une extension d’annonce et les conversions résultantes au mot-clé associé à l’annonce dans laquelle l’extension apparaît. Le coût au niveau de l’extension et les données de clic ne sont pas disponibles dans Search, Social et Commerce.

Vous pouvez afficher le coût au niveau de l’extension et cliquer sur les données dans l’interface [!DNL Google Ads].

>[!MORELIKETHIS]
>
>* [Gérer les extensions de lien de site partagées](sitelink-extension-manage.md)
>* [Gérer les associations d’extensions publicitaires](ad-extension-association-manage.md)
