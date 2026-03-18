---
title: Cas d’utilisation
description: Découvrez les cas pratiques de partage de vos données multimédia Advertising DSP avec Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Cas pratiques de capture de données d’exposition aux médias dans Adobe Audience Manager

*Annonceurs avec Advertising DSP uniquement*

*Publicitaires avec une intégration Adobe Advertising-Adobe Audience Manager uniquement*

Vous trouverez ci-dessous quelques avantages liés à la capture de vos <!-- ad impression data? --> de données d’exposition aux médias Advertising DSP dans Audience Manager.

## Gestion des récences et des fréquences

La capture de données d’impression dans Audience Manager vous permet d’améliorer la gestion de votre fréquence en créant des segments d’utilisateurs qui ont été exposés à une publicité ou une campagne particulière. Vous pouvez utiliser ces segments pour le ciblage des annonces si vous souhaitez augmenter la fréquence ou pour la suppression des annonces si vous souhaitez limiter la fréquence.

En outre, avec Audience Manager [!DNL Segment Builder], vous pouvez appliquer des contrôles [récence et fréquence](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html?lang=fr) à toutes les caractéristiques [basées sur des règles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=fr) qui contiennent des signaux exploitables. Vous pouvez ainsi, par exemple, limiter le nombre de fois qu’une création particulière est présentée à un utilisateur ou une utilisatrice dans une campagne multimédia. Lisez « [Suppression instantanée sur plusieurs appareils](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html?lang=fr) » pour savoir comment procéder.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Messagerie séquentielle

En capturant les données d’impression, vous pouvez créer un segment d’utilisateurs qui ont été exposés à une campagne ou à une publicité et utiliser ce segment pour la messagerie séquentielle ou la suppression. Par exemple, vous pouvez recibler les utilisateurs qui ont consulté les `123` de contenu créatif, mais qui n’ont pas cliqué ni effectué de conversion en leur présentant des `456` de contenu créatif.

Pour exécuter cet exemple dans Audience Manager, procédez comme suit :<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Créez une caractéristique pour capturer les utilisateurs qui ont vu le contenu créatif.

   Par exemple, pour nommer la caractéristique `Creative Trait 123`, utilisez la règle de caractéristique suivante :

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Créez une caractéristique pour capturer les utilisateurs qui cliquent ou effectuent une conversion.

   Par exemple, pour nommer cette caractéristique `Click and Converter`, utilisez la règle de caractéristique suivante :

   ```
   d_event == click OR d_event=conv
   ```

1. Créez un segment appelé `Retarget Users` pour renseigner les utilisateurs qui ont vu des `123` créatifs mais n’ont pas cliqué ni effectué de conversion. Utilisez la règle de caractéristique suivante :

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Mappez le segment `Retarget Users` à une destination et ciblez les utilisateurs de la destination avec des `456` créatifs.

## [!DNL Adobe Audience Analytics] et données d’exposition de campagne

Une fois que les données d’impression et de clic de campagne sont disponibles dans Audience Manager, vous pouvez créer des caractéristiques et des segments d’utilisateurs et d’utilisatrices qui ont été exposés à une campagne ou une tactique particulière ou qui ont interagi avec elle. Avec une [[!DNL Audience Analytics] intégration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=fr), vos segments Audience Manager peuvent être synchronisés avec [!DNL Analytics] pour une analyse plus approfondie. Les cas d’utilisation potentiels sont les suivants :

* **Analyse des interactions entre DSP et les publicités [!DNL Advertising Search, Social, & Commerce] :** la norme [[!DNL Analytics for Advertising] intégration](/help/integrations/analytics/overview.md) ne fournit pas d’informations sur l’interaction entre DSP et [!DNL Search, Social, & Commerce], car les deux canaux utilisent des AMO ID qui suivent les règles d’attribution des AMO ID, pour lesquelles un clic de recherche remplace une vue d’affichage. En créant un segment d’exposition DSP dans Audience Manager, vous pouvez utiliser [!DNL Audience Analytics] pour analyser l’interaction entre DSP et les publicités [!DNL Search, Social, & Commerce] dans [!DNL Analytics].

* **Analyse des fréquences :** vous pouvez créer des segments dans Audience Manager en fonction du nombre de fois où un utilisateur ou une utilisatrice a été exposé(e) à une annonce ou une campagne spécifique. Vous pouvez ensuite analyser les différents segments d’exposition dans Analytics pour voir comment le comportement des utilisateurs change en fonction du nombre d’expositions à DSP.

## [!DNL Audience Optimization Reports]

Vous pouvez tirer parti de [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html?lang=fr) pour identifier les opportunités de performances potentielles pour les segments de vos campagnes. Ces rapports combinent les données d’impression, de clic et de conversion de la campagne avec les mesures de segment afin d’informer les optimisations centrées sur les segments et un mix de canaux efficace.

### Types de rapports Audience Optimization pertinents

| Rapport | Description |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html?lang=fr) | Compare les segments mappés et non mappés par impressions et taux de conversion. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Reports]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Affichez des données sur les impressions, les taux de clics publicitaires et les conversions pour un large éventail de dimensions publicitaires. |
| [[!UICONTROL Optimal Frequency] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html?lang=fr) | Permet de trouver l’équilibre optimal entre le nombre d’impressions et de conversions diffusées. Il permet d’ajuster le nombre d’impressions à afficher avant de commencer à voir des retours décroissants. |
| [[!UICONTROL Unique User Reach] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html?lang=fr) | Un graphique à bulles, dans lequel chaque bulle est dimensionnée en proportion directe du nombre d’utilisateurs uniques pour la dimension sélectionnée. |

### Considérations

* Si [!DNL Audience Optimization Reports] utilisateurs disposent de contrôles d’accès basés sur les rôles (RBAC), [!DNL Adobe Customer Care] devez configurer un mappage entre l’ID publicitaire et le code d’intégration de source de données Audience Manager de l’organisation. Les utilisateurs administrateurs peuvent ensuite fournir des droits RBAC à différents utilisateurs.

* Les rapports de conversion dans [!DNL Audience Optimization Reports] nécessitent une configuration par l’utilisateur final. Les utilisateurs doivent renseigner les fichiers de métadonnées.

* [!DNL Audience Optimization Reports] ne prend pas en charge les modifications apportées aux métadonnées de campagne (telles que le nom de la campagne ou le nom de l&#39;emplacement).

* Les clics sur les annonces de recherche ne sont inclus dans [!DNL Audience Optimization Reports] que lorsqu’ils sont corrélés aux impressions. En d’autres termes, les clics sur les recherches sont traités comme des conversions suite à des impressions. Par conséquent, de nombreux clics de recherche peuvent ne pas être inclus dans [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Présentation de l’envoi de données d’exposition aux médias DSP vers Adobe Audience Manager](overview.md)
>* [Collectez les données de clics et d’impressions des campagnes Advertising DSP](collect.md)
