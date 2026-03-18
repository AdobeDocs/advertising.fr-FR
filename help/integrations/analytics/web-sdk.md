---
title: Utilisation de la bibliothèque  [!DNL Last Event Service] JavaScript avec  [!DNL Web SDK]
description: Découvrez les étapes à suivre pour passer de l’utilisation de la bibliothèque  [!DNL Analytics] [!DNL visitorAPI] à la bibliothèque  [!DNL Experience Platform] [!DNL Web SDK] pour votre  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Utilisation de la bibliothèque [!DNL Last Event Service] JavaScript avec Adobe Experience Platform [!DNL Web SDK]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Si votre entreprise utilise l’ancienne bibliothèque `visitorAPI.js` d’Adobe Analytics pour la collecte de données, vous pouvez éventuellement passer à l’utilisation de la bibliothèque [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) (`alloy.js`), qui vous permet d’interagir avec les différents services Experience Cloud via [!DNL Edge Network].

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
