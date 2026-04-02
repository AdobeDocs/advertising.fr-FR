---
title: Importez manuellement des segments authentifiés depuis  [!DNL LiveRamp]
description: Découvrez comment activer les audiences authentifiées via  [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
TQID: https://experienceleague.adobe.com/ln4e1Jmq7vRhOIeg25UwNR8yToni5CuokxAcmEPMwEQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 152
ht-degree: 0%

---

# Importer manuellement des segments authentifiés depuis [!DNL LiveRamp]

*Fonction*

Vous pouvez envoyer manuellement des segments de [!DNL LiveRamp] authentifiés à DSP à l’aide du tableau de bord [!DNL LiveRamp] [!DNL Connect]. Vous pouvez utiliser des segments importés pour le ciblage de l’emplacement. Pour les segments propriétaires, les frais sont de 0,15 USD par impression d’annonce publicitaire diffusée et de 0,25 USD par impression d’annonce vidéo diffusée.

Le mappage de segments et le chargement pour chaque tâche d’importation peuvent prendre jusqu’à sept jours.

<!--
Is this first step relevant for this process?

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
>* [Connexion &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
