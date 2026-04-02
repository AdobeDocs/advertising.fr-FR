---
title: Configurer une offre programmatique garantie
description: Découvrez comment configurer un contrat programmatique garanti (PG) que vous avez négocié avec un éditeur.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
TQID: https://experienceleague.adobe.com/z7kz7dnCjgCGmlgDlFvbZXTn8d9-OMEunv-Sm-k6TzY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# Configurer une offre programmatique garantie

*[Plateformes côté offre prises en charge uniquement](programmatic-guaranteed-about.md)*

Après avoir négocié une transaction programmatique garantie (PG) avec un éditeur pris en charge, vous pouvez configurer la transaction dans DSP à l’aide du [!DNL Deal ID Inbox] ou en saisissant manuellement les détails de la transaction.

>[!NOTE]
>
> Pour les offres PG, l’éditeur gère l’ensemble du rythme budgétaire, de la limitation du budget et du ciblage. Tous les SSP qui autorisent PG via DSP confirment que l’éditeur peut configurer la limitation du budget.
>
> La configuration d’offres programmatiques garanties avec les éditeurs sur [!DNL FreeWheel] nécessite des autorisations et des étapes supplémentaires. Pour plus d’informations, consultez « [Présentation de la configuration d’offres programmatiques garanties dans [!DNL FreeWheel]](freewheel-overview.md) ».

## Configurer une offre programmatique garantie à l’aide du [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

La méthode suivante est la procédure privilégiée pour [!DNL FreeWheel], [!DNL Google Authorized Buyers] et [!DNL Magnite DV+].

1. [Acceptez le contrat](deal-id-inbox-accept.md).

1. Après avoir enregistré l’offre, sélectionnez les annonces (ou le pixel de suivi 1x1 pour les annonces gérées par l’éditeur) à utiliser pour l’offre et créez un emplacement par défaut programmatique garanti (PG), comme vous y êtes invité.

   La création d’un placement PG par défaut pour l’offre est obligatoire pour diffuser 100 % de votre achat. Ce type d’emplacement ne dispose d’aucun ciblage. DSP peut donc renvoyer une offre à chaque demande d’offre de l’éditeur.

   * Si vous acceptez une seule offre, vous êtes automatiquement redirigé vers le workflow de création d’emplacement par défaut de PG.

     Toutes les offres [!DNL FreeWheel] sont proposées comme une seule offre.

   * Si vous acceptez une proposition avec plusieurs ID d’offre PG, identifiez chaque emplacement PG par défaut que vous devez créer. Une fois que vous avez créé tous les emplacements requis, le bouton Continuer est activé.

1. (Facultatif) Ciblez l’offre PG dans des emplacements PG ou non PG supplémentaires en cliquant sur ![menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Une offre peut cibler plusieurs emplacements prenant en charge n’importe quelle combinaison de types de médias (télévision connectée, ordinateur de bureau et audio, par exemple).

## Configurer manuellement une offre programmatique garantie

Utilisez cette méthode pour tous les autres SSP.

1. [Configurez manuellement les détails de l’ID d’offre](deal-id-create.md).

1. Après avoir enregistré l’offre, sélectionnez les annonces (ou 1x1 pixels de suivi pour les annonces gérées par l’éditeur) à utiliser pour l’offre et créez un emplacement par défaut PG, comme vous y êtes invité.

   La création d&#39;un placement PG par défaut pour l&#39;offre est obligatoire pour livrer 100 % de votre achat. Ce type d’emplacement ne dispose d’aucun ciblage. DSP peut donc renvoyer une offre à chaque demande d’offre de l’éditeur.

1. (Facultatif) Ciblez l’offre PG dans des emplacements PG ou non PG supplémentaires en cliquant sur ![menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Une offre peut cibler plusieurs emplacements prenant en charge n’importe quelle combinaison de types de médias (télévision connectée, ordinateur de bureau et audio, par exemple).

>[!MORELIKETHIS]
>
>* [À propos des offres programmatiques garanties](programmatic-guaranteed-about.md)
>* [Conseils pour négocier un contrat programmatique garanti](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Soumettre une annonce pour un contrat programmatique garanti avec  [!DNL FreeWheel]](freewheel-submit.md)
>* [Accepter une offre dans le [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Créer manuellement les détails de l’ID d’offre](deal-id-create.md)
>* [Partenaires SSP](ssp-partners.md)
>* [Présentation des fonctionnalités d’inventaire dans Advertising DSP](inventory-overview.md)
