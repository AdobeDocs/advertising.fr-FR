---
title: Objectifs personnalisés
description: Découvrez les objectifs personnalisés pour définir vos événements de succès dans des packages optimisés pour la CPA la plus faible ou le retour sur investissement le plus élevé.
feature: DSP Optimization
source-git-commit: f05d0f909cda6248260eaafd2fd24a8eca7f47e5
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---

# Objectifs personnalisés

Les objectifs personnalisés définissent les événements de succès dont un annonceur a besoin pour atteindre ses objectifs commerciaux. Chaque package qui utilise l’objectif d’optimisation »[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou «[!UICONTROL Lowest Cost per Acquisition (CPA)]« doit inclure un objectif personnalisé qui permettra d’atteindre l’objectif d’optimisation global. Vous pouvez créer des objectifs personnalisés en tant que *objectifs* dans [!DNL Advertising Search, Social, & Commerce].

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Chaque objectif personnalisé se compose d’une ou de plusieurs mesures de conversion et du poids relatif de ces mesures. Les mesures de conversion disponibles incluent toutes les mesures suivies à l’aide du pixel de conversion d’Adobe Advertising et via Adobe Analytics.

Supposons, par exemple, que trois mesures de conversion soient pertinentes pour un package spécifique dans l’une de vos campagnes : « Téléchargement du PDF » évalué à 20 USD, « Inscription par e-mail » évalué à 30 USD et « Confirmation de commande » évalué à 40 USD. Si vous souhaitez donner un poids en fonction de la valeur monétaire unique de l’action du client, les poids relatifs des mesures sont 1, 1,5 et 2.

Une fois que [créer un objectif personnalisé](#custom-goal-create), vous pouvez [l’affecter à un package](/help/dsp/campaign-management/packages/package-settings.md) pour la création de rapports et l’optimisation algorithmique à l’aide d’Adobe Sensei.

## Créer un objectif personnalisé {#custom-goal-create}

Pour créer un objectif personnalisé, le compte DSP doit être lié à un [!DNL Search, Social, & Commerce] compte avec le même ID d’organisation Adobe Experience Cloud, depuis le [!DNL Search, Social, & Commerce] paramètres client. Si votre compte DSP n’est pas lié à un compte [!DNL Search, Social, & Commerce] , puis contactez l’équipe chargée de votre compte d’Adobe.

1. Connectez-vous à [!DNL Advertising Search, Social, & Commerce] à (utilisateurs en Amérique du Nord) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) ou (tous les autres utilisateurs) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Assurez-vous que les mesures que vous souhaitez inclure dans votre objectif ont fait l’objet d’un suivi, sont disponibles dans le produit et incluent un nom d’affichage :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Localisez la mesure et assurez-vous que : **[!UICONTROL Show in UI and Reports]** est activé pour la mesure.

      >[!NOTE]
      >
      >* [!DNL Analytics] les événements personnalisés respectent cette convention de nommage : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid`

   1. Si la mesure n’a pas de valeur dans le **[!UICONTROL Display Name]** , puis cliquez dans la cellule, saisissez le nom d&#39;affichage, puis cliquez sur **[!UICONTROL Apply].**

1. Créer l’objectif personnalisé en tant que *objectif*:

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Dans la barre d’outils, cliquez sur ![Créer](/help/dsp/assets/create-search-ui.png "Créer").

   1. Saisissez les paramètres des objectifs, y compris les mesures associées et leur poids numérique relatif pour les appareils non mobiles et les appareils mobiles, puis enregistrez l’objectif.

      Au moins une mesure doit être de type *[!UICONTROL Goal]*.

      >[!NOTE]
      >
      >* [!DNL Analytics] les événements personnalisés respectent cette convention de nommage : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid`
      >* [!DNL Analytics] les dimensions et les segments ne sont pas disponibles pour l’optimisation de l’Adobe Advertising.

Dans les paramètres du package DSP pour les packages qui utilisent l’objectif d’optimisation « [!UICONTROL Highest Return on Ad Spend (ROAS)"] ou «[!UICONTROL Lowest Cost per Acquisition (CPA)], » le nom de l’objectif est désormais inclus dans [!UICONTROL Custom Goals] liste. Lorsque vous sélectionnez l’objectif en tant qu’objectif personnalisé d’un package, le [!UICONTROL Conversion Metric] la liste inclut toutes les mesures d’objectif pour l’objectif.

>[!TIP]
>
>Pour des performances optimales, les mesures combinées dans l’objectif personnalisé doivent totaliser au moins dix conversions par jour. Dans le cas contraire, il est recommandé d’ajouter à l’objectif des mesures de conversion supplémentaires, telles que les pages de produits ou les démarrages d’application. Voir [Bonnes pratiques pour créer un objectif personnalisé](custom-goal-best-practices.md) pour obtenir des instructions.

## Bonnes pratiques pour créer un objectif personnalisé [#custom-goal-best-practices]

### Objectifs personnalisés avec une mesure unique

Les exemples suivants montrent comment configurer des objectifs qui ciblent une seule mesure de conversion.

#### Exemple pour une campagne avec le «[!UICONTROL Highest Return on Ad Spend (ROAS)]« Objectif d’optimisation

Si l’objectif de votre campagne est le chiffre d’affaires ([!UICONTROL Highest Return on Ad Spend (ROAS)]), et le chiffre d’affaires de tous les types d’appareils est tout aussi important pour vous, puis incluez les «[!UICONTROL Revenue]« mesure avec un poids non mobile (pour les conversions à partir d’un appareil non mobile) de un (1) et un poids mobile (pour les conversions à partir d’un appareil mobile) de un (1). Sélectionner le type de mesure *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un poids mobile ou non mobile de un (1) équivaut à une valeur de un (1) pour chaque 1 $ de chiffre d’affaires qui fait l’objet d’un suivi.
>
> Par exemple, une conversion de 250 $ avec un poids non mobile de un (1) est signalée comme 250 $ pour les conversions. Si la mesure de conversion se voit attribuer un poids non mobile de 0,5, la conversion de 250 $ à partir d’un appareil non mobile est signalée comme un Adobe Advertising de 125 $ (conversion de 250 $ * 0,5 [!UICONTROL Non-mobile Weight] = 125 $).

#### Exemple pour une campagne avec le «[!UICONTROL Lowest Cost per Acquisition (CPA)]« Objectif d’optimisation

Si l’objectif de votre campagne est le coût par acquisition (CPA) le plus bas et qu’elle ne nécessite qu’un seul événement de succès (tel que « Envoi de la demande »), incluez cette mesure et indiquez le type de mesure comme suit : *[!UICONTROL Goal]*. La bonne pratique consiste à définir le poids non mobile et le poids mobile comme un seul (1).

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un poids mobile ou non mobile de un (1) équivaut à une valeur de un (1) pour chaque conversion qui est suivie. Par exemple, si 10 conversions d’envoi d’application sont suivies, 10 conversions d’envoi d’application sont signalées. Toutefois, si la mesure de conversion se voit attribuer un poids non mobile de 0,5, les 10 conversions non mobiles sont signalées comme cinq (5) en Adobe Advertising (10 conversions * 0,5 [!UICONTROL Non-mobile Weight] = 5).

### Objectifs personnalisés avec plusieurs mesures

Il existe deux scénarios dans lesquels vous utiliseriez plusieurs mesures dans un objectif personnalisé :

* L’objectif de votre campagne comporte plusieurs événements de succès. Par exemple, il se peut que vous fassiez de la publicité pour plusieurs actions sur site (téléchargement du PDF, nous contacter et inscription par e-mail) et que toutes ces actions contribuent à l’objectif de votre CPA. Si l’objectif inclut les trois mesures distinctes, chacune avec un poids non mobile et mobile d’une (1), la valeur [!DNL Adobe Sensei] L’algorithme traite avec la même importance chaque mesure et chaque type d’appareil utilisateur. Si les différentes mesures et les différents types d’appareils présentent des coûts ou une importance variables, vous ajustez leur poids relatif en conséquence.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La mesure de conversion unique de votre objectif personnalisé n’atteint pas le minimum de 10 conversions par jour requis pour optimiser les performances. Cela peut se produire en raison de dépenses quotidiennes minimales ou d’un nombre limité de conversions naturelles. L’ajout de mesures de prise en charge supplémentaires à l’objectif personnalisé peut vous aider à atteindre le seuil de 10 conversions par jour. Dix événements annexes peuvent aider un colis à atteindre le seuil de 10/jour, même lorsque chacun de leurs poids est inférieur à un (1). Mais vous n’aurez peut-être pas besoin d’ajouter autant d’événements.

  Lorsque vous ajoutez des mesures de soutien à un objectif personnalisé, pondérez-les en fonction de leur importance relative par rapport à l’événement de succès principal, et gardez à l’esprit la quantité de points de données. Cela permet à l’algorithme d’Adobe Sensei d’équilibrer plusieurs mesures et d’optimiser la réalisation de votre objectif.

  L’exemple d’objectif suivant inclut trois mesures, chacune ayant un poids non mobile différent : Envoi de la demande = 1, Début de la demande = 0,1 et Page de destination de l’annonceur = 0,01. Cela signifie que chaque conversion d’envoi d’application à partir d’appareils non mobiles a la même valeur pour votre entreprise qu’une moyenne de 10 conversions de démarrage d’application à partir d’appareils non mobiles et de 100 conversions de page de destination d’annonceur à partir d’appareils non mobiles.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Si, au contraire, vous pondériez les visites de pages de destination de manière égale dans les envois d’applications, alors la quantité naturellement plus élevée de visites de pages de destination pourrait dépasser votre objectif et biaiser les visites de pages de destination.<!--reword-->

>[!MORELIKETHIS]
>
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du package](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)
