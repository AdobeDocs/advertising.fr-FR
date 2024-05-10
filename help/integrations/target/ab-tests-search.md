---
title: Configuration de tests A/B pour les annonces Adobe Advertising Search, Social et Commerce dans Adobe Target
description: Découvrez comment configurer un test A/B dans [!DNL Target] pour votre [!DNL Google Ads] et [!DNL Microsoft Advertising] publicités dans Search, Social et Commerce.
exl-id: 564c7d61-beec-40cf-ac68-83d1e87e3008
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Configuration de tests A/B dans Adobe Target pour les publicités Search, Social et Commerce

*Annonceurs avec Advertising Search, Social et Commerce uniquement*

*[!DNL Google Ads]et [!DNL Microsoft Advertising] comptes uniquement*

Adobe Advertising et Adobe Target facilitent la configuration des tests A/B d’expérience de page d’entrée pour le trafic publicitaire numérique [!DNL Google Ads] et [!DNL Microsoft Advertising] à :

* Améliorez les taux de conversion (CVR) et les mesures d’efficacité d’acquisition (telles que CPA, CPL et CAC).

* Proposer une expérience de page d’entrée plus personnalisée qui soit pertinente pour la publicité (par exemple, faire correspondre l’image/la vidéo créative, la copie, le mot-clé ou tout autre signal publicitaire à la page d’entrée).

Vous pouvez également combiner les [[!DNL Analytics] pour la publicité](/help/integrations/analytics/overview.md) et [[!DNL Analytics] pour [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) dimensions de création de rapports d’intégration intégrées à Adobe Analytics pour mesurer et visualiser vos données de test avec [!DNL Analytics] mesures et événements de succès.

Consultez les sections suivantes pour connaître les conditions préalables et les instructions de configuration des tests A/B dans [!DNL Target] pour le trafic de clics publicitaires provenant des publicités dans Search, Social et Commerce, ainsi que des conseils sur la mesure et la visualisation de vos tests dans [!DNL Analytics].

## Conditions préalables

### Produits requis

* Recherche, Social et Commerce
* [!DNL Target]

### Produits et intégrations recommandés

* [!DNL Analytics]

* [[!DNL Analytics] pour la publicité](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] pour [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

## Étape 1 : Création d’une activité de test A/B dans [!DNL Target] pour Search, Social et Commerce

Les instructions suivantes présentent des informations relatives au cas d’utilisation de Search, Social et Commerce.

1. [Connexion à Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Création d’un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Dans le **[!UICONTROL Enter Activity URL]** , saisissez l&#39;URL de la landing page pour le test.

   1. Dans le **[!UICONTROL Goal]** , saisissez la mesure de succès du test.

      >[!NOTE]
      >
      >Assurez-vous que [!DNL Analytics] est activé en tant que source de données dans [!DNL Target]et que la suite de rapports correcte est sélectionnée.

   1. Définissez la variable **[!UICONTROL Priority]** to `High` ou `999` afin d’éviter les conflits lorsque les utilisateurs du segment de test reçoivent une expérience sur site incorrecte.


   1. Within **[!UICONTROL Reporting Settings]**, sélectionnez la variable **[!UICONTROL Company Name]** et **[!UICONTROL Report Suite]** Connecté à votre compte Search, Social et Commerce.

      Pour obtenir des conseils supplémentaires sur la création de rapports, voir &quot;[Bonnes pratiques et dépannage de la création de rapports](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. Dans le **[!UICONTROL Date Range]** , saisissez les dates de début et de fin appropriées pour le test.

   1. Sélectionner **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**. Dans le **[!UICONTROL Value]** , saisissez la valeur [!UICONTROL Network Account ID], [!UICONTROL Network Campaign ID], [!UICONTROL Network Adgroup ID], ou [!UICONTROL Network Ad ID] pour l’entité de réseau publicitaire appropriée dans Search, Social et Commerce. Vous pouvez ainsi utiliser la variable [!DNL Target] paramètres de chaîne de requête pour les audiences de clics publicitaires pour l’entité.

      Vous pouvez trouver l’ID en [l’ajout de la colonne d’identifiant appropriée à la vue d’entité ;](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md).

      ![[!UICONTROL Network Account ID] dans la colonne [!UICONTROL Accounts] view](/help/integrations/assets/target-search-id.png "[!UICONTROL Network Account ID] dans la colonne [!UICONTROL Accounts] view")

      Contactez votre équipe de compte d’Adobe si vous avez besoin d’aide.

   1. Pour le **[!UICONTROL Traffic Allocation Method]**, sélectionnez **[!UICONTROL Manual (Default)]** et fractionner l’50/50 de l’audience.

   1. Enregistrez l’activité.

1. Utilisation [Compositeur d’expérience visuelle de Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) pour apporter des modifications de conception au modèle de landing page de test A/B.

   * Expérience A : ne modifiez pas, car il s’agit de l’expérience de page d’entrée par défaut/de contrôle sans personnalisation.

   * Expérience B : utilisez la variable [!DNL Target] interface utilisateur pour personnaliser le modèle de landing page en fonction des ressources incluses dans le test (titres, copie, positionnement des boutons et éléments créatifs, par exemple).

   >[!NOTE]
   >
   >Par exemple, contactez votre équipe de compte d’Adobe pour des cas pratiques de test créatif.

## Étape 2 : configurez votre [!DNL Analytics for Target] Analysis Workspace dans [!DNL Analytics]

[!DNL Analytics for Target] (A4T) est une intégration intersolutions qui permet aux annonceurs de créer des [!DNL Target] activités basées sur [!DNL Analytics] mesures de conversion et segments d’audience, puis mesurer les résultats à l’aide de [!DNL Analytics] comme source des rapports. Toute la création de rapports et la segmentation pour cette activité est basée sur [!DNL Analytics] collecte de données.

Pour plus d’informations sur [!DNL Analytics for Target], y compris un lien vers des instructions de mise en oeuvre, voir &quot;[Adobe Analytics comme source des rapports pour Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configurez la variable [!DNL Analytics for Target] Panneau

Dans Analysis Workspace, configurez la variable [!DNL Analytics for Target panel] pour analyser votre [!DNL Target] activités et expériences. Gardez à l’esprit les recommandations et informations importantes suivantes concernant vos rapports.

#### Mesures

* Créez un panneau dans l’espace de travail spécifique au compte d’Adobe Advertising, à la campagne ou au groupe publicitaire.<!-- only applicable entities? --> pour lequel le test a été exécuté. Utilisez des visualisations récapitulatives pour afficher les mesures d’Adobe Advertising dans le même rapport que la variable [!DNL Target] performance du test.

* Définir la priorité de l’utilisation des mesures sur site (telles que les visites et les conversions) pour mesurer les performances.

* Comprendre que les mesures multimédia agrégées issues de l’Adobe Advertising (telles que les impressions, les clics et les coûts) ne peuvent pas être associées à [!DNL Target] mesures.

#### Dimensions

Les dimensions suivantes se rapportent à [!DNL Analytics for Target]:

* **Activités Target**: nom du test A/B.

* **Expériences Target**: noms des expériences de landing page utilisées dans l’activité

* **Activité Target** > **Expérience**: nom de l’activité et nom de l’expérience dans la même ligne.

### Dépannage d’Analytics pour [!DNL Target] Données

Dans Analysis Workspace, si vous constatez que les données d’activité et d’expérience sont minimales ou ne sont pas renseignées, procédez comme suit :

* Vérifiez que la même [!UICONTROL Supplemental Data ID] (SDID) est utilisé pour les deux [!DNL Target] et [!DNL Analytics]. Vous pouvez vérifier les valeurs du SDID à l’aide de la variable [Débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) sur la page d’entrée sur laquelle la campagne entraîne des utilisateurs.

[Valeurs SDID (Supplemental Data ID) dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Sur la même page d’entrée, vérifiez que a) la variable [!UICONTROL Hostname] affiché dans l’Adobe Debugger sous [!UICONTROL Solutions] > [!UICONTROL Target] correspond à b) la fonction [!UICONTROL Tracking Server] affiché dans [!DNL Target] pour l’activité (sous [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] nécessite une [!DNL Analytics] serveur de suivi à envoyer dans les appels depuis [!DNL Target] à la fonction [!DNL Modstats] serveur de collecte de données pour Analytics.<!-- just "to Analytics?"-->

[Valeur du nom d’hôte dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valeur du serveur de suivi dans Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Autres lectures

* [Intégration de Target à Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Explique comment configurer [!DNL Target] dans Analysis Workspace.
* [Présentation des tests A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Décrit les activités de test A/B que vous pouvez utiliser avec les annonces Search, Social et Commerce.
* [Présentation d’Analytics for Advertising](/help/integrations/analytics/overview.md) - Introduit Analytics for Advertising, qui vous permet d’effectuer le suivi des interactions de site avec les clics publicitaires et les affichages publicitaires dans vos instances Analytics.

>[!MORELIKETHIS]
>
>* [Configuration de tests A/B dans Adobe Target pour les publicités DSP](ab-tests-dsp.md)
