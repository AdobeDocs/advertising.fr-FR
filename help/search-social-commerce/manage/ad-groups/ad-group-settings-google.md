---
title: '[!DNL Google Ads] paramètres du groupe publicitaire'
description: Référencez les paramètres pour [!DNL Google Ads] groupes publicitaires.
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/pDFheVIM62XNCh2-7jbCscIqOrcTep7qnNg5S1tHYF8'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 0%
---
# [!DNL Google Ads] paramètres du groupe publicitaire

## \[Haut de la page]

**[!UICONTROL Ad Group Name]:** Nom de groupe publicitaire unique dans la campagne.

**[!UICONTROL Status]:** Statut d’affichage de la campagne : *Actif* ou *En pause*. La valeur par défaut pour les nouvelles campagnes publicitaires est *Active*.

## Onglet [!UICONTROL Basic Settings]

*Nouveaux groupes publicitaires uniquement*

**[!UICONTROL Network]:** Le réseau publicitaire.

**[!UICONTROL Account]:** Compte réseau publicitaire.

**[!UICONTROL Campaign]:** La campagne.

## Onglet [!UICONTROL Ad Group Details]

**[!UICONTROL Ad Group Type]:** (campagnes publicitaires de recherche dynamique étendues uniquement) Type de groupe publicitaire :

* *[!UICONTROL Search Standard]* (valeur par défaut) : pour les publicités standard.

* *[!UICONTROL Search Dynamic]:* pour les annonces de recherche dynamique.

**[!UICONTROL Ad Rotation Mode]:** Fréquence à laquelle [!DNL Google Ads] diffuse vos publicités actives les unes par rapport aux autres au sein du groupe publicitaire :

* *[!UICONTROL Optimize]:* [!DNL Google Ads] privilégie les annonces qu’il s’attend à voir apparaître plus performantes que les autres annonces du groupe publicitaire. Ces publicités entrent plus souvent dans les enchères publicitaires et, au fil du temps, une seule publicité est privilégiée. Cela peut être incompatible avec vos objectifs commerciaux et d’optimisation.

* *[!UICONTROL Rotate forever]:* Chacune de vos publicités entre dans la vente aux enchères un nombre plus pair de fois, ce qui permet à Search, Social et Commerce de noter vos publicités non seulement sur le taux de clic publicitaire, mais également sur les conversions.

* *[!UICONTROL Use campaign setting]* (valeur par défaut pour les nouveaux groupes d’annonces) : utilise le paramètre de rotation des annonces au niveau de la campagne existant. **Remarque :** le paramètre au niveau de la campagne n’est pas visible dans Search, Social et Commerce.

Si la campagne utilise une stratégie d’enchères intelligentes (telle que [!UICONTROL Target CPA], [!UICONTROL Target ROAS], alors [!DNL Google Ads] définit automatiquement l’option sur « [!UICONTROL Optimize] ».

**[!UICONTROL Custom Bid Level]:** (campagnes qui ciblent uniquement le réseau d’affichage) Comment enchérir : par *[!UICONTROL Ad Group]* (valeur par défaut), *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (intérêts et remarketing dans les publicités Google), *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* (site web), *[!UICONTROL Unknown]* ou *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* Lorsque vous enchérissez par mot-clé, créez des modèles de suivi au niveau du mot-clé. De même, lorsque vous enchérissez par emplacement, créez des modèles de suivi au niveau de l’emplacement. Pour toutes les autres dimensions, créez des modèles de suivi au niveau des annonces.
>* Lorsque vous enchérissez par âge, sexe, centre d’intérêt et liste ou vertical pour les campagnes des portefeuilles, la fonctionnalité d’optimisation n’optimise pas les enchères pour la dimension. En outre, toute attribution est appliquée au groupe publicitaire .
>* Les publicités sur le réseau de recherche utilisent toujours des offres par mot-clé.

**[!UICONTROL AI Max Search Term Matching]:** (campagnes qui ciblent le réseau de recherche et pour lesquelles la fonctionnalité [AI Max](https://support.google.com/google-ads/answer/15910366) et la fonctionnalité de correspondance des termes de recherche au niveau de la campagne sont activées ; lecture seule) Si la correspondance des termes de recherche au niveau du groupe publicitaire est activée : *[!UICONTROL Disabled]* ou *[!UICONTROL Enabled]*.

## Onglet [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** (campagnes avec [!UICONTROL Target CPA] enchères ; facultatif) coût cible par acquisition (CPA) pour le groupe publicitaire. Cette valeur remplace la cible au niveau de la campagne.

**[!UICONTROL Target ROAS]:** (campagnes avec [!UICONTROL Target ROAS] enchères ; facultatif) retour sur dépenses publicitaires cible (ROAS) pour le groupe publicitaire, en pourcentage. Cette valeur remplace la cible au niveau de la campagne.

## Onglet [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** (campagnes sur le réseau de recherche uniquement et campagnes [!DNL Gmail] existantes et en lecture seule sur le réseau d’affichage) Si :

* *[!UICONTROL Target and Bid]:* Pour afficher les publicités uniquement aux utilisateurs associés aux audiences cibles qui répondent également à d’autres cibles pour le groupe publicitaire.

* *[!UICONTROL Bid Only]:* Pour afficher des annonces même à des personnes qui ne sont pas associées à des audiences cibles tant qu’elles répondent à d’autres cibles au niveau du groupe publicitaire. Vous pouvez toutefois augmenter les chances que les publicités soient présentées à des audiences spécifiques en définissant des enchères plus élevées pour ces audiences.

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## Onglet [!UICONTROL AI Max]

*Campagnes ciblant uniquement le réseau de recherche*

## Onglet [!UICONTROL AI Max]

**[!UICONTROL AI Search Term Matching]:** (campagnes avec [!DNL AI Max] activé uniquement) Utilisation ou non de la correspondance de termes de recherche sans mots-clés pilotée par l’IA pour améliorer la portée et l’optimisation.<!--SUPPOSEDLY, BUT THIS IS OFF FOR ME:  It's enabled by default for campaigns with [!DNL AI Max], but you can disable it at the ad group level. -->

**[!UICONTROL Locations of Interest]:** (campagnes avec [!DNL AI Max] activé uniquement) emplacements spécifiques d’intention géographique à cibler (mais pas à exclure). Les utilisateurs doivent également répondre au ciblage géographique de la campagne. Par défaut, tous les utilisateurs et utilisatrices de , qui se trouvent régulièrement dans ou qui s’intéressent à toutes les zones géographiques sont ciblés. Pour réduire les cibles, sélectionnez chaque emplacement à cibler.

**[!UICONTROL URL inclusions]:** (campagnes pour lesquelles [!DNL AI Max] et [!UICONTROL Text customization] sont activés) URL à inclure en tant que pages de destination générées à partir de l’extension d’URL finale. Pour ajouter une URL, saisissez une URL ou un fragment d&#39;URL dans le champ de saisie, puis cliquez sur **+**.

>[!NOTE]
>
>* Lorsque le paramètre [!UICONTROL Final URL expansion] au niveau de la campagne est *activé*, [!DNL Google Ads] utilise les URL spécifiées et d’autres URL sélectionnées par Google comme pages de destination dynamiques pour le groupe publicitaire.
>* Lorsque le paramètre [!UICONTROL Final URL expansion] au niveau de la campagne est *désactivé*, [!DNL Google Ads] utilise uniquement les URL spécifiées comme pages de destination dynamiques pour le groupe publicitaire.
>* (Annonces de recherche réactives avec des ressources épinglées) Lorsque ce paramètre spécifie les inclusions d’URL, [!DNL Google Ads] n’utilise pas de ressources épinglées lorsque l’URL finale dirige vers une page de destination sur laquelle la copie épinglée ne correspond pas à l’intention de l’utilisateur. Pour toujours utiliser les ressources épinglées, ne spécifiez pas d’inclusions d’URL et désactivez le paramètre [!UICONTROL Final URL expansion] au niveau de la campagne.

**[!UICONTROL Brand inclusions]:** (campagnes pour lesquelles [!DNL AI Max] est activé) Listes de marques qui incluent les marques pour lesquelles des requêtes liées à la marque peuvent correspondre. Dans la liste de toutes les listes de marques configurées pour le compte dans l’éditeur [!DNL Google Ads], cochez la case en regard de chaque liste de marques à inclure. Ce paramètre remplace le paramètre au niveau de la campagne.

## Onglet [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## Onglet [!UICONTROL Additional Ad Group Information]

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
>* [Gérer les groupes publicitaires](/help/search-social-commerce/manage/ad-groups/ad-group-manage.md)
