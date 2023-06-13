---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---
# Chemin d’affichage 1 et Chemin d’affichage 2 dans certains paramètres de publicité

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** (Facultatif) Texte ajouté à l’URL d’affichage automatiquement extrait de l’URL finale. Chaque chemin est précédé d’une barre oblique (`/`). Un chemin ne peut pas contenir de barre oblique (`/`) ou nouvelle ligne (`\n`). La longueur maximale de chaque chemin est de 15 ou 7 caractères codés sur deux octets.

Pour insérer un personnalisateur de publicités, utilisez les formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide :

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Par exemple, si [!UICONTROL Display Path 1] est &quot;offres&quot; et [!UICONTROL Display Path 2] est &quot;local&quot;, l’URL d’affichage serait `<display URL>/deals/local`, par exemple www.example.com/deals/local.
