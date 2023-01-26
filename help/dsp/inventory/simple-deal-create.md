---
title: Créez un [!UICONTROL Simple Ad Serving] Deal
description: Découvrez comment créer un pixel de suivi pour un [!UICONTROL Simple Ad Serving] accord.
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Créez un [!UICONTROL Simple Ad Serving] Deal

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**, puis sélectionnez **[!UICONTROL Simple Ad Serving]**.

1. Saisissez le [paramètres de transaction](simple-deal-settings.md):

   1. Dans le [!UICONTROL Select Ad Source] , spécifiez des informations sur l’éditeur, l’annonceur et la campagne, ainsi que le type d’annonce, puis cliquez sur **[!UICONTROL Next]**.

   1. Dans le [!UICONTROL Select Ad(s)] , spécifiez une publicité à utiliser comme proxy dans DSP :

      1. Effectuez l’une des opérations suivantes :

         * Pour les publicités existantes, sélectionnez les publicités à utiliser.

         * Pour les nouvelles publicités, créez un proxy. [publicité tierce](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSP ne diffuse pas les publicités que vous spécifiez. L’éditeur diffuse la publicité.

      1. Cliquez sur **[!UICONTROL Next]**.
   1. Dans les détails du flux, modifiez les détails du flux, puis cliquez sur **[!UICONTROL Next]**.

      DSP génère automatiquement un emplacement nommé &quot;Emplacement SAS - &lt;*nom de l&#39;opération*>,&quot; pour la publicité. Dans l’emplacement, l’opération est automatiquement ciblée dans la variable [!UICONTROL Inventory Targets] . Toutes les autres options de ciblage ne sont pas applicables.



1. Envoyez les pixels de suivi d’événement à l’éditeur pour implémentation de l’une des façons suivantes :

   * (Facultatif) Dans le [!UICONTROL Activate Tag with Publisher] , envoyez la balise de transaction à l’éditeur.

      Une fois les étapes précédentes terminées, DSP génère un message électronique que vous pouvez envoyer à l’éditeur. Le message comprend les détails de la transaction, un lien à partir duquel récupérer la balise de la transaction et un code d’autorisation pour le lien.

      1. Vérifiez les détails de l’opération, puis effectuez l’une des opérations suivantes :

         * Pour coller les informations dans un message électronique dans une application de messagerie sur votre appareil, cliquez sur **[!UICONTROL Email & Done]** et sélectionnez l’application de messagerie. Le [!UICONTROL CC:] prérenseigné avec un [!DNL Adobe] Adresse de l’assistance. Vous pouvez ensuite envoyer le message au contact approprié pour l’éditeur.

         * Pour copier les informations dans le presse-papiers, cliquez sur **[!UICONTROL Copy Email].** Vous pouvez ensuite coller manuellement le contenu dans un message électronique et l’envoyer au contact approprié de l’éditeur. Vous devez inclure une copie (CC :) à `publisher-support-global@adobe.com`. Lorsque vous avez terminé de copier le message, cliquez sur **[!UICONTROL Email & Done]**.
      1. (Si nécessaire) Vérifiez auprès de l’éditeur si la balise contient les macros appropriées afin qu’elle fonctionne avec le serveur d’annonces de l’éditeur.
   * (Facultatif) Envoyez manuellement les pixels de suivi d’événement à l’éditeur :

      1. Dans la ligne d’opération au sein de la variable [!UICONTROL Deals] afficher, cliquez sur ![Menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Les pixels de l’événement incluent une balise [!UICONTROL Clickthrough] pixel et un [!UICONTROL Impression] pixel. Les publicités vidéo et audio incluent également les pixels d’événement par quartile terminé (à partir de [!UICONTROL 25% Complete] to [!UICONTROL 100% Complete]).

      1. Copiez les pixels de suivi d’événement et fournissez-les à votre éditeur.



>[!MORELIKETHIS]
>
>* [A propos [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Paramètres](simple-deal-settings.md)
>* [Afficher un rapport détaillé pour une transaction](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
