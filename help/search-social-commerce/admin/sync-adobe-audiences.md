---
title: Sync [!DNL Adobe] audiences
description: Découvrez comment synchroniser les métadonnées, les données hiérarchiques et les données d’audience uniques pour vos  [!DNL Adobe] .
exl-id: 8b8c3aa0-2aa9-4ad7-a4c0-1b7ba881acd3
feature: Search Admin
TQID: https://experienceleague.adobe.com/PKWhdnMHVAI3aI--1vdCeqnX6b8j34uvHycZLw1Yvjw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 191
ht-degree: 0%

---

# Synchroniser [!DNL Adobe] audiences

*[!DNL Direct Access]les gestionnaires et les administrateurs de clients uniquement*

*Publicitaires avec une intégration Adobe Advertising-Adobe Audience Manager ou Adobe Advertising-Adobe Analytics uniquement*

Vous pouvez permettre à Search, Social et Commerce d’extraire des métadonnées, des données hiérarchiques et des données d’audience uniques pour toutes les audiences [!DNL Adobe] d’un annonceur ou d’une agence dans les vues [!UICONTROL Campaigns] > [!UICONTROL Audiences]. Ces informations incluent des données pour :

* Segments Adobe Audience Manager

* Segments Adobe Analytics publiés sur Adobe CX Enterprise

* Segments créés à l’aide de l’[!DNL Audience Library] Adobe CX Enterprise

Pour être éligible, l’annonceur ou l’agence doit mettre en œuvre le [service d’identités Adobe Experience Platform](https://experienceleague.adobe.com/docs/id-service/using/home.html) et fournir son identifiant d’organisation (anciennement appelé [!DNL IMS Org ID]).

La synchronisation initiale prend environ 24 heures. Ensuite, les données sont synchronisées en temps réel, avec un délai d’une à deux secondes.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Audience Manager Setup]**.

1. Saisissez l’ID d’organisation unique du compte Adobe CX Enterprise de l’annonceur, puis cliquez sur **[!UICONTROL Submit]**.

   Si vous ne connaissez pas l’ID d’organisation de l’annonceur, recherchez-le dans le champ **[!UICONTROL IMS Org ID]** des paramètres de l’annonceur à [!UICONTROL Admin] > [!UICONTROL Manage Client].

>[!MORELIKETHIS]
>
>* [À propos des audiences](/help/search-social-commerce/campaign-management/campaigns/audience-about.md)
>* [Intégration aux solutions et services Adobe CX Enterprise](/help/search-social-commerce/introduction/integrations.md)
