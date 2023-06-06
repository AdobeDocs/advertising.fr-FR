---
title: Paramètres de mesure personnalisés
description: Référencez les paramètres des mesures personnalisées, qui sont calculées à partir de mesures standard.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# Paramètres de mesure personnalisés

Les paramètres de mesure personnalisés sont légèrement différents dans différentes parties de l’interface.

## Paramètres de mesure personnalisés dans les vues de gestion de campagne

| Paramètre/section | Description |
|----|----|
| Nom de mesure personnalisée | Nom de la mesure, qui s’affiche sous forme de nom de colonne. <b>Conseil :</b> Utilisez un nom de mesure significatif, mais considérez que les noms plus longs élargissent la colonne. |
| Insérer une mesure | Formule mathématique utilisée pour calculer la nouvelle mesure (telle que [Coût]/[Inscriptions]:<ul><li>Pour insérer une mesure à partir de la liste des mesures de trafic et de recettes, placez le curseur à l’endroit où vous souhaitez insérer la mesure, puis sélectionnez la mesure dans la liste ou saisissez-la manuellement et entre crochets (par exemple : `[CPC]`).</li><li>Pour insérer un opérateur, placez le curseur à l’endroit où vous souhaitez insérer l’opérateur, puis cliquez sur le bouton ou saisissez le symbole manuellement. Les opérateurs mathématiques disponibles : `+ - * / ( ) ()`</li></ul><b>Remarque :</b> Le calcul des mesures personnalisées complexes prend plus de temps et la génération des rapports et des vues qui les incluent (en particulier lorsqu’ils incluent des colonnes distinctes pour les conversions des clics publicitaires et des affichages publicitaires) prend plus de temps. |
| Format | Comment présenter les données pour cette mesure : *[!UICONTROL Currency]* (une valeur monétaire), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (un pourcentage avec deux points décimaux).<br><br><b>Attention :</b> Si vous créez une mesure dérivée au format [!UICONTROL Number w/out Decimal Points] (qui affiche les données sous forme d’entiers) et les inclut dans un affichage ou un rapport qui utilise une règle d’attribution de conversion pondérée ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]ou [!UICONTROL Even Distribution]), la sortie s’affiche sous forme d’entiers, et non de décimales. Par conséquent, les champs de données individuels peuvent être incorrects, même si les totaux sont corrects. Par exemple, si une commande est divisée uniformément entre trois événements, une commande (au lieu de 0,33) est attribuée à chacun des trois événements. Pour éviter ce problème, utilisez le format de mesure [!UICONTROL Number to 2 Decimal Points]. |

## Paramètres des mesures personnalisées dans les rapports et les modèles de rapports, ainsi que dans la variable [!UICONTROL Portfolios] views

| Paramètre/section | Description |
|----|----|
| Nom de mesure personnalisée | Nom de la mesure, qui s’affiche sous forme de nom de colonne. <b>Conseil :</b> Utilisez un nom de mesure significatif, mais considérez que les noms plus longs élargissent la colonne. |
| Format | Comment présenter les données pour cette mesure : *[!UICONTROL Currency]* (une valeur monétaire), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (un pourcentage avec deux points décimaux).<br><br><b>Attention :</b> Si vous créez une mesure dérivée au format [!UICONTROL Number w/out Decimal Points] (qui affiche les données sous forme d’entiers) et les inclut dans un affichage ou un rapport qui utilise une règle d’attribution de conversion pondérée ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]ou [!UICONTROL Even Distribution]), la sortie s’affiche sous forme d’entiers, et non de décimales. Par conséquent, les champs de données individuels peuvent être incorrects, même si les totaux sont corrects. Par exemple, si une commande est divisée uniformément entre trois événements, une commande (au lieu de 0,33) est attribuée à chacun des trois événements. Pour éviter ce problème, utilisez le format de mesure [!UICONTROL Number to 2 Decimal Points]. |
| Insérer une mesure | Liste des mesures existantes à partir desquelles vous pouvez créer une formule.<br><br>Pour insérer une mesure dans le champ de saisie de la formule, placez le curseur à l’endroit où vous souhaitez insérer la mesure, puis sélectionnez la mesure dans la liste ou saisissez-la manuellement et entre crochets (par exemple : `[CPC]`). |
| Insérer un opérateur | Les opérateurs mathématiques disponibles : `+ - x / ( )`<br><br>Pour insérer un opérateur dans le champ de saisie de la formule, placez le curseur à l&#39;endroit où vous souhaitez insérer l&#39;opérateur, puis cliquez sur le bouton ou saisissez le symbole manuellement. |
| [Champ d’entrée de formule pour la mesure] | Formule mathématique utilisée pour calculer la nouvelle mesure en fonction d’une ou de plusieurs propriétés existantes ou de mesures standard (telles que `[Cost]/[Registrations]`. Elle peut inclure n’importe quelle combinaison de mesures et d’opérateurs.<br><br><b>Remarque :</b> Le calcul des mesures personnalisées complexes prend plus de temps et la génération des rapports et des vues qui les incluent (en particulier lorsqu’ils incluent des colonnes distinctes pour les conversions des clics publicitaires et des affichages publicitaires) prend plus de temps. |

>[!MORELIKETHIS]
>
>* [À propos des mesures personnalisées](custom-metric-about.md)
>* [Création d’une mesure personnalisée](custom-metric-create.md)
>* [Modification d’une mesure personnalisée](custom-metric-edit.md)
>* [Suppression d’une mesure personnalisée](custom-metric-delete.md)

