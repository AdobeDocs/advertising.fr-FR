---
title: Configuration de tests A/B pour les publicités Adobe Advertising DSP dans Adobe Target
description: Découvrez comment configurer un test A/B dans  [!DNL Target]  pour vos publicités DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 964246bb2c8bfa442f2d4f981c9e02de35c69ed5
workflow-type: tm+mt
source-wordcount: '1384'
ht-degree: 0%

---

# Configuration de tests A/B dans Adobe Target pour les annonces Advertising DSP

*Annonceurs avec Advertising DSP uniquement*

Adobe Advertising et Adobe Target permettent aux marketeurs de proposer plus facilement une expérience personnalisée et connectée à l’aide de médias payants et de messages sur site. En partageant des signaux entre les produits, vous pouvez :

* Diminuez les taux de chute du site en liant l’exposition publicitaire des clients DSP campagnes à leurs expériences sur site.

* Créez des tests A/B en reflétant les expériences sur site avec les messages publicitaires à l’aide des données d’exposition Adobe Audience Manager et des audiences de clic pour alimenter [!DNL Target].

* Mesurez l’impact de la messagerie unifiée sur un effet élévateur objectif sur site à l’aide de visualisations simples dans Adobe Analytics pour [!DNL Target].

Consultez les sections suivantes pour connaître les conditions préalables et pour obtenir des instructions sur la configuration du suivi des clics publicitaires et des affichages publicitaires, la mise en oeuvre du partage de signal entre DSP et [!DNL Target], la configuration d’une activité de test A/B et la configuration d’Analysis Workspace [!DNL Analytics] pour afficher les données de test.

Si vous avez d’autres questions, contactez adcloud_support@adobe.com.

## Conditions préalables

Ce cas pratique nécessite les produits et intégrations suivants :

* [!DNL Target]

* [[!DNL Analytics] pour l’intégration Advertising](/help/integrations/analytics/overview.md)<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Intégration [[!DNL Analytics] pour [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)

* Audience Manager (requise pour les tests d’affichage publicitaire uniquement)

## Étape 1 : configuration de la structure de clic publicitaire {#click-through-framework}

![Cadre de clic publicitaire](/help/integrations/assets/target-ct-framework.png)

Lorsque vous ajoutez DSP macros à une URL de clic publicitaire (l’URL affichée lorsqu’un utilisateur clique sur une publicité et atteint la page d’entrée), DSP capture automatiquement la clé d’emplacement en incluant `${TM_PLACEMENT_ID}` dans l’URL de clic publicitaire. Cette macro capture la clé d’emplacement alphanumérique et non l’identifiant d’emplacement numérique.

![URL de clic publicitaire ajoutée à l’URL de la page d’entrée](/help/integrations/assets/target-ct-url.jpg)

### (DSP uniquement) Ajout de DSP Macros à vos URL de clic publicitaire

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Dans le cas de Google Campaign Manager 360 ou d’une conversation par Flash, mettez à jour manuellement l’URL du clic publicitaire pour chaque publicité afin d’inclure les macros requises pour capturer les variables AMO ID. Les variables AMO ID sont utilisées pour envoyer des données de clic à Adobe Analytics et pour partager des clés de placement pour les tests A/B. Consultez les pages suivantes pour obtenir des instructions :

* [Ajouter des  [!DNL Analytics for Advertising] macros à [!DNL Flashtalking] balises de publicité](/help/integrations/analytics/macros-flashtalking.md)

* [Ajouter des  [!DNL Analytics for Advertising] macros à [!DNL Google Campaign Manager 360] balises de publicité](/help/integrations/analytics/macros-google-campaign-manager.md)

Contactez votre équipe de compte d’Adobe et le groupe de solutions Advertising (aac-advertising-solutions-group@adobe.com) pour récupérer la clé d’emplacement requise et terminer la configuration, et pour vous assurer que chaque URL de clic publicitaire est renseignée avec la clé d’emplacement.

## Étape 2 : configuration de la structure d’affichage publicitaire avec Audience Manager {#view-through-framework}

![Structure d’affichage publicitaire](/help/integrations/assets/targetr-vt-framework.png)

En ajoutant un pixel d’événement d’impression d’Audience Manager dans vos balises publicitaires et paramètres d’emplacement, vous pouvez créer un segment de test pour d’autres opportunités de test d’affichage publicitaire.

1. Implémentez un pixel d’événement d’impression d’Audience Manager dans vos balises publicitaires et DSP paramètres d’emplacement.

   Pour plus d’informations, voir &quot;[Collecte de données d’exposition multimédia à partir des campagnes Advertising DSP](/help/integrations/audience-manager/media-data-integration/collect.md)&quot;.

   Veillez à ajouter [DSP macros](/help/dsp/campaign-management/macros.md) pour capturer toutes les données que le pixel d’événement d’impression doit transmettre, y compris `${TM_PLACEMENT_ID_NUM}` pour l’ID d’emplacement numérique.

   >[!NOTE]
   >
   >Les URL de suivi des clics incluent la macro `${TM_PLACEMENT_ID}` pour la clé d’emplacement alphanumérique, au lieu de `${TM_PLACEMENT_ID_NUM}` pour l’ID d’emplacement numérique.

1. Configurez un segment d’Audience Manager à partir des données d’impression DSP :

   1. Vérifiez que les données de segment sont disponibles :

      1. [Recherchez le signal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) pour la [paire clé-valeur](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) qui détermine à quel niveau les utilisateurs de segment sont regroupés.

         Utilisez une [clé prise en charge](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) avec une valeur qui correspond à une macro que vous avez ajoutée au pixel d’événement d’impression d’Audience Manager.

         Par exemple, pour regrouper des utilisateurs pour un emplacement particulier, utilisez la clé `d_placement`. Pour la valeur, utilisez un identifiant de placement numérique réel (tel que 2501853) capturé par la macro DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Si les résultats de la recherche indiquent le nombre d’utilisateurs pour la paire clé-valeur, ce qui indique que le pixel a été placé correctement et que les données circulent, passez à l’étape suivante.

   1. [Créez une caractéristique basée sur des règles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) pour la création de segments dans Audience Manager.

      * Nommez la caractéristique afin qu’elle soit facilement identifiable dans les activités de test. Stockez la caractéristique dans le dossier de votre choix.

      * Sélectionnez `Ad Cloud` comme **[!UICONTROL Data Source]**.

      * Pour l’expression de caractéristique, utilisez `d_event` comme **[!UICONTROL Key]** et `imp` comme **[!UICONTROL Value]**.

   1. [Configurez un segment de test](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) pour la nouvelle caractéristique en Audience Manager, en sélectionnant `Ad Cloud` comme **[!UICONTROL Data Source]**.

      L’Audience Manager divise automatiquement le segment en une population témoin qui reçoit l’expérience de page d’entrée standard et un groupe de test qui a reçu une expérience personnalisée sur site.

## Étape 3 : configuration d’une activité de test A/B dans [!DNL Target] pour DSP

Les instructions suivantes présentent des informations relatives au cas d’utilisation DSP.

1. [Connectez-vous à Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Créez un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) :

   1. Dans le champ **[!UICONTROL Enter Activity URL]** , saisissez l’URL de la landing page pour le test.

      >[!NOTE]
      >
      >Vous pouvez utiliser plusieurs URL pour tester l’entrée du site vue publicitaire. Pour plus d’informations, voir &quot;[Activité multi-page](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html)&quot;. Vous pouvez facilement identifier les entrées principales par URL de page en créant un [rapport d’entrée au site](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) dans Analytics.

   1. Dans le champ **[!UICONTROL Goal]** , saisissez la mesure de succès du test.

      >[!NOTE]
      >
      >Assurez-vous que [!DNL Analytics] est activé en tant que source de données dans [!DNL Target] et que la suite de rapports correcte est sélectionnée.

   1. Définissez **[!UICONTROL Priority]** sur `High` ou `999` pour éviter les conflits lorsque les utilisateurs du segment de test reçoivent une expérience sur site incorrecte.

   1. Dans **[!UICONTROL Reporting Settings]**, sélectionnez les **[!UICONTROL Company Name]** et **[!UICONTROL Report Suite]** connectés à votre compte DSP.

      Pour obtenir des conseils supplémentaires sur la création de rapports, voir &quot;[Bonnes pratiques en matière de création de rapports et résolution des problèmes](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html)&quot;.

   1. Dans le champ **[!UICONTROL Date Range]** , saisissez les dates de début et de fin appropriées pour le test.

   1. Ajoutez des audiences à l’activité :

      1. Sélectionnez le segment [que vous avez créé précédemment en Audience Manager pour tester les audiences d’affichage publicitaire](#view-through-framework).

      1. Sélectionnez **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]** et saisissez la clé de placement DSP dans le champ **[!UICONTROL Value]** afin d’utiliser les paramètres de chaîne de requête Target pour les audiences de clics publicitaires.

   1. Pour le **[!UICONTROL Traffic Allocation Method]**, sélectionnez **[!UICONTROL Manual (Default)]** et divisez l’audience 50/50.

   1. Enregistrez l’activité.

1. Utilisez [le compositeur d’expérience visuelle de Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) pour apporter des modifications de conception au modèle de page d’entrée de test A/B.

   * Expérience A : ne modifiez pas, car il s’agit de l’expérience de page d’entrée par défaut/de contrôle sans personnalisation.

   * Expérience B : utilisez l’interface utilisateur [!DNL Target] pour personnaliser le modèle de page d’entrée en fonction des ressources incluses dans le test (comme les titres, la copie, le positionnement des boutons et les éléments créatifs).

   >[!NOTE]
   >
   >Par exemple, contactez votre équipe de compte d’Adobe pour des cas pratiques de test créatif.

## Étape 4 : configuration de votre [!DNL Analytics for Target] Analysis Workspace dans [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) est une intégration intersolutions qui permet aux annonceurs de créer des activités [!DNL Target] basées sur [!DNL Analytics] mesures de conversion et segments d’audience, puis de mesurer les résultats à l’aide de [!DNL Analytics] comme source de création de rapports. Tous les rapports et segmentation pour cette activité sont basés sur la collecte de données [!DNL Analytics].

Pour plus d’informations sur [!DNL Analytics for Target], y compris un lien vers les instructions de mise en oeuvre, voir &quot;[Adobe Analytics as a reporting source for Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configuration du panneau [!DNL Analytics for Target]

Dans Analysis Workspace, configurez le [!DNL Analytics for Target panel] pour analyser vos activités et expériences [!DNL Target]. Gardez à l’esprit les recommandations et informations importantes suivantes concernant vos rapports.

#### Mesures

* Créez un panneau dans l’espace de travail spécifique à la campagne d’Adobe Advertising, au package ou à l’emplacement pour lequel le test a été exécuté. Utilisez des visualisations récapitulatives pour afficher les mesures d’Adobe Advertising dans le même rapport que les performances du test [!DNL Target].

* Définir la priorité de l’utilisation des mesures sur site (telles que les visites et les conversions) pour mesurer les performances.

* Comprenez que les mesures multimédia agrégées provenant de l’Adobe Advertising (telles que les impressions, les clics et les coûts) ne peuvent pas être associées aux mesures [!DNL Target].

#### Dimensions

Les dimensions suivantes se rapportent à [!DNL Analytics for Target] :

* **[!UICONTROL Target Activities]** : nom du test A/B

* **[!UICONTROL Target Experiences]** : noms des expériences de landing page utilisées dans l’activité

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]** : nom de l’activité et nom de l’expérience dans la même ligne

### Dépannage d’Analytics pour les données [!DNL Target]

Dans Analysis Workspace, si vous constatez que les données d’activité et d’expérience sont minimales ou ne sont pas renseignées, procédez comme suit :

* Vérifiez que le même [!UICONTROL Supplemental Data ID] (SDID) est utilisé pour [!DNL Target] et [!DNL Analytics]. Vous pouvez vérifier les valeurs du SDID à l’aide du [débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) sur la page d’entrée vers laquelle la campagne dirige les utilisateurs.

[Valeurs SDID (Supplemental Data ID) dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Sur la même page d’entrée, vérifiez que a) le [!UICONTROL Hostname] affiché dans l’Adobe Debugger sous [!UICONTROL Solutions] > [!UICONTROL Target] correspond à b) le [!UICONTROL Tracking Server] affiché dans [!DNL Target] pour l’activité (sous [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] nécessite qu’un serveur de suivi [!DNL Analytics] soit envoyé dans les appels de [!DNL Target] au serveur de collecte de données [!DNL Modstats] pour Analytics.<!-- just "to Analytics?"-->

[Valeur du nom d’hôte dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valeur du serveur de suivi dans Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Autres lectures

* [Intégrer Target avec Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Explique comment configurer la création de rapports [!DNL Target] dans Analysis Workspace.
* [Présentation du test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Décrit les activités de test A/B que vous pouvez utiliser avec DSP publicités.
* [Expériences et offres](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explique [!DNL Target] outils permettant de déterminer le contenu sur site auquel DSP utilisateurs de test sont exposés.
* [Signaux, caractéristiques et segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Définit certains des outils d’Audience Manager qui peuvent vous aider à effectuer DSP test d’affichage.
* [Présentation d’Analytics pour Advertising](/help/integrations/analytics/overview.md) - Introduit Analytics pour Advertising, qui vous permet d’effectuer le suivi des clics publicitaires et des interactions de site d’affichage publicitaire dans vos instances Analytics.

>[!MORELIKETHIS]
>
>* [Configuration de tests A/B dans Adobe Target pour Advertising Search, Social et Commerce Ads](ab-tests-search.md)
