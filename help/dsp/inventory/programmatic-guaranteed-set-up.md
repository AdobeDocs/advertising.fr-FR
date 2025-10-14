---
title: Configuration d’un contrat garanti programmatique
description: Découvrez comment configurer un contrat PG garanti par programmation que vous avez négocié avec un éditeur.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Configuration d’un contrat garanti programmatique

*[Plateformes côté offre prises en charge uniquement](programmatic-guaranteed-about.md)*

Après avoir négocié une transaction (PG) garantie par un programme avec un éditeur pris en charge, vous pouvez configurer l’opération dans DSP en utilisant l’ [!DNL Deal ID inbox] ou en saisissant manuellement les détails de l’opération.

>[!NOTE]
>
> Pour les offres PG, l’éditeur gère l’intégralité des opérations d’ajustement du budget, de limitation du budget et de ciblage. Tous les SSP qui autorisent PG par DSP confirment que l’éditeur peut configurer la limitation du budget.
>
> La configuration d’offres garanties par la programmation avec les éditeurs sur [!DNL FreeWheel] nécessite des autorisations et des étapes supplémentaires. Pour plus d’informations, voir &quot;[Présentation de la configuration des transactions garanties par programmation dans [!DNL FreeWheel]](freewheel-overview.md)&quot;.

## Configurez une transaction sécurisée par programmation à l’aide de [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

La méthode suivante est la méthode préférée pour [!DNL FreeWheel], [!DNL Google Authorized Buyers] et [!DNL Magnite DV+].

1. [Acceptez l’opération](deal-id-inbox-accept.md).

1. Après avoir enregistré l’opération, sélectionnez les publicités (ou 1x1 pixel de suivi pour les publicités gérées par l’éditeur) à utiliser pour l’opération et créez un emplacement par défaut garanti par programmation (PG), comme vous y êtes invité.

   La création d’un emplacement PG par défaut pour l’opération est obligatoire pour diffuser 100 % de votre achat. Ce type d’emplacement n’a pas de ciblage, DSP peut donc renvoyer une offre à chaque demande d’offre de l’éditeur.

   * Si vous acceptez une seule transaction, vous êtes automatiquement redirigé vers le workflow de création d’emplacements par défaut PG.

     Tous les [!DNL FreeWheel] contrats sont proposés comme un seul et même contrat.

   * Si vous acceptez une proposition avec plusieurs ID de transaction PG, identifiez chaque emplacement par défaut PG que vous devez créer. Une fois tous les emplacements requis créés, le bouton Continuer est activé.

1. (Facultatif) Ciblez l’opération PG dans des emplacements PG ou non PG supplémentaires en cliquant sur ![Menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Une transaction peut cibler plusieurs emplacements qui prennent en charge n’importe quelle combinaison de types de médias (comme la télévision connectée, le bureau et l’audio).

## Configuration manuelle d’une transaction sécurisée par programmation

Utilisez cette méthode pour tous les autres SSP.

1. [&#x200B; Configurez manuellement les détails de l’ID de transaction &#x200B;](deal-id-create.md).

1. Une fois l’opération enregistrée, sélectionnez les publicités (ou pixels de suivi 1x1 pour les publicités gérées par l’éditeur) à utiliser pour l’opération et créez un emplacement par défaut PG, le cas échéant.

   La création d’un emplacement par défaut PG pour l’opération est obligatoire pour diffuser 100 % de votre achat. Ce type d’emplacement n’a pas de ciblage, DSP peut donc renvoyer une offre à chaque demande d’offre de l’éditeur.

1. (Facultatif) Ciblez l’opération PG dans des emplacements PG ou non PG supplémentaires en cliquant sur ![Menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Une transaction peut cibler plusieurs emplacements qui prennent en charge n’importe quelle combinaison de types de médias (comme la télévision connectée, le bureau et l’audio).

>[!MORELIKETHIS]
>
>* [À propos des transactions garanties par programmation](programmatic-guaranteed-about.md)
>* [Conseils pour négocier un accord garanti par un programme](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Envoyer une publicité pour une transaction avec programme garanti avec [!DNL FreeWheel]](freewheel-submit.md)
>* [Accepter une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Créer manuellement des détails sur l’identifiant de transaction](deal-id-create.md)
>* [Partenaires SSP](ssp-partners.md)
>* [Présentation des fonctionnalités d’inventaire](inventory-overview.md)
