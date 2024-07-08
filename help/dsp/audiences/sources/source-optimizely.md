---
title: Convertir les ID utilisateur de [!DNL Optimizely] en ID universels
description: Découvrez comment DSP permettre l’assimilation de segments [!DNL Optimizely] propriétaires.
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL Optimizely] en ID universels

*Fonctionnalité bêta*

Use the DSP integration with the [!DNL Optimizely] customer data platform to convert your organization&#39;s first-party hashed email addresses to universal IDs for targeted advertising.

1. (To convert email addresses to [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) [Set up tracking to enable [!DNL Analytics] measurement](#analytics-tracking).

1. [Create an audience source in DSP](#source-create).

1. [Prepare and push the segment data](#push-data).

1. [Compare the number of universal IDs with the number of hashed email addresses](#compare-id-count).

## Step 1: Set up tracking for [!DNL Analytics] measurement {#analytics-tracking}

*Les annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))*

Pour convertir des adresses e-mail en [!DNL RampIDs] ou [!DNL ID5] ID, procédez comme suit :

1. (Si vous ne l’avez pas déjà fait) Remplissez toutes les conditions préalables à la [mise en œuvre [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et assurez-vous que l’AMO ID et l’EF [ID](/help/integrations/analytics/ids.md) sont renseignés dans vos URL de suivi.

1. Enregistrez-vous auprès du partenaire Universal ID et déployez du code spécifique à l’ID universel sur vos pages Web pour faire correspondre les conversions des ID sur les navigateurs Web de bureau et mobiles (mais pas les applications mobiles) aux affichages publicitaires :

   * **Pour [!DNL RampIDs]:** vous devez déployer une balise JavaScript supplémentaire sur vos pages Web pour faire correspondre les conversions des ID sur les navigateurs Web de bureau et mobiles (mais pas les applications mobiles) aux affichages publicitaires. Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

## Step 2: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

   The source settings will include an auto-generated source key, which you&#39;ll use to push the segment data.

1. After you create the audience source, share the source code key with the [!DNL Optimizely] user.

## Etape 3 : préparer et envoyer les données de segment {#push-data}

L’annonceur doit préparer et pousser les données avec l’aide de son [!DNL Optimizely] représentant.

1. Dans [!DNL Optimizely Data Platform], hachez les ID de message électronique pour l’audience de l’annonceur à l’aide de l’algorithme SHA-256.

1. Suivez les instructions pour [[!DNL Optimizely's] pousser le segment vers DSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads). Incluez les informations suivantes pour activer l’intégration :

   * **Source Key:** This is the source key created in [Step 2](#source-create).

   * **Account Code:** This is the alphanumeric DSP Account Code, which you can find within DSP at [!UICONTROL Settings] > [!UICONTROL Account].

The segments should be available in DSP within 24 hours and are refreshed as configured for the advertiser. Regardless of how frequently the segment is refreshed, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from [!DNL Optimizely] prior to the expiration. To request a custom segment expiration, contact your Adobe Account Team.

## Step 4: Compare the number of universal IDs with the number of hashed email addresses {#compare-id-count}

Une fois toutes les étapes terminées, vérifiez dans votre bibliothèque d’audiences (qui est disponible lorsque vous créez ou modifiez une audience à partir d&#39;> [!UICONTROL All Audiences] ou dans les paramètres de [!UICONTROL Audiences] placement) que le segment est disponible et se remplit dans les 24 heures. Compare the number of universal IDs with the number of original hashed email addresses.

Le taux de traduction des adresses e-mail hachées en ID universels doit être supérieur à 90%. Par exemple, si vous envoyez 100 adresses e-mail hachées à partir de votre plateforme de données client, elles doivent être traduites en plus de 90 identifiants universels. Un taux de traduction de 90 % ou moins pose problème. Pour plus d’informations sur la façon dont le nombre de segments peut varier, voir «[ Causes des écarts de données entre les ID de messagerie et les ID universels](#universal-ids-data-variances) ».

Pour obtenir de l’aide en matière de dépannage, contactez votre équipe de compte Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Manage Audience Sources to Activate Universal ID Audiences](source-manage.md)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [About Audience Management](/help/dsp/audiences/audience-about.md)
