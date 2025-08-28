---
title: Conditions préalables à l’intégration d’Adobe Advertising à Customer Journey Analytics
description: Conditions préalables à l’intégration d’Adobe Advertising à Customer Journey Analytics
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
source-git-commit: ba23ab97c916f829cf9d640669423dd8e72949c0
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Conditions préalables à l’intégration d’Adobe Advertising à Customer Journey Analytics

*Annonceurs avec Advertising DSP et[!DNL Advertising Search, Social, & Commerce]*

Consultez les informations suivantes avant d’intégrer Adobe Advertising à Adobe Customer Journey Analytics.

## Conditions requises pour la création de rapports sur les données Adobe Advertising dans Customer Journey Analytics

* Annonceurs avec [!DNL Analytics for Advertising] et Customer Journey Analytics :

   * Adobe Customer Journey Analytics <!-- any specific version? -->

   * [Toutes les autres conditions préalables pour [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md).

* Annonceurs avec Customer Journey Analytics, mais pas [!DNL Analytics for Advertising] :

   * Bibliothèque Adobe Experience Platform Web SDK : `alloy.js`

     Le [!DNL Org ID] utilisé pour Web SDK et pour le compte de l’annonceur Adobe Advertising doit être le même. Cet identifiant se trouve dans l’onglet [ Résumé de Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

     ![Écran Résumé d’Experience Cloud Debugger](/help/integrations/assets/a4adc-debugger-summary.png)

     Vous aurez besoin de l’aide de l’administrateur de votre site Experience Platform pour créer un flux de données Experience Platform et un schéma XDM.

   * Adobe Customer Journey Analytics <!-- any specific version? -->

     Vous aurez besoin de l’aide de votre analyste web interne pour configurer une connexion à votre jeu de données et configurer des rapports.

>[!TIP]
>
>Pour améliorer la fidélité des données, utilisez la version la plus récente de chaque bibliothèque.

>[!MORELIKETHIS]
>
>* [Aperçu](overview.md)
>* (Utilisateurs Adobe Analytics) [Collecter des données historiques pour les ID AMO et les ID EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
