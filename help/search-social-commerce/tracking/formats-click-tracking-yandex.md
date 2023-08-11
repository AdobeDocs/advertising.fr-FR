---
title: Formats de suivi des clics pour [!DNL Yandex]
description: Découvrez les formats de suivi des clics pour [!DNL Yandex] comptes.
exl-id: cf1d6c4b-9bcd-4b82-919f-c14dbaff9a76
feature: Search Tracking
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yandex]

Le format d’URL de destination de base suivant s’applique aux publicités sponsorisées :

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=90&ev_lx={phrase_id}&ev_crx={ad_id}&ev_ln={keyword}&ev_mt={source_type}&ev_ltx=&ev_src={source}&ev_pos={position}&ev_pt={position_type}&url=<the landing page>`

Exemple :

`http://pixel.everesttech.net/1234/cq?ev_sid=90&ev_lx={phrase_id}&amp;ev_crx={ad_id}&amp;ev_ln={keyword}&amp;ev_mt={source_type}&amp;ev_ltx=&amp;ev_src={source}&amp;ev_pos={position}&amp;ev_pt={position_type}&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` est une variable de l’identifiant unique de l’annonceur dans Adobe Advertising.
>
>* Ce format indique que la transmission de jetons est activée pour la campagne (valeur par défaut). Si la transmission de jeton est désactivée, remplacez `cq?` after `<advertiser_ID>` avec `c?`.
>
>* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés.
>
>* `source_type`  est le type de correspondance.
>
>* `source` indique si la publicité a été affichée sur un site de recherche ou de contenu.
>
>* `position` est le numéro de position de la publicité dans le bloc. Pour le trafic hors recherche, la valeur est &quot;0&quot;.
>
>* `position_type` est le bloc dans lequel la publicité a été affichée. [!DNL Yandex]. Valeurs possibles : &quot;premium&quot; (bloc supérieur), &quot;other&quot; (bloc de droite) ou &quot;none&quot; (trafic hors recherche).

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion Adobe Advertising](formats-click-tracking-about.md)
>* [Formats AMO ID](/help/integrations/analytics/ids.md#amo-id-formats)
