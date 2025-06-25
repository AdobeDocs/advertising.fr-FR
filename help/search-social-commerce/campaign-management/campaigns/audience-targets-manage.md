---
title: Gestion des cibles d’audience pour les campagnes et les groupes publicitaires
description: Découvrez comment configurer et gérer les cibles d’audience pour vos campagnes [!DNL Google Ads] et [!DNL Microsoft Advertising] groupes publicitaires.
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# Gérer les cibles d’audience pour vos campagnes et groupes publicitaires [!DNL Google Ads] et [!DNL Microsoft Advertising]

*[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

[!DNL Google Ads] campagnes et groupes publicitaires, ainsi que les groupes publicitaires [!DNL Microsoft Advertising], peuvent cibler des audiences spécifiques à partir du même réseau publicitaire. Le réseau publicitaire détermine la taille que doit avoir une audience pour pouvoir être ciblée.

>[!NOTE]
>
>Les exclusions remplacent toujours les inclusions/cibles.

Vous pouvez configurer des cibles d’audience, modifier les modificateurs d’enchères pour les cibles d’audience et modifier le statut des cibles d’audience.

## Configurer les cibles d’audience

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Sélectionnez le réseau publicitaire et le nom du compte, puis cliquez sur **[!UICONTROL Continue]**.

1. Configurez les cibles d’audience pour des campagnes et des groupes publicitaires spécifiques :

   1. Sélectionnez les audiences applicables pour le réseau publicitaire spécifié.

      Vous pouvez éventuellement rechercher des audiences qui contiennent une chaîne de texte spécifique d’au moins trois caractères. Pour toute audience correspondante, cliquez sur **[!UICONTROL Include]** pour la sélectionner.

      [!DNL Google Ads] audiences de correspondance client ne sont disponibles que pour les campagnes de recherche et d’achat.

   1. Spécifiez les cibles :

      1. (Facultatif) Pour développer une campagne avec ses groupes d’annonces enfants, cliquez sur le nom de la campagne.

      1. (Facultatif) Pour filtrer une liste de campagnes ou de groupes publicitaires selon une chaîne de texte incluse dans le nom, cliquez sur ![Filtrer](/help/search-social-commerce/assets/filter.png "Filtrer") , saisissez ou collez la chaîne de texte dans le champ de saisie, puis appuyez sur la touche **[!UICONTROL Enter]**.

      1. Spécifiez chaque campagne et cible de groupe publicitaire pour le réseau publicitaire spécifié en cliquant sur le cercle vide adjacent afin qu’une coche bleue (![Sélectionner](/help/search-social-commerce/assets/include.png "Sélectionner")) s’affiche.

      Vous ne pouvez pas configurer de cible à la fois pour une campagne parent et un groupe publicitaire enfant (qui utilise automatiquement la cible).

1. Cliquez sur **[!UICONTROL Post]**.

1. (Facultatif) Définissez un ajustement d’offre pour la cible de l’une des manières suivantes à partir de la vue [!UICONTROL Targets] :

   * Cliquez dans la colonne **[!UICONTROL Bid Adjustment]** et saisissez une valeur.

   * Cochez la case en regard de la ligne cible. Dans la barre d’outils , cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier"), saisissez le modificateur d’offre, puis cliquez sur **[!UICONTROL Post]**.

   Les valeurs peuvent inclure :

   * *0 % :* pour ne pas ajuster les enchères pour les publicités de cette audience.

   * /[*Autres valeurs de -90 % à 900 %*/] : pour augmenter ou diminuer l’enchère pour les publicités de cette audience. Par exemple, si l’enchère au niveau du mot-clé est de 1 USD et que l’ajustement d’enchère pour une cible d’audience spécifique est de 50 %, l’enchère pour cette audience augmente à 1,50 USD.

## Modifier le modificateur d’offre pour les cibles d’audience

Vous pouvez modifier les conditions commerciales et le statut des cibles d’audience pour tous les types d’audience, à l’exception des audiences de marché.

>[!NOTE]
>
>Search, Social et Commerce optimise automatiquement les conditions commerciales d’enchères lorsque la campagne parent utilise la stratégie d’enchères CPC et se trouve dans un portefeuille configuré pour optimiser automatiquement les valeurs d’ajustement d’enchère pour les cibles d’audience.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. Effectuez l’une des opérations suivantes :

   * Pour modifier un modificateur d&#39;offre pour une cible, cliquez dans la colonne **[!UICONTROL Bid Adjustment]** et modifiez l&#39;ajustement d&#39;offre.

   * Pour modifier un modificateur d&#39;offre pour une ou plusieurs cibles, procédez comme suit :

      1. Cochez la case en regard de chaque cible à modifier.

         Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

      1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

      1. Modifiez les champs de **[!UICONTROL Bid Modifier]** et/ou de **[!UICONTROL Status]**.

         Pour le champ [!UICONTROL Bid Modifier], vous avez la possibilité de modifier les valeurs existantes à une valeur spécifiée ou d’augmenter ou de diminuer le montant d’un pourcentage ou d’un montant monétaire spécifié, avec une limite.

         Pour une valeur définie, la valeur peut inclure :

         * *0 % :* pour ne pas ajuster les enchères pour les publicités de cette audience.

         * /[*Autres valeurs de -90 % à 900 %*/] : pour augmenter ou diminuer l’enchère pour les publicités de cette audience. Par exemple, si l’enchère au niveau du mot-clé est de 1 USD et que l’ajustement d’enchère pour une cible d’audience spécifique est de 50 %, l’enchère pour cette audience augmente à 1,50 USD.

         Si plusieurs cibles sont sélectionnées, vos modifications sont appliquées à toutes les cibles sélectionnées.

      1. (Facultatif) Cliquez sur **[!UICONTROL Additional Details]** et entrez éventuellement un nom et une description de projet.

      1. Cliquez sur **[!UICONTROL Post]**.

## Modifier le statut des cibles d’audience

Vous pouvez mettre en pause une cible d’audience active afin de désactiver les enchères associées. Vous pouvez ensuite reprendre les enchères en redéfinissant leur statut sur Actif.

Vous pouvez également supprimer une cible d’audience de recherche active ou en pause.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. (Facultatif) Filtrez la liste pour inclure des cibles d’audience spécifiques.

1. Cochez la case en regard de chaque cible d’audience dont vous souhaitez modifier le statut.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d&#39;outils, cliquez sur le bouton Statut :

   * Pour activer les lignes, cliquez sur ![Activer](/help/search-social-commerce/assets/activate.png "Activer").

   * Pour suspendre les lignes, cliquez sur ![Pause](/help/search-social-commerce/assets/pause.png "Pause").

   * Pour supprimer les lignes, cliquez sur ![Autres actions](/help/search-social-commerce/assets/more.png "Autres actions") et sélectionnez **[!UICONTROL Delete]**. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Gérer les exclusions d’audience pour les campagnes et les groupes publicitaires](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
