---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---
# Champ Type de redirection dans les paramètres du compte et de l’opération

**[!UICONTROL Redirect Type]:** (Pour [!UICONTROL EF Redirect] uniquement) Méthode de redirection des utilisateurs finaux vers l’URL finale ou l’URL de destination. L’option sélectionnée s’applique à toutes les publicités, mots-clés et emplacements du compte ou de la campagne. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur et le paramètre par défaut au niveau de la campagne est hérité des paramètres du compte.

* *[!UICONTROL Standard]:* Pour rediriger simplement l’utilisateur vers l’URL spécifiée.

* *[!UICONTROL Token]:* Pour rediriger l’utilisateur vers l’URL et enregistrer l’identifiant Search, Social &amp; Commerce du clic (`ef_id`) comme paramètre de chaîne de requête, utilisé comme jeton. Choisissez cette option si vous souhaitez signaler les transactions hors ligne, que Search, Social et Commerce échangent des données avec Adobe Analytics ou que vous souhaitez effectuer le suivi de toutes les conversions qui se produisent dans [!DNL Apple Safari] navigateurs.

**Remarques :**

* Si vous passez de [!UICONTROL Standard] to [!UICONTROL Token], ou vice versa, vous devez régénérer les URL de suivi pour le compte.
* Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.
