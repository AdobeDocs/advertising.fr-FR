---
title: Questions fréquentes à propos de [!UICONTROL Household] Rapport
description: En savoir plus sur les [!UICONTROL Household] , y compris la façon dont il diffère des autres rapports et la résolution des problèmes.
source-git-commit: d88ea4ab2ad4a2ee54475346a24724b766b024fc
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 0%

---

# Questions fréquentes à propos de [!UICONTROL Household] Rapport

## Comment [!UICONTROL Household] rapports de portée et de fréquence différents des autres rapports personnalisés ?

Le [!UICONTROL Household] mesure la portée, l’impression et la fréquence des rapports sur différentes dimensions au niveau du foyer en fonction de l’adresse IP. Les autres rapports personnalisés sont générés au niveau de l’appareil ou du cookie.

Par exemple, même si une impression est diffusée sur trois appareils au sein d’un même foyer, la mesure Ménage unique atteint est une.

### Dimensions prises en charge

Le [!UICONTROL Household] prend en charge la variable [dimensions suivantes](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot;[!UICONTROL Package],&quot;[!UICONTROL Placement],&quot;[!UICONTROL Site/Apps]&quot; (qui ne permet pas d’accéder aux mesures de chevauchement), &quot;[!UICONTROL Media Type],&quot;[!UICONTROL Feed Type],&quot;[!UICONTROL Device],&quot;[!UICONTROL Publisher],&quot;[!UICONTROL Audience],&quot;[!UICONTROL Creative Length],&quot; et placement créé par l’utilisateur &quot;[!UICONTROL Tags].&quot; |

### Mesures prises en charge

Le [mesures disponibles](/help/dsp/reports/report-columns.md) inclure :

* Mesures de chevauchement : [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], et [!UICONTROL Unique Household (Overlap)].

   Les mesures de chevauchement sont les valeurs qui se produisent uniquement pour la dimension signalée ou la combinaison de dimensions, et non pour les autres dimensions. <!-- For example, it might show the ?? -->

* Mesures autres que les chevauchements : [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], et [!UICONTROL Unique Household Reached]

Les mesures de conversion et les objectifs personnalisés ne sont pas pris en charge.

## Quelle est la différence entre les mesures de chevauchement et de non-chevauchement ?

La figure suivante présente trois mesures (Ménage unique, Ménage incrémentiel et Ménage incrémentiel (Chevauchement)) pour trois campagnes (A, B et C).

![Illustration des mesures de chevauchement des ménages](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustration des mesures de chevauchement des ménages")

* Le Ménage unique atteint (total) fournit le Ménage unique atteint par chacune des campagnes ou la zone totale de chacun des cercles. Sur la figure, Ménage unique atteint par A = Ménage incrémentiel atteint par A + (A+C) + (A+B) +(A+B+C)

* Le foyer incrémentiel atteint est le foyer unique atteint uniquement par une campagne. Dans la figure, les ménages incrémentiels atteints par A, B, C sont les ménages incrémentiels atteints par A, B, C, respectivement.

* Foyer incrémentiel (chevauchement) est le foyer unique atteint par la campagne ou la combinaison de campagnes. Dans la figure, le Ménage incrémentiel atteint par A, C est A+C.

## Workflow

Suivez les étapes normales pour [création d’un rapport personnalisé](report-create.md).

Le [!UICONTROL Household] ne peut inclure qu’une seule dimension. Il peut également inclure a) des mesures de chevauchement par dimension, à l’exception de Site/Applications ou b) des mesures de non-chevauchement, mais pas les deux.

## Quelles sont les limites de la variable [!UICONTROL Household] rapport ? 

Les rapports avec des mesures de chevauchement génèrent des intersections de trois valeurs au maximum. Par exemple, si vous utilisez la mesure [!UICONTROL Unique Household (Overlap)] pour 10 emplacements, vous pouvez ensuite voir les ménages uniques atteints par des emplacements individuels, les ménages communs atteints par une combinaison de deux emplacements, ou les ménages communs atteints par une combinaison de trois emplacements. Vous ne pouvez pas voir les foyers courants atteints par quatre emplacements ou plus.

Pour les dimensions autres que la campagne, le package ou l’emplacement, le rapport prend en charge jusqu’à 10 valeurs dans chaque dimension. Par exemple, pour générer une [!UICONTROL Unique Household Reached] pour le rapport [!UICONTROL Audience] , le nombre d’audiences uniques doit être inférieur ou égal à 10. Si vous incluez plus de 10 audiences uniques, un rapport vierge est généré.

## Pourquoi la fréquence et les valeurs de portée uniques sont-elles différentes entre mes [!UICONTROL Custom] et le rapport [!UICONTROL Household] rapport ?

Ces mesures dans [!UICONTROL Household] Les rapports sont calculés à l’aide du nombre réel d’adresses IP, tandis que les mesures de la variable [!UICONTROL Custom] le rapport utilise des nombres estimés calculés à l’aide de modèles. Toutefois, l’écart doit être inférieur à 10 %.

## Comment configurer le rapport pour la variable [!UICONTROL Placement Tags] dimension ?

Pour créer des balises pour l’emplacement, [ouvrir les paramètres d’emplacement ;](/help/dsp/campaign-management/placements/placement-edit.md) et saisissez les valeurs dans le champ [Champ Balises de placement](/help/dsp/campaign-management/placements/placement-settings.md).
 
Lorsqu’un emplacement comprend plusieurs balises, le rapport considère la chaîne entière comme une balise. Le rapport comprend une ligne pour chaque chaîne unique.

## [!UICONTROL Household] Comparaison entre les rapports et les données de [!DNL Advanced Measurement Services]

Pour des rapports avancés sur la portée et la fréquence des ménages, la variable [[!DNL Strategic Advertising Consulting] équipe](/help/dsp/introduction/advanced-measurement-services.md) peuvent fournir des rapports hautement personnalisables ainsi que des recommandations stratégiques globales. Pour plus d’informations sur [!DNL Advanced Measurement Services], contactez votre équipe de compte d’Adobe.

### Si j’utilise déjà [!DNL Advanced Measurement Services], pourquoi utiliser la variable [!UICONTROL Household] rapport ?

Le [!UICONTROL Household] Le rapport permet aux clients d’extraire de manière autonome en temps réel les mesures de portée et de fréquence au niveau du foyer.

### Puis-je utiliser les deux [!UICONTROL Household] rapport et [!DNL Advanced Measurement Services]? 

Le cas d’utilisation idéal consiste à utiliser les deux [!UICONTROL Household] et le rapport [!DNL Advanced Measurement Services] les services de reporting et de consulting ensemble. Considérez la variable [!UICONTROL Household] le rapport sous la forme d’un rapport transactionnel, destiné à informer les optimisations quotidiennes ; et [!DNL Advanced Measurement Services] plus stratégiques, destinées à informer les leçons et les enseignements holistiques liés aux objectifs généraux de l&#39;entreprise.

>[!MORELIKETHIS]
>
>* [À propos des rapports personnalisés](/help/dsp/reports/report-about.md)
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Modifier un rapport personnalisé](/help/dsp/reports/report-edit.md)
>* [Paramètres des rapports personnalisés](/help/dsp/reports/report-settings.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)

