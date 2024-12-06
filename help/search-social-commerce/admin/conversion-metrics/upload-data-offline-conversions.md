---
title: Chargement de données de conversion hors ligne pour des conversions améliorées
description: Découvrez comment charger des données de conversion hors ligne propriétaires pour mapper les conversions vers des  [!DNL Google Ads] conversions améliorées pour les pistes et [!DNL Microsoft Advertising] conversions améliorées.
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: eb7320fdddce4895a689c32ec6fb1e44cb8f2705
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Chargement de données de conversion hors ligne pour des conversions améliorées

*[!DNL Google Ads]et [!DNL Microsoft Advertising] comptes uniquement*

Vous pouvez télécharger vos données de conversion hors ligne propriétaires (y compris vos adresses électroniques hachées et vos numéros de téléphone) pour les mapper à vos [[!DNL Google Ads]  conversions améliorées pour les pistes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) et [[!DNL Microsoft Advertising]  conversions améliorées](https://help.ads.microsoft.com/#apex/ads/en/60178). Toutes les données chargées sont synchronisées en temps réel sur le réseau publicitaire.

## Chargement de données pour des conversions améliorées

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**, puis sur l’onglet **[!UICONTROL Upload]**.

1. Sélectionnez le réseau publicitaire, puis le compte.

1. (Facultatif) Pour télécharger un modèle avec tous les [ champs de données requis](#enhanced-conversions-leads-data) au format [!DNL Microsoft Excel], cliquez sur **[!UICONTROL View Template]**, puis téléchargez le fichier selon la procédure normale de votre navigateur.

   Vous pouvez modifier le fichier pour inclure vos données et enregistrer vos modifications, puis télécharger le fichier à l’étape suivante.

1. Cliquez sur **[!UICONTROL Choose File]**, puis sélectionnez un fichier à charger à partir de votre appareil ou de votre réseau.

## Données requises pour les fichiers chargés {#enhanced-conversions-leads-data}

### Données au-dessus du tableau

`Parameters:TimeZone=insert_timezone`

Saisissez le fuseau horaire du compte à cet emplacement ou dans la colonne &quot;[!UICONTROL Conversion Time]&quot; pour chaque ligne. Utilisez a\) ([!DNL Google Ads only]) le [ format d’ID de fuseau horaire pris en charge](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) ou b\) le décalage GMT, comme indiqué par + ou - et la différence de temps à 4 chiffres (par exemple -0500 pour New York, +0100 pour Berlin ou +0000 pour l’heure moyenne de Greenwich).

### Colonnes et valeurs de tableau pour [!DNL Google Ads]

| Colonne | Description |
| ------ | ----------- |
| Email | Adresse électronique de l’utilisateur, qui doit être hachée à l’aide de l’algorithme SHA-256. Chaque ligne doit inclure une valeur Email ou une valeur Phone Number. |
| Numéro de téléphone | Numéro de téléphone de l’utilisateur, qui doit être haché à l’aide de l’algorithme SHA-256. Il doit inclure un code de pays et peut contenir des tirets et d’autres symboles. Chaque ligne doit inclure une valeur Email ou une valeur Phone Number. |
| Nom de la conversion | (Obligatoire) Nom de l’action de conversion. |
| Temps de conversion | (Obligatoire) Heure à laquelle l’événement de conversion s’est produit dans un [format d’heure pris en charge](https://support.google.com/google-ads/answer/7014069#prepare_data). Si vous n’incluez pas l’identifiant de fuseau horaire du compte dans la ligne `Parameters:TimeZone=insert_timezone` située au-dessus du tableau de données, incluez le fuseau horaire pour chaque ligne à l’aide de a\) le [format d’identifiant de fuseau horaire pris en charge](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) ou b\) le décalage GMT, comme indiqué par + ou - et la différence de temps de 4 chiffres (par exemple -05000 pour New York, +000 pour Berlin ou +0 000 pour Greenwich Mean Time). |
| Valeur de conversion | (Obligatoire) La valeur de conversion numérique. |
| Devise de conversion | Code de devise de l’événement de conversion. |
| Données utilisateur de publicité | (Applicable aux données relatives aux utilisateurs de l’Espace économique européen (EEE) ou du Royaume-Uni (Royaume-Uni)) Indique si le consentement de l’utilisateur a été donné pour envoyer des données utilisateur à [!DNL Google] à des fins de personnalisation publicitaire. Les valeurs peuvent inclure `Granted`, `Denied` ou \[null\] (qui est envoyé à [!DNL Google Ads] en tant que `Unspecified`). **Remarque :** [!DNL Google Ads] n’impose actuellement pas le consentement pour les conversions améliorées pour les pistes, mais il peut le faire à l’avenir. |
| Personalization publicitaire | (Applicable aux données relatives aux utilisateurs de l’Espace économique européen (EEE) ou du Royaume-Uni (Royaume-Uni)) Indique si le consentement de l’utilisateur a été donné pour envoyer des données utilisateur à [!DNL Google] à des fins publicitaires. Les valeurs peuvent inclure `Granted`, `Denied` ou \[null\] (qui est envoyé à [!DNL Google Ads] en tant que `Unspecified`). **Remarque :** [!DNL Google Ads] n’impose actuellement pas le consentement pour les conversions améliorées pour les pistes, mais il peut le faire à l’avenir. |

### Colonnes et valeurs de tableau pour [!DNL Microsoft Advertising]

Pour plus d’instructions sur l’utilisation du modèle, voir [https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852).

| Colonne | Description |
| ------ | ----------- |
| Nom de la conversion | (Obligatoire) Nom de l’objectif de conversion. |
| Temps de conversion | (Obligatoire) Heure à laquelle l’événement de conversion s’est produit. Si vous n’incluez pas l’identifiant de fuseau horaire du compte dans la ligne `Parameters:TimeZone=insert_timezone` située au-dessus du tableau de données, incluez le fuseau horaire pour chaque ligne à l’aide du décalage GMT, comme indiqué par + ou - et l’écart de 4 chiffres (par exemple -0500 pour New York, +0100 pour Berlin ou +000 pour l’heure moyenne de Greenwich). Pour obtenir la liste des fuseaux horaires des différentes villes, voir [https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones), mais assurez-vous d’utiliser le format spécifié ici au lieu du format dans la liste des fuseaux horaires. |
| Valeur de conversion | (Obligatoire) La valeur de conversion numérique. |
| Devise de conversion | Code de devise de l’événement de conversion. |
| Microsoft Click ID | Identifiant de clic unique [!DNL Microsoft] associé (MSCLKID). Ce champ peut être vide pour les conversions hors ligne améliorées. |
| Adresse électronique hachée | Adresse électronique de l’utilisateur, qui doit être hachée à l’aide de l’algorithme SHA-256. Pour améliorer les conversions hors ligne, chaque ligne doit inclure une valeur Adresse électronique hachée ou Numéro de téléphone haché. |
| Numéro de téléphone haché | Numéro de téléphone de l’utilisateur, qui doit être haché à l’aide de l’algorithme SHA-256. Il doit inclure un code de pays et peut contenir des tirets et d’autres symboles. Pour améliorer les conversions hors ligne, chaque ligne doit inclure une valeur Adresse électronique hachée ou Numéro de téléphone haché. |

>[!MORELIKETHIS]
>
>* [Implémentation [!DNL Google Ads] de conversions améliorées pour les pistes](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [Implémentation [!DNL Microsoft Advertising] de conversions hors ligne améliorées](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* ([!DNL Google Ads only])[ Créez une action de conversion pour une  [!DNL Google Ads] conversion améliorée pour les pistes](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [ Télécharger les mesures de conversion de recherche, de Social et de suivi Commerce vers  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
