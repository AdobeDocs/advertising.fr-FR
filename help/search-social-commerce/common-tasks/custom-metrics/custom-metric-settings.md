---
title: Paramètres de mesure personnalisés
description: Référencez les paramètres des mesures personnalisées, qui sont calculées à partir de mesures standard.
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---

# Paramètres de mesure personnalisés

Les paramètres de mesure personnalisés sont légèrement différents dans différentes parties de l’interface.

## Paramètres de mesure personnalisés dans les vues de gestion de campagne

| Paramètre/section | Description |
|----|----|
| Nom de mesure personnalisée | Nom de la mesure, qui s’affiche sous forme de nom de colonne. <b>Conseil :</b> Utilisez un nom de mesure significatif, mais considérez que les noms plus longs élargissent la largeur de la colonne. |
| Insérer une mesure | La formule mathématique utilisée pour calculer la nouvelle mesure (telle que [Cost]/[Inscriptions]) :<ul><li>Pour insérer une mesure à partir de la liste des mesures de trafic et de recettes, placez le curseur à l’endroit où vous souhaitez insérer la mesure, puis sélectionnez la mesure dans la liste ou saisissez-la manuellement et entre crochets (par exemple, `[CPC]`).</li><li>Pour insérer un opérateur, placez le curseur à l’endroit où vous souhaitez insérer l’opérateur, puis cliquez sur le bouton ou saisissez le symbole manuellement. Les opérateurs mathématiques disponibles : `+ - * / ( ) ()`</li></ul><b>Remarque :</b> Le calcul des mesures personnalisées complexes prend plus de temps et la génération des rapports et des vues qui les incluent (en particulier lorsqu’ils incluent des colonnes distinctes pour les conversions des clics publicitaires et des affichages publicitaires) prend plus de temps. |
| Format | Comment présenter les données pour cette mesure : *[!UICONTROL Currency]* (une valeur monétaire), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (un pourcentage avec deux décimales).<br><br><b>Attention :</b> Si vous créez une mesure dérivée au format [!UICONTROL Number w/out Decimal Points] (qui affiche les données sous forme d’entiers) et que vous l’incluez dans une vue ou un rapport qui utilise une règle d’attribution de conversion pondérée ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] ou [!UICONTROL Even Distribution]), la sortie est alors affichée en entiers, et non en décimales. Par conséquent, les champs de données individuels peuvent être incorrects, même si les totaux sont corrects. Par exemple, si une commande est divisée uniformément entre trois événements, une commande (au lieu de 0,33) est attribuée à chacun des trois événements. Pour éviter ce problème, utilisez le format de mesure [!UICONTROL Number to 2 Decimal Points]. |

## Paramètres de mesure personnalisés dans les rapports et les modèles de rapport et dans les vues [!UICONTROL Portfolios]

| Paramètre/section | Description |
|----|----|
| Nom de mesure personnalisée | Nom de la mesure, qui s’affiche sous forme de nom de colonne. <b>Conseil :</b> Utilisez un nom de mesure significatif, mais considérez que les noms plus longs élargissent la largeur de la colonne. |
| Format | Comment présenter les données pour cette mesure : *[!UICONTROL Currency]* (une valeur monétaire), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (un pourcentage avec deux décimales).<br><br><b>Attention :</b> Si vous créez une mesure dérivée au format [!UICONTROL Number w/out Decimal Points] (qui affiche les données sous forme d’entiers) et que vous l’incluez dans une vue ou un rapport qui utilise une règle d’attribution de conversion pondérée ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] ou [!UICONTROL Even Distribution]), la sortie est alors affichée en entiers, et non en décimales. Par conséquent, les champs de données individuels peuvent être incorrects, même si les totaux sont corrects. Par exemple, si une commande est divisée uniformément entre trois événements, une commande (au lieu de 0,33) est attribuée à chacun des trois événements. Pour éviter ce problème, utilisez le format de mesure [!UICONTROL Number to 2 Decimal Points]. |
| Insérer une mesure | Liste des mesures existantes à partir desquelles vous pouvez créer une formule.<br><br>Pour insérer une mesure dans le champ d’entrée de la formule, placez le curseur à l’endroit où vous souhaitez insérer la mesure, puis sélectionnez la mesure dans la liste ou saisissez-la manuellement et entre crochets (par exemple, `[CPC]`). |
| Insérer un opérateur | Les opérateurs mathématiques disponibles : `+ - x / ( )`<br><br>Pour insérer un opérateur dans le champ de saisie de la formule, placez le curseur à l&#39;endroit où vous souhaitez insérer l&#39;opérateur, puis cliquez sur le bouton ou saisissez le symbole manuellement. |
| [Champ d’entrée de formule pour la mesure] | Formule mathématique utilisée pour calculer la nouvelle mesure en fonction d’une ou de plusieurs propriétés existantes ou de mesures standard (telles que `[Cost]/[Registrations]`. Elle peut inclure n’importe quelle combinaison de mesures et d’opérateurs.<br><br><b>Remarque :</b> Le calcul des mesures personnalisées complexes prend plus de temps et la génération des rapports et des vues qui les incluent (en particulier lorsqu’ils incluent des colonnes distinctes pour les conversions des clics publicitaires et des affichages publicitaires) prend plus de temps. |

>[!MORELIKETHIS]
>
>* [À propos des mesures personnalisées](custom-metric-about.md)
>* [Créer une mesure personnalisée](custom-metric-create.md)
>* [Modifier une mesure personnalisée](custom-metric-edit.md)
>* [Supprimer une mesure personnalisée](custom-metric-delete.md)
