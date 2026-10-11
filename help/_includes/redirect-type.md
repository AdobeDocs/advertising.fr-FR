---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# Champ Type de redirection dans les paramètres du compte et de la campagne

**[!UICONTROL Redirect Type]:** (Pour les [!UICONTROL EF Redirect] uniquement) Méthode de redirection des utilisateurs finaux vers l’URL finale ou l’URL de destination. L’option sélectionnée s’applique à toutes les annonces, tous les mots-clés et tous les emplacements dans le compte ou la campagne. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur et le paramètre par défaut au niveau de la campagne est hérité des paramètres du compte.

* *[!UICONTROL Standard]:* pour simplement rediriger l’utilisateur final vers l’URL spécifiée.

* *[!UICONTROL Token]:* pour rediriger l’utilisateur final vers l’URL et enregistrer également l’ID Search, Social et Commerce pour le clic (`ef_id`) en tant que paramètre de chaîne de requête, utilisé comme jeton. Choisissez cette option si vous souhaitez signaler des transactions hors ligne, que Search, Social et Commerce échangent des données avec Adobe Analytics ou que vous souhaitez suivre toutes les conversions qui se produisent dans les navigateurs [!DNL Apple Safari].

**Remarques :**

* Si vous passez de [!UICONTROL Standard] à [!UICONTROL Token], ou vice versa, vous devez régénérer les URL de tracking pour le compte.
* Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.
