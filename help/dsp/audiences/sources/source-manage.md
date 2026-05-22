---
title: Gérer les sources d’audience pour activer les audiences d’ID universel
description: Découvrez comment créer et gérer une source pour importer des audiences de votre plateforme de données clients et les convertir en segments contenant des identifiants universels.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
TQID: https://experienceleague.adobe.com/us8NC8BEngb240MAW8hEo-DHGoW7MRDWvu0HedMsnFs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 881
ht-degree: 0%

---

# Gérer les sources d’audience pour activer les audiences d’ID universel

Créez une source dans DSP pour chaque audience propriétaire de votre plateforme de données client que vous souhaitez importer ou convertir en segments contenant des types d’identifiants universels spécifiés. Vous pouvez importer les segments dans le compte DSP de votre organisation ou dans un compte d’annonceur. Lorsque vous convertissez des audiences en identifiants universels, des frais sont appliqués en fonction des types d’identifiants universels sélectionnés. Une fois que vous avez créé une source, des étapes supplémentaires sont nécessaires pour diffuser les audiences sources à partir de chaque plateforme de données client. Reportez-vous à la remarque à la fin de la procédure pour créer une source.

Pour toutes les plateformes de données client à l’exception de [!DNL AdFixus], vous pouvez par la suite modifier les types d’identifiants universels vers lesquels l’audience source est traduite et afficher un journal des modifications.

Vous pouvez également supprimer une source.

## Création d’une source d’audience

Vous pouvez créer une source pour chaque combinaison de partenaire d’ID universel et de compte ou d’annonceur individuel. Par exemple, vous pouvez avoir une source de [!UICONTROL RT-CDP] pour le compte, une source de [!UICONTROL RT-CDP] pour l’annonceur 1 et une source de [!UICONTROL RT-CDP] pour l’annonceur 2.

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Cliquez sur **[!UICONTROL Add Source]**.

1. Dans le menu [!UICONTROL Select a Type], sélectionnez votre [plateforme de données client](source-about.md) :

   * *[!UICONTROL RT-CDP]* : la [!DNL Adobe Real-Time CDP].

   * *[!UICONTROL AdFixus ID]* : plateforme de données client [!DNL AdFixus]. Applicable aux annonceurs en Australie uniquement.

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
>Après avoir créé une source pour votre plateforme de données client, vous devez effectuer des étapes supplémentaires pour importer votre audience :
>* Pour les sources [!DNL ActionIQ], travaillez avec l’équipe chargée de votre compte Adobe.
>* Pour les autres types de sources, voir <!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), --> le [workflow pour [!DNL AdFixus]](source-adfixus.md), the [workflow for [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md), le [workflow pour [!DNL Amperity]](source-amperity.md), le [workflow pour [!DNL Optimizely]](source-optimizely.md) et le [workflow pour [!DNL Tealium]](source-tealium.md).

## Modification des types d’identifiants pour une source d’audience

*Disponible pour toutes les plateformes de données client prises en charge, à l’exception de[!DNL AdFixus]*

<!-- 
Clarify this:

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses that you shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we don't delete any historical IDs of that type from the segments shared through the source.

-->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Placez le curseur sur la ligne source, puis cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les [ID sélectionnés pour la source](#source-settings).

1. Cliquez sur **[!UICONTROL Save]**.

## Supprimer une source d’audience

La suppression d’une source supprime les segments importés par le biais de la source, y compris tous les identifiants traduits.<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

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

**[!UICONTROL Enter IMS Org Id]:** (sources de [!DNL Real-Time CDP] uniquement) ID d’organisation de l’entreprise Adobe CX pour le compte [!DNL Adobe Experience Platform].

**[!UICONTROL Convert PII to the following IDs]:** (disponible pour toutes les plateformes de données client prises en charge, à l’exception de [!DNL AdFixus]) Types d’identifiants vers lesquels vous convertirez vos informations d’identification personnelle (PII). Si vous sélectionnez plusieurs types, le segment généré est renseigné avec des valeurs pour chaque type d’identifiant sélectionné (par exemple un [!DNL RampID] et un [!DNL Unified ID2.0] pour chaque adresse e-mail). Les frais de données sont appliqués en conséquence.

Pour [!DNL RampID] et [!DNL Unified ID2.0], le fournisseur recherche chaque adresse e-mail pour voir si un ID existe déjà et traduit l’adresse en un ID correspondant le cas échéant. S’il n’existe pas d’ID pour l’adresse, un nouvel ID est créé.

>[!NOTE]
>
>Vous ne pouvez cibler qu’un seul type d’identifiant dans un seul emplacement. Pour tester les performances par type d’identifiant, [créez un emplacement distinct](/help/dsp/campaign-management/placements/placement-create.md) pour chaque type d’identifiant du segment.

* *[!DNL RampID]:* pour convertir des informations d’identification personnelles en [!DNL RampID]. Vous pouvez utiliser [!DNL RampIDs] pour recibler les utilisateurs connectés et pour mesurer les [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).

* *[!DNL Unified ID2.0]:* Pour convertir les informations d&#39;identification personnelles en un [ID unifié 2.0](https://unifiedid.com) ID pour recibler les utilisateurs connectés.

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** Conditions d’utilisation de la conversion des informations d’identification personnelles en identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les conditions une seule fois avant de pouvoir importer des identifiants, convertir des données en un nouveau type d’identifiant ou cibler un type d’identifiant. Pour les clients disposant de contrats de services gérés, l’équipe chargée du compte Adobe obtient votre consentement et accepte les conditions au nom de votre entreprise. Pour lire les termes, cliquez sur **>**. Pour accepter les conditions, faites défiler l’écran jusqu’au bas des conditions et cliquez sur **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** (Lecture seule ; générée automatiquement) Clé source que vous pouvez utiliser pour créer une connexion de destination dans la plateforme de données client pour pousser les audiences vers Advertising DSP. Vous pouvez copier la valeur dans le presse-papiers pour la coller dans les paramètres de connexion de destination ou dans un fichier. Partagez la valeur avec l’équipe qui diffusera les audiences vers DSP.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [Convertir les ID utilisateur de  [!DNL Adobe Real-Time CDP]  en ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir les ID utilisateur de  [!DNL Amperity]  en ID universels](/help/dsp/audiences/sources/source-amperity.md)
>* [Convertir les ID utilisateur de  [!DNL Optimizely]  en ID universels](/help/dsp/audiences/sources/source-optimizely.md)
>* [Convertir les ID utilisateur de  [!DNL Tealium]  en ID universels](/help/dsp/audiences/sources/source-tealium.md)
>* [Importer des segments propriétaires depuis [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
