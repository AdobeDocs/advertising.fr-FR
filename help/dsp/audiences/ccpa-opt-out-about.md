---
title: À propos de [!UICONTROL CCPA Opt-out-of-Sale] segments et rapports
description: Découvrez comment créer des segments pour effectuer le suivi des ID à partir des demandes d’opposition à la vente des informations personnelles du CCPA et comment récupérer des rapports sur les ID.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# À propos de [!UICONTROL CCPA Opt-out-of-Sale] segments et rapports

Vous pouvez effectuer le suivi des ID d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, conformément à la California Consumer Privacy Act (CCPA), en [créant et en mettant en oeuvre un segment d’opposition à la vente des informations personnelles du CCPA](ccpa-opt-out-segment-create.md). Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente des informations personnelles du CCPA.

Une fois la balise de pixel de segment implémentée, Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

## Rapports d’exclusion de la vente aux consommateurs

Adobe Advertising génère des rapports mensuels sur les identifiants que les clients ont envoyés pour les demandes d’exclusion de la vente pour le compte. Les données consolident les demandes capturées à l’aide des segments d’opposition à la vente des informations personnelles (CCPA) qui ont été créés dans DSP et les envois effectués via l’API du Privacy Service.  Les rapports sont générés le premier de chaque mois pour le mois précédent. Par exemple, la liste mensuelle des utilisateurs pour juin est disponible le 1er juillet.

Chaque rapport est disponible sous la forme d’un fichier texte de données séparées par des tabulations compressé au format GZIP. Les identifiants utilisateur capturés dans les segments d’opposition à la vente des informations personnelles (CCPA) sont identifiés par le segment et par l’annonceur.

Vous pouvez [ récupérer les liens vers les rapports mensuels ](ccpa-opt-out-segment-report-retrieve.md) créés au cours des trois mois précédents, soit depuis DSP, soit en utilisant le DSP [!DNL Trafficking API]. Chaque lien est valide pendant sept jours, mais est actualisé chaque fois qu’un client tente d’en récupérer un.

>[!MORELIKETHIS]
>
>* [Prise en charge des Adobes Advertising pour le California Consumer Privacy Act : prise en charge de l’exclusion des consommateurs](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Créer et implémenter un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Récupérer les rapports d’exclusion de la vente pour les consommateurs](ccpa-opt-out-segment-report-retrieve.md)
>* [À propos de la gestion de l’audience](audience-about.md)
