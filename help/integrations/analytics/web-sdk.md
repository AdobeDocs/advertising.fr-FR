---
title: En utilisant la variable [!DNL Last Event Service] Bibliothèque JavaScript avec [!DNL Web SDK]
description: Découvrez les étapes à suivre pour passer de l’utilisation de la méthode [!DNL Analytics] [!DNL visitorAPI] vers la bibliothèque [!DNL Experience Platform] [!DNL Web SDK] de votre bibliothèque [!DNL Analytics for Advertising] implémentation.
feature: Integration with Adobe Analytics
exl-id: 764724a2-536a-43b9-955d-28d6146db29a
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# En utilisant la variable [!DNL Last Event Service] Bibliothèque JavaScript avec Adobe Experience Platform [!DNL Web SDK]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Si votre entreprise utilise l’Adobe Analytics hérité `visitorAPI.js` pour la collecte de données, vous pouvez éventuellement passer à l’aide de la bibliothèque [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) Bibliothèque (`alloy.js`), qui vous permet d’interagir avec les différents services Experience Cloud via le [!DNL Edge Network].

La variable [!DNL Analytics for Advertising] [!DNL Last Event Service] La bibliothèque JavaScript, en l’état, enregistre les événements d’affichage publicitaire et de clic publicitaire et les regroupe aux conversions associées à l’aide d’un ID supplémentaire (`SDID`). La variable [!DNL Web SDK] Toutefois, la bibliothèque ne fournit pas de [!DNL stitch ID]. Pour utiliser la variable [!DNL Web SDK] pour [!DNL Analytics for Advertising], vous devez modifier 1) la variable [!DNL Last Event Service] marquer que vous utilisez sur vos pages web et 2) vos [!DNL Web SDK] `sendEvent` des commandes en conséquence.

## Étape 1 : Modifiez votre [!DNL Last Event Service] Balise pour générer un `[!DNL StitchID]`

Dans le [!DNL Analytics for Advertising] [!DNL Last Event Service] de la balise que vous utilisez sur vos pages web, ajoutez le code pour générer la variable `[!DNL StitchID]` en utilisant le générateur d’ID aléatoire fourni dans la bibliothèque.

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

## Étape 2 : utilisez [!DNL Web SDK] pour envoyer le [!DNL StitchID] comme données XDM pour [!DNL Analytics]

Insérez la propriété suivante dans votre [!DNL Web SDK] `sendEvent` pour envoyer la commande [!DNL StitchID] to [!DNL Experience Edge] as [!DNL Experience Data Model] Données (XDM) pour [!DNL Analytics].<!-- The library sends the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] utilise la valeur comme `SDID`.

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
