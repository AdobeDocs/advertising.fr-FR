---
title: À propos du [!UICONTROL Deal ID Inbox]
description: Découvrez la fonctionnalité [!UICONTROL Deal ID inbox], qui vous permet d’accepter des offres privées que vous avez déjà négociées avec des éditeurs sur  [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anciennement appelé  [!DNL AdX]), and [!DNL Magnite DV+] (anciennement [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 394a281c9b9d7eeab939f4c58508ec1f34eba67c
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# À propos du [!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox] vous permet de configurer rapidement les offres que DSP a importées des éditeurs par le biais de plateformes côté offre (SSP) afin de ne pas avoir à configurer manuellement chaque offre. Vous pouvez accepter les contrats d&#39;inventaire privé garantis et non garantis que vous avez déjà négociés avec des éditeurs sur [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anciennement appelé [!DNL AdX]) et [!DNL Magnite DV+] (anciennement [!DNL Rubicon]) à partir de [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP est le premier DSP à s’intégrer à l’API [!DNL FreeWheel].

Dans le [!UICONTROL Deal ID inbox], vous pouvez voir les détails de l’opération tels que votre éditeur les voit, accélérer la configuration de l’opération et éviter les erreurs de saisie manuelle.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP actualise automatiquement tous les détails de l’offre tous les jours à 4 h 30 (heure de Paris). Elle actualise également toutes les offres [!DNL FreeWheel] et met à jour les offres existantes toutes les [!DNL Google] et [!DNL Magnite DV+] heures. Vous pouvez également actualiser manuellement les détails de l’opération pour renseigner les nouvelles opérations à tout moment.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->

>[!NOTE]
>
>Pour les offres programmatiques garanties via [!DNL Google Authorized Buyers], vous devez respecter au moins 90 % de votre budget ou votre compte perd l’accès aux offres [!DNL Google] dans le [!UICONTROL Deal ID inbox].

## Mise en œuvre de l’[!UICONTROL Deal ID Inbox]

Pour recevoir vos offres dans le [!UICONTROL Deal ID inbox], vos comptes SSP doivent mapper le compte DSP de votre organisation à votre compte SSP. DSP peut partager les noms de compte de l’organisation avec les fournisseurs de services partagés concernés. Pour obtenir des instructions, contactez l’équipe chargée de votre compte Adobe.

Lors des négociations de l’offre, indiquez à l’éditeur d’envoyer l’offre à votre acheteur plutôt qu’au compte DSP parent. L’identifiant de l’offre peut être un nom ou un identifiant, selon le fournisseur de services partagés.

## Actions que vous pouvez entreprendre concernant vos affaires

* **Consultez les offres** pour vérifier que le SSP a envoyé l&#39;éditeur correct, les dates de vol, CPM et d&#39;autres détails de l&#39;offre. Si l’éditeur a commis une erreur, contactez-le en dehors de DSP afin qu’il puisse corriger et renvoyer le contrat.

* **Acceptez les offres** après révision, et elles n’apparaissent plus dans le [!UICONTROL Deal ID inbox]. Les offres acceptées sont répertoriées dans [!UICONTROL Inventory] > [!UICONTROL Deals] et sont prêtes à être ciblées dans les emplacements des annonceurs.

* **Ignorer les offres** qui ne sont pas nécessaires ou qui ne sont pas sollicitées. Les offres ignorées sont déplacées vers l’onglet [!UICONTROL Ignored Deals] de la [!UICONTROL Deal ID inbox], qui sert d’archive. DSP n’alerte pas les fournisseurs de services partagés et les éditeurs lorsque vous ignorez une transaction.

* **Modifiez les détails des offres déjà acceptées** à partir de [!UICONTROL Inventory] > [!UICONTROL Deals] (pas dans le [!UICONTROL Deal ID inbox]). De même, lorsque les éditeurs envoient des modifications aux offres, les annonceurs sont responsables de l’implémentation de ces modifications dans [!UICONTROL Inventory] > [!UICONTROL Deals], car l’[!UICONTROL Deal ID inbox] ne synchronise pas les modifications à partir des SSP une fois les offres configurées.

## Quels types de contrats ne peuvent pas être acceptés ?

Lorsqu’une liste d’offres n’inclut pas d’icône ![Accepter](/help/dsp/assets/accept.png) ou de bouton [!UICONTROL Accept], vous ne pouvez pas l’accepter à partir du [!UICONTROL Deal ID inbox]. Au lieu de cela, vous pouvez [créer manuellement les détails de l’ID d’offre](/help/dsp/inventory/deal-id-create.md).

Vous ne pouvez pas accepter les types d&#39;offres suivants :

* [!DNL Google] les offres qui ne sont pas en USD.

* [!DNL Magnite DV+] les offres qui ne sont pas en USD

* [!DNL FreeWheel] des transactions qui ne sont pas dans la devise de votre compte.

* Affaires dont la date de fin est antérieure à aujourd’hui.

* Anciennes offres [!DNL Magnite DV+] libellées comme « types de médias multiples ».

Les détails de l’opération incluent la raison pour laquelle l’opération n’est pas disponible pour acceptation.

>[!MORELIKETHIS]
>
>* [Accepter une offre dans la boîte de réception des ID d’offres](deal-id-inbox-accept.md)
>* [Présentation des fonctions d&#39;inventaire](inventory-overview.md)
