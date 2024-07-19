---
title: Paramètres d’ID de transaction manuelle
description: Voir la description des paramètres des ID de transaction saisis manuellement.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Paramètres d’ID de transaction manuelle

| Section | Paramètre | Description | Obligatoire | Modifiable |
|---------|-----------|-------------|----------|----------|
| [Détails de l’opération] | [!UICONTROL Deal name] | Nom pour identifier votre [!UICONTROL Deal ID] dans Advertising DSP. Saisissez un nom ou sélectionnez **[!UICONTROL Auto-name]** pour DSP générer un nom en fonction des détails de l’opération.<br><br>Exemple de nom généré automatiquement : `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Oui | Oui |
| | [!UICONTROL External deal ID] | Identifiant utilisé par votre éditeur et le fournisseur de services de messagerie pour identifier cette transaction. | Oui | Non |
| | [!UICONTROL Publisher] | Nom de l’éditeur qui vend cet inventaire. | Oui | Non |
| | [!UICONTROL SSP] | Plateforme côté offre (SSP) sur laquelle s’exécute cet accord. | Oui | Non |
| | [!UICONTROL Media type] | Le type de média acheté lors de cette transaction : *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]*, *[!UICONTROL Audio]* ou *[!UICONTROL Publisher Managed]*. Les options varient selon SSP.<br><br> Si l’opération autorise plusieurs types de média, sélectionnez le type de média pour l’emplacement par défaut lors de la création de l’opération. Plus tard, vous pouvez modifier la valeur ou vous pouvez simplement [joindre un nouvel emplacement avec le type de média supplémentaire](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Oui | Non |
| | [!UICONTROL Deal type] | Engagement et structure de prix de l’opération :<br><ul><li>*[!UICONTROL Non guaranteed (floor)]* : vous et l’éditeur n’avez pas engagé de nombre fixe de diffusions d’impression. L&#39;accord spécifie le prix minimum pour l&#39;inventaire, bien que le CPM puisse fluctuer et augmenter en fonction des conditions du marché.</li><li>*[!UICONTROL Non guaranteed (fixed)]* : vous et l’éditeur n’avez pas engagé de nombre fixe de diffusions d’impression. La tarification est à un taux fixe négocié.</li><li>*[!UICONTROL Guaranteed (fixed)]* : vous et l’éditeur avez convenu d’un nombre prédéfini d’impressions, de ciblage, de dates de vol et de prix fixe.<br><br><b>Remarque :</b> Les offres garanties exigent des dates de vol et un nombre spécifié d’impressions dans la section [!UICONTROL Tracking]. Vous devez également créer un emplacement garanti par programme par défaut pour l’opération, et vous pouvez éventuellement utiliser l’opération pour d’autres emplacements.</li></ul> | Oui | Non |
| | [!UICONTROL CPM] | Le coût négocié par 1 000 impressions (CPM). | Oui | Oui |
| | [Devise] | Devise de l’accord.<br><br> Tous les SSP acceptent des offres en dollars américains. Lorsque le SSP accepte la devise de votre compte DSP, cette devise est également disponible. | Oui | Non |
| | [!UICONTROL Billing method] | Tous les identifiants de transaction sont [!DNL Adobe] financés et facturés. DSP paie tous les fournisseurs de médias disponibles en fonction de l’utilisation, gère les incohérences avec les fournisseurs et envoie une facture consolidée au compte. Cette option entraîne des frais supplémentaires, comme indiqué dans la carte de taux du compte. | Oui | Non |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | Adresse électronique du compte utilisateur qui peut accéder à la transaction. | Non | Oui |
| | [!UICONTROL Advertisers that can access this deal] | Les publicitaires spécifiques du compte qui peuvent accéder à cette transaction.<br><br><b>Remarque :</b> Vous pouvez partager l’opération avec des annonceurs dans des comptes supplémentaires à partir de la vue [!UICONTROL Deals]. Sur la ligne de la transaction, cliquez sur **[!UICONTROL #]**, cliquez sur **[!UICONTROL share]**, puis partagez la transaction avec une adresse électronique. | Oui | Oui |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Les dates de début et de fin du trafic utilisant cette transaction. Ces dates sont destinées au suivi uniquement et n’ont aucune incidence sur la diffusion des publicités.<br><br><b>Conseil : </b> Dans la vue [!UICONTROL Inventory] > [!UICONTROL Deals], la colonne [!UICONTROL Pacing & Budget] indique comment l’opération se déroule selon la date de vol spécifiée et l’objectif d’impression. Si la diffusion est en sous-ou en trop-rythme, contactez votre éditeur pour ajuster le volume qu’elle envoie via l’offre. | Offres garanties : Oui<br>Offres non garanties : Non | Oui |
| | [!UICONTROL Impressions] | (Facultatif pour les offres non garanties) Nombre estimé d’impressions que vous prévoyez d’exécuter à l’aide de cette opération. Cette valeur est destinée au suivi uniquement ; l’éditeur contrôle la diffusion de la publicité. | Offres garanties : Oui<br>Offres non garanties : Non | Oui |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Créer manuellement des détails sur l’identifiant de transaction](deal-id-create.md)
>* [Partenaires SSP](ssp-partners.md)
>* [À propos de l’inventaire privé](private-inventory-about.md)
