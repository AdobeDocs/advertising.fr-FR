---
source-git-commit: 287e8bd0c2a3c3aedbf5f1f9551823b0c4586a57
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---
# Champ Modèle de tracking des entités [!DNL Google Ads]

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de l’atterrissage et incorpore également l’URL finale/de la page de destination dans un paramètre de [!DNL ValueTrack]. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement un préfixe à son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour connaître les paramètres pris en charge afin d’incorporer l’URL finale, consultez la [[!DNL Google Ads] documentation sur les formats  [!DNL ValueTrack]  pris en charge](https://support.google.com/google-ads/answer/6305348). (Accédez aux paramètres « Modèle de tracking uniquement » dans la section Paramètres de [!DNL ValueTrack] disponibles.)

* Vous pouvez éventuellement inclure des paramètres d’URL et tout paramètre personnalisé défini pour la campagne, séparé par des esperluettes (&amp;), tel que {lpurl}?matchtype={matchtype}&amp;device={device}.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

>[!NOTE]
>
>* Évitez d’utiliser des macros qui ne remplacent pas les clics provenant de sources permettant le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte Adobe doit collaborer avec le service clientèle ou l’équipe d’implémentation pour les ajouter.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres des mots-clés incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Si vous mettez à jour un modèle de suivi au niveau de l’annonce, du lien du site ou du mot-clé, les annonces pertinentes sont envoyées à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans envoyer à nouveau vos publicités pour approbation.
