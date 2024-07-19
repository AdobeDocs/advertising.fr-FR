---
title: Ajouter des  [!DNL Analytics for Advertising] macros à [!DNL Flashtalking] balises de publicité
description: Découvrez pourquoi et comment ajouter des  [!DNL Analytics for Advertising] macros à vos  [!DNL Flashtalking] balises publicitaires
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Ajout de [!DNL Analytics for Advertising] macros à [!DNL Flashtalking] balises publicitaires

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable à Advertising DSP uniquement*

Si vous utilisez des balises d’annonce de [!DNL Flashtalking] pour vos publicités Advertising DSP, ajoutez les paramètres Analytics for Advertising aux URL de votre page d’entrée. Les paramètres enregistrent les paramètres de chaîne de requête AMO ID (`s_kwcid`) et `ef_id` dans l’URL de la page d’entrée, ce qui permet à l’Adobe Advertising d’envoyer des données de clic pour les publicités à Adobe Analytics.

Utilisez des macros pour [!DNL Flashtalking] publicités vidéo et display pour les types suivants de mises en oeuvre de [!DNL Analytics for Advertising] :

* **Les annonceurs dont le code JavaScript [!DNL Adobe] [!DNL Analytics for Advertising] est implémenté sur leurs sites web** : le code JavaScript enregistre déjà les paramètres de chaîne de requête AMO ID (`s_kwcid`) et `ef_id`. Cependant, l’utilisation de macros étend le suivi pour inclure les conversions basées sur les clics lorsque les cookies tiers ne sont pas pris en charge. La bonne pratique consiste à ajouter les macros des sections suivantes à vos balises publicitaires afin de capturer des données de clics publicitaires supplémentaires qui ne sont pas capturées par le code JavaScript.

>[!NOTE]
>
>Le code JavaScript est une solution pour le suivi des clics uniquement lorsque les cookies sont toujours disponibles. Une fois les cookies arrêtés, la mise en oeuvre des macros suivantes est nécessaire.

* **Les annonceurs dont les sites web n’utilisent pas le code JavaScript [!DNL Analytics for Advertising] et utilisent à la place le transfert côté serveur [!DNL Analytics] pour les données de clic publicitaire uniquement** (sans données d’affichage publicitaire) : les macros suivantes sont requises pour signaler l’activité de clic sur site basée sur les publicités que vous achetez par le biais de l’Adobe Advertising.

## Afficher les balises d’annonce

Dans les paramètres de balise publicitaire [!DNL Flashtalking], ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le champ `Clicktag` :

```
[ftqs:[AdobeAMO]]
```

S’il s’agit de la première ou de la seule chaîne de requête après l’URL de base, séparez-la de l’URL de base avec un `?`. Si l’URL de base inclut plusieurs chaînes de requête, commencez la première chaîne par un `?` et chaque chaîne suivante par un `&`.

Exemples :

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Balises de publicité vidéo

Dans les paramètres de balise publicitaire [!DNL Flashtalking], ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le champ `Clicktag` :

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

S’il s’agit de la première ou de la seule chaîne de requête après l’URL de base, séparez-la de l’URL de base avec un `?`. Si l’URL de base inclut plusieurs chaînes de requête, commencez la première chaîne par un `?` et chaque chaîne suivante par un `&`.

Exemples :

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Ajouter [!DNL Analytics for Advertising] Macros à [!DNL Google Campaign Manager 360] Balises publicitaires](/help/integrations/analytics/macros-google-campaign-manager.md)

