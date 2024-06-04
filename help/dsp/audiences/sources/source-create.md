---
title: Création d’une source d’audience pour activer les audiences d’ID universelles
description: Découvrez comment créer une source pour importer des audiences de votre plateforme de données client et les convertir en segments contenant des ID universels.
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 16a796e02150b00c77c825d7f54c6e390c85214a
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Création d’une source d’audience pour activer les audiences d’ID universelles

*Fonction bêta*

Créez une source dans DSP pour chaque audience propriétaire de votre plateforme de données client que vous souhaitez convertir en segments contenant des types d’ID universels spécifiés. Vous pouvez importer les segments dans le compte DSP de votre entreprise ou dans un compte publicitaire. Les frais de données sont appliqués en fonction des types d’ID universels sélectionnés.

Des étapes supplémentaires sont nécessaires pour ingérer les audiences à partir de chaque plateforme de données client. Consultez la note à la fin de la procédure.

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. Cliquez sur **[!UICONTROL Add Source]**.

1. Dans le [!UICONTROL Select a Type] , sélectionnez votre plateforme de données client :

   * *[!UICONTROL RT-CDP]*: [La variable [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*: la variable [[!DNL ActionIQ] plateforme de données client](source-about.md).

   * *[!UICONTROL Tealium CDP]*: (utilisateurs configurés uniquement) La variable [[!DNL Tealium] plateforme de données client](source-about.md).

1. Spécifiez la variable [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* ou *[!UICONTROL Account]*.

1. Saisissez le reste [paramètres source](source-settings.md).

   Conserver une copie de la fonction [!UICONTROL Source Key] qui est généré. Vous aurez besoin de la valeur plus tard.

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Après avoir créé une source pour votre plateforme de données client, vous devrez effectuer d’autres étapes. Voir [workflow pour importer des audiences depuis [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> et la variable [workflow pour importer des audiences depuis [!DNL Tealium]](source-tealium.md).

>[!MORELIKETHIS]
>
>* [Paramètres de la source d’audience](source-settings.md)
>* [À propos des sources d’audience propriétaires](source-about.md)
>* [Connexion Adobe Advertising Cloud DSP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
