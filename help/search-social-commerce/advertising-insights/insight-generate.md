---
title: Générer un [!DNL Advertising Insight]
description: Découvrez comment créer un [!DNL Advertising Insight].
exl-id: e6b692be-189e-4c6c-a536-e6c78801853d
feature: Search Advertising Insights
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---

# Générer un [!DNL Advertising Insight]

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Cliquez sur l’insight que vous souhaitez générer.

3. Spécifiez les paramètres d’aperçu :

   1. (Certains rapports ; facultatif) Spécifiez les plages de dates de l’insight.

   2. (La plupart des insights) Sélectionnez le portefeuille à analyser.

      En règle générale, tous les portfolios optimisés et actifs contenant des campagnes actives sont disponibles. Pour obtenir des informations, vous pouvez filtrer la liste de portefeuille afin d’inclure **[!UICONTROL Only Optimized Portfolios]**.

      Pour les [!UICONTROL Day of Week] insights, seuls les portefeuilles qui ont assez dépensé et qui ont également dépensé pour cibler les deux derniers jours sont disponibles.

   3. ([!UICONTROL Event Path Beta] insight uniquement) Effectuez les opérations suivantes :

      1. Sélectionnez le **[!UICONTROL Operation]** : *[!UICONTROL Extract events]* (pour charger un [!UICONTROL Channel Assist Report] ou [!UICONTROL Campaign Assist Report] et classer les événements utilisateur dans des groupes distincts à des fins d’analyse) ou *[!UICONTROL Analyze classified events]* (pour charger des groupes d’événements et les utiliser pour générer les informations).

      1. Cliquez sur **[!UICONTROL Select]** pour localiser un fichier au format XLSX et ZIP (XLSX compressé), puis cliquez sur **[!UICONTROL Upload]**.

   4. ([!UICONTROL Google Account Audit] insight uniquement) Effectuez les opérations suivantes :

      1. Saisissez les **[!UICONTROL Advertiser Name]** et **[!UICONTROL Account Name]**.

      1. Sélectionnez les **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* ou *[!UICONTROL United Kingdom]*) et **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* ou *[!UICONTROL German]*).

      1. Cliquez sur **[!UICONTROL Select]** pour localiser les rapports de campagne, de mot-clé et d’historique de modification téléchargés pour le compte à partir de l’interface utilisateur web [!DNL Google Ads] et d’un fichier de feuille d’envoi téléchargé pour le compte à partir de l’application [!DNL Google Ads Editor]. Cliquez ensuite sur **[!UICONTROL Upload]**.

         Tous les fichiers doivent être au format CSV, TSV, TXT ou ZIP (CSV compressé, TSV ou TXT).

   5. ([!UICONTROL Location Target Performance] insight uniquement ; facultatif) Pour agréger les données quotidiennement plutôt que sous forme de résumé, sélectionnez l’ **[!UICONTROL Time Aggregation]** de *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] insight uniquement) Effectuez les opérations suivantes :

      1. Dans le champ **[!UICONTROL Step]** , spécifiez le nombre de niveaux de dépenses cibles, ou étapes, à inclure dans l’insight. La valeur peut être comprise entre trois (3) et 100.

      1. Dans le champ **[!UICONTROL Type]** , sélectionnez le type de simulation :

         * *[!UICONTROL Optimized Multi-portfolio]* : génère une simulation unique sur plusieurs portefeuilles avec le même objectif et la même devise.

         * *[!UICONTROL Individual Normalized]* : génère une simulation individuelle pour chaque portefeuille sélectionné. Les portefeuilles peuvent avoir des objectifs et des devises différents.

   7. ([!UICONTROL Portfolio Launch] insight uniquement ; facultatif) Pour spécifier une date de lancement dans le futur, spécifiez une date dans le champ **[!UICONTROL Optional Date]**.

   8. ([!UICONTROL Quality Score] insight uniquement) Sélectionnez le réseau publicitaire approprié.

   9. ([!UICONTROL Query Cross Matching] insight uniquement) Dans le menu **[!UICONTROL Google Accounts]**, sélectionnez le compte.

4. Cliquez sur **[!UICONTROL Generate Insight]**.

   Vous recevez une notification lorsque la tâche est terminée ou échoue en fonction de vos [ paramètres de notification configurés](/help/search-social-commerce/notifications/notification-edit.md) pour [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [À propos de [!UICONTROL Advertising Insights]](insight-about.md)
>* [Afficher ou enregistrer un [!DNL Advertising Insight]](insight-view-save.md)
>* [Supprimer un [!DNL Advertising Insight]](insight-delete.md)
