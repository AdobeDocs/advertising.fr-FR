---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# Modèle de publicité texte - Paramètres des mots-clés négatifs au niveau de la campagne

**[!UICONTROL Delete negative keywords when omitted from list]:** (Tous les réseaux publicitaires, à l’exception de Yandex) ; facultatif) Supprime les mots-clés négatifs existants au niveau de la campagne créés précédemment à l’aide du modèle qui ne sont pas spécifiés dans les listes ci-dessous. **Remarque :** Mots-clés négatifs créés par d’autres moyens (par exemple dans les feuilles d’envoi groupées, la variable [!UICONTROL Campaigns] les vues (ou dans l’éditeur de publicités du réseau publicitaire) ne sont jamais supprimées à l’aide du modèle.

**[!UICONTROL Set negative keywords by campaign name condition]:** (Tous les réseaux publicitaires, à l’exception de Yandex) ; (facultatif) Permet de spécifier des mots-clés négatifs pour les campagnes dont le nom inclut une chaîne spécifiée. Lorsque vous sélectionnez cette option, vous pouvez ajouter jusqu’à trois chaînes de nom de campagne et mots-clés correspondants.

Pour chaque chaîne, cliquez sur **[!UICONTROL Add (Up to 3)]** et saisissez les informations suivantes :

* **[!UICONTROL If campaign name contains]:**  Chaîne de texte à rechercher n’importe où dans le nom de la campagne. La requête est sensible à la casse (par exemple, &quot;[!DNL Car]&quot; correspond au nom de la campagne &quot;[!DNL Car Parts]&quot;, mais pas &quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;).

* **[!UICONTROL Apply these negatives]:**  Tout mot-clé négatif statique au niveau de la campagne à ajouter pour les campagnes dont le nom inclut la chaîne spécifiée. Pour spécifier plusieurs mots-clés ou types de correspondance pour un même mot-clé, saisissez-les sur des lignes distinctes. Utilisez la syntaxe suivante, sans signe moins :

   * Correspondance large négative : `keyword` (non pris en charge par [!DNL Microsoft Advertising])
   * Correspondance d’expression négative : `"keyword"`
   * Correspondance exacte négative : `[keyword]`

La syntaxe habituelle des types d’expression et de correspondance exacte est utilisée dans la feuille d’envoi groupé générée lorsque vous propagez les données de flux par le biais du modèle. **Remarque :** Vous ne pouvez pas voir les mots-clés négatifs dans la variable [!UICONTROL Keywords] ou dans le [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vue.

**[!UICONTROL All other campaigns: Apply these negatives]:** (Tous les réseaux publicitaires sauf [!DNL Yandex]; (facultatif) Tout mot-clé négatif statique au niveau de la campagne à ajouter pour les campagnes dont le nom ne correspond pas à une chaîne spécifiée. Pour spécifier plusieurs mots-clés ou types de correspondance pour un même mot-clé, saisissez-les sur des lignes distinctes. Utilisez la syntaxe suivante, sans signe moins :

* Correspondance large négative : `keyword` (non pris en charge par [!DNL Microsoft Advertising])
* Correspondance d’expression négative : `"keyword"`
* Correspondance exacte négative : `[keyword]`

La syntaxe habituelle des types d’expression et de correspondance exacte est utilisée dans la feuille d’envoi groupé générée lorsque vous propagez les données de flux par le biais du modèle. **Remarque :** Vous ne pouvez pas voir les mots-clés négatifs dans la variable [!UICONTROL Keywords] ou dans le [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] vue.
