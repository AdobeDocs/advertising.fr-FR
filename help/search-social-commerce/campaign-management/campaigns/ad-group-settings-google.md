---
title: '[!DNL Google Ads] paramètres du groupe publicitaire'
description: Référencez les paramètres pour les groupes publicitaires  [!DNL Google Ads] .
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '420'
ht-degree: 0%

---

# [!DNL Google Ads] paramètres du groupe publicitaire

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** nom d’un groupe publicitaire unique dans la campagne. La longueur maximale est de 255 caractères sur deux octets.

**[!UICONTROL Status]:** État d’affichage du groupe publicitaire : *Actif* ou *En pause*. La valeur par défaut des nouveaux groupes publicitaires est *Active*.

**[!UICONTROL Ad Group Type]:** (campagnes de recherche dynamique étendues uniquement) Type de groupe publicitaire :

* *[!UICONTROL Search Standard]* (valeur par défaut) : pour les publicités standard.

* *[!UICONTROL Search Dynamic]:* pour les annonces de recherche dynamique.

**[!UICONTROL Ad Rotation Mode]:** À quelle fréquence [!DNL Google Ads] diffuse vos publicités actives les unes par rapport aux autres dans le groupe publicitaire :

* *[!UICONTROL Optimize]:* Google Ads favorise les publicités qu’il s’attend à réaliser mieux que les autres publicités du groupe publicitaire. Ces publicités entrent plus souvent dans la vente aux enchères et au fil du temps, une seule publicité est favorisée. Cela peut être incompatible avec vos objectifs d’entreprise et d’optimisation.

* *[!UICONTROL Rotate forever]:*   Chacune de vos publicités entre plus régulièrement dans la vente aux enchères, ce qui permet à Search, Social et Commerce de noter vos publicités non seulement au taux de clics publicitaires, mais également sur les conversions.

* *[!UICONTROL Use campaign setting]* (valeur par défaut pour les nouveaux groupes d’annonces) : permet d’utiliser le paramètre de rotation d’annonces existant au niveau de la campagne. **Remarque :** Le paramètre de niveau campagne n’est pas visible dans Search, Social et Commerce.

Si la campagne utilise une stratégie d’offre d’enchères dynamiques (telle que [!UICONTROL Target CPA], [!UICONTROL Target ROAS] ou [!UICONTROL Enhanced CPC]), [!DNL Google Ads] définit automatiquement l’option sur &quot;[!UICONTROL Optimize]&quot;.

**[!UICONTROL Custom Bid Level]:** (Campagnes ciblant uniquement le réseau d’affichage) Comment enchérir : par *[!UICONTROL Ad Group]* (valeur par défaut), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Intérêts et remarketing dans les publicités Google), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (site web), *[!UICONTROL Unknown]* ou *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Lorsque vous enchérissez par mot-clé, créez des modèles de suivi au niveau du mot-clé. De même, lorsque vous enchérissez par emplacement, créez des modèles de suivi au niveau de l’emplacement. Pour toutes les autres dimensions, créez des modèles de suivi au niveau de l’annonce.
>* Lorsque vous enchérissez par âge, par sexe, par intérêt et par liste, ou verticalement pour des campagnes dans des portefeuilles, la fonctionnalité d’optimisation n’optimise pas les offres pour la dimension. En outre, toutes les attributions sont appliquées au groupe publicitaire.
>* Les publicités sur le réseau de recherche utilisent toujours des offres sur les mots-clés.

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (Campagnes avec [!UICONTROL Target CPA] enchères ; facultatif) coût cible par acquisition (CPA) pour le groupe publicitaire. Cette valeur remplace la cible au niveau de la campagne.

**[!UICONTROL Target ROAS]:** (Campagnes avec [!UICONTROL Target ROAS] enchères ; facultatif) Le retour sur dépenses publicitaires cible pour le groupe publicitaire, en pourcentage. Cette valeur remplace la cible au niveau de la campagne.

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (Campagnes sur le réseau de recherche uniquement et campagnes existantes [!DNL Gmail] en lecture seule sur le réseau d’affichage) Indique si :

* *[!UICONTROL Target and Bid]:* pour afficher uniquement les publicités aux utilisateurs associés aux audiences cibles qui répondent également à d’autres cibles pour le groupe publicitaire.

* *[!UICONTROL Bid Only]:* pour afficher les publicités même aux personnes qui ne sont pas associées aux audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire. Vous pouvez toutefois augmenter les chances d&#39;affichage des publicités à des audiences spécifiques en définissant des offres plus élevées pour ces audiences.

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
>* [Gérer les groupes d’annonces](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
