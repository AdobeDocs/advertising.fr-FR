---
title: Paramètres des plans de portée TV connectés
description: Consultez la description des paramètres des plans de portée de la télévision connectée.
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 5d8d981f08eaea2b0a0bc553ab06bd47f1e88ac9
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Paramètres des plans de portée TV connectés

<!-- Move out of table for consistency at some point. -->

| Paramètre | Description | Obligatoire ? |
| --- | --- | --- |
| [!UICONTROL Name] | Nom pour identifier votre plan. | Oui |
| [!UICONTROL Advertiser] | L’annonceur spécifique dans le compte pour lequel le plan est en cours de création. | Oui |
| [!UICONTROL Media Type] | Type de média à inclure dans le plan.<br><br>Actuellement, seul [!UICONTROL Connected TV] est disponible. | Oui |
| [!UICONTROL Date Range] | Les dates de début et de fin du plan.<br><br>La date de début ne peut pas être antérieure à la date actuelle. La période ne peut pas être supérieure à 90 jours. | Oui |
| [!UICONTROL Goal Type] | Type d’objectif (tel que [!UICONTROL Budget]) à prendre en compte pour le plan.<br><br>Actuellement, seul [!UICONTROL Budget] est disponible. | Oui |
| [!UICONTROL Goal Value] | Valeur d’objectif de la prévision. Pour des résultats de prévision plus précis, utilisez une valeur supérieure à 5 000 USD. | Oui |
| [!UICONTROL Max Bid] | Montant maximum à payer pour 1 000 impressions. Si le type de média [!UICONTROL Connected TV] est sélectionné, saisissez une valeur d’au moins 10 USD. | Oui |
| [!UICONTROL Frequency Cap] | Nombre de fois où un foyer unique doit être servi avec des publicités.<br><br>Lorsque vous implémentez un plan et que vous devez créer plusieurs emplacements, appliquez le paramètre de limite de fréquence au niveau du package, et non au niveau de l’emplacement, pour assurer une diffusion correcte. | Oui |
| [!UICONTROL Geo-Targeting] | Emplacements à inclure ou à exclure en tant que cibles. Les options incluent :<ul><li>Pays, villes et états : cliquez sur l’onglet **[!UICONTROL Country/State/City]** ; choisissez si la zone est un *Pays*, un *État* ou une *Ville* ; développez éventuellement un emplacement pour afficher ses sous-composants, puis cliquez sur **[!UICONTROL Include]** ou **[!UICONTROL Exclude]** en regard de l’emplacement.</li><li>Zones de marché désignées (DMA) aux États-Unis : cliquez sur l’onglet **[!UICONTROL DMA]** ; développez éventuellement un état pour afficher ses DMA, puis cliquez sur **[!UICONTROL Include]** ou **[!UICONTROL Exclude]** en regard de l’emplacement.</li><li>Codes postaux : vous pouvez :<ul><li>Cliquez sur l&#39;onglet **[!UICONTROL Search postal code]** , sélectionnez le pays, saisissez le nom complet de la ville ou les lettres contenues dans le nom de la ville, puis appuyez sur la touche **[Entrée]** , cliquez sur le nom de la ville approprié pour afficher tous les codes postaux de la ville, cliquez sur le code postal approprié, puis sur **[!UICONTROL Include]** ou **[!UICONTROL Exclude]**.</li><li>Cliquez sur l’onglet **[!UICONTROL Paste postal code]**, sélectionnez le pays, saisissez ou collez des valeurs séparées par des virgules, puis cliquez sur **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**.</li></ul></li></ul> | Oui |
| [!UICONTROL Inventory Targeting] | Sources d’inventaire à inclure ou à exclure en tant que cibles. Sélectionnez au moins un flux ou une source. | Oui |
| [!UICONTROL Site/App Targeting] | Sites web et applications à inclure ou à exclure comme cibles. Saisissez une URL par ligne, puis cliquez sur **[!UICONTROL Include All]** ou **[!UICONTROL Exclude All]**. | Non |
| [!UICONTROL Audience Targeting] | Audiences à inclure ou à exclure en tant que cibles. | Non |
| [!UICONTROL Ad duration] | Durée des publicités à prendre en compte pour le plan. | Non |

>[!MORELIKETHIS]
>
>* [À propos de l’outil de planification DSP](planner-about.md)
>* [ Créer un plan de portée télévisée connectée ](planner-create.md)
>* [Duplication d’un plan de portée TV connecté](planner-duplicate.md)
>* [Modifier un plan de portée TV connecté](planner-edit.md)
>* [Exporter un plan de portée TV connecté](planner-export.md)
>* [Régénération des prévisions pour un plan de portée télévisée connecté](planner-forecast.md)
>* [ Archivage d’un plan de portée TV connecté](planner-archive.md)
