---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---
# Champ Modèle de suivi pour les entités Google Ads

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** (Facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi, et incorpore également l’URL de la page d’entrée/finale dans une [!DNL ValueTrack] . Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Pour le suivi de conversion Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour les paramètres pris en charge pour incorporer l’URL finale, voir [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] formats](https://support.google.com/google-ads/answer/6305348). (Accédez aux paramètres &quot;Modèle de suivi uniquement&quot; dans la section &quot;Disponible&quot; [!DNL ValueTrack] Paramètres.&quot;)

* Vous pouvez éventuellement inclure des paramètres d’URL et des paramètres personnalisés définis pour la campagne, séparés par des esperluettes (&amp;), tels que {lpurl}?matchtype={matchtype}&amp;device={device}.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

>[!NOTE]
>
>* Évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit travailler avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres du mot-clé incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Si vous mettez à jour un modèle de suivi au niveau de la publicité, du lien de site ou du mot-clé, les publicités pertinentes sont soumises à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans soumettre à nouveau vos publicités pour approbation.
