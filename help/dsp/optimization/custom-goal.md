---
title: Objectifs personnalisés
description: Découvrez les objectifs personnalisés pour définir vos événements de succès dans des modules optimisés pour le CPA le plus bas ou le ROAS le plus élevé.
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
source-git-commit: 42fca0c829c708281703a6a1ea59c42dc7ac9f0d
workflow-type: tm+mt
source-wordcount: '1248'
ht-degree: 0%

---

# Objectifs personnalisés

Les objectifs personnalisés définissent les événements de succès dont un annonceur a besoin pour atteindre ses objectifs commerciaux. Chaque module qui utilise l’objectif d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot; doit inclure un objectif personnalisé pour atteindre l’objectif d’optimisation général. Vous pouvez créer des objectifs personnalisés sous la forme *objectifs* in [!DNL Advertising Search, Social, & Commerce]. Le nom de chaque objectif pour DSP doit comporter le préfixe &quot;ADSP_&quot;.

<!-- update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

Chaque objectif personnalisé (objectif) comprend une ou plusieurs mesures de conversion et les poids relatifs de ces mesures. Les mesures de conversion disponibles comprennent toutes les mesures suivies à l’aide du pixel de conversion d’Adobe Advertising et par le biais d’Adobe Analytics. Seuls les poids non mobiles sont pris en compte pour DSP objectifs personnalisés, mais ils sont utilisés pour tous les types d’annonces.

Supposons, par exemple, que trois mesures de conversion soient pertinentes pour un module spécifique dans l’une de vos campagnes : &quot;Téléchargement du PDF&quot; (20 USD), &quot;Enregistrement par e-mail&quot; (30 USD) et &quot;Confirmation de commande&quot; (40 USD). Si vous souhaitez donner du poids en fonction de la valeur monétaire ponctuelle de l’action du client, les poids relatifs des mesures seront de 1, 1,5 et 2.

Une fois que [créer un objectif personnalisé ;](#custom-goal-create), vous pouvez [l’affecter à un module](/help/dsp/campaign-management/packages/package-settings.md) pour la création de rapports et l’optimisation algorithmique à l’aide d’Adobe Sensei.

Les recommandations de poids sont générées automatiquement pour les mesures DSP attribuées dans les objectifs et peuvent appliquer toutes les recommandations de poids en un seul clic. Tous les changements de poids apportés aux objectifs dotés du préfixe &quot;ADSP_&quot; sont appliqués algorithmiquement dans DSP dans un délai de deux jours. Pour plus d’informations sur les recommandations relatives au poids, reportez-vous au chapitre du Guide d’optimisation intitulé &quot;Nouveaux objectifs (Beta)&quot;, disponible dans Search, Social et Commerce.

## Création d’un objectif personnalisé {#custom-goal-create}

Pour créer un objectif personnalisé, le compte DSP doit être associé à un [!DNL Search, Social, & Commerce] avec le même ID d’organisation Adobe Experience Cloud, depuis le [!DNL Search, Social, & Commerce] paramètres du client. Si votre compte DSP n’est pas lié à un [!DNL Search, Social, & Commerce] , puis contactez votre équipe de compte d’Adobe.

1. Connexion à [!DNL Advertising Search, Social, & Commerce] at (utilisateurs en Amérique du Nord) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) ou (tous les autres utilisateurs) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).

1. Assurez-vous que les mesures que vous souhaitez inclure dans votre objectif ont été suivies, sont disponibles dans le produit et incluez un nom d’affichage :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   1. Recherchez la mesure et assurez-vous que la variable **[!UICONTROL Show in UI and Reports]** est activé pour la mesure.

      >[!NOTE]
      >
      >* [!DNL Analytics] les événements personnalisés suivent cette convention d’affectation des noms : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid`

   1. Si la mesure n’a pas de valeur dans la variable **[!UICONTROL Display Name]** , puis cliquez dans la cellule, saisissez le nom d’affichage et cliquez sur **[!UICONTROL Apply].**

1. Créez l’objectif personnalisé en tant que *objectif*:

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL New Objectives Beta]**.

   1. Dans la barre d’outils, cliquez sur ![Créer](/help/dsp/assets/create-search-ui.png "Créer").

   1. Saisissez les paramètres de l’objectif, y compris les mesures associées et leur poids numérique relatif pour les appareils non mobiles, puis enregistrez l’objectif. Tenez compte des points suivants :

      * Pour les objectifs utilisés pour les packages Advertising DSP, le nom de l’objectif doit être précédé du préfixe &quot;ADSP_&quot; tel que &quot;ADSP_Inscriptions&quot;. Le préfixe n’est pas sensible à la casse.

      * Inclure uniquement les mesures attribuées à DSP. Toutes les mesures attribuées à Search, Social et Commerce ou à tout autre réseau publicitaire sont ignorées.

      * Au moins une mesure doit avoir le type de mesure *[!UICONTROL Goal]*.

      * DSP utilise les poids non mobiles pour toutes les publicités. Les poids mobiles spécifiés sont ignorés.

      >[!NOTE]
      >
      >* [!DNL Analytics] les événements personnalisés suivent cette convention d’affectation des noms : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid`
      >* [!DNL Analytics] les dimensions et les segments ne sont pas disponibles pour l’optimisation des Adobes Advertising.

      >[!TIP]
      >
      >Pour des performances optimales, les mesures combinées de l’objectif personnalisé (objectif) doivent totaliser au moins dix conversions par jour. Dans le cas contraire, la bonne pratique consiste à ajouter à l’objectif des mesures de conversion supplémentaires, telles que des pages de produits ou des démarrages d’application, qui prennent en charge la conversion. Voir [Bonnes pratiques pour la création d’un objectif personnalisé](#custom-goal-best-practices) pour obtenir des instructions.

Dans les paramètres du module DSP pour les modules qui utilisent l’objectif d’optimisation &quot;[!UICONTROL Highest Return on Ad Spend (ROAS)"] ou &quot;[!UICONTROL Lowest Cost per Acquisition (CPA)],&quot; le nom de l’objectif est désormais inclus dans la variable [!UICONTROL Custom Goals] liste. Lorsque vous sélectionnez l’objectif comme objectif personnalisé pour un module, la variable [!UICONTROL Conversion Metric] liste comprend toutes les mesures d’objectif pour l’objectif.

## Bonnes pratiques pour la création d’un objectif personnalisé {#custom-goal-best-practices}

### Objectifs personnalisés avec une seule mesure

Les exemples suivants montrent comment configurer des objectifs qui ciblent une seule mesure de conversion.

#### Exemple pour une campagne avec le[!UICONTROL Highest Return on Ad Spend (ROAS)]&quot;Objectif d’optimisation

Si l’objectif de votre campagne est le chiffre d’affaires ([!UICONTROL Highest Return on Ad Spend (ROAS)]), les recettes provenant de tous les types d’appareils sont également importantes pour vous, puis incluez le[!UICONTROL Revenue]&quot;mesure avec un poids non mobile (pour les conversions à partir d’un appareil non mobile) d’un (1) et un poids mobile (pour les conversions à partir d’un appareil mobile) d’un (1). Sélection du type de mesure *[!UICONTROL Goal]*.

<!-- update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un poids mobile ou un poids non mobile d’une (1) équivaut à une (1) valeur pour chaque 1 $ de chiffre d’affaires suivi.
>
> Par exemple, une conversion de 250 $ avec un poids non mobile d’un (1) est signalée comme 250 $ pour les conversions. Si la mesure de conversion se voit attribuer un poids non mobile de 0,5, la conversion de 250 $ d’un appareil non mobile est signalée comme étant de 125 $ en Adobe Advertising (250 $ Conversion * 0,5 [!UICONTROL Non-mobile Weight] = 125 $).

#### Exemple pour une campagne avec le[!UICONTROL Lowest Cost per Acquisition (CPA)]&quot;Objectif d’optimisation

Si l’objectif de votre campagne est le coût par acquisition le plus bas (CPA) et qu’il ne nécessite qu’un seul événement de succès (par exemple &quot;Envoi de demande&quot;), incluez cette mesure et spécifiez le type de mesure comme *[!UICONTROL Goal]*. La bonne pratique consiste à définir le poids non mobile et le poids mobile sur un (1).

<!-- update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> Un poids mobile ou un poids non mobile d’une (1) équivaut à une (1) valeur pour chaque conversion suivie. Par exemple, si 10 conversions d’envoi de demande sont suivies, 10 conversions d’envoi de demande sont signalées. Toutefois, si la mesure de conversion se voit attribuer un poids non mobile de 0,5, les 10 conversions non mobiles sont signalées comme étant de cinq (5) en Adobe Advertising (10 conversions * 0,5). [!UICONTROL Non-mobile Weight] = 5).

### Objectifs personnalisés avec plusieurs mesures

Il existe deux scénarios dans lesquels vous utiliseriez plusieurs mesures dans un objectif personnalisé :

* L’objectif de votre campagne comporte plusieurs événements de succès. Par exemple, vous annoncez peut-être plusieurs actions sur site (téléchargement de PDF, contact avec nous et inscription par e-mail), et toutes ces actions contribuent à votre objectif de CPA. Si l’objectif comprend les trois mesures distinctes, chacune avec des poids non mobiles et mobiles d’une (1), la variable [!DNL Adobe Sensei] l’algorithme traite chaque mesure et chaque type d’appareil utilisateur avec la même importance. Si les différentes mesures et les différents types d’appareils ont des coûts ou une importance variables, vous ajustez leur poids relatif en conséquence.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* La mesure de conversion unique de votre objectif personnalisé n’atteint pas le minimum de 10 conversions par jour requis pour des performances optimisées. Cela peut se produire en raison de dépenses journalières minimales ou d’un nombre limité de conversions naturelles. L’ajout de mesures de prise en charge supplémentaires à l’objectif personnalisé peut vous aider à atteindre le seuil de 10 conversions par jour. Dix événements de prise en charge peuvent aider un kit à atteindre le seuil de 10/jours, même si chaque poids est inférieur à un (1). Mais vous n’aurez peut-être pas besoin d’ajouter autant d’événements.

  Lorsque vous ajoutez des mesures de prise en charge à un objectif personnalisé, pondérez-les en fonction de leur importance relative par rapport à l’événement de succès principal et gardez à l’esprit la quantité de points de données. Cela permet à l’algorithme Adobe Sensei d’équilibrer plusieurs mesures et d’optimiser en fonction de votre objectif.

  L’exemple d’objectif suivant comprend trois mesures, chacune avec un poids non mobile différent : envoi de la demande = 1, démarrage de la demande = 0,1 et page d’entrée des annonceurs = 0,01. Cela signifie que chaque conversion d’envoi d’application à partir d’appareils non mobiles a la même valeur pour votre entreprise qu’une moyenne de 10 conversions de démarrage d’application à partir d’appareils non mobiles et de 100 conversions de page d’entrée des annonceurs à partir d’appareils non mobiles.

<!-- update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

Si, à la place, vous aviez pondéré les visites de page d’entrée de manière égale par rapport aux envois de demande, le nombre naturellement plus élevé de visites de page d’entrée pourrait dépasser votre objectif et augmenter le nombre de visites de page d’entrée.<!--reword-->

>[!MORELIKETHIS]
>
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)
