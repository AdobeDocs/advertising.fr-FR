---
title: Utilisation de la bibliothèque  [!DNL Last Event Service] JavaScript avec  [!DNL Web SDK]
description: Découvrez les étapes à suivre pour passer de l’utilisation de la bibliothèque  [!DNL Analytics] [!DNL visitorAPI] à la bibliothèque  [!DNL Experience Platform] [!DNL Web SDK] pour votre  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
TQID: https://experienceleague.adobe.com/zT1lQV1yotCfJJdzTBGzSspsNEKQEB5ulxYE0qyWa9Q
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 0%

---

# Utilisation de la bibliothèque [!DNL Last Event Service] JavaScript avec Adobe Experience Platform [!DNL Web SDK]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Si votre entreprise utilise l’ancienne bibliothèque `visitorAPI.js` d’Adobe Analytics pour la collecte de données, vous pouvez éventuellement passer à l’utilisation de la bibliothèque [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) (`alloy.js`), qui vous permet d’interagir avec les différents services Adobe CX Enterprise via [!DNL Edge Network].

La bibliothèque JavaScript [!DNL Analytics for Advertising] [!DNL Last Event Service], en l’état, enregistre les événements de visualisation et de clic publicitaire et les associe aux conversions associées à l’aide d’un ID supplémentaire (`SDID`). Cependant, la bibliothèque [!DNL Web SDK] ne fournit pas de [!DNL stitch ID]. Pour utiliser le [!DNL Web SDK] par [!DNL Analytics for Advertising], vous devez modifier 1) la balise [!DNL Last Event Service] que vous utilisez sur vos pages web et 2) vos commandes [!DNL Web SDK] `sendEvent` en conséquence.

## Étape 1 : modifier la balise [!DNL Last Event Service] pour générer une `[!DNL StitchID]`

Dans la balise [!DNL Analytics for Advertising] [!DNL Last Event Service] que vous utilisez sur vos pages web, ajoutez du code pour générer le `[!DNL StitchID]` à l’aide du générateur d’identifiants aléatoires fourni dans la bibliothèque.

**Balise héritée :**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id','rsid');
</script>
```

**Nouvelle balise :**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id','rsid').generateRandomId();
</script>
```

## Étape 2 : utiliser [!DNL Web SDK] pour envoyer le [!DNL StitchID] en tant que données XDM pour [!DNL Analytics]

Insérez la propriété suivante dans votre commande [!DNL Web SDK] `sendEvent` pour envoyer le [!DNL StitchID] à [!DNL Experience Edge] en tant que données [!DNL Experience Data Model] (XDM) pour [!DNL Analytics].<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] utilise la valeur comme `SDID`.

**Propriété à ajouter :**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Exemple:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Code JavaScript pour  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
