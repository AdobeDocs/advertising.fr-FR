---
title: (Nouvelle interface utilisateur) Créer une action de conversion pour une conversion améliorée  [!DNL Google Ads]  prospects
description: Découvrez comment créer une action  [!DNL Google Ads]  conversion pour améliorer la conversion des prospects.
feature: Conversions
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Créer une action de conversion pour une conversion améliorée [!DNL Google Ads] pour les prospects

*Fonction*

Comptes *[!DNL Google Ads]uniquement*

Vous pouvez créer des actions de conversion pour [!DNL Google Ads] les conversions améliorées des prospects à suivre pour les comptes de [!DNL Google Ads] individuels, et non les conversions suivies au niveau du compte du responsable.

Une fois que vous avez créé l’action de conversion et implémenté une balise de suivi des conversions, vous pouvez [charger les données de conversion hors ligne que votre organisation capture](conversions-upload-offline-enhanced-conversions.md) et les attribuer à l’action de conversion.

La prise en charge n’est pas disponible pour les comptes [!DNL Microsoft Advertising].

## Création d’une action de conversion

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversions]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Set up Conversion]**.

1. Spécifiez les [paramètres de l’action de conversion](#conversion-action-settings-google).

   1. Sélectionnez le *[!UICONTROL Create Conversion]* de [!UICONTROL Setup Method].

   1. Sélectionnez le compte, puis sélectionnez le type de conversion : *[!UICONTROL Import conversion]*.

   1. Cliquez sur **[!UICONTROL Next]**.

   1. Spécifiez les options de l’action de conversion.

   1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

   1. Cliquez sur **[!UICONTROL Generate]**.

1. Lisez des informations sur la création d’une balise de suivi pour la conversion améliorée pour les prospects, puis cliquez sur **[!UICONTROL Next]**.

   Vous devez créer la balise de conversion et l’implémenter selon vos besoins sur les sites Web à partir desquels vous souhaitez effectuer le suivi de la mesure de conversion. Vous devrez également activer les conversions améliorées pour les prospects et accepter les conditions générales relatives aux données client. Pour obtenir des instructions détaillées, reportez-vous aux instructions [!DNL Google Ads] « [Configurer la balise  [!DNL Google]  pour des conversions améliorées de prospects](https://support.google.com/google-ads/answer/11021502) ».

   Si vous souhaitez effectuer le suivi des valeurs de conversion spécifiques aux transactions, [personnalisez votre fragment de code d’événement](https://support.google.com/google-ads/answer/6095947).

1. Cliquez sur **[!UICONTROL Close].**

## Paramètres des actions de conversion {#conversion-action-settings-google}

### Section Chemin de configuration

**[!UICONTROL Setup Method]:** Type d’action : *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]:** Réseau publicitaire : *[!UICONTROL Google]*.

### Section Détails de la conversion

**[!UICONTROL Select Account]:** compte [!DNL Google Ads] applicable.

**[!UICONTROL Type of conversions]:** Type de conversion à suivre : sélectionnez *[!UICONTROL Import conversion]*. Tous les autres types sont utilisés pour créer des balises de suivi de conversion (et non des actions de conversion) pour d’autres types de conversions.

### Section Paramètres de conversion

**[!UICONTROL Conversion Name]:** Nom unique de l’action de conversion.

**[!UICONTROL Goal Category]:** catégorie de conversion, par exemple *Prospect qualifié* ou *Inscription*.

**[!UICONTROL Preferred Action optimization]:** si l’objectif est un *[!UICONTROL Primary action used for bidding optimization]* ou un *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Conversion Value]:** Comment mesurer la [valeur de chaque conversion](https://support.google.com/google-ads/answer/13064207) :

* *[!UICONTROL Use the same value for each conversion],* qui nécessite de sélectionner une devise et de saisir la valeur pour chaque conversion.

* *[!UICONTROL Use different values for each conversion],* qui nécessite de sélectionner une devise et de saisir une valeur par défaut pour chaque conversion. Vous pouvez modifier la valeur par défaut dans la balise avec une valeur spécifique à la transaction lorsque vous implémentez la balise sur une page web spécifique.

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [Nombre de conversions à comptabiliser par clic ou interaction](https://support.google.com/google-ads/answer/3438531) : *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* ou *[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*.

**[!UICONTROL Click-Through Conversion Window]:** nombre maximal de jours après une interaction publicitaire pour lequel des conversions sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou sélectionnez **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL View-Through Conversion Window]:** nombre maximal de jours après la consultation par un utilisateur de vos publicités pour lequel les conversions d’affichage publicitaire sont enregistrées. Pour les campagnes de recherche, d’affichage et d’achat, la fenêtre peut être comprise entre 1 et 90 jours. Sélectionnez un nombre ou sélectionnez **[!UICONTROL Custom]** et saisissez un nombre.

**[!UICONTROL Attribution Model]:** [modèle d’attribution qui détermine le crédit accordé à chaque interaction publicitaire](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138) : *[!UICONTROL Data driven]* ou *[!UICONTROL Last click]*.

>[!MORELIKETHIS]
>
>* [(Nouvelle interface utilisateur) Charger des données de conversion hors ligne pour des conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Chargement des données de conversion hors ligne pour les conversions améliorées](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [Implémenter  [!DNL Google Ads]  conversions améliorées pour les prospects](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
