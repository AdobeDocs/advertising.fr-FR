---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---
# Champ Ajouter des paramètres dans les paramètres du compte et de la campagne

**[!UICONTROL Append Parameters]:** (facultatif) Paramètres de tracking supplémentaires à ajouter aux URL de base.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Les paramètres d’ajout au niveau de l’annonceur sont inclus par défaut au niveau du compte et de la campagne, mais vous pouvez les remplacer.

Vous pouvez utiliser n’importe quelle chaîne de texte statique, y compris des paramètres de suivi tiers ou l’un des [paramètres de suivi pris en charge](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), qui insère une valeur de données appropriée dans l’URL de base.

Séparez plusieurs paramètres par des virgules ou des esperluettes (&amp;). Les crochets imbriqués ne sont pas pris en charge.

**Remarques :**

* Les modifications apportées aux paramètres d&#39;ajout ne sont pas contrôlées par l&#39;option [!UICONTROL Auto Upload]. Si vous modifiez les paramètres d’ajout pour les URL de base existantes, les nouvelles URL ne sont pas générées automatiquement. Ajoutez les nouveaux paramètres en téléchargeant un fichier de feuille d’envoi groupé pour le compte ou la campagne, en mettant à jour les champs de [!UICONTROL Base URL/Final URL], puis en chargeant et en validant la feuille d’envoi groupé.

* (Réseaux publicitaires avec suivi parallèle) Évitez d’utiliser des macros qui ne remplacent pas les clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte Adobe doit collaborer avec le service clientèle ou l’équipe d’implémentation pour les ajouter.

* (Annonceurs avec une intégration Adobe Advertising-Adobe Analytics) Pour inclure un paramètre d’ID AMO afin d’envoyer des données Search, Social et Commerce aux [!DNL Analytics], consultez les formats [spécifiques au réseau publicitaire](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items). Il n’est pas nécessaire d’ajouter manuellement le paramètre pour les comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] avec une implémentation AMO ID côté serveur.
