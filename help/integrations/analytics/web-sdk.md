---
title: Utilisation de la  [!DNL Last Event Service] bibliothèque JavaScript avec [!DNL Web SDK]
description: Découvrez les étapes pour passer de l’utilisation de la bibliothèque [!DNL Analytics] [!DNL visitorAPI] à la bibliothèque [!DNL Experience Platform] [!DNL Web SDK] pour votre implémentation  [!DNL Analytics for Advertising] .
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Utilisation de la bibliothèque [!DNL Last Event Service] JavaScript avec Adobe Experience Platform [!DNL Web SDK]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Si votre organisation utilise la bibliothèque Adobe Analytics `visitorAPI.js` héritée pour la collecte de données, vous pouvez éventuellement passer à l’utilisation de la bibliothèque [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr) (`alloy.js`), qui vous permet d’interagir avec les différents services Experience Cloud par le biais de [!DNL Edge Network].

La bibliothèque JavaScript [!DNL Analytics for Advertising] [!DNL Last Event Service], en l’état, enregistre les événements d’affichage publicitaire et de clic publicitaire et les regroupe aux conversions associées à l’aide d’un ID supplémentaire (`SDID`). La bibliothèque [!DNL Web SDK] ne fournit toutefois pas de [!DNL stitch ID]. Pour utiliser [!DNL Web SDK] pour [!DNL Analytics for Advertising], vous devez modifier 1) la balise [!DNL Last Event Service] que vous utilisez sur vos pages web et 2) vos commandes [!DNL Web SDK] `sendEvent` en conséquence.

## Étape 1 : modifiez votre balise [!DNL Last Event Service] pour générer un `[!DNL StitchID]`

Dans la balise [!DNL Analytics for Advertising] [!DNL Last Event Service] que vous utilisez sur vos pages web, ajoutez du code pour générer le `[!DNL StitchID]` à l’aide du générateur d’ID aléatoire fourni dans la bibliothèque .

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

## Étape 2 : utilisez [!DNL Web SDK] pour envoyer les [!DNL StitchID] en tant que données XDM pour [!DNL Analytics]

Insérez la propriété suivante dans votre commande [!DNL Web SDK] `sendEvent` pour envoyer les [!DNL StitchID] vers [!DNL Experience Edge] en tant que données [!DNL Experience Data Model] (XDM) pour [!DNL Analytics].<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] utilise la valeur comme `SDID`.

**Propriété à ajouter :**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Exemple :**

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
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [Code JavaScript pour [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)
