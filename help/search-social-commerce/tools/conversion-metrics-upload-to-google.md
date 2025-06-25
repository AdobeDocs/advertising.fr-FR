---
title: Chargez les mesures de conversion suivies par Search, Social et Commerce vers  [!DNL Google Ads]
description: Découvrez comment télécharger des mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Chargement des mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads]

*Publicitaires avec comptes [!DNL Google Ads] et suivi des conversions Adobe Advertising uniquement*

Search, Social et Commerce peuvent éventuellement charger vers [!DNL Google Ads] toutes les mesures de conversion qu’il suit pour [!DNL Google Ads] campagnes qui utilisent le service de suivi des conversions d’Adobe Advertising. Cette option ne rend pas les conversions disponibles pour l’optimisation hybride. Si vous souhaitez utiliser vos conversions Adobe pour l’optimisation hybride, reportez-vous à la rubrique « [ Activer le chargement des objectifs vers les réseaux publicitaires ](objective-upload-to-networks.md) ».

Les chargements quotidiens incluent la valeur de `gclid` suivie, la valeur de conversion définie à l’aide du modèle d’attribution au niveau de l’annonceur et la date et l’heure. Si le modèle d’attribution est mis à jour, le chargement suivant utilise le nouveau modèle, mais les données antérieures ne sont pas mises à jour pour utiliser le nouveau modèle.

>[!NOTE]
>
>Les chargements n’incluent pas les mesures de conversion téléchargées vers Adobe Advertising à partir de fichiers de flux.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Cochez la case en regard de **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Annonceurs exerçant leur activité dans l’Espace économique européen (EEE) ou au Royaume-Uni (Royaume-Uni) ; facultatif) Si vous avez obtenu le consentement des utilisateurs de l’EEE et du Royaume-Uni pour télécharger leurs données à des fins publicitaires, cochez la case en regard de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Cliquez sur **[!UICONTROL Save]**.

1. (Si vos conversions font l’objet d’un suivi au niveau du compte du responsable) [Ajoutez les informations d’identification pour votre compte du responsable](/help/search-social-commerce/admin/manager-accounts.md) à l’adresse **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Activer le chargement des objectifs sur les réseaux publicitaires](objective-upload-to-networks.md)
