---
title: Créez une balise de conversion pour  [!DNL Google Ads]
description: Découvrez comment créer une balise  [!DNL Google Ads]  conversion.
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Créer une balise de conversion pour [!DNL Google Ads]

Vous pouvez créer des balises de conversion pour les nouvelles conversions à suivre pour les comptes de [!DNL Google Ads] individuels, et non au niveau du compte du responsable.

Pour générer des balises de conversion pour des conversions existantes, utilisez l’éditeur du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]** pour ouvrir l’onglet **[!UICONTROL Summary]** .

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Spécifiez les [paramètres de balise de conversion](#conversion-tag-settings-google).

   1. Sélectionnez le compte, puis sélectionnez le type de conversion.

   1. Cliquez sur **[!UICONTROL Next]**.

   1. Spécifiez les options de conversion.

   1. Cliquez sur **[!UICONTROL Generate]**.

1. Copiez la balise de conversion et implémentez-la sur les sites web à partir desquels vous souhaitez effectuer le suivi de la mesure de conversion.

   Voir « Installation de la balise [!DNL Google] » dans l’aide [!DNL Google Ads] sur « [2. Configurez votre balise Google](https://support.google.com/google-ads/answer/12215519). »

1. Cliquez sur **[!UICONTROL Done].**

Une fois que vous avez ajouté les balises à votre site web et qu’elles commencent à se déclencher, [!DNL Google Ads] enregistre les conversions sur le site web. Search, Social et Commerce synchronisent les conversions tous les jours. Pour plus d’informations sur les données synchronisées, voir « [[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Paramètres des balises de conversion {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** compte Google Ads applicable.

**[!UICONTROL Type of Conversion]:** type de conversion à suivre : *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* ou *[!UICONTROL Clicks to your number on your mobile website]*. **Remarque :** *[!UICONTROL Import conversion]* est utilisé à une autre fin. Voir « [Créer une action de conversion pour une conversion  [!DNL Google Ads]  pour les prospects](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) ».

**[!UICONTROL Conversion Name]:** Nom unique de la mesure de conversion.

**\[Catégorie de conversion\] :** la catégorie de conversion. Les catégories disponibles varient selon le type de conversion. Par *[!UICONTROL Calls to a phone number on your website]* et *[!UICONTROL Clicks to your number on your mobile website]*, « [!UICONTROL Phone Call Lead] » est sélectionné par défaut.

**\[Type d’action\] :** si l’objectif est un *[!UICONTROL Primary action used for bidding optimization]* ou un *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Comment mesurer la [valeur de chaque conversion](https://support.google.com/google-ads/answer/3419241) :

* *[!UICONTROL Use the same value for each conversion],* qui nécessite de sélectionner une devise et de saisir la valeur pour chaque conversion.

* *[!UICONTROL Use a different value for each conversion],* qui nécessite de sélectionner une devise et de saisir une valeur par défaut pour chaque conversion. Vous pouvez modifier la valeur par défaut dans la balise avec une valeur spécifique à la transaction lorsque vous implémentez la balise sur une page web spécifique.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Nombre de conversions à comptabiliser par clic ou interaction](https://support.google.com/google-ads/answer/3438531) : *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** nombre maximal de jours après une interaction publicitaire pour lequel des conversions sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou sélectionnez **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL View Through Conversion Window]:** nombre maximal de jours après la consultation par un utilisateur de vos publicités pour lequel les conversions d’affichage publicitaire sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou sélectionnez **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL Attribution Model]:** [Crédit attribué à chaque interaction publicitaire](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138) : *[!UICONTROL Data driven]* ou *[!UICONTROL Last click]*. **Remarque :** les actions de conversion qui utilisaient auparavant les modèles *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* ou *[!UICONTROL Position based]* désormais non pris en charge utilisent désormais le modèle *[!UICONTROL Data driven]*.

>[!MORELIKETHIS]
>
>* [Chargement des données de conversion hors ligne pour les conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
