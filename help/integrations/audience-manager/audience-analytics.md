---
title: '[!DNL Adobe] [!DNL Audience Analytics] pour les clients Adobes Advertising'
description: Découvrez comment utiliser [!DNL Adobe] [!DNL Audience Analytics] pour des cas d’utilisation publicitaire
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] pour les clients Adobes Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=fr) est une intégration entre Adobe Audience Manager et Adobe Analytics qui permet aux clients d’Audience Manager d’envoyer des segments à [!DNL Analytics] pour obtenir des informations enrichies sur l’activité du site.

Les clients Adobe Advertising peuvent en bénéficier en utilisant [!DNL Audience Analytics]. L’intégration vous permet d’effectuer les opérations suivantes :

* Envoyez directement des données d’exposition à l’Adobe Advertising à [!DNL Analytics] pour déterminer l’impact de l’activité d’entonnoir supérieur sur l’activité du site en aval.

* Déterminez les canaux marketing et les points d’entrée du site à partir des publicités haut de l’entonnoir.

* Associez l’intégration à [!DNL Analytics for Advertising] pour incorporer des segments démographiques tiers de [l’Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html?lang=fr) avec des données [!DNL Analytics for Advertising] pour obtenir plus d’informations sur les profils utilisateur.

  [!DNL Audience Marketplace] donne accès aux flux de données tiers avec des modèles d’abonnement &quot;Activation&quot;, qui permettent aux acheteurs d’envoyer des données vers une destination. Si les données sont utilisées dans une destination [!DNL Analytics], les frais d’activation ne sont pas appliqués.

* (Publicitaires avec Advertising DSP) Ajoutez des segments d’exposition supplémentaires pour obtenir des informations de gestion de parcours globale.

  Advertising DSP peut envoyer des données d’exposition à l’Audience Manager sous forme de signaux exploitables par le biais de l’implémentation de Adobe Experience Platform ou des pixels de suivi des impressions de l’Audience Manager. Le transfert des mêmes données vers [!DNL Analytics] permet une analyse avancée des données. Pour plus d’informations, voir &quot;[Présentation de l’intégration des données multimédia Adobe Advertising avec Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

Pour plus d’informations sur [!DNL Audience Analytics], y compris ses conditions préalables et son workflow, voir &quot;[Audience Analytics overview](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=fr)&quot;.

## Exemples d&#39;utilisation des données [!DNL Audience Analytics] avec des données d&#39;Adobe Advertising

Vous trouverez ci-dessous des exemples d’utilisation des données combinées dans [!DNL Analytics] [!DNL Analysis Workspace].

### Afficher l’impact de l’activité Entonnoir supérieur sur l’activité en aval

Utilisez les segments d’exposition à l’Audience Manager pour voir l’impact de l’activité du site entonnoir supérieur sur l’activité du site en aval. Incluez des identifiants de macro tiers ou d’Adobe Advertising dans vos pixels de suivi pour suivre l’impact à un niveau détaillé, du niveau de la campagne au niveau du site sur lequel l’utilisateur a été exposé.

Principaux avantages :

* Effectuez le suivi de l’exposition par type d’entonnoir/de publicité et utilisez [!DNL Audience Analytics] pour déterminer les taux d’entrée et le chevauchement avec la phase suivante du parcours client.

* Déterminez l’impact de l’activité d’entonnoir supérieur sur l’activité de site en aval.

* Connectez les données [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> et [!DNL Audience Analytics] <!-- (which includes the user's last exposure event) --> pour déterminer un parcours holistique au site.

Vous trouverez ci-dessous des exemples de rapports que vous pouvez créer dans [!DNL Analysis Workspace].

![Voir l&#39;impact de l&#39;activité entonnoir supérieur sur l&#39;activité du site en aval](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Utilisation de [!DNL Audience Analytics] données de segment tierces pour l’analyse du profil utilisateur

Utilisez des segments d’Audience Manager tiers pour une analyse plus approfondie de la manière dont les utilisateurs interagissent avec votre site. Vous pouvez utiliser ces informations pour déterminer les nouvelles audiences tierces pour lesquelles activer les médias, en fonction de la manière dont les profils des segments tiers interagissent avec les indicateurs de performances clés des sites des campagnes multimédia.

>[!TIP]
> Utilisez les dimensions `Audiences ID` et `Audiences Name` de l&#39;Audience Manager dans [!DNL Analytics], comme toute autre dimension collectée par [!DNL Analytics].

Vous trouverez ci-dessous des exemples de rapports que vous pouvez créer dans [!DNL Analysis Workspace].

![Utilisation de segments tiers pour enrichir l’analyse de profil utilisateur](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Advertising des intégrations avec Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
