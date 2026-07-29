---
title: '[!DNL Google Ads] paramètres de groupe publicitaire'
description: Référencez les paramètres des groupes  [!DNL Google Ads] ’annonces.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/pDFheVIM62XNCh2-7jbCscIqOrcTep7qnNg5S1tHYF8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 75e264e213f60ae45c4f51f0a21352f690d6d699
workflow-type: tm+mt
source-wordcount: 549
ht-degree: 0%

---

# [!DNL Google Ads] paramètres de groupe publicitaire

## \[Haut de la page]

**[!UICONTROL Ad Group Name]:** nom de groupe publicitaire unique dans la campagne.

**[!UICONTROL Status]:** statut d’affichage de la campagne : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Active*.

## onglet [!UICONTROL Basic Settings]

*Nouvelles campagnes uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte de réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne.

## onglet [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Group Type]:** (Campagnes publicitaires de recherche dynamique étendue uniquement) Type de groupe publicitaire :

* *[!UICONTROL Search Standard]* (valeur par défaut) : pour les publicités standard.

* *[!UICONTROL Search Dynamic]:* Pour les annonces de recherches dynamiques.

**[!UICONTROL Ad Rotation Mode]:** fréquence à laquelle [!DNL Google Ads] diffuse vos publicités actives les unes par rapport aux autres au sein du groupe publicitaire :

* *[!UICONTROL Optimize]:* [!DNL Google Ads] privilégie les annonces qu’il s’attend à voir performer plus que les autres annonces du groupe publicitaire. Ces publicités entrent plus souvent dans les enchères publicitaires et, au fil du temps, une seule publicité est privilégiée. Cela peut être incompatible avec vos objectifs commerciaux et d’optimisation.

* *[!UICONTROL Rotate forever]:* Chacune de vos publicités entre dans la vente aux enchères un nombre plus régulier de fois, ce qui permet à Search, Social et Commerce de noter vos publicités non seulement sur le taux de clic publicitaire, mais également sur les conversions.

* *[!UICONTROL Use campaign setting]* (valeur par défaut pour les nouveaux groupes d’annonces) : utilise le paramètre de rotation des annonces au niveau de la campagne. **Remarque :** le paramètre au niveau de la campagne n’est pas visible dans Search, Social et Commerce.

Si la campagne utilise une stratégie d’enchères intelligentes (telle que [!UICONTROL Target CPA], [!UICONTROL Target ROAS], [!DNL Google Ads] définit automatiquement l’option sur « [!UICONTROL Optimize] ».

**[!UICONTROL Custom Bid Level]:** (Campagnes qui ciblent uniquement le réseau d’affichage) Comment enchérir : par *[!UICONTROL Ad Group]* (par défaut), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Centres d’intérêt et remarketing dans Google Ads), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (site web), *[!UICONTROL Unknown]* ou *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Lorsque vous enchérissez par mot-clé, créez des modèles de suivi au niveau du mot-clé. De même, lorsque vous enchérissez par emplacement, créez des modèles de suivi au niveau de l’emplacement. Pour toutes les autres dimensions, créez des modèles de suivi au niveau des annonces.
>* Lorsque vous enchérissez par âge, sexe, centre d’intérêt et liste ou vertical pour les campagnes des portefeuilles, la fonctionnalité d’optimisation n’optimise pas les enchères pour la dimension. En outre, toute attribution est appliquée au groupe publicitaire .
>* Les publicités sur le réseau de recherche utilisent toujours des offres par mot-clé.

**[!UICONTROL AI Max Search Term Matching]:** (campagnes qui ciblent le réseau de recherche et pour lesquelles la fonctionnalité [AI Max](https://support.google.com/google-ads/answer/15910366) et la fonctionnalité de correspondance des termes de recherche au niveau de la campagne sont activées ; lecture seule) Si la correspondance des termes de recherche au niveau du groupe publicitaire est activée : *[!UICONTROL Disabled]* ou *[!UICONTROL Enabled]*.

## onglet [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (campagnes avec enchères [!UICONTROL Target CPA] ; facultatif) Coût par acquisition cible (CPA) pour le groupe publicitaire. Cette valeur remplace la cible au niveau de la campagne.

**[!UICONTROL Target ROAS]:** (campagnes avec enchères [!UICONTROL Target ROAS] ; facultatif) Retour sur dépenses publicitaires cible pour le groupe publicitaire, sous la forme d’un pourcentage. Cette valeur remplace la cible au niveau de la campagne.

## onglet [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (campagnes uniquement sur le réseau de recherche et campagnes [!DNL Gmail] existantes en lecture seule sur le réseau d’affichage) Si :

* *[!UICONTROL Target and Bid]:* pour afficher les annonces uniquement aux utilisateurs et utilisatrices associés aux audiences cibles qui répondent également à d’autres cibles du groupe publicitaire.

* *[!UICONTROL Bid Only]:* pour afficher des annonces même à des personnes qui ne sont pas associées à des audiences cibles, à condition qu’elles répondent aux cibles d’autres groupes d’annonces. Vous pouvez toutefois augmenter les chances que les publicités soient présentées à des audiences spécifiques en définissant des enchères plus élevées pour ces audiences.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## onglet [!UICONTROL AI Max]

*Campagnes ciblant uniquement le réseau de recherche*

## onglet [!UICONTROL AI Max]

**[!UICONTROL AI Search Term Matching]:** (Campagnes avec [!DNL AI Max] activé uniquement) Utilisation ou non de la correspondance de termes de recherche sans mots-clés pilotée par l’IA pour améliorer la portée et l’optimisation.<!--SUPPOSEDLY, BUT THIS IS OFF FOR ME:  It's enabled by default for campaigns with [!DNL AI Max], but you can disable it at the ad group level. -->

**[!UICONTROL Locations of Interest]:** (Campagnes avec [!DNL AI Max] activé uniquement) Emplacements spécifiques de l’intention géographique à cibler (sans exclure) ; les utilisateurs doivent également répondre au ciblage géographique de la campagne. Par défaut, tous les utilisateurs et utilisatrices de , qui se trouvent régulièrement dans ou qui s’intéressent à toutes les zones géographiques sont ciblés. Pour réduire les cibles, sélectionnez chaque emplacement à cibler.

## onglet [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## onglet [!UICONTROL Additional Ad Group Information]

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

### [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [Gérer les groupes publicitaires](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)
