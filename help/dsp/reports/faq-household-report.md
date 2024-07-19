---
title: Questions fréquentes sur les rapports sur les ménages
description: En savoir plus sur la portée, la fréquence et les données de conversion des ménages, y compris sur la différence entre les rapports des ménages et les autres rapports et dépannage.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '921'
ht-degree: 0%

---

# Questions fréquentes sur les rapports sur les ménages

## Rapport [!UICONTROL Household Reach & Frequency]

### En quoi les rapports [!UICONTROL Household Reach & Frequency] sont-ils différents des autres rapports personnalisés ?

Le rapport [!UICONTROL Household Reach & Frequency] mesure la portée, l’impression et la fréquence de différentes dimensions au niveau du foyer en fonction de l’adresse IP. Les autres rapports personnalisés sont générés au niveau de l’appareil ou du cookie.

Par exemple, même si une impression est diffusée sur trois appareils au sein d’un même foyer, la mesure Ménage unique atteint est une.

#### Dimensions prises en charge

Le rapport [!UICONTROL Household Reach & Frequency] prend en charge les [ dimensions suivantes](/help/dsp/reports/report-columns.md) : &quot;[!UICONTROL Campaign]&quot;, &quot;[!UICONTROL Package]&quot;, &quot;[!UICONTROL Placement]&quot;, &quot;[!UICONTROL Site/Apps]&quot; (qui ne permet pas l’accès aux mesures de chevauchement), &quot;[!UICONTROL Media Type]&quot;, &quot;[!UICONTROL Feed Type]&quot;, &quot;[!UICONTROL Device]&quot;, &quot;[!UICONTROL Publisher]&quot;, &quot;[!UICONTROL Audience]&quot;, &quot;[!UICONTROL Creative Length]&quot; et &quot;emplacement créé par l’utilisateur[!UICONTROL Tags].&quot; |

#### Mesures prises en charge

Les [mesures disponibles](/help/dsp/reports/report-columns.md) incluent :

* Mesures de chevauchement : [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)] et [!UICONTROL Unique Household (Overlap)].

  Les mesures de chevauchement sont les valeurs qui se produisent uniquement pour la dimension signalée ou la combinaison de dimensions, et non pour les autres dimensions. <!-- For example, it might show the ?? -->

* Mesures autres que les chevauchements : [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions] et [!UICONTROL Unique Household Reached]

Les mesures de conversion et les objectifs personnalisés ne sont pas pris en charge.

### Quelle est la différence entre les mesures de chevauchement et de non-chevauchement ?

La figure suivante présente trois mesures (Ménage unique atteint, Ménage incrémentiel atteint et Ménage incrémentiel (chevauchement))) pour trois campagnes (A, B et C).

![Illustration des mesures de chevauchement des ménages](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustration des mesures de chevauchement des ménages")

* Le Ménage unique atteint (total) fournit le Ménage unique atteint par chacune des campagnes ou la zone totale de chacun des cercles. Sur la figure, Ménage unique atteint par A = Ménage incrémentiel atteint par A + (A+B) + (A+C) +(A+B+C)

* Le foyer incrémentiel atteint est le foyer unique atteint uniquement par une campagne. Dans la figure, les ménages incrémentiels atteints par A, B, C sont les ménages incrémentiels atteints par A, B, C, respectivement.

* Foyer incrémentiel (chevauchement) est le foyer unique atteint par la campagne ou la combinaison de campagnes. Sur la figure, le Ménage incrémentiel atteint par A, C est A+C.

### Workflow

Suivez les étapes normales pour [créer un rapport personnalisé](report-create.md).

Le rapport [!UICONTROL Household Reach & Frequency] ne peut inclure qu’une seule dimension. Il peut également inclure a) des mesures de chevauchement par dimension, à l’exception de Site/Applications ou b) des mesures de non-chevauchement, mais pas les deux.

### Quelles sont certaines limites du rapport [!UICONTROL Household Reach & Frequency] ?

Les rapports avec des mesures de chevauchement génèrent des intersections de trois valeurs au maximum. Si, par exemple, vous utilisez la mesure [!UICONTROL Unique Household (Overlap)] pour 10 emplacements, vous pouvez voir les ménages uniques atteints par des emplacements individuels, les ménages communs atteints par une combinaison de deux emplacements ou les ménages communs atteints par une combinaison de trois emplacements. Vous ne pouvez pas voir les foyers courants atteints par quatre emplacements ou plus.

Pour les dimensions autres que la campagne, le package ou l’emplacement, le rapport prend en charge jusqu’à 10 valeurs dans chaque dimension. Par exemple, pour générer un rapport [!UICONTROL Unique Household Reached] pour la dimension [!UICONTROL Audience], le nombre d’audiences uniques doit être inférieur ou égal à 10. Si vous incluez plus de 10 audiences uniques, un rapport vierge est généré.

### Pourquoi la fréquence et les valeurs de portée uniques sont-elles différentes entre mes rapports [!UICONTROL Custom] et le rapport [!UICONTROL Household Reach & Frequency] ?

Ces mesures dans les rapports [!UICONTROL Household] sont calculées à l’aide du nombre réel d’adresses IP, tandis que les mesures dans le rapport [!UICONTROL Custom] utilisent des nombres estimés calculés à l’aide de modèles. Toutefois, l’écart doit être inférieur à 10 %.

### Comment configurer le rapport pour la dimension [!UICONTROL Placement Tags] ?

Pour créer des balises pour l’emplacement, [ouvrez les paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-edit.md) et saisissez des valeurs dans le [champ Balises d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

Lorsqu’un emplacement comprend plusieurs balises, le rapport considère la chaîne entière comme une balise. Le rapport comprend une ligne pour chaque chaîne unique.

## Rapport [!UICONTROL Household Conversions]

### Quels sont les types de méthodes d’attribution pris en charge dans le rapport [!UICONTROL Household Conversions] ?

Deux types de méthodes d’attribution sont pris en charge :

* [!UICONTROL Unique] : compte le nombre de fois qu’une valeur de dimension (un appareil ou un emplacement, par exemple) a été sur le chemin de la conversion.

* [!UICONTROL Multi-Touch Attribution (MTA)] : distribue le crédit de chaque conversion en fonction de la fréquence d’occurrence de la valeur de dimension (un appareil ou un emplacement, par exemple) sur le chemin de conversion. Par exemple, s’il y avait un total de 10 impressions avant conversion, dont 8 sur CTV et 2 sur Mobile, alors 80 % du crédit (0,8) est attribué aux écrans CTV et 0,2 à Mobile.

### En quoi les rapports de conversion des ménages diffèrent-ils des rapports d’affichage publicitaire CTV dans Adobe Analytics ?

Les données d’affichage publicitaire CTV dans [!DNL Analytics] optimisent le suivi [!DNL Analytics], et les données de conversion des ménages utilisent les données collectées à l’aide du suivi de conversion des Adobes Advertising. En outre, la logique d’attribution DSP dans [!DNL Analytics] utilise uniquement le dernier événement, mais les rapports de conversion des ménages prennent en charge deux méthodes d’attribution différentes : Unique et MTA.

### Puis-je afficher les données d’affichage publicitaire CTV dans [!DNL Analytics for Advertising] et dans les rapports personnalisés ?

Les annonceurs qui ne disposent pas de [!DNL Analytics for Advertising] peuvent utiliser uniquement le rapport Conversion de foyer pour les rapports de conversion de foyer.

Si votre organisation possède [!DNL Analytics for Advertising], utilisez les deux types de rapports ensemble. Bien que les rapports d’affichage publicitaire CTV soient adaptés à l’analyse de canaux larges, au comportement du site, etc., les rapports personnalisés offrent une vue granulaire (avec des données ventilées par type de média, éditeurs, etc.) pour indiquer les facteurs qui génèrent les taux de conversion.

## [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] Rapports et données provenant de [!DNL Advanced Measurement Services]

Pour des rapports avancés sur la portée et la fréquence des conversions basées sur les ménages, l&#39;[[!DNL Strategic Advertising Consulting] équipe](/help/dsp/introduction/advanced-measurement-services.md) peut fournir des rapports hautement personnalisables ainsi que des recommandations stratégiques holistiques. Pour plus d’informations sur [!DNL Advanced Measurement Services], contactez votre équipe de compte d’Adobe.

### Si j’utilise déjà [!DNL Advanced Measurement Services], pourquoi dois-je utiliser les rapports [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] ?

Les rapports [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] permettent aux clients d’extraire de manière autonome en temps réel les mesures de portée, de fréquence et de conversion au niveau du foyer.

### Puis-je utiliser les rapports [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] et [!DNL Advanced Measurement Services] ?

Le cas d’utilisation idéal consiste à utiliser conjointement le rapport [!UICONTROL Household] et les services de reporting et de conseil [!DNL Advanced Measurement Services]. Considérez le rapport [!UICONTROL Household] comme transactionnel, destiné à informer les optimisations au jour le jour, et [!DNL Advanced Measurement Services] comme plus stratégique, destiné à informer les leçons et les enseignements holistiques liés aux objectifs commerciaux globaux.

>[!MORELIKETHIS]
>
>* [À propos des rapports personnalisés](/help/dsp/reports/report-about.md)
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Modifier un rapport personnalisé](/help/dsp/reports/report-edit.md)
>* [Paramètres de rapport personnalisés](/help/dsp/reports/report-settings.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)
