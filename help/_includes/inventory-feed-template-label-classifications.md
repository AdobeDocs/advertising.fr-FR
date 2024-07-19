---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---
# Modèle de publicité texte - Classifications des étiquettes

**\[Composant\] [!UICONTROL Label Classifications] > \[Classification d’étiquette et valeur\]:** (facultatif) Valeurs de cinq classifications d’étiquettes existantes au maximum à attribuer aux différents composants de campagne créés ou modifiés à l’aide du modèle. Les valeurs d’étiquette sont héritées par les entités enfants (y compris les entités enfants qui sont créées ultérieurement). Vous n’avez donc pas besoin de saisir de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées. Les classifications d’étiquettes pour les groupes de produits sont appliquées au niveau de l’unité (la plus granulaire).

Pour chaque composant de campagne auquel vous souhaitez affecter des classifications d’étiquettes :

1. Cochez la case en regard de **\[Component\][!UICONTROL Label Classifications]**.

1. Configurez les valeurs de classification des étiquettes pour le modèle :

   * Pour chaque classification et valeur d’étiquette à affecter au composant, procédez comme suit :

      1. Cliquez sur **[!UICONTROL Add Label Classification]**.

      1. Sélectionnez la classification de libellé existante, puis sélectionnez une valeur existante ou saisissez une nouvelle valeur.

         La longueur maximale de chaque valeur est de 100 caractères. Elle peut contenir des caractères ASCII et non ASCII.

         Pour insérer un nom de colonne en tant que paramètre dynamique pour une valeur de classification de libellé, cliquez dans le champ de saisie (le deuxième champ), puis cliquez sur un nom de colonne dans la liste des colonnes.

         Vous ne pouvez inclure qu’une seule valeur par classification par composant de campagne. Par exemple, une campagne peut avoir Color=Red mais pas Color=Red et Color=Blue.

   * Pour modifier une valeur de classification de libellé existante, sélectionnez ou saisissez une nouvelle valeur.

   * Pour supprimer une valeur de classification d’étiquette existante, cliquez sur **[!UICONTROL X]** en regard de la valeur.
