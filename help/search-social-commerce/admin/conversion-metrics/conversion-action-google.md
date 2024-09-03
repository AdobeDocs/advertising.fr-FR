---
title: Création d’une action de conversion pour une  [!DNL Google Ads] conversion améliorée pour les pistes
description: Découvrez comment créer une action de conversion  [!DNL Google Ads] pour une conversion améliorée pour les pistes.
feature: Conversions
source-git-commit: 5eb6ed5b42e74f424fc8499f6df0dbe3f2430ab2
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Créer une action de conversion pour une conversion améliorée de [!DNL Google Ads] pour les pistes

*[!DNL Google Ads]comptes uniquement*

Vous pouvez créer des actions de conversion pour [!DNL Google Ads] conversions améliorées pour le suivi des pistes pour des comptes [!DNL Google Ads] individuels, et non pas pour le suivi des conversions au niveau du compte du gestionnaire.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, ce qui ouvre l’onglet **[!UICONTROL Summary]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").

1. Spécifiez les [paramètres d’action de conversion](#conversion-action-settings-google).

   1. Sélectionnez le compte, puis le type de conversion : *[!UICONTROL Import conversion]*.

   1. Cliquez sur **[!UICONTROL Next]**.

   1. Spécifiez les options d’action de conversion.

   1. Cliquez sur **[!UICONTROL Generate]**.

1. Lisez des informations sur la création d’une balise de suivi pour la conversion améliorée pour les pistes, puis cliquez sur **[!UICONTROL Next]**.

   Créez la balise de conversion et mettez-la en oeuvre selon les besoins sur les sites web à partir desquels vous souhaitez effectuer le suivi de la mesure de conversion. Pour obtenir des instructions, voir :

   * Pour utiliser la balise [!DNL Google], reportez-vous aux instructions [!DNL Google Ads] pour &quot;configurer les paramètres de balise [!DNL Google]&quot; dans &quot;[Configuration de conversions améliorées pour les pistes avec la  [!DNL Google] balise](https://support.google.com/google-ads/answer/11347292)&quot;.

   * Pour utiliser [!DNL Google Tag Manager], consultez les instructions [!DNL Google Ads] pour &quot;Configurer les paramètres de balise [!DNL Google]&quot; et &quot;Vérifier votre configuration et publier le conteneur&quot; dans &quot;[Configuration de conversions améliorées pour les pistes avec [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure)&quot;.

1. Cliquez sur **[!UICONTROL Done].**

Une fois que vous avez créé l’action de conversion et implémenté une balise de suivi de conversion, vous pouvez charger les données de conversion hors ligne que votre organisation capture et les attribuer à l’action de conversion. Voir &quot;[Chargement de données de conversion hors ligne pour des conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)&quot;.

## Paramètres d’action de conversion {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** Compte Google Ads applicable.

**[!UICONTROL Type of Conversion]:** Type de conversion à suivre : sélectionnez *[!UICONTROL Import conversion]*. Tous les autres types sont utilisés pour créer des balises de suivi de conversion (et non des actions de conversion) pour d’autres types de conversion.

**[!UICONTROL Conversion Name]:** Nom unique de l’action de conversion.

**\[Catégorie de conversion\] :** Catégorie de conversion, telle que *piste qualifiée* ou *inscription*.

**\[Type d’action\]:** Indique si l’objectif est un *[!UICONTROL Primary action used for bidding optimization]* ou un *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** Comment mesurer la [valeur de chaque conversion](https://support.google.com/google-ads/answer/13064207) :

* *[!UICONTROL Use the same value for each conversion],* qui nécessite de sélectionner une devise et de saisir la valeur de chaque conversion.

* *[!UICONTROL Use a different value for each conversion],* qui nécessite de sélectionner une devise et de saisir une valeur par défaut pour chaque conversion. Vous pouvez modifier la valeur par défaut de la balise avec une valeur spécifique à la transaction lorsque vous implémentez la balise sur une page web spécifique.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Combien de conversions à comptabiliser par clic ou interaction](https://support.google.com/google-ads/answer/3438531) : *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** nombre maximal de jours après une interaction publicitaire pour laquelle des conversions sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL View Through Conversion Window]:** nombre maximal de jours après qu’un utilisateur a affiché vos publicités pour lesquelles des conversions d’affichages publicitaires sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL Attribution Model]:** [Le crédit obtenu par chaque interaction publicitaire ](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138) : *[!UICONTROL Data driven]* ou *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [Chargement de données de conversion hors ligne pour des conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implémentation [!DNL Google Ads] de conversions améliorées pour les pistes](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
