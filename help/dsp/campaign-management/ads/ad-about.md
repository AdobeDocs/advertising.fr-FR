---
title: À propos de la gestion des publicités dans Advertising DSP
description: En savoir plus sur la gestion des publicités.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# À propos de la gestion des publicités dans Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP prend en charge la diffusion de publicités par le biais de balises de service de publicités tierces (telles que Google, Flashtalking ou Sizmek) pour divers types d’annonces et le chargement direct de ressources pour les annonces d’affichage natives. Vous pouvez charger des balises tierces individuellement ou en bloc. Les téléchargements en masse utilisent des feuilles de balises partenaires ou un modèle de balise en bloc.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Une fois vos publicités configurées, associez-les à un emplacement, qui comprend les paramètres de ciblage (tels que la géographie, l’audience, le périphérique et le ciblage d’inventaire) qui contrôlent la manière dont votre campagne diffuse. Vous pouvez joindre une publicité à un ou plusieurs emplacements.

## Types de publicité disponibles {#ad-types}

Tous les types d’annonces suivants sont disponibles dans DSP. Pour obtenir des spécifications complètes pour chaque type d’annonce, reportez-vous à la section [Spécifications de l’annonce](ad-specs.md).

* **Publicités audio (tierces uniquement)** : les publicités audio s’exécutent sur le contenu des sites d’éditeurs numériques et peuvent être exécutées de manière autonome sous la forme de fichiers audio ou avec des bannières d’accompagnement. L’audio est le meilleur moyen d’accroître la notoriété de la marque et d’interagir avec les publics en ligne. Les indicateurs de performances clés pour le son incluent [!UICONTROL Completion Rate] et [!UICONTROL Cost per Completion].

* **Publicités d’affichage (tiers uniquement)** : les publicités d’affichage sont des images animées ou statiques affichées dans les navigateurs web ou dans les applications. Cliquer sur l’unité publicitaire permet à l’utilisateur d’accéder à un site ou à un microsite de marque. L’affichage est le meilleur outil utilisé pour générer des CPM efficaces, augmenter l’association des messages, ajouter des points de contact de marque ou de produit supplémentaires et faire descendre les utilisateurs dans l’entonnoir d’achat. Les indicateurs de performances clés pour l&#39;affichage sont [!UICONTROL Clicks], [!UICONTROL Cost per Click], [!UICONTROL Conversions] et [!UICONTROL Cost per Conversion]. DSP prend en charge un large éventail de tailles de bannières publicitaires.

* **Publicités mobiles (tiers uniquement)** : les publicités mobiles peuvent être au format vidéo preroll (VAST, MRAID) ou d’affichage standard. La vidéo preroll mobile peut être lancée automatiquement ou un clic pour être lue. Elle est préférable pour atteindre les visionneuses sur plusieurs écrans. L’affichage standard mobile est une image statique affichée dans les navigateurs web mobiles ou dans les applications. Il est préférable de l’utiliser pour compléter les achats de vidéos numériques, générer l’association des messages et ajouter des points de contact de marque ou de produit supplémentaires. Les publicités mobiles peuvent également fonctionner comme des prises de vue en plein écran ou comme des spots mobiles, qui sont des publicités mobiles à fort impact en plein écran et qui sont les mieux utilisées pour développer la notoriété de la marque pour les audiences mobiles et stimuler les conversions.

* **Publicités d’affichage natives (propriétaire uniquement)** : les publicités natives sont prises en charge dans le format d’affichage standard. Les annonces natives incluent un titre et/ou un titre, une description, un logo et une image. Les éléments d’annonce sont combinés et rendus pour correspondre au style de page de l’éditeur afin que l’annonce se fonde avec le contenu organique de l’éditeur et entraîne un engagement plus important. L’option native est la mieux utilisée pour la sensibilisation à la marque et pour stimuler les taux d’affichage et d’engagement des audiences grâce à la publicité conviviale destinée aux visiteurs. Les indicateurs de performances clés sont les suivants : [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions] et [!UICONTROL Cost Per Conversion].

* **Publicités preroll (tiers uniquement)** : les publicités preroll (VAST et VPAID) sont affichées avant le contenu vidéo de qualité supérieure et offrent une expérience de visionneuse immersive et attrayante. La vidéo preroll peut être interactive, contenir des fonctions multimédias enrichies et inclure des superpositions, des roulements et des appels à l’action. [!UICONTROL Video Completion Rate] et [!UICONTROL Viewability Rate] sont les indicateurs de performances clés des publicités vidéo preroll.

* **Publicités TV connectées (tiers uniquement)** : les publicités TV connectées sont affichées avant et pendant le contenu vidéo de la télévision premium. L’inventaire de toutes les télévisions connectées s’exécute sur les appareils télévisés, ce qui signifie que la vidéo est lue automatiquement dans un environnement en arrière-plan plein écran que les téléspectateurs ne peuvent pas ignorer. La télévision connectée est le format vidéo numérique le plus proche des publicités télévisées. [!UICONTROL Completion Rate] sont les indicateurs de performances clés de la télévision connectée.

* **Publicités vidéo universelles (tierces uniquement)** : les publicités vidéo universelles vous permettent de cibler l’inventaire vidéo des environnements de bureau, mobiles et de télévision connectés pour les inventaires VPAID et VAST à l’aide d’un seul emplacement vidéo. Elles combinent toutes les fonctionnalités des publicités preroll, mobiles et de télévision connectées et sont affichées avant et pendant le contenu vidéo. [!UICONTROL Completion Rate] et [!UICONTROL Viewability Rate] sont les indicateurs de performances clés de la vidéo universelle.

  Les publicités vidéo universelles ne peuvent être associées qu’à des emplacements vidéo universels.

  Pour plus d’informations sur les publicités vidéo universelles, voir &quot;[FAQ à propos de la vidéo universelle](/help/dsp/campaign-management/faq-universal-video.md)&quot;.

## DSP Approbations publicitaires

Lorsque vous créez une publicité, DSP la révise pour les catégories sensibles, cliquez sur la fonctionnalité d’URL et prévisualisez le rendu.

Au départ, la colonne [!UICONTROL Status] de la publicité affiche un point rouge. Le processus de révision prend normalement 24 à 48 heures. Toutefois, une publicité interrompue peut avoir un état en attente pendant plus de 48 heures, vous avez donc le temps de corriger les erreurs avant le rejet de la publicité. Les publicités refusées incluent une raison de rejet.

Lorsque DSP approuve une publicité, la colonne État de la publicité affiche un point vert.

![indicateur d&#39;approbation dans la colonne [!UICONTROL Status]](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Votre publicité ne peut être diffusée que si DSP et le SSP ont tous deux approuvé le contenu créatif. Chaque SSP possède ses propres exigences et processus d’approbation.

>[!MORELIKETHIS]
>
>* [Créer une publicité unique](ad-create.md)
>* [Créer plusieurs publicités tierces](ad-create-multiple.md)
>* [Spécifications de la publicité](ad-specs.md)
