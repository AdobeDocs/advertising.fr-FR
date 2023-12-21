---
title: Activation des segments authentifiés à partir des partenaires d’ID universel
description: Découvrez comment activer des audiences authentifiées par le biais d’une solution d’ID universelle.
feature: DSP Audiences
exl-id: c56a54c7-5300-4cda-96d0-82d86e76ee39
source-git-commit: e9ff454428d0256402a2ef2fa74f8bd45bd7592f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Activation des segments authentifiés à partir des partenaires d’ID universel

Pour activer les audiences authentifiées par le biais d’une solution d’ID universelle dans Advertising DSP, vos segments doivent être traduits en [!DNL RampIDs], qui sont reconnaissables dans un environnement admissible. Pour ce faire, vous pouvez :

* Utilisation de l’intégration DSP avec la [!DNL Adobe Real-Time Customer Data Platform (CDP)] et la variable [!DNL Adobe-LiveRamp Retrieval API].

* Envoi manuel de segments authentifiés à DSP à partir du [!DNL LiveRamp] [!DNL Connect] tableau de bord.

## Tâche

1. Pour chaque option, contactez `adcloud-support@adobe.com` pour activer les paramètres suivants dans DSP, ce qui vous permettra de cibler les segments authentifiés dans DSP campagnes une seule fois. [toutes les étapes du workflow d’activation sont terminées.](source-adobe-rtcdp.md):

   1. [!DNL LiveRamp] [!DNL RampID] configuration de campagne avant le partage de segments à partir de [!DNL Real-Time CDP].

   1. Au niveau du compte &quot;[!UICONTROL LiveRamp segments]&quot;.

1. (Utilisateurs partageant manuellement des segments authentifiés depuis [!DNL LiveRamp]) Effectuez les étapes suivantes dans la section [!DNL LiveRamp] [!DNL Connect] tableau de bord :

   1. Activer la mosaïque de destination **[!DNL AAC API 1P Onboarding]**.

   1. Définir [!DNL Identifier Settings] to **[!DNL Ramp ID]** uniquement.

      ![Paramètres d’identifiant](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Facultatif) Si vous souhaitez toujours recevoir des identifiants basés sur des cookies, créez une seconde [!DNL AAC API 1P Onboarding] mosaïque de destination avec &quot;[!DNL Cookies],&quot;[!DNL IDFA],&quot; et &quot;[!DNL AAID]&quot; sélectionné.

## Bonnes pratiques relatives aux tests et à la validation des données

* **Cible [!DNL RampID]segments basés sur des cookies et segments basés sur des cookies dans des campagnes distinctes.**

   * Les paramètres de Campaign ne permettent de prioriser qu’un seul identifiant.

   * Actuellement, [!DNL RampIDs] ne peuvent pas être récupérés pendant les événements sur site. Cela signifie que certains objectifs personnalisés, tels que le CPA le plus bas et le RSDP, ne sont pas disponibles avec l’utilisation de segments authentifiés. Utilisez les segments basés sur des cookies uniquement si vous disposez d’un IPC de performances restrictif.

* **Créez un emplacement dans les deux [!DNL RampID] et des campagnes basées sur des cookies.**

   * Ciblage des segments partagés à partir de [!DNL LiveRamp] en utilisant le processus d’activation du segment standard.

   * Collaborez avec votre équipe d’assistance Adobe Advertising pour valider la distribution correcte des données.

Pour en savoir plus sur l’intégration DSP avec [!DNL LiveRamp], contactez `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [À propos de l’activation de segments authentifiés à partir des sources d’audience](source-about.md)
>* [Création d’une source d’audience pour activer les audiences propriétaires](source-create.md)
>* [Paramètres de la source d’audience](source-settings.md)
>* [Adobe Advertising DSP la connexion](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
