---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---
# Champ Périphériques dans les paramètres de campagne et de groupe publicitaire GGL et MS

**[!UICONTROL Devices]:** (Facultatif) n’est pas disponible pour [!DNL Google Ads] campagnes max de performances) Configurez les ajustements d’offres pour différents types d’appareils, en tant que pourcentages de l’offre au niveau du mot-clé. Par exemple, si l’offre au niveau du mot-clé est de 1 USD et que l’ajustement de l’offre pour les smartphones est de 50 %, l’offre pour les smartphones est de 1,50 USD. Par défaut, aucune valeur n’est saisie (ajustement d’offre = 0) et tous les périphériques sont soumis à l’offre au niveau du mot-clé.

Pour les publicités Google, les pourcentages valides peuvent inclure -100 pour les smartphones et les tablettes (pour ne pas enchérir pour le type d’appareil) et de -90 à 900 pour tous les types d’appareils.

Pour Microsoft Advertising, les pourcentages valides peuvent inclure :

* Smartphones et tablettes : -100 (pour ne pas enchérir pour le type d’appareil) et de -90 à 900
* Bureau : de 0 à 900

>[!NOTE]
>* Les paramètres au niveau du groupe d’annonces remplacent les paramètres au niveau de la campagne. Cependant, si vous excluez un appareil au niveau de la campagne, vous ne pouvez pas remplacer l’exclusion au niveau du groupe d’annonces.
>* Si vous attribuez cette campagne à un portefeuille optimisé standard, Search, Social et Commerce détermine automatiquement l’offre au niveau du mot-clé de base pour aider le portefeuille à atteindre son objectif. Le réseau publicitaire ajuste ensuite l’offre comme indiqué pour différents types d’appareils.
>* (Pour toutes les campagnes/tous les groupes d’annonces, à l’exception de [!DNL Microsoft Advertising] groupes d’annonces dans le réseau d’audience) Si vous attribuez cette campagne à un portefeuille optimisé standard configuré sur &quot;[!UICONTROL Auto-optimize Bid Adjustment Values],&quot; la fonctionnalité d’optimisation modifie ensuite les ajustements d’enchères des périphériques spécifiés au niveau du groupe publicitaire, à condition que la valeur idéale qu’il calcule tombe dans les valeurs minimale et maximale spécifiées dans les paramètres du portfolio et que le groupe publicitaire n’exclue pas les enchères pour le type de périphérique.

