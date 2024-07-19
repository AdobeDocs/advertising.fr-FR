---
title: Créer une transaction [!UICONTROL Simple Ad Serving]
description: Découvrez comment créer un pixel de suivi pour une transaction [!UICONTROL Simple Ad Serving].
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Créer une transaction [!UICONTROL Simple Ad Serving]

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**, puis sélectionnez **[!UICONTROL Simple Ad Serving]**.

1. Saisissez les [paramètres de transaction](simple-deal-settings.md) :

   1. Dans la section [!UICONTROL Select Ad Source] , spécifiez des informations sur l’éditeur, l’annonceur et la campagne, ainsi que le type d’annonce, puis cliquez sur **[!UICONTROL Next]**.

   1. Dans la section [!UICONTROL Select Ad(s)] , spécifiez une publicité à utiliser comme proxy dans DSP :

      1. Effectuez l’une des opérations suivantes :

         * Pour les annonces existantes, sélectionnez les annonces à utiliser.

         * Pour les nouvelles publicités, créez un proxy [publicité tierce](/help/dsp/campaign-management/ads/ad-create-multiple.md).

      >[!NOTE]
      > DSP ne diffuse pas les publicités que vous spécifiez. L’éditeur diffuse la publicité.

      1. Cliquez sur **[!UICONTROL Next]**.

   1. Dans les détails du flux, modifiez les détails du flux, puis cliquez sur **[!UICONTROL Next]**.

      DSP génère automatiquement un emplacement, nommé &quot;Emplacement SAS - &lt;*nom de l’offre*>&quot; pour la publicité. Dans l’emplacement, l’opération est automatiquement ciblée dans la section [!UICONTROL Inventory Targets] . Toutes les autres options de ciblage ne sont pas applicables.

1. Envoyez les pixels de suivi d’événement à l’éditeur pour implémentation de l’une des façons suivantes :

   * (Facultatif) Dans l’écran [!UICONTROL Activate Tag with Publisher], envoyez la balise de transaction à l’éditeur.

     Une fois les étapes précédentes terminées, DSP génère un message électronique que vous pouvez envoyer à l’éditeur. Le message comprend les détails de la transaction, un lien à partir duquel récupérer la balise de la transaction et un code d’autorisation pour le lien.

      1. Vérifiez les détails de l’opération, puis effectuez l’une des opérations suivantes :

         * Pour coller les informations dans un message électronique dans une application de messagerie sur votre appareil, cliquez sur **[!UICONTROL Email & Done]** et sélectionnez l’application de messagerie. Le champ [!UICONTROL CC:] est prérenseigné avec une adresse de support [!DNL Adobe]. Vous pouvez ensuite envoyer le message au contact approprié pour l’éditeur.

         * Pour copier les informations dans le presse-papiers, cliquez sur **[!UICONTROL Copy Email].** Vous pouvez ensuite coller manuellement le contenu dans un email et l’envoyer au contact approprié de l’éditeur. Vous devez inclure une copie (CC :) vers `publisher-support-global@adobe.com`. Lorsque vous avez terminé de copier le message, cliquez sur **[!UICONTROL Email & Done]**.

      1. (Si nécessaire) Vérifiez auprès de l’éditeur si la balise contient les macros appropriées afin qu’elle fonctionne avec le serveur d’annonces de l’éditeur.

   * (Facultatif) Envoyez manuellement les pixels de suivi d’événement à l’éditeur :

      1. Dans la ligne de la transaction dans la vue [!UICONTROL Deals], cliquez sur ![Menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Les pixels d’événement incluent un pixel [!UICONTROL Clickthrough] et un pixel [!UICONTROL Impression]. Les publicités vidéo et audio incluent également les pixels d’événement par quartile terminé (de [!UICONTROL 25% Complete] à [!UICONTROL 100% Complete]).

      1. Copiez les pixels de suivi d’événement et fournissez-les à votre éditeur.

>[!MORELIKETHIS]
>
>* [À propos de [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Paramètres](simple-deal-settings.md)
>* [Afficher un rapport détaillé pour une transaction](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
