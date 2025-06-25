---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---
# Champs de niveau 2 - niveau 8 dans les modèles d’annonces d’achats

**[!UICONTROL Tier  2 - Tier 8]:** (lorsque vous ajoutez des niveaux de groupes de produits). Type d’attribut de produit selon lequel cibler les produits, et critères de qualification pour le type d’attribut sélectionné (par exemple, Brand=Acme ou Condition=New). Les valeurs sont appliquées de manière hiérarchique pour déterminer les produits éligibles. Sélectionnez un type d’attribut et saisissez les critères de qualification. Les caractères interdits sont les suivants : `[ ] < > >>` (deux signes « supérieur à » consécutifs), utilisés pour désigner les noms de colonne dans le modèle, les noms de modificateur dans le modèle et les séparateurs de niveau dans la colonne [!UICONTROL Parent Product Grouping] dans les feuilles d’envoi groupé.

Vous pouvez inclure jusqu’à huit niveaux (niveaux) de groupes de produits, y compris « [!UICONTROL All Products] » (niveau 1). Chaque niveau peut inclure plusieurs groupes de produits, mais ils doivent appartenir au même type d’attribut (tel que « Condition »).

>[!NOTE]
>
>* ([!DNL Google Ads] uniquement) Les valeurs possibles pour [!UICONTROL Channel] sont « [!UICONTROL Local] » ou « [!UICONTROL Online] » et les valeurs possibles pour [!UICONTROL ChannelExclusivity] sont « [!UICONTROL SingleChannel] » et « [!UICONTROL MultiChannel] ».
>* Lorsque vous créez un groupe de produits de second niveau (enfant) pour un groupe publicitaire à partir de l’onglet [!UICONTROL Product Groups] dans la vue [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] , un autre groupe de produits, appelé « [!UICONTROL Everything Else] », est automatiquement créé à l’aide de l’enchère du groupe publicitaire par défaut. Toutefois, en utilisant des modèles de flux d’inventaire, les groupes de produits « [!UICONTROL Everything Else] » sont exclus.
>* Lorsque vous incluez plusieurs niveaux et qu’aucune valeur n’est disponible pour le dernier niveau (le plus grand nombre), le niveau supérieur suivant est utilisé comme groupe de produits soumissionnaires. Par exemple, si vous incluez cinq niveaux et qu’aucune valeur n’est disponible pour le niveau 5, le niveau 4 est utilisé comme groupe de produits (unité) pouvant faire l’objet d’une offre. Cependant, si aucune valeur n’est disponible pour un niveau intermédiaire, la ligne est ignorée. Par exemple, si vous incluez cinq niveaux et que le niveau 5 a une valeur, mais que le niveau 4 n’en a pas, la ligne 4 est ignorée.
