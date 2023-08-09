---
title: Création d’un objectif personnalisé
description: Création d’un objectif personnalisé
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Création d’un objectif personnalisé

Vous pouvez créer des objectifs personnalisés sous la forme *objectifs* dans [!DNL Advertising Search, Social, & Commerce].

Pour créer un objectif personnalisé, le compte DSP doit être associé à un [!DNL Search, Social, & Commerce] avec le même ID d’organisation Adobe Experience Cloud, depuis le [!DNL Search, Social, & Commerce] paramètres du client. Si votre compte DSP n’est pas lié à un [!DNL Search, Social, & Commerce] contactez votre équipe de compte d’Adobe.

>[!TIP]
>
>Voir [bonnes pratiques pour la création d’objectifs personnalisés](custom-goal-best-practices.md) pour obtenir des conseils sur la configuration de vos objectifs personnalisés.

1. Se connecter [!DNL Advertising Search, Social, & Commerce] at (utilisateurs en Amérique du Nord) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) ou (tous les autres utilisateurs) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. Assurez-vous que les mesures que vous souhaitez inclure dans votre objectif ont été suivies, sont disponibles dans le produit et incluez un nom d’affichage :
   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.
   1. Recherchez la mesure et assurez-vous que la variable **[!UICONTROL Show in UI and Reports]** est activé pour la mesure.
   1. Si la mesure n’a pas de valeur dans la variable **[!UICONTROL Display Name]** , cliquez dans la cellule, saisissez le nom d’affichage, puis cliquez sur **[!UICONTROL Apply].**
1. Créez l’objectif personnalisé en tant que *objectif*:
   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. Dans la barre d’outils, cliquez sur **[!UICONTROL Create objective].**
   1. Renseignez les paramètres de l&#39;objectif :
      1. Dans le **[!UICONTROL Change Objective Name]** , saisissez le nom de l’objectif.

         Le nom de l’objectif s’affiche dans la [!UICONTROL Custom Goals] dans les paramètres du module DSP.

      1. Associez les propriétés à l’objectif :

         >[!NOTE]
         >
         > Toutes les mesures de conversion suivies pour l’annonceur sont répertoriées par défaut dans la variable [!UICONTROL Available Properties] liste.

         * Pour importer un fichier CSV avec des mesures de conversion et leur poids, cliquez sur **[!UICONTROL Import]** et localisez le fichier à importer.

           Les mesures de conversion importées doivent déjà exister pour l’annonceur ; les noms ne respectent pas la casse.

           Les mesures de conversion importées remplacent toutes les propriétés existantes spécifiées.

         * Pour spécifier manuellement la première mesure de conversion avec le poids par défaut (1), sélectionnez dans la liste de toutes les mesures de conversion suivies pour l’annonceur.

         * Pour ajouter manuellement une autre mesure de conversion avec le poids par défaut (1), cliquez sur **[!UICONTROL +]** .

           >[!TIP]
           >
           > Pour rechercher une mesure dans la liste, saisissez une chaîne n’importe où dans le nom de la mesure.

         * Pour ajouter manuellement plusieurs mesures de conversion, cliquez sur **[!UICONTROL Add Multiple Properties].** Pour chaque mesure de conversion à ajouter, cliquez sur le nom de la mesure dans la variable [!UICONTROL Available Properties] et faites-le glisser dans la [!UICONTROL Added Properties] colonne . Lorsque vous avez terminé d’ajouter des mesures, cliquez sur **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* Pour rechercher une mesure dans la liste, saisissez une chaîne n’importe où dans le nom de la mesure dans le champ de saisie.
           >* Pour filtrer la liste afin d’exclure les mesures qui sont exclues des rapports, sélectionnez l’option . **[!UICONTROL Hide properties excluded from reports].**

         * (Lorsque l’objectif contient plusieurs mesures de conversion) Pour modifier le poids d’une mesure par rapport aux autres mesures de l’objectif, saisissez des valeurs dans la variable **[!UICONTROL Weight]** champs.

      1. Au bas des paramètres, cliquez sur **[!UICONTROL Save]**.

Une fois que vous avez créé un objectif, vous pouvez l’affecter à un module DSP en tant qu’objectif personnalisé lorsque l’objectif d’optimisation est &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; ou &quot;[!UICONTROL Lowest CPA - Custom Goal].&quot;

>[!TIP]
>
>Pour des performances optimales, les mesures combinées de l’objectif personnalisé (objectif) doivent totaliser au moins dix conversions par jour. Dans le cas contraire, la bonne pratique consiste à ajouter à l’objectif des mesures de conversion supplémentaires, telles que des pages de produits ou des démarrages d’application, qui prennent en charge la conversion. Voir [Bonnes pratiques pour la création d’un objectif personnalisé](custom-goal-best-practices.md) pour obtenir des instructions.

>[!MORELIKETHIS]
>
>* [À propos des objectifs personnalisés](custom-goal-about.md)
>* [Bonnes pratiques pour la création d’un objectif personnalisé](custom-goal-best-practices.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
> * [Optimisation des campagnes par DSP](optimization-how-dsp-optimizes-campaigns.md)
