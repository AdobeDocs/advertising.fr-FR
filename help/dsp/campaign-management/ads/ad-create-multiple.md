---
title: Création de plusieurs annonces publicitaires tierces
description: Découvrez comment créer plusieurs annonces tierces à la fois.
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 3538c1d881a3032863c5a6f8c7361ac1c0bc35f9
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Création de plusieurs annonces publicitaires tierces

Vous pouvez créer jusqu’à 500 annonces tierces à la fois en chargeant des balises qui pointent vers des ressources créatives hébergées sur des serveurs de publicités tiers. Vous pouvez inclure des pixels de suivi pour les publicités.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Vous pouvez charger des feuilles de balises [!DNL DoubleClick] et [!DNL Flashtalking] ou un fichier renseigné manuellement à l’aide du modèle fourni.

>[!TIP]
>
> La bonne pratique consiste à utiliser des annonces tierces diffusées en toute sécurité à l’aide de HTTPS. Les URL diffusées en utilisant HTTPS commencent par « https ».

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne dans laquelle vous souhaitez inclure la publicité.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**. Dans la section Types d’annonces du menu, cliquez sur **[!UICONTROL Bulk upload ads]**.

1. Sélectionnez le serveur de publicités sur lequel la publicité est hébergée : *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* ou *[!UICONTROL Other]*.

1. (Annonces [!DNL DoubleClick] et [!DNL Flashtalking]) Sélectionnez le type de balise à utiliser pour chaque ressource vidéo et chaque ressource d’affichage. Les options disponibles varient selon le serveur de publicités.

1. (Publicités sur tous les serveurs de publicités, à l’exception de [!DNL DoubleClick] et [!DNL Flashtalking]) Cliquez sur **[!UICONTROL Download this template]** pour télécharger un modèle au format [!DNL Microsoft Excel] feuille de calcul (XLSX), que vous pouvez remplir avec des données publicitaires et enregistrer localement. Les colonnes obligatoires comprennent [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag] et [!UICONTROL Ad Types].

1. Cliquez sur **[!UICONTROL Upload]** et sélectionnez un fichier aux formats .xlsx ou .xls sur votre appareil ou réseau.

   Pour les publicités [!DNL DoubleClick] et [!DNL Flashtalking], chargez des feuilles de balises non modifiées à partir du serveur de publicités. Pour les autres serveurs de publicités, utilisez le modèle que vous avez téléchargé à l’étape 3.

1. Une fois le chargement terminé, cliquez sur **[!UICONTROL Start Building Ads]**.

1. Examinez les détails et le statut de chaque publicité :

   1. (Publicités vidéo universelles à l’aide de balises [!DNL Google] ou [!DNL Flashtalking]) Cliquez sur le champ **[!UICONTROL Ad Type]** et sélectionnez **[!UICONTROL Universal Video]**.

   1. (Publicités vidéo universelles) Pour chaque nouvelle publicité, cliquez sur ![Modifier](/help/dsp/assets/edit.png), sélectionnez le [format vidéo applicable](/help/dsp/campaign-management/ads/ad-settings-universal-video.md), puis cliquez sur **Enregistrer**.

   1. Vérifiez le statut de chaque publicité, qui est basé sur les contrôles de validation de la balise chargée.

   1. (Facultatif) Effectuez l’une des opérations suivantes pour chaque publicité :

      * Pour prévisualiser une publicité, cliquez sur ![lecture](/help/dsp/assets/play.png) dans la ligne de publicité.

      * Pour modifier les détails de l’annonce publicitaire, cliquez sur ![modifier](/help/dsp/assets/edit.png), modifiez les détails, puis cliquez sur **Enregistrer**.

      * Pour supprimer une publicité, cliquez sur **[!UICONTROL X]** dans la ligne de publicité.

1. Cliquez sur **[!UICONTROL Create *N *Annonce(s) publicitaire(s)]**.

1. Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Done]**.

   * (Si une publicité est rejetée, facultatif) Pour modifier l’enregistrement de la publicité et la soumettre à nouveau pour révision :

      1. Cliquez sur le nom de l’annonce publicitaire.

      1. Modifiez les paramètres de la publicité.

      1. Cliquez sur **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>Les publicités vidéo universelles ne peuvent être associées qu’à des emplacements vidéo universels.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Spécifications publicitaires](ad-specs.md)
>* [Créer une publicité unique](ad-create.md)
>* [Vidéo : Comment télécharger en bloc des balises de publicité tierces &#x200B;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html?lang=fr)
>* [FAQ sur Universal Video](/help/dsp/campaign-management/faq-universal-video.md)
