---
title: Méthode de calcul des règles d’attribution
description: Découvrez comment l’Adobe Advertising calcule chaque type de règle d’attribution.
exl-id: b61561fa-8c01-4989-9ef7-620d2b4c2c0b
feature: Search Reports
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '2439'
ht-degree: 0%

---

# Méthode de calcul des règles d’attribution pour l’Adobe Advertising

*Publicitaires avec suivi de conversion des Adobes Advertising uniquement*

<!-- Verify statements about cross-device events -->

La règle d’attribution au niveau de l’annonceur est utilisée pour attribuer des données de conversion, potentiellement sur plusieurs canaux publicitaires, dans une série d’événements qui mènent à une conversion.

Dans les rapports, les vues par défaut et personnalisées pour Advertising Search, Social &amp; Commerce (Search, Social, &amp; Commerce) et (certains rôles utilisateur) les simulations au niveau du portefeuille pour Search, Social, &amp; Commerce, la règle sélectionnée n’est utilisée que pour les données d’affichage, de rapport ou de simulation. Les différentes règles d’attribution sont appliquées comme suit.

>[!NOTE]
>
>* Les règles d’attribution s’appliquent aux clics sur les publicités payantes de n’importe quel canal et aux impressions sur les publicités affichées et sociales. Elles ne s’appliquent pas aux impressions pour les annonces de référencement payant, qui ne peuvent pas être suivies au niveau de l’événement.
>* Adobe Advertising stocke toujours les événements suivants pour chaque internaute avant une conversion : a) le premier clic payant ; b) jusqu’à 10 clics pour chaque canal (recherche, réseaux sociaux ou affichage), y compris le premier clic ; et c) jusqu’à 10 impressions display. <!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
* Dans Advertising DSP et Advertising Creative, les définitions entre appareils ne prennent en compte que le chemin d’événement de la règle d’attribution sélectionnée.<!-- cross-device attribution via LiveRamp only -->
* Dans les rapports et les vues de gestion, le nombre de décimales affichées pour une valeur dépend de la devise, mais Adobe Advertising stocke des valeurs plus précises.

## Dernier événement (valeur par défaut)

Attribue la conversion au dernier clic payant de la série dans le rapport [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) ou, si aucun clic payant n’a eu lieu, à la dernière impression dans le rapport [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j).

Lorsque la conversion est précédée uniquement par des impressions, la conversion est considérée comme une *affichage publicitaire*, qui est pondéré selon le [définition du poids d’affichage publicitaire](/help/search-social-commerce/glossary.md#uv) ou — comme spécifié — en fonction de la méthode d’évaluation d’affichage publicitaire définie dans le rapport, l’affichage ou les paramètres personnalisés de la simulation.

![Pourcentages d’attribution des derniers événements](/help/search-social-commerce/assets/attribution-percent-last-event.png "Pourcentages d’attribution des derniers événements")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l’événement : Click1, Click2, Click3, Conversion de 120 USD

La conversion est attribuée à Click 3 pour un montant de 120 USD.

### Exemple avec des impressions et des clics

**Remarque :** Les impressions ne s’appliquent qu’à partir des publicités display et sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Conversion de 120 USD

La conversion est attribuée à Click 1 pour un montant de 120 USD.

### Exemple avec toutes les impressions

**Remarque :** Seules les impressions pour l’affichage et les publicités sociales s’appliquent.

Chemin de l’événement : Impression 1, Impression 2, Impression 3, Conversion de 120 USD

La conversion est attribuée à Impression 3. La conversion étant un affichage publicitaire, la méthode d’évaluation d’affichage publicitaire sélectionnée dans la section &quot;Attribution de conversion&quot; des paramètres du rapport est appliquée :

* Si le paramètre de rapport indique un poids d’affichage publicitaire pondéré, ce poids est appliqué à l’affichage publicitaire. Par exemple, si le poids d’affichage publicitaire de l’annonceur est de 40 %, alors 120 USD x 40 % = 48 USD, donc 48 USD sont attribués à Impression 3.

* Si le paramètre de rapport indique l’utilisation de valeurs brutes pour les affichages publicitaires, aucun poids d’affichage publicitaire n’est appliqué à l’affichage publicitaire et les 120 USD complets sont attribués à l’impression 3.

+++

<!-- end examples as collapsible content -->

## Premier événement

Attribue la conversion au premier clic payant de la série dans le rapport de l’annonceur. [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) ou, si aucun clic payant n’a eu lieu, à la première impression dans le rapport [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j). Cette règle est disponible uniquement pour les événements sur des appareils uniques.

Lorsque la conversion est précédée uniquement par des impressions, la conversion est considérée comme une *affichage publicitaire*, qui est pondéré selon le [définition du poids d’affichage publicitaire](/help/search-social-commerce/glossary.md#uv) ou — comme spécifié — en fonction de la méthode d’évaluation d’affichage publicitaire définie dans le rapport, l’affichage ou les paramètres personnalisés de la simulation.

![Premiers pourcentages d’attribution d’événement](/help/search-social-commerce/assets/attribution-percent-first-event.png "Premiers pourcentages d’attribution d’événement")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l’événement : cliquez sur 1, sur 2, sur 3, sur Conversion de 120 USD

La conversion est attribuée à Click 1 pour un montant de 120 USD.

### Exemple avec des impressions et des clics

**Remarque :** Les impressions ne s’appliquent qu’à partir des publicités display et sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Conversion de 120 USD

La conversion est attribuée à Click 1 pour un montant de 120 USD.

### Exemple avec toutes les impressions

**Remarque :** Seules les impressions pour l’affichage et les publicités sociales s’appliquent.

Chemin de l’événement : Impression 1, Impression 2, Impression 3, Conversion de 120 USD

La conversion est attribuée à Impression 1. La conversion étant un affichage publicitaire, la méthode d’évaluation d’affichage publicitaire sélectionnée dans la section &quot;(Campagnes d’affichage) Attribution de conversion&quot; des paramètres du rapport est appliquée :

* Si le paramètre de rapport indique un poids d’affichage publicitaire pondéré, ce poids est appliqué à l’affichage publicitaire. Par exemple, si le poids d’affichage publicitaire de l’annonceur est de 40 %, alors 120 x 40 % = 48 USD, donc 48 USD sont attribués à Impression 1.

* Si le paramètre de rapport indique l’utilisation de valeurs brutes pour les affichages publicitaires, aucun poids d’affichage publicitaire n’est appliqué à l’affichage publicitaire et les 120 USD complets sont attribués à l’impression 1.

+++

<!-- end examples as collapsible content -->

## Poids - Premier événement Plus

Attribue la conversion à tous les événements de la série qui se sont produits dans le rapport [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j), mais donne le plus de poids au premier événement et successivement moins de poids aux événements suivants. Cette règle est disponible pour les événements sur des appareils uniques uniquement.

Lorsque la conversion est précédée uniquement par des impressions, la conversion est considérée comme une *affichage publicitaire*, qui est pondéré selon le [définition du poids d’affichage publicitaire](/help/search-social-commerce/glossary.md#uv) ou — comme spécifié — en fonction de la méthode d’évaluation d’affichage publicitaire définie dans le rapport, l’affichage ou les paramètres personnalisés de la simulation.

Lorsque le chemin de conversion inclut à la fois des clics payants et des impressions, les impressions sont traitées différemment par différents produits d’Adobe Advertising :

* Dans Search, Social et Commerce, la variable [poids du remplacement d’impression](/help/search-social-commerce/glossary.md#i-j) — qui est spécifié dans le paramètre de poids de remplacement d’impression de l’annonceur et dans les paramètres de rapport, d’affichage ou de simulation personnalisés — est d’abord appliqué aux impressions.

* Dans DSP, les impressions sont ignorées et seuls les clics sont pondérés. DSP ne prend pas en compte les poids de remplacement d’impression pour l’attribution.

![Poids du premier événement plus de pourcentages d’attribution](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Poids du premier événement plus de pourcentages d’attribution")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l’événement : cliquez sur 1, sur 2, sur 3, sur Conversion de 120 USD

Attribution : cliquez sur 1 = 60 USD, cliquez sur 2 = 40 USD, cliquez sur 3 = 20 USD (120 USD au total).

### Exemples avec des impressions et des clics

**Remarque :** Les impressions ne s’appliquent qu’à partir des publicités display et sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Clic 2, Conversion de 120 USD

#### (Recherche, Social et Commerce uniquement) Utilisation du &quot;poids de remplacement d’impression&quot; par défaut de 10 %

La série d’événements comprenant à la fois des impressions et des clics, le poids du remplacement d’impression s’applique aux impressions.

Attribution : Impression 1 = 8 USD, clic 1 = 72 USD, impression 2 = 4 USD, clic 2 = 36 USD (120 USD au total)

#### Utilisation (DSP uniquement) de l’option Aucun poids de remplacement d’impression ou (Recherche, Social et Commerce uniquement) d’un &quot;poids de remplacement d’impression&quot; de 0 %

Comme la série d’événements comprenait à la fois des impressions et des clics, les impressions sont ignorées.

Attribution : Impression 1 = 0 USD, clic 1 = 80 USD, impression 2 = 0 USD, clic 2 = 40 USD (120 USD au total)

### Exemple avec toutes les impressions

**Remarque :** Seules les impressions pour les publicités affichées s’appliquent.

Chemin de l’événement : Impression 1, Impression 2, Impression 3, Conversion de 120 USD

Comme la conversion est une vue publicitaire, la méthode d’évaluation d’affichage publicitaire (plutôt que le poids de remplacement d’impression) est appliquée pour déterminer la valeur de chaque impression :

* Si le paramètre du rapport spécifie un poids d’affichage publicitaire pondéré, ce poids est appliqué aux valeurs d’impression. Par exemple, si le poids d’affichage publicitaire est de 40 %, Impression 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (48 USD au total)

* Si le paramètre de rapport indique l’utilisation de valeurs brutes pour les affichages publicitaires, aucun poids d’affichage publicitaire n’est appliqué à l’impression et les 120 USD complets sont répartis entre les trois impressions : Impression 1 = 60 USD, Impression 2 = 40 USD, Impression 3 = 20 USD (120 USD au total)

+++

<!-- end examples as collapsible content -->

## Même distribution

>[!NOTE]
>
>Cette règle est disponible uniquement pour les événements sur des appareils uniques.

Attribue la conversion de manière égale à chaque événement de la série qui s’est produit dans le rapport [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j).

Lorsque la conversion est précédée uniquement par des impressions, la conversion est considérée comme une *affichage publicitaire*, qui est pondéré selon le [définition du poids d’affichage publicitaire](/help/search-social-commerce/glossary.md#uv) ou — comme spécifié — en fonction de la méthode d’évaluation d’affichage publicitaire définie dans le rapport, l’affichage ou les paramètres personnalisés de la simulation.

Lorsque le chemin de conversion inclut à la fois des clics payants et des impressions, les impressions sont traitées différemment par différents produits d’Adobe Advertising :

* Dans Search, Social et Commerce, la variable [poids du remplacement d’impression](/help/search-social-commerce/glossary.md#i-j) — qui est spécifié dans le paramètre de poids de remplacement d’impression de l’annonceur et dans les paramètres de rapport, d’affichage ou de simulation personnalisés — est d’abord appliqué aux impressions.

* Dans DSP, les impressions sont ignorées et seuls les clics sont pondérés. DSP ne prend pas en compte les poids de remplacement d’impression pour l’attribution.

![Pourcentages d’attribution égaux](/help/search-social-commerce/assets/attribution-percent-even.png "Pourcentages d’attribution égaux")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l’événement : cliquez sur 1, sur 2, sur 3, sur une conversion de 120 USD

Aucune impression n’a entraîné la conversion. Par conséquent, le poids du remplacement d’impression n’est pas applicable et la conversion est répartie équitablement entre les trois clics :

Attribution : cliquez sur 1 = 40 USD, cliquez sur 2 = 40 USD, cliquez sur 3 = 40 USD (120 USD au total).

### Exemples avec des impressions et des clics

**Remarque :** Les impressions ne s’appliquent qu’à partir des publicités display et sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Clic 2, Conversion de 120 USD

#### (Recherche, Social et Commerce uniquement) Utilisation du &quot;poids de remplacement d’impression&quot; par défaut de 10 %

La série d’événements comprenant à la fois des impressions et des clics, le poids du remplacement d’impression s’applique aux impressions.

Attribution : Impression 1 = 6 USD, clic 1 = 54 USD, impression 2 = 6 USD, clic 2 = 54 USD (120 USD au total)

#### Utilisation (par Adobe Advertising DSP uniquement) d’un poids de remplacement d’impression ou (recherche, Social et Commerce uniquement) d’un poids de remplacement d’impression de 0 %

Comme la série d’événements comprenait à la fois des impressions et des clics, les impressions sont ignorées.

Attribution : Impression 1 = 0 USD, clic 1 = 60 USD, impression 2 = 0 USD, clic 2 = 60 USD (120 USD au total)

## Exemple avec toutes les impressions

**Remarque :** Seules les impressions pour les publicités affichées s’appliquent.

Chemin de l’événement : Impression 1, Impression 2, Impression 3, Conversion de 120 USD

Comme la conversion est une vue publicitaire, la méthode d’évaluation d’affichage publicitaire (plutôt que le poids de remplacement d’impression) est appliquée pour déterminer la valeur de chaque impression :

* Si le paramètre du rapport spécifie un poids d’affichage publicitaire pondéré, ce poids est appliqué aux valeurs d’impression. Par exemple, si le poids d’affichage publicitaire est de 40 %, Impression 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (48 USD au total)

* Si le paramètre de rapport indique l’utilisation de valeurs brutes pour les affichages publicitaires, aucun poids d’affichage publicitaire n’est appliqué à l’impression et les 120 USD complets sont répartis entre les trois impressions : Impression 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (120 USD au total)

+++

<!-- end examples as collapsible content -->

## Poids du dernier événement plus

Attribue la conversion à tous les événements de la série qui se sont produits dans le rapport [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j), mais donne le plus de poids au dernier événement et, successivement, moins de poids aux événements précédents.

Lorsque la conversion est précédée uniquement par des impressions, la conversion est considérée comme une *affichage publicitaire*, qui est pondéré selon le [définition du poids d’affichage publicitaire](/help/search-social-commerce/glossary.md#uv) ou — comme spécifié — en fonction de la méthode d’évaluation d’affichage publicitaire définie dans le rapport, l’affichage ou les paramètres personnalisés de la simulation.

Lorsque le chemin de conversion inclut à la fois des clics payants et des impressions, les impressions sont traitées différemment par différents produits d’Adobe Advertising :

* Dans Search, Social et Commerce, la variable [poids du remplacement d’impression](/help/search-social-commerce/glossary.md#i-j) — qui est spécifié dans le paramètre de poids de remplacement d’impression de l’annonceur et dans les paramètres de rapport, d’affichage ou de simulation personnalisés — est d’abord appliqué aux impressions.

* Dans DSP, les impressions sont ignorées et seuls les clics sont pondérés. DSP ne prend pas en compte les poids de remplacement d’impression pour l’attribution.

![Poids du dernier événement plus de pourcentages d’attribution](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Poids du dernier événement plus de pourcentages d’attribution")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l’événement : cliquez sur 1, sur 2, sur 3, sur Conversion de 120 USD

Attribution : cliquez sur 3 = 60 USD, cliquez sur 2 = 40 USD, cliquez sur 1 = 20 USD (120 USD au total).

### Exemples avec des impressions et des clics

**Remarque :** Les impressions ne s’appliquent qu’à partir des publicités display et sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Clic 2, Conversion de 120 USD

#### (Recherche, Social et Commerce uniquement) Utilisation du &quot;poids de remplacement d’impression&quot; par défaut de 10 %

La série d’événements comprenant à la fois des impressions et des clics, le poids du remplacement d’impression s’applique aux impressions.

Attribution : Impression 1 = 4 USD, clic 1 = 36 USD, impression 2 = 8 USD, clic 2 = 72 USD (120 USD au total)

#### Utilisation (DSP uniquement) de l’option Aucun poids de remplacement d’impression ou (Recherche, Social et Commerce uniquement) d’un &quot;poids de remplacement d’impression&quot; de 0 %

Comme la série d’événements comprenait à la fois des impressions et des clics, les impressions sont ignorées.

Attribution : Impression 1 = 0 USD, clic 1 = 40 USD, impression 2 = 0 USD, clic 2 = 80 USD (120 USD au total)

### Exemple avec toutes les impressions

**Remarque :** Les impressions ne s’appliquent qu’à partir des publicités display et sociales.

Chemin de l’événement : Impression 1, Impression 2, Impression 3, Conversion de 120 USD

Comme la conversion est une vue publicitaire, la méthode d’évaluation d’affichage publicitaire (plutôt que le poids de remplacement d’impression) est appliquée pour déterminer la valeur de chaque impression :

* Si le paramètre du rapport spécifie un poids d’affichage publicitaire pondéré, ce poids est appliqué aux valeurs d’impression. Par exemple, si le poids de l’affichage publicitaire est de 40 %, multipliez chaque valeur de &quot;Exemple avec tous les clics&quot; par 40 % : Impression 3 = 24 USD, Impression 2 = 16 USD, Impression 1 = 8 USD (48 USD au total).

* Si le paramètre de rapport indique l’utilisation de valeurs brutes pour les affichages publicitaires, alors l’ensemble des 120 USD est divisé entre les impressions : Impression 3 = 60 USD, Impression 2 = 40 USD, Impression 1 = 20 USD (120 USD au total)

+++

<!-- end examples as collapsible content -->

## En forme de U

Attribue la conversion à tous les événements de la série qui se sont produits dans le rapport [intervalle de recherche en amont des clics](/help/search-social-commerce/glossary.md#c-d) et [intervalle de recherche en amont des impressions](/help/search-social-commerce/glossary.md#i-j), mais donne le plus de poids aux premiers et derniers événements, avec successivement moins de poids aux événements au milieu du chemin de conversion.

Lorsque la conversion est précédée uniquement par des impressions, la conversion est considérée comme une *affichage publicitaire*, qui est pondéré selon le [définition du poids d’affichage publicitaire](/help/search-social-commerce/glossary.md#uv) ou — comme spécifié — en fonction de la méthode d’évaluation d’affichage publicitaire définie dans le rapport, l’affichage ou les paramètres personnalisés de la simulation.

Lorsque le chemin de conversion inclut à la fois des clics payants et des impressions, les impressions sont traitées différemment par différents produits d’Adobe Advertising :

* Dans Search, Social et Commerce, la variable [poids du remplacement d’impression](/help/search-social-commerce/glossary.md#i-j) — qui est spécifié dans le paramètre de poids de remplacement d’impression de l’annonceur et dans les paramètres de rapport, d’affichage ou de simulation personnalisés — est d’abord appliqué aux impressions.

* Dans DSP, les impressions sont ignorées et seuls les clics sont pondérés. DSP ne prend pas en compte les poids de remplacement d’impression pour l’attribution.

![Pourcentages d’attribution en forme de U](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "Pourcentages d’attribution en forme de U")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l’événement : cliquez sur 1, sur 2, sur 3, sur 4, sur Conversion de 120 USD

Attribution : cliquez sur 1 = 36 USD, cliquez sur 2 = 24 USD, cliquez sur 3 = 24 USD, cliquez sur 4 = 36 USD (120 USD au total).

### Exemples avec des impressions et des clics

**Remarque :** Les impressions ne s’appliquent qu’à partir des publicités display et sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Clic 2, Conversion de 120 USD

#### (Recherche, Social et Commerce uniquement) Utilisation du &quot;poids de remplacement d’impression&quot; par défaut de 10 %

La série d’événements comprenant à la fois des impressions et des clics, le poids du remplacement d’impression s’applique aux impressions.

Attribution : Impression 1 = 6 USD, clic 1 = 54 USD, impression 2 = 6 USD, clic 2 = 54 USD (120 USD au total)

#### Utiliser (DSP uniquement) aucun poids de remplacement d’impression ou (Recherche, Social et Commerce uniquement) un &quot;poids de remplacement d’impression&quot; de 0 %

Comme la série d’événements comprenait à la fois des impressions et des clics, les impressions sont ignorées.

Attribution : Impression 1 = 0 USD, clic 1 = 60 USD, impression 2 = 0 USD, clic 2 = 60 USD (120 USD au total)

### Exemple avec toutes les impressions

**Remarque :** Seules les impressions pour les publicités affichées s’appliquent.

Chemin de l’événement : Impression 1, Impression 2, Impression 3, Impression 4, Conversion de 120 USD

Comme la conversion est une vue publicitaire, la méthode d’évaluation d’affichage publicitaire (plutôt que le poids de remplacement d’impression) est appliquée pour déterminer la valeur de chaque impression :

* Si le paramètre du rapport spécifie un poids d’affichage publicitaire pondéré, ce poids est appliqué aux valeurs d’impression. Par exemple, si le poids de l’affichage publicitaire est de 40 %, cliquez sur 1 = 14,40 USD, cliquez sur 2 = 9,60 USD, cliquez sur 3 = 9,60 USD, cliquez sur 4 = 14,40 USD (48 USD au total).

* Si le paramètre du rapport indique l’utilisation de valeurs brutes pour les affichages publicitaires, alors l’ensemble des 120 USD est divisé entre les impressions : cliquez sur 1 = 36 USD, cliquez sur 24 USD, cliquez sur 3 = 24 USD, cliquez sur 4 = 36 USD (120 USD total).

+++

<!-- end examples as collapsible content -->
