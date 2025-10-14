---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# Ajouter le champ Paramètres dans les paramètres du compte et de la campagne

**[!UICONTROL Append Parameters]:** (Facultatif) Tous paramètres de suivi supplémentaires à ajouter aux URL de base.<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. Les paramètres d’ajout au niveau de l’annonceur sont inclus par défaut au niveau du compte et au niveau de la campagne, mais vous pouvez les remplacer.

Vous pouvez utiliser n’importe quelle chaîne de texte statique, y compris les paramètres de suivi tiers, ou n’importe lequel des [&#x200B; paramètres de suivi pris en charge](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md), qui insère une valeur de données appropriée dans l’URL de base.

Séparez plusieurs paramètres par des virgules ou des esperluettes (&amp;). Les crochets imbriqués ne sont pas pris en charge.

**Notes :**

* Les modifications apportées aux paramètres d’ajout ne sont pas contrôlées par l’option [!UICONTROL Auto Upload]. Si vous modifiez les paramètres d’ajout pour les URL de base existantes, les nouvelles URL ne sont pas générées automatiquement. Ajoutez les nouveaux paramètres en téléchargeant un fichier de feuille d’envoi groupé pour le compte ou la campagne, en mettant à jour les champs [!UICONTROL Base URL/Final URL], puis en chargeant et en publiant la feuille d’envoi groupé.

* (Réseaux publicitaires avec suivi parallèle) Évitez d’utiliser des macros, qui ne se substituent pas aux clics provenant de sources qui activent le suivi parallèle. Si l’annonceur doit utiliser des macros, l’équipe du compte d’Adobe doit travailler avec le service clientèle ou l’équipe de mise en oeuvre pour les ajouter.

* (Publicitaires avec intégration Adobe Advertising-Adobe Analytics) Pour inclure un paramètre AMO ID pour envoyer des données Search, Social et Commerce à [!DNL Analytics], reportez-vous aux [formats spécifiques au réseau publicitaire](/help/integrations/analytics/ids.md#amo-id-formats). Il n’est pas nécessaire d’ajouter manuellement le paramètre pour les comptes [!DNL Google Ads] et [!DNL Microsoft Advertising] avec une implémentation AMO ID côté serveur.
