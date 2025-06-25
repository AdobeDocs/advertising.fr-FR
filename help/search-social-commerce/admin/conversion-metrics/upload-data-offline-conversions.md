---
title: Chargement des données de conversion hors ligne pour les conversions améliorées
description: Découvrez comment charger des données de conversion propriétaires hors ligne pour mapper vers des conversions  [!DNL Google Ads]  pour les prospects et des conversions  [!DNL Microsoft Advertising] .
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Chargement des données de conversion hors ligne pour les conversions améliorées

Comptes *[!DNL Google Ads]et [!DNL Microsoft Advertising] uniquement*

Vous pouvez charger vos données de conversion propriétaires hors ligne, y compris les adresses e-mail et les numéros de téléphone hachés, pour les mapper à vos [[!DNL Google Ads] conversions améliorées pour les prospects](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) et [[!DNL Microsoft Advertising] conversions améliorées](https://help.ads.microsoft.com/#apex/ads/en/60178) existantes. Toutes les données chargées sont synchronisées en temps réel avec le réseau publicitaire.

## Charger des données pour des conversions améliorées

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, puis sur l&#39;onglet **[!UICONTROL Upload]**.

1. Sélectionnez le réseau publicitaire, puis le compte.

1. (Facultatif) Pour télécharger un modèle avec tous les [champs de données obligatoires](#enhanced-conversions-leads-data) au format [!DNL Microsoft Excel], cliquez sur **[!UICONTROL View Template]**, puis téléchargez le fichier conformément à la procédure normale de votre navigateur.

   Vous pouvez modifier le fichier pour inclure vos données et enregistrer vos modifications, puis charger le fichier à l’étape suivante.

1. Cliquez sur **[!UICONTROL Choose File]**, puis sélectionnez un fichier à charger à partir de votre appareil ou réseau.

## Données requises pour les fichiers chargés {#enhanced-conversions-leads-data}

### Données au-dessus du tableau

`Parameters:TimeZone=insert_timezone`

Entrez le fuseau horaire du compte à cet emplacement ou dans la colonne « [!UICONTROL Conversion Time] » pour chaque ligne. Utilisez a\) ([!DNL Google Ads only]) le [format d’ID de fuseau horaire pris en charge](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) ou b\) le décalage GMT, comme indiqué par + ou - et la différence temporelle à 4 chiffres (par exemple : -0500 pour New York, +0100 pour Berlin ou +0000 pour le temps universel coordonné).

### Colonnes et valeurs du tableau pour les [!DNL Google Ads]

| Colonne | Description |
| ------ | ----------- |
| E-mail | L’adresse e-mail de l’utilisateur, qui doit être hachée à l’aide de l’algorithme SHA-256. Chaque ligne doit inclure une valeur E-mail ou Numéro de téléphone. |
| Numéro de téléphone | Le numéro de téléphone de l’utilisateur ou de l’utilisatrice, qui doit être haché à l’aide de l’algorithme SHA-256. Il doit inclure un code de pays et peut contenir des tirets et d’autres symboles. Chaque ligne doit inclure une valeur E-mail ou Numéro de téléphone. |
| Nom de la conversion | (Obligatoire) Nom de l’action de conversion. |
| Heure de conversion | (Obligatoire) Heure à laquelle l’événement de conversion s’est produit [format d’heure pris en charge](https://support.google.com/google-ads/answer/7014069#prepare_data). Si vous n’incluez pas l’identifiant de fuseau horaire du compte sur la ligne de `Parameters:TimeZone=insert_timezone` au-dessus du tableau de données, incluez le fuseau horaire pour chaque ligne à l’aide de a\) le [format d’identifiant de fuseau horaire pris en charge](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) ou b\) le décalage GMT, comme indiqué par + ou - et le décalage horaire à 4 chiffres (comme -0500 pour New York, +0100 pour Berlin ou +000 pour le temps moyen de Greenwich). |
| Valeur de conversion | (Obligatoire) Valeur de conversion numérique. |
| Devise de conversion | Code de devise de l’événement de conversion. |
| Ajouter des données utilisateur | (Applicable aux données relatives aux utilisateurs de l’Espace économique européen (EEE) ou du Royaume-Uni (UK)) Indique si l’utilisateur a donné son consentement pour envoyer des données utilisateur à [!DNL Google] à des fins de personnalisation publicitaire. Les valeurs peuvent inclure `Granted`, `Denied` ou \[null\] (qui est envoyé à [!DNL Google Ads] en tant que `Unspecified`). **Remarque :** [!DNL Google Ads] n’applique pas actuellement le consentement pour les conversions améliorées de prospects, mais il pourra le faire à l’avenir. |
| Personalization publicitaire | (Applicable aux données relatives aux utilisateurs dans l’Espace économique européen (EEE) ou au Royaume-Uni (UK)) Indique si l’utilisateur a donné son consentement pour envoyer des données utilisateur à [!DNL Google] à des fins publicitaires. Les valeurs peuvent inclure `Granted`, `Denied` ou \[null\] (qui est envoyé à [!DNL Google Ads] en tant que `Unspecified`). **Remarque :** [!DNL Google Ads] n’applique pas actuellement le consentement pour les conversions améliorées de prospects, mais il pourra le faire à l’avenir. |

### Colonnes et valeurs du tableau pour les [!DNL Microsoft Advertising]

Pour plus d’instructions sur l’utilisation du modèle, voir [https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852).

| Colonne | Description |
| ------ | ----------- |
| Nom de la conversion | (Obligatoire) Nom de l’objectif de conversion. |
| Heure de conversion | (Obligatoire) Heure à laquelle l’événement de conversion s’est produit. Si vous n’incluez pas l’identifiant de fuseau horaire du compte sur la ligne `Parameters:TimeZone=insert_timezone` au-dessus du tableau de données, incluez le fuseau horaire de chaque ligne à l’aide du décalage GMT, comme indiqué par + ou - et la différence temporelle à 4 chiffres (comme -0500 pour New York, +0100 pour Berlin ou +0000 pour le temps universel coordonné). Pour obtenir la liste des fuseaux horaires de différentes villes, voir [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), mais veillez à utiliser le format spécifié ici au lieu du format de la liste des fuseaux horaires. |
| Valeur de conversion | (Obligatoire) Valeur de conversion numérique. |
| Devise de conversion | Code de devise de l’événement de conversion. |
| ID de clic Microsoft | Identifiant de clic de [!DNL Microsoft] unique associé (MSCLKID). Ce champ peut être vide pour les conversions hors ligne améliorées. |
| Adresse e-mail hachée | L’adresse e-mail de l’utilisateur, qui doit être hachée à l’aide de l’algorithme SHA-256. Pour les conversions hors ligne améliorées, chaque ligne doit inclure une valeur d’adresse électronique hachée ou de numéro de téléphone haché. |
| Numéro de téléphone haché | Le numéro de téléphone de l’utilisateur ou de l’utilisatrice, qui doit être haché à l’aide de l’algorithme SHA-256. Il doit inclure un code de pays et peut contenir des tirets et d’autres symboles. Pour les conversions hors ligne améliorées, chaque ligne doit inclure une valeur d’adresse électronique hachée ou de numéro de téléphone haché. |

>[!MORELIKETHIS]
>
>* [Implémenter  [!DNL Google Ads]  conversions améliorées pour les prospects](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implémenter  [!DNL Microsoft Advertising]  conversions hors ligne améliorées](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* ([!DNL Google Ads only]) [Créer une action de conversion pour une conversion améliorée  [!DNL Google Ads]  prospects](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [Charger les mesures de conversion suivies par Search, Social et Commerce vers [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
