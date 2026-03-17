---
title: À propos des balises de suivi des conversions d’Adobe Advertising
description: Découvrez comment utiliser les balises de suivi des conversions Adobe Advertising.
exl-id: 8194d5eb-9a5d-4c4e-bb02-e578ffb84d18
feature: Search Tracking
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# À propos des balises de suivi des conversions d’Adobe Advertising

Adobe Advertising effectue le suivi des conversions résultant des clics sur les annonces à l’aide des balises de suivi des conversions Adobe Advertising insérées dans les pages web qui s’ouvrent lorsqu’un événement de conversion se produit, comme une page « succès ». Les balises incluent des informations intégrées pour envoyer les données de transaction, avec le cookie Adobe Advertising de l’utilisateur, à un serveur de suivi, à partir duquel la transaction est créditée au clic publicitaire ou à l’impression publicitaire appropriés (conformément aux paramètres d’attribution de conversion de l’annonceur).

Vous pouvez [générer des balises de suivi des conversions](/help/search-social-commerce/tools/conversion-tag-generate.md) dans Search, Social et Commerce ou utiliser des balises dans Adobe Experience Platform (anciennement appelé Adobe Experience Platform Launch).

>[!NOTE]
>
>Si l’utilisateur ne dispose pas d’un cookie valide, Adobe Advertising ne signale pas la conversion.

Pour chaque ensemble de mesures de conversion que vous souhaitez suivre, vous devez créer et implémenter une balise de conversion distincte. Vous pouvez générer l’un des types de balises de conversion suivants.

* (Recommandé) Balises JavaScript (Version 3 ou Version 2), qui ne sont pas visibles dans les pages web.

* Balises d’image HTML pour afficher sur les pages web des images transparentes d’un pixel sur un pixel (pixels), qui sont invisibles pour les utilisateurs finaux. Utilisez les balises d’image uniquement lorsque la société a une politique contre l’utilisation des balises JavaScript.

Pour plus d’informations sur les différences entre les types de balises, voir « [FAQ sur les balises de suivi de conversion Advertising Cloud](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md) ».

>[!NOTE]
>
>* Cette fonction n’ajoute pas de balises d’image ni de balises JavaScript sur les pages web de l’annonceur. Les balises doivent être ajoutées conformément à la procédure normale de l’annonceur pour la mise à jour des pages web.
>* Veillez à tenir compte du temps nécessaire à l’implémentation des balises. En fonction des politiques de l’entreprise, la mise en œuvre peut prendre des semaines, voire des mois.

## Fonctionnalités des balises de suivi des conversions Adobe Advertising

Le pixel de suivi des conversions permet à Adobe Advertising d’effectuer les opérations suivantes :

* Effectuez le suivi et générez des rapports sur les données de conversion au niveau des mots-clés pour les campagnes de recherche.

* Suivez et générez des rapports sur les données de conversion au niveau des annonces (contenu créatif) sur tous les canaux marketing (référencement payant et affichage), ce qui peut faciliter les tests de contenu créatif.

* Suivez et générez des rapports sur les données de conversion au niveau des transactions sur tous vos canaux marketing.

* Montrez comment vos conversions sont distribuées sur vos différents canaux marketing afin que vous puissiez identifier celui qui est le plus efficace.

* Générez des rapports et optimisez-les sur différents niveaux d’attribution (comme l’attribution de conversions au dernier événement associé ou la pondération uniforme de tous les événements).

* Fournissez de la visibilité sur les aides aux clics (mots-clés de recherche ou emplacements ayant contribué à un funnel de conversion) et les aides aux canaux (événements utilisateur ayant contribué à un funnel de conversion, éventuellement sur plusieurs canaux marketing).

* Fournissez une visibilité sur la distribution géographique et les domaines référents du trafic et des conversions de votre site afin d’affiner le ciblage géographique et de votre site web.

* Analysez les tendances quotidiennes ou intrajournalières afin d’améliorer les taux de conversion.

>[!MORELIKETHIS]
>
>* [Options de suivi des conversions](conversion-tracking-about.md)
>* [Générer et implémenter une balise de conversion Adobe Advertising](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format des balises de suivi des conversions JavaScript version 3](format-conversion-tag-jsv3.md)
>* [Format des balises de suivi des conversions JavaScript version 2](format-conversion-tag-jsv2.md)
>* [Format des balises de tracking de conversion d’images](format-conversion-tag-image.md)
>* [FAQ sur les balises de suivi des conversions et des pages vues](faqs-conversion-page-view-tracking-tags.md)
>* [Balise de mappage de conversion Adobe Advertising JavaScript](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)
