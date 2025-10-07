---
title: Champs disponibles pour les fichiers dynamiques et de flux
description: Découvrez les champs que vous pouvez inclure dans les fichiers de flux que vous utilisez pour créer des annonces dynamiques.
feature: Creative Dynamic Creatives
source-git-commit: 67ee38860ac5cb7e9340f8e9d4667353e509b1ec
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Annexe : champs disponibles pour les fichiers dynamiques et de flux

Les champs de flux suivants sont disponibles sur le serveur principal d’Advertising Creative. Vous pouvez charger un [fichier de flux](/help/creative/feeds/asset-manage.md) qui utilise des noms de champ spécifiques à votre organisation. Cependant, avant de pouvoir créer un [catalogue](/help/creative/feeds/catalog-manage.md) à partir de votre fichier de flux, vous devez mapper chaque champ du fichier de flux à l’un des champs suivants du [modèle de flux](/help/creative/feeds/feed-template-manage.md) que vous utiliserez pour créer le catalogue.

Le seul champ qui doit avoir un équivalent dans votre fichier de flux est `PART_NUM`.

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| Nom du champ | Type de données | Obligatoire ? |
|------------|-----------|-----------|
| PART_NUM | varchar(64) | OUI |
| PRODUCT_NAME | texte | NON |
| PRODUCT_URL | texte | NON |
| PRIX | decimal(10,2) | NON |
| PRIX_REMISE | decimal(10,2) | NON |
| IMAGE | varchar(1024) | NON |
| IMAGE_HEIGHT | int | NON |
| IMAGE_WIDTH | int | NON |
| IMAGE_1 | varchar(1024) | NON |
| IMAGE_2 | varchar(1024) | NON |
| IMAGE_3 | varchar(1024) | NON |
| IMAGE_4 | varchar(1024) | NON |
| IMAGE_5 | varchar(1024) | NON |
| IMAGE_6 | varchar(1024) | NON |
| IMAGE_7 | varchar(1024) | NON |
| IMAGE_8 | varchar(1024) | NON |
| IMAGE_9 | varchar(1024) | NON |
| IMAGE_10 | varchar(1024) | NON |
| TEXT_1 | texte | NON |
| TEXT_2 | texte | NON |
| TEXT_3 | texte | NON |
| TEXT_4 | texte | NON |
| TEXT_5 | texte | NON |
| TEXT_6 | texte | NON |
| TEXT_7 | texte | NON |
| TEXT_8 | texte | NON |
| TEXT_9 | texte | NON |
| TEXT_10 | texte | NON |
| TEXT_11 | texte | NON |
| TEXT_12 | texte | NON |
| TEXT_13 | texte | NON |
| TEXT_14 | texte | NON |
| TEXT_15 | texte | NON |
| ADDITIONAL_PRICE_1 | decimal(10,2) | NON |
| ADDITIONAL_PRICE_2 | decimal(10,2) | NON |
| ADDITIONAL_PRICE_3 | decimal(10,2) | NON |
| AD_SIZE | varchar(32) | NON |
| RANG | int | NON |
| PAYS | texte | NON |
| ÉTAT | texte | NON |
| VILLE | texte | NON |
| ZIP | texte | NON |
| DMA | texte | NON |
| PROFILE_FILTER_1 | texte | NON |
| PROFILE_FILTER_2 | texte | NON |
| PROFILE_FILTER_3 | texte | NON |
| PROFILE_FILTER_4 | texte | NON |
| PROFILE_FILTER_5 | texte | NON |
| DATAPASS_FILTER_1 | texte | NON |
| DATAPASS_FILTER_2 | texte | NON |
| DATAPASS_FILTER_3 | texte | NON |
| DATAPASS_FILTER_4 | texte | NON |
| DATAPASS_FILTER_5 | texte | NON |
| AUDIENCE_SEGMENT | texte | NON |
| LANGUE | texte | NON |
| CREATIVE_ATTRIBUTE_1 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_2 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_3 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_4 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_5 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_6 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_7 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_8 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_9 | varchar(256) | NON |
| CREATIVE_ATTRIBUTE_10 | varchar(256) | NON |
| IS_DEFAULT | énumération | NON |

>[!MORELIKETHIS]
>
>* [Workflows pour les publicités dynamiques](/help/creative/introduction/workflow-dynamic-ads.md)
>* [Gérer les fichiers de ressources](/help/creative/feeds/asset-manage.md)
>* [Gérer les modèles de flux](/help/creative/feeds/feed-template-manage.md)
>* [Gérer les catalogues](/help/creative/feeds/catalog-manage.md)
