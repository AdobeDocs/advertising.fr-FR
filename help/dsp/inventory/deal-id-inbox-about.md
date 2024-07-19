---
title: À propos de [!UICONTROL Deal ID Inbox]
description: Découvrez la fonctionnalité [!UICONTROL Deal ID inbox], qui vous permet d’accepter des offres privées que vous avez déjà négociées avec les éditeurs sur  [!DNL FreeWheel], [!DNL Google Authorized Buyers]  (anciennement appelé [!DNL AdX]), and [!DNL Magnite DV+] (anciennement [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# À propos de [!UICONTROL Deal ID Inbox]

Advertising DSP [!UICONTROL Deal ID inbox] vous permet de configurer rapidement des offres que DSP a importées depuis des éditeurs via des plateformes côté offre (SSP) afin que vous n’ayez pas à configurer chaque opération manuellement. Vous pouvez accepter les offres d’inventaire privé garanties et non garanties que vous avez déjà négociées avec les éditeurs sur [!DNL FreeWheel], [!DNL Google Authorized Buyers] (anciennement appelé [!DNL AdX]) et [!DNL Magnite DV+] (anciennement [!DNL Rubicon]) à partir de [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSP est la première DSP à intégrer à l’API [!DNL FreeWheel].

Dans le [!UICONTROL Deal ID inbox], vous pouvez voir les détails de l’opération à mesure que votre éditeur les voit, accélérer la configuration de l’opération et éviter les erreurs de saisie manuelle.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP actualise automatiquement tous les détails de la transaction tous les jours à 4 h 30 HNE. Il actualise également toutes les [!DNL FreeWheel] offres et met à jour les offres existantes à partir des [!DNL Google] et [!DNL Magnite DV+] toutes les heures. Vous pouvez également actualiser manuellement les détails de l’opération pour renseigner à tout moment les nouvelles offres.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Pour les offres garanties par la programmation via [!DNL Google Authorized Buyers], vous devez exécuter au moins 90 % de votre budget, sinon votre compte ne peut plus accéder aux [!DNL Google] offres dans [!UICONTROL Deal ID inbox].

## Implémentation de [!UICONTROL Deal ID Inbox]

Pour recevoir vos offres dans [!UICONTROL Deal ID inbox], vos comptes SSP doivent mapper le compte DSP de votre organisation à votre compte SSP. DSP peut partager les noms de compte de l’organisation avec les SSP appropriés. Contactez votre équipe de compte d’Adobe pour obtenir des instructions.

Pendant les négociations de l’opération, demandez à l’éditeur d’envoyer l’opération à votre acheteur au lieu du compte DSP parent. L’identifiant de l’opération peut être un nom ou un identifiant, selon le SSP.

## Actions possibles sur vos transactions

* **Consultez les offres** pour vérifier que le fournisseur de services de messagerie a envoyé l’éditeur, les dates de vol, le CPM et d’autres détails sur l’opération corrects. Si l’éditeur a commis une erreur, contactez-les en dehors de DSP afin qu’il puisse corriger et renvoyer l’opération.

* **Acceptez les transactions** après révision et elles n’apparaissent plus dans le [!UICONTROL Deal ID inbox]. Les offres acceptées sont répertoriées dans [!UICONTROL Inventory] > [!UICONTROL Deals] et sont prêtes à être ciblées dans les emplacements des annonceurs.

* **Ignorer les transactions** qui ne sont pas nécessaires ou qui ne sont pas sollicitées. Les offres ignorées sont déplacées vers l’onglet [!UICONTROL Ignored Deals] dans [!UICONTROL Deal ID inbox], qui sert d’archive. DSP n’alerte pas les SSP et les éditeurs lorsque vous ignorez une transaction.

* **Modifiez les détails des offres déjà acceptées** à partir de [!UICONTROL Inventory] > [!UICONTROL Deals] (et non dans [!UICONTROL Deal ID inbox]). De même, lorsque les éditeurs envoient des modifications aux offres, les annonceurs sont responsables de l’implémentation de ces modifications dans [!UICONTROL Inventory] > [!UICONTROL Deals], car [!UICONTROL Deal ID inbox] ne synchronise pas les modifications des SSP une fois les offres configurées.

## Quels types d&#39;accords ne peuvent être acceptés ?

Lorsqu&#39;une liste d&#39;offres ne contient pas d&#39;icône ![Accept](/help/dsp/assets/accept.png) ni de bouton [!UICONTROL Accept], vous ne pouvez pas l&#39;accepter à partir de [!UICONTROL Deal ID inbox]. Au lieu de cela, vous pouvez [créer manuellement les détails de l’ID de transaction](/help/dsp/inventory/deal-id-create.md).

Vous ne pouvez pas accepter les types d’offres suivants :

* [!DNL Google] offres qui ne sont pas en USD.

* [!DNL Magnite DV+] offres qui ne sont pas en USD

* [!DNL FreeWheel] offres qui ne sont pas dans la devise de votre compte.

* Offres dont la date de fin est antérieure à aujourd’hui.

* Les [!DNL Magnite DV+] anciens contrats étiquetés &quot;types de médias multiples&quot;.

Les détails de l’accord incluent la raison pour laquelle l’accord n’est pas disponible.

>[!MORELIKETHIS]
>
>* [Accepter une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Présentation des fonctionnalités d’inventaire](inventory-overview.md)
