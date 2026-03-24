---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---
# Champ Chargement automatique dans les paramètres du compte et de la campagne

**[!UICONTROL Auto Upload]:** (pour les campagnes synchronisées avec [!UICONTROL EF Redirect] uniquement) Charge automatiquement les éléments suivants sur le réseau publicitaire la prochaine fois que Search, Social et Commerce s’y synchronise : (a) Paramètres de tracking Search, Social et Commerce pour les modèles de tracking et les mêmes paramètres ajoutés aux URL finales ou (b) Nouvelles URL de destination incorporées avec le code de tracking Search, Social et Commerce. Pour les annonceurs et annonceuses disposant d’une intégration [Adobe Advertising-Adobe Analytics](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) et d’une configuration d’AMO ID côté serveur (s_kwcid), le chargement inclut également les paramètres [AMO ID](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id) pour vos comptes [!DNL Google Ads] et [!DNL Microsoft Advertising]. Le paramètre par défaut au niveau du compte est hérité des paramètres de suivi de l’annonceur. Vous pouvez remplacer le paramètre au niveau du compte au niveau de la campagne.

**Remarque :** les URL de tracking ne sont mises à jour quotidiennement que pour les entités non synchronisées (c’est-à-dire les nouvelles entités ajoutées et les entités existantes dont les propriétés ont été modifiées). Par conséquent, si vous modifiez ce paramètre de désactivé à activé pour un annonceur/compte/campagne existant, les URL de suivi ne sont pas mises à jour pour les entités existantes qui sont déjà synchronisées. Pour ajouter le tracking aux URL des entités existantes non synchronisées, contactez l’équipe de votre compte Adobe et demandez un processus de synchronisation manuel unique. Le processus de chargement automatique gérera les modifications futures.
