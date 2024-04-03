---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# Extraits de code

## Champ Modèle de suivi pour les entités Google Ads {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** (Facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi, et incorpore également l’URL de la page d’entrée/finale dans une [!DNL ValueTrack] . Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour les paramètres pris en charge pour incorporer l’URL finale, voir [[!DNL Google Ads] la documentation pour la prise en charge [!DNL ValueTrack] formats](https://support.google.com/google-ads/answer/6305348). (Accédez aux paramètres &quot;Modèle de suivi uniquement&quot; dans la section &quot;Disponible&quot; [!DNL ValueTrack] Paramètres.&quot;)

* Vous pouvez éventuellement inclure des paramètres d’URL et des paramètres personnalisés définis pour la campagne, séparés par des esperluettes (&amp;), tels que {lpurl}?matchtype={matchtype}&amp;device={device}.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

>[!NOTE]
>
>* Évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit travailler avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres du mot-clé incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Si vous mettez à jour un modèle de suivi au niveau de la publicité, du lien de site ou du mot-clé, les publicités pertinentes sont soumises à nouveau pour révision. Vous pouvez mettre à jour vos modèles de suivi au niveau du compte, de la campagne ou du groupe publicitaire sans soumettre à nouveau vos publicités pour approbation.

## Champ Modèle de suivi pour [!DNL Microsoft Advertising] entities {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (Facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine hors entrée et les paramètres de suivi, et incorpore également l’URL de page d’entrée/finale dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Pour le suivi de conversion d’Adobe Advertising, qui est appliqué lorsque les paramètres de campagne incluent &quot;[!UICONTROL EF Redirect]&quot; et &quot;[!UICONTROL Auto Upload],&quot; Search, Social et Commerce préfixe automatiquement son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour les paramètres pris en charge pour incorporer l’URL finale, voir [[!DNL Microsoft Advertising] documentation sur les paramètres pour indiquer l’URL finale](https://help.ads.microsoft.com/#apex/3/en/56799).

* Vous pouvez éventuellement inclure des paramètres d’URL et des paramètres personnalisés définis pour la campagne, séparés par des esperluettes (&amp;), tels que {lpurl}?matchtype={matchtype}&amp;device={device}.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres du mot-clé incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Vous pouvez mettre à jour vos modèles de suivi à n’importe quel niveau sans soumettre à nouveau vos publicités pour approbation.

## Modèle de publicité textuelle - Remarque expliquant comment insérer un paramètre dynamique {#inventory-feed-template-insert-dynamic-parameter}

Pour insérer un nom de colonne ou un groupe de modificateurs en tant que paramètre dynamique, cliquez dans le champ de saisie, puis sur un nom de colonne dans la liste de colonnes ou dans un [modifier le nom](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) dans la liste Modificateurs. Pour insérer la variable [!DNL Param1] ou [!DNL Param2] , saisissez la valeur `{param1:default text}` ou `{param2:default text}`, où &quot;texte par défaut&quot; est du texte utilisé si la colonne de paramètre du fichier de flux est vide pour une ligne de publicité.

## Modèle de publicité textuelle - Remarque expliquant comment insérer un personnalisateur de publicité {#inventory-feed-template-insert-ad-customizer}

Pour insérer un personnalisateur de publicités, utilisez les formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas de valeur valide :

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`
