---
title: Objectifs personnalisés
description: Découvrez les objectifs personnalisés pour définir vos événements de succès dans des packages optimisés pour la CPA la plus faible ou le retour sur dépenses publicitaires le plus élevé.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '1189'
ht-degree: 0%

---

# Objectifs personnalisés

Les objectifs personnalisés définissent les événements de succès dont un annonceur a besoin pour atteindre ses objectifs commerciaux. Chaque package qui utilise l’objectif d’optimisation « [!UICONTROL Highest Return on Ad Spend (ROAS)"] » ou « [!UICONTROL Lowest Cost per Acquisition (CPA)] » doit inclure un objectif personnalisé pour faciliter l’atteinte de l’objectif d’optimisation global. Vous pouvez créer des objectifs personnalisés sous la forme d’*objectifs* dans [!DNL Advertising Search, Social, & Commerce]. Le nom de chaque objectif pour DSP doit comporter le préfixe « ADSP_ ».

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Chaque objectif personnalisé se compose d’une ou de plusieurs mesures de conversion et des poids relatifs de ces mesures. Les mesures de conversion disponibles incluent toutes les mesures suivies à l’aide du pixel de conversion d’Adobe Advertising et via Adobe Analytics. Seuls les poids non mobiles sont pris en compte pour les objectifs personnalisés de DSP, mais ils sont utilisés pour tous les types d’annonces.

Supposons, par exemple, que trois mesures de conversion soient pertinentes pour un package spécifique dans l’une de vos campagnes : « Téléchargement PDF » évalué à 20 USD, « Inscription par e-mail » évalué à 30 USD et « Confirmation de commande » évalué à 40 USD. Si vous souhaitez donner un poids en fonction de la valeur monétaire unique de l’action du client, les poids relatifs des mesures sont 1, 1,5 et 2.

Une fois que vous avez [créé un objectif personnalisé](#custom-goal-create), vous pouvez [l’affecter à un package](/help/dsp/campaign-management/packages/package-settings.md) pour la création de rapports et l’optimisation algorithmique à l’aide de [!DNL Adobe AI].

Les recommandations de poids sont automatiquement générées pour les mesures attribuées à DSP dans les objectifs et peuvent appliquer toutes les recommandations de poids en un seul clic. Toutes les modifications de poids apportées aux objectifs précédés du préfixe « ADSP_ » sont appliquées de manière algorithmique dans DSP dans les deux jours. Pour plus d’informations sur les recommandations de poids, consultez le chapitre du guide d’optimisation intitulé « Objectifs », disponible dans Search, Social et Commerce.

## Créer un objectif personnalisé {#custom-goal-create}

Pour créer un objectif personnalisé, le compte DSP doit être lié à un compte [!DNL Search, Social, & Commerce] avec le même ID d’organisation Adobe Experience Cloud, depuis les paramètres du client [!DNL Search, Social, & Commerce]. Si votre compte DSP n’est pas lié à un compte [!DNL Search, Social, & Commerce], contactez l’équipe chargée de votre compte Adobe.

1. [Connexion à Advertising Search, Social et Commerce](/help/search-social-commerce/getting-started/sign-in.md){target="_blank"}.

1. Assurez-vous que les mesures que vous souhaitez inclure dans votre objectif ont fait l’objet d’un suivi, sont disponibles dans le produit et incluent un nom d’affichage :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]** > **[!UICONTROL Conversions]**.

      La vue Conversions s’ouvre dans un nouvel onglet du navigateur.

   1. Recherchez la mesure et assurez-vous que **[!UICONTROL Show in UI and Reports]** est activé pour la mesure.

      >[!NOTE]
      >
      >* [!DNL Analytics] événements personnalisés suivent cette convention d’affectation des noms : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid`

   1. Si la mesure ne comporte pas de valeur dans la colonne **[!UICONTROL Display Name]**, cliquez dans la cellule, saisissez le nom d’affichage, puis cliquez sur **[!UICONTROL Apply].**

1. [Créez l’objectif personnalisé comme *objectif*](/help/search-social-commerce/new-ui/goals/objectives/objective-create.md){target="_blank"}. Tenez compte des points suivants :

   * Pour les objectifs utilisés pour les packages Advertising DSP, le nom de l’objectif doit comporter le préfixe « ADSP_ » tel que « ADSP_Registrations ». Le préfixe n’est pas sensible à la casse.

   * Incluez uniquement les mesures attribuées à DSP. Toutes les mesures attribuées à Search, Social et Commerce ou à tout autre réseau publicitaire sont ignorées.

   * Au moins une mesure doit être de type *[!UICONTROL Goal]*.

   * DSP utilise les poids non mobiles pour toutes les publicités. Tous les poids mobiles spécifiés sont ignorés.

   >[!NOTE]
   >
   >* [!DNL Analytics] événements personnalisés suivent cette convention d’affectation des noms : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid`
   >* [!DNL Analytics] dimensions et les segments ne sont pas disponibles pour l’optimisation d’Adobe Advertising.

   >[!TIP]
   >
   >Pour des performances optimales, les mesures combinées dans l’objectif personnalisé doivent totaliser au moins dix conversions par jour. Dans le cas contraire, il est recommandé d’ajouter à l’objectif des mesures de conversion supplémentaires, telles que les pages de produits ou les démarrages d’application. Consultez [ Bonnes pratiques pour créer un objectif personnalisé ](#custom-goal-best-practices) pour obtenir des instructions.

Dans les paramètres du package DSP pour les packages qui utilisent l’objectif d’optimisation « [!UICONTROL Highest Return on Ad Spend (ROAS)"] ou [!UICONTROL Lowest Cost per Acquisition (CPA)] », le nom de l’objectif est désormais inclus dans la liste [!UICONTROL Custom Goals]. Lorsque vous sélectionnez l’objectif en tant qu’objectif personnalisé pour un package, la liste [!UICONTROL Conversion Metric] inclut toutes les mesures d’objectif pour l’objectif.

## Bonnes pratiques pour créer un objectif personnalisé {#custom-goal-best-practices}

### Objectifs personnalisés avec une mesure unique

Les exemples suivants montrent comment configurer des objectifs qui ciblent une seule mesure de conversion.

#### Exemple pour une campagne avec l’objectif d’optimisation « [!UICONTROL Highest Return on Ad Spend (ROAS)] »

Si l’objectif de votre campagne est le chiffre d’affaires ([!UICONTROL Highest Return on Ad Spend (ROAS)]) et que le chiffre d’affaires de tous les types d’appareils est également important pour vous, incluez la mesure « [!UICONTROL Revenue] » avec un poids non mobile de un (1) ; le poids mobile est ignoré. Sélectionnez le type de mesure *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un poids non mobile de un (1) équivaut à une valeur de un (1) pour chaque dollar de chiffre d’affaires qui est suivi pour les publicités display sur n’importe quel appareil. Par exemple, une conversion de 250 $ avec un poids non mobile de un (1) est signalée comme 250 $ pour les conversions. Si la mesure de conversion se voit attribuer un poids non mobile de 0,5, la conversion de 250 $ est signalée comme 125 $ dans Adobe Advertising (250 $ de conversion * 0,5 [!UICONTROL Non-mobile Weight] = 125 $).

#### Exemple pour une campagne avec l’objectif d’optimisation « [!UICONTROL Lowest Cost per Acquisition (CPA)] »

Si l’objectif de votre campagne est le coût par acquisition (CPA) le plus faible et ne nécessite qu’un seul événement de succès (tel que « Envoi de la demande »), incluez cette mesure et indiquez le type de mesure comme *[!UICONTROL Goal]*. La bonne pratique consiste à définir le poids non mobile sur un (1) ; le poids mobile est ignoré.

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un poids non mobile de un (1) équivaut à une valeur de un (1) pour chaque conversion qui est suivie pour les publicités display sur n&#39;importe quel appareil. Par exemple, si 10 conversions d’envoi d’application sont suivies, 10 conversions d’envoi d’application sont signalées. Cependant, si la mesure de conversion se voit attribuer un poids non mobile de 0,5, les 10 conversions sont signalées comme cinq (5) dans Adobe Advertising (10 conversions * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Objectifs personnalisés avec plusieurs mesures

Il existe deux scénarios dans lesquels vous utiliseriez plusieurs mesures dans un objectif personnalisé :

* L’objectif de votre campagne comporte plusieurs événements de succès. Par exemple, il se peut que vous fassiez de la publicité pour plusieurs actions sur site (téléchargement de PDF, nous contacter et inscription par e-mail) et que toutes ces actions contribuent à l’objectif de votre CPA. Si l’objectif inclut les trois mesures distinctes, ayant chacune un poids non mobile d’une (1), l’algorithme optimisé par [!DNL Adobe AI] traite chacune des mesures et chacun des types d’appareils utilisateur avec la même importance. Si les différentes mesures ont des coûts ou une importance variables, vous ajustez leur poids relatif en conséquence.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La mesure de conversion unique de votre objectif personnalisé n’atteint pas le minimum de 10 conversions par jour requis pour optimiser les performances. Cela peut se produire en raison de dépenses quotidiennes minimales ou d’un nombre limité de conversions naturelles. L’ajout de mesures de prise en charge supplémentaires à l’objectif personnalisé peut vous aider à atteindre le seuil de 10 conversions par jour. Dix événements annexes peuvent aider un paquet à atteindre le seuil de 10/jour, même lorsque chacun de leurs poids est inférieur à un (1). Mais vous n’aurez peut-être pas besoin d’ajouter autant d’événements.

  Lorsque vous ajoutez des mesures de soutien à un objectif personnalisé, pondérez-les en fonction de leur importance relative par rapport à l’événement de succès principal, et gardez à l’esprit la quantité de points de données. Cela permet à l’algorithme optimisé par [!DNL Adobe AI] d’équilibrer plusieurs mesures et de réaliser une optimisation en vue de votre objectif.

  L’exemple d’objectif suivant inclut trois mesures, chacune ayant un poids non mobile différent : Envoi de l’application = 1, Début de l’application = 0,1 et Page de destination de l’annonceur = 0,01. Cela signifie que chaque conversion d’envoi d’application a la même valeur pour votre entreprise qu’une moyenne de 10 conversions de début d’application et de 100 conversions de page de destination d’annonceur.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Si, au contraire, vous pondériez les visites de pages de destination de manière égale dans les envois d’applications, alors la quantité naturellement plus élevée de visites de pages de destination pourrait dépasser votre objectif et biaiser les visites de pages de destination.<!--reword-->

>[!MORELIKETHIS]
>
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du package](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)
