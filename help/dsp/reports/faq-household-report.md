---
title: Questions fréquentes sur les rapports sur les ménages
description: En savoir plus sur la portée, la fréquence et les données de conversion des ménages, y compris sur la différence entre les rapports des ménages et les autres rapports et dépannage.
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
source-git-commit: ae6028d7dc9b35906e4abcd727b84b169e5594b1
workflow-type: tm+mt
source-wordcount: '914'
ht-degree: 0%

---

# Questions fréquentes sur les rapports sur les ménages

## Le [!UICONTROL Household Reach & Frequency] Rapport

### Comment [!UICONTROL Household Reach & Frequency] rapports différents des autres rapports personnalisés ?

Le [!UICONTROL Household Reach & Frequency] mesure la portée, l’impression et la fréquence des rapports sur différentes dimensions au niveau du foyer en fonction de l’adresse IP. Les autres rapports personnalisés sont générés au niveau de l’appareil ou du cookie.

Par exemple, même si une impression est diffusée sur trois appareils au sein d’un même foyer, la mesure Ménage unique atteint est une.

#### Dimensions prises en charge

Le [!UICONTROL Household Reach & Frequency] prend en charge la variable [dimensions suivantes](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot;[!UICONTROL Package],&quot;[!UICONTROL Placement],&quot;[!UICONTROL Site/Apps]&quot; (qui ne permet pas d’accéder aux mesures de chevauchement), &quot;[!UICONTROL Media Type],&quot;[!UICONTROL Feed Type],&quot;[!UICONTROL Device],&quot;[!UICONTROL Publisher],&quot;[!UICONTROL Audience],&quot;[!UICONTROL Creative Length],&quot; et placement créé par l’utilisateur &quot;[!UICONTROL Tags].&quot; |

#### Mesures prises en charge

Le [mesures disponibles](/help/dsp/reports/report-columns.md) inclure :

* Mesures de chevauchement : [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)], et [!UICONTROL Unique Household (Overlap)].

  Les mesures de chevauchement sont les valeurs qui se produisent uniquement pour la dimension signalée ou la combinaison de dimensions, et non pour les autres dimensions. <!-- For example, it might show the ?? -->

* Mesures autres que les chevauchements : [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions], et [!UICONTROL Unique Household Reached]

Les mesures de conversion et les objectifs personnalisés ne sont pas pris en charge.

### Quelle est la différence entre les mesures de chevauchement et de non-chevauchement ?

La figure suivante présente trois mesures (Ménage unique atteint, Ménage incrémentiel atteint et Ménage incrémentiel (chevauchement))) pour trois campagnes (A, B et C).

![Illustration des mesures de chevauchement des ménages](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustration des mesures de chevauchement des ménages")

* Le Ménage unique atteint (total) fournit le Ménage unique atteint par chacune des campagnes ou la zone totale de chacun des cercles. Sur la figure, Ménage unique atteint par A = Ménage incrémentiel atteint par A + (A+B) + (A+C) +(A+B+C)

* Le foyer incrémentiel atteint est le foyer unique atteint uniquement par une campagne. Dans la figure, les ménages incrémentiels atteints par A, B, C sont les ménages incrémentiels atteints par A, B, C, respectivement.

* Foyer incrémentiel (chevauchement) est le foyer unique atteint par la campagne ou la combinaison de campagnes. Sur la figure, le Ménage incrémentiel atteint par A, C est A+C.

### Workflow

Suivez les étapes normales pour [création d’un rapport personnalisé](report-create.md).

Le [!UICONTROL Household Reach & Frequency] ne peut inclure qu’une seule dimension. Il peut également inclure a) des mesures de chevauchement par dimension, à l’exception de Site/Applications ou b) des mesures de non-chevauchement, mais pas les deux.

### Quelles sont les limites de la variable [!UICONTROL Household Reach & Frequency] rapport ?

Les rapports avec des mesures de chevauchement génèrent des intersections de trois valeurs au maximum. Par exemple, si vous utilisez la mesure [!UICONTROL Unique Household (Overlap)] pour 10 emplacements, vous pouvez ensuite voir les ménages uniques atteints par des emplacements individuels, les ménages communs atteints par une combinaison de deux emplacements, ou les ménages communs atteints par une combinaison de trois emplacements. Vous ne pouvez pas voir les foyers courants atteints par quatre emplacements ou plus.

Pour les dimensions autres que la campagne, le package ou l’emplacement, le rapport prend en charge jusqu’à 10 valeurs dans chaque dimension. Par exemple, pour générer une [!UICONTROL Unique Household Reached] pour le rapport [!UICONTROL Audience] , le nombre d’audiences uniques doit être inférieur ou égal à 10. Si vous incluez plus de 10 audiences uniques, un rapport vierge est généré.

### Pourquoi la fréquence et les valeurs de portée uniques sont-elles différentes entre mes [!UICONTROL Custom] et le rapport [!UICONTROL Household Reach & Frequency] rapport ?

Ces mesures dans [!UICONTROL Household] Les rapports sont calculés à l’aide du nombre réel d’adresses IP, tandis que les mesures de la variable [!UICONTROL Custom] le rapport utilise des nombres estimés calculés à l’aide de modèles. Toutefois, l’écart doit être inférieur à 10 %.

### Comment configurer le rapport pour la variable [!UICONTROL Placement Tags] dimension ?

Pour créer des balises pour l’emplacement, [ouvrir les paramètres d’emplacement ;](/help/dsp/campaign-management/placements/placement-edit.md) et saisissez les valeurs dans le champ [Champ Balises de placement](/help/dsp/campaign-management/placements/placement-settings.md).

Lorsqu’un emplacement comprend plusieurs balises, le rapport considère la chaîne entière comme une balise. Le rapport comprend une ligne pour chaque chaîne unique.

## Le [!UICONTROL Household Conversions] Rapport

### Quels sont les types de méthodes d’attribution pris en charge dans [!UICONTROL Household Conversions] rapport ?

Deux types de méthodes d’attribution sont pris en charge :

* Unique : Compte le nombre de fois où une valeur de dimension (un appareil ou un emplacement, par exemple) se trouvait sur le chemin de la conversion.

* MTA (Attribution multi-écrans) : Distribue le crédit de chaque conversion en fonction de la fréquence d’occurrence de la valeur de dimension (un appareil ou un emplacement, par exemple) sur le chemin de conversion. Par exemple, s’il y avait un total de 10 impressions avant conversion, dont 8 sur CTV et 2 sur Mobile, alors 80 % du crédit (0,8) est attribué aux écrans CTV et 0,2 à Mobile.

### En quoi les rapports de conversion des ménages diffèrent-ils des rapports d’affichage publicitaire CTV dans Adobe Analytics ?

Données d’affichage publicitaire CTV dans [!DNL Analytics] est alimenté [!DNL Analytics] et les données de conversion des ménages utilisent les données collectées à l’aide du suivi de conversion des Adobes Advertising. En outre, la logique d’attribution DSP dans [!DNL Analytics] utilise uniquement le dernier événement, mais la création de rapports de conversion des ménages prend en charge deux méthodes d’attribution différentes : Unique et MTA.

### Puis-je afficher les données d’affichage publicitaire CTV dans les deux [!DNL Analytics for Advertising] et dans les rapports personnalisés ?

Annonceurs sans [!DNL Analytics for Advertising] Vous ne pouvez utiliser que le rapport Conversion de foyer pour les rapports de conversion de foyer.

Si votre entreprise dispose des [!DNL Analytics for Advertising], utilisez les deux types de rapports ensemble. Bien que les rapports d’affichage publicitaire CTV soient adaptés à l’analyse de canaux larges, au comportement du site, etc., les rapports personnalisés offrent une vue granulaire (avec des données ventilées par type de média, éditeurs, etc.) pour indiquer les facteurs qui entraînent les taux de conversion.

## [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] Rapports et données provenant de [!DNL Advanced Measurement Services]

Pour des rapports avancés sur la portée et la fréquence des conversions basées sur les ménages, la variable [[!DNL Strategic Advertising Consulting] équipe](/help/dsp/introduction/advanced-measurement-services.md) peuvent fournir des rapports hautement personnalisables ainsi que des recommandations stratégiques globales. Pour plus d’informations sur [!DNL Advanced Measurement Services], contactez votre équipe de compte d’Adobe.

### Si j’utilise déjà [!DNL Advanced Measurement Services], pourquoi utiliser la variable [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] rapports ?

Le [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] Les rapports permettent aux clients d’extraire de manière autonome en temps réel les mesures de portée, de fréquence et de conversion au niveau du foyer.

### Puis-je utiliser les deux [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] rapports et [!DNL Advanced Measurement Services]?

Le cas d’utilisation idéal consiste à utiliser les deux [!UICONTROL Household] et le rapport [!DNL Advanced Measurement Services] les services de reporting et de consulting ensemble. Considérez la variable [!UICONTROL Household] le rapport sous la forme d’un rapport transactionnel, destiné à informer les optimisations quotidiennes ; et [!DNL Advanced Measurement Services] plus stratégiques, destinées à informer les leçons et les enseignements holistiques liés aux objectifs généraux de l&#39;entreprise.

>[!MORELIKETHIS]
>
>* [À propos des rapports personnalisés](/help/dsp/reports/report-about.md)
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Modifier un rapport personnalisé](/help/dsp/reports/report-edit.md)
>* [Paramètres des rapports personnalisés](/help/dsp/reports/report-settings.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)
