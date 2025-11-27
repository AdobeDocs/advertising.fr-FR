---
title: Paramètres des plans de portée télévisuelle connectée
description: Voir les descriptions des paramètres des plans de portée TV connectée.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Paramètres des plans de portée télévisuelle connectée

<!-- Move out of table for consistency at some point. -->

| Paramètre | Description | Obligatoire ? |
| --- | --- | --- |
| [!UICONTROL Name] | Nom permettant d’identifier votre plan. | Oui |
| [!UICONTROL Advertiser] | Annonceur spécifique dans le compte pour lequel le plan est en cours de création. | Oui |
| [!UICONTROL Media Type] | Type de média à inclure dans le plan.<br><br>Actuellement, seul [!UICONTROL Connected TV] est disponible. | Oui |
| [!UICONTROL Date Range] | Dates de début et de fin du plan.<br><br>La date de début ne peut pas être antérieure à la date actuelle. La période ne peut pas dépasser 90 jours. | Oui |
| [!UICONTROL Goal Type] | Type d’objectif (tel que [!UICONTROL Budget]) à prendre en compte pour le plan.<br><br>Actuellement, seul [!UICONTROL Budget] est disponible. | Oui |
| [!UICONTROL Goal Value] | Valeur d’objectif de la prévision. Pour des résultats de prévision plus précis, utilisez une valeur > 5 000 USD. | Oui |
| [!UICONTROL Max Bid] | Montant maximal à payer pour 1 000 impressions. Si le type de média [!UICONTROL Connected TV] est sélectionné, saisissez une valeur d’au moins 10 USD. | Oui |
| [!UICONTROL Frequency Cap] | Le nombre de fois où un foyer unique doit recevoir des publicités.<br><br>Lorsque vous implémentez un plan et que vous devez créer plusieurs emplacements, appliquez le paramètre de limitation de fréquence au niveau du package et non au niveau de l’emplacement, pour garantir une diffusion correcte. | Oui |
| [!UICONTROL Geo-Targeting] | Emplacements à inclure ou à exclure en tant que cibles. Les options incluent :<ul><li>Pays, villes, états : cliquez sur l’onglet **[!UICONTROL Country/State/City]** ; indiquez si la zone est un *Pays*, *État* ou *Ville* ; développez éventuellement un emplacement pour afficher ses sous-composants, puis cliquez sur **[!UICONTROL Include]** ou **[!UICONTROL Exclude]** en regard de l’emplacement.</li><li>Zones de marché désignées (DMA) aux États-Unis : cliquez sur l’onglet **[!UICONTROL DMA]** ; si vous le souhaitez, développez un État pour afficher ses DMA, puis cliquez sur **[!UICONTROL Include]** ou **[!UICONTROL Exclude]** en regard de l’emplacement.</li><li>Codes postaux : Vous pouvez effectuer l’une des opérations suivantes :<ul><li>Cliquez sur l’onglet **[!UICONTROL Search postal code]**, sélectionnez le pays, saisissez le nom complet de la ville ou les lettres contenues dans le nom de la ville, puis appuyez sur la touche **[Entrée]**, cliquez sur le nom correct de la ville pour afficher tous les codes postaux de la ville, cliquez sur le code postal correct, puis cliquez sur **[!UICONTROL Include]** ou **[!UICONTROL Exclude]**.</li><li>Cliquez sur l’onglet **[!UICONTROL Paste postal code]** , sélectionnez le pays, saisissez ou collez des valeurs séparées par des virgules, puis cliquez sur **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**.</li></ul></li></ul> | Oui |
| [!UICONTROL Inventory Targeting] | Sources de stock à inclure ou exclure en tant que cibles. Sélectionnez au moins un flux ou une source. | Oui |
| [!UICONTROL Site/App Targeting] | Sites web et applications à inclure ou à exclure en tant que cibles. Saisissez une URL par ligne, puis cliquez sur **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**. | Non |
| [!UICONTROL Audience Targeting] | Audiences à inclure ou à exclure en tant que cibles. | Non |
| [!UICONTROL Ad duration] | Durée des publicités à prendre en compte pour le plan. | Non |

>[!MORELIKETHIS]
>
>* [À propos de l’outil Planificateur DSP](planner-about.md)
>* [Créer un plan de portée TV connectée](planner-create.md)
>* [Dupliquer un plan de portée TV connectée](planner-duplicate.md)
>* [Modification d’un plan de portée TV connectée](planner-edit.md)
>* [Exporter un plan de portée TV connectée](planner-export.md)
>* [Régénérer la prévision pour un plan de portée de télévision connectée](planner-forecast.md)
>* [Archiver un plan de portée TV connectée](planner-archive.md)
