---
title: À propos de la gestion des publicités dans Advertising DSP
description: En savoir plus sur la gestion des publicités.
feature: DSP Ads
exl-id: 41dbe28e-a476-4601-a3d8-a9111eae3f6b
source-git-commit: 7f9b118ffe0b8e972296f79b19f6dcd2a9dedabe
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# À propos de la gestion des publicités dans Advertising DSP

<!-- add "The Ads View (Dashboard?)" section -->

DSP prend en charge la diffusion de publicités par le biais de balises de diffusion de publicités tierces (telles que Google, Flashtalking ou Sizmek) pour divers types de publicités et le chargement direct des ressources pour les publicités display natives. Vous pouvez charger des balises tierces individuellement ou en bloc. Les chargements en masse utilisent des feuilles de balises de partenaire ou un modèle de balise en masse.

<!-- The bulk upload feature requires you to either a) upload DoubleClick and Flashtalking tag sheets or b) download a template, input your tags into the template, and then re-upload the template. -->
<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Une fois vos annonces configurées, joignez chaque annonce à un ou plusieurs emplacements, qui incluent les paramètres de ciblage (tels que la zone géographique, l’audience, l’appareil et le ciblage d’inventaire) qui contrôlent la manière dont votre campagne s’affiche. Vous devez joindre une publicité à un emplacement pour commencer à exécuter la publicité.

## Types d’annonces disponibles {#ad-types}

Tous les types d’annonces suivants sont disponibles dans DSP. Pour obtenir les spécifications complètes de chaque type d’annonce, reportez-vous à la [Spécifications d’annonce](ad-specs.md).

* **Annonces audio (tierces uniquement)** : les annonces audio sont lues entre le contenu sur les sites d’éditeur numérique et peuvent être exécutées seules en tant que fichiers audio ou avec les bannières associées. L’audio est idéal pour renforcer la notoriété de la marque et interagir avec les audiences en déplacement. Les indicateurs clés de performance pour l’audio incluent le [!UICONTROL Completion Rate] et le [!UICONTROL Cost per Completion].

* **Annonces display (tierces uniquement)** : les annonces display sont des images animées ou statiques affichées dans des navigateurs web ou des applications. Cliquez sur l’unité publicitaire pour diriger l’utilisateur vers un site ou un microsite de marque. Il est préférable d’utiliser l’affichage pour optimiser les CPM, augmenter l’association des messages, ajouter des points de contact de marque ou de produit supplémentaires et inciter les utilisateurs à acheter des funnel. Les indicateurs clés de performances pour l’affichage comprennent les [!UICONTROL Clicks], les [!UICONTROL Cost per Click], les [!UICONTROL Conversions] et les [!UICONTROL Cost per Conversion]. DSP prend en charge une grande variété de tailles de bannières publicitaires.

* **Publicités mobiles (tierces uniquement)** : les publicités mobiles peuvent être au format vidéo pré-roll (VAST, MRAID) ou au format d’affichage standard. La vidéo preroll mobile peut être lue automatiquement ou cliquer pour lire. Il est préférable de l’utiliser pour atteindre les visionneuses sur plusieurs écrans. L’affichage standard mobile est une image statique affichée sur les navigateurs web mobiles ou dans les applications. Il est préférable de l’utiliser pour compléter les achats de vidéos numériques, stimuler l’association des messages et ajouter des points de contact de marque ou de produit supplémentaires. Les annonces mobiles peuvent également fonctionner comme des prises de contrôle en plein écran ou des interstitiels mobiles, qui sont des annonces mobiles en plein écran à fort impact qui sont mieux utilisées pour développer la notoriété de la marque pour les audiences mobiles et générer des conversions.

* **Annonces display natives (propriétaires uniquement)** : les annonces natives sont prises en charge au format d’affichage standard. Les annonces natives comprennent un titre et/ou un titre, une description, un logo et une image. Les éléments publicitaires sont combinés et rendus de manière à correspondre au style de page de l’éditeur, de sorte que l’annonce publicitaire s’intègre au contenu organique de l’éditeur et génère un engagement plus élevé. Native est particulièrement utile pour la notoriété de la marque et pour stimuler l’affichage de l’audience et les taux d’engagement grâce à une publicité conviviale pour les téléspectateurs. Les indicateurs clés de performance incluent les [!UICONTROL Clicks], [!UICONTROL Cost Per Click], [!UICONTROL Conversions] et [!UICONTROL Cost Per Conversion].

* **Annonces preroll (tierces uniquement)** : les annonces preroll (VAST et VPAID) s’affichent avant le contenu vidéo premium et offrent une expérience client immersive et attrayante. La vidéo preroll peut être interactive, contenir des fonctionnalités de médias riches et inclure des recouvrements, des survols et des appels à l’action. Les indicateurs clés de performance pour les publicités vidéo preroll incluent [!UICONTROL Video Completion Rate] et [!UICONTROL Viewability Rate].

* **Publicités TV connectées (tierces uniquement)** : les publicités TV connectées sont affichées avant et pendant le contenu vidéo TV premium. Tous les stocks de télévisions connectées s’exécutent sur les appareils de télévision, ce qui signifie que la vidéo est lue automatiquement dans un environnement en lecture seule et en plein écran que les spectateurs ne peuvent pas ignorer. Connected TV est le format vidéo numérique le plus proche des publicités TV. Les indicateurs clés de performance pour la télévision connectée incluent les [!UICONTROL Completion Rate].

* **Publicités vidéo universelles (tierces uniquement)** : les publicités vidéo universelles vous permettent de cibler l’inventaire vidéo à partir d’environnements de bureau, mobiles et de télévision connectée pour un inventaire VPAID et VAST à l’aide d’un seul emplacement vidéo. Ils combinent toutes les fonctionnalités des publicités pré-roll, mobiles et TV connectées et sont affichés avant et pendant le contenu vidéo. Les indicateurs clés de performance pour la vidéo universelle incluent la [!UICONTROL Completion Rate] et la [!UICONTROL Viewability Rate].

  Les publicités vidéo universelles ne peuvent être associées qu’à des emplacements vidéo universels.

  Voir « [FAQ sur la vidéo universelle](/help/dsp/campaign-management/faq-universal-video.md) » pour plus d’informations sur les publicités vidéo universelles.

## Approbations d’annonces DSP

Lorsque vous créez une publicité, DSP la passe en revue pour les catégories sensibles, clique sur la fonctionnalité d’URL et prévisualise le rendu.

Au départ, la colonne [!UICONTROL Status] de l’annonce affiche un point rouge. Le processus d&#39;examen dure normalement de 24 à 48 heures. Toutefois, une publicité rompue peut avoir un statut en attente pendant plus de 48 heures afin que vous ayez le temps de corriger les erreurs avant que la publicité ne soit rejetée. Les publicités rejetées incluent un motif de rejet.

Lorsque DSP approuve une publicité, la colonne Statut de la publicité affiche un point vert.

![indicateur de validation dans [!UICONTROL Status] colonne](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Votre publicité ne peut être diffusée que si DSP et le fournisseur de services partagés ont approuvé le contenu publicitaire. Chaque fournisseur de services partagés a ses propres exigences et processus d&#39;approbation.

>[!MORELIKETHIS]
>
>* [Créer une seule annonce publicitaire](ad-create.md)
>* [Créer plusieurs annonces tierces](ad-create-multiple.md)
>* [Spécifications publicitaires](ad-specs.md)
