---
title: À propos de Adobe Advertising Creative
description: En savoir plus sur  [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
TQID: https://experienceleague.adobe.com/UfaLj12BFBAxCDvtb6cUtVxlcuOSYgnZPTAn7494APk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 507
ht-degree: 0%

---

# À propos de Adobe Advertising Creative 2.0

<!-- verify all and rewrite to include new stuff -->

Dans le cadre d’Adobe Advertising, Advertising Creative est une plateforme en libre-service permettant d’automatiser les expériences publicitaires personnalisées en temps réel et d’optimiser éventuellement vos publicités au niveau des éléments créatifs.<!-- Verify --> Vous pouvez implémenter les expériences publicitaires sous la forme de publicités dans n’importe quel DSP, y compris Adobe Advertising DSP.

## Bibliothèques créatives personnalisées de contenus créatifs réutilisables

Vos bibliothèques Creative vous permettent de gérer les contenus publicitaires que vous utiliserez dans vos expériences publicitaires. Vous pouvez créer plusieurs bibliothèques, chacune avec des contenus créatifs individuels et des groupes de contenus créatifs (appelés *lots*, que vous joindrez à des expériences).

### Intégrations de ressources [!DNL Adobe]

[!DNL Creative] est directement intégré aux produits [!DNL Adobe] suivants, ce qui vous permet d’importer des ressources dans vos bibliothèques de contenu créatif :

* **Adobe Experience Manager :** chargez les ressources d’image [!DNL Adobe] que votre équipe de conception crée et approuve pour les publicités d’image standard.

* **Adobe GenStudio for Performance Marketing :** importez toutes les variantes d’annonces de vos expériences d’affichage publicitaire sous forme de contenus publicitaires HTML5.

## Expériences basées sur des règles et expériences non ciblées

* **Expériences ciblées et basées sur des règles :** créez des histoires à l’aide d’un modèle d’arbre de décision basé sur des règles, en déployant une chaîne chorégraphiée d’annonces personnalisées en temps réel en fonction de ce que vous savez de votre audience. Par exemple, les histoires peuvent changer en fonction du comportement des clients, de la zone géographique, des données démographiques, du reciblage, de la position sur le parcours des clients, etc.

* **Expériences non ciblées :** planifiez et optimisez les éléments publicitaires sans réduire l’audience.

### Intégrations de données [!DNL Adobe]

Utilisez vos segments d’audience propriétaires de Adobe Audience Manager et Adobe Analytics, ainsi que les segments d’audience personnalisés que vous créez dans Advertising DSP et recibler les pixels que vous créez à l’aide de [!DNL Creative], en tant que cibles pour des contenus publicitaires spécifiques dans une expérience publicitaire. <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### Implémentation d’expériences en tant que publicités

Une fois une expérience créée, vous pouvez générer une balise JavaScript ou iframe pour l’expérience et implémenter la balise en tant qu’annonce tierce dans une campagne Advertising DSP ou dans tout autre DSP.

### Optimisation des éléments publicitaires

Vous pouvez éventuellement [!DNL Creative] permettre d’optimiser les éléments d’annonce publicitaire pour toute expérience en fonction des performances (que vous définissiez ou non des cibles d’audience spécifiques) à l’aide d’une rotation d’annonce optimisée et pondérée, optimisée par [!DNL Adobe AI].

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
