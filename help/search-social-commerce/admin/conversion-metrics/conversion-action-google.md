---
title: Création d’une action de conversion pour une conversion  [!DNL Google Ads]  pour les prospects
description: Découvrez comment créer une action  [!DNL Google Ads]  conversion pour améliorer la conversion des prospects.
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Création d’une action de conversion pour une conversion améliorée [!DNL Google Ads] pour les prospects

Comptes *[!DNL Google Ads]uniquement*

Vous pouvez créer des actions de conversion pour [!DNL Google Ads] les conversions améliorées des prospects à suivre pour les comptes de [!DNL Google Ads] individuels, et non les conversions suivies au niveau du compte du responsable.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, ce qui ouvre l’onglet **[!UICONTROL Summary]** .

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Spécifiez les [paramètres de l’action de conversion](#conversion-action-settings-google).

   1. Sélectionnez le compte, puis sélectionnez le type de conversion : *[!UICONTROL Import conversion]*.

   1. Cliquez sur **[!UICONTROL Next]**.

   1. Spécifiez les options de l’action de conversion.

   1. Cliquez sur **[!UICONTROL Generate]**.

1. Lisez des informations sur la création d’une balise de suivi pour la conversion améliorée pour les prospects, puis cliquez sur **[!UICONTROL Next]**.

   Créez la balise de conversion et implémentez-la si nécessaire sur les sites web à partir desquels vous souhaitez effectuer le suivi de la mesure de conversion. Pour obtenir des instructions, reportez-vous aux sections suivantes :

   * Pour utiliser la balise [!DNL Google], reportez-vous aux instructions [!DNL Google Ads] de la section « Configuration des paramètres de balise [!DNL Google] » de la section « [Configuration de conversions améliorées pour les prospects utilisant la balise  [!DNL Google] &#x200B;](https://support.google.com/google-ads/answer/11347292) ».

   * Pour utiliser [!DNL Google Tag Manager], reportez-vous aux instructions [!DNL Google Ads] « Configurer [!DNL Google] paramètres de balise » et « Vérifier votre configuration et publier le conteneur » dans « [&#x200B; Configurer des conversions améliorées pour les prospects avec  [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure) ».

1. Cliquez sur **[!UICONTROL Done].**

Une fois que vous avez créé l’action de conversion et implémenté une balise de suivi des conversions, vous pouvez charger les données de conversion hors ligne que votre organisation capture et les attribuer à l’action de conversion. Voir « [&#x200B; Chargement des données de conversion hors ligne pour les conversions améliorées &#x200B;](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) ».

## Paramètres des actions de conversion {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** compte Google Ads applicable.

**[!UICONTROL Type of Conversion]:** Type de conversion à suivre : sélectionnez *[!UICONTROL Import conversion]*. Tous les autres types sont utilisés pour créer des balises de suivi de conversion (et non des actions de conversion) pour d’autres types de conversions.

**[!UICONTROL Conversion Name]:** Nom unique de l’action de conversion.

**\[Catégorie de conversion\] :** la catégorie de conversion, telle que *Lead qualifié* ou *Inscription*.

**\[Type d’action\] :** si l’objectif est un *[!UICONTROL Primary action used for bidding optimization]* ou un *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Comment mesurer la [valeur de chaque conversion](https://support.google.com/google-ads/answer/13064207) :

* *[!UICONTROL Use the same value for each conversion],* qui nécessite de sélectionner une devise et de saisir la valeur pour chaque conversion.

* *[!UICONTROL Use a different value for each conversion],* qui nécessite de sélectionner une devise et de saisir une valeur par défaut pour chaque conversion. Vous pouvez modifier la valeur par défaut dans la balise avec une valeur spécifique à la transaction lorsque vous implémentez la balise sur une page web spécifique.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Nombre de conversions à comptabiliser par clic ou interaction](https://support.google.com/google-ads/answer/3438531) : *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** nombre maximal de jours après une interaction publicitaire pour lequel des conversions sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou sélectionnez **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL View Through Conversion Window]:** nombre maximal de jours après la consultation par un utilisateur de vos publicités pour lequel les conversions d’affichage publicitaire sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou sélectionnez **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL Attribution Model]:** [Crédit attribué à chaque interaction publicitaire](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138) : *[!UICONTROL Data driven]* ou *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Chargement des données de conversion hors ligne pour les conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implémenter  [!DNL Google Ads]  conversions améliorées pour les prospects](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
