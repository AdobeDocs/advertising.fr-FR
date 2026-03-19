---
title: Gérer les sources d’audience pour activer les audiences d’ID universel
description: Découvrez comment créer et gérer une source pour importer des audiences de votre plateforme de données clients et les convertir en segments contenant des identifiants universels.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: b14f9c4ff59332c8850d1c1534d286aa79fe575a
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# Gérer les sources d’audience pour activer les audiences d’ID universel

*Fonction Beta*

Créez une source dans DSP pour chaque audience propriétaire de votre plateforme de données client que vous souhaitez convertir en segments contenant des types d’identifiants universels spécifiés. Vous pouvez importer les segments dans le compte DSP de votre organisation ou dans un compte d’annonceur. Les frais de données sont appliqués en fonction des types d’ID universels sélectionnés. Une fois que vous avez créé une source, des étapes supplémentaires sont nécessaires pour ingérer les audiences de chaque plateforme de données client. Reportez-vous à la remarque à la fin de la procédure pour créer une source.

Vous pouvez par la suite modifier les types d’identifiants universels vers lesquels l’audience source est traduite et afficher un journal des modifications.

Vous pouvez également supprimer une source.

## Création d’une source d’audience

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Cliquez sur **[!UICONTROL Add Source]**.

1. Dans le menu [!UICONTROL Select a Type], sélectionnez votre [plateforme de données client](source-about.md) :

   * *[!UICONTROL RT-CDP]* : la [!DNL Adobe Real-Time CDP].

   * *[!UICONTROL ActionIQ]* : plateforme de données client [!DNL ActionIQ].

   * *[!UICONTROL Amperity]* : plateforme de données client [!DNL Amperity].

   * *[!UICONTROL Optimizely]* : plateforme de données client [!DNL Optimizely].

   * *[!UICONTROL Tealium CDP]* : (utilisateurs configurés uniquement) Plateforme de données client [!DNL Tealium].

1. Spécifiez le [!UICONTROL Data Visibility Level] : *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Saisissez les [paramètres source](#source-settings) restants.

   Conservez une copie du [!UICONTROL Source Key] généré. Vous aurez besoin de la valeur plus tard.

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Après avoir créé une source pour votre plateforme de données client, vous devez effectuer des étapes supplémentaires pour importer votre audience. Voir le [workflow pour  [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md), <!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> le [workflow pour  [!DNL Amperity]](source-amperity.md), le [workflow pour  [!DNL Optimizely]](source-optimizely.md) et le [workflow pour  [!DNL Tealium]](source-tealium.md).

## Modification des types d’identifiants pour une source d’audience

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Placez le curseur sur la ligne source, puis cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les [ID sélectionnés pour la source](#source-settings).

1. Cliquez sur **[!UICONTROL Save]**.

## Supprimer une source d’audience

La suppression d’une source supprime les segments traduits par la source.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Placez le curseur sur la ligne source, puis cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Affichage du journal des modifications d’une source d’audience

Vous pouvez afficher les détails des modifications apportées à un enregistrement de source d’audience et éventuellement joindre des notes au journal.

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Placez le curseur sur la ligne source, puis cliquez sur **[!UICONTROL Change log]**.

1. (Facultatif) Pour joindre une note au journal des modifications :

   1. Placez le curseur sur la ligne source, puis cliquez sur **[!UICONTROL Add Notes]**.

   1. Saisissez la note, puis cliquez sur **[!UICONTROL Save]**.

      La longueur maximale est de 256 caractères.

1. (Facultatif) Pour ouvrir le journal dans un écran de détails plus grand, placez le curseur sur la ligne source et cliquez sur **[!UICONTROL View Details]**.

## Paramètres de la source d’audience {#source-settings}

**[!UICONTROL Data Visibility Level]:** indique si les segments sont disponibles pour un seul annonceur ayant accès au compte (*[!UICONTROL Advertiser]*) ou pour tous les annonceurs ayant accès au compte *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** (visibilité au niveau de l’annonceur uniquement) Annonceur pour lequel les segments sont disponibles. Sélectionnez-en un dans la liste des annonceurs ayant accès au compte.

**[!UICONTROL Enter IMS Org Id]:** (sources de [!DNL Real-Time CDP] uniquement) ID d’organisation Adobe Experience Cloud pour le compte [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** types d’ID auxquels vous convertirez vos informations d’identification personnelle (PII). Si vous sélectionnez plusieurs types, le segment généré est renseigné avec des valeurs pour chaque type d’identifiant sélectionné (par exemple un [!DNL RampID] et un [!DNL Unified ID2.0] pour chaque adresse e-mail). Les frais de données sont appliqués en conséquence.

Pour [!DNL RampID] et [!DNL Unified ID2.0], le fournisseur recherche chaque adresse e-mail pour voir si un ID existe déjà et traduit l’adresse en un ID correspondant le cas échéant. S’il n’existe pas d’ID pour l’adresse, un nouvel ID est créé.

>[!NOTE]
>
>Vous ne pouvez cibler qu’un seul type d’identifiant dans un seul emplacement. Pour tester les performances par type d’identifiant, [créez un emplacement distinct](/help/dsp/campaign-management/placements/placement-create.md) pour chaque type d’identifiant du segment.

* *[!DNL RampID]:* pour convertir des informations d’identification personnelles en [!DNL RampID]. Vous pouvez utiliser [!DNL RampIDs] pour recibler les utilisateurs connectés et pour mesurer les [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0](Beta) :* pour convertir les informations d’identification personnelles en un [identifiant unifié 2.0](https://unifiedid.com) pour le reciblage des utilisateurs connectés.

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Conditions d’utilisation de la conversion des informations d’identification personnelles en identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les conditions une seule fois avant de pouvoir convertir des données en un nouveau type d’identifiant. Pour les clients qui disposent de contrats de service géré, l’équipe chargée de votre compte Adobe obtiendra votre consentement et acceptera les conditions au nom de votre entreprise. Pour lire les termes, cliquez sur **>**. Pour accepter les conditions, faites défiler l’écran jusqu’au bas des conditions et cliquez sur **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Lecture seule ; générée automatiquement) Clé source que vous pouvez utiliser pour créer une connexion de destination dans la plateforme de données client afin de pousser les audiences vers Advertising DSP. Vous pouvez copier la valeur dans le presse-papiers pour la coller dans les paramètres de connexion de destination ou dans un fichier.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [Convertir les ID utilisateur de  [!DNL Adobe Real-Time CDP]  en ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir les ID utilisateur de  [!DNL Amperity]  en ID universels](/help/dsp/audiences/sources/source-amperity.md)
>* [Convertir les ID utilisateur de  [!DNL Optimizely]  en ID universels](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convertir les ID utilisateur de  [!DNL Tealium]  en ID universels](/help/dsp/audiences/sources/source-tealium.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
