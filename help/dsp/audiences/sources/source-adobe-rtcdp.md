---
title: Utilisation de l’intégration de DSP avec  [!DNL Adobe] [!DNL Real-time CDP]
description: Découvrez comment activer DSP pour ingérer vos segments propriétaires [!DNL Adobe] [!DNL Real-time CDP]
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: cff6b5ad2c66699a6e0402bce6685acc536fd0a0
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# Convertir les ID utilisateur de [!DNL Adobe Real-Time CDP] en ID universels

*Fonction Beta*

Utilisez l’intégration de DSP à [the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), qui fait partie de Adobe Experience Platform, pour convertir vos adresses e-mail hachées en identifiants universels pour la publicité ciblée.

1. (Pour convertir des adresses e-mail en [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> ; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurez le suivi pour la mesure des [!DNL Analytics] :

   1. (Si vous ne l’avez pas déjà fait) Remplissez toutes les [conditions préalables à l’implémentation [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) ainsi que l’[AMO ID et l’EF ID dans vos URL de tracking](/help/integrations/analytics/ids.md).

   1. Enregistrez-vous auprès du partenaire d’ID universel et déployez du code spécifique à l’ID universel sur vos pages web pour faire correspondre les conversions des ID sur les navigateurs web de bureau et mobiles (mais pas sur les applications mobiles) aux affichages publicitaires :

      * **Par [!DNL RampIDs] :** vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants des navigateurs web de bureau et mobiles (mais pas des applications mobiles) aux affichages publicitaires. Contactez l’équipe chargée de votre compte Adobe qui vous donnera les instructions nécessaires pour vous inscrire à une balise [!DNL LiveRamp] [!DNL LaunchPad] auprès de [!DNL LiveRamp] solutions de trafic d’authentification. L&#39;inscription est gratuite, mais vous devez signer un contrat. Une fois enregistré, votre équipe de compte Adobe génère et fournit une balise unique que votre organisation peut implémenter sur vos pages web.

1. [Créez une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte d’annonceur. Vous pouvez choisir de convertir vos identifiants d’utilisateur vers l’un des [formats d’ID universels disponibles](source-about.md).

   Les paramètres source incluent une clé source générée automatiquement, que vous utiliserez à l’étape suivante.

1. Dans Adobe Experience Platform, configurez une connexion de destination Advertising DSP à l’aide de la [!UICONTROL Source Key] générée dans les paramètres source DSP.

   Pour obtenir des instructions sur l’activation de la connexion de destination DSP, la sélection de segments et l’accès aux autorisations de contrôle, voir « [Connexion DSP Adobe Advertising Cloud](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html) ».

   Les adresses e-mail sources doivent être hachées à l’aide de l’algorithme SHA-256.

1. Vérifiez dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est renseigné et comparez le nombre d’identifiants universels avec le nombre d’adresses e-mail hachées d’origine.

   Les segments doivent être disponibles dans DSP dans les 24 heures. Une fois que DSP a reçu les données de segment, le nombre de profils des audiences doit être visible dans les neuf (9) heures. Pour plus d’informations sur les taux de traduction des identifiants acceptables et sur les raisons pour lesquelles le nombre de segments peut varier, voir « [Variances des données entre les ID d’e-mail et les ID universels](#universal-ids-data-variances) ».

Les segments sont actualisés toutes les 24 heures. Cependant, l’inclusion dans un segment expire après 30 jours par défaut ou après une période d’expiration spécifiée par le client ou la cliente. Actualisez vos segments en les poussant à nouveau depuis Real-Time CDP avant l’expiration. Pour demander une expiration de segment personnalisé, contactez l’équipe chargée de votre compte Adobe.

## Dépannage

Pour résoudre les problèmes de taux de traduction et de nombre d’utilisateurs, consultez « [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md) ».

Pour résoudre les problèmes liés à la procédure de conversion, contactez l’équipe ou l’`adcloud-support@adobe.com` de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](source-manage.md)
>* [Connexion Adobe Advertising DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Présentation du catalogue des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
