---
title: Importez manuellement des segments authentifiés depuis  [!DNL LiveRamp]
description: Découvrez comment activer les audiences authentifiées via  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: cff6b5ad2c66699a6e0402bce6685acc536fd0a0
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Importer manuellement des segments authentifiés depuis [!DNL LiveRamp]

*Fonction Beta*

Vous pouvez envoyer manuellement des segments de [!DNL LiveRamp] authentifiés à DSP à l’aide du tableau de bord [!DNL LiveRamp] [!DNL Connect]. Vous pouvez utiliser des segments importés pour le ciblage de l’emplacement. Pour les segments propriétaires, les frais sont de 0,15 USD par impression d’annonce publicitaire diffusée et de 0,25 USD par impression d’annonce vidéo diffusée.

Le mappage de segments et le chargement pour chaque tâche d’importation peuvent prendre jusqu’à sept jours.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Procédez comme suit dans le tableau de bord [!DNL Connect] :

   1. Activez la mosaïque de destination **[!DNL AAC API 1P Onboarding]**.

   1. Définissez [!DNL Identifier Settings] sur **[!DNL Ramp ID]** uniquement.

      ![Paramètres des identifiants](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Facultatif) Si vous souhaitez toujours recevoir des identifiants basés sur des cookies, créez une deuxième mosaïque de destination [!DNL AAC API 1P Onboarding] avec « [!DNL Cookies] », « [!DNL IDFA] » et « [!DNL AAID] » sélectionnés.

   1. Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le nombre de segments complet a été importé.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](source-manage.md)
>* [Connexion Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
