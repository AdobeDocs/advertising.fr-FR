---
title: Générer une [!DNL Advertising Insight]
description: Découvrez comment créer une [!DNL Advertising Insight].
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Générer une [!DNL Advertising Insight]

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Advertising Insights]**.

2. Cliquez sur l’insight que vous souhaitez générer.

3. Spécifiez les paramètres d’aperçu :

   1. (Certains rapports ; (facultatif) Spécifiez les plages de dates de l’insight.

   2. (La plupart des insights) Sélectionnez le portefeuille à analyser.

      En règle générale, tous les portfolios optimisés et principaux qui contiennent des campagnes principales sont disponibles. Pour obtenir quelques informations, vous pouvez filtrer la liste des portefeuilles à inclure. **[!UICONTROL Only Optimized Portfolios]**.

      Pour [!UICONTROL Day of Week] les insights, seuls les portefeuilles qui ont assez dépensé et qui ont également dépensé pour cibler les deux derniers jours sont disponibles.

   3. ([!UICONTROL Event Path Beta] Infos uniquement) Effectuez les opérations suivantes :

      1. Sélectionnez la **[!UICONTROL Operation]**: *[!UICONTROL Extract events]* (pour charger une [!UICONTROL Channel Assist Report] ou [!UICONTROL Campaign Assist Report] et classer les événements utilisateur en groupes distincts pour analyse) ou *[!UICONTROL Analyze classified events]* (pour charger des groupes d’événements et les utiliser pour générer les informations).

      1. Cliquez sur **[!UICONTROL Select]** pour localiser un fichier au format XLSX et ZIP (XLSX compressé), puis cliquez sur **[!UICONTROL Upload]**.
   4. ([!UICONTROL Google Account Audit] Infos uniquement) Effectuez les opérations suivantes :

      1. Saisissez le **[!UICONTROL Advertiser Name]** et **[!UICONTROL Account Name]**.

      1. Sélectionnez la **[!UICONTROL Account Currency]**, **[!UICONTROL File Format Region]** (*[!UICONTROL United States]* ou *[!UICONTROL United Kingdom]*), et la variable **[!UICONTROL Output Language]** (*[!UICONTROL English (USA)]*, *[!UICONTROL French]* ou *[!UICONTROL German]*).

      1. Cliquez sur **[!UICONTROL Select]** pour localiser les rapports de campagne, de mot-clé et d’historique de modification téléchargés pour le compte à partir de la variable [!DNL Google Ads] l’interface utilisateur web et un fichier de feuille d’envoi groupé téléchargé pour le compte à partir du [!DNL Google Ads Editor] application. Cliquez ensuite sur **[!UICONTROL Upload]**.

         Tous les fichiers doivent être au format CSV, TSV, TXT ou ZIP (CSV compressé, TSV ou TXT).
   5. ([!UICONTROL Location Target Performance] la perspicacité uniquement; (facultatif) Pour agréger les données quotidiennement plutôt que sous forme de résumé, sélectionnez la variable **[!UICONTROL Time Aggregation]** de *[!UICONTROL Daily]*.

   6. ([!UICONTROL Normalized Sim (Combined)] Infos uniquement) Effectuez les opérations suivantes :

      1. Dans le **[!UICONTROL Step]** , indiquez le nombre de niveaux de dépenses cibles, ou étapes, à inclure dans l’insight. La valeur peut être comprise entre trois (3) et 100.

      1. Dans le **[!UICONTROL Type]** sélectionnez le type de simulation :

         * *[!UICONTROL Optimized Multi-portfolio]*: Génère une simulation unique sur plusieurs portefeuilles avec le même objectif et la même devise.

         * *[!UICONTROL Individual Normalized]*: Génère une simulation individuelle pour chaque portefeuille sélectionné. Les portefeuilles peuvent avoir des objectifs et des devises différents.
   7. ([!UICONTROL Portfolio Launch] la perspicacité uniquement; (facultatif) Pour spécifier une date de lancement dans le futur, indiquez une date dans la variable **[!UICONTROL Optional Date]** champ .

   8. ([!UICONTROL Quality Score] insight uniquement) Sélectionnez le réseau publicitaire approprié.

   9. ([!UICONTROL Query Cross Matching] (Infos uniquement) Dans la variable **[!UICONTROL Google Accounts]** , sélectionnez le compte .




4. Cliquez sur **[!UICONTROL Generate Insight]**.

   Vous recevrez une notification lorsque la tâche sera terminée ou échouera en fonction de votre [paramètres de notification configurés](/help/search-social-commerce/notifications/notification-edit.md) pour [!UICONTROL Advertising Insights].

>[!MORELIKETHIS]
>
>* [A propos [!UICONTROL Advertising Insights]](insight-about.md)
>* [Affichage ou enregistrement d’une [!DNL Advertising Insight]](insight-view-save.md)
>* [Suppression d’un [!DNL Advertising Insight]](insight-delete.md)

