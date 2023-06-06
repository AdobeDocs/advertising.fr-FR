---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---
# Ajouter le champ Paramètres dans les paramètres du compte et de la campagne

**[!UICONTROL Append Parameters]:** (Facultatif) Tous paramètres de suivi supplémentaires à ajouter aux URL de base.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Les paramètres d’ajout au niveau de l’annonceur sont inclus par défaut au niveau du compte et au niveau de la campagne, mais vous pouvez remplacer l’un ou l’autre.

Vous pouvez utiliser n’importe quelle chaîne de texte statique, y compris les paramètres de suivi tiers, ou n’importe quelle chaîne de texte statique. [paramètres de suivi pris en charge](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), qui insère une valeur de données appropriée dans l’URL de base.

Séparez plusieurs paramètres par des virgules ou des esperluettes (&amp;). Les crochets imbriqués ne sont pas pris en charge.

**Remarques :**

* Les modifications apportées aux paramètres d’ajout ne sont pas contrôlées par la variable [!UICONTROL Auto Upload] . Si vous modifiez les paramètres d’ajout pour les URL de base existantes, les nouvelles URL ne sont pas générées automatiquement. Ajoutez les nouveaux paramètres en téléchargeant un fichier de feuille d’envoi groupé pour le compte ou la campagne, en mettant à jour la variable [!UICONTROL Base URL/Final URL] puis transférez et publiez la feuille d’envoi groupé.

* (Réseaux publicitaires avec suivi parallèle) Évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit travailler avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.

* (Publicitaires avec une intégration Advertising-Adobe Analytics Adobe) Pour inclure une `s_kwcid` paramètre permettant d’envoyer des données de recherche, de Social et de Commerce à [!DNL Analytics], reportez-vous à la section [formats spécifiques au réseau publicitaire](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md). Il n’est pas nécessaire d’ajouter manuellement le paramètre pour [!DNL Google Ads] et [!DNL Microsoft Advertising] comptes avec une implémentation s\_kwcid côté serveur.
