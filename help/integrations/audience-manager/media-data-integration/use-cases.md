---
title: Cas d’utilisation
description: En savoir plus sur les cas d’utilisation pour le partage de vos données multimédia Advertising DSP avec Audience Manager
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Cas d’utilisation de la capture de données d’exposition aux médias dans Adobe Audience Manager

*Annonceurs avec Advertising DSP uniquement*

*Annonceurs avec une intégration Adobe Advertising-Adobe Audience Manager uniquement*

Vous trouverez ci-dessous quelques façons de tirer parti de la capture de vos données d’exposition multimédia Advertising DSP <!-- ad impression data? --> en Audience Manager.

## Gestion de la récence et des fréquences

La capture des données d’impression dans Audience Manager vous permet d’améliorer votre gestion des fréquences en créant des segments d’utilisateurs qui ont été exposés à une publicité ou à une campagne spécifique. Vous pouvez utiliser ces segments pour le ciblage des publicités si vous souhaitez augmenter la fréquence ou pour la suppression des publicités si vous souhaitez limiter la fréquence.

En outre, avec l&#39;Audience Manager [!DNL Segment Builder], vous pouvez appliquer des [contrôles de récence et de fréquence](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) à toute [ caractéristiques basées sur des règles ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) qui contiennent des signaux exploitables. Cela vous permet, par exemple, de limiter le nombre de fois où un utilisateur voit apparaître un élément créatif particulier dans une campagne multimédia. Lisez &quot;[Suppression instantanée inter-périphérique](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot; pour apprendre à le faire.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Messagerie séquentielle

En capturant les données d’impression, vous pouvez créer un segment d’utilisateurs qui ont été exposés à une campagne ou à une publicité et utiliser ce segment pour la messagerie ou la suppression séquentielle. Par exemple, vous pouvez recibler les utilisateurs qui ont vu les créatifs `123` mais qui n’ont pas cliqué ni converti en leur affichant des créatifs `456`.

Pour exécuter cet exemple en Audience Manager, procédez comme suit :<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Créez une caractéristique pour capturer les utilisateurs qui ont vu le contenu créatif.

   Par exemple, pour nommer la caractéristique `Creative Trait 123`, utilisez la règle de caractéristique suivante :

   ```
   d_creative == 123 AND d_event == imp
   ```

1. Créez une caractéristique pour capturer les utilisateurs qui cliquent ou convertissent.

   Par exemple, pour nommer cette caractéristique `Click and Converter`, utilisez la règle de caractéristique suivante :

   ```
   d_event == click OR d_event=conv
   ```

1. Créez un segment appelé `Retarget Users` à remplir avec les utilisateurs qui ont vu les éléments créatifs `123` mais n’ont pas cliqué ni converti. Utilisez la règle de caractéristique suivante :

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. Faites correspondre le segment `Retarget Users` à une destination et ciblez les utilisateurs de la destination avec l’élément créatif `456`.

## [!DNL Adobe Audience Analytics] et données d’exposition Campaign

Une fois que les données d’impression et de clic de campagne sont disponibles dans Audience Manager, vous pouvez créer des caractéristiques et des segments d’utilisateurs qui ont été exposés à une campagne ou à une tactique spécifique ou ont interagi avec celle-ci. Avec une [[!DNL Audience Analytics] intégration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), vos segments d’Audience Manager peuvent être synchronisés avec [!DNL Analytics] pour une analyse plus approfondie. Les cas d’utilisation potentiels sont les suivants :

* **Analyse de l’interaction entre DSP et [!DNL Advertising Search, Social, & Commerce] publicités :** L’ [[!DNL Analytics for Advertising] intégration](/help/integrations/analytics/overview.md) standard ne fournit pas d’informations sur l’interaction entre DSP et [!DNL Search, Social, & Commerce], car les deux canaux utilisent des AMO ID qui suivent les règles d’attribution AMO ID, pour lesquels un clic de recherche remplace un affichage publicitaire. En créant un segment d&#39;exposition DSP dans Audience Manager, vous pouvez utiliser [!DNL Audience Analytics] pour analyser l&#39;interaction entre DSP et [!DNL Search, Social, & Commerce] publicités dans [!DNL Analytics].

* **Analyse de la fréquence :** Vous pouvez créer des segments en Audience Manager en fonction du nombre de fois où un utilisateur a été exposé à une publicité ou une campagne spécifique. Vous pouvez ensuite analyser les différents segments d’exposition dans Analytics afin de voir comment le comportement des utilisateurs change en fonction du nombre d’expositions DSP.

## [!DNL Audience Optimization Reports]

Vous pouvez tirer parti de [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) pour identifier les opportunités de performances potentielles pour les segments dans vos campagnes. Ces rapports combinent les données d’impression, de clics et de conversion de campagnes avec des mesures de segments afin d’informer les optimisations centrées sur les segments et d’offrir une combinaison efficace de canaux.

### Types de rapports d’Audience Optimization pertinents

| Rapport | Description |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Compare les segments mappés et non mappés en fonction des impressions et des taux de conversion. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Reports]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Renvoie des données sur les impressions, les taux de clics publicitaires et les conversions pour un large éventail de dimensions publicitaires. |
| [[!UICONTROL Optimal Frequency] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Permet de découvrir l’équilibre optimal entre le nombre d’impressions diffusées et de conversions. Il vous permet d’ajuster le nombre d’impressions à afficher avant de commencer à voir des rendements décroissants. |
| [[!UICONTROL Unique User Reach] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Graphique à bulles, dans lequel chaque bulle est dimensionnée en proportion directe du nombre d’utilisateurs uniques pour la dimension sélectionnée. |

### Considérations

* Si [!DNL Audience Optimization Reports] utilisateurs disposent de contrôles d’accès en fonction du rôle, [!DNL Adobe Customer Care] doit configurer un mappage entre l’identifiant publicitaire et le code d’intégration de la source de données d’Audience Manager de l’entreprise. Les utilisateurs administrateurs peuvent alors fournir des droits RBAC à différents utilisateurs.

* La création de rapports de conversion dans [!DNL Audience Optimization Reports] nécessite une configuration par l’utilisateur final. Les utilisateurs doivent renseigner les fichiers de métadonnées.

* [!DNL Audience Optimization Reports] ne prend pas en charge les modifications apportées aux métadonnées de campagne (telles que le nom de la campagne ou le nom de l’emplacement).

* Les clics sur les publicités de recherche ne sont inclus dans [!DNL Audience Optimization Reports] que lorsqu’ils sont corrélés avec les impressions. En d’autres termes, les clics de recherche sont traités comme des conversions suite aux impressions. Par conséquent, de nombreux clics de recherche peuvent ne pas être inclus dans [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Présentation de l’envoi DSP données d’exposition aux médias à Adobe Audience Manager](overview.md)
>* [Collecter les données de clics et d’impressions à partir des campagnes Advertising DSP](collect.md)
