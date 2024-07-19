---
title: Création manuelle des détails de l’identifiant de transaction
description: Découvrez comment saisir manuellement les détails d’un ID de transaction.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# Création manuelle des détails de l’identifiant de transaction

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**, puis sélectionnez **[!UICONTROL Deal ID]**.

1. Saisissez les [paramètres de transaction](deal-id-settings.md) :

   1. Dans la section [!UICONTROL Deal ID basics] , spécifiez les détails de la transaction et les annonceurs qui peuvent accéder à la transaction. Pour les offres garanties, vous devez également spécifier les dates de vol prévues et le nombre estimé d&#39;impressions, à des fins de suivi uniquement.

      Vous pouvez suivre le rythme des offres garanties en incluant la colonne &quot;Calcul de l’impression PG&quot; dans la vue Inventaire > Transactions.

   1. (Utilisateurs administrateurs uniquement ; facultatif) Dans la section [!UICONTROL Technical], modifiez les paramètres par défaut selon vos besoins.

   1. Cliquez sur **[!UICONTROL Save]**.

1. (Offres garanties uniquement) Sélectionnez les publicités à utiliser pour l’opération (ou le pixel 1x1 pour les publicités gérées par l’éditeur) et créez un emplacement par défaut garanti par la programmation (PG).

   Les emplacements PG par défaut garantissent que votre transaction renvoie toujours une offre pour chaque demande d’offre. Si vous ne créez pas d’emplacement PG par défaut, tous les emplacements qui ciblent l’opération ne placent pas d’offres à moins qu’ils ne soient correctement configurés. Vous devez toujours créer un emplacement PG par défaut. Dans la vue [!UICONTROL Placements], les emplacements PG par défaut ont une valeur de colonne [!UICONTROL Sub-type] de &quot;[!UICONTROL PG Default]&quot;.

   Vous pouvez éventuellement utiliser l’opération comme cible d’inventaire dans d’autres emplacements, mais vous devez les configurer correctement pour placer des offres.

   1. Dans les paramètres [!UICONTROL Ad & Campaign Selection], sélectionnez les publicités à utiliser pour l’opération :

      1. Sélectionnez l’annonceur, la campagne et le type d’annonce. Vous pouvez éventuellement sélectionner l’état d’une publicité pour filtrer les publicités.

      1. Dans la liste des publicités disponibles, cochez la case en regard de chaque publicité à utiliser pour l’opération.

         Pour chaque publicité gérée par l’éditeur, un pixel de suivi 1x1 est automatiquement appliqué après la sélection d’un annonceur et d’une campagne.

      1. Cliquez sur **[!UICONTROL Apply]**.

   1. Dans l’écran des paramètres d’emplacement :

      1. Saisissez le nom de l’emplacement.

      1. (Facultatif) Modifiez les [paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md), y compris le remplacement de l’offre par défaut, qui est automatiquement renseignée avec la valeur CPM de l’opération, la modification de la période ou l’ajout d’annonces en pièce jointe.

      L’opération est automatiquement ciblée dans la section Cibles de l’inventaire . Toutes les autres options de ciblage ne sont pas applicables.

      1. Cliquez sur **[!UICONTROL Create placement]**.

Une fois l’opération créée, vous pouvez l’utiliser comme cible d’inventaire pour plusieurs emplacements.

>[!NOTE]
>
> Vous n’avez pas besoin d’envoyer la balise de transaction à l’éditeur pour vérification.

>[!TIP]
>
>* Dans la vue [!UICONTROL Inventory] > [!UICONTROL Deals], la colonne [!UICONTROL Pacing & Budget] indique comment l’opération se déroule selon la date de vol spécifiée et l’objectif d’impression.
>
>* Si la diffusion est en sous-ou en trop-rythme, contactez votre éditeur pour ajuster le volume qu’elle envoie via l’offre.

>[!MORELIKETHIS]
>
>* [Paramètres d’ID de transaction manuelle](deal-id-settings.md)
>* [Configuration d’une transaction sécurisée par programmation](programmatic-guaranteed-set-up.md)
>* [Envoyer une publicité pour une transaction avec programme garanti avec [!DNL FreeWheel]](freewheel-submit.md)
>* [À propos des transactions garanties par programmation](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
