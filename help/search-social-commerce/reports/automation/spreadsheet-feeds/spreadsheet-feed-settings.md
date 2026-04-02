---
title: Paramètres de flux de rapports des feuilles de calcul
description: Découvrez les paramètres des flux de feuilles de calcul.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
TQID: https://experienceleague.adobe.com/4JPflN5lVXkNf2nWszh-LznW2xNaMkQMGPOxo6Ac2WU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 513
ht-degree: 0%

---

# Paramètres de flux de rapports des feuilles de calcul

| Champ | Description |
|---|---|
| [!UICONTROL Feed Name] | Nom du flux de la feuille de calcul. |
| [!UICONTROL Report Template] | Modèle de rapport spécifiant les données de rapport requises. Sélectionnez celui que vous avez utilisé pour créer le modèle de [!DNL Excel]. Tous les modèles de rapport de base sont répertoriés.<br><br><b>Remarque :</b> si vous modifiez le modèle de rapport utilisé pour le rapport ou si vous mettez à jour les colonnes du modèle, vous devez créer et charger un nouveau modèle de [!DNL Excel]. |
| [!UICONTROL Excel Template] | Modèle de [!DNL Excel] spécialement formaté que vous avez créé au format .XLSX et qui est appliqué aux données spécifiées dans le modèle de rapport. Indiquez le fichier à charger en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur <b>[!UICONTROL Browse]</b> pour localiser le fichier sur votre appareil ou réseau. |
| [!UICONTROL Back Fill From] | Date de début pour laquelle les données existantes sur l’onglet [!UICONTROL RAW] sont actualisées, représentée par un nombre de jours dans le passé. Entrez une valeur allant jusqu’à 90 jours ; la valeur par défaut est de sept (7) jours.<br><br>Par exemple, si la valeur est 7 et que la date d’aujourd’hui est le 7 mars, les données existantes dans l’onglet [!UICONTROL RAW] commençant par le 1er mars sont actualisées (jusqu’à la date de fin spécifiée par le paramètre [!UICONTROL Back Fill Until] ). Les lignes de données existantes pour les dates antérieures au 1er mars ne sont pas supprimées, mais elles ne sont pas actualisées. |
| [!UICONTROL Back Fill Until] | Date de fin à laquelle les données existantes sur l’onglet [!UICONTROL RAW] sont actualisées, représentée par un nombre de jours dans le passé. La valeur par défaut est de un (1) jour.<br><br>Par exemple, si cette valeur est définie sur 1 et que la date d’aujourd’hui est le 7 mars, les données existantes dans l’onglet [!UICONTROL RAW] sont actualisées jusqu’au 6 mars (et en commençant par la date de début spécifiée par le paramètre [!UICONTROL Back Fill From] ). Si cette valeur est définie sur 1, le paramètre [!UICONTROL Back Fill Until] est défini sur 7 et que la valeur actuelle est le 7 mars, les données existantes dans l’onglet [!UICONTROL RAW] sont actualisées du 1er au 6 mars. Dans les deux exemples, les lignes de données existantes pour les dates postérieures au 6 mars ne sont pas supprimées, mais elles ne sont pas actualisées. |
| [!UICONTROL Email Recipients] | Adresses e-mail auxquelles envoyer des notifications chaque fois que le rapport est actualisé ou chaque fois que le rapport est exécuté lorsque le modèle inclut un planning. Par défaut, l’adresse de votre compte utilisateur est saisie. Pour spécifier plusieurs adresses, séparez-les par des virgules, des espaces ou de nouvelles lignes. |
| [!UICONTROL Schedule Time] | Heure à laquelle les flux de la feuille de calcul sont actualisés : soit à 08:00 soit à n’importe quelle heure entre 10 :00 et 23 :00 dans le fuseau horaire de l’annonceur. La valeur par défaut pour les nouveaux flux de feuille de calcul est 10 :00.<br><br><b>Remarque :</b> pour des raisons de performances, vous ne pouvez pas actualiser les flux de feuille de calcul à 09:00, lorsque d&#39;autres rapports sont générés. |
| [!UICONTROL Email Notification] | (Lorsque les destinataires d’e-mails sont spécifiés) Éléments à inclure dans les notifications par e-mail aux adresses spécifiées :<ul><li><i>Joindre un flux</i> — Pour envoyer une copie du rapport complété au format XLSX. Si le fichier dépasse 10 Mo, la notification n’inclut pas de pièce jointe.</li><li><i>Notification uniquement</i> (valeur par défaut) : pour envoyer uniquement une notification de fin ou d’échec du rapport, avec un lien vers le rapport.</li></ul> |

>[!MORELIKETHIS]
>
>* [À propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [Créer un flux de rapport de feuille de calcul](spreadsheet-feed-create.md)
>* [Créer un modèle [!DNL Excel] de flux de rapport de feuille de calcul](spreadsheet-feed-create-excel-template.md)
>* [Modifier les paramètres de flux de rapports des feuilles de calcul](spreadsheet-feed-edit.md)
>* [Afficher ou enregistrer un fichier de flux de rapports de feuille de calcul](spreadsheet-feed-view-or-save.md)
>* [Actualiser manuellement les flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
>* [Supprimer des flux de rapports de feuille de calcul](spreadsheet-feed-delete.md)
