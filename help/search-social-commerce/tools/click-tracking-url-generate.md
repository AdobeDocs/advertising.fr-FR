---
title: Générer une URL de tracking des clics
description: Découvrez comment générer manuellement une URL de suivi des clics Search, Social et Commerce.
exl-id: 43a36869-146a-4c5f-b4f2-eddfb856480b
feature: Search Tools, Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Générez une URL de suivi des clics Search, Social et Commerce à l’aide de l’outil URL de suivi

*Annonceurs avec suivi des conversions Adobe Advertising uniquement*

Pour plus d’informations sur le moment où vous devez générer et implémenter manuellement une URL de suivi des clics, reportez-vous à la section « [ Quand et comment générer des URL de suivi des clics ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) ».

>[!NOTE]
>
>Cette fonctionnalité n’implémente pas le modèle de suivi ou l’URL de destination dans le compte publicitaire approprié.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Tracking URL]**.

1. Sélectionnez le compte réseau publicitaire dans la liste.

   (Mots-clés [!DNL Google Ads], texte, installation d’application mobile et annonces de recherche dynamique, emplacements, liens de site et groupes de produits) Les balises de suivi du champ Modèle de suivi s’affichent. Ils n’incluent aucun paramètre d’ajout au niveau du compte. Passez à l’étape 4.

   Pour tous les autres types de balises, saisissez des informations afin de générer une balise.

1. (Si nécessaire) Générez une balise :

   1. Spécifiez les pages de destination, avec des liens de site ou des noms de produits si nécessaire, de l’une des manières suivantes :

      * Spécifiez un fichier contenant les informations en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur **[!UICONTROL Browse]** pour localiser le fichier sur votre appareil ou réseau. Le fichier doit être un fichier texte délimité par des tabulations avec un élément par ligne au format suivant :

         * (contenus publicitaires, publicités standard) `**landing_page**`

           où `landing_page` est une URL de page de destination ou une URL de base valide.

           Exemple : http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] les liens du site) `sitelink <tab> ** <tab> landing_page`

           où `sitelink` est le nom du lien du site et `landing_page` est une URL de page de destination ou une URL de base valide.

           Exemple : `Careers <tab> ** <tab> http://www.example.com/careers.html`

           Le fichier peut contenir jusqu’à 10 000 lignes.

         * ([!DNL Google Merchant Center] des groupes de produits et [!DNL Microsoft Advertising] des annonces de produits) `product name <tab> ** <tab> landing_page`

           où `product name` est le nom du produit et `landing_page` est une URL de page de destination ou une URL de base valide.

           Exemple : `Acme PR208 <tab> ** <tab> http://www.example.com/travel.html`

           Le fichier peut contenir jusqu’à 10 000 lignes.

      * Dans le champ de saisie, saisissez un élément par ligne au format suivant :

         * (contenus publicitaires, publicités standard) `landing_page`

           où `landing_page` est une URL de page de destination ou une URL de base valide.

           Exemple : http://www.example.com/travel.html

         * ([!DNL Microsoft Advertising] les liens du site) `sitelink**landing_page`

           où `sitelink` est le nom du lien du site et `landing_page` est une URL de page de destination ou une URL de base valide.

           Exemple : `Careers**http://www.example.com/careers.html`

         * ([!DNL Google Merchant Center] des groupes de produits et [!DNL Microsoft Advertising] des annonces de produits) `product name**landing_page`

           où `product name` est le nom du produit et `landing_page` est une URL de page de destination ou une URL de base valide.

           Exemple : Acme PR208**http://www.example.com/travel.html

   1. Cliquez sur **[!UICONTROL Generate Tracking URLs]**.

1. (Facultatif) Copiez les URL (commençant par « http » ou « https ») à partir de l’écran ou de la page de sortie et implémentez-les dans la recherche ou le compte social.

Pour les comptes avec des URL de destination, saisissez les valeurs dans les champs de [!UICONTROL Base URL] appropriés.

Pour les comptes avec des URL finales, saisissez la valeur à l’écran dans le champ [!UICONTROL Tracking Template] approprié. Vous devez ajouter un paramètre pour l’URL finale après le paramètre `&url=` (tel que `{lpurl}`). Pour les comptes [!DNL Yahoo! Japan Ads], utilisez le paramètre `{lpurl}`. Pour obtenir la liste des paramètres de [!DNL Google Ads] et de [!DNL Microsoft Advertising] afin d’indiquer les URL finales dans les modèles de tracking, consultez la [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/6305348) (voir les paramètres « Modèle de tracking uniquement » dans la section sur « Paramètres de [!DNL ValueTrack] disponibles ») et la [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/3/en/56799/2).

>[!MORELIKETHIS]
>
>* [À propos des outils de création et de décodage des balises de tracking](tracking-tools-about.md)
>* [Quand et comment générer des URL de suivi des clics ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
>* [Décoder une URL de suivi des clics Search, Social et Commerce](click-tracking-url-decode.md)
