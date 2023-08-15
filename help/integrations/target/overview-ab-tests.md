---
title: Configuration de tests A/B pour les publicités Adobe Advertising dans Adobe Target
description: Découvrez comment configurer un test A/B dans [!DNL Target] pour vos publicités DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: 1dbe8da7122b38dd11a242c453d71a832b31eee8
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# Configuration de tests A/B dans Adobe Target pour les publicités DSP

<!-- In title and Heading1:  DSP and [!DNL Advertising Search, Social, & Commerce] Ads -->

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Publicitaires avec DSP Advertising uniquement*

Adobe Advertising et Adobe Target permettent aux marketeurs de proposer plus facilement une expérience personnalisée et connectée à l’aide de médias payants et de messages sur site. En partageant des signaux entre les produits, vous pouvez :

* Diminuez les taux de chute du site en liant l’exposition publicitaire des clients DSP campagnes à leurs expériences sur site.

* Créez des tests A/B en mettant en miroir les expériences sur site avec les messages publicitaires à l’aide des données d’exposition Adobe Audience Manager et des audiences Target cliquer pour alimenter.

* Mesurez l’impact de la messagerie unifiée sur un effet élévateur objectif sur site à l’aide de visualisations simples dans Adobe Analytics pour [!DNL Target].

Consultez les sections suivantes pour connaître les conditions préalables et pour obtenir des instructions sur la configuration du suivi des clics publicitaires et des affichages publicitaires, implémenter le partage de signal entre DSP et [!DNL Target] et configurer une activité de test A/B, puis [!DNL Analytics] Analysis Workspace pour afficher les données de test.

Si vous avez d’autres questions, contactez adcloud_support@adobe.com.

## Conditions préalables

Ce cas pratique nécessite les produits et intégrations suivants :

* [!DNL Target]

* [[!DNL Analytics] pour la publicité](/help/integrations/analytics/overview.md) integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] pour [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integration

* Audience Manager (requise pour les tests d’affichage publicitaire uniquement)

## Étape 1 : configuration de la structure de clic publicitaire {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Structure du clic publicitaire](/help/integrations/assets/target-ct-framework.png)

Lorsque vous ajoutez DSP macros à une URL de clic publicitaire (l’URL affichée lorsqu’un utilisateur clique sur une publicité et atteint la page d’entrée), DSP capture automatiquement la clé d’emplacement en incluant `${TM_PLACEMENT_ID}` dans l’URL du clic publicitaire. Cette macro capture la clé d’emplacement alphanumérique et non l’identifiant d’emplacement numérique.

![URL de clic publicitaire ajoutée à l’URL de la page d’entrée](/help/integrations/assets/target-ct-url.jpg)

### (DSP uniquement) Ajout de DSP Macros à vos URL de clic publicitaire

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Dans le cas de Google Campaign Manager 360 ou d’une conversation par Flash, mettez à jour manuellement l’URL du clic publicitaire pour chaque publicité afin d’inclure les macros requises pour capturer les variables AMO ID. Les variables AMO ID sont utilisées pour envoyer des données de clic à Adobe Analytics et pour partager des clés de placement pour les tests A/B. Consultez les pages suivantes pour obtenir des instructions :

* [Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Flashtalking] Balises publicitaires](/help/integrations/analytics/macros-flashtalking.md)

* [Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Google Campaign Manager 360] Balises publicitaires](/help/integrations/analytics/macros-google-campaign-manager.md)

Contactez votre équipe de compte d’Adobe et le groupe de solutions Advertising (aac-advertising-solutions-group@adobe.com) pour récupérer la clé d’emplacement requise et finaliser la configuration, et pour vous assurer que chaque URL de clic publicitaire est renseignée avec la clé d’emplacement.

## Étape 2 : configuration de la structure d’affichage publicitaire avec Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Structure d’affichage publicitaire](/help/integrations/assets/targetr-vt-framework.png)

En ajoutant un pixel d’événement d’impression d’Audience Manager dans vos balises publicitaires et paramètres d’emplacement, vous pouvez créer un segment de test pour d’autres opportunités de test d’affichage publicitaire.

1. Implémentez un pixel d’événement d’impression d’Audience Manager dans vos balises publicitaires et DSP paramètres d’emplacement.

   Pour obtenir des instructions, voir &quot;[Collecte de données Media Exposure à partir de campagnes Advertising DSP](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Veillez à ajouter [Macros DSP](/help/dsp/campaign-management/macros.md) pour capturer toutes les données que le pixel d’événement d’impression doit transmettre, y compris `${TM_PLACEMENT_ID_NUM}` pour l’identifiant d’emplacement numérique.

   >[!NOTE]
   >
   >Les URL de suivi des clics incluent la variable `${TM_PLACEMENT_ID}` pour la clé d’emplacement alphanumérique, au lieu de `${TM_PLACEMENT_ID_NUM}` pour l’identifiant d’emplacement numérique.

1. Configurez un segment d’Audience Manager à partir des données d’impression DSP :

   1. Vérifiez que les données de segment sont disponibles :

      1. [Recherche du signal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) pour le [paire clé-valeur](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) qui détermine à quel niveau les utilisateurs du segment sont regroupés.

         Utilisez une [clé prise en charge](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) avec une valeur qui correspond à une macro que vous avez ajoutée au pixel d’événement d’impression d’Audience Manager.

         Par exemple, pour regrouper des utilisateurs pour un emplacement spécifique, utilisez la variable `d_placement` clé. Pour la valeur , utilisez un identifiant d’emplacement numérique réel (2501853, par exemple) capturé par la macro DSP `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Si les résultats de la recherche indiquent le nombre d’utilisateurs pour la paire clé-valeur, ce qui indique que le pixel a été placé correctement et que les données circulent, passez à l’étape suivante.

   1. [Création d’une caractéristique basée sur des règles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) pour la création de segments dans Audience Manager.

      * Nommez la caractéristique afin qu’elle soit facilement identifiable dans les activités de test. Stockez la caractéristique dans le dossier de votre choix.

      * Sélectionner `Ad Cloud` comme la propriété **Source de données**.

      * Pour l’expression de caractéristique, utilisez `d_event` comme la propriété **Clé** et `imp` comme la propriété **Valeur**.

   1. [Configurer un segment de test](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) pour la nouvelle caractéristique en Audience Manager, en sélectionnant `Ad Cloud` comme la propriété **Source de données**.

      L’Audience Manager divise automatiquement le segment en une population témoin qui reçoit l’expérience de page d’entrée standard et un groupe de test qui a reçu une expérience personnalisée sur site.

## Étape 3 : configuration d’une activité de &quot;test A/B&quot; dans Target

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

Les instructions suivantes présentent des informations relatives au cas d’utilisation DSP. Pour obtenir des instructions complètes, voir &quot;&quot;.

1. [Connexion à Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Création d’un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html):

   1. Dans le **Entrée dans l’URL d’activité** , saisissez l&#39;URL de la landing page pour le test.

      >[!NOTE]
      >
      >Vous pouvez utiliser plusieurs URL pour tester l’entrée du site vue publicitaire. Pour plus d’informations, voir &quot;[Activité multi-page](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Vous pouvez facilement identifier les entrées principales par URL de page en créant un [Rapport Entrée de site](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) dans Analytics.

   1. Dans le **Objectif** , saisissez la mesure de succès du test.

      >[!NOTE]
      >
      >Assurez-vous que [!DNL Analytics] est activé en tant que source de données dans [!DNL Target]et que la suite de rapports correcte est sélectionnée.

   1. Définissez la variable **Priorité** to `High` ou `999` afin d’éviter les conflits lorsque les utilisateurs du segment de test reçoivent une expérience sur site incorrecte.

   1. Within **Paramètres de création de rapports**, sélectionnez la variable **Nom de la société** et **Suite de rapports** connecté à votre compte DSP.

      Pour obtenir des conseils supplémentaires sur la création de rapports, voir &quot;[Bonnes pratiques et dépannage de la création de rapports](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

   1. Dans le **Période** , saisissez les dates de début et de fin appropriées pour le test.

   1. Ajoutez des audiences à l’activité :

      1. Choisissez la [segment précédemment créé en Audience Manager pour tester les audiences d’affichage publicitaire](#view-through-framework).

      1. Sélectionner **Pages du site** > **Page d’entrée** > **Requête**, puis saisissez la clé de placement DSP dans le champ **Valeur** pour utiliser les paramètres de chaîne de requête Target pour les audiences de clics publicitaires.

   1. Pour le **Méthode d’affectation du trafic**, sélectionnez **Manuel (par défaut)** et fractionner l’50/50 de l’audience.

   1. Enregistrez l’activité.

1. Utilisation [!DNL Target] [Compositeur d’expérience visuelle](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) pour apporter des modifications de conception au modèle de landing page de test A/B.

   * Expérience A : ne modifiez pas, car il s’agit de l’expérience de page d’entrée par défaut/de contrôle sans personnalisation.

   * Expérience B : utilisez la variable [!DNL Target] interface utilisateur pour personnaliser le modèle de landing page en fonction des ressources incluses dans le test (titres, copie, positionnement des boutons et éléments créatifs, par exemple).

   >[!NOTE]
   >
   >Par exemple, contactez votre équipe de compte d’Adobe pour des cas pratiques de test créatif.

## Étape 4 : configurez votre [!DNL Analytics for Target] Analysis Workspace dans [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) est une intégration intersolutions qui permet aux annonceurs de créer des [!DNL Target] activités basées sur [!DNL Analytics] mesures de conversion et segments d’audience, puis mesurer les résultats à l’aide de [!DNL Analytics] comme source des rapports. Toute la création de rapports et la segmentation pour cette activité est basée sur [!DNL Analytics] collecte de données.

Pour plus d’informations sur [!DNL Analytics for Target], y compris un lien vers des instructions de mise en oeuvre, voir &quot;[Adobe Analytics comme source des rapports pour Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Configurez la variable [!DNL Analytics for Target] Panneau

Dans Analysis Workspace, configurez la variable [!DNL Analytics for Target panel] pour analyser votre [!DNL Target] activités et expériences. Gardez à l’esprit les recommandations et informations importantes suivantes concernant vos rapports.

#### Mesures

* Créez un panneau dans l’espace de travail spécifique à la campagne d’Adobe Advertising, au package ou à l’emplacement pour lequel le test a été exécuté. Utilisez des visualisations récapitulatives pour afficher les mesures d’Adobe Advertising dans le même rapport que les performances du test Target.

* Définir la priorité de l’utilisation des mesures sur site (telles que les visites et les conversions) pour mesurer les performances.

* Comprenez que les mesures multimédia agrégées provenant d’Adobe Advertising (telles que les impressions, les clics et les coûts) ne peuvent pas être associées aux mesures Target.

#### Dimensions

Les dimensions suivantes se rapportent à [!DNL Analytics for Target]:

* **Activités Target**: nom du test A/B.

* **Expériences Target**: noms des expériences de landing page utilisées dans l’activité

* **Activité Target** > **Expérience**: nom de l’activité et nom de l’expérience dans la même ligne.

### Dépannage d’Analytics pour [!DNL Target] Données

Dans Analysis Workspace, si vous constatez que les données d’activité et d’expérience sont minimales ou ne sont pas renseignées, procédez comme suit :

* Vérifiez que le même SDID (Supplemental Data ID) est utilisé pour Target et Analytics. Vous pouvez vérifier les valeurs du SDID à l’aide de la variable [Débogueur Adobe Experience Cloud](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) sur la page d’entrée sur laquelle la campagne entraîne des utilisateurs.

[Valeurs SDID (Supplemental Data ID) dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Sur la même page d’entrée, vérifiez que a) le nom d’hôte affiché dans l’Adobe Debugger sous Solutions> Target correspond à b) le serveur de suivi affiché dans [!DNL Target] pour l’activité (sous Objectifs et paramètres > Paramètres de création de rapports).

  [!DNL Analytics For Target] nécessite une [!DNL Analytics] serveur de suivi à envoyer dans les appels depuis [!DNL Target] à la fonction [!DNL Modstats] serveur de collecte de données pour Analytics.<!-- just "to Analytics?"-->

[Valeur du nom d’hôte dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valeur du serveur de suivi dans Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Autres lectures

* [Intégration de Target à Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Explique comment configurer les rapports Target dans Analysis Workspace.
* [Présentation des tests A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Décrit les activités de test A/B que vous pouvez utiliser avec DSP publicités.
* [Offres et expériences](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Expressions [!DNL Target] outils permettant de déterminer le contenu sur site auquel DSP utilisateurs de test sont exposés.
* [Signaux, caractéristiques et segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Définit certains des outils d’Audience Manager qui peuvent vous aider à DSP les tests d’affichage publicitaire.
* [Présentation d’Analytics for Advertising](/help/integrations/analytics/overview.md) - Introduit Analytics for Advertising, qui vous permet d’effectuer le suivi des interactions de site avec les clics publicitaires et les affichages publicitaires dans vos instances Analytics.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
