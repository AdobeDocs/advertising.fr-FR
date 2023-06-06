---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---
# Champ Descriptions des publicités dans les paramètres publicitaires RSA

**[!UICONTROL Ad Descriptions]:** Au moins deux, et jusqu’à quatre, descriptions d’annonce, avec des pin’s de position facultatives. Le réseau publicitaire affiche des publicités comportant jusqu’à deux descriptions ; saisissez au moins deux. La longueur maximale de chaque description est de 90 caractères, y compris tout texte dynamique (comme les valeurs des mots-clés et des personnalisateurs de publicités).

Pour insérer un personnalisateur de publicités, utilisez les formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide :

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Pour épingler une description à une position spécifique, sélectionnez l’option d’épingle (par exemple, &quot;[!UICONTROL Pinned at position 1]&quot;). Au moins une description doit être disponible pour chaque poste. Si vous épinglez plusieurs descriptions à la même position, la publicité finale inclut toujours l’une de ces descriptions à la position spécifiée. Il se peut que les descriptions épinglées à la position 2 ne s’affichent pas avec la publicité.

Pour ajouter une description supplémentaire, cliquez sur **[!UICONTROL + Add]**.
