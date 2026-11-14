---
title: Données utilisées pour les rapports
description: Découvrez les différents types de données disponibles dans les vues de données et les rapports personnalisés.
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
TQID: 'https://experienceleague.adobe.com/dJGj3NmyEAmXwLdTYqCURrPhiIlJzpY1XdjrBVVUsgU'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9166e3e1-13c1-5edf-bc2a-c6e22231df68
    internal-label: Search Reports
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: fbbc4aabc435023aafbef2443735a7fb285561be
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 6%
---
# Données utilisées pour les rapports

Search, Social et Commerce comprend un ensemble complet de rapports de performances basés sur les données de clics et de conversion. Vous pouvez afficher des données de performances de base pour les différents composants d’un portefeuille ou d’un compte publicitaire à partir des vues [!UICONTROL Portfolios] et [!UICONTROL Campaigns], ainsi qu’en générant divers rapports de base et avancés.

Les annonceurs qui utilisent le service de suivi des conversions d’Adobe Advertising peuvent également identifier le nombre de clics pour un emplacement géographique ou un nom de domaine d’un site web de référence, la manière dont les publicités dans chaque canal et les différents événements menant à une conversion contribuent au taux de conversion global, ainsi que la répartition des conversions pour une [mesure de conversion](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) unique par canal marketing. Les rapports disponibles varient selon le type de compte utilisateur. L’équipe du compte Adobe a accès à tous les rapports.

La plupart des rapports peuvent être personnalisés pour afficher uniquement les informations souhaitées. Les mesures standard suivantes sont disponibles dans la plupart des rapports et sont calculées au niveau des annonces :

* **Mesures de performances standard :**

  * **[!UICONTROL Impressions]:** Le nombre total de fois où la publicité a été placée.

  * **[!UICONTROL Clicks]:** Nombre total de clics sur un lien de la publicité.

  * **[!UICONTROL Cost]:** Coût total de la publicité. Le coût de la publicité de paiement par clic (PPC) correspond toujours au nombre de clics multiplié par le coût par clic.

  * **[!UICONTROL Cost per Click]:** coût moyen d’un clic pour une annonce publicitaire, qui correspond au coût de l’annonce publicitaire divisé par le nombre total de clics sur l’annonce. Par exemple, si vous dépensez 100 USD pour une impression d’annonce et que l’annonce génère 10 clics, le coût par clic est de 100 USD/10=10 USD par clic.

  * **[!UICONTROL Average Position]:** (le cas échéant) Position moyenne d’une publicité qui a été placée, pondérée par le nombre d’impressions.

  * **[!UICONTROL Estimated Clicks]:** (inclus dans les rapports avancés pour les annonceurs avec le service de suivi des conversions Adobe Advertising uniquement) Nombre total estimé de clics pour une ville ou un nom de domaine d’un site web de référence. Cela peut inclure des données pour les réseaux publicitaires pour lesquels un annonceur n’a pas de compte publicitaire.

* **Mesures de conversion :** Nombre total de conversions pour chacune des mesures de conversion de l’annonceur ou des données de transaction suivies vers une mesure de conversion. Il peut s’agir de mesures d’engagement du site et de conversion, mais pas de mesures calculées ni de mesures calculées avancées, synchronisées à partir d’Adobe Analytics.

  Cela peut également inclure les conversions [[!DNL Google Ads] suivies](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) et les conversions [[!DNL Google Analytics] suivies](/help/search-social-commerce/admin/data-sources/data-source-about.md) synchronisées pour le compte de l’annonceur.

* **Mesures personnalisées :** vos propres mesures, que vous obtenez en créant des formules basées sur des mesures existantes (telles que le coût par commande).

## Disponibilité des données

Lorsque vous générez des rapports, vous pouvez choisir comment attribuer les données de conversion dans une série d’événements qui conduisent à une conversion. Par exemple, vous pouvez choisir d’attribuer l’intégralité de la conversion au dernier événement ou de pondérer le dernier événement plus que les autres. Par défaut, les conversions sont attribuées au dernier événement.

Selon la règle d’attribution que vous spécifiez pour le rapport, les données de chaque type de rapport sont disponibles pour les dates suivantes.

| Groupe de rapports | Rapport | Dates pour lesquelles des données sont disponibles |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | Les 36 mois précédents. |
| | Tous les autres [!UICONTROL Basic Reports] | Les 36 mois précédents. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Les 45 jours précédents. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Les deux (2) mois précédents plus le mois en cours. |
| [!UICONTROL Assist Reports] | Tous | Les 18 mois précédents. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | L&#39;année précédente. |
| | [!UICONTROL Google Asset Group Performance Report] | Les 36 mois précédents. |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | Les 180 derniers jours. |
| | [!UICONTROL RSA Assets Report] | Les 36 mois précédents. |
| | Tous les autres [!UICONTROL Specialty Reports] | Les deux (2) mois précédents. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Les 18 mois précédents. |
| [!UICONTROL Change History Report] | — | Les 31 jours précédents. |

>[!MORELIKETHIS]
>
>* [À propos des rapports](/help/search-social-commerce/reports/report-about.md)
>* [Tâches de configuration initiale pour les rapports](/help/search-social-commerce/reports/initial-setup.md)
