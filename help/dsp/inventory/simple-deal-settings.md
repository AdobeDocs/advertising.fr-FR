---
title: Paramètres des offres [!UICONTROL Simple Ad Serving]
description: Découvrez les paramètres disponibles pour les offres [!UICONTROL Simple Ad Serving].
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: dad30b0bd24c0286c1de6520471cb90707046ff3
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Paramètres des offres [!UICONTROL Simple Ad Serving]

## Nouvelles offres [!UICONTROL Simple Ad Serving]

### [!UICONTROL Select ad source]

| Paramètre | Description |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Type de média pour cette offre : *[!UICONTROL Video],* *[!UICONTROL Display],* ou *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Nom de l’éditeur qui vend ce stock. Recherchez un éditeur en saisissant au moins les deux premiers caractères du nom. Pour ajouter un éditeur qui n’est pas répertorié, contactez l’équipe chargée de votre compte Adobe. |
| **[!UICONTROL Advertiser]** | Un seul annonceur dans le compte qui peut accéder à cette offre. Sélectionnez également la campagne et (éventuellement) le package dans lequel l’offre est disponible. |
| **[!UICONTROL Media Quality Assessment?]** | (Certains utilisateurs) Permet à la publicité de s’exécuter sur un autre DSP pour une vérification tierce. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | La seule option est *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Nouvelles offres uniquement) S’il faut :<ul><li>*[!UICONTROL Create New]:* pour créer une annonce publicitaire pour cette offre.</li><li>*[!UICONTROL Select Ads]:* pour utiliser une annonce publicitaire existante pour cette offre.</li></ul> |
| **[!UICONTROL Ad Type]** | Type d’annonce publicitaire pour cette offre. Si vous allez créer des annonces pour l&#39;offre, incluez la taille ou la durée de l&#39;annonce, comme demandé. Les options disponibles varient selon le type de média. |

{style="table-layout:auto"}

### [!UICONTROL Select ad(s)]

(Lorsque vous utilisez des annonces existantes) Les annonces à inclure dans l’offre. Cochez la case en regard de chaque publicité à inclure.

### [!UICONTROL Select & upload [Media Type]]

(Nouvelles annonces uniquement) Screens pour créer une [annonce tierce](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed details]

| Paramètre | Description |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | Coût par 1 000 impressions (CPM), tel qu’il figure dans la carte tarifaire de votre contrat. Contactez l’équipe chargée de votre compte Adobe pour connaître cette valeur. <br><br>Indiquez également la devise de l’opération. Tous les utilisateurs peuvent sélectionner USD ou, si le fournisseur de services partagés prend en charge d’autres devises, la devise du compte DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Facultatif) Frais de tiers statiques à suivre en tant que coût non facturable, et devise de l’opération.<br><br>Tous les utilisateurs peuvent sélectionner USD ou, si le SSP prend en charge d’autres devises, la devise du compte DSP. **REMARQUE :** les frais facturables sont reflétés dans la mesure [!UICONTROL Net CPM]. |
| **[!UICONTROL Third Party Fee Description]** | (Facultatif) Description des frais facturés aux tiers. |
| **[!UICONTROL Flight Dates]** | Dates de début et de fin du trafic utilisant cette offre. Les dates des vols doivent être incluses dans les dates des vols de la campagne. Les balises d’annonces ne renvoient une réponse que pendant le vol spécifié.<br><br> Il est recommandé de créer une campagne de diffusion d’annonces simple distincte d’une durée d’un an et d’y créer des pixels de suivi. |
| **[!UICONTROL Impressions]** | (Facultatif) Estimation du nombre d’impressions que vous prévoyez d’exécuter à l’aide de cette offre. Cette valeur est utilisée uniquement à des fins de suivi et pour indiquer le moment où les objectifs de diffusion sont atteints. L’éditeur contrôle la diffusion réelle des annonces. La bonne pratique consiste à saisir un grand nombre d’impressions pour que la balise reste active dans DSP afin qu’elle puisse être renouvelée ou étendue si nécessaire. |
| **[!UICONTROL Deal Name]** | Nom de l’offre. Saisissez un nom ou sélectionnez *[!UICONTROL Auto Generate Deal Name]* pour laisser DSP générer un nom en fonction des détails de l’opération.<br><br>Exemple de nom généré automatiquement : `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Lecture seule) Publicités qui font partie de l’offre. Pour modifier une publicité, cliquez sur son nom. Pour supprimer une annonce de l’offre, cliquez sur **[!UICONTROL X]** en regard du nom de l’annonce. |

{style="table-layout:auto"}

<!-- 
## Existing [!UICONTROL Simple Ad Serving] deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [À propos des [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Créer un [!UICONTROL Simple Ad Serving] contrat](simple-deal-create.md)
>* [Modifier les paramètres de l’offre [!UICONTROL Simple Ad Serving]](simple-deal-edit.md)
>* [Afficher un rapport détaillé pour une affaire](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
