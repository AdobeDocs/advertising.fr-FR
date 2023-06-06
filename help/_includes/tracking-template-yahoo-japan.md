---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---
# Champ Modèle de suivi pour Yahoo! Entités de publicité au Japon

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]:** (Facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi, et incorpore également l’URL de page d’entrée/finale dans un paramètre. Utilisation du paramètre `!{lpurl}` pour indiquer l&#39;URL de la landing page. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

Pour le suivi de conversion Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

>[!NOTE]
>
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres du mot-clé incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Vous pouvez mettre à jour vos modèles de suivi à n’importe quel niveau sans soumettre à nouveau vos publicités pour approbation.

