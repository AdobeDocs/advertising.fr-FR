---
title: '[!DNL Adobe] [!DNL Audience Analytics] pour les clients Adobe Advertising'
description: Découvrez comment utiliser  [!DNL Adobe] [!DNL Audience Analytics] pour les cas d’utilisation publicitaire.
feature: Integration with Adobe Audience Manager
exl-id: 457d4335-2762-4aab-94b8-12f8a79d109b
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] pour les clients Adobe Advertising

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) est une intégration entre Adobe Audience Manager et Adobe Analytics qui permet aux clients Audience Manager d’envoyer des segments à [!DNL Analytics] pour obtenir des informations enrichies sur l’activité du site.

Les clients Adobe Advertising peuvent tirer parti de l’utilisation de [!DNL Audience Analytics]. L’intégration vous permet d’effectuer les opérations suivantes :

* Envoyez les données d’exposition d’Adobe Advertising directement à [!DNL Analytics] pour déterminer l’impact de l’activité de funnel supérieure sur l’activité du site en aval.

* Déterminez les canaux marketing et les points d’entrée de site à partir des publicités de risque de funnel supérieur.

* Superposez l’intégration à [!DNL Analytics for Advertising] pour incorporer des segments démographiques tiers provenant de [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) avec des données [!DNL Analytics for Advertising] pour obtenir plus d’informations sur les profils utilisateur.

  [!DNL Audience Marketplace] permet d’accéder à des flux de données tiers avec des modèles d’abonnement « Activation », qui permettent aux acheteurs d’envoyer des données vers une destination. Si les données sont utilisées dans une destination [!DNL Analytics], les frais d’activation ne sont pas appliqués.

* (Annonceurs avec Advertising DSP) Ajoutez des segments d’exposition supplémentaires pour obtenir des informations holistiques sur la gestion des parcours.

  Advertising DSP peut envoyer des données d’exposition à Audience Manager sous forme de signaux exploitables par le biais de l’implémentation de pixels de suivi d’impression Adobe Experience Platform ou Audience Manager. Le transfert des mêmes données vers [!DNL Analytics] permet une analyse avancée des données. Pour plus d’informations, consultez « [Présentation de l’envoi de données d’exposition aux médias DSP vers Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md) ».

Pour plus d’informations sur [!DNL Audience Analytics], y compris sur ses conditions préalables et son workflow, consultez la section « [Présentation d’Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) ».

## Exemples d’utilisation des données [!DNL Audience Analytics] avec les données Adobe Advertising

Vous trouverez ci-dessous des exemples d’utilisation des données combinées dans [!DNL Analytics] [!DNL Analysis Workspace].

### Examiner l’impact de l’activité des funnel supérieures sur l’activité en aval

Utilisez les segments d’exposition Audience Manager pour voir l’impact de l’activité du site funnel supérieur sur l’activité du site en aval. Incluez des identifiants de macro Adobe Advertising ou tiers dans vos pixels de suivi pour suivre l’impact à un niveau détaillé, du niveau de la campagne au niveau du site sur lequel l’utilisateur a été exposé.

Principaux avantages :

* Suivez l’exposition par type de funnel/publicité et utilisez [!DNL Audience Analytics] pour déterminer les taux d’entrée et le chevauchement avec la phase suivante du parcours client.

* Déterminez l’impact de l’activité du funnel supérieur sur l’activité du site en aval.

* Connectez les données [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> et [!DNL Audience Analytics] pour déterminer un parcours holistique au site.

<!-- (which includes the user's last exposure event) -->

Vous trouverez ci-dessous des exemples de rapports que vous pouvez créer dans [!DNL Analysis Workspace].

![Voir l’impact de l’activité du funnel supérieur sur l’activité du site en aval](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Utiliser [!DNL Audience Analytics] données de segments tiers pour l’analyse des profils d’utilisateurs

Utilisez des segments Audience Manager tiers pour une analyse plus riche de la manière dont les utilisateurs interagissent avec votre site. Vous pouvez utiliser les informations pour déterminer de nouvelles audiences tierces pour lesquelles activer des médias, en fonction de la manière dont les profils des segments tiers interagissent avec les indicateurs clés de performance des sites des campagnes multimédia.

>[!TIP]
> Utilisez les dimensions `Audiences ID` et `Audiences Name` d’Audience Manager dans [!DNL Analytics], comme toutes les autres dimensions collectées par [!DNL Analytics].

Vous trouverez ci-dessous des exemples de rapports que vous pouvez créer dans [!DNL Analysis Workspace].

![Utilisation de segments tiers pour enrichir l’analyse des profils utilisateur](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Intégrations Adobe Advertising avec Adobe Audience Manager](/help/integrations/audience-manager/overview.md)
