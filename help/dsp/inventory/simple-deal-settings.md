---
title: '[!UICONTROL Simple Ad Serving] Paramètres du contrat'
description: Découvrez les paramètres disponibles pour les [!UICONTROL Simple Ad Serving] offres.
feature: DSP Simple Ad Serving
exl-id: 20e23182-d3d0-457f-a821-0ad4770a138d
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Paramètres de transaction

## Nouvelles [!UICONTROL Simple Ad Serving] transactions

### [!UICONTROL Select Ad Source]

| Paramètre | Description |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Type de média pour cette transaction : *[!UICONTROL Video],* *[!UICONTROL Display],* ou *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Nom de l’éditeur qui vend cet inventaire. Recherchez un éditeur en saisissant au moins les deux premiers caractères du nom. Pour ajouter un éditeur qui n’est pas répertorié, contactez votre équipe de compte d’Adobe. |
| **[!UICONTROL Advertiser]** | Un seul annonceur sur le compte qui peut accéder à cette offre. Sélectionnez également l&#39;opération et (éventuellement) le kit dans lequel l&#39;opération est disponible. |
| **[!UICONTROL Media Quality Assessment?]** | (Certains utilisateurs) Permet à la publicité de s’exécuter sur un autre DSP pour la vérification tierce. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | La seule option est *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Nouvelles offres uniquement) Indique si :<ul><li>*[!UICONTROL Create New]:* Pour créer une publicité pour cette opération.</li><li>*[!UICONTROL Select Ads]:* pour utiliser une publicité existante pour cette opération.</li></ul> |
| **[!UICONTROL Ad Type]** | Type d’annonce pour cette opération. Si vous allez créer des publicités pour l’opération, incluez la taille ou la durée de l’annonce, comme demandé. Les options disponibles varient en fonction du type de média. |

{style="table-layout:auto"}

### [!UICONTROL Select Ad(s)]

(Lorsque vous utilisez des publicités existantes) Publicités à inclure dans l’offre. Cochez la case en regard de chaque publicité à inclure.

### [!UICONTROL Select & Upload [Media Type]]

(Nouvelles publicités uniquement) Screens pour créer une [publicité tierce](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| Paramètre | Description |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | Le coût par 1 000 impressions (CPM), tel qu’il est reflété dans la carte de taux de votre contrat. Contactez votre équipe de compte d’Adobe pour cette valeur. <br><br>Indiquez également la devise de l’opération. Tous les utilisateurs peuvent sélectionner USD ou, si le SSP prend en charge d’autres devises, la devise du compte DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Facultatif) Des frais tiers statiques à suivre en tant que coût non facturable et la devise de l’opération.<br><br>Tous les utilisateurs peuvent sélectionner USD, ou, si le SSP prend en charge d’autres devises, la devise du compte DSP. **REMARQUE :** Les frais facturables sont reflétés dans la mesure [!UICONTROL Net CPM]. |
| **[!UICONTROL Third Party Fee Description]** | (Facultatif) Description des frais tiers. |
| **[!UICONTROL Flight Dates]** | Les dates de début et de fin du trafic utilisant cette transaction. Les dates de vol doivent être incluses dans les dates de vol de l&#39;opération. Les balises de publicité renvoient une réponse uniquement pendant le vol spécifié.<br><br> La bonne pratique pour créer une campagne de diffusion d’annonces simple distincte d’une durée d’un an et y créer des pixels de suivi. |
| **[!UICONTROL Impressions]** | (Facultatif) Nombre estimé d’impressions que vous prévoyez d’exécuter à l’aide de cette opération. Cette valeur est utilisée à des fins de suivi uniquement et pour marquer lorsque les objectifs de diffusion sont atteints ; l’éditeur contrôle la diffusion réelle de la publicité. Il est recommandé de saisir un grand nombre d’impressions pour que la balise reste active dans DSP afin qu’elle puisse être renouvelée ou étendue si nécessaire. |
| **[!UICONTROL Deal Name]** | Nom de l’opération. Saisissez un nom ou sélectionnez *[!UICONTROL Auto Generate Deal Name]* pour DSP générer un nom en fonction des détails de l’opération.<br><br>Exemple de nom généré automatiquement : `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Lecture seule) Publicités faisant partie de l’offre. Pour modifier une publicité, cliquez sur son nom. Pour supprimer une publicité de l’opération, cliquez sur **[!UICONTROL X]** en regard de son nom. |

{style="table-layout:auto"}

<!-- 
## Existing Simple Ad Serving Deals

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
>* [À propos de [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Créer une [!UICONTROL Simple Ad Serving] transaction](simple-deal-create.md)
>* [Modifier [!UICONTROL Simple Ad Serving] paramètres de transaction](simple-deal-edit.md)
>* [Afficher un rapport détaillé pour une transaction](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
