---
title: Envoyer une publicité pour une transaction PG à  [!DNL FreeWheel]
description: Découvrez comment demander l’approbation d’une publicité pour une transaction garantie par un programme avec un éditeur sur  [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Envoyer une publicité pour une transaction gérée par programmation à [!DNL Freewheel]

*Comptes avec l’autorisation [!DNL FreeWheel] Programmatic Guaranteed only*

Une fois que vous [acceptez une offre garantie par programmation avec un éditeur sur FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), y compris la sélection d’une publicité et la création de l’emplacement par défaut garanti par programmation à utiliser pour l’offre, vous devez envoyer la publicité à [!DNL Freewheel] pour approbation.

>[!PREREQUISITES]
>
>Collaborez avec votre équipe de compte d’Adobe pour vous assurer que votre compte [!DNL DSP] est autorisé à utiliser le workflow garanti par la programmation [!DNL FreeWheel].

1. Copiez la clé publicitaire de la publicité utilisée avec la transaction [!DNL Freewheel] :

   1. Cliquez sur le nom de la campagne.

   1. Dans le sous-menu, cliquez sur **[!UICONTROL Ads]**.

   1. Cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]** en regard du nom de la publicité.

   1. Une fois les paramètres de publicité ouverts, copiez la clé publicitaire alphanumérique dans l’URL qui s’affiche dans la barre d’adresse du navigateur.

      Par exemple, dans l’URL suivante, la clé publicitaire est `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Envoyez la publicité à [!DNL Freewheel] :

   1. Effectuez l’une des opérations suivantes :

      * En regard du nom de la publicité, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Sur la ligne de la transaction, cliquez sur ![Menu Options](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Vérifiez l’ID de l’opération, saisissez le **[!UICONTROL Ad Key]** que vous avez copié à l’étape 1, puis cliquez sur **[!UICONTROL Submit]**.

   La publicité doit être envoyée et approuvée avant son exécution.

1. [Vérifiez l’état d’envoi de la publicité](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Présentation de la configuration de transactions garanties par programmation dans [!DNL Freewheel]](freewheel-overview.md)
>* [Accepter une transaction dans la boîte de réception Deal ID](deal-id-inbox-accept.md)
>* [Vérifiez l’état des publicités pour les  [!DNL FreeWheel] affaires programmatiques garanties](freewheel-check-status.md)
>* [Codes d’erreur pour [!DNL Freewheel] Envois de publicité](freewheel-error-codes.md)
