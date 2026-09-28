---
source-git-commit: 24aa1afe9611ca6ae46795c9bca2964e1d9c4f97
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%
---
# Champ Appareils dans les paramètres des campagnes et des groupes publicitaires GGL et MS

**[!UICONTROL Devices]:** (facultatif ; non disponible pour les campagnes de performances maximales [!DNL Google Ads] ou les publicités vidéo [!DNL Microsoft Advertising] ou CTV) Configurez les ajustements d’enchères pour différents types d’appareils, sous la forme de pourcentages de l’enchère au niveau du mot-clé. Par exemple, si l’enchère au niveau du mot-clé est de 1 USD et que l’ajustement d’enchère pour les smartphones est de 50 %, l’enchère pour les smartphones est de 1,50 USD. Par défaut, aucune valeur n’est saisie (ajustement d’offre=0) et tous les appareils sont offerts au niveau de l’offre par mot-clé.

Par [!DNL Google Ads], les pourcentages valides peuvent inclure -100 pour les smartphones et les tablettes (pour ne pas enchérir sur le type d’appareil), et de -90 à 900 pour tous les types d’appareils.

Par [!DNL Microsoft Advertising], les pourcentages valides peuvent inclure :

* Smartphones et tablettes : -100 (pour ne pas enchérir sur le type d&#39;appareil) et de -90 à 900
* Bureau : de 0 à 900

>[!NOTE]
>* Les paramètres au niveau du groupe publicitaire remplacent ceux de la campagne. Cependant, si vous excluez un appareil au niveau de la campagne, vous ne pouvez pas remplacer l’exclusion au niveau du groupe publicitaire.
>* Si vous affectez cette campagne à un portfolio optimisé standard, Search, Social et Commerce détermine automatiquement l’enchère de base au niveau du mot-clé pour aider le portfolio à atteindre son objectif. Le réseau publicitaire ajuste ensuite l’offre comme indiqué pour différents types d’appareils.
>* (Pour toutes les campagnes/groupes publicitaires, à l’exception des groupes publicitaires [!DNL Microsoft Advertising] dans le réseau d’audiences) Si vous affectez cette campagne à un portfolio optimisé standard configuré sur « [!UICONTROL Auto-optimize Bid Adjustment Values] », la fonctionnalité d’optimisation modifie les ajustements d’enchères de l’appareil spécifié au niveau du groupe publicitaire, à condition que la valeur idéale qu’elle calcule se situe entre les valeurs minimale et maximale spécifiées dans les paramètres du portfolio et que le groupe publicitaire n’exclut pas les enchères pour le type d’appareil.
