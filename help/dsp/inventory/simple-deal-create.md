---
title: Créer une offre [!UICONTROL Simple Ad Serving]
description: Découvrez comment créer un pixel de tracking pour une offre [!UICONTROL Simple Ad Serving].
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# Créer une offre [!UICONTROL Simple Ad Serving]

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**, puis sélectionnez **[!UICONTROL Simple Ad Serving]**.

1. Saisissez les [ paramètres de l’offre ](simple-deal-settings.md) :

   1. Dans la section [!UICONTROL Select Ad Source], spécifiez des informations sur l’éditeur, l’annonceur et la campagne, ainsi que le type d’annonce, puis cliquez sur **[!UICONTROL Next]**.

   1. Dans la section [!UICONTROL Select Ad(s)] , spécifiez une annonce publicitaire à utiliser comme proxy dans DSP :

      1. Effectuez l’une des opérations suivantes :

         * Pour les publicités existantes, sélectionnez les publicités à utiliser.

         * Pour les nouvelles publicités, créez un proxy [publicité tierce](/help/dsp/campaign-management/ads/ad-create-multiple.md).

      >[!NOTE]
      > DSP ne diffuse pas les publicités que vous spécifiez. L’éditeur diffuse la publicité.

      1. Cliquez sur **[!UICONTROL Next]**.

   1. Dans Détails du flux, modifiez les détails du flux, puis cliquez sur **[!UICONTROL Next]**.

      DSP génère automatiquement un emplacement nommé « Emplacement SAS - &lt;*nom de l’offre*> » pour la publicité. Dans l’emplacement, l’offre est automatiquement ciblée dans la section [!UICONTROL Inventory Targets] . Toutes les autres options de ciblage ne sont pas applicables.

1. Envoyez les pixels de suivi d’événement à l’éditeur pour implémentation de l’une des façons suivantes :

   * (Facultatif) Dans l’écran [!UICONTROL Activate Tag with Publisher], envoyez la balise d’offre à l’éditeur.

     Lorsque vous avez terminé les étapes précédentes, DSP génère un e-mail que vous pouvez envoyer à l’éditeur. Le message comprend les détails de l’opération, un lien à partir duquel récupérer l’étiquette de l’opération et un code d’autorisation pour le lien.

      1. Passez en revue les détails de l’opération, puis effectuez l’une des opérations suivantes :

         * Pour coller les informations dans un e-mail dans une application de messagerie sur votre appareil, cliquez sur **[!UICONTROL Email & Done]** et sélectionnez l’application de messagerie. Le champ [!UICONTROL CC:] est prérempli avec une adresse d’assistance [!DNL Adobe]. Vous pouvez ensuite envoyer le message au contact approprié pour l’éditeur.

         * Pour copier les informations dans le presse-papiers, cliquez sur **[!UICONTROL Copy Email].** Vous pouvez ensuite coller manuellement le contenu dans un e-mail et l’envoyer au contact approprié pour l’éditeur. Insérez une copie (CC :) à `publisher-support-global@adobe.com`. Lorsque vous avez terminé de copier le message, cliquez sur **[!UICONTROL Email & Done]**.

      1. (Si nécessaire) Contactez l’éditeur pour vérifier si la balise inclut les macros appropriées afin que la balise fonctionne avec le serveur de publicités de l’éditeur.

   * (Facultatif) Envoyez manuellement les pixels de suivi d’événement à l’éditeur :

      1. Dans la ligne d&#39;opération de la vue [!UICONTROL Deals], cliquez sur ![menu Options](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Les pixels d’événement comprennent un pixel [!UICONTROL Clickthrough] et un pixel [!UICONTROL Impression]. Les publicités vidéo et audio incluent également des pixels d’événement par quartile renseigné (de [!UICONTROL 25% Complete] à [!UICONTROL 100% Complete]).

      1. Copiez les pixels de suivi d’événement et fournissez-les à votre éditeur.

>[!MORELIKETHIS]
>
>* [À propos des [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] les paramètres](simple-deal-settings.md)
>* [Afficher un rapport détaillé pour une affaire](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
