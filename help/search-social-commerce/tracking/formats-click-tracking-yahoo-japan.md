---
title: Formats de suivi des clics pour [!DNL Yahoo! Japan Ads]
description: Découvrez les formats de suivi des clics pour [!DNL Yahoo! Japan Ads] comptes.
exl-id: 4584f2c4-8090-4931-bd44-0df42f350755
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yahoo! Japan Ads]

Les formats de modèle de suivi de base suivants s’appliquent aux publicités sponsorisées :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

ou, lorsque l’option de balisage automatique est définie pour le compte dans [!DNL Yahoo! Japan Ads]:

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si la transmission de jeton est désactivée, remplacez `cq?` after `<advertiser_ID>` avec `c?`.
>
>* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion Adobe Advertising](formats-click-tracking-about.md)
>* [Formats du code de suivi s\_kwcid](skwcid-tracking-parameter.md)
