---
title: Ajouter [!DNL Analytics for Advertising] des macros à des balises  [!DNL Flashtalking] ’annonces
description: Découvrez pourquoi et comment ajouter  [!DNL Analytics for Advertising]  macros à vos balises  [!DNL Flashtalking]  publicité
feature: Integration with Adobe Analytics
exl-id: ce81824c-60bf-487c-8358-d18fcb3cc95f
source-git-commit: c4db5727def6125b65fb2146666b988ae3b0db27
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Ajout de macros [!DNL Analytics for Advertising] aux balises de publicité [!DNL Flashtalking]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Organisations sans partenariat direct avec [!DNL Flashtalking] uniquement*

*Applicable à Advertising DSP uniquement*

Si vous utilisez les balises d’annonce publicitaire de [!DNL Flashtalking] pour vos annonces Advertising DSP, vous devez ajouter des paramètres de suivi à vos URL de page de destination. Pour utiliser le partenariat Advertising DSP avec [!DNL Flashtalking], ajoutez les paramètres Analytics for Advertising à vos URL de page de destination. Les paramètres enregistrent l’ID AMO (`s_kwcid`) et `ef_id` les paramètres de chaîne de requête dans l’URL de la page de destination, ce qui permet à Adobe Advertising d’envoyer des données de clic pour les publicités à Adobe Analytics.

>[!NOTE]
>
>Si votre organisation a un partenariat direct avec [!DNL Flashtalking], cette procédure n&#39;est pas nécessaire pour vous. Connectez-vous plutôt à votre compte [!DNL Flashtalking] et consultez la documentation d’assistance [!DNL Flashtalking] pour accéder aux macros data-pass à l’adresse `https://support.flashtalking.com%2Fhc%2Fen-us%2Farticles%2F4409808166419-Accessing-Data-Pass-Macros`.

Utilisez des macros pour [!DNL Flashtalking] les publicités vidéo et d’affichage pour les types d’implémentation [!DNL Analytics for Advertising] suivants :

* **Annonceurs avec le code [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript implémenté sur leurs sites web** : le code JavaScript enregistre déjà les paramètres AMO ID (`s_kwcid`) et `ef_id` chaîne de requête. Toutefois, l’utilisation de macros étend le suivi pour inclure les conversions basées sur les clics lorsque les cookies tiers ne sont pas pris en charge. Il est recommandé d’ajouter les macros des sections suivantes à vos balises d’annonces afin de capturer des données de clic publicitaire supplémentaires qui ne sont pas capturées par le code JavaScript.

  >[!NOTE]
  >
  >Le code JavaScript est une solution permettant le suivi des clics uniquement tant que des cookies sont disponibles. Une fois les cookies arrêtés, la mise en œuvre des macros suivantes sera nécessaire.

* **Annonceurs dont les sites web n’utilisent pas le code JavaScript [!DNL Analytics for Advertising] et comptent plutôt sur [!DNL Analytics] transfert côté serveur pour les données de clic publicitaire uniquement** (sans données de vue publicitaire) : les macros suivantes sont nécessaires pour signaler l’activité de clic sur site pilotée par les publicités que vous achetez via Adobe Advertising.

## Afficher les balises de publicité

Dans les paramètres des balises d’annonces [!DNL Flashtalking], ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le champ `Clicktag` :

```
[ftqs:[AdobeAMO]]
```

S’il s’agit de la première ou de la seule chaîne de requête après l’URL de base, séparez-la de l’URL de base avec une `?`. Si l’URL de base comprend plusieurs chaînes de requête, commencez la première chaîne par une `?` et chaque chaîne suivante par une `&`.

Exemples :

`https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

`https://www.adobe.com/products/photoshop?cid=email&[ftqs:[AdobeAMO]]`

## Balises de publicité vidéo

Dans les paramètres des balises d’annonces [!DNL Flashtalking], ajoutez la macro suivante à la fin de l’URL de clic publicitaire dans le champ `Clicktag` :

```
[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

S’il s’agit de la première ou de la seule chaîne de requête après l’URL de base, séparez-la de l’URL de base avec une `?`. Si l’URL de base comprend plusieurs chaînes de requête, commencez la première chaîne par une `?` et chaque chaîne suivante par une `&`.

Exemples :

`https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

`https://www.adobe.com/products/photoshop?cid=email&[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [ID Adobe Advertising utilisés par  [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

