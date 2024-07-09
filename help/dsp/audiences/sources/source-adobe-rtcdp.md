---
title: Utilisation de l’intégration DSP avec [!DNL Adobe] [!DNL Real-time CDP]
description: Découvrez comment activer DSP d’ingérer votre [!DNL Adobe] [!DNL Real-time CDP] segments propriétaires.
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# Convertir les ID utilisateur à partir de [!DNL Adobe Real-Time CDP] vers des ID universels

*Fonctionnalité Beta*

Utilisation de l’intégration DSP avec [la valeur [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), qui fait partie de Adobe Experience Platform, pour convertir vos adresses électroniques hachées en identifiants universels pour la publicité ciblée.

1. (Pour convertir des adresses électroniques en [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurez le suivi pour [!DNL Analytics] mesure :

   1. (Si vous ne l’avez pas déjà fait) Complétez tous les [conditions préalables à la mise en oeuvre [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et la variable [AMO ID et EF ID dans vos URL de suivi](/help/integrations/analytics/ids.md).

   1. Inscrivez-vous auprès du partenaire d’ID universel et déployez le code spécifique à l’ID universel sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs de bureau et les navigateurs web mobiles (mais pas les applications mobiles) aux affichages publicitaires :

      * **Pour [!DNL RampIDs]:** Vous devez déployer une balise JavaScript supplémentaire sur vos pages web pour faire correspondre les conversions des identifiants sur les navigateurs de bureau et les navigateurs web mobiles (mais pas les applications mobiles) aux affichages publicitaires. Contactez votre équipe de compte d’Adobe, qui vous donnera des instructions pour vous inscrire à une [!DNL LiveRamp] [!DNL LaunchPad] de [!DNL LiveRamp] Solutions de trafic d’authentification. L&#39;inscription est gratuite, mais vous devez signer un accord. Une fois que vous vous êtes enregistré, votre équipe de compte d’Adobe génère et fournit une balise unique que votre organisation doit implémenter sur vos pages web.

1. [Création d’une source d’audience](source-manage.md) pour importer des audiences dans votre compte DSP ou un compte publicitaire. Vous pouvez choisir de convertir vos identifiants d’utilisateur en l’un des [formats d’ID universels disponibles](source-about.md).

   Les paramètres de la source comprennent une clé source générée automatiquement, que vous utiliserez à l’étape suivante.

1. Dans Adobe Experience Platform, configurez une connexion de destination Advertising DSP à l’aide de la variable [!UICONTROL Source Key] qui a été généré dans les paramètres source DSP.

   Pour obtenir des instructions sur l’activation de la connexion DSP destination, la sélection de segments et l’accès aux autorisations de contrôle, voir &quot;[Connexion Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

   Les adresses électroniques source doivent être hachées à l’aide de l’algorithme SHA-256.

1. Vérifier dans votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment renseigne et comparez le nombre d’identifiants universels au nombre d’adresses électroniques hachées d’origine.

   Les segments doivent être disponibles dans DSP dans les 24 heures. Une fois DSP les données du segment reçues, le nombre d’audiences doit être visible dans les neuf (9) heures.

   Pour plus d’informations sur les taux de traduction des identifiants acceptables et sur les raisons pour lesquelles les nombres de segments peuvent varier, voir &quot;[Écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances).&quot;

   Pour obtenir une assistance en matière de dépannage, contactez votre équipe de compte d’Adobe ou `adcloud-support@adobe.com`.

Les segments sont actualisés toutes les 24 heures. Cependant, l’inclusion dans un segment expire après 30 jours par défaut ou après une période d’expiration spécifiée par le client. Actualisez vos segments en les republiant à partir de Real-Time CDP avant l’expiration. Pour demander une expiration de segment personnalisée, contactez votre équipe de compte d’Adobe.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gestion des sources d’audience pour activer les audiences d’ID universelles](source-manage.md)
>* [Adobe Advertising DSP la connexion](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Présentation du catalogue des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
