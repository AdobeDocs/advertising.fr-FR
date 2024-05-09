---
title: Création d’une source d’audience pour activer les audiences propriétaires
description: Découvrez comment créer une source pour importer des audiences dans votre compte ou un compte publicitaire.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---

# Création d’une source d’audience pour activer les audiences propriétaires

<!-- Will this remain for admin users/Adobe Account Team users only? -->

Créez une source dans DSP pour importer des audiences propriétaires vers votre compte DSP ou un compte publicitaire.

Pour connaître les étapes supplémentaires requises pour ingérer des segments à partir de plateformes de données client spécifiques, voir [les workflows d’activation spécifiques à l’audience ;](source-about.md)

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Cliquez sur **[!UICONTROL Add Source]**.

1. Dans le [!UICONTROL Select a Type] , sélectionnez le type de source.

   * *[!UICONTROL RT-CDP]*: [La variable [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   <!-- * *[!UICONTROL ActionIQ]*: The [[!DNL ActionIQ] customer data platform](source-about.md). -->

   * *[!UICONTROL Tealium CDP]*: la variable [[!DNL Tealium] plateforme de données client](source-about.md).

1. Spécifiez la variable [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Saisissez le reste [paramètres source](source-settings.md).

   Conserver une copie de la fonction [!UICONTROL Source Key] qui est généré. Vous aurez besoin de la valeur plus tard.

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Après avoir créé une source pour votre plateforme de données client, vous devez effectuer d’autres étapes. Voir [workflow d’activation pour [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> et la variable [workflow d’activation pour [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Paramètres de la source d’audience](source-settings.md)
>* [À propos de l’activation de segments authentifiés à partir des sources d’audience](source-about.md)
>* [Activation des segments authentifiés à partir des partenaires d’ID universels](source-universal-id.md)<!-- title?-->
>* [Connexion Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
