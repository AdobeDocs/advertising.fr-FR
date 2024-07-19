---
title: Formats de suivi des clics pour [!DNL Baidu]
description: Découvrez les formats de suivi des clics pour les comptes  [!DNL Baidu] .
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Baidu]

Le format d’URL de destination de base suivant s’applique aux publicités sponsorisées :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si le transfert de jeton est désactivé, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `<campaignID>` est une variable de l’identifiant de campagne numérique.
>
>* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion d’Adobe Advertising](formats-click-tracking-about.md)
>* [Formats AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
