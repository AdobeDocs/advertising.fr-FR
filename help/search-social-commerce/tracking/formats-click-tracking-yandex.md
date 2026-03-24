---
title: Formats de suivi des clics pour  [!DNL Yandex]
description: Découvrez les formats de suivi des clics pour les comptes  [!DNL Yandex] .
exl-id: bcbd369b-b98d-491c-a921-58bf79e01744
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yandex]

Le format d’URL de destination de base suivant s’applique aux publicités sponsorisées :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable pour l’ID unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission du jeton est activée pour la campagne (valeur par défaut). Si la transmission du jeton est désactivée, remplacez `cq?` après `<advertiser_ID>` par `c?`.
>
>* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés.
>
>* `source_type` est le type de correspondance.
>
>* `source` s’agit de savoir si la publicité a été affichée sur un site de recherche ou basé sur du contenu.
>
>* `position` est le numéro de position de l’annonce publicitaire dans le bloc. Pour le trafic hors recherche, la valeur est « 0 ».
>
>* `position_type` est le bloc dans lequel la publicité a été affichée sur [!DNL Yandex]. Valeurs possibles : « premium » (bloc supérieur), « other » (bloc de droite) ou « none » (trafic hors recherche).

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi des conversions Adobe Advertising](formats-click-tracking-about.md)
>* [Formats d’ID AMO](https://experienceleague.adobe.com/fr/docs/analytics/components/dimensions/amo-id#dimension-items)
