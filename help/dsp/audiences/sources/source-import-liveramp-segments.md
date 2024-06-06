---
title: Importation manuelle de segments authentifiés depuis [!DNL LiveRamp]
description: En savoir plus sur l’activation d’audiences authentifiées par le biais de [!DNL LiveRamp].
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: 0a1555875fd18b326297475bc19fcfd6f28ea0c5
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# Importation manuelle de segments authentifiés depuis [!DNL LiveRamp]

*Fonction bêta*

Vous pouvez envoyer manuellement les messages authentifiés [!DNL LiveRamp] segments à DSP à l’aide de la fonction [!DNL LiveRamp] [!DNL Connect] tableau de bord. Vous pouvez utiliser des segments importés pour le ciblage des emplacements. Pour les segments propriétaires, les frais sont de 0,15 USD par impression de publicité display diffusée et de 0,25 USD par impression de publicité vidéo diffusée.

Le mappage et le chargement des segments pour chaque tâche d’importation peuvent prendre jusqu’à sept jours.

<!--Is this first step relevant for this process?

1. For measurement using [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md):

   1. Complete all [prerequisites for implementing [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) and make sure that the [AMO ID and EF ID](/help/integrations/analytics/ids.md) are being populated in your tracking URLs.
   
   1. [Maybe just add a param to existing tag] Deploy a second JavaScript tag for [!DNL RampIDs] on your webpages to match onsite events to ad impressions. Contact your Adobe Account Team to get the tag and instructions for where to implement it.

 -->

1. Procédez comme suit dans la section [!DNL Connect] tableau de bord :

   1. Activer la mosaïque de destination **[!DNL AAC API 1P Onboarding]**.

   1. Définir [!DNL Identifier Settings] to **[!DNL Ramp ID]** uniquement.

      ![Paramètres d’identifiant](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Facultatif) Si vous souhaitez toujours recevoir des identifiants basés sur des cookies, créez une seconde [!DNL AAC API 1P Onboarding] mosaïque de destination avec &quot;[!DNL Cookies],&quot;[!DNL IDFA],&quot; et &quot;[!DNL AAID]&quot; sélectionné.

   1. Vérifier dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le nombre de segments entier a été importé.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [Gestion des sources d’audience pour activer les audiences d’ID universelles](source-manage.md)
>* [Adobe Advertising DSP la connexion](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
