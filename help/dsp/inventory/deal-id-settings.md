---
title: Paramètres manuels des ID d’offres
description: Voir les descriptions des paramètres des ID d’offres saisis manuellement.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: 21ed5558a39ea9b097be8e70ef81bcf8e59c14b4
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Paramètres manuels des ID d’offres

| Section | Paramètre | Description | Obligatoire | Modifiable |
|---------|-----------|-------------|----------|----------|
| [Détails de l’offre] | [!UICONTROL Deal name] | Nom permettant d’identifier votre [!UICONTROL Deal ID] dans Advertising DSP. Saisissez un nom ou sélectionnez **[!UICONTROL Auto-name]** pour permettre à DSP de générer un nom en fonction des détails de l’opération.<br><br>Exemple de nom généré automatiquement : `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Oui | Oui |
| | [!UICONTROL External deal ID] | Identifiant utilisé par votre éditeur et le fournisseur de services partagés pour identifier cette offre. | Oui | Non |
| | [!UICONTROL Publisher] | Nom de l’éditeur qui vend ce stock. | Oui | Non |
| | [!UICONTROL SSP] | Plateforme côté offre (SSP) via laquelle cette transaction est exécutée. | Oui | Non |
| | [!UICONTROL Media type] | Type de média acheté dans le cadre de cette transaction : *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* ou *[!UICONTROL Publisher Managed]*. Les options varient selon le fournisseur de services partagés.<br><br> Si l’opération autorise plusieurs types de médias, sélectionnez le type de média pour l’emplacement par défaut lorsque vous créez l’opération. Par la suite, vous pouvez modifier la valeur ou simplement [joindre un nouvel emplacement avec le type de média supplémentaire](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Oui | Non |
| | [!UICONTROL Deal type] | L&#39;engagement de l&#39;entente et la structure de prix : <br><ul><li>*[!UICONTROL Non guaranteed (floor)]* : vous et l&#39;éditeur n&#39;avez pas validé un nombre fixe de diffusions d&#39;impressions. L&#39;opération précise le prix minimum de l&#39;inventaire, bien que le CPM puisse fluctuer et augmenter en fonction des conditions du marché.</li><li>*[!UICONTROL Non guaranteed (fixed)]* : vous et l&#39;éditeur n&#39;avez pas validé un nombre fixe de diffusions d&#39;impressions. Les prix sont négociés à un taux fixe.</li><li>*[!UICONTROL Guaranteed (fixed)]* : Vous et l&#39;éditeur vous êtes mis d&#39;accord sur un nombre prédéfini d&#39;impressions, de ciblage, de dates de vol et de prix fixe.<br><br><b>Remarque </b> les offres garanties nécessitent des dates de vol et un nombre spécifié d’impressions dans la section [!UICONTROL Tracking]. Vous devez également créer un emplacement programmatique garanti (PG) par défaut pour l’opération, et vous pouvez éventuellement utiliser l’opération pour d’autres emplacements à la place.</li></ul> | Oui | Non |
| | [!UICONTROL CPM] | Coût négocié pour 1 000 impressions (CPM). | Oui | Oui |
| | [Devise] | Devise de l’opération.<br><br>Tous les SSP acceptent les offres en USD. Lorsque le fournisseur de services partagés accepte la devise de votre compte DSP, cette devise est également disponible. | Oui | Non |
| | [!UICONTROL Billing method] | Tous les ID d’offres sont financés et facturés par [!DNL Adobe]. DSP paie tous les fournisseurs de médias disponibles en fonction de l’utilisation, gère les écarts avec les fournisseurs et envoie une facture consolidée au compte. Cette option entraîne des frais supplémentaires, comme indiqué dans la carte tarifaire du compte. | Oui | Non |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | Adresse e-mail du compte utilisateur pouvant accéder à l’offre. | Non | Oui |
| | [!UICONTROL Advertisers that can access this deal] | Publicitaires spécifiques dans le compte qui peuvent accéder à cette offre.<br><br><b>Remarque :</b> vous pouvez partager l’offre avec des annonceurs dans des comptes supplémentaires à partir de la vue [!UICONTROL Deals]. Dans la ligne de l’offre, cliquez sur **[!UICONTROL #]**, sur **[!UICONTROL share]**, puis partagez l’offre avec une adresse e-mail. | Oui | Oui |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Dates de début et de fin du trafic utilisant cette offre. Ces dates sont fournies à des fins de suivi uniquement et n’ont aucune incidence sur la diffusion des publicités.<br><br><b>Conseil :</b> dans la vue [!UICONTROL Inventory] > [!UICONTROL Deals], la colonne [!UICONTROL Pacing & Budget] indique le rythme de l’opération par rapport à la date de vol et à l’objectif d’impression spécifiés. Si la diffusion est insuffisante ou excessive, contactez votre éditeur pour ajuster le volume qu’il envoie dans le cadre de l’offre. | Offres garanties : Oui<br>Offres non garanties : Non | Oui |
| | [!UICONTROL Impressions] | (Facultatif pour les opérations non garanties) Estimation du nombre d’impressions que vous prévoyez d’exécuter à l’aide de cette opération. Cette valeur est utilisée à des fins de suivi uniquement ; l’éditeur contrôle et diffuse la diffusion. | Offres garanties : Oui<br>Offres non garanties : Non | Oui |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Créer manuellement les détails de l’ID d’offre](deal-id-create.md)
>* [Partenaires SSP](ssp-partners.md)
>* [À propos de l&#39;inventaire privé](private-inventory-about.md)
