---
title: "Convertir les ID utilisateur à partir de [!DNL ActionIQ] à des ID universels"
description: "Découvrez comment activer DSP d’ingérer votre [!DNL ActionIQ] segments propriétaires."
feature: DSP Audiences
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Convertir les ID utilisateur à partir de [!DNL ActionIQ] vers des ID universels

*Fonctionnalité Beta*

Utilisez l’intégration DSP avec la [!DNL ActionIQ] plateforme de données client pour convertir vos adresses électroniques hachées en identifiants universels pour la publicité ciblée.

Il y a <!-- NN --> étapes de partage de données depuis [!DNL ActionIQ] avec DSP :

1. [Création d’une source d’audience dans DSP](#source-create).

1. ?

## Étape 1 : création d’une source d’audience dans DSP {#source-create}

1. [Création d’une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire, en spécifiant la variable [formats d’ID universels](source-about.md) dans lequel vous souhaitez convertir vos identifiants utilisateur.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec la variable [!DNL ActionIQ] utilisateur.

1. 
   <!-- ActionIQ-specific step(s) -->

1. Vérifier dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment renseigne et comparez le nombre d’identifiants universels au nombre d’adresses électroniques hachées d’origine.

   Les segments doivent être disponibles dans DSP dans les 24 heures. Une fois DSP les données du segment reçues, le nombre d’audiences doit être visible dans les neuf (9) heures.

   Pour plus d’informations sur les taux de traduction des identifiants acceptables et sur les raisons pour lesquelles les nombres de segments peuvent varier, voir &quot;[Écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances).&quot;

   Pour obtenir une assistance en matière de dépannage, contactez votre équipe de compte d’Adobe ou `adcloud-support@adobe.com`.

Les segments sont actualisés toutes les 24 heures.

## Étape 2 :

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gestion des sources d’audience pour activer les audiences d’ID universelles](source-manage.md)
>* [Convertir les ID utilisateur à partir de [!DNL Adobe Real-Time CDP] vers des ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir les ID utilisateur à partir de [!DNL Tealium] vers des ID universels](/help/dsp/audiences/sources/source-tealium.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
