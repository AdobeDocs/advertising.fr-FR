---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Modèle de publicité textuelle - Paramètres des mots-clés négatifs au niveau du groupe publicitaire

**[!UICONTROL Delete negative keywords when omitted from list]:** (Tous les réseaux publicitaires à l’exception de Yandex ; facultatif) supprime les mots-clés négatifs existants au niveau du groupe publicitaire précédemment créés à l’aide du modèle qui ne sont pas spécifiés dans les listes ci-dessous. **Remarque :** Les mots-clés négatifs créés par d’autres moyens (par exemple dans des feuilles d’envoi groupées, dans les vues [!UICONTROL Campaigns] ou dans l’éditeur de publicités du réseau publicitaire) ne sont jamais supprimés à l’aide du modèle.

**[!UICONTROL Apply these negatives]:** (Tous les réseaux publicitaires sauf [!DNL Yandex] ; facultatif) Tous les mots-clés négatifs statiques au niveau du groupe publicitaire à ajouter. Pour spécifier plusieurs mots-clés ou types de correspondance pour un même mot-clé, saisissez-les sur des lignes distinctes. Utilisez la syntaxe suivante, sans signe moins :

* Correspondance large négative : `keyword` (non pris en charge par [!DNL Microsoft Advertising])
* Correspondance d’expression négative : `"keyword"`
* Correspondance exacte négative : `[keyword]`

La syntaxe habituelle des types d’expression et de correspondance exacte est utilisée dans la feuille d’envoi groupé générée lorsque vous propagez les données de flux par le biais du modèle. **Remarque :** Vous ne pouvez pas voir les mots-clés négatifs dans l’onglet [!UICONTROL Keywords] ou dans la vue [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].
