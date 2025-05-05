---
title: Configuration de tests A/B pour les annonces Adobe Advertising Search, Social et Commerce dans Adobe Target
description: Découvrez comment configurer un test A/B dans  [!DNL Target] pour vos  [!DNL Google Ads] publicités et [!DNL Microsoft Advertising] dans Search, Social et Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configuration de tests A/B dans Adobe Target pour les annonces Advertising Search, Social et Commerce

*Annonceurs avec Advertising Search, Social et Commerce uniquement*

*[!DNL Google Ads]et [!DNL Microsoft Advertising] comptes uniquement*

Adobe Advertising et Adobe Target facilitent la configuration des tests A/B d’expérience de page d’entrée pour le trafic publicitaire numérique [!DNL Google Ads] et [!DNL Microsoft Advertising] pour :

* Améliorez les taux de conversion (CVR) et les mesures d’efficacité d’acquisition (telles que CPA, CPL et CAC).

* Proposer une expérience de page d’entrée plus personnalisée qui soit pertinente pour la publicité (par exemple, faire correspondre l’image/la vidéo créative, la copie, le mot-clé ou tout autre signal publicitaire à la page d’entrée).

Vous pouvez également combiner les dimensions de création de rapports natives [[!DNL Analytics] pour Advertising](/help/integrations/analytics/overview.md) et [[!DNL Analytics] pour [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=fr) intégrées à Adobe Analytics pour mesurer et visualiser vos données de test avec des mesures [!DNL Analytics] et des événements de succès.

Reportez-vous aux sections suivantes pour connaître les conditions préalables, les instructions de configuration des tests A/B dans [!DNL Target] pour le trafic de clics publicitaires dans Search, Social et Commerce, ainsi que des conseils sur la mesure et la visualisation de vos tests dans [!DNL Analytics].

## Conditions préalables

### Produits requis

* Recherche, Social et Commerce
* [!DNL Target]

### Produits et intégrations recommandés

* [!DNL Analytics]

* [[!DNL Analytics] pour l’intégration Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Intégration [[!DNL Analytics] pour [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=fr)

## Étape 1 : création d’une activité de test A/B dans [!DNL Target] pour Search, Social et Commerce

Les instructions suivantes présentent des informations relatives au cas d’utilisation de Search, Social et Commerce.

1. [Connectez-vous à Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html?lang=fr).

1. [Créez un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=fr) :

   1. Dans le champ **[!UICONTROL Enter Activity URL]** , saisissez l’URL de la landing page pour le test.

   1. Dans le champ **[!UICONTROL Goal]** , saisissez la mesure de succès du test.

      >[!NOTE]
      >
      >Assurez-vous que [!DNL Analytics] est activé en tant que source de données dans [!DNL Target] et que la suite de rapports correcte est sélectionnée.

   1. Définissez **[!UICONTROL Priority]** sur `High` ou `999` pour éviter les conflits lorsque les utilisateurs du segment de test reçoivent une expérience sur site incorrecte.


   1. Dans **[!UICONTROL Reporting Settings]**, sélectionnez les **[!UICONTROL Company Name]** et **[!UICONTROL Report Suite]** connectés à votre compte Search, Social, &amp; Commerce.

      Pour obtenir des conseils supplémentaires sur la création de rapports, voir &quot;[Bonnes pratiques en matière de création de rapports et résolution des problèmes](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html?lang=fr)&quot;.

   1. Dans le champ **[!UICONTROL Date Range]** , saisissez les dates de début et de fin appropriées pour le test.

   1. Sélectionnez **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. Dans le champ **[!UICONTROL Value]** , saisissez les [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID] ou [!UICONTROL Network Ad ID] correspondant à l’entité de réseau publicitaire appropriée dans Search, Social et Commerce. Vous pouvez ainsi utiliser les paramètres de chaîne de requête [!DNL Target] pour les audiences de clics publicitaires pour l’entité.

      Vous pouvez trouver l&#39;ID en [ajoutant la colonne d&#39;ID appropriée à la vue d&#39;entité](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] dans la colonne [!UICONTROL Accounts] view](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] dans la [!UICONTROL Accounts] view")

      Contactez votre équipe de compte d’Adobe si vous avez besoin d’aide.

   1. Pour le **[!UICONTROL Traffic Allocation Method]**, sélectionnez **[!UICONTROL Manual (Default)]** et divisez l’audience 50/50.

   1. Enregistrez l’activité.

1. Utilisez [le compositeur d’expérience visuelle de Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html?lang=fr) pour apporter des modifications de conception au modèle de page d’entrée de test A/B.

   * Expérience A : ne modifiez pas, car il s’agit de l’expérience de page d’entrée par défaut/de contrôle sans personnalisation.

   * Expérience B : utilisez l’interface utilisateur [!DNL Target] pour personnaliser le modèle de page d’entrée en fonction des ressources incluses dans le test (comme les titres, la copie, le positionnement des boutons et les éléments créatifs).

   >[!NOTE]
   >
   >Par exemple, contactez votre équipe de compte d’Adobe pour des cas pratiques de test créatif.

## Étape 2 : configuration de votre [!DNL Analytics for Target] Analysis Workspace dans [!DNL Analytics]

[!DNL Analytics for Target] (A4T) est une intégration intersolutions qui permet aux annonceurs de créer des activités [!DNL Target] basées sur [!DNL Analytics] mesures de conversion et segments d’audience, puis de mesurer les résultats à l’aide de [!DNL Analytics] comme source de création de rapports. Tous les rapports et segmentation pour cette activité sont basés sur la collecte de données [!DNL Analytics].

Pour plus d’informations sur [!DNL Analytics for Target], y compris un lien vers les instructions de mise en oeuvre, voir &quot;[Adobe Analytics as a reporting source for Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=fr)&quot;.

### Configuration du panneau [!DNL Analytics for Target]

Dans Analysis Workspace, configurez le [!DNL Analytics for Target panel] pour analyser vos activités et expériences [!DNL Target]. Gardez à l’esprit les recommandations et informations importantes suivantes concernant vos rapports.

#### Mesures

* Créez un panneau dans l’espace de travail spécifique au compte d’Adobe Advertising, à la campagne ou au groupe publicitaire <!-- only applicable entities? --> pour lequel le test a été exécuté. Utilisez des visualisations récapitulatives pour afficher les mesures d’Adobe Advertising dans le même rapport que les performances du test [!DNL Target].

* Définir la priorité de l’utilisation des mesures sur site (telles que les visites et les conversions) pour mesurer les performances.

* Comprenez que les mesures multimédia agrégées provenant de l’Adobe Advertising (telles que les impressions, les clics et les coûts) ne peuvent pas être associées aux mesures [!DNL Target].

#### Dimensions

Les dimensions suivantes se rapportent à [!DNL Analytics for Target] :

* **Activités cibles** : nom du test A/B

* **Expériences Target** : noms des expériences de page d’entrée utilisées dans l’activité

* **Activité cible** > **Expérience** : nom de l’activité et nom de l’expérience dans la même ligne

### Dépannage d’Analytics pour les données [!DNL Target]

Dans Analysis Workspace, si vous constatez que les données d’activité et d’expérience sont minimales ou ne sont pas renseignées, procédez comme suit :

* Vérifiez que le même [!UICONTROL Supplemental Data ID] (SDID) est utilisé pour [!DNL Target] et [!DNL Analytics]. Vous pouvez vérifier les valeurs du SDID à l’aide du [débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html?lang=fr) sur la page d’entrée vers laquelle la campagne dirige les utilisateurs.

[Valeurs SDID (Supplemental Data ID) dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Sur la même page d’entrée, vérifiez que a) le [!UICONTROL Hostname] affiché dans l’Adobe Debugger sous [!UICONTROL Solutions] > [!UICONTROL Target] correspond à b) le [!UICONTROL Tracking Server] affiché dans [!DNL Target] pour l’activité (sous [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] nécessite qu’un serveur de suivi [!DNL Analytics] soit envoyé dans les appels de [!DNL Target] au serveur de collecte de données [!DNL Modstats] pour Analytics.<!-- just "to Analytics?"-->

[Valeur du nom d’hôte dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valeur du serveur de suivi dans Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Autres lectures

* [Intégrer Target avec Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html?lang=fr) - Explique comment configurer la création de rapports [!DNL Target] dans Analysis Workspace.
* [Présentation du test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html?lang=fr) - Décrit les activités de test A/B que vous pouvez utiliser avec les annonces Search, Social et Commerce.
* [Présentation d’Analytics pour Advertising](/help/integrations/analytics/overview.md) - Introduit Analytics pour Advertising, qui vous permet d’effectuer le suivi des clics publicitaires et des interactions de site d’affichage publicitaire dans vos instances Analytics.

>[!MORELIKETHIS]
>
>* [Configuration de tests A/B dans Adobe Target pour Advertising DSP Ads](ab-tests-dsp.md)
