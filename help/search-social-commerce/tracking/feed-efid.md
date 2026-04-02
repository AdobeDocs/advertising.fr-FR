---
title: Suivi des conversions à l’aide d’un flux d’ID d’EF
description: Découvrez comment utiliser un flux d’ID EF pour les données de suivi des conversions.
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
TQID: https://experienceleague.adobe.com/D4OpKvTL-jjIOgMaakH78aYA7q9p2BXcc2P-RI8blfY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---

# Suivi des conversions à l’aide d’un flux d’ID d’EF

Dans cette méthode, Advertising Cloud collecte une valeur `ef_id` chaque fois qu’un utilisateur clique sur une publicité et arrive à la page de destination, et l’annonceur stocke la valeur `ef_id` avec les données de conversion et l’envoie dans un flux de données.

## Présentation de l’implémentation

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte [!DNL Adobe] et d’utilisateur administrateur uniquement*

1. Utilisez les options de suivi de compte ou de campagne « [!UICONTROL EF Redirect] », le type de redirection « [!UICONTROL Token] » et « [!UICONTROL Auto Upload] » pour générer automatiquement une URL de destination ou une URL finale avec un jeton Adobe Advertising (ef_id) pour chaque mot-clé (pour le suivi au niveau du mot-clé) ou publicité (pour le suivi au niveau de l’annonce) dans le compte ou la campagne.

   >[!NOTE]
   >* Cette méthode ne nécessite pas que l’annonceur utilise les balises de suivi des conversions Adobe Advertising.
   >* Si vous passez du type de redirection d’un compte ou d’une campagne existant de [!UICONTROL Standard] à [!UICONTROL Token], ou vice versa, vous devez régénérer toutes les URL de suivi applicables.

   L’ef_id est renseigné et ajouté à l’URL de la page de destination lorsque l’utilisateur final clique sur la publicité et est redirigé vers un serveur Adobe Advertising. L’ef_id est ensuite transmis à l’annonceur dans l’URL de destination ou l’URL finale pour l’annonce ou le mot-clé. Voici un exemple d’URL de destination transmise à l’annonceur pendant la redirection :

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. L’annonceur extrait le ef_id de la redirection et le stocke avec les données de conversion pertinentes à inclure dans le fichier de flux. Ne modifiez pas l’ef_id ni sa casse.

1. (Facultatif mais recommandé) L’annonceur peut créer un identifiant de transaction unique pour chaque transaction à inclure dans le fichier de flux.

1. L’annonceur télécharge un fichier contenant les [données de conversion requises](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) à l’emplacement du serveur désigné.

1. Les services techniques analysent les données de conversion dans les fichiers chargés, puis chargent les données dans Adobe Advertising. Adobe Advertising effectue ensuite le suivi des données par rapport à des mots-clés, des annonces et des emplacements individuels et crée des prévisions de chiffre d’affaires pour chacun.

1. Les services techniques valident les données traitées par rapport aux données de flux et vérifient toute [transaction orpheline](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [Exigences relatives aux fichiers de flux de conversion](feed-file-requirements.md)
>* [Exigences en matière de données pour les flux de données utilisant des identifiants EF](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
