---
title: À propos des objectifs personnalisés
description: Découvrez les objectifs personnalisés pour définir vos événements de succès dans des modules optimisés pour le CPA le plus bas ou le ROAS le plus élevé.
feature: DSP Optimization
exl-id: 806450b9-ce32-4f5c-a2ac-ba8e435ce36d
source-git-commit: eda0459472c1e4a8297daf69454de0fcb3d4f8ca
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# À propos des objectifs personnalisés

Les objectifs personnalisés définissent les événements de succès dont un annonceur a besoin pour atteindre ses objectifs commerciaux. Chaque module qui utilise des objectifs d’optimisation se terminant par &quot;[!UICONTROL - Custom Goal]&quot; (par exemple,[!UICONTROL Highest ROAS - Custom Goal]&quot;) doit inclure un objectif personnalisé qui permettra d’atteindre l’objectif d’optimisation général. Vous pouvez créer des objectifs personnalisés sous la forme *objectifs* in [!DNL Advertising Search, Social, & Commerce].

![objectifs personnalisés](/help/dsp/assets/objective-goals.png)

Chaque objectif personnalisé comprend une ou plusieurs mesures de conversion et les poids relatifs de ces mesures. Les mesures de conversion disponibles comprennent toutes les mesures suivies à l’aide du pixel de conversion d’Adobe Advertising et par le biais d’Adobe Analytics.

>[!NOTE]
>
>* [!DNL Analytics] les dimensions et les segments ne sont pas disponibles pour l’optimisation des Adobes Advertising.
>* Pour utiliser les événements Analytics dans DSP, demandez à votre équipe de compte d’Adobe de configurer une intégration de niveau annonceur.
>* [!DNL Analytics] les événements personnalisés suivent cette convention d’affectation des noms : `custom_event_[*event #*]_[*Analytics report suite ID*]`. Exemple : `custom_event_16_examplersid`

Supposons, par exemple, que trois mesures de conversion soient pertinentes pour un module spécifique dans l’une de vos campagnes : &quot;Téléchargement du PDF&quot; (20 USD), &quot;Enregistrement par e-mail&quot; (30 USD) et &quot;Confirmation de commande&quot; (40 USD). Si vous souhaitez donner du poids en fonction de la valeur monétaire ponctuelle de l’action du client, le poids relatif des propriétés est de 1, 2 et 1,5.

Voir [bonnes pratiques pour la création d’objectifs personnalisés](custom-goal-best-practices.md) pour obtenir des conseils sur la configuration de vos objectifs personnalisés.

Une fois que [créer un objectif personnalisé ;](custom-goal-create.md), vous pouvez [l’affecter à un module](/help/dsp/campaign-management/packages/package-settings.md) pour la création de rapports et l’optimisation algorithmique à l’aide d’Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Création d’un objectif personnalisé](custom-goal-create.md)
>* [Bonnes pratiques pour la création d’un objectif personnalisé](custom-goal-best-practices.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)
