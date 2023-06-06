---
title: À propos des balises de suivi de conversion Adobe Advertising
description: Découvrez comment utiliser les balises de suivi de conversion Adobe Advertising.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# À propos des balises de suivi de conversion Adobe Advertising

Adobe Advertising effectue le suivi des conversions résultant des clics sur les publicités à l’aide des balises de suivi de conversion Adobe Advertising insérées dans les pages web qui s’ouvrent lorsqu’un événement de conversion se produit, par exemple une page &quot;succès&quot;. Les balises comprennent des informations intégrées pour envoyer les données de transaction, ainsi que le cookie Adobe Advertising de l’utilisateur, à un serveur de suivi, à partir duquel la transaction est créditée au clic ou à l’impression de publicité approprié (selon les paramètres d’attribution de conversion de l’annonceur).

>[!NOTE]
>
>Si l’utilisateur ne dispose pas d’un cookie valide, Adobe Advertising ne signale pas la conversion.

Pour chaque ensemble de mesures de conversion dont vous souhaitez effectuer le suivi, vous devez créer une balise de conversion distincte. Fournissez à l’annonceur ou à l’agence la liste des pages Web sur lesquelles insérer chaque balise. Vous pouvez générer l’un des types de balises de conversion suivants. Voir &quot;[Génération d’une balise de conversion Advertising Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)&quot; pour obtenir des instructions.

* (Recommandé) Balises JavaScript (version 3 ou version 2), qui ne sont pas visibles dans les pages web.

* HTML des balises d’image pour afficher des images transparentes de 1 pixel x 1 pixel (pixels), qui sont invisibles pour les utilisateurs finaux, sur les pages web. Utilisez des balises d’image uniquement lorsque l’entreprise a une politique contre l’utilisation de balises JavaScript.

Pour plus d’informations sur les différences entre les types de balises, voir &quot;[Questions fréquentes sur les balises de suivi de conversion Advertising Cloud](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).&quot;

>[!NOTE]
>
>* Cette fonctionnalité n’ajoute pas de balises d’image ou JavaScript aux pages web de l’annonceur. Les balises doivent être ajoutées conformément à la procédure normale de mise à jour des pages web de l’annonceur.
>* Veillez à prendre en compte le temps nécessaire à la mise en oeuvre des balises. Selon les politiques de l’entreprise, la mise en oeuvre peut prendre des semaines, voire des mois.


## Fonctionnalités des balises de suivi de conversion d’Adobe Advertising

Le pixel de suivi de conversion permet à Adobe Advertising d’effectuer les opérations suivantes :

* Effectuez le suivi des données de conversion et créez des rapports au niveau des mots-clés pour les campagnes de recherche.

* Effectuez le suivi et créez des rapports sur les données de conversion au niveau de la publicité (créative) sur tous les canaux marketing (référencement payant et affichage), ce qui peut faciliter les tests créatifs.

* Effectuez le suivi des données de conversion et générez des rapports au niveau des transactions sur tous vos canaux marketing.

* Afficher la manière dont vos conversions sont distribuées sur vos différents canaux marketing afin que vous puissiez voir lequel est le plus efficace.

* Effectuez des rapports et des optimisations sur différents niveaux d’attribution (par exemple, en attribuant des conversions au dernier événement associé ou en pondérant tous les événements de manière uniforme).

* Fournir une visibilité sur les aides aux clics (mots-clés de recherche ou emplacements ayant contribué à un entonnoir de conversion) et aux aides aux canaux (événements utilisateur ayant contribué à un entonnoir de conversion, éventuellement sur plusieurs canaux marketing).

* Fournissez une visibilité sur la répartition géographique et les domaines référents du trafic et des conversions de votre site afin d’affiner le ciblage géographique et de votre site web.

* Analysez les tendances du jour de la semaine ou au cours de la journée, qui peuvent être utilisées pour améliorer les taux de conversion.

>[!MORELIKETHIS]
>
>* [Options de suivi des conversions](conversion-tracking-about.md)
>* [Génération d’une balise de conversion Advertising Adobe](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [Format des balises de suivi de conversion JavaScript version 3](format-conversion-tag-jsv3.md)
>* [Format des balises de suivi de conversion JavaScript version 2](format-conversion-tag-jsv2.md)
>* [Format des balises de suivi de conversion d’image](format-conversion-tag-image.md)
>* [Questions fréquentes sur les balises de suivi de conversion et de pages vues](faqs-conversion-page-view-tracking-tags.md)
>* [Balise de mappage de conversion JavaScript Adobe Advertising](/help/search-social-commerce/tracking/itp-conversion-mapping-tag.md)

