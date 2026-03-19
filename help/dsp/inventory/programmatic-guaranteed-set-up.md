---
title: Configurer une offre programmatique garantie
description: Découvrez comment configurer un contrat programmatique garanti (PG) que vous avez négocié avec un éditeur.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 54f69e4c0fa20b918a037cc5d2003d67db889913
workflow-type: tm+mt
source-wordcount: '452'
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
