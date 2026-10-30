---
title: Personnalisation des URL de tracking pour une expérience
description: Découvrez comment personnaliser les URL de tracking de chaque contenu créatif dans une expérience avec le ciblage d’arborescence de décision.
feature: Creative Experiences
exl-id: ba3b15b4-116e-4caa-8ce1-4d2e488a6362
TQID: 'https://experienceleague.adobe.com/LjeF7eYU8V93W28VbV-D6NNWWwdKqywOP2BwzDwQAgo'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: f1a0ef49-c5d6-4fdf-b0dc-ae6685afe30b
    internal-label: Creative experiences
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 8a75f4a164b25ed8e73816c3d853d9650f470118
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%
---
# Personnaliser les URL de tracking pour les créatifs d’une expérience avec le ciblage de l’arborescence de décision

*Nœuds Target avec contenu publicitaire existant uniquement*

Pour les expériences avec le ciblage d’arborescence de décision, vous pouvez créer jusqu’à cinq URL de suivi d’impression personnalisées et cinq URL de suivi des clics personnalisées pour chaque élément créatif individuel utilisé pour l’expérience. Lorsque le remplacement de la page de destination est disponible, vous pouvez également spécifier une URL de page de destination personnalisée. Vous pouvez personnaliser les URL de suivi dans l’un des éditeurs d’arborescence de décision.

Les URL personnalisées sont utilisées uniquement pour les annonces créées à partir de l’expérience et ne sont pas enregistrées dans les paramètres de création de base dans [!UICONTROL Creative Libraries].

Le remplacement de la page de destination est disponible pour les expériences standard et pour les nœuds utilisant des contenus publicitaires par défaut. Pour les lots dynamiques attribués, les pages de destination sont déterminées par le flux et l’onglet de page de destination n’est pas affiché.

## Utilisation de l’éditeur piloté par l’IA (Beta) {#ai-editor}

Pendant que vous [créez](experience-create-targeting.md#ai-editor) ou [modifiez](experience-edit-targeting.md#ai-editor) l’expérience, utilisez les commandes de la zone de travail :

1. Sur le nœud feuille de contenu créatif situé sous le nœud cible, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Sélectionnez l’onglet de **[!UICONTROL Landing URL]** **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** ou (le cas échéant).

   Les contenus publicitaires sont regroupés par lot. Les tailles de contenu créatif par défaut de l’expérience déterminent les tailles de contenu créatif disponibles.

1. Développez le contenu créatif à modifier et effectuez l’une des opérations suivantes :

   * Pour ajouter ou modifier une URL personnalisée, saisissez l’URL dans le champ de saisie.

   * Pour ajouter une autre URL de tracking personnalisée, cliquez sur **[!UICONTROL Add URL]**, puis saisissez l&#39;URL dans le champ de saisie.

   * Pour supprimer une URL personnalisée, cliquez sur **[!UICONTROL Delete URL]**.

   Cliquez en dehors d’un champ modifié et corrigez les erreurs de validation avant d’enregistrer.

1. Cliquez sur **[!UICONTROL Save]** dans la boîte de dialogue pour mettre à jour l’arborescence de travail.

1. [Enregistrez l’expérience](#save) à partir de l’en-tête de l’arborescence.

## Utilisation de l’éditeur manuel {#manual-editor}

[Ouvrez l’éditeur manuel](experience-edit-targeting.md#experience-open) avant de suivre ces étapes.

1. Sur le nœud feuille de contenu créatif situé sous le nœud cible, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit Tracking URLs]**.

1. Sélectionnez l’onglet de **[!UICONTROL Landing URLs]** **[!UICONTROL Click Tracking URLs]**, **[!UICONTROL Impression Tracking URLs]** ou (le cas échéant).

   Les onglets répertorient les contenus publicitaires dans les lots attribués. Les tailles de contenu créatif par défaut de l’expérience déterminent les tailles de contenu créatif disponibles.<!-- There's no distinct "Creative Sizes" setting. -->

1. Développez le contenu créatif à modifier et effectuez l’une des opérations suivantes :

   * Pour ajouter ou modifier une URL personnalisée, saisissez l’URL dans le champ de saisie.

   * Pour ajouter une autre URL de tracking personnalisée, cliquez sur **[!UICONTROL +]**, puis saisissez l&#39;URL dans le champ de saisie.

   * Pour supprimer une URL personnalisée, placez le curseur sur la ligne Creative, puis cliquez sur ![Supprimer](/help/creative/assets/delete.png "Supprimer").

1. Cliquez sur **[!UICONTROL Save]** dans la boîte de dialogue pour mettre à jour l’arborescence de travail.

1. [Enregistrez l’expérience](#save) à partir de l’en-tête de l’arborescence.

## Enregistrer l’expérience {#save}

Les étapes suivantes s’appliquent aux deux éditeurs. L’enregistrement de la boîte de dialogue d’URL de tracking seule n’enregistre ni ne publie l’expérience.

{{$include /help/_includes/experience-save.md}}

>[!MORELIKETHIS]
>
>* [Affectez et annulez l’affectation des lots de contenu créatif à un nœud final d’une expérience](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [Personnaliser les URL de tracking pour une expérience sans ciblage d’arborescence de décision](experience-tracking-urls-no-targeting.md)
