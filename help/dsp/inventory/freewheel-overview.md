---
title: Présentation de la configuration des contrats PG dans [!DNL Freewheel]
description: Découvrez les conditions préalables et les étapes supplémentaires nécessaires à l’exécution de publicités pour des offres garanties par programmation avec les éditeurs sur [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# Présentation de la configuration de transactions garanties par la programmation dans [!DNL Freewheel]

Configuration d’offres garanties par la programmation avec les éditeurs sur [!DNL Freewheel] nécessite des autorisations et des étapes supplémentaires.

>[!PREREQUISITES]
>
>Collaborez avec votre équipe de compte d’Adobe pour vous assurer que votre [!DNL DSP] compte dispose des autorisations suivantes :
>
>* Autorisation d’utiliser la variable [!DNL FreeWheel] workflow garanti par la programmation, qui est requis pour envoyer une publicité pour une offre garantie par la programmation à [!DNL FreeWheel].
>
>* (Si vous travaillez avec des éditeurs britanniques qui ont besoin d’une [!DNL Clearcast] numéro de l’horloge avec chaque publicité) Autorisation d’inclure les numéros de l’horloge dans vos publicités.


## Workflow

1. Créez une publicité avec le type de média spécifié dans l’opération.

   Pour certains éditeurs britanniques, vous devez inclure une [!DNL Clearcast] numéro de l’horloge avec votre publicité.

1. [Acceptation de l’ID de transaction](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) que vous avez déjà négocié avec un éditeur le [!DNL Freewheel] à l’aide de la boîte de réception Deal ID.

   Une fois que vous avez accepté l’offre, suivez les invites à 1) sélectionnez la publicité à utiliser pour l’offre et 2) créez un emplacement par défaut garanti par programme pour diffuser l’annonce.

1. [Envoyer la publicité à [!DNL Freewheel]](freewheel-submit.md)

   La publicité doit être envoyée et approuvée avant son exécution.

1. [Vérification de l’état d’envoi de la publicité](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Acceptation d’une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Envoyer une publicité pour une transaction garantie par un programme à [!DNL Freewheel]](freewheel-submit.md)
>* [Vérification de l’état des publicités pour [!DNL FreeWheel] Offres garanties par la programmation](freewheel-check-status.md)
>* [Codes d’erreur pour [!DNL Freewheel] Envois de publicités](freewheel-error-codes.md)

