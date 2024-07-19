---
title: Données utilisées pour les rapports
description: Découvrez les différents types de données disponibles dans les vues de données et les rapports personnalisés.
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
source-git-commit: 840c7f6295b73a784725c301a78ae89c827fd45e
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# Données utilisées pour les rapports

Search, Social et Commerce comprend un ensemble complet de rapports de performances reposant sur les données de clics et de conversions. Vous pouvez afficher des données de performances de base pour les différents composants d’un portefeuille ou d’un compte publicitaire à partir des vues [!UICONTROL Portfolios] et [!UICONTROL Campaigns] ainsi qu’en générant divers rapports de base et avancés.

Les annonceurs qui utilisent le service de suivi de conversion Adobe Advertising peuvent également identifier le nombre de clics pour un emplacement géographique ou le nom de domaine d’un site web référent, la manière dont les publicités dans chaque canal et les différents événements menant à une conversion contribuent au taux de conversion global et la distribution des conversions pour une seule [mesure de conversion](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) par canal marketing. Les rapports disponibles varient en fonction du type de compte d’utilisateur. L’équipe Compte d’Adobe a accès à tous les rapports.

La plupart des rapports peuvent être personnalisés pour afficher uniquement les informations que vous souhaitez afficher. Les mesures standard suivantes sont disponibles dans la plupart des rapports et sont calculées au niveau de la publicité :

* **Mesures de performances standard :**

   * **[!UICONTROL Impressions]:** nombre total de fois où la publicité a été placée.

   * **[!UICONTROL Clicks]:** nombre total de clics sur un lien de la publicité.

   * **[!UICONTROL Cost]:** coût total de la publicité. Le coût de la publicité PPC (paiement par clic) est toujours le nombre de clics multiplié par le coût par clic.

   * **[!UICONTROL Cost per Click]:** coût moyen d’un clic pour une publicité, qui est le coût de la publicité divisé par le nombre total de clics pour la publicité. Par exemple, si vous dépensez 100 USD pour une impression publicitaire et que la publicité génère 10 clics, le coût par clic est de 100 USD/10=10 USD par clic.

   * **[!UICONTROL Average Position]:** (le cas échéant) Position moyenne d’une publicité qui a été placée, pondérée par le nombre d’impressions.

   * **[!UICONTROL Estimated Clicks]:** (Inclus dans les rapports avancés pour les annonceurs disposant uniquement du service de suivi de conversion d’Adobe Advertising) Nombre total de clics estimés pour une ville ou un nom de domaine d’un site web référent. Cela peut inclure les données des réseaux publicitaires pour lesquels un annonceur ne dispose pas de compte publicitaire.

* **Mesures de conversion :** nombre total de conversions pour chacune des mesures de conversion de l’annonceur ou données de transaction suivies vers une mesure de conversion. Cela peut inclure des mesures de conversion et d’engagement du site, mais pas des mesures calculées ni des mesures calculées avancées, qui sont synchronisées à partir d’Adobe Analytics.

  Cela peut également inclure les [[!DNL Google Ads] conversions suivies](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) et les [[!DNL Google Analytics] conversions suivies](/help/search-social-commerce/admin/data-sources/data-source-about.md) synchronisées pour le compte de l’annonceur.

* **Mesures personnalisées :** vos propres mesures, que vous dérivez en créant des formules basées sur des mesures existantes (comme le coût par commande).

## Disponibilité des données

Lorsque vous générez des rapports, vous pouvez choisir comment attribuer des données de conversion dans une série d’événements qui mènent à une conversion. Par exemple, vous pouvez choisir d’attribuer la conversion entière au dernier événement ou de peser le dernier plus que les autres. Par défaut, les conversions sont attribuées au dernier événement.

Selon la règle d’attribution que vous spécifiez pour le rapport, les données de chaque type de rapport sont disponibles pour les dates suivantes.

| Groupe de rapports | Rapport | Dates pour lesquelles des données sont disponibles |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | À partir du 15 mai 2021.<br><br><b>Exception :</b> Les données des mesures de visibilité sont disponibles à partir du 8 septembre 2022. |
| | Tous les autres [!UICONTROL Basic Reports] | Les 36 mois précédents.<br><br><b>Exception :</b> Les données des mesures de visibilité sont disponibles à partir du 8 septembre 2022. |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | Les 45 jours précédents. |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | Les deux (2) mois précédents plus le mois en cours. |
| [!UICONTROL Assist Reports] | Tous | Les 18 mois précédents. |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | L&#39;année précédente. |
| | [!UICONTROL RSA Assets Report] | À partir du 10 août 2022. |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | Les 180 derniers jours. |
| | Tous les autres [!UICONTROL Specialty Reports] | Les deux (2) mois précédents. |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | Les 18 mois précédents. |
| [!UICONTROL Change History Report] | — | Les 31 jours précédents. |

>[!MORELIKETHIS]
>
>* [À propos des rapports](report-about.md)
>* [ Tâches de configuration initiales pour les rapports ](initial-setup.md)
