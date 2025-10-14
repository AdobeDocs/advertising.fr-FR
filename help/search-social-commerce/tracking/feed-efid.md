---
title: Suivi des conversions à l’aide d’un flux d’identifiant EF
description: Découvrez comment utiliser un flux d’identifiant EF pour les données de suivi de conversion.
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# Suivi des conversions à l’aide d’un flux d’identifiant EF

Dans cette méthode, Advertising Cloud collecte une valeur `ef_id` chaque fois qu’un utilisateur clique sur la publicité et arrive sur la page d’entrée, et l’annonceur stocke la valeur `ef_id` avec les données de conversion et l’envoie dans un flux de données.

## Présentation de l’implémentation

*Gestionnaire de compte de l’agence, [!DNL Adobe] gestionnaire de compte et rôles utilisateur administrateur uniquement*

1. Utilisez les options de suivi de compte ou de campagne &quot;[!UICONTROL EF Redirect]&quot;, le type de redirection de &quot;[!UICONTROL Token]&quot; et &quot;[!UICONTROL Auto Upload]&quot; pour générer automatiquement une URL de destination ou une URL finale avec un jeton d’Adobe Advertising (ef_id) pour chaque mot-clé (pour le suivi au niveau des mots-clés) ou publicité (pour le suivi au niveau des publicités) dans le compte ou la campagne.

   >[!NOTE]
   >* Cette méthode ne nécessite pas que l’annonceur utilise des balises de suivi de conversion Adobe Advertising.
   >* Si vous basculez le type de redirection d’un compte ou d’une campagne existant de [!UICONTROL Standard] à [!UICONTROL Token], ou inversement, vous devez régénérer toutes les URL de suivi applicables.

   ef_id est renseigné et ajouté à l’URL de la page d’entrée lorsque l’utilisateur final clique sur la publicité et est redirigé vers un serveur d’Adobe Advertising. L’ef_id est ensuite transmis à l’annonceur dans l’URL de destination ou l’URL finale de la publicité ou du mot-clé. Voici un exemple d’URL de destination transmise à l’annonceur lors de la redirection :

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. L’annonceur extrait l’ef_id de la redirection et le stocke avec les données de conversion appropriées à inclure dans le fichier de flux. Ne modifiez pas ef_id ni sa casse.

1. (Facultatif mais recommandé) L’annonceur peut créer un ID de transaction unique pour chaque transaction à inclure dans le fichier de flux.

1. L’annonceur charge un fichier avec les [&#x200B; données de conversion requises](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) vers l’emplacement de serveur désigné.

1. Les services techniques analysent les données de conversion dans les fichiers chargés, puis chargent les données dans Adobe Advertising. Adobe Advertising effectue ensuite le suivi des données par rapport à des mots-clés, publicités et emplacements individuels, puis crée une prévision de recettes pour chacun d’eux.

1. Les services techniques valident les données traitées par rapport aux données de flux et recherchent toutes les [transactions orphelines](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Exigences liées aux fichiers pour les fichiers de flux de conversion](feed-file-requirements.md)
>* [Exigences de données pour les flux de données à l’aide des ID EF](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
