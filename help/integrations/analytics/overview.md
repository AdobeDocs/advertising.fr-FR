---
title: Présentation de  [!DNL Analytics for Advertising]
description: Présentation de  [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Présentation de [!DNL Analytics for Advertising]

*Annonceurs avec Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] intègre Adobe Analytics et Adobe Advertising pour étendre et améliorer les fonctionnalités de chaque produit.

L’intégration permet aux annonceurs de suivre les interactions de site en cas de clic publicitaire et d’affichage publicitaire dans leurs instances [!DNL Analytics], ce qui permet aux marques de voir comment leurs dépenses publicitaires conduisent à l’engagement du site et aux objectifs commerciaux critiques.

En outre, Adobe Advertising peut accéder aux vastes données propriétaires que [!DNL Analytics] collecte à l’aide de balises [!DNL Analytics] déjà présentes sur le site. Cela permet une gestion de parcours plus robuste, un remarketing propriétaire et des rapports de sites de médias achetés. Adobe Advertising peut utiliser davantage les données [!DNL Analytics] pour l’optimisation des dépenses et des enchères.

Lorsqu’il est correctement utilisé, [!DNL Analytics for Advertising] brouille les lignes entre deux rôles traditionnels : la gestion du parcours publicitaire (le fait d’envoyer des utilisateurs et utilisatrices sur le site par le biais d’annonces publicitaires) et la compréhension de l’engagement du site par le biais d’analyses web.

Avantages du Principal :

* Envoyez [!DNL Analytics] segments directement à Adobe Advertising pour le remarketing de site propriétaire.
* Utilisez [!DNL Analytics] événements personnalisés et standard comme signaux de conversion pour optimiser la publicité sur les médias achetés.
* Tirez parti d’[!DNL Analytics] Analysis Workspace pour mieux comprendre les points d’entrée du site et le comportement des visites.
* resserrer la collaboration entre les analystes web et les équipes de médias achetés.
* Utilisez les identifiants Adobe Advertising persistants d’affichage publicitaire et de clic publicitaire dans [!DNL Analytics] pour comprendre l’engagement du site.
* Améliorez les rapports de médias achetés traditionnels dans Analysis Workspace avec des mesures, des dimensions et une activité de site personnalisées, ce qui n’est pas possible lors de l’exportation de données ou de pixels vers des serveurs de publicités ou d’autres DSP.
* Tirez parti du code [!DNL Analytics] déjà présent sur votre site web pour le tracking et l’optimisation dans Adobe Advertising.

>[!TIP]
>
> Regardez une [vidéo de présentation de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=fr#analytics).

## Utilisation d’Analytics pour le reporting de médias payants

[!DNL Analytics for Advertising] améliore les rapports et insight sur la manière dont votre publicité oriente le comportement du site en vous permettant de :

* Utilisez les identifiants Adobe Advertising persistants d’affichage publicitaire et de clic publicitaire dans [!DNL Analytics] pour comprendre l’engagement du site.
* Tirez parti d’Analysis Workspace pour mieux comprendre les points d’entrée du site et le comportement des visites. Vous pouvez accéder aux données dimensionnelles et d’événement du média payant, qui incluent les noms des entités de la campagne Adobe Advertising (jusqu’aux emplacements et aux annonces) et leurs mesures associées, telles que les clics, les impressions et les coûts.

Pour utiliser [!DNL Analytics] comme outil de création de rapports multimédia payant, votre entreprise a besoin d’une connexion Experience Cloud avec accès à Analysis Workspace. Votre équipe Adobe Advertising vous aidera à mapper vos données Adobe Advertising à des suites de rapports individuelles dans Analysis Workspace. Vous pouvez envoyer des données Adobe Advertising à n’importe quelle suite de rapports, mais vous devez tenir compte des suites de rapports qui ont été mappées à Adobe Advertising et de celles qui ne l’ont pas été. Selon la suite de rapports, cela peut modifier les données signalées.

[Les Adobe Advertising ID dans  [!DNL Analytics]](ids.md) fonctionnent comme d’autres [!DNL eVars], avec une expiration personnalisée et persistante. Par défaut, l’intervalle de recherche en amont d’attribution est défini sur 60 jours pendant la mise en œuvre d’Adobe Advertising. Pour modifier ce paramètre, contactez l’équipe chargée de votre compte Adobe.

Les dimensions Adobe Advertising sont ajoutées avec le suffixe « (AMO ID) » (par exemple, « Type d’annonce (AMO ID) »). Voir « [Mesures Adobe Advertising dans Analysis Workspace »](advertising-metrics-in-analytics.md) pour obtenir une liste des dimensions disponibles.

>[!NOTE]
>
> Lorsque vous affichez des données Adobe Advertising (ou tout jeu de données) dans [!DNL Analytics], sachez que les mesures et les rapports sont basés sur les règles définies dans [!DNL Analytics]. Les données peuvent être différentes de ce que vous voyez dans d’autres systèmes de création de rapports, tels que les rapports de serveur de publicités, les rapports de [!DNL DSP] ou les rapports de moteur de recherche. Pour comprendre les différences de données dans [!DNL Analytics], vous devez savoir quand [!DNL eVar] données expirent, ce qui définit une visite, ce qui est considéré comme l’attribution Dernière touche par rapport à l’attribution persistante totale, etc. Pour plus d’informations, voir [Écarts de données attendus entre  [!DNL Analytics]  et Adobe Advertising](data-variances.md).

## Utilisation d’Analytics pour alimenter les campagnes et portfolios Adobe Advertising

Sans nécessiter de pixels supplémentaires, [!DNL Analytics for Advertising] permet une meilleure optimisation et une segmentation plus facile de l’audience en envoyant deux signaux principaux à Adobe Advertising :

* Mesures de conversion à utiliser comme signaux d’offre :
   * mesures standard, telles que [!UICONTROL Revenue] et [!UICONTROL Cart Views].
   * mesures d’engagement du site, telles que les mesures de pages vues et de visites.
   * mesures de chiffre d’affaires personnalisé.
   * mesures de chiffre d’affaires réservé.
* Segments créés dans [!DNL Analytics] et publiés sur Experience Cloud.

  Vous pouvez utiliser des segments [!DNL Analytics] pour le reciblage de site propriétaire dans les annonces de référencement [!DNL DSP] et payant.

  ([!DNL Search, Social, & Commerce] uniquement) Les annonceurs qui disposent de [!DNL Analytics] mais pas d’Audience Manager peuvent également créer des audiences basées sur les balises de sites web Google (listes de remarketing) et des audiences de correspondance client (listes de clients) à partir de [!DNL Analytics] segments partagés avec Experience Cloud.

### Mesures de conversion du site en tant que signaux d’offres

Vous pouvez utiliser les événements standard et les événements personnalisés de [!DNL Analytics] pour créer des objectifs pondérés dans Adobe Advertising. Les objectifs orientent les décisions d’offres pour vos packages [!DNL DSP] et vos portfolios Search, Social et Commerce.

Pour les campagnes [!DNL Google Ads] et [!DNL Google Microsoft Advertising] dans les portfolios hybrides Search, Social et Commerce, vous pouvez éventuellement charger les objectifs, y compris les événements [!DNL Analytics] dans les objectifs, directement dans les réseaux publicitaires, où ils deviennent disponibles en tant qu’actions de conversion pour les objectifs de conversion personnalisés au niveau du compte et de la campagne.

>[!NOTE]
>
> Vous ne pouvez pas mapper des mesures calculées de [!DNL Analytics] à Adobe Advertising.

Votre équipe Adobe Advertising vous aidera à identifier et à mapper les événements applicables aux performances de médias payants dans Adobe Advertising, où ils sont répertoriés dans [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Consultez « [&#x200B; Mesures Analytics dans Adobe Advertising &#x200B;](analytics-data-in-advertising.md) » pour obtenir une liste des mesures disponibles.

### Segments Analytics pour le reciblage de site

Adobe Advertising peut ingérer des segments [!DNL Analytics] à des fins de remarketing pour Advertising DSP et [!DNL Search, Social, & Commerce] des publicités à l’aide de l’intégration native des audiences Experience Cloud entre [!DNL Analytics] et Experience Cloud.

Pour accéder aux segments [!DNL Analytics], un compte d’annonceur doit activer le service [Experience Cloud ID](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=fr). Lorsque le service d’ID est activé, tous les segments Experience Cloud (y compris les segments créés dans [!DNL Analytics] et publiés sur Experience Cloud, les segments créés dans Adobe Audience Manager, les segments créés dans Experience Cloud à l’aide du [!DNL People core service] et les segments créés dans Adobe Experience Platform et envoyés à Adobe Advertising via Audience Manager) sont disponibles dans Adobe Advertising dès qu’ils sont traités.

[!DNL Analytics] segments sont disponibles dans les 24 heures et sont mis à jour quotidiennement.

Pour plus d’informations sur le service Audiences Experience Cloud, voir [Audiences Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=fr).

## Exemples d’utilisation de l’intégration {#integration-examples}

### Utilisation des données Adobe Advertising dans Analysis Workspace

Pour découvrir comment utiliser vos données Adobe Advertising pour créer des rapports visuels dans Analysis Workspace, regardez la vidéo « [Présentation de Workspace et des rapports](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html?lang=fr) ».

#### Utilisation de conversions d’affichage publicitaire TV connectées dans les rapports

*Utilisateurs Advertising DSP uniquement*

Vous pouvez mesurer l’efficacité de l’entonnoir complet de vos campagnes TV connectée (CTV) en liant l’exposition des annonces sur les appareils CTV aux conversions sur site. Le nouveau filtre de [!UICONTROL Landing Type] « [!UICONTROL View-through (CTV)] » divise les conversions en lignes distinctes pour les valeurs [!UICONTROL Click Through], [!UICONTROL View Through] et [!UICONTROL View Through (CTV)].

Pour afficher vos mesures de conversion des affichages publicitaires CTV, utilisez la vue Emplacement ou la vue Canal marketing dans Analysis Workspace.

Utilisation de la vue Emplacement :

1. Incluez les emplacements de dépenses CTV dans la vue de rapport.

1. Incluez les mesures souhaitées, telles que « Impressions », « Clics », etc.

1. Appliquez les filtres suivants :

   Plateforme publicitaire : `Advertising Cloud DSP`

   Page de destination : `View-Through (CTV)`

Utilisation de la vue Canal marketing :

1. Incluez la dimension `Marketing Channel`.

1. Incluez les mesures souhaitées, telles que « Impressions », « Clics », etc.

1. Appliquez les filtres suivants :

   Plateforme publicitaire : `Advertising Cloud DSP`

   Page de destination : `View-Through (CTV)`

### Création de tableaux de bord Adobe Advertising

Pour découvrir comment effectuer le suivi de vos données Adobe Advertising par rapport à vos objectifs dans Analysis Workspace, regardez la vidéo « [Création de tableaux de bord Adobe Advertising avec Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html?lang=fr) ».

### Utilisation de l’Adobe Advertising ID pour l’analyse de l’entrée sur le site

Pour découvrir comment créer un rapport d’entrée sur le site Adobe Advertising afin de surveiller les influences géographiques, le navigateur et le jour de la semaine, regardez la vidéo « [&#x200B; Créer des rapports d’entrée sur le site Adobe Advertising &#x200B;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html?lang=fr) ».

## Lancement d’une implémentation [!DNL Analytics for Advertising]

Contactez l’équipe chargée de votre compte Adobe, qui effectuera la configuration initiale nécessaire pour commencer et qui vous aidera à planifier votre implémentation et l’utilisation des données en fonction des besoins de votre entreprise.

>[!MORELIKETHIS]
>
>* [Vidéo : présentation de  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=fr)
>* [Conditions préalables et informations clés pour l’implémentation de  [!DNL Analytics for Advertising]](prerequisites.md)
>* [Adobe Advertising ID utilisés par Analytics](ids.md)
>* [Code JavaScript pour Analytics pour Advertising](/help/integrations/analytics/javascript.md)
>* [Écarts de données attendus entre  [!DNL Analytics]  et Adobe Advertising](data-variances.md)
>* [Mesures Adobe Advertising dans Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Données dans Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
