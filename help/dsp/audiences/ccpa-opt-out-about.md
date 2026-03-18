---
title: À propos des segments et des rapports [!UICONTROL CCPA Opt-out-of-Sale]
description: Découvrez comment créer des segments pour effectuer le suivi des identifiants à partir des demandes d’opposition à la vente du CCPA et comment récupérer les rapports des identifiants.
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: e61f3c7d066a72f9a438ef292122cdf99370fd0c
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# À propos des segments et des rapports [!UICONTROL CCPA Opt-out-of-Sale]

Vous pouvez suivre les ID des utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, conformément à la Loi sur la protection de la vie privée des consommateurs de Californie (CCPA), en [créant et en implémentant un segment d’opposition à la vente des consommateurs de la CCPA](ccpa-opt-out-segment-create.md). Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente du CCPA.

Une fois la balise de pixel de segment implémentée, Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

## Rapports de désinscription de la vente par les consommateurs

Adobe Advertising génère des rapports mensuels sur les identifiants que les clients et clientes ont envoyés pour des requêtes d’opposition à la vente des informations personnelles pour le compte. Les données consolident les requêtes capturées à l’aide des segments d’opposition à la vente du CCPA qui ont été créés dans DSP et de tout envoi effectué via l’API Privacy Service.  Les rapports sont générés le premier de chaque mois du mois précédent. Par exemple, la liste mensuelle des utilisateurs de juin est disponible le 1er juillet.

Chaque rapport est disponible sous la forme d’un fichier texte séparé par des tabulations compressé au format GZIP. Les identifiants d’utilisateur capturés dans les segments d’opposition à la vente du CCPA sont identifiés par segment et par annonceur.

Vous pouvez [récupérer les liens vers les rapports mensuels](ccpa-opt-out-segment-report-retrieve.md) créés au cours des trois mois précédents, depuis DSP ou à l’aide de l’[!DNL Trafficking API] DSP. Chaque lien est valide pendant sept jours, mais est actualisé chaque fois qu’un client tente d’en récupérer un.

>[!MORELIKETHIS]
>
>* [Prise en charge par Adobe Advertising de la Loi sur la confidentialité des consommateurs de Californie : prise en charge du droit d’opposition des consommateurs](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [Création et implémentation d’un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Récupérer les rapports d’opposition à la vente des clients](ccpa-opt-out-segment-report-retrieve.md)
>* [À propos de la gestion de l’audience](audience-about.md)
