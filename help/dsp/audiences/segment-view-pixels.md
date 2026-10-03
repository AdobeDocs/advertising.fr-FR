---
title: Affichage des pixels de suivi pour un segment
description: Découvrez comment afficher les pixels de tracking pour un segment d’opt-out à la vente personnalisé ou CCPA.
feature: DSP Segments
exl-id: 3b67ab72-d7bb-45a0-b5ba-e4b811b7d2b3
TQID: 'https://experienceleague.adobe.com/jWneyyCriQcP299jQg-6Ggue0AObOfyehJwPvemYSfY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 2b670c6e-542a-5afe-b96b-d9ce7818cd55
    internal-label: DSP Segments
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
    internal-label: Segments
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 0%
---
# Affichage des pixels de suivi pour un segment

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

1. Placez le curseur sur la ligne de segment et cliquez sur **[!UICONTROL Get Pixel]**.

   * La balise de suivi des pages vues, qui effectue le suivi des visiteurs sur poste de travail et mobile vers une page web, est intitulée « [!UICONTROL Desktop or mobile websites] ». Pour les segments qui effectuent le suivi des ID de [!DNL ID5], remplacez `ID5_PARTNER_ID` dans la balise copiée par l’ID de partenaire qui [!DNL ID5] affecté à votre organisation lorsqu’elle a signé un accord avec [!DNL ID5]. Si vous ne connaissez pas votre ID de partenaire, contactez l’équipe chargée de votre compte Adobe.

     Ajoutez la balise aux pages dont vous souhaitez suivre les vues.

   * (Segments personnalisés uniquement) La balise de suivi d’impression, qui suit les utilisateurs exposés à une unité publicitaire sur des appareils de bureau, mobiles ou CTV, est intitulée « [!UICONTROL Desktop or mobile ads] ». Ajoutez la balise aux publicités dont vous souhaitez suivre les vues. Vous pouvez éventuellement ajouter la balise à un emplacement pour la joindre par défaut à toutes les publicités associées à l’emplacement.

Une fois qu’une balise de tracking est implémentée, vous pouvez utiliser le segment dans les cibles ou exclusions d’audience pour n’importe quel emplacement.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des audiences](audience-about.md)
>* [Créer un segment personnalisé](custom-segment-create.md)
>* [Modifier les informations sur le segment](segment-edit.md)
>* [Supprimer un segment](segment-delete.md)
>* [Partager ou arrêter le partage d’un segment](segment-share.md)
