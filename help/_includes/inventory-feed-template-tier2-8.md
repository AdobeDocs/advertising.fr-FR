---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 0%

---
# Niveau 2 - Champs de niveau 8 dans les modèles de publicités commerciales

**[!UICONTROL Tier  2 - Tier 8]:** (Lorsque vous ajoutez des niveaux de groupes de produits) Un type d’attribut de produit par lequel cibler les produits, ainsi que les critères admissibles pour le type d’attribut sélectionné (par exemple, Marque=Acme ou Condition=Nouveau). Les valeurs sont appliquées de manière hiérarchique pour déterminer les produits éligibles. Sélectionnez un type d’attribut et saisissez les critères de qualification. Les caractères interdits sont les suivants : `[ ] < > >>` (deux signes &quot;supérieur à&quot; consécutifs), qui sont utilisés pour désigner les noms de colonne dans le modèle, les noms de modificateur dans le modèle et les séparateurs de niveau dans le [!UICONTROL Parent Product Grouping] dans les feuilles d’envoi groupé.

Vous pouvez inclure jusqu’à huit niveaux (niveaux) de groupes de produits, y compris &quot;[!UICONTROL All Products]&quot; (Niveau 1). Chaque niveau peut inclure plusieurs groupes de produits, mais ils doivent se rapporter au même type d’attribut (comme &quot;Condition&quot;).

>[!NOTE]
>
>* ([!DNL Google Ads] uniquement) Les valeurs possibles pour [!UICONTROL Channel] sont &quot;[!UICONTROL Local]&quot; ou &quot;[!UICONTROL Online],&quot; et les valeurs possibles pour [!UICONTROL ChannelExclusivity] sont &quot;[!UICONTROL SingleChannel]&quot; et &quot;[!UICONTROL MultiChannel].&quot;
>* Lorsque vous créez un groupe de produits de deuxième niveau (enfant) pour un groupe publicitaire à partir de la variable [!UICONTROL Product Groups] dans le [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] view, un autre groupe de produits appelé &quot;[!UICONTROL Everything Else],&quot; est automatiquement créé à l’aide de l’offre par défaut du groupe publicitaire. Toutefois, en utilisant des modèles de flux d’inventaire, &quot;[!UICONTROL Everything Else]&quot;les groupes de produits sont exclus.
>* Lorsque vous incluez plusieurs niveaux et qu’aucune valeur n’est disponible pour le niveau final (le plus élevé), le niveau supérieur est utilisé comme groupe de produits admissible. Par exemple, si vous incluez cinq niveaux et qu’aucune valeur n’est disponible pour le niveau 5, le niveau 4 est utilisé comme groupe de produits soumis à enchères (unité). Cependant, si aucune valeur n’est disponible pour un niveau intermédiaire, la ligne est ignorée. Par exemple, si vous incluez cinq niveaux et que le niveau 5 a une valeur mais que le niveau 4 ne l’a pas, la ligne 4 est ignorée.

