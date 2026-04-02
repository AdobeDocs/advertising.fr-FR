---
title: À propos des [!UICONTROL Simple Ad Serving]
description: Découvrez les offres [!UICONTROL Simple Ad Serving] à l’aide de pixels de suivi d’événement.
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
TQID: https://experienceleague.adobe.com/w4KFePatd7CZ1xC8dd1CItl88-6myAZw8TuatHzHnRI
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# À propos des [!UICONTROL Simple Ad Serving]

[!UICONTROL Simple Ad Serving] fournit une diffusion et un reporting d’annonces garantis et non décisionnels pour un éditeur spécifié et un type d’annonce unique à l’aide d’un emplacement unique dédié. Utilisez [!DNL Simple Ad Serving] lorsque votre éditeur ne peut pas exécuter votre offre via les ID d’offre. L’éditeur gère l’ensemble du ciblage, de la limitation et du rythme budgétaire, ainsi que de la limitation de la fréquence. Exécutez ces transactions au moyen de pixels de suivi d’événement.

Avec [!UICONTROL Simple Ad Serving], chaque publicité est diffusée directement par l’éditeur (serveur de sites) et DSP fournit un pixel de suivi d’événement à envoyer à l’éditeur, qui doit mettre en œuvre le pixel et traiter les publicités DSP. Selon le type d’inventaire, les pixels d’événement mesurent les événements d’impression, de clic publicitaire et de lecture vidéo.

Les types d&#39;annonces suivants sont disponibles :

* Pré-roll standard pour ordinateurs de bureau
* pre-roll pour tablette et mobile standard
* pre-roll standard pour téléviseur connecté
* afficher
* audio

Vous pouvez créer une offre [!UICONTROL Simple Ad Serving] dans la vue [!UICONTROL Inventory] > [!UICONTROL Deals] . DSP génère automatiquement un emplacement avec le sous-type « [!DNL Simple ad serving] » pour la publicité. L’emplacement cible l’offre, mais n’autorise pas de ciblage, de budget ou de capping de la fréquence supplémentaires. Vous ne pouvez modifier que certains paramètres de l’offre, tels que le nom de l’offre, le CPM, les impressions et les dates de vol.<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

Les emplacements [!UICONTROL Simple Ad Serving] ne sont pas conformes aux fonds utilisables du compte ou aux budgets de campagne et de package. Toutefois, les dépenses sont comptabilisées dans ces budgets. Même lorsque le CPM est à 0 $, les données d’événement sont toujours suivies.

>[!MORELIKETHIS]
>
>* [Créer un [!UICONTROL Simple Ad Serving] contrat](simple-deal-create.md)
>* [Modifier les paramètres de l’offre [!UICONTROL Simple Ad Serving]](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] les paramètres](simple-deal-settings.md)
>* [Afficher un rapport détaillé pour une affaire](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
