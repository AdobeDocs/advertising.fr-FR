---
title: Formats de suivi des clics pour les [!DNL Baidu]
description: Découvrez les formats de suivi des clics pour les comptes [!DNL Baidu].
exl-id: 4f4ed518-aa25-4a29-b263-c01f78b69b92
feature: Search Tracking
TQID: 'https://experienceleague.adobe.com/iV5-TNxdMov1LoPZzwP3RqkP93fp8A9TvAlY-2R-ZGo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 2206c6aa-b5c2-51b3-88e0-706d57048fe4
    internal-label: Search Tracking
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%
---
# Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Baidu]

Le format d’URL de destination de base suivant s’applique aux publicités sponsorisées :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=<ad network ID>&ev_cmpid=<campaignID>&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=<the landing page>`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=88&ev_cmpid=800577124&&ev_lx={keywordid}&ev_crx={creative}&ev_pl={placement}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable pour l’ID unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission du jeton est activée pour la campagne (valeur par défaut). Si la transmission du jeton est désactivée, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `<campaignID>` est une variable pour l’identifiant numérique de campagne.
>
>* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi des conversions Adobe Advertising](formats-click-tracking-about.md)
>* [Formats d’ID AMO](https://experienceleague.adobe.com/fr/docs/analytics/components/dimensions/amo-id#dimension-items)
