---
title: Formats de suivi des clics pour [!DNL Yahoo! Japan Ads]
description: Découvrez les formats de suivi des clics pour les comptes  [!DNL Yahoo! Japan Ads] .
exl-id: 79e45205-5c72-4612-9b60-36538e3c48c4
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yahoo! Japan Ads]

Les formats de modèle de suivi de base suivants s’appliquent aux publicités sponsorisées :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}`

ou, lorsque l’option de balisage automatique est définie pour le compte dans [!DNL Yahoo! Japan Ads] :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=!{unescapedlpurl}/?yclid=<yclid>`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=94&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_dvc={device}&url=http%3A//www.example.com/?yclid=1234567890`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si le transfert de jeton est désactivé, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion d’Adobe Advertising](formats-click-tracking-about.md)
>* [Formats AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
