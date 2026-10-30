---
title: Gérer [!DNL ChatGPT Ads] campagnes publicitaires conversationnelles
description: Découvrez comment créer et gérer des campagnes [!DNL ChatGPT Ads], des groupes publicitaires et des annonces de cartes de conversation, une fonctionnalité bêta qui place les annonces dans les conversations des assistants d’IA.
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
source-wordcount: '1188'
ht-degree: 0%
---
# Gérer [!DNL ChatGPT Ads] campagnes publicitaires conversationnelles, des groupes publicitaires et des annonces

*Fonction*

Gérez les campagnes [!DNL ChatGPT Ads], les groupes publicitaires et les annonces par carte de conversation au sein d’un [compte d’annonces conversationnelles](account-manage.md).

Vous êtes facturé pour l&#39;utilisation du [!DNL ChatGPT Ads] à la fin du mois avec vos autres factures. Pour toute question sur la facturation, contactez l’équipe chargée de votre compte Adobe.

## La vue [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] {#campaign-views-about}

La vue [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] comprend trois onglets : [!UICONTROL Campaigns], [!UICONTROL Ad Groups] et [!UICONTROL Ads]. Chaque onglet répertorie les campagnes, les groupes d’annonces ou les annonces du compte sélectionné, ainsi que les données de performances de la période sélectionnée. Les données de performances au niveau de la campagne, du groupe publicitaire et de l’annonce publicitaire incluent les [!UICONTROL Impressions], [!UICONTROL Clicks], [!UICONTROL Spend], [!UICONTROL CTR], [!UICONTROL Avg CPC] et [!UICONTROL Avg CPM].

>[!NOTE]
>
>* Les organisations configurées pour afficher les valeurs de taxe dans les vues de rapports ne les verront pas pour les [!DNL ChatGPT Ads]. Calculez vos valeurs fiscales manuellement.

### Actions disponibles

<!-- * [Refresh information about your campaigns](#refresh) -- Add topic below. -->

* [Créer](#campaign-create) ou [modifier](#campaign-edit) une campagne

* [Créer](#ad-group-create) ou [modifier](#ad-group-edit) un groupe publicitaire pour une campagne existante

* [Créer](#ad-create) ou [modifier](#ad-edit) une annonce pour un groupe d’annonces existant

* [Activer ou mettre en pause une campagne, un groupe publicitaire ou une publicité](#pause-activate)

* [Archiver une campagne, un groupe publicitaire ou une annonce publicitaire](#archive)

* [Accéder aux groupes et aux annonces publicitaires à partir des campagnes](#drill-down)

* [Actualiser la campagne, le groupe publicitaire ou la liste publicitaire](#refresh)

## Campagnes

### Création d’une campagne publicitaire conversationnelle [!DNL ChatGPT Ads] {#campaign-create}

Lorsque vous créez une campagne, vous pouvez éventuellement créer son premier groupe publicitaire et sa première publicité. Chaque étape crée cette entité dès que vous cliquez sur **[!UICONTROL Next]**, de sorte que vous ne pouvez pas revenir à une étape précédente ; si vous devez modifier quelque chose par la suite, modifiez-la une fois l’assistant fermé.

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans le sous-menu, cliquez sur l’onglet **[!UICONTROL Campaigns]** .

1. Dans le coin supérieur droit, sélectionnez un annonceur et un compte [!DNL ChatGPT Ads].

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]>[!UICONTROL Campaign]**.

1. Spécifiez les [paramètres de la campagne](#campaign-settings).

1. Cliquez sur **[!UICONTROL Next]** pour enregistrer les paramètres de la campagne.

1. Effectuez l’une des opérations suivantes :

   * Si vous ne souhaitez pas créer de groupe publicitaire pour la campagne, cliquez sur **[!UICONTROL Close]**.

     >[!TIP]
     >
     >Pour créer un groupe publicitaire ou une annonce publicitaire ultérieurement, reportez-vous à « [Créer un groupe publicitaire](#ad-group-create) » ou « [Créer une annonce publicitaire](#ad-create) ».

   * (Facultatif) Créez un groupe publicitaire :

     1. Spécifiez les paramètres [groupe publicitaire](#ad-group-settings).

     1. Cliquez sur **[!UICONTROL Next]** pour enregistrer les paramètres du groupe publicitaire.

     1. (Facultatif) Si vous ne souhaitez pas créer d’annonce pour la campagne, cliquez sur **[!UICONTROL Close]**.

   * (Facultatif après la création d’un groupe publicitaire) Créez une publicité :

     1. Spécifiez les paramètres [ad](#ad-settings).

     1. Cliquez sur **[!UICONTROL Create ad]**.

### Modifier [!DNL ChatGPT Ads] paramètres de la campagne publicitaire conversationnelle {#campaign-edit}

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans le sous-menu de gauche, cliquez sur **[!UICONTROL Campaigns]**.

1. Dans le coin supérieur droit, sélectionnez un annonceur et un compte [!DNL ChatGPT Ads].

1. (Si nécessaire) Au-dessus du tableau de données, cliquez sur l’onglet **[!UICONTROL Campaigns]** .

1. Placez le curseur sur la ligne et cliquez sur **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Modifiez l’un des [paramètres de campagne](#campaign-settings), [paramètres de groupe publicitaire](#ad-group-settings) et [paramètres de publicité](#ad-settings).

1. Cliquez sur **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] des paramètres de campagne publicitaire conversationnelle {#campaign-settings}

**[!UICONTROL Campaign name]:** Nom unique de la campagne. Le nom doit comporter au moins trois caractères.

**[!UICONTROL Campaign type]:** (Lecture seule) *Standard* est le seul type disponible.

**[!UICONTROL Objective]:** mesure sur laquelle cibler la campagne : *Atteindre* ou *Clics*. L’objectif détermine le type d’enchère pour les groupes publicitaires de la campagne.

**[!UICONTROL Locations]:** (facultatif) Emplacements spécifiques à cibler. Pour cibler tous les emplacements, laissez ce paramètre vide. Pour spécifier un emplacement spécifique, saisissez au moins deux lettres qui apparaissent n’importe où dans le nom, puis cliquez sur le nom dans les résultats de la recherche.

**[!UICONTROL Budget type]:** *Budget quotidien* ou *Budget de durée de vie*.

**[!UICONTROL Budget]:** budget pour le type de budget spécifié. La valeur doit être supérieure à zéro (0).

**[!UICONTROL Start date]:** date de début de la campagne, dans le fuseau horaire du compte.

**[!UICONTROL Set an end date]:** (facultatif) Permet de spécifier une date de fin pour la campagne. Lorsque vous sélectionnez cette option, spécifiez le **[!UICONTROL End date]** .

## Groupes publicitaires

### Créer un groupe publicitaire [!DNL ChatGPT Ads] pour une campagne existante {#ad-group-create}

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans le sous-menu, cliquez sur l’onglet **[!UICONTROL Campaigns]** .

1. Dans le coin supérieur droit, sélectionnez un annonceur et un compte [!DNL ChatGPT Ads].

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]>[!UICONTROL Ad Group]**.

1. Spécifiez les paramètres du [groupe publicitaire](#ad-group-settings), y compris la campagne parente.

1. Cliquez sur **[!UICONTROL Create ad group]**.

## Modification d’un groupe publicitaire [!DNL ChatGPT Ads] {#ad-group-edit}

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans le sous-menu de gauche, cliquez sur **[!UICONTROL Campaigns]**.

1. Dans le coin supérieur droit, sélectionnez un annonceur et un compte [!DNL ChatGPT Ads].

1. Au-dessus du tableau de données, cliquez sur l’onglet **[!UICONTROL Ad Groups]** .

1. Placez le curseur sur la ligne et cliquez sur **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Modifiez les paramètres [groupe publicitaire](#ad-group-settings).

1. Cliquez sur **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] paramètres de groupe publicitaire {#ad-group-settings}

**[!UICONTROL Parent campaign]:** (Groupes publicitaires pour les campagnes existantes uniquement) Campagne à laquelle le groupe publicitaire appartient.

**[!UICONTROL Ad group name]:** Nom unique du groupe publicitaire. Le nom doit comporter au moins trois caractères.

**[!UICONTROL Maximum CPC bid]** ou **[!UICONTROL Maximum CPM bid]:** montant maximal que vous paierez pour chaque clic ou pour 1 000 impressions. La valeur doit être supérieure à zéro (0). L’objectif de la campagne détermine le champ d’enchère : les campagnes *Clics* affichent **[!UICONTROL Maximum CPC bid]** et les campagnes *Atteindre* affichent **[!UICONTROL Maximum CPM bid]**.

>[!TIP]
>
>Des enchères plus élevées pourraient permettre de remporter plus d&#39;enchères.

**[!UICONTROL Context hints]:** (facultatif) Description des conversations, sujets ou mots-clés pour lesquels vos produits ou services sont pertinents. Ces indications guident la correspondance, mais ne sont pas des règles de ciblage de correspondance exacte.

## Publicités

### Créer une publicité de carte de conversation [!DNL ChatGPT Ads] pour un groupe publicitaire existant {#ad-create}

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans le sous-menu, cliquez sur l’onglet **[!UICONTROL Campaigns]** .

1. Dans le coin supérieur droit, sélectionnez un annonceur et un compte [!DNL ChatGPT Ads].

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create]>[!UICONTROL Ad]**.

1. Spécifiez les [paramètres de publicité](#ad-settings), y compris la campagne parente et le groupe publicitaire.

1. Cliquez sur **[!UICONTROL Create ad]**.

## Modification d’une publicité de carte de conversation [!DNL ChatGPT Ads] {#ad-edit}

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans le sous-menu de gauche, cliquez sur **[!UICONTROL Campaigns]**.

1. Dans le coin supérieur droit, sélectionnez un annonceur et un compte [!DNL ChatGPT Ads].

1. Au-dessus du tableau de données, cliquez sur l’onglet **[!UICONTROL Ads]** .

1. Placez le curseur sur la ligne et cliquez sur **[!UICONTROL ...]>[!UICONTROL Edit]**.

1. Modifiez les paramètres [ad](#ad-settings).

1. Cliquez sur **[!UICONTROL Save]**.

### [!DNL ChatGPT Ads] des paramètres publicitaires de la carte de conversation {#ad-settings}

**[!UICONTROL Parent campaign]** et **[!UICONTROL Parent ad group]:** (publicités dans les groupes publicitaires existants uniquement) Campagne et groupe publicitaire auxquels la publicité appartient.

**[!UICONTROL Ad name]:** Nom unique de l’annonce publicitaire. Le nom doit comporter au moins trois caractères.

**[!UICONTROL Ad URL (Link)]:** URL de la page de destination, commençant par `http://` ou `https://`.

**[!UICONTROL Title (headline)]:** Titre de la publicité. Le titre doit comporter entre 3 et 50 caractères. **Remarque :** le titre peut être tronqué dans certains types d’emplacement.

**[!UICONTROL Description]:** corps du texte de l’annonce publicitaire. La description doit comporter entre 3 et 100 caractères.

**[!UICONTROL Ad image]:** image JPG ou PNG à inclure dans la publicité. Pour charger une image, cliquez sur (nouvelles publicités) **[!UICONTROL Upload image (PNG/JPG)]** ou **[!UICONTROL Change image]**, puis recherchez et sélectionnez un fichier sur votre appareil ou réseau.

**[!UICONTROL Preview]:** aperçu de l’annonce publicitaire en fonction des paramètres de l’annonce publicitaire.

## Activer ou mettre en pause une campagne, un groupe publicitaire ou une annonce [!DNL ChatGPT Ads] {#pause-activate}

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans le sous-menu de gauche, cliquez sur **[!UICONTROL Campaigns]**.

1. Dans le coin supérieur droit, sélectionnez un annonceur et un compte [!DNL ChatGPT Ads].

1. Sur l’onglet **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** ou **[!UICONTROL Ads]**, recherchez la ligne .

1. Dans la colonne **[!UICONTROL Active]**, effectuez l’une des opérations suivantes :

   * Pour activer un élément en pause, activez le bouton (bascule) (à droite).

   * Pour suspendre un élément actif, désactivez le bouton (à gauche).

## Archivage d’une campagne, d’un groupe publicitaire ou d’une publicité [!DNL ChatGPT Ads] {#archive}

L’archivage supprime définitivement la campagne, le groupe publicitaire ou l’annonce publicitaire des vues [!UICONTROL Conversational Ads].

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans le sous-menu de gauche, cliquez sur **[!UICONTROL Campaigns]**.

1. Dans le coin supérieur droit, sélectionnez un annonceur et un compte [!DNL ChatGPT Ads].

1. Sur l’onglet **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** ou **[!UICONTROL Ads]**, placez le curseur sur la ligne et cliquez sur **[!UICONTROL ...]>[!UICONTROL Archive]**.

## Accéder aux groupes et aux annonces publicitaires à partir des campagnes [!DNL ChatGPT Ads] {#drill-down}

* Cliquez sur une ligne de campagne pour n’afficher que ses groupes publicitaires dans l’onglet **[!UICONTROL Ad Groups]** ou sur une ligne de groupe publicitaire pour n’afficher que ses annonces dans l’onglet **[!UICONTROL Ads]** .

Pour supprimer le filtre et afficher toutes les lignes de la vue, cliquez sur **X** dans le filtre au-dessus du tableau de données.

## Actualiser la campagne, le groupe publicitaire ou la liste publicitaire {#refresh}

Affichez à nouveau la liste des campagnes, des groupes d’annonces ou des annonces lorsque d’autres utilisateurs ou utilisatrices ont pu apporter des modifications ou des ajouts.

1. Dans le menu principal, cliquez sur **[!UICONTROL Conversational Ads Beta]**.

1. Dans la vue **[!UICONTROL Campaigns]**, **[!UICONTROL Ad Groups]** ou **[!UICONTROL Ads]**, cliquez sur **[!UICONTROL Refresh]** au-dessus du tableau de données.

>[!MORELIKETHIS]
>
>* [Gestion des comptes publicitaires conversationnels](account-manage.md)
