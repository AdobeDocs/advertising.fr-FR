---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---
# Champ Chargement automatique dans les paramètres du compte et de la campagne

**[!UICONTROL Auto Upload]:** (Pour les campagnes synchronisées avec [!UICONTROL EF Redirect] uniquement) Télécharge automatiquement les éléments suivants sur le réseau publicitaire la prochaine fois que Search, Social et Commerce se synchronise avec celui-ci : (a) paramètres de suivi de recherche, Social et Commerce pour les modèles de suivi et les mêmes paramètres ajoutés aux URL finales ou (b) nouvelles URL de destination incorporées avec le code de suivi Search, Social et Commerce. Pour les annonceurs qui disposent d’un [Intégration Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) et une configuration AMO ID (s_kwcid) côté serveur, le chargement inclut également [Paramètres AMO ID](/help/integrations/analytics/ids.md#amo-id) pour votre [!DNL Google Ads] et [!DNL Microsoft Advertising] comptes. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur. Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.

**Remarque :** Les URL de suivi ne sont mises à jour quotidiennement que pour les entités désynchronisées (c’est-à-dire, les nouvelles entités ajoutées et les entités existantes dont les propriétés ont été modifiées). Par conséquent, si vous modifiez ce paramètre de désactivé à activé pour un annonceur/compte/campagne existant, les URL de suivi ne sont pas mises à jour pour les entités existantes déjà synchronisées. Pour ajouter le suivi aux URL des entités existantes et synchronisées, contactez votre équipe de compte d’Adobe et demandez un processus de synchronisation manuel unique. Le processus de chargement automatique prendra en charge les modifications futures.
