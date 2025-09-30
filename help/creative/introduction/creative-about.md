---
title: À propos de Adobe Advertising Creative
description: En savoir plus sur  [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: 41814881a2fc0efde76927d12a8649efad86f4cb
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# À propos de Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

Dans le cadre d’Adobe Advertising, Advertising Creative est une plateforme en libre-service permettant d’automatiser les expériences publicitaires personnalisées en temps réel et d’optimiser éventuellement vos publicités au niveau des éléments créatifs.<!-- Verify --> Vous pouvez implémenter les expériences publicitaires sous la forme de publicités dans n’importe quel DSP, y compris Adobe Advertising DSP.

## Bibliothèques créatives personnalisées de contenus créatifs réutilisables

Vos bibliothèques Creative vous permettent de gérer les contenus publicitaires que vous utiliserez dans vos expériences publicitaires. Vous pouvez créer plusieurs bibliothèques, chacune avec des contenus créatifs individuels et des groupes de contenus créatifs (appelés *lots*, que vous joindrez à des expériences).

### Intégrations de ressources [!DNL Adobe]

[!DNL Creative] est directement intégré à Adobe Experience Manager, ce qui vous permet de charger facilement les ressources d’images [!DNL Adobe] créées et approuvées par votre équipe de conception pour les publicités d’images standard.

## Expériences basées sur des règles et expériences non ciblées

* **Expériences ciblées et basées sur des règles :** créez des histoires à l’aide d’un modèle d’arbre de décision basé sur des règles, en déployant une chaîne chorégraphiée d’annonces personnalisées en temps réel en fonction de ce que vous savez de votre audience. Par exemple, les histoires peuvent changer en fonction du comportement des clients, de la zone géographique, des données démographiques, du reciblage, de la position sur le parcours des clients, etc.

* **Expériences non ciblées :** planifiez et optimisez les éléments publicitaires sans réduire l’audience.

### Intégrations de données [!DNL Adobe]

Vous pouvez utiliser vos segments d’audience propriétaires de Adobe Audience Manager et Adobe Analytics, ainsi que les segments d’audience personnalisés que vous créez dans Advertising DSP et les pixels de reciblage que vous créez à l’aide de [!DNL Creative], en tant que cibles pour des contenus publicitaires spécifiques dans une expérience publicitaire. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Implémentation d’expériences en tant que publicités

Une fois une expérience créée, vous pouvez générer une balise JavaScript ou iframe pour l’expérience et implémenter la balise en tant qu’annonce publicitaire tierce standard dans une campagne Advertising DSP ou dans tout autre DSP.<!-- Will add video and other ad formats; not sure if they'll be available for both standard and dynamic ads. -->

### Optimisation des éléments publicitaires

Vous pouvez éventuellement [!DNL Creative] permettre d’optimiser les éléments publicitaires de n’importe quelle expérience en fonction des performances (que vous définissiez ou non des cibles d’audience spécifiques) à l’aide de la rotation optimisée et pondérée des publicités, optimisée par Adobe Sensei.

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## Reciblage des pixels

Vous pouvez créer des pixels de reciblage à utiliser comme cibles pour les créatifs dans une expérience publicitaire. Les cibles affichent les publicités uniquement pour les utilisateurs et utilisatrices disposant d’attributs spécifiés qui ont précédemment visité des pages web spécifiques.

## Suivi des impressions, clics et conversions

[!DNL Creative] effectue automatiquement le suivi de toutes les impressions et de tous les clics pour les publicités diffusées à partir d’une expérience . Vous pouvez également ajouter des URL de suivi d’impressions et de clics tierces aux contenus publicitaires dans les bibliothèques Creative, ainsi que des URL de suivi personnalisées dans une expérience.

[!DNL Creative] effectue également le suivi des conversions à partir des annonces diffusées créées à partir de vos expériences publicitaires.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Rapports de performance

Vous pouvez afficher des rapports de performances détaillés au niveau de l’expérience dans Creatives > Expériences.

Vous pouvez également créer des rapports Creative personnalisés dans Rapports > Rapports personnalisés pour surveiller les performances au niveau de l’expérience sur l’ensemble de vos expériences. Si vous utilisez vos expériences [!DNL Creative] comme annonces dans les campagnes DSP, les données de performances de ces annonces sont disponibles dans des rapports personnalisés supplémentaires, tout comme les données de vos autres annonces DSP. <!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

Vous pouvez éventuellement diffuser vos rapports personnalisés vers des [destinations de rapports](/help/dsp/reports/report-destinations/report-destination-about.md) spécifiées.

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [À propos de vos bibliothèques de création](/help/creative/creative-libraries/creative-libraries-about.md)
>* [À propos des expériences dans Advertising Creative](/help/creative/experiences/experience-about.md)
