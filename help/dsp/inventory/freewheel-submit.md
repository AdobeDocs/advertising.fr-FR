---
title: Envoyez une annonce pour une offre PG à  [!DNL FreeWheel]
description: Découvrez comment demander l’approbation d’une publicité pour une offre programmatique garantie avec un éditeur le  [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
TQID: https://experienceleague.adobe.com/f6Cu6mG77YOjwshI4xVbkLSkykAhqXonfSMg5ynDK5g
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 237
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
