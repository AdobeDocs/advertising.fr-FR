---
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# Champ Modèle de tracking des entités [!DNL LY Ads]

<!-- Search CRUD and bulk edit of LY Ads entity settings -->

**[!UICONTROL Tracking Template]:** (facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de la destination et incorpore également l’URL finale/de la page de destination dans un paramètre. Utilisez le paramètre `!{lpurl}` pour indiquer l’URL de la page de destination. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement un préfixe à son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

>[!NOTE]
>
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres des mots-clés incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Vous pouvez mettre à jour vos modèles de tracking à n’importe quel niveau sans avoir à soumettre à nouveau vos publicités pour approbation.
