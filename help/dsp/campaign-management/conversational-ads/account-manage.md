---
title: Gestion des comptes publicitaires conversationnels [!DNL ChatGPT Ads]
description: Découvrez comment créer et gérer des comptes pour les annonces par carte de conversation [!DNL ChatGPT Ads], une fonctionnalité bêta qui place des annonces dans les conversations de l’assistant d’IA.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%
---
# Gestion des comptes publicitaires conversationnels [!DNL ChatGPT Ads]

*Fonction*

Grâce à l’intégration d’Adobe DSP à [!DNL OpenAI Ads], vous pouvez exécuter [!DNL ChatGPT Ads] publicités par carte de conversation qui apparaissent dans les conversations [!DNL ChatGPT]. Pour cette fonctionnalité, DSP crée un compte publicitaire conversationnel et achète des médias au nom de votre entreprise. Vous ne pourrez pas accéder au compte publicitaire à partir de ads.openai.com. Utilisez cette fonctionnalité pour tester les médias d’IA sans établir de relation directe avec [!DNL ChatGPT Ads].

Vous gérerez vos comptes publicitaires conversationnels [!DNL ChatGPT Ads] (y compris ses campagnes, groupes publicitaires et annonces) séparément de vos campagnes DSP standard, qui sont structurées différemment. Vous [affichez également les données de performances des campagnes [!DNL ChatGPT Ads]  des groupes publicitaires et des annonces](campaign-manage.md#campaign-views-about) séparément de vos campagnes DSP.

## Admissibilité

Les critères d’éligibilité pour cette fonctionnalité sont les suivants :

* **Clients [!DNL Search, Social, & Commerce] existants :** si votre annonceur utilise déjà [!DNL Search, Social, & Commerce], [ [!DNL ChatGPT Ads]  créez et gérez ses campagnes dans Search, Social et Commerce](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md) plutôt que dans DSP.

* **Secteurs restreints :** les annonceurs appartenant à des catégories restreintes (par exemple, finance ou santé) ne peuvent pas créer de comptes ou de campagnes publicitaires conversationnels.

Si l’annonceur sélectionné n’est pas éligible, les onglets [!UICONTROL Accounts] et [!UICONTROL Campaigns] en indiquent la raison. Vous pouvez toujours passer à un autre annonceur à l’aide du sélecteur d’annonceurs.

Pour utiliser la fonctionnalité, contactez l’équipe de votre compte Adobe pour commencer le processus d’intégration.

## Facturation

L’utilisation des [!DNL ChatGPT Ads] vous est facturée à la fin du mois avec vos autres factures, en utilisant la devise de facturation et le fuseau horaire de facturation de votre compte DSP (quelle que soit la [devise et le fuseau horaire utilisés pour le [!DNL ChatGPT Ads] compte](#account-settings)). Pour toute question sur la facturation, contactez l’équipe chargée de votre compte Adobe.

## La vue [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] {#accounts-view}

L’onglet [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] répertorie les comptes [!DNL OpenAI] pour l’annonceur sélectionné. Les informations de chaque compte incluent :

**[!UICONTROL Status]:** si le compte diffuse actuellement des publicités : *Actif* ou *En pause*. Vous ne pouvez pas modifier le statut d’un compte ; contactez l’équipe chargée de votre compte Adobe si vous souhaitez suspendre ou réactiver un compte.

**[!UICONTROL Review status]:** l’état de révision [!DNL OpenAI] : *En cours de révision*, *Approuvé* ou *Désapprouvé*. Placez le curseur sur le statut pour connaître la raison, le cas échéant.

**[!UICONTROL Active campaigns]:** nombre de campagnes actuellement actives dans le compte.

**[!UICONTROL Cost]:** Dépenses totales du compte.

### Actions disponibles

* [Afficher les limites de compte](#account-limits)

<!-- * [Refresh information about your accounts](#refresh) -- Add topic below. -->

* [Créer un compte](#account-create)

* [Modification d’un compte](#account-edit)

* [Actualiser la liste des comptes](#account-refresh)

* [Revenir au menu principal de DSP](#return-to-menu)

## Gestion des comptes

### Afficher les limites de compte {#account-limits}

Une limite de compte limite les dépenses totales d’un compte sur une période spécifique. Vous pouvez afficher les limites d’un compte, mais seule votre équipe de compte Adobe peut créer, modifier ou supprimer les limites.

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans la vue **[!UICONTROL Accounts]**, placez le curseur sur la ligne Compte et cliquez sur **[!UICONTROL ...]>[!UICONTROL View account limit]**.

La page [!UICONTROL Account limits] répertorie chaque limite du compte :

**[!UICONTROL Name]:** Nom de la limite.

**[!UICONTROL Amount]:** plafond de dépenses total pour la période limite.

**[!UICONTROL Period]:** période à laquelle la limite s’applique.

**[!UICONTROL Status]:** *Actif*, *À venir* ou *Terminé*.

**[!UICONTROL Spent]:** Montant dépensé jusqu’à présent dans la période limite.

>[!NOTE]
>
>Vous ne pouvez pas modifier ni supprimer les limites terminées, et les périodes de limite pour le même compte ne peuvent pas se chevaucher.

### Créer un compte publicitaire conversationnel [!DNL ChatGPT Ads] {#account-create}

Pour créer plus de deux comptes [!DNL ChatGPT Ads] pour un annonceur, contactez l’équipe chargée de votre compte Adobe.

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Effectuez l’une des opérations suivantes :

   * (Votre premier compte uniquement) Sur l’écran de bienvenue, cliquez sur **[!UICONTROL Create an Account]**.

   * Dans la vue **[!UICONTROL Accounts]**, sélectionnez un annonceur, puis cliquez sur **[!UICONTROL Create Account]**.

1. Spécifiez les [paramètres du compte](#account-settings).

1. Cochez la case **[!UICONTROL I agree to the Terms and Conditions]** .

1. Cliquez sur **[!UICONTROL Create account]**.

Les nouveaux comptes sont créés en pause pendant que [!DNL OpenAI] les révise. DSP active le compte une fois qu’il a été approuvé.

### Modification d’un compte publicitaire conversationnel [!DNL ChatGPT Ads] {#account-edit}

Vous pouvez modifier la raison sociale et le site web légaux d’un compte après l’avoir créé.

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans la vue **[!UICONTROL Accounts]**, placez le curseur sur la ligne Compte et cliquez sur **[!UICONTROL ...]>[!UICONTROL Edit account]**.

1. Modifiez les **[!UICONTROL Legal Business Name]** et/ou les **[!UICONTROL Advertiser Website]**. Pour plus d’informations sur les champs, voir « [Paramètres du compte](#account-settings) ».

1. Cliquez sur **[!UICONTROL Save changes]**.

>[!IMPORTANT]
>
>L’enregistrement des modifications redémarre la révision de [!DNL OpenAI] pour le compte. Le compte ne diffusera plus de publicités tant que le compte n’aura pas été réapprouvé.

### Actualiser la liste des comptes {#account-refresh}

Réafficher la liste des comptes lorsque d’autres utilisateurs ont pu apporter des modifications ou des ajouts.

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans la vue **[!UICONTROL Accounts]**, cliquez sur **[!UICONTROL Refresh]** au-dessus de la liste des comptes.

### Revenir au menu principal de DSP {#return-to-menu}

* Au-dessus du menu principal, cliquez sur **[!UICONTROL Back to DSP]**.

### [!DNL ChatGPT Ads] des paramètres du compte publicitaire conversationnel {#account-settings}

**[!UICONTROL Legal Business Name]:** Nom commercial enregistré de l’organisation.

**[!UICONTROL Advertiser Website]:** URL du site web de l’annonceur, commençant par `http://` ou `https://`.

**[!UICONTROL Country]:** le pays dans lequel l&#39;organisation est légalement enregistrée (et non le pays dans lequel vous allez publier des annonces). Il doit être identique au pays utilisé pour le contrat DSP de l’organisation. Vous ne pouvez pas modifier cette valeur après avoir enregistré le compte.

**[!UICONTROL Currency]:** (Lecture seule) Devise configurée par l’équipe de compte Adobe pour le compte [!DNL ChatGPT Ads]. Il peut s’agir d’une devise différente de celle de votre compte DSP, visible ailleurs dans DSP. **Remarque :** quelle que soit cette valeur, toutes les factures d’utilisation sont libellées dans la *devise de facturation* utilisée pour le compte DSP.

**[!UICONTROL Timezone]:** (Lecture seule) Fuseau horaire configuré par l’équipe de compte Adobe pour le compte [!DNL ChatGPT Ads]. Il peut s’agir d’un fuseau horaire différent de celui utilisé pour votre compte DSP, visible ailleurs dans DSP. **Remarque :** quelle que soit cette valeur, toutes les factures d’utilisation représentent le *fuseau horaire de facturation* utilisé pour le compte DSP.

**[!UICONTROL Favicon]:** fichier image à utiliser comme favicon du site web pour le compte.<!-- How is this used within this context? --> Le navigateur affiche la favicon à différents endroits, tels que la barre d’adresse, l’onglet ou les signets. Le fichier doit être au format JPG, PNG ou WEBP et faire au moins 256 x 256 pixels.

Pour charger une icône, cliquez sur **[!UICONTROL Upload favicon]**, puis recherchez et sélectionnez un fichier sur votre appareil ou réseau.

**[!UICONTROL I agree to the Terms and Conditions]:** case à cocher pour indiquer que vous acceptez tous les termes juridiques. Cochez la case pour créer un compte ou mettre à jour les paramètres du compte.

>[!MORELIKETHIS]
>
>* [Gérer des campagnes publicitaires conversationnelles](campaign-manage.md)
