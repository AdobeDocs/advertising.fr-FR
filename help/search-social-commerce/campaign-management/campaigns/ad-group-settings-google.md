---
title: '[!DNL Google Ads] paramètres de groupe publicitaire'
description: Référencez les paramètres des groupes  [!DNL Google Ads] ’annonces.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: 345c2af5363ca10412f3809700e281af5b06897f
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# [!DNL Google Ads] paramètres de groupe publicitaire

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** nom de groupe publicitaire unique dans la campagne. La longueur maximale est de 255 caractères codés sur deux octets.

**[!UICONTROL Status]:** statut d’affichage du groupe publicitaire : *Actif* ou *En pause*. La valeur par défaut pour les nouveaux groupes publicitaires est *Actif*.

**[!UICONTROL Ad Group Type]:** (Campagnes publicitaires de recherche dynamique étendue uniquement) Type de groupe publicitaire :

* *[!UICONTROL Search Standard]* (valeur par défaut) : pour les publicités standard.

* *[!UICONTROL Search Dynamic]:* Pour les annonces de recherches dynamiques.

**[!UICONTROL Ad Rotation Mode]:** fréquence à laquelle [!DNL Google Ads] diffuse vos publicités actives les unes par rapport aux autres au sein du groupe publicitaire :

* *[!UICONTROL Optimize]:* Google Ads privilégie les publicités dont il s’attend à ce qu’elles soient plus performantes que les autres publicités du groupe. Ces publicités entrent plus souvent dans les enchères publicitaires et, au fil du temps, une seule publicité est privilégiée. Cela peut être incompatible avec vos objectifs commerciaux et d’optimisation.

* *[!UICONTROL Rotate forever]:*   Chacune de vos publicités entre dans la vente aux enchères un nombre plus régulier de fois, ce qui permet à Search, Social et Commerce de noter vos publicités non seulement sur le taux de clic publicitaire, mais également sur les conversions.

* *[!UICONTROL Use campaign setting]* (valeur par défaut pour les nouveaux groupes d’annonces) : utilise le paramètre de rotation des annonces au niveau de la campagne. **Remarque :** le paramètre au niveau de la campagne n’est pas visible dans Search, Social et Commerce.

Si la campagne utilise une stratégie d’enchères intelligentes (telle que [!UICONTROL Target CPA], [!UICONTROL Target ROAS], [!DNL Google Ads] définit automatiquement l’option sur « [!UICONTROL Optimize] ».

**[!UICONTROL Custom Bid Level]:** (Campagnes qui ciblent uniquement le réseau d’affichage) Comment enchérir : par *[!UICONTROL Ad Group]* (par défaut), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Centres d’intérêt et remarketing dans Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (site web), *[!UICONTROL Unknown]* ou *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Lorsque vous enchérissez par mot-clé, créez des modèles de suivi au niveau du mot-clé. De même, lorsque vous enchérissez par emplacement, créez des modèles de suivi au niveau de l’emplacement. Pour toutes les autres dimensions, créez des modèles de suivi au niveau des annonces.
>* Lorsque vous enchérissez par âge, sexe, centre d’intérêt et liste ou vertical pour les campagnes des portefeuilles, la fonctionnalité d’optimisation n’optimise pas les enchères pour la dimension. En outre, toute attribution est appliquée au groupe publicitaire .
>* Les publicités sur le réseau de recherche utilisent toujours des offres par mot-clé.

**[!UICONTROL AI Max Search Term Matching]:** (campagnes qui ciblent le réseau de recherche et pour lesquelles la fonctionnalité [AI Max](https://support.google.com/google-ads/answer/15910366) et la fonctionnalité de correspondance des termes de recherche au niveau de la campagne sont activées ; lecture seule) Si la correspondance des termes de recherche au niveau du groupe publicitaire est activée : *[!UICONTROL Disabled]* ou *[!UICONTROL Enabled]*.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (campagnes avec enchères [!UICONTROL Target CPA] ; facultatif) Coût par acquisition cible (CPA) pour le groupe publicitaire. Cette valeur remplace la cible au niveau de la campagne.

**[!UICONTROL Target ROAS]:** (campagnes avec enchères [!UICONTROL Target ROAS] ; facultatif) Retour sur dépenses publicitaires cible pour le groupe publicitaire, sous la forme d’un pourcentage. Cette valeur remplace la cible au niveau de la campagne.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (campagnes uniquement sur le réseau de recherche et campagnes [!DNL Gmail] existantes en lecture seule sur le réseau d’affichage) Si :

* *[!UICONTROL Target and Bid]:* pour afficher les annonces uniquement aux utilisateurs et utilisatrices associés aux audiences cibles qui répondent également à d’autres cibles du groupe publicitaire.

* *[!UICONTROL Bid Only]:* pour afficher des annonces même à des personnes qui ne sont pas associées à des audiences cibles, à condition qu’elles répondent aux cibles d’autres groupes d’annonces. Vous pouvez toutefois augmenter les chances que les publicités soient présentées à des audiences spécifiques en définissant des enchères plus élevées pour ces audiences.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Gérer les groupes publicitaires](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
