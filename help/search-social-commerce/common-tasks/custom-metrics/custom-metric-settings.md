---
title: Paramètres de mesure personnalisés
description: Référencez les paramètres des mesures personnalisées, qui sont calculées à partir des mesures standard.
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Paramètres de mesure personnalisés

Les paramètres des mesures personnalisées sont légèrement différents dans différentes parties de l’interface.

## Paramètres de mesure personnalisés dans la plupart des vues de gestion

| Paramètre/Section | Description |
|----|----|
| Nom de la mesure personnalisée | Nom de la mesure qui s’affiche comme nom de colonne. <b>Conseil :</b> utilisez un nom de mesure significatif, mais considérez que les noms plus longs élargissent la colonne. |
| Insérer une mesure | Formule mathématique utilisée pour calculer la nouvelle mesure (par exemple [Coût]/[Enregistrements] :<ul><li>Pour insérer une mesure dans la liste des mesures de trafic et de recettes, placez le curseur à l’endroit où vous souhaitez insérer la mesure, puis sélectionnez-la dans la liste ou saisissez-la manuellement et placez-la entre crochets (par exemple, `[CPC]`).</li><li>Pour insérer un opérateur, placez le curseur à l&#39;endroit où vous souhaitez insérer l&#39;opérateur, puis cliquez sur le bouton ou saisissez manuellement le symbole. Opérateurs mathématiques disponibles : `+ - * / ( ) ()`</li></ul><b>Remarque :</b> les mesures personnalisées complexes prennent plus de temps à calculer et les rapports et les vues qui les incluent (en particulier lorsqu’ils incluent des colonnes distinctes pour les conversions de clics publicitaires et de vues publicitaires) prennent plus de temps à générer. |
| Format | Présentation des données pour cette mesure : *[!UICONTROL Currency]* (valeur monétaire), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (pourcentage à deux décimales).<br><br><b>Attention :</b> si vous créez une mesure dérivée au format [!UICONTROL Number w/out Decimal Points] (qui affiche les données sous forme d’entiers) et que vous l’incluez dans une vue ou un rapport qui utilise une règle d’attribution de conversion pondérée ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] ou [!UICONTROL Even Distribution]), la sortie s’affiche sous forme d’entiers et non de décimales. Par conséquent, les champs de données individuels peuvent être incorrects, même si les totaux sont corrects. Par exemple, si un ordre est divisé de manière égale entre trois événements, un ordre (plutôt que 0,33 ordre) est attribué à chacun des trois événements. Pour éviter le problème, utilisez le format de mesure [!UICONTROL Number to 2 Decimal Points]. |

## Paramètres de mesure personnalisés dans les rapports et les modèles de rapport, ainsi que dans les vues de [!UICONTROL Portfolios] héritées

| Paramètre/Section | Description |
|----|----|
| Nom de la mesure personnalisée | Nom de la mesure qui s’affiche comme nom de colonne. <b>Conseil :</b> utilisez un nom de mesure significatif, mais considérez que les noms plus longs élargissent la colonne. |
| Format | Présentation des données pour cette mesure : *[!UICONTROL Currency]* (valeur monétaire), *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]* ou *[!UICONTROL Percentage]* (pourcentage à deux décimales).<br><br><b>Attention :</b> si vous créez une mesure dérivée au format [!UICONTROL Number w/out Decimal Points] (qui affiche les données sous forme d’entiers) et que vous l’incluez dans une vue ou un rapport qui utilise une règle d’attribution de conversion pondérée ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More] ou [!UICONTROL Even Distribution]), la sortie s’affiche sous forme d’entiers et non de décimales. Par conséquent, les champs de données individuels peuvent être incorrects, même si les totaux sont corrects. Par exemple, si un ordre est divisé de manière égale entre trois événements, un ordre (plutôt que 0,33 ordre) est attribué à chacun des trois événements. Pour éviter le problème, utilisez le format de mesure [!UICONTROL Number to 2 Decimal Points]. |
| Insérer une mesure | Liste des mesures existantes à partir desquelles vous pouvez créer une formule.<br><br>Pour insérer une mesure dans le champ de saisie de formule, placez le curseur à l’endroit où vous souhaitez insérer la mesure, puis sélectionnez-la dans la liste ou saisissez-la manuellement et placez-la entre crochets (par exemple, `[CPC]`). |
| Insérer un opérateur | Opérateurs mathématiques disponibles : `+ - x / ( )`<br><br>Pour insérer un opérateur dans le champ de saisie de formule, placez le curseur à l&#39;endroit où vous souhaitez insérer l&#39;opérateur, puis cliquez sur le bouton ou saisissez manuellement le symbole. |
| [Champ de saisie de formule pour la mesure] | Formule mathématique utilisée pour calculer la nouvelle mesure en fonction d’une ou de plusieurs propriétés existantes ou mesures standard (telles que `[Cost]/[Registrations]`. Il peut inclure n’importe quelle combinaison de mesures et d’opérateurs.<br><br><b>Remarque :</b> les mesures personnalisées complexes prennent plus de temps à calculer et les rapports et les vues qui les incluent (en particulier lorsqu’ils incluent des colonnes distinctes pour les conversions de clics publicitaires et de vues publicitaires) prennent plus de temps à générer. |

>[!MORELIKETHIS]
>
>* [À propos des mesures personnalisées](custom-metric-about.md)
>* [Créer une mesure personnalisée](custom-metric-create.md)
>* [Modifier une mesure personnalisée](custom-metric-edit.md)
>* [Supprimer une mesure personnalisée](custom-metric-delete.md)
