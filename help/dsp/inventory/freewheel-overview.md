---
title: Présentation de la configuration des contrats PG dans  [!DNL Freewheel]
description: Découvrez les conditions préalables et les étapes supplémentaires nécessaires à l’exécution de publicités pour des offres garanties par la programmation avec les éditeurs sur  [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 0%

---

# Présentation de la configuration de transactions garanties par la programmation dans [!DNL Freewheel]

La configuration d’offres garanties par la programmation avec les éditeurs sur [!DNL Freewheel] nécessite des autorisations et des étapes supplémentaires.

>[!PREREQUISITES]
>
>Consultez votre équipe de compte d’Adobe pour vous assurer que votre compte [!DNL DSP] dispose des autorisations suivantes :
>
>* Autorisation d’utiliser le workflow garanti par la programmation [!DNL FreeWheel], nécessaire pour envoyer une publicité pour une offre garantie par la programmation à [!DNL FreeWheel].
>
>* (Si vous travaillez avec des éditeurs britanniques qui ont besoin d’un numéro d’horloge [!DNL Clearcast] avec chaque publicité) Autorisation d’inclure des numéros d’horloge dans vos publicités.

## Workflow

1. Créez une publicité avec le type de média spécifié dans l’opération.

   Pour certains éditeurs britanniques, vous devez inclure un numéro d’horloge [!DNL Clearcast] à votre publicité.

1. [Acceptez l’ID de transaction](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) que vous avez déjà négocié avec un éditeur sur [!DNL Freewheel] à l’aide de la boîte de réception Deal ID.

   Une fois que vous avez accepté l’offre, suivez les invites à 1) sélectionnez la publicité à utiliser pour l’offre et 2) créez un emplacement par défaut garanti par programme pour diffuser l’annonce.

1. [Envoyer la publicité à [!DNL Freewheel]](freewheel-submit.md)

   La publicité doit être envoyée et approuvée avant son exécution.

1. [Vérifiez l’état d’envoi de la publicité](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Accepter une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Envoyer une publicité pour une transaction GARANTIE programmatique à [!DNL Freewheel]](freewheel-submit.md)
>* [Vérifiez l’état des publicités pour les  [!DNL FreeWheel] affaires programmatiques garanties](freewheel-check-status.md)
>* [Codes d’erreur pour [!DNL Freewheel] Envois de publicité](freewheel-error-codes.md)
