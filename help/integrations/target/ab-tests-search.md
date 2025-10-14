---
title: Configuration des tests A/B pour les publicités Commerce, sociales et de recherche Adobe Advertising dans Adobe Target
description: Découvrez comment configurer un test A/B dans  [!DNL Target]  pour vos publicités  [!DNL Google Ads]  et  [!DNL Microsoft Advertising]  dans Search, Social et Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configuration des tests A/B dans Adobe Target pour les publicités Advertising Search, Social et Commerce

*Publicitaires avec Advertising Search, Social et Commerce uniquement*

Comptes *[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

Adobe Advertising et Adobe Target facilitent la configuration des tests A/B d’expérience de page de destination pour le trafic publicitaire numérique [!DNL Google Ads] et [!DNL Microsoft Advertising] :

* Améliorer les taux de conversion (CVR) et les mesures d&#39;efficacité d&#39;acquisition (telles que CPA, CPL et CAC).

* Offrez une expérience de page de destination plus personnalisée et pertinente pour la publicité (par exemple, en faisant correspondre la création image/vidéo, la copie, le mot-clé ou tout autre signal publicitaire à la page de destination).

Vous pouvez également combiner les dimensions de rapports d’intégration natives [[!DNL Analytics] pour Advertising](/help/integrations/analytics/overview.md) et [[!DNL Analytics] pour [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=fr) intégrées à Adobe Analytics afin de mesurer et de visualiser vos données de test avec des mesures et des événements de succès [!DNL Analytics].

Consultez les sections suivantes pour connaître les conditions préalables, les instructions de configuration des tests A/B dans [!DNL Target] pour le trafic de clics publicitaires provenant des publicités dans Search, Social et Commerce, ainsi que des conseils sur la manière de mesurer et de visualiser vos tests dans [!DNL Analytics].

## Conditions préalables

### Produits requis

* Recherche, réseaux sociaux et Commerce
* [!DNL Target]

### Produits et intégrations recommandés

* [!DNL Analytics]

* [[!DNL Analytics] pour Advertising](/help/integrations/analytics/overview.md) intégration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Intégration [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=fr)

## Étape 1 : créer une activité de test A/B dans [!DNL Target] pour Search, Social et Commerce

Les instructions suivantes mettent en évidence des informations relatives au cas d’utilisation de Search, Social et Commerce.

1. [Connexion à Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=fr).

1. [Créer un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=fr) :

   1. Dans le champ **[!UICONTROL Enter Activity URL]** , saisissez l’URL de la page de destination pour le test.

   1. Dans le champ **[!UICONTROL Goal]** , saisissez la mesure de succès du test.

      >[!NOTE]
      >
      >Assurez-vous que [!DNL Analytics] est activé en tant que source de données dans [!DNL Target] et que la suite de rapports appropriée est sélectionnée.

   1. Définissez la **[!UICONTROL Priority]** sur `High` ou `999` pour éviter les conflits lorsque les utilisateurs et utilisatrices du segment de test reçoivent une expérience sur site incorrecte.


   1. Dans **[!UICONTROL Reporting Settings]**, sélectionnez les **[!UICONTROL Company Name]** et **[!UICONTROL Report Suite]** connectés à votre compte Search, Social et Commerce.

      Pour obtenir des conseils supplémentaires sur les rapports, voir « [Bonnes pratiques et dépannage en matière de rapports](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=fr) ».

   1. Dans le champ **[!UICONTROL Date Range]** , saisissez les dates de début et de fin appropriées pour le test.

   1. Sélectionnez **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. Dans le champ **[!UICONTROL Value]** , saisissez le [!UICONTROL Network Account ID], le [!UICONTROL Network Campaign ID], le [!UICONTROL Network Adgroup ID] ou le [!UICONTROL Network Ad ID] de l’entité de réseau publicitaire appropriée dans Search, Social et Commerce. Vous pouvez ainsi utiliser les paramètres de chaîne de requête [!DNL Target] pour les audiences de clics publicitaires de l’entité.

      Vous pouvez trouver l’identifiant en [ajoutant la colonne d’identifiant appropriée à la vue d’entité](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] colonne dans la vue [!UICONTROL Accounts]](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] colonne dans la vue [!UICONTROL Accounts]")

      Contactez l’équipe chargée de votre compte Adobe si vous avez besoin d’aide.

   1. Pour l’**[!UICONTROL Traffic Allocation Method]**, sélectionnez **[!UICONTROL Manual (Default)]** et divisez l’audience 50/50.

   1. Enregistrez l’activité.

1. Utilisez le [compositeur d’expérience visuelle Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=fr) pour apporter des modifications de conception au modèle de page de destination du test A/B.

   * Expérience A : ne pas modifier, car il s’agit de l’expérience de page de destination par défaut/de contrôle sans personnalisation.

   * Expérience B : utilisez l’interface utilisateur [!DNL Target] pour personnaliser le modèle de page de destination en fonction des ressources incluses dans le test (telles que les titres, la copie, l’emplacement du bouton et les éléments créatifs).

   >[!NOTE]
   >
   >Pour des cas d’utilisation de test créatif, contactez l’équipe chargée de votre compte Adobe.

## Étape 2 : configurer votre [!DNL Analytics for Target] Analysis Workspace dans [!DNL Analytics]

[!DNL Analytics for Target] (A4T) est une intégration intersolutions qui permet aux annonceurs de créer des activités [!DNL Target] basées sur des mesures de conversion [!DNL Analytics] et des segments d’audience, puis de mesurer les résultats à l’aide de [!DNL Analytics] comme source de création de rapports. Toutes les créations de rapports et segmentations pour cette activité sont basées sur la collecte de données [!DNL Analytics].

Pour plus d’informations sur [!DNL Analytics for Target], y compris un lien vers des instructions d’implémentation, consultez « [Adobe Analytics comme source de création de rapports pour Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=fr) ».

### Configurer le panneau [!DNL Analytics for Target]

Dans Analysis Workspace, configurez l’[!DNL Analytics for Target panel] pour analyser vos activités et expériences [!DNL Target]. Gardez à l’esprit les informations et conseils importants suivants concernant vos rapports.

#### Mesures

* Créez un panneau dans l’espace de travail spécifique au compte, à la campagne ou au groupe publicitaire Adobe Advertising<!-- only applicable entities? --> pour lequel le test a été exécuté. Utilisez des visualisations de synthèse pour afficher les mesures Adobe Advertising dans le même rapport que les performances du test [!DNL Target].

* Établissez la priorité en utilisant les mesures sur site (telles que les visites et les conversions) pour mesurer les performances.

* Sachez que les mesures multimédia agrégées d’Adobe Advertising (telles que les impressions, les clics et les coûts) ne peuvent pas être mises en correspondance avec les mesures [!DNL Target].

#### Dimensions

Les dimensions suivantes se rapportent aux [!DNL Analytics for Target] :

* **Activités cibles** : nom du test A/B

* **Expériences Target** : noms des expériences de page de destination utilisées dans l’activité

* **Activité cible** > **Expérience** : nom de l’activité et nom de l’expérience sur la même ligne

### Dépannage d’Analytics for [!DNL Target] Data

Dans Analysis Workspace, si vous constatez que les données d’activité et d’expérience sont minimales ou ne sont pas renseignées, procédez comme suit :

* Vérifiez que le même [!UICONTROL Supplemental Data ID] (SDID) est utilisé pour les [!DNL Target] et les [!DNL Analytics]. Vous pouvez vérifier les valeurs du SDID à l’aide du débogueur Adobe Experience Cloud [&#128279;](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=fr) sur la page de destination vers laquelle la campagne dirige les utilisateurs.

[Valeurs de SDID (Supplemental Data ID) dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Sur la même page de destination, vérifiez que a) le [!UICONTROL Hostname] affiché dans Adobe Debugger sous [!UICONTROL Solutions] > [!UICONTROL Target] correspond à b) le [!UICONTROL Tracking Server] affiché dans [!DNL Target] pour l’activité (sous [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] nécessite l’envoi d’un serveur de suivi [!DNL Analytics] dans les appels de [!DNL Target] vers le serveur de collecte de données [!DNL Modstats] pour Analytics.<!-- just "to Analytics?"-->

[Valeur du nom d’hôte dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valeur du serveur de suivi dans Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Informations complémentaires

* [Intégrer Target à Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=fr) - Explique comment configurer le reporting [!DNL Target] dans Analysis Workspace.
* [Présentation du test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=fr) - Décrit les activités de test A/B que vous pouvez utiliser avec les annonces Search, Social et Commerce.
* [Présentation d’Analytics pour Advertising &#x200B;](/help/integrations/analytics/overview.md) - Introduit Analytics pour Advertising, qui vous permet d’effectuer le suivi des interactions de site de clics publicitaires et de vues publicitaires dans vos instances Analytics.

>[!MORELIKETHIS]
>
>* [Configuration de tests A/B dans Adobe Target pour Advertising DSP Ads](ab-tests-dsp.md)
