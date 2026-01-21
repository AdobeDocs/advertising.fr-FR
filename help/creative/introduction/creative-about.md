---
title: A propos de Adobe Advertising Creative
description: En savoir plus [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: 1394b988828f5400b858f1a40b1b6382431a62b0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# A propos de Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

Dans le cadre de Adobe Advertising, Advertising Creative est une plate-forme en libre-service permettant d’automatiser les expériences publicitaires personnalisées en temps réel et d’optimiser éventuellement vos annonces au niveau de l’élément créatif.<!-- Verify --> Vous pouvez mettre en œuvre les expériences publicitaires sous forme d’annonces dans n’importe quel DSP, y compris Adobe Advertising DSP.

## Bibliothèques personnalisées de créations réutilisables

Vos bibliothèques Creative vous permettent de gérer les créations que vous utiliserez dans vos expériences publicitaires. Vous pouvez créer plusieurs bibliothèques, chacune avec des créations individuelles et des groupes créatifs (appelés *bundles, que vous attacherez aux expériences*).

### [!DNL Adobe] Intégrations d’actifs

[!DNL Creative] est directement intégré aux produits suivants [!DNL Adobe] , ce qui vous permet d’importer des ressources dans vos bibliothèques créatives :

* **Adobe Experience Manager :** transférez les ressources d’image [!DNL Adobe] que votre équipe de conception crée et approuve pour les annonces illustrées standard.

* **Adobe GenStudio pour le marketing de performance :** importez toutes les variantes d’annonces de vos expériences d’affichage d’annonces en tant que créations HTML5.

## Expériences à la fois basées sur des règles et non ciblées

* **Expériences ciblées et basées sur des règles :** créez des histoires à l’aide d’un modèle d’arbre de décision basé sur des règles, en déployant une série chorégraphiée d’annonces personnalisées en temps réel en fonction de ce que vous savez de votre public. Par exemple, les stories peuvent changer en fonction du comportement des clients, de la géographie, des données démographiques, du reciblage, de la position dans le parcours client, etc.

* **Expériences non ciblées :** planifiez et optimisez les éléments d’annonce sans restreindre l’audience.

### [!DNL Adobe] Intégrations de données

Utilisez vos segments d’audience propriétaires de Adobe Audience Manager et d’Adobe Analytics, ainsi que les segments d’audience personnalisés que vous créez dans Advertising DSP et les pixels de reciblage que vous créez à l’aide [!DNL Creative] de Advertising, comme cibles pour des créations spécifiques dans une expérience publicitaire. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Mise en œuvre d’expériences sous forme de publicités

Une fois que vous avez créé une expérience, vous pouvez générer une balise JavaScript ou iframe pour l’expérience et l’implémenter en tant qu’annonce tierce dans une campagne de DSP publicitaires ou dans toute autre DSP.

### Optimisation des éléments publicitaires

Vous pouvez éventuellement autoriser [!DNL Creative] l’optimisation des éléments publicitaires pour n’importe quelle expérience en fonction des performances (que vous définissiez ou non des cibles d’audience spécifiques) à l’aide d’une rotation d’annonce optimisée et pondérée, optimisée qui est alimentée par [!DNL Adobe AI].

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## Pixels de reciblage

Vous pouvez créer des pixels de reciblage à utiliser comme cibles pour les créations dans une expérience publicitaire. Les cibles diffusent des annonces uniquement pour les utilisateurs ayant des attributs spécifiés qui ont déjà visité des pages Web spécifiques.

## Suivi des impressions, clics et conversions

[!DNL Creative] Effectue automatiquement le suivi de toutes les impressions et clics pour les publicités diffusées à partir d’une expérience. Vous pouvez également ajouter des URL de suivi des impressions et des clics tierces aux créations dans Creative bibliothèques, ainsi que des URL de suivi personnalisées dans une expérience.

[!DNL Creative] Effectue également le suivi des conversions à partir des annonces diffusées créées à partir de vos expériences publicitaires.<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## Rapports sur le rendement

Vous pouvez afficher des rapports de performance détaillés au niveau de l’expérience dans Creatives > Experiences.

Vous pouvez également créer des rapports Creative personnalisés dans Rapports > Rapports personnalisés pour surveiller les performances au niveau de l’expérience dans vos expériences. Si vous utilisez vos [!DNL Creative] expériences en tant qu’annonces dans DSP campagnes, les données de performances de ces annonces sont disponibles dans des rapports personnalisés supplémentaires, tout comme les données de vos autres annonces DSP. <!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

Vous pouvez éventuellement livrer vos rapports personnalisés vers des destinations de rapport spécifiées[](/help/dsp/reports/report-destinations/report-destination-about.md).

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [À propos de vos bibliothèques créatives](/help/creative/creative-libraries/creative-libraries-about.md)
>* [À propos des expériences dans Advertising Creative](/help/creative/experiences/experience-about.md)
