---
title: Configuration de tests A/B pour Adobe Advertising DSP Ads dans Adobe Target
description: Découvrez comment configurer un test A/B dans  [!DNL Target]  pour vos publicités DSP.
exl-id: 5092e06b-eef0-43f3-ba81-6dbe7164158c
source-git-commit: a69bef9d249514f5c494cff8d706b9df792eaf23
workflow-type: tm+mt
source-wordcount: '1413'
ht-degree: 0%

---

# Configuration de tests A/B dans Adobe Target pour Advertising DSP Ads

*Annonceurs avec Advertising DSP uniquement*

Adobe Advertising et Adobe Target permettent aux marketeurs de fournir encore plus facilement une expérience personnalisée et connectée sur les médias achetés et la messagerie sur site. En partageant des signaux entre les produits, vous pouvez :

* Réduisez les taux de chute sur le site en liant l’exposition des clients aux annonces des campagnes DSP à leurs expériences sur site.

* Établissez des tests A/B en reflétant les expériences sur site avec les messages publicitaires à l’aide des données d’exposition Adobe Audience Manager et des audiences de [!DNL Target] de clics publicitaires.

* Mesurez l’impact de la messagerie unifiée sur un effet élévateur d’objectifs sur site avec des visualisations simples dans Adobe Analytics for [!DNL Target].

Consultez les sections suivantes pour connaître les conditions préalables et les instructions permettant de configurer le suivi des clics publicitaires et des affichages publicitaires, d’implémenter le partage de signaux entre DSP et [!DNL Target] et de configurer une activité de test A/B, ainsi que de configurer [!DNL Analytics]’Analysis Workspace pour afficher les données de test.

Si vous avez d’autres questions, contactez adcloud_support@adobe.com.

## Conditions préalables

Ce cas d’utilisation nécessite les produits et intégrations suivants :

* [!DNL Target]

* [[!DNL Analytics] pour Advertising](/help/integrations/analytics/overview.md) intégration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* Intégration [[!DNL Analytics] for [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)

* Audience Manager (requis pour les tests d’affichage publicitaire uniquement)

## Étape 1 : configurer le framework de clic publicitaire {#click-through-framework}

![Framework de clic publicitaire](/help/integrations/assets/target-ct-framework.png)

Lorsque vous ajoutez des macros DSP à une URL de clic publicitaire (l’URL affichée lorsqu’un utilisateur clique sur une annonce et atteint la page de destination), DSP capture automatiquement la clé d’emplacement en incluant `${TM_PLACEMENT_ID}` dans l’URL de clic publicitaire. Cette macro capture la clé d’emplacement alphanumérique et non l’identifiant d’emplacement numérique.

![URL de clic publicitaire ajoutée à l’URL de la page de destination](/help/integrations/assets/target-ct-url.jpg)

### (DSP uniquement) Ajouter des macros DSP à vos URL de clics publicitaires

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Dans [!DNL Flashtalking] ou Google Campaign Manager 360, mettez manuellement à jour l’URL de clic publicitaire pour chaque publicité afin d’inclure les macros requises pour capturer les variables d’ID AMO. Les variables d’ID AMO sont utilisées pour envoyer des données de clic à Adobe Analytics et partager des clés d’emplacement pour les tests A/B. Consultez les pages suivantes pour obtenir des instructions :

* [Ajouter [!DNL Analytics for Advertising] des macros aux balises  [!DNL Flashtalking] ’annonces](/help/integrations/analytics/macros-flashtalking.md). **Remarque :** cette procédure n’est pas nécessaire si votre entreprise entretient un partenariat direct avec [!DNL Flashtalking] et que vous utilisez des macros de transfert de données pour effectuer le suivi des paramètres de suivi `s_kwcid` et `ef_id` conformément à la documentation d’assistance [!DNL Flashtalking] à l’adresse [https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros).

* [Ajouter [!DNL Analytics for Advertising] des macros à des balises  [!DNL Google Campaign Manager 360] ’annonces](/help/integrations/analytics/macros-google-campaign-manager.md)

Contactez l’équipe chargée de votre compte Adobe et le groupe de solutions Advertising (aac-advertising-solutions-group@adobe.com) pour récupérer la clé d’emplacement requise, finaliser la configuration et vous assurer que chaque URL de clic publicitaire est renseignée avec la clé d’emplacement.

## Étape 2 : configurer la structure d’affichage publicitaire à l’aide d’Audience Manager {#view-through-framework}

![Structure des vues publicitaires](/help/integrations/assets/targetr-vt-framework.png)

En ajoutant un pixel d’événement d’impression Audience Manager à vos balises d’annonces et paramètres d’emplacement, vous pouvez créer un segment de test pour d’autres opportunités de test d’affichage publicitaire.

1. Implémentez un pixel d’événement d’impression Audience Manager dans vos balises d’annonces publicitaires et paramètres d’emplacement DSP.

   Pour obtenir des instructions, reportez-vous à « [Collecter des données d’exposition des médias à partir de campagnes Advertising DSP](/help/integrations/audience-manager/media-data-integration/collect.md) ».

   Veillez à ajouter [des macros DSP](/help/dsp/campaign-management/macros.md) pour capturer toutes les données que le pixel d&#39;événement d&#39;impression doit renvoyer, y compris les `${TM_PLACEMENT_ID_NUM}` de l&#39;identifiant d&#39;emplacement numérique.

   >[!NOTE]
   >
   >Les URL de suivi des clics incluent la macro `${TM_PLACEMENT_ID}` pour la clé d’emplacement alphanumérique, au lieu de `${TM_PLACEMENT_ID_NUM}` pour l’ID d’emplacement numérique.

1. Configurez un segment Audience Manager à partir des données d’impression DSP :

   1. Vérifiez que les données de segment sont disponibles :

      1. [Recherchez le signal](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-signals-search.html) pour la [paire clé-valeur](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-explorer/signals-search/data-explorer-search-pairs.html) qui détermine à quel niveau les utilisateurs du segment sont regroupés.

         Utilisez une [clé prise en charge](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html) avec une valeur correspondant à une macro que vous avez ajoutée au pixel d’événement d’impression Audience Manager.

         Par exemple, pour regrouper des utilisateurs pour un emplacement spécifique, utilisez la touche `d_placement` . Pour la valeur, utilisez un identifiant d&#39;emplacement numérique réel (tel que 2501853) capturé par le `${TM_PLACEMENT_ID_NUM}` de macro DSP. <!-- Explain where to find the placement ID, other than in a custom report. -->

         Si les résultats de la recherche affichent le nombre d’utilisateurs pour la paire clé-valeur, ce qui indique que le pixel a été placé correctement et que les données circulent, passez à l’étape suivante.

   1. [Créer une caractéristique basée sur des règles](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) pour la création de segments dans Audience Manager.

      * Nommez la caractéristique afin qu’elle soit facilement identifiable dans les activités de test. Stockez la caractéristique dans le dossier de votre choix.

      * Sélectionnez `Ad Cloud` comme **[!UICONTROL Data Source]**.

      * Pour l’expression de la caractéristique, utilisez `d_event` comme **[!UICONTROL Key]** et `imp` comme **[!UICONTROL Value]**.

   1. [Configurer un segment de test](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segment-builder.html) pour la nouvelle caractéristique dans Audience Manager, en sélectionnant `Ad Cloud` comme **[!UICONTROL Data Source]**.

      Audience Manager divise automatiquement le segment en une population témoin qui reçoit l’expérience standard de la page de destination et une population test qui reçoit une expérience personnalisée sur site.

## Étape 3 : Configurer une activité de test A/B dans [!DNL Target] pour DSP

Les instructions suivantes mettent en évidence les informations relatives au cas d’utilisation de DSP.

1. [Connexion à Adobe Target](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. [Créer un test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) :

   1. Dans le champ **[!UICONTROL Enter Activity URL]** , saisissez l’URL de la page de destination pour le test.

      >[!NOTE]
      >
      >Vous pouvez utiliser plusieurs URL pour tester l’entrée de site en mode affichage publicitaire. Pour plus d’informations, voir « [Activité multipage](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html) ». Vous pouvez facilement identifier les entrées principales par URL de page en créant un [rapport d’entrée de site](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/integrations/adobe-advertising-dsp/create-advertising-cloud-site-entry-reports) dans Analytics.

   1. Dans le champ **[!UICONTROL Goal]** , saisissez la mesure de succès du test.

      >[!NOTE]
      >
      >Assurez-vous que [!DNL Analytics] est activé en tant que source de données dans [!DNL Target] et que la suite de rapports appropriée est sélectionnée.

   1. Définissez la **[!UICONTROL Priority]** sur `High` ou `999` pour éviter les conflits lorsque les utilisateurs et utilisatrices du segment de test reçoivent une expérience sur site incorrecte.

   1. Dans **[!UICONTROL Reporting Settings]**, sélectionnez les **[!UICONTROL Company Name]** et **[!UICONTROL Report Suite]** connectés à votre compte DSP.

      Pour obtenir des conseils supplémentaires sur les rapports, voir « [Bonnes pratiques et dépannage en matière de rapports](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html) ».

   1. Dans le champ **[!UICONTROL Date Range]** , saisissez les dates de début et de fin appropriées pour le test.

   1. Ajoutez des audiences à l’activité :

      1. Choisissez le [segment que vous avez précédemment créé dans Audience Manager pour tester les audiences de visionnage publicitaire](#view-through-framework).

      1. Sélectionnez **[!UICONTROL Site Pages]** > **[!UICONTROL Landing Page]** > **[!UICONTROL Query]**, puis saisissez la clé d’emplacement DSP dans le champ **[!UICONTROL Value]** pour utiliser les paramètres de chaîne de requête Target pour les audiences de clics publicitaires.

   1. Pour l’**[!UICONTROL Traffic Allocation Method]**, sélectionnez **[!UICONTROL Manual (Default)]** et divisez l’audience 50/50.

   1. Enregistrez l’activité.

1. Utilisez le [compositeur d’expérience visuelle Target](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) pour apporter des modifications de conception au modèle de page de destination du test A/B.

   * Expérience A : ne pas modifier, car il s’agit de l’expérience de page de destination par défaut/de contrôle sans personnalisation.

   * Expérience B : utilisez l’interface utilisateur [!DNL Target] pour personnaliser le modèle de page de destination en fonction des ressources incluses dans le test (telles que les titres, la copie, l’emplacement du bouton et les éléments créatifs).

   >[!NOTE]
   >
   >Pour des cas d’utilisation de test créatif, contactez l’équipe chargée de votre compte Adobe.

## Étape 4 : Configurer votre [!DNL Analytics for Target] Analysis Workspace dans [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) est une intégration intersolutions qui permet aux annonceurs de créer des activités [!DNL Target] basées sur des mesures de conversion [!DNL Analytics] et des segments d’audience, puis de mesurer les résultats à l’aide de [!DNL Analytics] comme source de création de rapports. Toutes les créations de rapports et segmentations pour cette activité sont basées sur la collecte de données [!DNL Analytics].

Pour plus d’informations sur [!DNL Analytics for Target], y compris un lien vers des instructions d’implémentation, consultez « [Adobe Analytics comme source de création de rapports pour Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) ».

### Configurer le panneau [!DNL Analytics for Target]

Dans Analysis Workspace, configurez l’[!DNL Analytics for Target panel] pour analyser vos activités et expériences [!DNL Target]. Gardez à l’esprit les informations et conseils importants suivants concernant vos rapports.

#### Mesures

* Créez un panneau dans l’espace de travail spécifique à la campagne, au package ou à l’emplacement Adobe Advertising pour lequel le test a été exécuté. Utilisez des visualisations de synthèse pour afficher les mesures Adobe Advertising dans le même rapport que les performances du test [!DNL Target].

* Établissez la priorité en utilisant les mesures sur site (telles que les visites et les conversions) pour mesurer les performances.

* Sachez que les mesures multimédia agrégées d’Adobe Advertising (telles que les impressions, les clics et les coûts) ne peuvent pas être mises en correspondance avec les mesures [!DNL Target].

#### Dimensions

Les dimensions suivantes se rapportent aux [!DNL Analytics for Target] :

* **[!UICONTROL Target Activities]** : nom du test A/B

* **[!UICONTROL Target Experiences]** : noms des expériences de page de destination utilisées dans l’activité

* **[!UICONTROL Target Activity]** > **[!UICONTROL Experience]** : nom de l’activité et nom de l’expérience sur la même ligne

### Dépannage d’Analytics for [!DNL Target] Data

Dans Analysis Workspace, si vous constatez que les données d’activité et d’expérience sont minimales ou ne sont pas renseignées, procédez comme suit :

* Vérifiez que le même [!UICONTROL Supplemental Data ID] (SDID) est utilisé pour les [!DNL Target] et les [!DNL Analytics]. Vous pouvez vérifier les valeurs du SDID à l’aide du débogueur Adobe Experience Cloud [&#128279;](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) sur la page de destination vers laquelle la campagne dirige les utilisateurs.

[Valeurs de SDID (Supplemental Data ID) dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Sur la même page de destination, vérifiez que a) le [!UICONTROL Hostname] affiché dans Adobe Debugger sous [!UICONTROL Solutions] > [!UICONTROL Target] correspond à b) le [!UICONTROL Tracking Server] affiché dans [!DNL Target] pour l’activité (sous [!UICONTROL Goals & Settings] > [!UICONTROL Reporting Settings]).

  [!DNL Analytics For Target] nécessite l’envoi d’un serveur de suivi [!DNL Analytics] dans les appels de [!DNL Target] vers le serveur de collecte de données [!DNL Modstats] pour Analytics.<!-- just "to Analytics?"-->

[Valeur du nom d’hôte dans Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Valeur du serveur de suivi dans Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Informations complémentaires

* [Intégrer Target à Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html) - Explique comment configurer le reporting [!DNL Target] dans Analysis Workspace.
* [Présentation du test A/B](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Décrit les activités de test A/B que vous pouvez utiliser avec les publicités DSP.
* [Expériences et offres](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Explique [!DNL Target] outils permettant de déterminer le contenu sur site auquel sont exposés les utilisateurs et utilisatrices du test DSP.
* [Signaux, caractéristiques et segments](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Définit certains des outils Audience Manager qui peuvent vous aider dans les tests d’affichage publicitaire de DSP.
* [Présentation d’Analytics pour Advertising ](/help/integrations/analytics/overview.md) - Introduit Analytics pour Advertising, qui vous permet d’effectuer le suivi des interactions de site de clics publicitaires et de vues publicitaires dans vos instances Analytics.

>[!MORELIKETHIS]
>
>* [Configuration des tests A/B dans Adobe Target pour Advertising Search, Social et Commerce Ads](ab-tests-search.md)
