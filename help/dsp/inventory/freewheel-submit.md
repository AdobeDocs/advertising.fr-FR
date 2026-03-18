---
title: Envoyez une annonce pour une offre PG à  [!DNL FreeWheel]
description: Découvrez comment demander l’approbation d’une publicité pour une offre programmatique garantie avec un éditeur le  [!DNL Freewheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 4264d6032a8d31004e66fd4ee033d9ecd51918c8
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# Envoyer une annonce pour une offre programmatique garantie à [!DNL Freewheel]

*Comptes avec l’autorisation Programmatique Garantie [!DNL FreeWheel] uniquement*

Une fois que vous [acceptez une offre programmatique garantie avec un éditeur sur FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox), y compris en sélectionnant une annonce et en créant l’emplacement par défaut programmatique garanti à utiliser pour l’offre, vous devez soumettre l’annonce à [!DNL Freewheel] pour approbation.

>[!PREREQUISITES]
>
>Contactez l’équipe chargée de votre compte Adobe pour vous assurer que votre compte [!DNL DSP] est autorisé à utiliser le workflow programmatique garanti [!DNL FreeWheel].

1. Copiez la clé de l’annonce publicitaire utilisée avec l’offre [!DNL Freewheel] :

   1. Cliquez sur le nom de la campagne.

   1. Dans le sous-menu, cliquez sur **[!UICONTROL Ads]**.

   1. Cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Edit]** en regard du nom de l’annonce publicitaire.

   1. Une fois les paramètres d’annonce ouverts, copiez la clé d’annonce alphanumérique dans l’URL affichée dans la barre d’adresse du navigateur.

      Par exemple, dans l’URL suivante, la clé publicitaire est `3NtNC5ZbaGZtqbei8jD3`

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. Envoyez l’annonce à [!DNL Freewheel] :

   1. Effectuez l’une des opérations suivantes :

      * En regard du nom de l’annonce publicitaire, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**.

      * Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals]**. Dans la ligne d&#39;offre, cliquez sur ![menu Options](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]**.

   1. Vérifiez l&#39;ID d&#39;opération, saisissez le **[!UICONTROL Ad Key]** que vous avez copié à l&#39;étape 1, puis cliquez sur **[!UICONTROL Submit]**.

   La publicité doit être soumise et approuvée avant son exécution.

1. [Vérifiez le statut d’envoi de l’annonce](freewheel-check-status.md).

>[!MORELIKETHIS]
>
>* [Présentation de la configuration d&#39;affaires programmatiques garanties dans [!DNL Freewheel]](freewheel-overview.md)
>* [Accepter une offre dans la boîte de réception des ID d’offres](deal-id-inbox-accept.md)
>* [Vérifier le statut des publicités pour les offres programmatiques garanties [!DNL FreeWheel] &#x200B;](freewheel-check-status.md)
>* [Codes d’erreur pour les envois  [!DNL Freewheel]  publicités](freewheel-error-codes.md)
