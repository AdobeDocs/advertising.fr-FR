---
title: Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Flashtalking] Balises publicitaires
description: Découvrez pourquoi et comment ajouter [!DNL Analytics for Advertising] des macros à vos [!DNL Flashtalking] balises publicitaires
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Flashtalking] Balises publicitaires

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable aux DSP Advertising uniquement*

Si vous utilisez des balises de publicité de [!DNL Flashtalking] pour vos publicités Advertising DSP, ajoutez les paramètres Analytics for Advertising aux URL de votre page d’entrée. Les paramètres enregistrent l’AMO ID (`s_kwcid`) et `ef_id` paramètres de chaîne de requête dans l’URL de la page d’entrée, ce qui permet à l’Adobe Advertising d’envoyer des données de clic pour les publicités à Adobe Analytics.

Utilisez des macros pour [!DNL Flashtalking] publicités display et vidéo pour les types suivants de [!DNL Analytics for Advertising] Implémentations :

* **Les annonceurs qui utilisent la variable [!DNL Adobe] [!DNL Analytics for Advertising] Code JavaScript implémenté sur leurs sites web**: le code JavaScript enregistre déjà l’AMO ID (`s_kwcid`) et `ef_id` paramètres de chaîne de requête. Cependant, l’utilisation de macros étend le suivi pour inclure les conversions basées sur les clics lorsque les cookies tiers ne sont pas pris en charge. Il est recommandé d’ajouter les macros des sections suivantes à vos balises publicitaires afin de capturer des données de clics publicitaires supplémentaires qui ne sont pas capturées par le biais du code JavaScript.

>[!NOTE]
>
>Le code JavaScript est une solution pour le suivi des clics uniquement lorsque des cookies sont toujours disponibles. Une fois les cookies arrêtés, la mise en oeuvre des macros suivantes est nécessaire.

* **Annonceurs dont les sites web n’utilisent pas la variable [!DNL Analytics for Advertising] Code JavaScript et s’appuient sur [!DNL Analytics] transfert côté serveur pour les données de clic publicitaire uniquement** (sans aucune donnée d’affichage publicitaire) : les macros suivantes sont requises pour signaler les activités de clics sur site effectuées à partir de publicités achetées via Adobe Advertising.

## Afficher les balises d’annonce

Dans le [!DNL Flashtalking] paramètres de balise publicitaire, ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le `Clicktag` field :

```html
?[ftqs:[AdobeAMO]]
```

Exemple :  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

## Balises de publicité vidéo

Dans le [!DNL Flashtalking] paramètres de balise publicitaire, ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le `Clicktag` field :

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Exemple :  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Google Campaign Manager 360] Balises publicitaires](/help/integrations/analytics/macros-google-campaign-manager.md)
