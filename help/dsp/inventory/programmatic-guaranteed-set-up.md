---
title: Configuration d’un contrat garanti programmatique
description: Découvrez comment configurer un contrat PG garanti par programmation que vous avez négocié avec un éditeur.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: b1a772acbd9b934f2b4679d1111d56e1059e0cca
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 0%

---

# Configuration d’un contrat garanti programmatique

*[Plateformes côté offre prises en charge uniquement](programmatic-guaranteed-about.md)*

Après avoir négocié une transaction (PG) garantie par un programme avec un éditeur pris en charge, vous pouvez configurer l’opération dans DSP en utilisant la variable [!DNL Deal ID inbox] ou en saisissant manuellement les détails de l’opération.

>[!NOTE]
>
> Pour les offres PG, l’éditeur gère l’intégralité des opérations d’ajustement du budget, de limitation du budget et de ciblage. Tous les SSP qui autorisent PG par DSP confirment que l’éditeur peut configurer la limitation du budget.
>
> Configuration d’offres garanties par la programmation avec les éditeurs sur [!DNL FreeWheel] nécessite des autorisations et des étapes supplémentaires. Voir &quot;[Présentation de la configuration de transactions garanties par la programmation dans [!DNL FreeWheel]](freewheel-overview.md)&quot; pour plus d’informations.

## Configuration d’une transaction sécurisée par programmation à l’aide de la variable [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

La méthode suivante est la procédure recommandée pour [!DNL FreeWheel], [!DNL Google Authorized Buyers], et [!DNL Magnite DV+].

1. [Accepter l&#39;accord](deal-id-inbox-accept.md).

1. Après avoir enregistré l’opération, sélectionnez les publicités (ou 1x1 pixel de suivi pour les publicités gérées par l’éditeur) qui seront utilisées pour l’opération et créez un emplacement par défaut garanti par programmation (PG), comme vous y êtes invité.

   La création d’un emplacement PG par défaut pour l’opération est obligatoire pour diffuser 100 % de votre achat. Ce type d’emplacement n’a pas de ciblage, DSP peut donc renvoyer une offre à chaque demande d’offre de l’éditeur.

   * Si vous acceptez une seule transaction, vous êtes automatiquement redirigé vers le workflow de création d’emplacements par défaut PG.

     Tous [!DNL FreeWheel] les accords sont proposés comme un accord unique.

   * Si vous acceptez une proposition avec plusieurs ID de transaction PG, identifiez chaque emplacement par défaut PG que vous devez créer. Une fois tous les emplacements requis créés, le bouton Continuer est activé.

1. (Facultatif) Ciblez l’opération PG dans des emplacements PG ou autres en cliquant sur ![Menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Une transaction peut cibler plusieurs emplacements qui prennent en charge n’importe quelle combinaison de types de médias (comme la télévision connectée, le bureau et l’audio).

## Configuration manuelle d’une transaction sécurisée par programmation

Utilisez cette méthode pour tous les autres SSP.

1. [Configuration manuelle des détails de l’ID de transaction](deal-id-create.md).

1. Une fois l’opération enregistrée, sélectionnez les publicités (ou 1x1 pixel de suivi pour les publicités gérées par l’éditeur) qui seront utilisées pour l’opération et créez un emplacement par défaut PG, le cas échéant.

   La création d’un emplacement par défaut PG pour l’opération est obligatoire pour diffuser 100 % de votre achat. Ce type d’emplacement n’a pas de ciblage, DSP peut donc renvoyer une offre à chaque demande d’offre de l’éditeur.

1. (Facultatif) Ciblez l’opération PG dans des emplacements PG ou autres en cliquant sur ![Menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Une transaction peut cibler plusieurs emplacements qui prennent en charge n’importe quelle combinaison de types de médias (comme la télévision connectée, le bureau et l’audio).

>[!MORELIKETHIS]
>
>* [A propos des contrats garantis par programmation](programmatic-guaranteed-about.md)
>* [Conseils pour négocier un accord garanti programmatique](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Envoyer une publicité pour une transaction sécurisée par programmation [!DNL FreeWheel]](freewheel-submit.md)
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Création manuelle des détails de l’identifiant de transaction](deal-id-create.md)
>* [Partenaires SSP](ssp-partners.md)
>* [Présentation des fonctionnalités du stock](inventory-overview.md)
