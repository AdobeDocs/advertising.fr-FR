---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---
# Champ Chargement automatique dans les paramètres du compte et de la campagne

**[!UICONTROL Auto Upload]:** (Pour les campagnes synchronisées avec [!UICONTROL EF Redirect] uniquement) Télécharge automatiquement les éléments suivants sur le réseau publicitaire lors de la prochaine synchronisation de Search, Social et Commerce avec celui-ci : (a) Paramètres de suivi de recherche, de Social et de Commerce pour les modèles de suivi et les mêmes paramètres ajoutés aux URL finales ou (b) nouvelles URL de destination incorporées avec le code de suivi de recherche, de Social et de Commerce. Pour les annonceurs qui disposent d’un [Intégration d’Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) et une configuration s_kwcid côté serveur, le téléchargement comprend également des paramètres s_kwcid pour votre [!DNL Google Ads] et [!DNL Microsoft Advertising] comptes. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur. Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.

**Remarque :** Les URL de suivi ne sont mises à jour quotidiennement que pour les entités désynchronisées (c’est-à-dire, les nouvelles entités ajoutées et les entités existantes dont les propriétés ont été modifiées). Par conséquent, si vous modifiez ce paramètre de désactivé à activé pour un annonceur/compte/campagne existant, les URL de suivi ne sont pas mises à jour pour les entités existantes déjà synchronisées. Pour ajouter le suivi aux URL des entités existantes et synchronisées, contactez votre équipe de compte d’Adobe et demandez un processus de synchronisation manuel unique. Le processus de chargement automatique prendra en charge les modifications futures.
