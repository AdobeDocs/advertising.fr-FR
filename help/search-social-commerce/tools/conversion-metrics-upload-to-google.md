---
title: Chargement des mesures de conversion dans [!DNL Google Ads]
description: Découvrez comment télécharger des mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---

# Chargement des mesures de conversion dans [!DNL Google Ads]

*Annonceurs avec [!DNL Google Ads] Comptes uniquement*

Search, Social et Commerce peuvent éventuellement effectuer un chargement vers [!DNL Google Ads] toutes les mesures de conversion suivies pour [!DNL Google Ads] campagnes qui utilisent le service de suivi de conversion d’Adobe Advertising Adobe et les mesures de conversion synchronisées à partir d’Adobe Analytics. Cette option ne rend pas les conversions disponibles pour l’optimisation hybride. Si vous souhaitez utiliser vos conversions Adobe pour l’optimisation hybride, reportez-vous à la section &quot;[Activer le téléchargement des objectifs vers les réseaux publicitaires](objective-upload-to-networks.md).&quot;

Les téléchargements quotidiens incluent le suivi `gclid` , la valeur de conversion définie à l’aide du modèle d’attribution au niveau de l’annonceur et l’horodatage. Si le modèle d’attribution est mis à jour, le téléchargement suivant utilise le nouveau modèle, mais les données antérieures ne sont pas mises à jour pour utiliser le nouveau modèle.

>[!NOTE]
>
>Les téléchargements n’incluent pas les mesures de conversion chargées dans Adobe Advertising à partir de fichiers de flux.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Cochez la case en regard de **[!UICONTROL Upload Conversions to Google Ads]**.

1. Cliquez sur **[!UICONTROL Save]**.

1. (Si les conversions sont suivies au niveau du compte de gestionnaire) [Ajout des informations d’identification de votre compte de gestionnaire](/help/search-social-commerce/admin/manager-accounts.md) at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Activer le téléchargement des objectifs vers les réseaux publicitaires](objective-upload-to-networks.md)
