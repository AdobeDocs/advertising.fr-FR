---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# Texte et modèle - Paramètres des mots-clés négatifs au niveau du groupe publicitaire

**[!UICONTROL Delete negative keywords when omitted from list]:** (Tous les réseaux publicitaires, à l’exception de Yandex ; facultatif) Supprime les mots-clés négatifs existants au niveau du groupe publicitaire créés précédemment à l’aide du modèle qui ne sont pas spécifiés dans les listes ci-dessous. **Remarque :** les mots-clés négatifs créés par d’autres moyens (tels que dans les feuilles d’envoi groupé simples, les vues [!UICONTROL Campaigns] ou dans l’éditeur d’annonces du réseau publicitaire) ne sont jamais supprimés à l’aide du modèle.

**[!UICONTROL Apply these negatives]:** (Tous les réseaux publicitaires, à l’exception de [!DNL Yandex] ; facultatif) Tous les mots-clés négatifs au niveau du groupe publicitaire statique à ajouter. Pour spécifier plusieurs mots-clés ou plusieurs types de correspondance pour le même mot-clé, saisissez-les sur des lignes distinctes. Utilisez la syntaxe suivante, sans signe moins :

* Correspondance large négative : `keyword` (non prise en charge par [!DNL Microsoft Advertising])
* Correspondance de l’expression négative : `"keyword"`
* Correspondance exacte négative : `[keyword]`

La syntaxe habituelle pour les types de correspondance exacte et d’expression est utilisée dans la feuille d’envoi groupé générée lorsque vous propagez des données de flux à travers le modèle. **Remarque :** vous ne pouvez pas voir les mots-clés négatifs dans l&#39;onglet [!UICONTROL Keywords] ou dans la vue [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns].
