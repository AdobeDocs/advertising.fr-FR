---
title: Questions fréquentes sur les rapports personnalisés
description: En savoir plus sur les rapports personnalisés, y compris les rapports ménagers et les rapports d’analyse des chemins de conversion.
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: a1ece707f43af4a6a3fc5573e41c75622f9b502f
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 0%

---

# Questions fréquentes sur les rapports personnalisés

## Rapports sur les ménages

### Le rapport [!UICONTROL Household Reach & Frequency]

#### En quoi les rapports [!UICONTROL Household Reach & Frequency] diffèrent-ils des autres rapports personnalisés ?

Le rapport [!UICONTROL Household Reach & Frequency] mesure la portée, l’impression et la fréquence sur différentes dimensions au niveau d’un foyer en fonction de l’adresse IP. Les autres rapports personnalisés sont générés au niveau de l’appareil ou du cookie.

Par exemple, même si une impression est transmise à trois appareils au sein d’un foyer, la mesure Ménage unique atteint en est une.

##### Dimensions prises en charge

Le rapport [!UICONTROL Household Reach & Frequency] prend en charge les [dimensions suivantes](/help/dsp/reports/report-columns.md) : « [!UICONTROL Campaign] », « [!UICONTROL Package] », « [!UICONTROL Placement] », « [!UICONTROL Site/Apps] » (qui ne permet pas d’accéder aux mesures de chevauchement), « [!UICONTROL Media Type] », « [!UICONTROL Feed Type] », « [!UICONTROL Device] », « [!UICONTROL Publisher] », « [!UICONTROL Audience] », « [!UICONTROL Creative Length] » et l’emplacement créé par l’utilisateur ou l’utilisatrice « [!UICONTROL Tags] ». |

##### Mesures prises en charge

Les [mesures disponibles](/help/dsp/reports/report-columns.md) incluent :

* Mesures de chevauchement : [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)] et [!UICONTROL Unique Household (Overlap)].

  Les mesures de chevauchement sont les valeurs qui se produisent uniquement pour la dimension ou la combinaison de dimensions signalée, et non pour d’autres dimensions. <!-- For example, it might show the ?? -->

* Mesures ne se chevauchant pas : [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions] et [!UICONTROL Unique Household Reached]

Les mesures de conversion et les objectifs personnalisés ne sont pas pris en charge.

#### Quelle est la différence entre les mesures de chevauchement et de non-chevauchement ?

La figure suivante montre trois mesures (Ménage unique atteint, Ménage incrémentiel atteint et Ménage incrémentiel (Chevauchement)) pour trois campagnes (A, B et C).

![Illustration des mesures de chevauchement des ménages](/help/dsp/assets/household-overlap-metrics-illustration.png "Illustration des mesures de chevauchement des ménages")

* Ménage unique atteint (total) indique le Ménage unique atteint par chacune des campagnes ou la surface totale de chacun des cercles. Dans la figure, Ménage unique atteint par A = Ménage incrémental atteint par A + (A+B) + (A+C) + (A+B+C)

* Ménage incrémentiel atteint est le ménage unique qui a été atteint uniquement par une campagne. Dans la figure, les ménages incrémentiels atteints par A, B, C sont les ménages incrémentiels atteints par A, B, C respectivement.

* Ménage incrémentiel (chevauchement) est le ménage unique atteint par la campagne ou la combinaison de campagnes. Dans la figure, le ménage supplémentaire atteint par A, C est A+C.

#### Workflow

Suivez les étapes normales pour [créer un rapport personnalisé](report-create.md).

Le rapport [!UICONTROL Household Reach & Frequency] ne peut inclure qu’une seule dimension. Il peut également inclure a) des mesures de chevauchement par n’importe quelle dimension, à l’exception de Site/Applications, ou b) des mesures sans chevauchement, mais pas les deux.

#### Quelles sont les limites du rapport [!UICONTROL Household Reach & Frequency] ?

Rapports avec des intersections de sortie de mesures de chevauchement pouvant prendre jusqu’à trois valeurs. Par exemple, si vous utilisez la mesure [!UICONTROL Unique Household (Overlap)] pour 10 emplacements, vous pouvez voir les ménages uniques atteints par des emplacements individuels, les ménages communs atteints par une combinaison de deux emplacements, et les ménages communs atteints par des combinaisons de trois emplacements. Vous ne pouvez pas voir des ménages communs atteints par quatre emplacements ou plus.

Pour les dimensions autres que campagne, package ou emplacement, le rapport prend en charge jusqu’à 10 valeurs dans chaque dimension. Par exemple, pour générer un rapport [!UICONTROL Unique Household Reached] pour la dimension [!UICONTROL Audience] , le nombre d’audiences uniques doit être inférieur ou égal à 10. Si vous incluez plus de 10 audiences uniques, un rapport vierge est généré.

#### Pourquoi les valeurs de fréquence et d’étendue unique sont-elles différentes entre mes rapports [!UICONTROL Custom] et le rapport [!UICONTROL Household Reach & Frequency] ?

Ces mesures dans les rapports [!UICONTROL Household] sont calculées à l’aide du nombre réel d’adresses IP, tandis que les mesures du rapport [!UICONTROL Custom] utilisent des nombres estimés calculés à l’aide de modèles. Toutefois, l’écart devrait être inférieur à 10 %.

#### Comment configurer le rapport pour la dimension [!UICONTROL Placement Tags] ?

Pour créer des balises pour l&#39;emplacement, [ouvrez les paramètres d&#39;emplacement](/help/dsp/campaign-management/placements/placement-edit.md) et saisissez des valeurs dans le champ [Balises d&#39;emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

Lorsqu’un emplacement inclut plusieurs balises, le rapport considère l’ensemble de la chaîne comme une seule balise. Le rapport comprend une ligne pour chaque chaîne unique.

### Le rapport [!UICONTROL Household Conversions]

#### Quelles méthodes d’attribution sont prises en charge dans [!UICONTROL Household Conversions] rapport ?

Deux types de méthodes d’attribution sont pris en charge :

* [!UICONTROL Unique] : compte le nombre de fois qu’une valeur de dimension (un appareil ou un emplacement, par exemple) a été sur le chemin de conversion.

* [!UICONTROL Multi-Touch Attribution (MTA)] : distribue le crédit de chaque conversion en fonction de la fréquence d’occurrence de la valeur de dimension (telle qu’un appareil ou un emplacement) sur le chemin d’accès vers la conversion. Par exemple, s’il y avait un total de 10 impressions avant la conversion, avec 8 sur CTV et 2 sur Mobile, alors 80 % du crédit (0,8) est attribué aux écrans de CTV et 0,2 à Mobile.

#### En quoi les rapports de conversion des ménages diffèrent-ils des rapports d’affichage publicitaire de CTV dans Adobe Analytics ?

* En [!DNL Analytics], le rapport [!DNL CTV View-Through Conversion] indique le nombre de conversions pour lesquelles une impression CTV était le dernier point de contact avant la conversion. En revanche, le rapport DSP [!UICONTROL Household Conversions] indique le nombre de foyers uniques qui ont été exposés à une impression CTV à tout moment dans l’intervalle de recherche en amont défini avant la conversion.

* Dans [!DNL Analytics], la logique d’attribution attribue des conversions exclusivement au dernier point de contact d’Adobe Advertising. En revanche, le rapport [!UICONTROL Household Conversions] de DSP prend en charge des modèles d’attribution supplémentaires, *[!UICONTROL Unique]* et *[!UICONTROL Multi-Touch Attribution (MTA)]*.

* [!DNL Analytics] données de rapport sont particulièrement utiles pour l’analyse par canaux marketing, mesures d’engagement du site, etc. Le rapport [!UICONTROL Household Conversions] de DSP offre des informations plus granulaires en permettant la division des données de conversion en différentes dimensions, telles que le type de média et l’éditeur.

### Rapports [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] par rapport aux données provenant de l’[!DNL Advanced Measurement Services]

Pour des rapports avancés sur la portée et la fréquence des conversions à domicile, l’équipe [[!DNL Strategic Advertising Consulting] team](/help/dsp/introduction/advanced-measurement-services.md) peut fournir des rapports hautement personnalisables ainsi que des recommandations stratégiques holistiques. Pour plus d’informations sur [!DNL Advanced Measurement Services], contactez l’équipe chargée de votre compte Adobe.

#### Si j’utilise déjà [!DNL Advanced Measurement Services], pourquoi devrais-je utiliser les rapports [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] ?

Les rapports [!UICONTROL Household Reach & Frequency] et [!UICONTROL Household Conversions] permettent aux clients d’extraire respectivement de manière autonome en temps réel les mesures de portée, de fréquence et de conversion au niveau du foyer.

#### Puis-je utiliser les rapports et [!UICONTROL Household Reach & Frequency] [!UICONTROL Household Conversions] et [!DNL Advanced Measurement Services] ?

Le cas d’utilisation idéal consiste à utiliser à la fois le rapport [!UICONTROL Household] et les services de reporting et de conseil [!DNL Advanced Measurement Services]. Considérez le rapport [!UICONTROL Household] comme transactionnel, destiné à éclairer les optimisations quotidiennes. Il s’[!DNL Advanced Measurement Services] comme plus stratégique, destiné à informer des apprentissages et des points à retenir holistiques liés à des objectifs commerciaux globaux.

## Rapports d’analyse des chemins de conversion

### Comment le rapport Chemin d’accès à la conversion se compare-t-il aux rapports créés par [!DNL Advanced Measurement Services] et Adobe Analytics Analysis Workspace ?

| | Chemin vers le rapport de conversion | Effet Halo des services de mesure avancés sur les rapports de recherche | Rapports dans Analysis Workspace |
| --- | --- | --- |---|
| Valeur client | Générez un rapport personnalisé en libre-service pour identifier les chemins du parcours publicitaire qui ont conduit à davantage de conversions afin d’améliorer l’optimisation. | Comprendre l’influence des tactiques de télévision connectée (CTV) sur les clics de recherche | Découvrez l’influence de votre investissement holistique dans Adobe Advertising, aux côtés d’autres canaux marketing, sur les clics de recherche |
| Niveau Du Ménage | Oui | Oui | Non |
| CTV est-il pris en charge ? | Oui | Oui | Oui |
| Méthodologie d’attribution | L’événement de dernière touche (impression ou clic) doit se trouver dans la fenêtre du lookbook. | Uniques | Dernière touche |
| | Les points d’interaction plus de 30 jours avant l’événement de dernière touche sont pris en compte pour le chemin de conversion. | (CTV reçoit du crédit, quel que soit l’endroit où l’exposition au CTV se produit dans le chemin de l’utilisateur pour cliquer) | (CTV reçoit du crédit si l&#39;impression est le dernier événement dans l&#39;intervalle de recherche en amont ET qu&#39;il n&#39;y a pas de clic payant provenant d&#39;autres formats avant ou après l&#39;exposition à CTV) |
| Niveau de reporting | Granulaire | Granulaire | Large |
| | (Type De Canal, Creative/Publicité, Mot-Clé, Chemins, Longueur, Délai De Conversion) | (CTV Tactic, CTV App/Publisher) | (Adobe Advertising et autres canaux marketing) |
| Canaux marketing | DSP + Recherche (à partir de Recherche, Social et Commerce) | DSP + Recherche (à partir de Recherche, Social et Commerce) | Canaux marketing non suivis par l’identifiant de l’EF de clics Adobe Advertising (recherche organique, réseaux sociaux organiques, e-mail et affilié, par exemple) |
| Mesures de conversion prises en charge | Mesures suivies à l’aide du pixel d’événement Adobe Advertising (AMO ID) et du suivi Adobe Analytics | Clics (aucune conversion) | Mesures suivies à l’aide du suivi Adobe Analytics |

Pour plus d’informations sur l’effet Halo d’Advanced Measurement Services sur les rapports de recherche, voir « [Advanced Measurement Services](/help/dsp/introduction/advanced-measurement-services.md) ».

>[!MORELIKETHIS]
>
>* [À propos des rapports personnalisés](/help/dsp/reports/report-about.md)
>* [Créer un rapport personnalisé](/help/dsp/reports/report-create.md)
>* [Modifier un rapport personnalisé](/help/dsp/reports/report-edit.md)
>* [Paramètres de rapport personnalisés](/help/dsp/reports/report-settings.md)
>* [Colonnes de rapport disponibles](/help/dsp/reports/report-columns.md)
