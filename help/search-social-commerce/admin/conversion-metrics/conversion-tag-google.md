---
title: Création d’une balise de conversion pour [!DNL Google Ads]
description: Découvrez comment créer une [!DNL Google Ads] balise de conversion.
exl-id: 322be2d5-0d66-4d0c-a17a-619a1f6c0644
source-git-commit: 54d253f672569467dab5129d172b77340dd13593
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# Création d’une balise de conversion pour [!DNL Google Ads]

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Spécifiez la variable [paramètres de balise de conversion](#conversion-tag-settings-google).

   1. Sélectionnez le compte, puis le type de conversion.

   1. Cliquez sur **[!UICONTROL Next]**.

   1. Spécifiez les options de conversion.

   1. Cliquez sur **[!UICONTROL Generate]**.

Une fois la balise créée, implémentez-la sur les sites web à partir desquels vous souhaitez effectuer le suivi de la mesure de conversion. Voir &quot;Installation de la balise Google&quot; dans l’aide de Google Ads à la rubrique &quot;[2. Configuration de votre balise Google](https://support.google.com/google-ads/answer/12215519).&quot;

## Paramètres des balises de conversion {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** Compte Google Ads applicable.

**[!UICONTROL Type of Conversion]:** Le type de conversion à suivre : *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]*, ou *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** Nom unique de la mesure de conversion.

**\[Catégorie de l’objectif\] :** L’objectif de conversion. Les objectifs disponibles varient en fonction du type de conversion. Pour *[!UICONTROL Calls to a phone number on your website]* et *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]&quot; est sélectionné par défaut.

**\[Type d’action\] :** Si l’objectif est un *[!UICONTROL Primary action used for bidding optimization]* ou *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Comment mesurer la variable [valeur de chaque conversion](https://support.google.com/google-ads/answer/3419241): *[!UICONTROL Use the same value for each conversion]*, *[!UICONTROL Use a different value for each conversion]*, ou *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*.

**[!UICONTROL Count]:** [Nombre de conversions à comptabiliser par clic ou interaction](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** Nombre maximal de jours après une interaction publicitaire pour laquelle des conversions sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou sélectionnez **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL View Through Conversion Window]:** Nombre maximal de jours après l’affichage par un utilisateur de vos publicités pour lesquelles des conversions d’affichage publicitaire sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou sélectionnez **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL Attribution Model]:** [Quelle quantité de crédit obtient chaque interaction publicitaire ?](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*, ou *[!UICONTROL Position based]*.

