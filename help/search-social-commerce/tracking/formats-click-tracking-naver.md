---
title: Formats de suivi des clics pour  [!DNL Naver]
description: Découvrez les formats de suivi des clics pour les comptes  [!DNL Naver] .
exl-id: b438652e-6e98-4223-8169-2bfb37500670
feature: Search Tracking
TQID: https://experienceleague.adobe.com/c1zAy1aKgr4MRpyiitdmO4VxP7kfKfFWHzYk88lvX2w
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 0%

---

# Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Naver]

Le format d’URL de destination de base suivant s’applique aux publicités sponsorisées :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=87&ev_cl={ef_uniqueid}&url=<the landing page>`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable pour l’ID unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission du jeton est activée pour la campagne (valeur par défaut). Si la transmission du jeton est désactivée, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés.

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi des conversions Adobe Advertising](formats-click-tracking-about.md)
>* [Formats d’ID AMO](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
