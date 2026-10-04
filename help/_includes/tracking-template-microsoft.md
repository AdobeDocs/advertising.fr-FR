---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%
---
# Champ Modèle de tracking des entités Microsoft Advertising

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (facultatif ; non disponible pour toutes les entités) Modèle de suivi ou URL de suivi, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de la page d’entrée et incorpore également l’URL finale/de la page de destination dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement un préfixe à son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour connaître les paramètres pris en charge afin d’incorporer l’URL finale, consultez la [[!DNL Microsoft Advertising] documentation sur les paramètres permettant d’indiquer l’URL finale](https://help.ads.microsoft.com/#apex/3/en/56799).

* Vous pouvez éventuellement inclure des paramètres d’URL et tout paramètre personnalisé défini pour la campagne, séparé par des esperluettes (&amp;), tel que {lpurl}?matchtype={matchtype}&amp;device={device}.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres des mots-clés incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Vous pouvez mettre à jour vos modèles de tracking à n’importe quel niveau sans avoir à soumettre à nouveau vos publicités pour approbation.
