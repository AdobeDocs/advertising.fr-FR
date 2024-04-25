---
title: Génération d’une URL de suivi des clics
description: Découvrez comment générer manuellement une URL de suivi des clics Search, Social et Commerce.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: 0da23a2756fc7ed4d2ef8fb739d94a91ac6400ba
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Générez une URL de suivi des clics Search, Social et Commerce à l’aide de l’outil de suivi des URL.

*Publicitaires avec suivi de conversion des Adobes Advertising uniquement*

Pour plus d’informations sur le moment où vous devez générer et implémenter manuellement une URL de suivi des clics, voir &quot;[Quand et comment générer des URL de suivi des clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

>[!NOTE]
>
>Cette fonctionnalité ne met pas en oeuvre le modèle de suivi ou l’URL de destination dans le compte publicitaire approprié.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Sélectionnez le compte réseau publicitaire dans la liste.

   ([!DNL Google Ads] mots-clés ; texte, installation d’applications mobiles et annonces de recherche dynamique ; emplacements ; liens de site ; et groupes de produits) Les balises de suivi pour le champ de modèle de suivi s’affichent. Ils n’incluent aucun paramètre d’ajout au niveau du compte. Passez à l’étape 4.

   Pour tous les autres types de balises, saisissez les informations permettant de générer une balise.

1. (Si nécessaire) Générez une balise :

   1. Spécifiez les pages d’entrée, avec des liens de site ou des noms de produit, si nécessaire, de l’une des manières suivantes :

      * Spécifiez un fichier contenant les informations en saisissant le chemin d’accès complet et le nom de fichier ou en cliquant sur **[!UICONTROL Browse]** pour localiser le fichier sur votre périphérique ou réseau. Le fichier doit être un fichier texte délimité par des tabulations avec un élément par ligne au format suivant :

         * (Créatifs, Publicités standard) `**landing_page**`

           where `landing_page` est une URL de page d’entrée ou une URL de base valide.

           Exemple : http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink <tab> ** <tab> landing_page`

           where `sitelink` est le nom du lien de site et `landing_page` est une URL de page d’entrée ou une URL de base valide.

           Exemple : `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Le fichier peut contenir jusqu’à 10 000 lignes.

         * ([!DNL Google Merchant Center] groupes de produits et [DNL Microsoft® Advertising] publicités de produit) `product name <tab> ** <tab> landing_page`

           where `product name` est le nom du produit et `landing_page` est une URL de page d’entrée ou une URL de base valide.

           Exemple : `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Le fichier peut contenir jusqu’à 10 000 lignes.

      * Dans le champ de saisie, saisissez un élément par ligne au format suivant :

         * (Créatifs, Publicités standard) `landing_page`

           where `landing_page` est une URL de page d’entrée ou une URL de base valide.

           Exemple : http://www.example.com/travel.html

         * ([!DNL Microsoft® Advertising] sitelinks) `sitelink**landing_page`

           where `sitelink` est le nom du lien de site et `landing_page` est une URL de page d’entrée ou une URL de base valide.

           Exemple : `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] groupes de produits et [!DNL Microsoft® Advertising] publicités de produit) `product name**landing_page`

           where `product name` est le nom du produit et `landing_page` est une URL de page d’entrée ou une URL de base valide.

           Exemple : Acme PR208**http://www.example.com/travel.html

   1. Cliquez sur **[!UICONTROL Generate Tracking URLs]**.

1. (Facultatif) Copiez les URL (commençant par &quot;http&quot; ou &quot;https&quot;) dans l’écran ou la page de sortie et implémentez-les dans le compte de recherche ou de réseau social.

Pour les comptes disposant d’URL de destination, saisissez les valeurs dans la variable [!UICONTROL Base URL] des champs.

Pour les comptes disposant d’URL finales, saisissez la valeur à l’écran dans le [!UICONTROL Tracking Template] champ . Vous devez ajouter un paramètre pour l’URL finale après l’événement `&url=` (par exemple `{lpurl}`). Pour [!DNL Yahoo! Japan Ads] comptes, utiliser le paramètre `{lpurl}`. Pour une liste de [!DNL Google Ads] et [!DNL Microsoft® Advertising] pour indiquer les URL finales dans les modèles de tracking, voir la section [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348) (voir les paramètres &quot;Modèle de suivi uniquement&quot; dans la section &quot;Disponible&quot; [!DNL ValueTrack] Paramètres&quot;) et [[!DNL Microsoft® Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [A propos des outils de création et de décodage des balises de suivi](tracking-tools-about.md)
>* [Quand et comment générer des URL de suivi des clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Décodage d’une URL de suivi des clics Search, Social et Commerce](click-tracking-url-decode.md)
