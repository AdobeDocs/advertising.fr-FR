---
title: "Convertir les ID utilisateur de [!DNL ActionIQ] en ID universels"
description: '"Découvrez comment activer DSP d’ingérer vos  [!DNL ActionIQ] segments propriétaires".'
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL ActionIQ] en ID universels

*Fonctionnalité Beta*

Utilisez l’intégration DSP à la plateforme de données client [!DNL ActionIQ] pour convertir vos adresses électroniques hachées en identifiants universels pour la publicité ciblée.

Il existe <!-- NN --> étapes pour partager des données de [!DNL ActionIQ] avec DSP :

1. [Créez une source d’audience dans DSP](#source-create).

1. ?

## Étape 1 : création d’une source d’audience dans DSP {#source-create}

1. [Créez une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire, en spécifiant les [formats d’ID universels](source-about.md) vers lesquels vous souhaitez convertir vos identifiants utilisateur.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec l’utilisateur [!DNL ActionIQ].

## Étape 2 :

## Étape 3 :

1. Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est renseigné et comparez le nombre d’identifiants universels au nombre d’adresses électroniques hachées d’origine.

   Les segments doivent être disponibles dans DSP dans les 24 heures. Une fois DSP les données du segment reçues, le nombre d’audiences doit être visible dans les neuf (9) heures. Pour plus d’informations sur les taux de traduction des ID acceptables et sur les raisons pour lesquelles les nombres de segments peuvent varier, voir &quot;[Écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances)&quot;.

Les segments sont actualisés toutes les 24 heures.

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, voir &quot;[Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)&quot;.

Pour résoudre les problèmes liés à la procédure de conversion, contactez votre équipe de compte d’Adobe ou `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universels](source-manage.md)
>* [Convertir les ID utilisateur de [!DNL Adobe Real-Time CDP]  en ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir les ID utilisateur de [!DNL Tealium]  en ID universels](/help/dsp/audiences/sources/source-tealium.md)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)
