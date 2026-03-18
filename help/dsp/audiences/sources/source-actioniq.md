---
title: Convertir les ID utilisateur de  [!DNL ActionIQ]  en ID universels
description: Découvrez comment activer DSP pour ingérer vos segments  [!DNL ActionIQ] .
feature: DSP Audiences
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL ActionIQ] en ID universels

*Fonction Beta*

Utilisez l’intégration de DSP à la plateforme de données clients [!DNL ActionIQ] pour convertir vos adresses e-mail hachées en identifiants universels pour la publicité ciblée.

Il existe <!-- NN --> étapes pour partager des données de [!DNL ActionIQ] avec DSP :

1. [Créer une source d’audience dans DSP](#source-create).

1. ?

## Étape 1 : créer une source d’audience dans DSP {#source-create}

1. [Créez une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte d’annonceur, en spécifiant les [formats d’ID universels](source-about.md) vers lesquels vous souhaitez convertir vos identifiants d’utilisateur.

1. Après avoir créé la source de l’audience, partagez la clé de code source avec l’utilisateur [!DNL ActionIQ].

## Étape 2 :

## Étape 3 :

1. Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est renseigné et comparez le nombre d’identifiants universels avec le nombre d’adresses e-mail hachées d’origine.

   Les segments doivent être disponibles dans DSP dans les 24 heures. Une fois que DSP a reçu les données de segment, le nombre de profils des audiences doit être visible dans les neuf (9) heures. Pour plus d’informations sur les taux de traduction des identifiants acceptables et sur les raisons pour lesquelles le nombre de segments peut varier, voir « [Variances de données entre les ID d’e-mail et les ID universels](#universal-ids-data-variances) ».

Les segments sont actualisés toutes les 24 heures.

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, consultez « [&#x200B; Prise en charge de l’activation des identifiants universels &#x200B;](/help/dsp/audiences/universal-ids.md) ».

Pour résoudre les problèmes liés à la procédure de conversion, contactez l’équipe ou l’`adcloud-support@adobe.com` de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À Propos Des Sources D’Audience Propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences Universal ID](source-manage.md)
>* [Convertir les ID utilisateur de  [!DNL Adobe Real-Time CDP]  en ID universels](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Convertir les ID utilisateur de  [!DNL Tealium]  en ID universels](/help/dsp/audiences/sources/source-tealium.md)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)
