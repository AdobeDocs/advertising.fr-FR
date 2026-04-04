---
title: À propos  [!DNL Google Ads]  règles de valeur de conversion
description: Découvrez comment afficher et gérer les règles  [!DNL Google Ads]  valeur de conversion dans Search, Social et Commerce.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# À propos des règles de valeur de conversion [!DNL Google Ads]

Search, Social et Commerce synchronise automatiquement les [&#x200B; règles de valeur de conversion &#x200B;](https://support.google.com/google-ads/answer/10518330) de vos comptes [!DNL Google Ads]. Les règles de valeur de conversion vous permettent d’ajuster les valeurs des événements de conversion en fonction des informations sur l’utilisateur ou l’utilisatrice, y compris le type d’appareil, l’emplacement et le segment d’audience. Vous pouvez utiliser des règles pour les enchères basées sur la valeur dans les campagnes de recherche, d’affichage, d’achat et de performances maximales avec les enchères intelligentes Google. Pour les campagnes avec les stratégies d’enchères Maximiser les conversions et Retour sur les dépenses publicitaires cible , [!DNL Google Ads] algorithmes commencent à préférer les conversions de valeur supérieure.

Les règles de valeur de conversion au niveau de la campagne remplacent les règles au niveau du compte. Lorsqu’une conversion satisfait à plusieurs règles de valeur de conversion, une seule des règles est appliquée. En règle générale, la règle la plus spécifique est appliquée. Consultez toutefois la [[!DNL Google Ads] documentation sur les priorités pour les différents types de conditions de règle](https://support.google.com/google-ads/answer/10520348).

## Vue et fonctionnalité [!UICONTROL Conversion Value Rules]

Toutes les règles créées dans l’interface [!DNL Google Ads] sont synchronisées dans les 24 heures et sont disponibles dans la vue [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules] . Certains comptes peuvent gérer leurs règles de valeur de conversion :

* Dans les comptes pour lesquels les conversions sont suivies au niveau du compte individuel ou de la campagne, vous pouvez créer, modifier et modifier le statut de vos règles au niveau du compte et de la campagne.

  Les comptes peuvent être liés aux comptes [!DNL Google Ads] Manager, mais ils ne peuvent pas utiliser le suivi des conversions entre comptes (pour lequel les conversions sont suivies sur tous les comptes du compte Manager).

* Dans les comptes qui utilisent le suivi des conversions entre comptes, vos règles au niveau du compte et de la campagne sont héritées du compte du responsable et sont en lecture seule.

## Règles de valeur de conversion avec les portfolios Search, Social et Commerce

Lorsque le compte de l’annonceur est configuré pour charger les objectifs Search, Social et Commerce vers [!DNL Google Ads] et que vous incluez une campagne qui utilise une règle de valeur de conversion dans un portfolio avec un objectif , [!DNL Google Ads] applique la règle de valeur de conversion à la valeur de conversion d’origine spécifiée dans l’objectif . Par conséquent, les données de conversion dans Search, Social et Commerce diffèrent des données de conversion dans [!DNL Google Ads].

Supposons, par exemple, que l’objectif utilise une mesure de conversion unique « Leads » et donne aux conversions provenant d’appareils mobiles un poids de 10 et aux conversions provenant d’appareils non mobiles un poids de 10. Search, Social et Commerce comptabilise un événement de l’un des types d’appareils comme une (1) conversion et attribue à la valeur de conversion la valeur 10. Cependant, supposons qu’une campagne de ce portefeuille utilise une règle de valeur de conversion « Si l’appareil est mobile, multipliez par 2 ». Lorsqu’un événement Leads mobile est suivi pour cette campagne, [!DNL Google Ads] attribue également au nombre de conversions la valeur un (1), mais à la valeur de conversion (10 x 2) = 20.

Pour obtenir plus d’informations sur vos règles, y compris les valeurs de conversion d’origine avant l’application des règles, consultez le rapport [&#x200B; règles de valeur de conversion dans  [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

>[!MORELIKETHIS]
>
>* [Créer une règle  [!DNL Google Ads]  valeur de conversion](create-google-conversion-value-rule.md)
>* [Modifier une règle  [!DNL Google Ads]  valeur de conversion](edit-google-conversion-value-rule.md)
>* [Modifier le statut d’une règle  [!DNL Google Ads]  valeur de conversion](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] paramètres des règles de valeur de conversion](google-conversion-value-rule-settings.md)

