---
title: Envoyez une annonce pour une offre PG à  [!DNL FreeWheel]
description: Découvrez comment demander l’approbation d’une publicité pour une offre programmatique garantie avec un éditeur le  [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Envoyer une annonce pour une offre programmatique garantie à [!DNL FreeWheel]

*Comptes avec l’autorisation Programmatique Garantie [!DNL FreeWheel] uniquement*

Une fois que vous [acceptez une offre programmatique garantie avec un éditeur sur FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), y compris en sélectionnant une annonce et en créant l’emplacement par défaut programmatique garanti à utiliser pour l’offre, vous devez soumettre l’annonce à [!DNL FreeWheel] pour approbation.

>[!PREREQUISITES]
>
>Contactez l’équipe chargée de votre compte Adobe pour vous assurer que votre compte [!DNL DSP] est autorisé à utiliser le workflow programmatique garanti [!DNL FreeWheel].

1. Copiez la clé de l’annonce publicitaire utilisée avec l’offre [!DNL FreeWheel] :

   1. Cliquez sur le nom de la campagne.

   1. Dans le sous-menu, cliquez sur **[!UICONTROL Ads]**.

   1. Cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]** en regard du nom de l’annonce publicitaire.

   1. Une fois les paramètres d’annonce ouverts, copiez la clé d’annonce alphanumérique dans l’URL affichée dans la barre d’adresse du navigateur.

      Par exemple, dans l’URL suivante, la clé publicitaire est `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Envoyez l’annonce à [!DNL FreeWheel] :

   1. Effectuez l’une des opérations suivantes :

      * En regard du nom de l’annonce publicitaire, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Dans la ligne d&#39;offre, cliquez sur ![menu Options](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Vérifiez l&#39;ID d&#39;opération, saisissez le **[!UICONTROL Ad Key]** que vous avez copié à l&#39;étape 1, puis cliquez sur **[!UICONTROL Submit]**.

   La publicité doit être soumise et approuvée avant son exécution.

1. [Vérifiez le statut d’envoi de l’annonce](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Présentation de la configuration d’offres programmatiques garanties dans  [!DNL FreeWheel]](freewheel-overview.md)
>* [Accepter une offre dans le [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Consultez le statut des publicités pour une offre  [!DNL FreeWheel] PG](freewheel-check-status.md)
>* [Codes d’erreur pour les envois  [!DNL FreeWheel]  publicités](freewheel-error-codes.md)
