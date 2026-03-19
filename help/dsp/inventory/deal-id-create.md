---
title: Créer manuellement les détails de l’ID d’offre
description: Découvrez comment saisir manuellement les détails d’un ID d’offre.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: a5be425ee34960cf58642cb850ae817998652f53
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Créer manuellement les détails de l’ID d’offre

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**, puis sélectionnez **[!UICONTROL Deal ID]**.

1. Saisissez les [ paramètres de l’offre ](deal-id-settings.md) :

   1. Dans la section [!UICONTROL Deal ID basics] , spécifiez les détails de l’offre et les annonceurs qui peuvent y accéder. Pour les offres garanties, vous devez également spécifier les dates de vol prévues et le nombre estimé d’impressions, à des fins de suivi uniquement.

      Vous pouvez suivre le rythme des offres garanties en incluant la colonne « Fréquence d’impression PG » dans la vue Inventaire > Offres .

   1. (Utilisateurs administrateurs uniquement ; facultatif) Dans la section [!UICONTROL Technical], modifiez les paramètres par défaut selon vos besoins.

   1. Cliquez sur **[!UICONTROL Save]**.

1. (Offres garanties uniquement) Sélectionnez les annonces à utiliser pour l’offre (ou le pixel 1x1 pour les annonces gérées par l’éditeur) et créez un emplacement programmatique garanti (PG) par défaut.

   Les emplacements PG par défaut garantissent que votre offre renvoie toujours une offre pour chaque demande d’offre. Si vous ne créez pas d’emplacement PG par défaut, les emplacements qui ciblent l’offre ne placent pas d’offres, sauf s’ils sont correctement configurés. Vous devez toujours créer un emplacement PDF par défaut. Dans la vue [!UICONTROL Placements], les emplacements PG par défaut ont une valeur de colonne [!UICONTROL Sub-type] de « [!UICONTROL PG Default] ».

   Vous pouvez éventuellement utiliser l’opération comme cible de stock dans des emplacements supplémentaires, mais vous devez la configurer correctement pour placer des offres.

   1. Dans les paramètres [!UICONTROL Ad & Campaign Selection], sélectionnez les annonces à utiliser pour la transaction :

      1. Sélectionnez l’annonceur, la campagne et le type d’annonce. Vous pouvez éventuellement sélectionner un statut d’annonce publicitaire selon lequel filtrer les annonces.

      1. Dans la liste des publicités disponibles, cochez la case en regard de chaque publicité à utiliser pour l’offre.

         Pour chaque publicité gérée par l’éditeur, un pixel de suivi 1x1 est automatiquement appliqué après la sélection d’un annonceur et d’une campagne.

      1. Cliquez sur **[!UICONTROL Apply]**.

   1. Dans l’écran des paramètres d’emplacement :

      1. Saisissez le nom de l’emplacement.

      1. (Facultatif) Modifiez les [paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md), y compris en remplaçant l’enchère par défaut, qui est automatiquement renseignée avec la valeur CPM de l’opération ; en modifiant la période ; ou en joignant d’autres annonces.

      L’opération est automatiquement ciblée dans la section Cibles d’inventaire . Toutes les autres options de ciblage ne sont pas applicables.

      1. Cliquez sur **[!UICONTROL Create placement]**.

Après avoir créé l’opération, vous pouvez l’utiliser comme cible de stock pour plusieurs emplacements.

>[!NOTE]
>
> Vous n’avez pas besoin d’envoyer la balise d’offre à l’éditeur pour vérification.

>[!TIP]
>
>* Dans la vue [!UICONTROL Inventory] > [!UICONTROL Deals] , la colonne [!UICONTROL Pacing & Budget] indique le rythme de l’opération par rapport à la date de vol et à l’objectif d’impression spécifiés.
>
>* Si la diffusion est insuffisante ou excessive, contactez votre éditeur pour ajuster le volume qu’il envoie dans le cadre de l’offre.

>[!MORELIKETHIS]
>
>* [Paramètres manuels d’ID d’offre](deal-id-settings.md)
>* [Configurer une offre programmatique garantie](programmatic-guaranteed-set-up.md)
>* [Soumettre une annonce pour un contrat programmatique garanti avec  [!DNL FreeWheel]](freewheel-submit.md)
>* [À propos des offres programmatiques garanties](programmatic-guaranteed-about.md)
<!-- >* [Specify placements and ads for a private deal](deal-id-attach-placements.md)-->
