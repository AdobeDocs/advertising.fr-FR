---
title: Paramètres des publicités audio
description: Consultez les descriptions des paramètres d’annonce publicitaire disponibles pour les annonces publicitaires audio.
feature: DSP Ads
exl-id: 2fa1143b-6e83-4729-91cd-7a5da357509e
TQID: https://experienceleague.adobe.com/rP0SJspXvqzivctnNqe7b35mbL-ARZlGzC3cLAS-uwA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 277
ht-degree: 0%

---

# Paramètres des publicités audio

## [!UICONTROL Insert Ad Tag]

*Nouvelles annonces uniquement*

**[!UICONTROL URL]** : l’URL de balise VAST.

**[!UICONTROL Title]** : nom du fichier, qui est utilisé dans la vue [!UICONTROL Ads] et les rapports.

>[!TIP]
>
> Pour vérifier la validité d’une balise VAST, collez-la dans un navigateur et appuyez sur la touche **[!UICONTROL Enter]**. Si la balise est valide, un fichier XML contenant des `<VAST>` s’affiche en haut de l’écran.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Lecture seule) Type d’annonce publicitaire que vous créez, qui correspond au type d’emplacement auquel l’annonce publicitaire peut être associée. La valeur par défaut est *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Nom de l’annonce publicitaire. Le titre de la ressource est utilisé par défaut, mais vous pouvez en modifier le nom.

>[!TIP]
>
> Utilisez un nom facile à trouver lorsque vous joignez l’annonce à un emplacement, dans la vue [!UICONTROL Ads] et dans les rapports. Par exemple, décrivez le type d’unité et certains attributs clés (tels que Aperçu du produit Holiday : 30sec Audio »).

**[!UICONTROL Ad Duration]:** longueur du fichier audio. Il est automatiquement défini sur [!UICONTROL 15] ou [!UICONTROL 30], selon l’unité publicitaire sélectionnée.

Ce champ peut s’afficher ou non, selon les autorisations du compte.

**[!UICONTROL VAST Tag]:** (publicités à l’aide de balises VAST uniquement) URL d’une source publicitaire tierce. Assurez-vous que la balise VAST comprend uniquement des fichiers multimédias audio.

**[!UICONTROL Final VAST Tag]:** (publicités à l’aide de balises VAST uniquement) URL de la source publicitaire tierce avec les [macros de suivi Advertising DSP nécessaires](/help/dsp/campaign-management/macros.md) insérées, le cas échéant.

**[!UICONTROL Select Rate]:** (Utilisateurs avec autorisation uniquement) Taux prénégocié facturé via Adobe, ou l’un des taux que vous avez négociés et facturé via le fournisseur. Pour ajouter un taux, contactez l’équipe chargée de votre compte Adobe.

### [!UICONTROL Pixel]

<!-- **[!UICONTROL Pixel]:** -->

{{$include /help/_includes/dsp-ad-pixel.md}}

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités dans Advertising DSP](ad-about.md)
>* [Créer une seule annonce publicitaire](ad-create.md)
>* [Liste des emplacements associés à une publicité](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Macros ](/help/dsp/campaign-management/macros.md)
