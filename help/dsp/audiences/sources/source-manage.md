---
title: Gestion des sources d’audience pour activer les audiences d’ID universelles
description: Découvrez comment créer et gérer une source pour importer des audiences de votre plateforme de données client et les convertir en segments contenant des ID universels.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# Gestion des sources d’audience pour activer les audiences d’ID universelles

*Fonctionnalité Beta*

Créez une source dans DSP pour chaque audience propriétaire de votre plateforme de données client que vous souhaitez convertir en segments contenant des types d’ID universels spécifiés. Vous pouvez importer les segments dans le compte DSP de votre entreprise ou dans un compte publicitaire. Les frais de données sont appliqués en fonction des types d’ID universels sélectionnés. Une fois que vous avez créé une source, des étapes supplémentaires sont nécessaires pour ingérer les audiences à partir de chaque plateforme de données client. Consultez la note à la fin de la procédure de création d’une source.

Vous pouvez ensuite modifier les types d’ID universels vers lesquels l’audience source est traduite et afficher un journal des modifications.

Vous pouvez également supprimer une source.

## Création d’un Source d’audience

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Cliquez sur **[!UICONTROL Add Source]**.

1. Dans le menu [!UICONTROL Select a Type], sélectionnez votre [plateforme de données client](source-about.md) :

   * *[!UICONTROL RT-CDP]* : [!DNL Adobe Real-Time CDP].

   * *[!UICONTROL ActionIQ]* : plateforme de données client [!DNL ActionIQ].

   * *[!UICONTROL Amperity]* : plateforme de données client [!DNL Amperity].

   * *[!UICONTROL Optimizely]* : plateforme de données client [!DNL Optimizely].

   * *[!UICONTROL Tealium CDP]* : (utilisateurs configurés uniquement) plateforme de données client [!DNL Tealium].

1. Spécifiez [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Saisissez les [paramètres source](#source-settings) restants.

   Conservez une copie de l’ [!UICONTROL Source Key] généré. Vous aurez besoin de la valeur plus tard.

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Après avoir créé une source pour votre plateforme de données client, vous devez suivre d’autres étapes pour importer votre audience. Voir le [workflow pour [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md),<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> le [workflow pour [!DNL Amperity]](source-amperity.md), le [workflow pour [!DNL Optimizely]](source-optimizely.md) et le [workflow pour [!DNL Tealium]](source-tealium.md).

## Modification des types d’ID pour un Source d’audience

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Placez le curseur sur la ligne source et cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les [ID sélectionnés pour la source](#source-settings).

1. Cliquez sur **[!UICONTROL Save]**.

## Suppression d’un Source d’audience

La suppression d’une source supprime les segments traduits via la source.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Placez le curseur sur la ligne source et cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Affichage du journal des modifications d’un Source d’audience

Vous pouvez afficher des détails sur les modifications apportées à un enregistrement source d’audience et éventuellement joindre des notes au journal.

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Placez le curseur sur la ligne source et cliquez sur **[!UICONTROL Change log]**.

1. (Facultatif) Pour joindre une note au journal des modifications :

   1. Placez le curseur sur la ligne source et cliquez sur **[!UICONTROL Add Notes]**.

   1. Saisissez la note, puis cliquez sur **[!UICONTROL Save]**.

      La longueur maximale est de 256 caractères.

1. (Facultatif) Pour ouvrir le journal dans un écran de détail plus grand, placez le curseur sur la ligne source et cliquez sur **[!UICONTROL View Details]**.

## Paramètres d’Audience Source {#source-settings}

**[!UICONTROL Data Visibility Level]:** Indique si les segments sont disponibles pour un seul annonceur ayant accès au compte (*[!UICONTROL Advertiser]*) ou pour tous les annonceurs ayant accès au compte *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (Visibilité au niveau de l’annonceur uniquement) L’annonceur pour lequel les segments sont disponibles. Sélectionnez-en un dans la liste des annonceurs ayant accès au compte.

**[!UICONTROL Enter IMS Org Id]:** ([!DNL Real-Time CDP] sources uniquement) ID d’organisation Adobe Experience Cloud pour le compte [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** Types d’ID dans lesquels vous convertirez vos informations d’identification personnelle (PII). Si vous sélectionnez plusieurs types, le segment généré est renseigné avec des valeurs pour chaque type d’ID sélectionné (par exemple, [!DNL RampID] et [!DNL Unified ID2.0] pour chaque adresse électronique). Les taxes sur les données sont appliquées en conséquence.

Pour [!DNL RampID] et [!DNL Unified ID2.0], le fournisseur recherche chaque adresse électronique pour voir si un ID existe déjà et convertit l’adresse en un ID correspondant le cas échéant. Si aucun identifiant n’existe pour l’adresse, un nouvel identifiant est créé.

>[!NOTE]
>
>Vous ne pouvez cibler qu’un seul type d’ID au sein d’un seul emplacement. Pour tester les performances par type d’identifiant, [ créez un emplacement](/help/dsp/campaign-management/placements/placement-create.md) distinct pour chaque type d’identifiant dans le segment.

* *[!DNL RampID]:* Pour convertir les PII en [!DNL RampID]. Vous pouvez utiliser [!DNL RampIDs] pour recibler les utilisateurs qui se connectent et pour la mesure [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0] (Beta) :* Pour convertir les PII en [ ID unifié 2.0](https://unifiedid.com) pour recibler les utilisateurs qui se connectent.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Conditions d’utilisation pour la conversion des PII en identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les termes une fois avant de pouvoir convertir les données en un nouveau type d’ID. Pour les clients disposant de contrats de service géré, votre équipe de compte d’Adobe obtiendra votre consentement et acceptera les conditions pour le compte de votre organisation. Pour lire les termes, cliquez sur **>**. Pour accepter les termes, faites défiler l’écran jusqu’au bas des termes et cliquez sur **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Lecture seule ; généré automatiquement) clé source que vous pouvez utiliser pour créer une connexion de destination dans la plateforme de données client afin de pousser des audiences vers Advertising DSP. Vous pouvez copier la valeur dans le presse-papiers pour la coller dans les paramètres de connexion de destination ou dans un fichier.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [Convertir les ID utilisateur de [!DNL Adobe Real-Time CDP]  en ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir les ID utilisateur de [!DNL Amperity]  en ID universels](/help/dsp/audiences/sources/source-amperity.md)
>* [Convertir les ID utilisateur de [!DNL Optimizely]  en ID universels](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convertir les ID utilisateur de [!DNL Tealium]  en ID universels](/help/dsp/audiences/sources/source-tealium.md)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)
