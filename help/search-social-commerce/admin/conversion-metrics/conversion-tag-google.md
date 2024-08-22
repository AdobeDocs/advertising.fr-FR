---
title: Création d’une balise de conversion pour [!DNL Google Ads]
description: Découvrez comment créer une balise de conversion  [!DNL Google Ads] .
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: 04330e26dbad6efe76dfcbe4662b062511ae14f6
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Créer une balise de conversion pour [!DNL Google Ads]

Vous pouvez créer des balises de conversion pour que les nouvelles conversions soient suivies pour des comptes [!DNL Google Ads] individuels et non pas suivies au niveau du compte de gestionnaire.

Pour générer des balises de conversion pour les conversions existantes, utilisez l’éditeur du réseau publicitaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Spécifiez les [paramètres de balise de conversion](#conversion-tag-settings-google).

   1. Sélectionnez le compte, puis le type de conversion.

   1. Cliquez sur **[!UICONTROL Next]**.

   1. Spécifiez les options de conversion.

   1. Cliquez sur **[!UICONTROL Generate]**.

1. Copiez la balise de conversion et implémentez-la sur les sites web à partir desquels vous souhaitez effectuer le suivi de la mesure de conversion.

   Voir &quot;Installation de la balise [!DNL Google]&quot; dans l’aide [!DNL Google Ads] à &quot;[2&quot;. Configurez votre balise Google](https://support.google.com/google-ads/answer/12215519).&quot;

1. Cliquez sur **[!UICONTROL Done].**

Une fois que vous avez ajouté les balises à votre site web et qu’elles commencent à se déclencher, [!DNL Google Ads] enregistre des conversions sur le site web. La recherche, Social et Commerce synchronisent quotidiennement les conversions. Pour plus d’informations sur les données synchronisées, voir &quot;[[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## Paramètres des balises de conversion {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** Compte Google Ads applicable.

**[!UICONTROL Type of Conversion]:** Type de conversion à suivre : *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]* ou *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** nom unique de la mesure de conversion.

**\[Catégorie de conversion\]:** Catégorie de conversion. Les catégories disponibles varient en fonction du type de conversion. Pour *[!UICONTROL Calls to a phone number on your website]* et *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; est sélectionné par défaut.

**\[Type d’action\]:** Indique si l’objectif est un *[!UICONTROL Primary action used for bidding optimization]* ou un *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Comment mesurer la [valeur de chaque conversion](https://support.google.com/google-ads/answer/3419241) :

* *[!UICONTROL Use the same value for each conversion],* qui nécessite de sélectionner une devise et de saisir la valeur de chaque conversion.

* *[!UICONTROL Use a different value for each conversion],* qui nécessite de sélectionner une devise et de saisir une valeur par défaut pour chaque conversion. Vous pouvez modifier la valeur par défaut de la balise avec une valeur spécifique à la transaction lorsque vous implémentez la balise sur une page web spécifique.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Combien de conversions à comptabiliser par clic ou interaction](https://support.google.com/google-ads/answer/3438531) : *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** nombre maximal de jours après une interaction publicitaire pour laquelle des conversions sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL View Through Conversion Window]:** nombre maximal de jours après qu’un utilisateur a affiché vos publicités pour lesquelles des conversions d’affichages publicitaires sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL Attribution Model]:** [Le crédit obtenu par chaque interaction publicitaire ](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138) : *[!UICONTROL Data driven]* ou *[!UICONTROL Last click]*. **Remarque :** Les actions de conversion qui utilisaient auparavant les modèles *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]* ou *[!UICONTROL Position based]* désormais non pris en charge utilisent désormais le modèle *[!UICONTROL Data driven]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] données de conversion dans Search, Social et Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
