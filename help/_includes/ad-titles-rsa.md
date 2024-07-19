---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Champ Titre de publicité dans les paramètres de publicité RSA

**[!UICONTROL Ad Titles]:** Au moins trois titres de publicité (titres) et jusqu’à quinze titres (titres), avec des pointes de position facultatives. Le réseau publicitaire affiche des publicités avec jusqu’à trois titres ; saisissez au moins trois titres. La longueur maximale de chaque titre est de 30 caractères, y compris les caractères dynamiques
texte (comme les valeurs des mots-clés et des personnalisateurs de publicités).

Pour insérer un personnalisateur de publicités, utilisez les formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide :

* [!DNL Google Ads] : `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising] : `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

Pour épingler un titre à une position spécifique, sélectionnez l’option d’épingle (telle que &quot;[!UICONTROL Pinned at position 1]&quot;). Au moins un titre doit être disponible pour chaque poste. Si vous épinglez plusieurs titres à la même position, la publicité finale inclut toujours l’un de ces titres à la position spécifiée. Il se peut que les titres épinglés à la position 3 ne s’affichent pas avec la publicité.

Pour ajouter un titre supplémentaire, cliquez sur **[!UICONTROL + Add]**.
