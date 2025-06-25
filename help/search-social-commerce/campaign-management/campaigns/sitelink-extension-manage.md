---
title: Gestion des liens de site partagés
description: Découvrez comment créer et gérer des extensions de lien de site partagées.
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Gestion des liens de site partagés

*[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

Créez et gérez des liens de site partagés au niveau du compte pour tout compte [!DNL Google Ads] ou [!DNL Microsoft Advertising] synchronisé à partir de la bibliothèque [!UICONTROL Extensions] > [!UICONTROL Sitelinks] .

## Créer un lien de site partagé

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Saisissez les [paramètres de lien du site partagé](#shared-sitelink-settings).

1. Cliquez sur **[!UICONTROL Post]**.

Une fois que vous avez créé un lien de site, vous pouvez [l’affecter à un compte, une campagne ou un groupe publicitaire](sitelink-extension-associate.md).

## Modifier les paramètres du lien de site partagé

Vous pouvez modifier un lien de site partagé à la fois.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Cochez la case en regard du lien du site à modifier.

1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez les [paramètres de lien du site partagé](#shared-sitelink-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Supprimer les liens de site partagés

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Cochez la case en regard de chaque lien de site partagé à supprimer.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") et sélectionnez **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Paramètres de lien de site partagé {#shared-sitelink-settings}

Pour d’autres politiques et raisons de désapprobation du lien du site, consultez les exigences relatives à l’extension du lien du site [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) et [[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206).

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** texte à afficher pour le lien. Il peut contenir jusqu’à 25 caractères codés sur un octet ou 12 caractères codés sur deux octets. Le texte du lien doit être unique dans le compte ou la campagne.

>[!NOTE]
>
>([!DNL Google Ads]) Le texte existant de 35 caractères est affiché dans les publicités sur les ordinateurs de bureau et les tablettes, mais pas sur les appareils mobiles.

**[!UICONTROL Status]:** statut d&#39;affichage du lien du site : *[!UICONTROL Active]* ou *[!UICONTROL Deleted]* (liens du site existants uniquement). La valeur par défaut des nouveaux liens de site est *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2] :** texte supplémentaire que le moteur de recherche peut afficher sous le texte du lien. Pour inclure une description, saisissez des valeurs pour les deux champs de description. Chaque champ de description peut contenir jusqu’à 35 caractères codés sur un octet ou 17 caractères codés sur deux octets.

**[!UICONTROL Start Date]:** (campagnes avec liens de site hérités existants ou sans liens de site uniquement ; facultatif) Première date à laquelle le lien de site peut être affiché avec des annonces dans la campagne. La valeur par défaut pour les nouveaux liens de site est la date actuelle. Pour spécifier une date de début ultérieure, entrez une date au format MM/JJ/AAAA ou MM/JJ/AAAA, ou cliquez sur   et sélectionnez une date.

**[!UICONTROL End Date]:** (facultatif) Dernière date à laquelle le lien du site peut être affiché avec des annonces dans la campagne. Par défaut, le lien du site peut être affiché indéfiniment. Pour spécifier une date de fin, saisissez une date au format MM/JJ/AAAA ou MM/J/AAAA, ou cliquez sur   et sélectionnez une date.

**[!UICONTROL Mobile Preference]:** (facultatif) Permet au réseau d’essayer d’afficher l’extension d’annonce aux utilisateurs d’appareils mobiles plutôt qu’aux utilisateurs d’ordinateurs de bureau ou de tablettes. Par défaut, l’option n’est pas activée et l’extension d’annonce publicitaire apparaît sur n’importe quel type d’appareil.

>[!NOTE]
>
>Le réseau ne garantit pas qu’il affichera l’extension publicitaire sur le type d’appareil préféré.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** URL de la page de destination vers laquelle les utilisateurs du moteur de recherche sont dirigés lorsqu’ils cliquent sur votre annonce. Incluez tous les paramètres qui déterminent le contenu de la page. Si vous saisissez une valeur, elle remplace l’URL de base de la publicité.

Une fois l’enregistrement enregistré, l’URL de base inclut tous les paramètres d’ajout configurés pour la campagne ou le compte.

>[!NOTE]
>
>* (Comptes avec URL finales) L’URL de base peut contenir des redirections dans le domaine ou le sous-domaine de la page de destination, mais aucune redirection en dehors du domaine de la page de destination. Le réseau publicitaire extrait le domaine de cette URL et ajoute tous les chemins d’affichage facultatifs pour la publicité afin de créer l’URL d’affichage de la publicité.
>* ([!DNL Google Ads]) Chaque lien de site d’une campagne ou d’un groupe publicitaire doit avoir une page de destination unique, et le contenu de chaque page de destination de lien de site doit avoir environ 80 % de contenu unique. Par exemple, vous ne pouvez pas avoir de liens de site avec des liens vers plusieurs ancres dans la même page.
>* ([!DNL Google Ads]) Évitez d’utiliser des macros qui ne remplacent pas les clics provenant de sources permettant le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte Adobe doit collaborer avec le service clientèle ou l’équipe d’implémentation pour les ajouter.

**[!UICONTROL Tracking Template]:** (facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de la destination et incorpore également l’URL finale/de la page de destination dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

* Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « Chargement automatique », Search, Social et Commerce ajoute automatiquement un préfixe à son propre code de suivi des clics lorsque vous enregistrez l’enregistrement.

* Pour connaître les paramètres pris en charge afin d’incorporer l’URL finale, consultez les paramètres ([!DNL Microsoft Advertising] uniquement) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou ([!DNL Google Ads] uniquement) du « Modèle de tracking uniquement » dans la section sur les « Paramètres de [!DNL ValueTrack] disponibles » dans la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

* Vous pouvez éventuellement inclure des paramètres d’URL et tout paramètre personnalisé défini pour la campagne, séparés par des esperluettes (&amp;), tel que `{lpurl}?matchtype={matchtype}&device={device}`.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

>[!NOTE]
>
>* Lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres des mots-clés incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* ([!DNL Google Ads]) Si vous mettez à jour un modèle de suivi au niveau du lien du site ou du mot-clé, les publicités pertinentes sont soumises à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans envoyer à nouveau vos publicités pour approbation.
>* ([!DNL Microsoft Advertising]) Vous pouvez mettre à jour vos modèles de tracking à n’importe quel niveau sans avoir à soumettre à nouveau vos publicités pour approbation.
>* Par [!DNL Google Ads], évitez d’utiliser des macros qui ne remplacent pas les clics provenant de sources permettant le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte Adobe doit collaborer avec le service clientèle ou l’équipe d’implémentation pour les ajouter.

>[!MORELIKETHIS]
>
>* [À propos des extensions sitelink](sitelink-extension-about.md)
>* [Associer des liens de site partagés à des comptes, campagnes et groupes publicitaires](sitelink-extension-associate.md)
