---
title: Présentation de [!DNL Analytics for Advertising]
description: Présentation de [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 94558478-ffa6-4b83-bc79-c7589fe0f14c
source-git-commit: 8911f6ea16878bede96151f004e6de2717484140
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# Présentation de [!DNL Analytics for Advertising]

*Annonceurs avec Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

[!DNL Analytics for Advertising] intègre Adobe Analytics et Adobe Advertising pour étendre et améliorer les fonctionnalités de chaque produit.

L’intégration permet aux annonceurs de suivre les clics publicitaires et les interactions d’affichage publicitaire sur le site dans leurs instances [!DNL Analytics], ce qui permet aux marques de voir comment leurs dépenses publicitaires conduisent à l’engagement sur le site et à des objectifs commerciaux essentiels.

En outre, Adobe Advertising peut accéder aux vastes données propriétaires que [!DNL Analytics] collecte déjà à l’aide de balises [!DNL Analytics] sur le site. Cela permet une gestion plus robuste des parcours, un remarketing propriétaire et des rapports sur les sites de médias payants. Adobe Advertising peut utiliser les données [!DNL Analytics] pour l’optimisation des dépenses et des offres.

Lorsqu&#39;elle est correctement utilisée, [!DNL Analytics for Advertising] brouille les lignes entre deux rôles traditionnels : la gestion des parcours publicitaires (l&#39;acte d&#39;envoyer des utilisateurs sur le site par le biais de publicités) et la compréhension de l&#39;engagement du site par le biais d&#39;analyses web.

Avantages du Principal :

* Envoyez directement des segments [!DNL Analytics] à Adobe Advertising pour le remarketing de site propriétaire.
* Utilisez [!DNL Analytics] événements personnalisés et standard comme signaux de conversion pour optimiser la publicité médias payants.
* Profitez de [!DNL Analytics] Analysis Workspace pour mieux comprendre les points d’entrée sur le site et le comportement des visites.
* Permettre une collaboration plus étroite entre les analystes web et les équipes de médias payants.
* Utilisez des identifiants d’affichage et de clic publicitaire d’Adobe Advertising persistant dans [!DNL Analytics] pour comprendre l’engagement du site.
* Améliorez les rapports multimédia payants traditionnels dans Analysis Workspace avec des mesures personnalisées, des dimensions personnalisées et l’activité du site impossible à réaliser lors de l’exportation de données ou de pixels vers des serveurs d’annonces ou d’autres DSP.
* Profitez du code [!DNL Analytics] déjà présent sur votre site web pour le suivi et l’optimisation dans Adobe Advertising.

>[!TIP]
>
> Regardez une [présentation vidéo de [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=fr#analytics).

## Utilisation d’Analytics pour les rapports sur les médias payants

[!DNL Analytics for Advertising] améliore la création de rapports et les informations sur la manière dont votre publicité entraîne le comportement du site en vous permettant :

* Utilisez des identifiants d’affichage et de clic publicitaire d’Adobe Advertising persistant dans [!DNL Analytics] pour comprendre l’engagement du site.
* Tirer parti d’Analysis Workspace pour mieux comprendre les points d’entrée sur le site et le comportement des visites. Vous pouvez accéder aux données de dimension et d’événement de média payant, qui incluent les noms des entités de campagne d’Adobe Advertising (jusqu’aux emplacements et publicités) et leurs mesures associées, telles que les clics, les impressions et les coûts.

Pour utiliser [!DNL Analytics] comme outil de reporting multimédia payant, votre entreprise a besoin d’une connexion Experience Cloud avec accès à Analysis Workspace. Votre équipe d’Adobes Advertising vous aidera à mapper vos données d’Adobe Advertising à des suites de rapports individuelles dans Analysis Workspace. Vous pouvez envoyer des données d’Adobe Advertising à n’importe quelle suite de rapports, mais vous devez connaître les suites de rapports qui ont été mappées à l’Adobe Advertising et celles qui ne l’ont pas fait. Selon la suite de rapports, cela peut modifier les données signalées.

[Les identifiants d’Adobe Advertising dans  [!DNL Analytics]](ids.md) fonctionnent comme d’autres [!DNL eVars], avec une expiration personnalisée et persistante. Par défaut, l’intervalle de recherche en amont des attributions est défini sur 60 jours pendant la mise en oeuvre de l’Adobe Advertising. Pour modifier ce paramètre, contactez votre équipe de compte d’Adobe.

Les dimensions d’Adobe Advertising sont ajoutées avec le suffixe &quot;(AMO ID)&quot; (par exemple, &quot;Type de publicité (AMO ID)&quot;). Voir &quot;[Adobe Advertising des mesures dans Analysis Workspace](advertising-metrics-in-analytics.md)&quot; pour obtenir la liste des dimensions disponibles.

>[!NOTE]
>
> Lorsque vous affichez des données d’Adobe Advertising (ou tout jeu de données) dans [!DNL Analytics], sachez que les mesures et les rapports sont basés sur les règles définies dans [!DNL Analytics]. Les données peuvent être différentes de celles que vous voyez dans d’autres systèmes de création de rapports, tels que les rapports sur les serveurs de publicités, les rapports [!DNL DSP] ou les rapports sur les moteurs de recherche. Pour comprendre les différences de données dans [!DNL Analytics], vous devez savoir à quel moment les données [!DNL eVar] expirent, ce qui définit une visite, ce qui est considéré comme une attribution Dernière touche par rapport à une attribution persistante totale, et d’autres facteurs. Pour plus d’informations, voir [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](data-variances.md).

## Utilisation d’Analytics pour optimiser les campagnes et les Portfolios Adobe Advertising

Sans nécessiter de pixels supplémentaires, [!DNL Analytics for Advertising] permet une meilleure optimisation et une segmentation plus facile de l’audience en envoyant deux signaux principaux à Adobe Advertising :

* Mesures de conversion à utiliser comme signaux d’offre :
   * des mesures standard, telles que [!UICONTROL Revenue] et [!UICONTROL Cart Views].
   * les mesures d’engagement du site, telles que les mesures de pages vues et de visites.
   * mesures de recettes personnalisées.
   * mesures de recettes réservées.
* Segments créés dans [!DNL Analytics] et publiés sur Experience Cloud.

  Vous pouvez utiliser des segments [!DNL Analytics] pour le reciblage de site propriétaire dans [!DNL DSP] et les publicités de référencement payant.

  ([!DNL Search, Social, & Commerce] uniquement) Les annonceurs disposant de [!DNL Analytics] mais ne bénéficiant pas d’une Audience Manager peuvent également créer des audiences basées sur des balises de site web Google (listes de remarketing) et des audiences de correspondance de clients (listes de clients) à partir de [!DNL Analytics] segments partagés avec Experience Cloud.

### Mesures de conversion de site en tant que signaux d’offre

Vous pouvez utiliser vos événements standard et personnalisés de [!DNL Analytics] pour créer des objectifs pondérés dans Adobe Advertising. Les objectifs informent les décisions d’offre pour vos packages [!DNL DSP] et vos portefeuilles Search, Social et Commerce.

Pour les campagnes [!DNL Google Ads] et [!DNL Google Microsoft Advertising] des portefeuilles hybrides Search, Social et Commerce, vous pouvez éventuellement télécharger les objectifs (y compris tout événement [!DNL Analytics] des objectifs) directement vers les réseaux publicitaires, où ils deviennent disponibles en tant qu’actions de conversion pour les objectifs de conversion personnalisés au niveau du compte et de la campagne.

>[!NOTE]
>
> Vous ne pouvez pas mapper les mesures calculées de [!DNL Analytics] vers Adobe Advertising.

Votre équipe d’Adobe Advertising vous aidera à identifier et à mapper les événements applicables aux performances des médias payants dans Adobe Advertising, où ils sont répertoriés dans [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Conversions].

Voir &quot;[Mesures Analytics dans Adobe Advertising](analytics-data-in-advertising.md)&quot; pour obtenir la liste des mesures disponibles.

### Segments Analytics pour le reciblage de site

Adobe Advertising peut ingérer [!DNL Analytics] segments à des fins de remarketing pour les annonces Advertising DSP et [!DNL Search, Social, & Commerce] à l’aide de l’intégration d’audiences Experience Cloud natives entre [!DNL Analytics] et Experience Cloud.

Pour accéder aux segments [!DNL Analytics], un compte publicitaire doit activer le [service d’ID Experience Cloud](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=fr). Lorsque le service d’ID est activé, tous les segments Experience Cloud (y compris les segments créés dans [!DNL Analytics] et publiés dans Experience Cloud, les segments créés dans Adobe Audience Manager, les segments créés dans Experience Cloud à l’aide de [!DNL People core service] et les segments créés dans Adobe Experience Platform et envoyés à l’Adobe Advertising par Audience Manager) sont disponibles dans Adobe Advertising dès qu’ils sont traités.

[!DNL Analytics] segments sont disponibles dans les 24 heures et sont mis à jour quotidiennement.

Pour plus d’informations sur le service Audiences Experience Cloud, voir [Audiences Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html?lang=fr).

## Exemples d’utilisation de l’intégration {#integration-examples}

### Utilisation des données d’Adobe Advertising dans Analysis Workspace

Pour savoir comment utiliser vos données d’Adobe Advertising pour créer des rapports visuels dans Analysis Workspace, visionnez la vidéo &quot;[Introduction à Workspace et création de rapports](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html?lang=fr)&quot;.

#### Utilisation de conversions d’affichages publicitaires de la télévision connectée dans les rapports

*Utilisateurs d’Advertising DSP uniquement*

Vous pouvez mesurer l’efficacité de l’entonnoir complet de vos campagnes de télévision connectée (CTV) en liant l’exposition aux publicités sur les appareils CTV aux conversions sur site. Le nouveau filtre [!UICONTROL Landing Type] &quot;[!UICONTROL View-through (CTV)]&quot; divise les conversions en lignes distinctes pour les valeurs [!UICONTROL Click Through], [!UICONTROL View Through] et [!UICONTROL View Through (CTV)].

Pour afficher vos mesures de conversion d’affichage publicitaire CTV, utilisez la vue Emplacement ou la vue Canal marketing dans Analysis Workspace.

Utilisation de la vue Emplacement :

1. Incluez des emplacements de dépenses CTV dans la vue de création de rapports.

1. Incluez les mesures souhaitées, telles que &quot;Impressions&quot;, &quot;Clics&quot;, etc.

1. Appliquez les filtres suivants :

   Plateforme d’annonces publicitaires : `Advertising Cloud DSP`

   Page d’entrée : `View-Through (CTV)`

Utilisation de la vue Canal marketing :

1. Incluez la dimension `Marketing Channel`.

1. Incluez les mesures souhaitées, telles que &quot;Impressions&quot;, &quot;Clics&quot;, etc.

1. Appliquez les filtres suivants :

   Plateforme d’annonces publicitaires : `Advertising Cloud DSP`

   Page d’entrée : `View-Through (CTV)`

### Création de tableaux de bord d’Adobe Advertising

Pour savoir comment effectuer le suivi de vos données d’Adobe Advertising par rapport à vos objectifs dans Analysis Workspace, visionnez la vidéo &quot;[Création de tableaux de bord d’Adobe Advertising avec Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-dashboards-a4adc.html?lang=fr)&quot;.

### Utilisation de l’Adobe Advertising ID pour l’analyse des entrées dans le site

Pour savoir comment créer un rapport d’entrée sur le site d’Adobe Advertising afin de surveiller les influences jour de la semaine, heure de la journée, navigateur et géographique, visionnez la vidéo &quot;[Créer des rapports d’entrée sur le site d’Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-site-entry-a4adc.html?lang=fr)&quot;.

## Initiation d’une implémentation [!DNL Analytics for Advertising]

Contactez votre équipe de compte d’Adobe, qui effectuera la configuration initiale nécessaire pour commencer et vous aidera à planifier votre mise en oeuvre et votre utilisation des données en fonction des besoins de votre organisation.

>[!MORELIKETHIS]
>
>* [Vidéo : Introduction à [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/intro-a4adc.html?lang=fr)
>* [Conditions préalables et informations clés pour la mise en oeuvre  [!DNL Analytics for Advertising]](prerequisites.md)
>* [ID d’Adobe Advertising utilisés par Analytics](ids.md)
>* [Code JavaScript pour Analytics pour Advertising](/help/integrations/analytics/javascript.md)
>* [Écarts de données attendus entre [!DNL Analytics] et Adobe Advertising](data-variances.md)
>* [Adobe Advertising des mesures dans Analysis Workspace](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Données en Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
