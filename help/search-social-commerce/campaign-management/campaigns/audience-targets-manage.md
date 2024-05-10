---
title: Gestion des cibles d’audience pour les campagnes et les groupes publicitaires
description: Découvrez comment configurer et gérer les cibles d’audience pour vos [!DNL Google Ads] et [!DNL Microsoft Advertising] campagnes et groupes publicitaires.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Gestion des cibles d’audience pour votre [!DNL Google Ads] et [!DNL Microsoft Advertising] campagnes et groupes publicitaires

*[!DNL Google Ads]et [!DNL Microsoft Advertising] only*

[!DNL Google Ads] campagnes et groupes publicitaires, et [!DNL Microsoft Advertising] groupes publicitaires peuvent cibler des audiences spécifiques du même réseau publicitaire. Le réseau publicitaire détermine la taille d’une audience qui doit pouvoir être ciblée.

>[!NOTE]
>
>Les exclusions remplacent toujours les inclusions/cibles.

Vous pouvez configurer des cibles d’audience, modifier les modificateurs d’offre des cibles d’audience et modifier l’état des cibles d’audience.

## Configuration des cibles d’audience

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Configurez les cibles d’audience pour des campagnes et des groupes d’annonces spécifiques :

   1. Sélectionnez les audiences applicables pour le réseau publicitaire spécifié.

      Vous pouvez éventuellement rechercher des audiences qui contiennent une chaîne de texte spécifique avec un minimum de trois caractères. Pour toute audience correspondante, cliquez sur **[!UICONTROL Include]** pour la sélectionner.

      [!DNL Google Ads] les audiences de correspondance client sont disponibles uniquement pour les campagnes de recherche et d’achat.

   1. Spécifiez les cibles :

      1. (Facultatif) Pour développer une campagne avec ses groupes d’annonces enfants, cliquez sur le nom de la campagne.

      1. (Facultatif) Pour filtrer une liste de campagnes ou de groupes publicitaires selon une chaîne de texte incluse dans le nom, cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter.png "Filtrer") , saisissez ou collez la chaîne de texte dans le champ de saisie, puis appuyez sur la touche **[!UICONTROL Enter]** clé.

      1. Spécifiez chaque cible de campagne et de groupe publicitaire pour le réseau publicitaire spécifié en cliquant sur le cercle vide adjacent afin d’obtenir une coche bleue (![Sélectionner](/help/search-social-commerce/assets/include.png "Sélectionner")) s’affiche.

      Vous ne pouvez pas configurer de cible pour une campagne parente et un groupe d’annonces enfants (qui utilise automatiquement la cible).

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Définissez un ajustement d’offre pour la cible de l’une des façons suivantes de la variable [!UICONTROL Targets] view :

   * Cliquez sur dans le **[!UICONTROL Bid Adjustment]** et saisissez une valeur.

   * Cochez la case en regard de la ligne cible. Dans la barre d’outils , cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier"), saisissez le modificateur d’offre, puis cliquez sur **[!UICONTROL Post]**.

   Les valeurs peuvent inclure :

   * *0 % :* Pour ne pas ajuster les offres pour les publicités de cette audience.

   * /[*Autres valeurs comprises entre -90 % et 900 %*/]: pour augmenter ou diminuer l’offre pour les publicités de cette audience. Par exemple, si l’offre au niveau du mot-clé est de 1 USD et que l’ajustement de l’offre pour une cible d’audience spécifique est de 50 %, l’offre pour cette audience passe à 1,50 USD.

## Modifier le modificateur d’offre pour les cibles d’audience

Vous pouvez modifier le modificateur d’offre et l’état des cibles d’audience pour tous les types d’audience, à l’exception des audiences du marché.

>[!NOTE]
>
>Search, Social et Commerce optimise automatiquement le modificateur d’offre lorsque la campagne parente utilise la stratégie d’offre CPC et se trouve dans un portefeuille configuré pour optimiser automatiquement les valeurs d’ajustement d’offre pour les cibles d’audience.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Effectuez l’une des opérations suivantes :

   * Pour modifier un modificateur d’offre pour une cible, cliquez sur dans le **[!UICONTROL Bid Adjustment]** et modifiez l’ajustement de l’offre.

   * Pour modifier un modificateur d’offre pour une ou plusieurs cibles, procédez comme suit :

      1. Cochez la case en regard de chaque cible à modifier.

         Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

      1. Modifiez la variable **[!UICONTROL Bid Modifier]** et/ou **[!UICONTROL Status]** des champs.

         Pour le [!UICONTROL Bid Modifier] , vous avez la possibilité de modifier les valeurs existantes en une valeur spécifique ou d’augmenter ou de diminuer le montant d’un pourcentage spécifié ou d’un montant monétaire, avec une limite.

         Pour une valeur définie, la valeur peut inclure :

         * *0 % :* Pour ne pas ajuster les offres pour les publicités de cette audience.

         * /[*Autres valeurs comprises entre -90 % et 900 %*/]: pour augmenter ou diminuer l’offre pour les publicités de cette audience. Par exemple, si l’offre au niveau du mot-clé est de 1 USD et que l’ajustement de l’offre pour une cible d’audience spécifique est de 50 %, l’offre pour cette audience passe à 1,50 USD.

         Pour plusieurs cibles, vos modifications sont appliquées à toutes les cibles sélectionnées.

      1. (Facultatif) Cliquez sur **[!UICONTROL Additional Details]** et éventuellement saisir un nom et une description du projet.

      1. Cliquez sur **[!UICONTROL Post]**.

## Modifier l’état des cibles d’audience

Vous pouvez suspendre une cible d’audience active pour désactiver l’offre sur celle-ci. Vous pouvez reprendre l’enchère ultérieurement en redéfinissant l’état sur actif.

Vous pouvez également supprimer une cible d’audience de recherche active ou suspendue.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Facultatif) Filtrez la liste pour inclure des cibles d’audience spécifiques.

1. Cochez la case en regard de chaque cible d’audience dont vous souhaitez modifier l’état.

   Pour plus d’informations sur la sélection de plusieurs lignes, voir &quot;[Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. Dans la barre d’outils, cliquez sur le bouton d’état :

   * Pour activer les lignes, cliquez sur ![Activer](/help/search-social-commerce/assets/activate.png "Activer").

   * Pour suspendre les lignes, cliquez sur ![Pause](/help/search-social-commerce/assets/pause.png "Pause").

   * Pour supprimer les lignes, cliquez sur ![Autres actions](/help/search-social-commerce/assets/more.png "Autres actions") et sélectionnez **[!UICONTROL Delete]**. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [A propos des audiences](audience-about.md)
>* [Gestion des exclusions d’audience pour les campagnes et les groupes publicitaires](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
