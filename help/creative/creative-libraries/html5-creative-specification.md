---
title: Spécification de création HTML 5
description: Référencez la spécification de création HTML5 pour l’Advertising Creative.
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---

# Spécification créative HTML 5 pour l’Advertising Creative

Ce document décrit les exigences et la prise en charge de l’API pour les contenus publicitaires HTML 5 dans [!DNL Creative]. L’API permet le développement de contenus publicitaires HTML 5 dont les attributs peuvent être configurés au moment de la diffusion des contenus publicitaires.

## Champ d’application

[!DNL Creative] prend en charge les bannières HTML5 avec des contenus publicitaires non enrichis qui apparaissent dans des bordures définies sur une page. Vous pouvez utiliser les types de contenus publicitaires HTML 5 suivants :

<!--Remove to simplify:

* **Simple HTML5:** Supports a single landing page URL that can be configured during creative creation and trafficking.

* **Static HTML5:** Supports up to 5 landing page URLs that can be configured during creative creation and trafficking.

-->

* **HTML 5:** prend en charge jusqu’à 5 URL de page de destination configurables lors de la création créative et du trafic.

* **Flexible HTML 5:** prend en charge jusqu’à 5 URL de page de destination qui peuvent être configurées lors de la création créative et du trafic. Il permet également de modifier les attributs créatifs lors de la création créative et du trafic.

## Conditions requises

### Exigences relatives aux dossiers et à la compression

* Le contenu créatif doit être compressé dans un fichier ZIP (format .ZIP). Les fichiers ZIP imbriqués ne sont pas pris en charge. N’incluez donc pas de dossier compressé dans le dossier compressé externe.

* Le fichier ZIP doit contenir au moins un fichier d’HTML (le fichier d’affichage d’HTML principal) qui inclut une référence à la bibliothèque JavaScript [!DNL Creative]. Le fichier d’HTML principal peut se trouver dans le dossier racine ou dans un sous-dossier.

* Le fichier d’HTML principal peut porter n’importe quel nom, à condition qu’il n’inclue pas de caractères spéciaux, bien que `index.html` soit recommandé.

* Toutes les ressources nécessaires au rendu de la création finale doivent se trouver dans le même dossier que le fichier d’affichage HTML ou dans des sous-dossiers du dossier principal.

* N’incluez dans le contenu créatif aucun fichier qui n’est pas référencé pour ce contenu créatif.

### Inclusion du fichier JavaScript Advertising Creative

Le fichier d&#39;HTML principal — et aucun autre fichier — doit contenir une référence au fichier JavaScript `AMOLibrary.js`. Appelez le fichier à la première ligne de la section `<head>` en utilisant l’adresse suivante :

`https://ads.everesttech.net/ads/static/local/AMOLibrary.js`

Ce fichier contient des fonctions pour s’assurer que le test local des événements de sortie se produit sans problème.

<!-- Remove to simplify:

### Simple HTML5 creative requirements

#### Support for click-through URLS in simple HTML5

The `<head>` section of the main HTML file must include a JavaScript variable name `clickTag` or `clickTAG`. The value of the variable should be the landing page URL. See the following example.

```
<script type=”text/javascript”>
var clickTag = “http://www.example.com”;
</script>
```

>[!NOTE]
>
>The static URL you include in the HTML5 creative is used for local testing purposes only and will be overwritten. When you upload an HTML5 creative, you'll define the default landing page for the `clickTag` variable. When you assign an uploaded HTML5 creative to an ad experience, you can optionally override the default landing page for the `clickTag` variable, and [!DNL Creative] adds click tracking to the URL when you save the experience.

-->

<!-- Renamed to simplify:
### Static HTML5 creative requirements
-->

### Exigences de création HTML5

#### Prise en charge des URL de clics publicitaires en HTML statique5

##### `amo.registerClick(clkVar, clkUrl)`

Enregistre les URL de clics publicitaires et le paramètre associé utilisé pour référencer chaque URL (connu sous le nom de `clickTag`). Cela indique au serveur de publicités [!DNL Creative] où ajouter le suivi des clics. Vous pouvez utiliser cette API pour enregistrer jusqu’à cinq variables de balises de clic, chacune avec une URL de page de destination correspondante.

>[!NOTE]
>
>Les URL statiques que vous incluez dans le contenu créatif d’HTML 5 sont utilisées uniquement à des fins de test local et seront remplacées. Lorsque vous téléchargez un contenu créatif HTML5, vous définissez la page de destination par défaut pour chaque variable `clickTag`. Lorsque vous affectez un contenu créatif HTML 5 chargé à une expérience publicitaire, vous pouvez éventuellement remplacer la page de destination par défaut pour chaque variable de `clickTag`, et [!DNL Creative] ajoute le suivi des clics aux URL lorsque vous enregistrez l’expérience.

###### Paramètres

* `clkVar` : nom de la variable de clic (généralement « clickTag »), entre guillemets.

* `clkUrl` : URL de la page de destination de cette variable de clic, entre guillemets doubles.

###### Utilisation

Appelez `amo.registerClick()` dans la section `<head>` du fichier d’HTML principal.

###### Exemple

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Déclenche l’événement de sortie, qui redirige l’utilisateur vers la page de destination configurée pour le `clickTag`. Lors des tests locaux, cette fonction avertit les développeurs si l’URL transmise à la fonction a été enregistrée.

###### Paramètres

* `clkTag` : nom de la variable de clic que vous utilisez pour attribuer l&#39;URL de la page de destination à l&#39;aide de la fonction `amo.registerClick()`, entre guillemets simples.

* `event` — (Facultatif) Objet d’événement « clic » JavaScript. Cette option enregistre les coordonnées des clics, qui peuvent ensuite être utilisées pour analyser les performances créatives.

###### Utilisation

Appelez `amo.onAdClick()` dans la section `<body>` du fichier d’HTML principal.

###### Exemples

`amo.onAdClick('clickTag')` OU `amo.onAdClick('clickTag',clickEvt)`

### Exigences de création flexibles d’HTML 5

#### Prise en charge des URL de clics publicitaires dans un HTML flexible5

##### `amo.registerClick(clkVar, clkUrl)`

Enregistre les URL de clics publicitaires et le paramètre associé utilisé pour référencer chaque URL (connu sous le nom de `clickTag`). Cela indique au serveur de publicités [!DNL Creative] où ajouter le suivi des clics. Vous pouvez utiliser cette API pour enregistrer jusqu’à cinq variables de balises de clic, chacune avec une URL de page de destination correspondante.

>[!NOTE]
>
>Les URL statiques que vous incluez dans le contenu créatif d’HTML 5 sont utilisées uniquement à des fins de test local et seront remplacées. Lorsque vous téléchargez un contenu créatif HTML5, vous définissez la page de destination par défaut pour chaque variable `clickTag`. Lorsque vous affectez un contenu créatif HTML 5 chargé à une expérience publicitaire, vous pouvez éventuellement remplacer la page de destination par défaut pour chaque variable de `clickTag`, et [!DNL Creative] ajoute le suivi des clics aux URL lorsque vous enregistrez l’expérience.

###### Paramètres

* `clkVar` : nom de la variable de clic (généralement « clickTag »), entre guillemets.

* `clkUrl` : URL de la page de destination de cette variable de clic, entre guillemets doubles.

###### Utilisation

Appelez `amo.registerClick()` dans la section `<head>` du fichier d’HTML principal.

###### Exemple

`amo.registerClick("clickTag","http://www.example.com")`

##### `amo.onAdClick(clk, event)`

Déclenche l’événement de sortie, qui redirige l’utilisateur vers la page de destination configurée pour le `clickTag`. Lors des tests locaux, cette fonction avertit les développeurs si l’URL transmise à la fonction a été enregistrée.

###### Paramètres

* `clkTag` : nom de la variable de clic que vous utilisez pour attribuer l&#39;URL de la page de destination à l&#39;aide de la fonction `amo.registerClick()`, entre guillemets simples.

* `event` — (Facultatif) Objet d’événement « clic » JavaScript. Cette option enregistre les coordonnées des clics, qui peuvent ensuite être utilisées pour analyser les performances créatives.

###### Utilisation

Appelez `amo.onAdClick()` dans la section `<body>` du fichier d’HTML principal.

###### Exemples

`amo.onAdClick('clickTag')` OU `amo.onAdClick('clickTag',clickEvt)`

#### Prise en charge des attributs créatifs dans un HTML flexible5

##### `amo.registerAttribute(key, type, value)`

Définit les attributs des contenus publicitaires qui peuvent être modifiés au moment de la création ou de l’expérience. Vous pouvez définir jusqu’à 20 attributs de création configurables au moment de la création de contenu créatif ou d’expérience.

>[!NOTE]
>
>Les valeurs définies dans cette méthode sont utilisées uniquement pour le développement local et ne sont pas utilisées dans les services de publicités en direct.

###### Paramètres

* `key` : nom alphanumérique de l&#39;attribut. Il doit commencer par un caractère alphabétique.

* `type` — Type d&#39;attribut (`TEXT` ou `IMAGE`).

* `value` — Valeur de l&#39;attribut pour le test. Pour les attributs de type `IMAGE`, la valeur doit être le chemin d’accès relatif au fichier image.

###### Utilisation

Appelez `amo.registerAttribute()` pour enregistrer un attribut créatif, un type et une valeur lors du test en mode local. Tous les fichiers image utilisés comme exemples de valeurs doivent être compressés dans le fichier ZIP avec le package chargé.

##### `amo.attributes`

Objet JSON pour interroger les noms et valeurs des variables d’attributs de création. Les clés d’objet seront les noms d’attributs et les valeurs seront les valeurs de ces attributs.

En mode de test local, les paires clé-valeur sont les paires enregistrées par l’API `amo.registerAttribute`. Pour la production, les noms et valeurs des variables d’attributs créatifs doivent être configurés au moment de la création créative et du trafic.

### Exigences en matière de contenu créatif

La plupart des exchanges d’affichage disponibles dans Advertising DSP ont les exigences de création suivantes :

* Une bordure pleine doit entourer toutes les images publicitaires.

* L’extension des annonces n’est pas autorisée.

* La page de destination doit s’ouvrir dans une nouvelle fenêtre.

* Le domaine de la page de destination et ses sous-domaines ne doivent pas dépasser 35 caractères. **Remarque :** les URL de la page de destination finale sont définies dans le DSP et non dans les ressources HTML5 elles-mêmes.

* Toutes les clauses de non-responsabilité concernant l’offre d’une publicité doivent être incluses dans la publicité elle-même, et pas seulement sur la page de destination.

<!-- * (Dynamic HTML5 creatives) Do not use `window.open` to handle clicks in your code. Always use `amo.onDynAdClick` to handle click-throughs. -->

## Exemple de contenu en tant qu’objet et tableau JSON

### Exemple de contenu en tant qu’objet JSON

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
}
```

### Exemple de contenu en tant que tableau JSON

<!-- Should I update these to current/real URLs? Sent email to Apoorva 1/22. -->

```
[{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-assets-720x472.png",
"product_url": "http://www.adobe.com/creativecloud.html?promoid=ZP46FD38&mv=other"
},

{
"name": "Adobe Creative",
"description": "Creative",
"picture_url": "http://wwwimages.adobe.com/content/dam/acom/en/products/creativecloud/max2016/images/cc-overview-mobile-720x520.png",
"product_url": "http://adobe.com/"
}

]
```

## Exemple de contenu créatif HTML 5

### Exemple de structure de dossiers (après décompression)

* index.html

* /assets (dossier)

   * bg.jpg (image JPG, PNG, SVG ou GIF)

### Exemple de fichier d’HTML (index.html) pour les contenus publicitaires HTML 5 simples

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

### Exemple de fichier d’HTML (index.html) pour les contenus publicitaires HTML 5 statiques

```
<!DOCTYPE html>
<html>
<head>
  <script type="text/javascript" src="https://ads.everesttech.net/ads/static/local/AMOLibrary.js"></script>
  <script type="text/javascript">
  amo.registerClick("clickTag","http://www.example.com");
  amo.registerClick("clickTag2","http://www.example2.com");
  amo.registerClick("clickTag3","http://www.example3.com");
  amo.registerClick("clickTag4","http://www.example4.com");
  amo.registerClick("clickTag5","http://www.example5.com");
  </script>
</head>
<body>
  <a href="javascript:amo.onAdClick('clickTag')">
  <img src="assets/bg.jpg" width="300" height="250" style="position:absolute;top:0px;left:0px;">
  </a>
</body>
</html>
```

>[!MORELIKETHIS]
>
>* [Ajouter des contenus publicitaires standard à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-standard.md)
