---
title: Chargement des mesures de conversion de recherche, de Social et de suivi Commerce sur  [!DNL Google Ads]
description: Découvrez comment charger des mesures de conversion de suivi de recherche, de Social et de Commerce vers  [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Télécharger les mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads]

*Annonceurs avec [!DNL Google Ads] comptes et suivi de conversion d’Adobe Advertising uniquement*

Search, Social et Commerce peuvent éventuellement charger vers [!DNL Google Ads] toutes les mesures de conversion suivies pour les campagnes [!DNL Google Ads] qui utilisent le service de suivi de conversion d’Adobe Advertising. Cette option ne rend pas les conversions disponibles pour l’optimisation hybride. Si vous souhaitez utiliser vos conversions d’Adobe pour une optimisation hybride, voir &quot;[Activer le téléchargement d’objectifs vers les réseaux publicitaires](objective-upload-to-networks.md)&quot;.

Les téléchargements quotidiens incluent la valeur `gclid` suivie, la valeur de conversion définie à l’aide du modèle d’attribution au niveau de l’annonceur et l’horodatage. Si le modèle d’attribution est mis à jour, le téléchargement suivant utilise le nouveau modèle, mais les données antérieures ne sont pas mises à jour pour utiliser le nouveau modèle.

>[!NOTE]
>
>Les téléchargements n’incluent pas les mesures de conversion chargées dans Adobe Advertising à partir de fichiers de flux.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. Cochez la case en regard de **[!UICONTROL Upload Conversions to Google Ads]**.

1. (Publicitaires exerçant leurs activités dans l’Espace économique européen (EEE) ou au Royaume-Uni (Royaume-Uni) ; facultatif) Si vous avez recueilli le consentement des utilisateurs de l’EEE et du Royaume-Uni pour télécharger leurs données à des fins publicitaires, cochez la case en regard de **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. Cliquez sur **[!UICONTROL Save]**.

1. (Si vos conversions sont suivies au niveau du compte du gestionnaire) [Ajoutez des informations d’identification pour votre compte du gestionnaire](/help/search-social-commerce/admin/manager-accounts.md) à l’adresse **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [Activer le téléchargement des objectifs vers les réseaux publicitaires](objective-upload-to-networks.md)
