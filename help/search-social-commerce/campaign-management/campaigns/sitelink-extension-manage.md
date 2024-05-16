---
title: Gestion des liens de site partagés
description: Découvrez comment créer et gérer des extensions de lien de site partagées.
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: c3b8e387cfc38d195e77761791e689fd094d8f39
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# Gestion des liens de site partagés

*[!DNL Google Ads]et [!DNL Microsoft Advertising] only*

Créer et gérer des liens de site partagés au niveau du compte pour toute synchronisation [!DNL Google Ads] ou [!DNL Microsoft Advertising] du compte [!UICONTROL Extensions] > [!UICONTROL Sitelinks] bibliothèque .

## Création d’un lien de site partagé

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Saisissez le [paramètres de lien de site partagé](#shared-sitelink-settings).

1. Cliquez sur **[!UICONTROL Post]**.

Une fois que vous avez créé un lien de site, vous pouvez [l’affecter à un compte, une campagne ou un groupe publicitaire ;](sitelink-extension-associate.md).

## Modification des paramètres de lien de site partagé

Vous pouvez modifier un lien de site partagé à la fois.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Cochez la case en regard du lien de site à modifier.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez la variable [paramètres de lien de site partagé](#shared-sitelink-settings).

1. Cliquez sur **[!UICONTROL Post]**.

## Suppression des liens de site partagés

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. Cochez la case en regard de chaque lien de site partagé que vous souhaitez supprimer.

   Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Dans la barre d’outils, cliquez sur ![Plus](/help/search-social-commerce/assets/more.png "Plus") et sélectionnez **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Paramètres des liens de site partagés {#shared-sitelink-settings}

Pour connaître d’autres politiques et raisons de désapprobation des liens de site, voir la section [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) et [[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206) exigences d’extension sitelink.

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** Texte à afficher pour le lien. Il peut contenir jusqu’à 25 caractères codés sur un octet ou 12 caractères codés sur deux octets. Le texte du lien doit être unique dans le compte ou la campagne.

>[!NOTE]
>
>([!DNL Google Ads]) Le texte existant de 35 caractères s’affiche dans les annonces sur les ordinateurs de bureau et les tablettes, mais pas sur les appareils mobiles.

**[!UICONTROL Status]:** État d’affichage du lien de site :  *[!UICONTROL Active]* ou *[!UICONTROL Deleted]* (liens de site existants uniquement). La valeur par défaut pour les nouveaux liens de site est *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** Texte supplémentaire qui peut s’afficher sous le texte du lien. Pour inclure une description, saisissez les valeurs des deux champs de description. Chaque champ de description peut contenir jusqu’à 35 caractères sur un ou 17 caractères sur deux octets.

**[!UICONTROL Start Date]:** (Campagnes avec des liens de site hérités existants ou pas de liens de site uniquement ; facultatif) Date à laquelle le lien de site peut être affiché pour les publicités dans la campagne. La valeur par défaut des nouveaux liens de site est le jour actuel. Pour spécifier une date de début future, saisissez une date au format MM/JJ/AAAA ou M/J/AAAA, ou cliquez et sélectionnez une date.

**[!UICONTROL End Date]:** (Facultatif) Dernière date à laquelle le lien de site peut être affiché avec les publicités dans la campagne. Par défaut, le lien de site peut s’afficher indéfiniment. Pour spécifier une date de fin, saisissez une date au format MM/JJ/AAAA ou M/J/AAAA, ou cliquez et sélectionnez une date.

**[!UICONTROL Mobile Preference]:** (Facultatif) Permet au réseau de tenter d’afficher l’extension d’annonce aux utilisateurs d’appareils mobiles plutôt qu’aux utilisateurs d’ordinateurs de bureau ou de tablettes. Par défaut, l’option n’est pas activée et l’extension de publicité s’affiche sur n’importe quel type d’appareil.

>[!NOTE]
>
>Le réseau ne garantit pas qu’il affichera l’extension publicitaire sur le type d’appareil préféré.

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** URL de la page d’entrée vers laquelle les utilisateurs du moteur de recherche sont redirigés lorsqu’ils cliquent sur votre publicité. Incluez les paramètres qui déterminent le contenu de la page. Si vous saisissez une valeur, elle remplace l’URL de base de la publicité.

Une fois l’enregistrement enregistré, l’URL de base inclut tous les paramètres d’ajout configurés pour la campagne ou le compte.

>[!NOTE]
>
>* (Comptes avec URL finales) L’URL de base peut contenir des redirections dans le domaine ou le sous-domaine de la page d’entrée, mais aucune redirection en dehors du domaine de la page d’entrée. Le réseau publicitaire extrait le domaine de cette URL et ajoute tous les chemins d’affichage facultatifs pour la publicité, afin de créer l’URL d’affichage de la publicité.
>* ([!DNL Google Ads]) Chaque lien de site d’une campagne ou d’un groupe publicitaire doit avoir une page d’entrée unique et le contenu de chaque page d’entrée de lien de site doit comporter environ 80 % de contenu unique. Par exemple, vous ne pouvez pas avoir de liens de site avec des liens vers plusieurs ancres dans la même page.
>* ([!DNL Google Ads]) Évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit travailler avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.

**[!UICONTROL Tracking Template]:** (Facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi, et incorpore également l’URL de page d’entrée/finale dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

* Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;Chargement automatique&quot;, Search, Social et Commerce préfixe automatiquement son propre code de suivi des clics lorsque vous enregistrez l’enregistrement.

* Pour les paramètres pris en charge pour incorporer l’URL finale, voir la section ([!DNL Microsoft Advertising] uniquement) [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799) ou ([!DNL Google Ads] uniquement) les paramètres &quot;Modèle de tracking uniquement&quot; dans la section &quot;Disponible&quot; [!DNL ValueTrack] Paramètres&quot; dans la variable [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348).

* Vous pouvez éventuellement inclure des paramètres d’URL et des paramètres personnalisés définis pour la campagne, séparés par des esperluettes (&amp;), tels que `{lpurl}?matchtype={matchtype}&device={device}`.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

>[!NOTE]
>
>* Lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres du mot-clé incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* ([!DNL Google Ads]) Si vous mettez à jour un modèle de suivi au niveau du lien de site ou du mot-clé, les publicités pertinentes sont soumises à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans soumettre à nouveau vos publicités pour approbation.
>* ([!DNL Microsoft Advertising]) Vous pouvez mettre à jour vos modèles de suivi à n’importe quel niveau sans soumettre à nouveau vos publicités pour approbation.
>* Pour [!DNL Google Ads], évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit collaborer avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.

>[!MORELIKETHIS]
>
>* [À propos des extensions sitelink](sitelink-extension-about.md)
>* [Association de liens de site partagés à des comptes, des campagnes et des groupes publicitaires](sitelink-extension-associate.md)
