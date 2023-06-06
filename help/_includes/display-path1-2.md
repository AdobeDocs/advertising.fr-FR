---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# Chemin d’affichage 1 et Chemin d’affichage 2 dans certains paramètres de publicité

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Facultatif) Texte ajouté à l’URL d’affichage automatiquement extrait de l’URL finale. Chaque chemin est précédé d’une barre oblique (`/`). Un chemin ne peut pas contenir de barre oblique (`/`) ou nouvelle ligne (`\n`). La longueur maximale de chaque chemin est de 15 ou 7 caractères codés sur deux octets.

Pour insérer un personnalisateur de publicités, utilisez les formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide :

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Par exemple, si Chemin d’affichage 1 est &quot;offres&quot; et Chemin d’affichage 2 est &quot;local&quot;, l’URL d’affichage sera `<display URL>/deals/local`, par exemple www.example.com/deals/local.
