---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---
# Modèle de publicité texte - Méthode de mappage de groupe publicitaire

**[!UICONTROL Map Method]:** (Lorsque [!UICONTROL Map Only] est activé pour les groupes d’annonces ; tous les réseaux publicitaires sauf [!DNL Yandex]) Méthode par laquelle les nouveaux mots-clés et les nouvelles publicités sont mappés aux groupes publicitaires existants :

* *[!UICONTROL Contains Anywhere]:* Ajoute des données à un groupe publicitaire existant dont le nom inclut la chaîne spécifiée, le cas échéant.

* *[!UICONTROL Contains Exactly]:* Ajoute des données à un groupe publicitaire existant dont le nom inclut la chaîne spécifiée, le cas échéant.

* *[!UICONTROL Exactly Matches]* (valeur par défaut) : Ajoute des données à un groupe publicitaire existant portant le même nom, le cas échéant.

Lorsqu’aucune correspondance n’est trouvée, toutes les données du groupe publicitaire sont ignorées. Si les données du groupe publicitaire dans le flux n’incluent pas de données de campagne, le groupe publicitaire est mappé à un groupe publicitaire portant le même nom dans une campagne, le cas échéant. Si plusieurs correspondances de groupes publicitaires sont trouvées, les mots-clés et les publicités sont mappés à tous.
