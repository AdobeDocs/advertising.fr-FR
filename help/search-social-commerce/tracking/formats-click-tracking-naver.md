---
title: Formats de suivi des clics pour [!DNL Naver]
description: Découvrez les formats de suivi des clics pour [!DNL Naver] comptes.
exl-id: ff243eb5-d768-4e5c-b5b3-015fe22c9d5a
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Naver]

Le format d’URL de destination de base suivant s’applique aux publicités sponsorisées :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si la transmission de jeton est désactivée, remplacez `cq?` after `<advertiser_ID>` avec `c?`.
>
* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion Adobe Advertising](formats-click-tracking-about.md)
>* [Formats du code de suivi s\_kwcid](skwcid-tracking-parameter.md)
