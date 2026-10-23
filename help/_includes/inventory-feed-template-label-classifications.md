---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%
---
# Texte et modèle - Classifications de libellés

**\[Composant\] [!UICONTROL Label Classifications] > \[Classification de libellé et valeur\]:** (facultatif) valeurs pour un maximum de cinq classifications de libellé existantes à affecter aux différents composants de campagne créés ou modifiés à l’aide du modèle. Les valeurs de libellé sont héritées par les entités enfants (y compris les entités enfants créées ultérieurement). Il n’est donc pas nécessaire de saisir des valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées. Les classifications d’étiquettes pour les groupes de produits sont appliquées au niveau de l’unité (le plus granulaire).

Pour chaque composant de campagne auquel vous souhaitez affecter des classifications de libellés :

1. Cochez la case en regard de **\[Composant\][!UICONTROL Label Classifications]**.

1. Configurez les valeurs de classification des libellés pour le modèle :

   * Pour chaque classification de libellé et valeur à affecter au composant, procédez comme suit :

     1. Cliquez sur **[!UICONTROL Add Label Classification]**.

     1. Sélectionnez la classification d’étiquettes existante, puis sélectionnez une valeur existante ou saisissez-en une nouvelle.

        La longueur maximale de chaque valeur est de 100 caractères et peut inclure des caractères ASCII et non ASCII.

        Pour insérer un nom de colonne en tant que paramètre dynamique pour une valeur de classification d&#39;étiquette, cliquez dans le champ de saisie (deuxième champ), puis cliquez sur un nom de colonne dans la liste des colonnes.

        Vous ne pouvez inclure qu’une seule valeur par classification par composant de campagne. Par exemple, une campagne peut avoir Color=Red mais pas Color=Red et Color=Blue.

   * Pour modifier une valeur de classification de libellé existante, sélectionnez ou saisissez une nouvelle valeur.

   * Pour supprimer une valeur de classification de libellé existante, cliquez sur **[!UICONTROL X]** en regard de la valeur.
