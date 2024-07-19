---
title: Affichage des pixels de suivi pour un segment
description: Découvrez comment afficher les pixels de suivi pour un segment d’exclusion de vente personnalisé ou CCPA.
feature: DSP Segments
exl-id: 3b67ab72-d7bb-45a0-b5ba-e4b811b7d2b3
source-git-commit: 8e3afe50db8f3d0795838c071a01f3c5688f701f
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Affichage des pixels de suivi pour un segment

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

1. Placez le curseur sur la ligne de segment et cliquez sur **[!UICONTROL Get Pixel]**.

   * La balise de suivi des pages vues, qui effectue le suivi des visiteurs de bureau et mobiles sur une page web, est étiquetée &quot;[!UICONTROL Desktop or mobile websites]&quot;. Pour les segments qui effectuent le suivi de [!DNL ID5] ID, remplacez `ID5_PARTNER_ID` dans la balise copiée par l’ID de partenaire affecté à votre organisation lors de la signature d’un accord avec [!DNL ID5]. [!DNL ID5] Si vous ne connaissez pas votre identifiant de partenaire, contactez votre équipe de compte d’Adobe.

     Ajoutez la balise aux pages dont vous souhaitez effectuer le suivi des vues.

   * (Segments personnalisés uniquement) La balise de suivi d’impression, qui suit les utilisateurs exposés à une unité publicitaire sur un ordinateur de bureau, un appareil mobile ou un appareil CTV, est étiquetée &quot;[!UICONTROL Desktop or mobile ads]&quot;. Ajoutez la balise aux publicités dont vous souhaitez effectuer le suivi. Vous pouvez éventuellement ajouter la balise à un emplacement pour la joindre par défaut à toutes les publicités associées à l’emplacement.

Une fois qu’une balise de suivi est implémentée, vous pouvez utiliser le segment dans les cibles ou exclusions d’audience pour n’importe quel emplacement.

>[!MORELIKETHIS]
>
>* [À propos de la gestion de l’audience](audience-about.md)
>* [Créer un segment personnalisé](custom-segment-create.md)
>* [Modifier les informations sur le segment](segment-edit.md)
>* [Supprimer un segment](segment-delete.md)
>* [Partager ou arrêter le partage d’un segment](segment-share.md)
