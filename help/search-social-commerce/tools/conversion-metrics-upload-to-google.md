---
title: Chargement des mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads]
description: Découvrez comment télécharger des mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads].
exl-id: 976792ae-135c-4790-82cf-9503edb93fb1
feature: Search Tools
TQID: 'https://experienceleague.adobe.com/ayxUfDgkrnPz0s-pFAdkmvYy94Il5szQHl6lYg8DpF8'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 9f383e89-9ec3-5629-8dc3-d5aa5ab0be32
    internal-label: Search Tools
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '216'
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
