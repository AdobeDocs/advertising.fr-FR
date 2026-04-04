---
source-git-commit: 287e8bd0c2a3c3aedbf5f1f9551823b0c4586a57
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---
# Fragments de code

## Champ Modèle de tracking des entités [!DNL Google Ads] {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

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

## Champ Modèle de tracking des entités [!DNL Microsoft Advertising] {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** (facultatif) Le modèle de suivi ou l’URL de suivi, qui spécifie toutes les redirections de domaine et tous les paramètres de suivi hors de la destination et incorpore également l’URL finale/de la page de destination dans un paramètre. Exemple : `{lpurl}?source={network}&id=5` ou `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` pour inclure une redirection.

Pour le suivi des conversions Adobe Advertising, qui est appliqué lorsque les paramètres de la campagne incluent « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Search, Social et Commerce ajoute automatiquement un préfixe à son propre code de redirection et de suivi lorsque vous enregistrez l’enregistrement.

* Pour connaître les paramètres pris en charge afin d’incorporer l’URL finale, consultez la [[!DNL Microsoft Advertising] documentation sur les paramètres permettant d’indiquer l’URL finale](https://help.ads.microsoft.com/#apex/3/en/56799).

* Vous pouvez éventuellement inclure des paramètres d’URL et tout paramètre personnalisé défini pour la campagne, séparé par des esperluettes (&amp;), tel que {lpurl}?matchtype={matchtype}&amp;device={device}.

* Vous pouvez éventuellement ajouter des redirections et un suivi tiers.

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* Le modèle de suivi au niveau le plus granulaire remplace les valeurs à tous les niveaux supérieurs. Par exemple, si les paramètres du compte et les paramètres des mots-clés incluent tous deux une valeur, la valeur du mot-clé est appliquée.
>* Vous pouvez mettre à jour vos modèles de tracking à n’importe quel niveau sans avoir à soumettre à nouveau vos publicités pour approbation.

## Texte et modèle - Remarque expliquant comment insérer un paramètre dynamique {#inventory-feed-template-insert-dynamic-parameter}

Pour insérer un nom de colonne ou un groupe de modificateurs en tant que paramètre dynamique, cliquez dans le champ de saisie, puis cliquez sur un nom de colonne dans la liste Colonne ou sur un [nom de modificateur](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) dans la liste Modificateurs. Pour insérer la variable [!DNL Param1] ou [!DNL Param2], saisissez la valeur `{param1:default text}` ou `{param2:default text}`, où « texte par défaut » correspond au texte utilisé si la colonne de paramètres du fichier de flux est vide pour une ligne d’annonce.

## Modèle d’annonce publicitaire - Remarque expliquant comment insérer un personnalisateur d’annonce publicitaire {#inventory-feed-template-insert-ad-customizer}

Pour insérer un personnalisateur d’annonce publicitaire, utilisez les formats suivants, où `Default text` est une valeur facultative à insérer lorsque votre fichier de flux n’inclut pas une valeur valide :

* [!DNL Google Ads] : `{CUSTOMIZER.AdCustomizerName:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising] : `{CUSTOMIZER.Attribute name:Default text}`, par exemple `{CUSTOMIZER.Discount:10%}`
