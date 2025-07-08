---
title: Méthode de calcul des règles d’attribution
description: Découvrez comment Adobe Advertising calcule chaque type de règle d’attribution.
exl-id: 15beeadd-bb65-4efe-8c4f-34c4a48cc775
feature: Search Reports
source-git-commit: b24673e05f95bac404301d71ad9c0d1d0593aafb
workflow-type: tm+mt
source-wordcount: '2716'
ht-degree: 0%

---

# Méthode de calcul des règles d’attribution pour Adobe Advertising

*Annonceurs avec suivi des conversions Adobe Advertising uniquement*

<!-- Verify statements about cross-device events -->

La règle d’attribution au niveau de l’annonceur est utilisée pour attribuer des données de conversion, potentiellement sur plusieurs canaux publicitaires, dans une série d’événements qui conduisent à une conversion.

Dans les rapports, les vues par défaut et personnalisées pour les simulations au niveau du portfolio Advertising Search, Social et Commerce (Search, Social et Commerce), et (certains rôles utilisateur) pour les simulations Search, Social et Commerce, la règle sélectionnée n’est utilisée que pour les données d’affichage, de rapport ou de simulation. Les différentes règles d’attribution sont appliquées comme suit.

>[!NOTE]
>
>* Les règles d’attribution s’appliquent aux clics sur les annonces payantes dans n’importe quel canal et aux impressions sur l’affichage et aux annonces sur les réseaux sociaux. Elles ne s’appliquent pas aux impressions pour les annonces de référencement payant, qui ne peuvent pas être suivies au niveau de l’événement.
>* Adobe Advertising stocke toujours les événements suivants pour chaque internaute avant une conversion : a) le premier clic payant ; b) jusqu’à 10 clics pour chaque canal (recherche, réseau social ou affichage), y compris le premier clic ; et c) jusqu’à 10 impressions d’affichage.<!-- But it can continue to attribute conversions to clicks and impressions for longer. -->
>* Dans Advertising DSP et Advertising Creative, les définitions inter-appareils ne prennent en compte que le chemin d’accès à l’événement de la règle d’attribution sélectionnée.<!-- cross-device attribution via LiveRamp only -->
>* Dans les rapports et les vues de gestion, le nombre de décimales affichées pour une valeur dépend de la devise, mais Adobe Advertising stocke des valeurs plus précises.

## Dernier événement (valeur par défaut)

Attribue la conversion au dernier clic payant de la série dans l’intervalle de recherche en amont de l’annonceur [clic](/help/search-social-commerce/glossary.md#c-d) ou, en l’absence de clics payants, à la dernière impression dans l’intervalle de recherche en amont de l’annonceur [impression](/help/search-social-commerce/glossary.md#i-j).

Lorsque la conversion n&#39;est précédée que d&#39;impressions, elle est considérée comme une *vue directe*, qui est pondérée soit selon le paramètre de pondération de la [vue directe](/help/search-social-commerce/glossary.md#uv) de l&#39;annonceur, soit, comme spécifié, selon la méthode d&#39;évaluation de la vue directe spécifiée dans le rapport, la vue ou les paramètres de simulation personnalisés.

![Pourcentage d’attribution du dernier événement](/help/search-social-commerce/assets/attribution-percent-last-event.png "Pourcentage d’attribution du dernier événement")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l’événement : Click1, Click2, Click3, Conversion de 120 USD

La conversion est attribuée à Click 3 pour un montant de 120 USD.

### Exemple avec des impressions et des clics

**Remarque :** les impressions s’appliquent uniquement à partir de l’affichage et des publicités sociales.

Chemin de l’événement : impression 1, clic 1, impression 2, conversion de 120 USD

La conversion est attribuée à Click 1 pour un montant de 120 USD.

### Exemple avec toutes les impressions

**Remarque :** seules les impressions pour l’affichage et les publicités sociales sont applicables.

Chemin de l’événement : impression 1, impression 2, impression 3, conversion de 120 USD

La conversion est attribuée à l’impression 3. Comme la conversion est une visualisation directe, la méthode d’évaluation de la visualisation directe sélectionnée dans la section « Attribution de conversion » des paramètres du rapport est appliquée :

* Si le paramètre d&#39;état spécifie un poids pondéré pour la vue, ce poids est appliqué à la vue. Par exemple, si le poids de l’affichage publicitaire de l’annonceur est de 40 %, alors 120 USD x 40 % = 48 USD, donc 48 USD sont attribués à l’impression 3.

* Si le paramètre de rapport spécifie l&#39;utilisation de valeurs brutes pour les vues publicitaires, aucun poids de vue publicitaire n&#39;est appliqué à la vue publicitaire et la totalité des 120 USD est attribuée à l&#39;impression 3.

+++

<!-- end examples as collapsible content -->

## Premier Événement

Attribue la conversion au premier clic payant de la série dans l’intervalle de recherche en amont de l’annonceur [clic](/help/search-social-commerce/glossary.md#c-d) ou, en l’absence de clics payants, à la première impression dans l’intervalle de recherche en amont de l’annonceur [impression](/help/search-social-commerce/glossary.md#i-j). Cette règle est disponible pour les événements sur des appareils uniques uniquement.

Lorsque la conversion n’est précédée que d’impressions, elle est considérée comme une *vue directe*, qui est pondérée selon le paramètre de pondération de la [vue directe](/help/search-social-commerce/glossary.md#uv) de l’annonceur ou, comme indiqué, selon la méthode d’évaluation de la vue directe spécifiée dans le rapport, la vue ou les paramètres de simulation personnalisés.

![Pourcentages d’attribution du premier événement](/help/search-social-commerce/assets/attribution-percent-first-event.png "Pourcentages d’attribution du premier événement")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l&#39;événement : Cliquez 1, Cliquez 2, Cliquez 3, Conversion de 120 USD

La conversion est attribuée à Click 1 pour un montant de 120 USD.

### Exemple avec des impressions et des clics

**Remarque :** les impressions s’appliquent uniquement à partir de l’affichage et des publicités sociales.

Chemin de l’événement : impression 1, clic 1, impression 2, conversion de 120 USD

La conversion est attribuée à Click 1 pour un montant de 120 USD.

### Exemple avec toutes les impressions

**Remarque :** seules les impressions pour l’affichage et les publicités sociales sont applicables.

Chemin de l’événement : impression 1, impression 2, impression 3, conversion de 120 USD

La conversion est attribuée à l’impression 1. La conversion étant une vue directe, la méthode d’évaluation de la vue directe sélectionnée dans la conversion « (Afficher les campagnes) »
La section « Attribution » des paramètres du rapport est appliquée :

* Si le paramètre d&#39;état spécifie un poids pondéré pour la vue, ce poids est appliqué à la vue. Par exemple, si le poids de l’affichage publicitaire de l’annonceur est de 40 %, alors 120 x 40 % = 48 USD, donc 48 USD sont attribués à l’impression 1.

* Si le paramètre de rapport spécifie l&#39;utilisation de valeurs brutes pour les vues publicitaires, aucun poids de vue publicitaire n&#39;est appliqué à la vue publicitaire et la totalité des 120 USD est attribuée à l&#39;impression 1.

+++

<!-- end examples as collapsible content -->

## Poids du premier événement Plus

Attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et l’intervalle de recherche en amont [impression](/help/search-social-commerce/glossary.md#i-j) de l’annonceur, mais donne le plus de poids au premier événement et successivement moins de poids aux événements suivants. Cette règle est disponible pour les événements sur un seul appareil uniquement.

Lorsque la conversion n’est précédée que d’impressions, elle est considérée comme une *vue directe*, qui est pondérée selon le paramètre de pondération de la [vue directe](/help/search-social-commerce/glossary.md#uv) de l’annonceur ou, comme indiqué, selon la méthode d’évaluation de la vue directe spécifiée dans le rapport, la vue ou les paramètres de simulation personnalisés.

Lorsque le chemin de conversion comprend à la fois des clics payants et des impressions, les impressions sont traitées différemment par différents produits Adobe Advertising :

* Dans Search, Social et Commerce, le [poids de remplacement d’impression](/help/search-social-commerce/glossary.md#i-j), qui est spécifié dans le paramètre de poids de remplacement d’impression de l’annonceur et dans les paramètres de rapport, de vue ou de simulation personnalisée, est d’abord appliqué aux impressions.

* Dans DSP, les impressions sont ignorées et seuls les clics sont pondérés. DSP ne prend pas en compte les poids de remplacement d’impression pour l’attribution.

![Poids premier événement plus de pourcentages d’attribution](/help/search-social-commerce/assets/attribution-percent-weight-first-more.png "Poids premier événement plus de pourcentages d’attribution")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l&#39;événement : Cliquez 1, Cliquez 2, Cliquez 3, Conversion de 120 USD

Attribution : cliquez sur 1 = 60 USD, cliquez sur 2 = 40 USD, cliquez sur 3 = 20 USD (total de 120 USD).

### Exemples d’impressions et de clics

**Remarque :** les impressions s’appliquent uniquement à partir de l’affichage et des publicités sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Clic 2, Conversion de 120 USD

#### (Recherche, réseaux sociaux et Commerce uniquement) Utilisation du « poids de remplacement d’impression » par défaut de 10 %

Comme la série d’événements incluait à la fois des impressions et des clics, le poids de remplacement d’impression s’applique aux impressions.

Attribution : impression 1 = 8 USD, clic 1 = 72 USD, impression 2 = 4 USD, clic 2 = 36 USD (total de 120 USD)

#### en utilisant (DSP uniquement) aucun poids de remplacement d’impression ou (Search, Social et Commerce uniquement) un « poids de remplacement d’impression » de 0 % ;

Comme la série d’événements incluait à la fois des impressions et des clics, les impressions sont ignorées.

Attribution : impression 1 = 0 USD, clic 1 = 80 USD, impression 2 = 0 USD, clic 2 = 40 USD (total de 120 USD).

### Exemple avec toutes les impressions

**Remarque :** seules les impressions pour les publicités display sont applicables.

Chemin de l’événement : impression 1, impression 2, impression 3, conversion de 120 USD

Comme la conversion est une visualisation directe, la méthode d&#39;évaluation de la visualisation directe, plutôt que le poids de remplacement de l&#39;impression, est appliquée pour déterminer la valeur de chaque impression :

* Si le paramètre d&#39;état spécifie un poids pondéré pour les vues publicitaires, ce poids est appliqué aux valeurs d&#39;impression. Par exemple, si le poids de l’affichage publicitaire est de 40 %, alors Impression 1 = 24 USD, Impression 2 = 16 USD, Impression 3 = 8 USD (total de 48 USD)

* Si le paramètre d&#39;état spécifie l&#39;utilisation de valeurs brutes pour les affichages publicitaires, aucun poids d&#39;affichage publicitaire n&#39;est appliqué à l&#39;impression et la totalité des 120 USD est divisée entre les trois impressions : Impression 1 = 60 USD, Impression 2 = 40 USD, Impression 3 = 20 USD (total de 120 USD)

+++

<!-- end examples as collapsible content -->

## Distribution des événements

>[!NOTE]
>
>Cette règle est disponible pour les événements sur des appareils uniques uniquement.

Attribue la conversion de la même manière à chaque événement de la série qui s’est produit dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et [impression de l’annonceur](/help/search-social-commerce/glossary.md#i-j).

Lorsque la conversion n’est précédée que d’impressions, elle est considérée comme une *vue directe*, qui est pondérée selon le paramètre de pondération de la [vue directe](/help/search-social-commerce/glossary.md#uv) de l’annonceur ou, comme indiqué, selon la méthode d’évaluation de la vue directe spécifiée dans le rapport, la vue ou les paramètres de simulation personnalisés.

Lorsque le chemin de conversion comprend à la fois des clics payants et des impressions, les impressions sont traitées différemment par différents produits Adobe Advertising :

* Dans Search, Social et Commerce, le [poids de remplacement d’impression](/help/search-social-commerce/glossary.md#i-j), qui est spécifié dans le paramètre de poids de remplacement d’impression de l’annonceur et dans les paramètres de rapport, de vue ou de simulation personnalisée, est d’abord appliqué aux impressions.

* Dans DSP, les impressions sont ignorées et seuls les clics sont pondérés. DSP ne prend pas en compte les poids de remplacement d’impression pour l’attribution.

![Pourcentages d’attribution pairs](/help/search-social-commerce/assets/attribution-percent-even.png "Pourcentages d’attribution pairs")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l&#39;événement : Cliquez 1, Cliquez 2, Cliquez 3, Conversion de 120 USD

Aucune impression n’a conduit à la conversion. Par conséquent, le poids de remplacement d’impression n’est pas applicable et la conversion est divisée de manière égale entre les trois clics :

Attribution : cliquez sur 1 = 40 USD, cliquez sur 2 = 40 USD, cliquez sur 3 = 40 USD (total de 120 USD).

### Exemples d’impressions et de clics

**Remarque :** les impressions s’appliquent uniquement à partir de l’affichage et des publicités sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Clic 2, Conversion de 120 USD

#### (Recherche, réseaux sociaux et Commerce uniquement) Utilisation du « poids de remplacement d’impression » par défaut de 10 %

Comme la série d’événements incluait à la fois des impressions et des clics, le poids de remplacement d’impression s’applique aux impressions.

Attribution : impression 1 = 6 USD, clic 1 = 54 USD, impression 2 = 6 USD, clic 2 = 54 USD (total de 120 USD)

#### en utilisant (Adobe Advertising DSP uniquement) aucun poids de remplacement d’impression ou (Search, Social et Commerce uniquement) un « poids de remplacement d’impression » de 0 % ;

Comme la série d’événements incluait à la fois des impressions et des clics, les impressions sont ignorées.

Attribution : impression 1 = 0 USD, clic 1 = 60 USD, impression 2 = 0 USD, clic 2 = 60 USD (total de 120 USD).

## Exemple avec toutes les impressions

**Remarque :** seules les impressions pour les publicités display sont applicables.

Chemin de l’événement : impression 1, impression 2, impression 3, conversion de 120 USD

Comme la conversion est une visualisation directe, la méthode d&#39;évaluation de la visualisation directe, plutôt que le poids de remplacement de l&#39;impression, est appliquée pour déterminer la valeur de chaque impression :

* Si le paramètre d&#39;état spécifie un poids pondéré pour les vues publicitaires, ce poids est appliqué aux valeurs d&#39;impression. Par exemple, si le poids de l’affichage publicitaire est de 40 %, alors Impression 1 = 16 USD, Impression 2 = 16 USD, Impression 3 = 16 USD (total de 48 USD)

* Si le paramètre d&#39;état spécifie l&#39;utilisation de valeurs brutes pour les affichages publicitaires, aucun poids d&#39;affichage publicitaire n&#39;est appliqué à l&#39;impression et la totalité des 120 USD est divisée entre les trois impressions : Impression 1 = 40 USD, Impression 2 = 40 USD, Impression 3 = 40 USD (total de 120 USD)

+++

<!-- end examples as collapsible content -->

## Poids Dernier Événement Plus

Attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et l’intervalle de recherche en amont [impression](/help/search-social-commerce/glossary.md#i-j) de l’annonceur, mais donne le plus de poids au dernier événement et successivement moins de poids aux événements précédents.

Lorsque la conversion n’est précédée que d’impressions, elle est considérée comme une *vue directe*, qui est pondérée selon le paramètre de pondération de la [vue directe](/help/search-social-commerce/glossary.md#uv) de l’annonceur ou, comme indiqué, selon la méthode d’évaluation de la vue directe spécifiée dans le rapport, la vue ou les paramètres de simulation personnalisés.

Lorsque le chemin de conversion comprend à la fois des clics payants et des impressions, les impressions sont traitées différemment par différents produits Adobe Advertising :

* Dans Search, Social et Commerce, le [poids de remplacement d’impression](/help/search-social-commerce/glossary.md#i-j), qui est spécifié dans le paramètre de poids de remplacement d’impression de l’annonceur et dans les paramètres de rapport, de vue ou de simulation personnalisée, est d’abord appliqué aux impressions.

* Dans DSP, les impressions sont ignorées et seuls les clics sont pondérés. DSP ne prend pas en compte les poids de remplacement d’impression pour l’attribution.

![Poids du dernier événement plus de pourcentages d’attribution](/help/search-social-commerce/assets/attribution-percent-weight-last-more.png "Poids du dernier événement plus de pourcentages d’attribution")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l&#39;événement : Cliquez 1, Cliquez 2, Cliquez 3, Conversion de 120 USD

Attribution : cliquez 3 = 60 USD, cliquez 2 = 40 USD, cliquez 1 = 20 USD (total de 120 USD).

### Exemples d’impressions et de clics

**Remarque :** les impressions s’appliquent uniquement à partir de l’affichage et des publicités sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Clic 2, Conversion de 120 USD

#### (Recherche, réseaux sociaux et Commerce uniquement) Utilisation du « poids de remplacement d’impression » par défaut de 10 %

Comme la série d’événements incluait à la fois des impressions et des clics, le poids de remplacement d’impression s’applique aux impressions.

Attribution : impression 1 = 4 USD, clic 1 = 36 USD, impression 2 = 8 USD, clic 2 = 72 USD (total de 120 USD)

#### en utilisant (DSP uniquement) aucun poids de remplacement d’impression ou (Search, Social et Commerce uniquement) un « poids de remplacement d’impression » de 0 % ;

Comme la série d’événements incluait à la fois des impressions et des clics, les impressions sont ignorées.

Attribution : impression 1 = 0 USD, clic 1 = 40 USD, impression 2 = 0 USD, clic 2 = 80 USD (total de 120 USD).

### Exemple avec toutes les impressions

**Remarque :** les impressions s’appliquent uniquement à partir de l’affichage et des publicités sociales.

Chemin de l’événement : impression 1, impression 2, impression 3, conversion de 120 USD

Comme la conversion est une visualisation directe, la méthode d&#39;évaluation de la visualisation directe, plutôt que le poids de remplacement de l&#39;impression, est appliquée pour déterminer la valeur de chaque impression :

* Si le paramètre d&#39;état spécifie un poids pondéré pour les vues publicitaires, ce poids est appliqué aux valeurs d&#39;impression. Par exemple, si le poids de l’affichage publicitaire est de 40 %, multipliez chaque valeur dans l’« Exemple avec tous les clics » par 40 % : impression 3 = 24 USD, impression 2 = 16 USD, impression 1 = 8 USD (total de 48 USD)

* Si le paramètre de rapport spécifie l’utilisation de valeurs brutes pour les affichages publicitaires, la totalité des 120 USD est divisée entre les impressions : impression 3 = 60 USD, impression 2 = 40 USD, impression 1 = 20 USD (total de 120 USD)

+++

<!-- end examples as collapsible content -->

## en U

Attribue la conversion à tous les événements de la série qui se sont produits dans l’intervalle de recherche en amont [clic](/help/search-social-commerce/glossary.md#c-d) et l’intervalle de recherche en amont [impression](/help/search-social-commerce/glossary.md#i-j) de l’annonceur, mais donne le plus de poids au premier événement et aux derniers événements, avec successivement moins de poids aux événements au milieu du chemin de conversion.

Lorsque la conversion n’est précédée que d’impressions, elle est considérée comme une *vue directe*, qui est pondérée selon le paramètre de pondération de la [vue directe](/help/search-social-commerce/glossary.md#uv) de l’annonceur ou, comme indiqué, selon la méthode d’évaluation de la vue directe spécifiée dans le rapport, la vue ou les paramètres de simulation personnalisés.

Lorsque le chemin de conversion comprend à la fois des clics payants et des impressions, les impressions sont traitées différemment par différents produits Adobe Advertising :

* Dans Search, Social et Commerce, le [poids de remplacement d’impression](/help/search-social-commerce/glossary.md#i-j), qui est spécifié dans le paramètre de poids de remplacement d’impression de l’annonceur et dans les paramètres de rapport, de vue ou de simulation personnalisée, est d’abord appliqué aux impressions.

* Dans DSP, les impressions sont ignorées et seuls les clics sont pondérés. DSP ne prend pas en compte les poids de remplacement d’impression pour l’attribution.

Pourcentages d’attribution en forme de ![U](/help/search-social-commerce/assets/attribution-percent-u-shaped.png "Pourcentages d’attribution en forme de U")

<!-- start examples as collapsible content -->

+++Exemples de calculs d’événement

### Exemple avec tous les clics

Chemin de l&#39;événement : Cliquez 1, Cliquez 2, Cliquez 3, Cliquez 4, Conversion de 120 USD

Attribution : cliquez sur 1 = 36 USD, cliquez sur 2 = 24 USD, cliquez sur 3 = 24 USD, cliquez sur 4 = 36 USD (total de 120 USD).

### Exemples d’impressions et de clics

**Remarque :** les impressions s’appliquent uniquement à partir de l’affichage et des publicités sociales.

Chemin de l’événement : Impression 1, Clic 1, Impression 2, Clic 2, Conversion de 120 USD

#### (Recherche, réseaux sociaux et Commerce uniquement) Utilisation du « poids de remplacement d’impression » par défaut de 10 %

Comme la série d’événements incluait à la fois des impressions et des clics, le poids de remplacement d’impression s’applique aux impressions.

Attribution : impression 1 = 6 USD, clic 1 = 54 USD, impression 2 = 6 USD, clic 2 = 54 USD (total de 120 USD)

#### en utilisant (DSP uniquement) aucun poids de remplacement d’impression ou (Search, Social et Commerce uniquement) un « Poids de remplacement d’impression » de 0 % ;

Comme la série d’événements incluait à la fois des impressions et des clics, les impressions sont ignorées.

Attribution : impression 1 = 0 USD, clic 1 = 60 USD, impression 2 = 0 USD, clic 2 = 60 USD (total de 120 USD).

### Exemple avec toutes les impressions

**Remarque :** seules les impressions pour les publicités display sont applicables.

Chemin de l’événement : impression 1, impression 2, impression 3, impression 4, conversion de 120 USD

Comme la conversion est une visualisation directe, la méthode d&#39;évaluation de la visualisation directe, plutôt que le poids de remplacement de l&#39;impression, est appliquée pour déterminer la valeur de chaque impression :

* Si le paramètre d&#39;état spécifie un poids pondéré pour les vues publicitaires, ce poids est appliqué aux valeurs d&#39;impression. Par exemple, si le poids de l&#39;affichage publicitaire est de 40 %, cliquez sur 1 = 14,40 USD, cliquez sur 2 = 9,60 USD, cliquez sur 3 = 9,60 USD, cliquez sur 4 = 14,40 USD (48 USD au total)

* Si le paramètre de rapport spécifie l’utilisation de valeurs brutes pour les vues publicitaires, les 120 USD complets sont divisés entre les impressions : cliquez sur 1 = 36 USD, cliquez sur 2 = 24 USD, cliquez sur 3 = 24 USD, cliquez sur 4 = 36 USD (total de 120 USD)

+++

<!-- end examples as collapsible content -->
