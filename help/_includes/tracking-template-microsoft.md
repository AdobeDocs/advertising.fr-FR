---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Champ Modèle de suivi pour les entités Microsoft Advertising

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Facultatif ; non disponible pour toutes les entités) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine hors entrée et paramètres de suivi et incorpore également l’URL de page d’entrée/finale dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload]&quot;, Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lors de l’enregistrement.

* Pour les paramètres pris en charge pour incorporer l’URL finale, consultez la [[!DNL Microsoft Advertising] documentation sur les paramètres pour indiquer l’URL finale](https://help.ads.microsoft.com/#apex/3/en/56799).

* Vous pouvez éventuellement inclure des paramètres d’URL et des paramètres personnalisés définis pour la campagne, séparés par des esperluettes (&amp;), tels que {lpurl}?matchtype={matchtype}&amp;device={device}.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres du mot-clé incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Vous pouvez mettre à jour vos modèles de suivi à n’importe quel niveau sans soumettre à nouveau vos publicités pour approbation.
