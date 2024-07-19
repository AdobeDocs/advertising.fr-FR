---
title: Paramètres du flux de rapports de feuille de calcul
description: Découvrez les paramètres des flux de feuille de calcul.
exl-id: 88836c15-81fe-4fe7-8321-2c984b4dcb5d
feature: Search Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '513'
ht-degree: 0%

---

# Paramètres du flux de rapports de feuille de calcul

| Champ | Description |
|---|---|
| [!UICONTROL Feed Name] | Nom du flux de feuille de calcul. |
| [!UICONTROL Report Template] | Le modèle de rapport qui spécifie les données de rapport requises ; sélectionnez celui que vous avez utilisé pour créer le modèle [!DNL Excel]. Tous les modèles de rapport de base sont répertoriés.<br><br><b>Remarque :</b> Si vous modifiez le modèle de rapport utilisé pour le rapport ou que vous mettez à jour les colonnes du modèle, vous devez créer et charger un nouveau modèle [!DNL Excel]. |
| [!UICONTROL Excel Template] | Le modèle [!DNL Excel] spécialement formaté que vous avez créé au format .XLSX, qui est appliqué aux données spécifiées dans le modèle de rapport. Indiquez le fichier à télécharger en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur <b>[!UICONTROL Browse]</b> pour localiser le fichier sur votre appareil ou votre réseau. |
| [!UICONTROL Back Fill From] | La date de début pour laquelle les données existantes sur l’onglet [!UICONTROL RAW] sont actualisées, représentée par un nombre de jours dans le passé. Saisissez une valeur allant jusqu’à 90 jours ; la valeur par défaut est de sept (7) jours.<br><br>Par exemple, si la valeur est 7 et que la date d’aujourd’hui est le 7 mars, les données existantes sur l’onglet [!UICONTROL RAW] commençant par le 1er mars sont actualisées (jusqu’à la date de fin spécifiée par le paramètre [!UICONTROL Back Fill Until] ). Les lignes de données existantes pour les dates antérieures au 1er mars ne sont pas supprimées, mais elles ne sont pas actualisées. |
| [!UICONTROL Back Fill Until] | Date de fin pour laquelle les données existantes sur l’onglet [!UICONTROL RAW] sont actualisées, représentée par un nombre de jours dans le passé. La valeur par défaut est d’un (1) jour.<br><br>Par exemple, si cette valeur est de 1 et que la date d’aujourd’hui est le 7 mars, les données existantes sur l’onglet [!UICONTROL RAW] sont actualisées jusqu’au 6 mars (à partir de la date de début spécifiée par le paramètre [!UICONTROL Back Fill From] ). Si cette valeur est 1, le paramètre [!UICONTROL Back Fill Until] est 7 et que la date d’aujourd’hui est le 7 mars, les données existantes sur l’onglet [!UICONTROL RAW] sont actualisées du 1er au 6 mars. Dans les deux exemples, les lignes de données existantes pour les dates postérieures au 6 mars ne sont pas supprimées, mais elles ne sont pas actualisées. |
| [!UICONTROL Email Recipients] | Adresses électroniques auxquelles envoyer des notifications chaque fois que le rapport est actualisé ou chaque fois que le rapport est exécuté lorsque le modèle inclut un planning. Par défaut, l’adresse de votre compte utilisateur est renseignée. Pour spécifier plusieurs adresses, séparez-les par des virgules, des espaces ou de nouvelles lignes. |
| [!UICONTROL Schedule Time] | Heure à laquelle les flux de feuille de calcul sont actualisés : à 8h00 ou à toute heure entre 10h00 et 23h00 dans le fuseau horaire de l’annonceur. La valeur par défaut des nouveaux flux de feuille de calcul est 10 h 00.<br><br><b>Remarque : </b> Pour des raisons de performances, vous ne pouvez pas actualiser les flux de feuille de calcul à 9 h 00, lorsque d’autres rapports sont générés. |
| [!UICONTROL Email Notification] | (Lorsque les destinataires du courrier électronique sont spécifiés) Que inclure dans les notifications par courrier électronique à des adresses spécifiées :<ul><li><i>Joindre le flux</i> — Pour envoyer une copie du rapport complété au format XLSX. Si le fichier est supérieur à 10 Mo, la notification ne contient pas de pièce jointe.</li><li><i>Notification uniquement</i> (valeur par défaut) : pour envoyer uniquement une notification de la fin ou de l’échec du rapport, avec un lien vers le rapport.</li></ul> |

>[!MORELIKETHIS]
>
>* [À propos des flux de rapports de feuille de calcul](spreadsheet-feed-about.md)
>* [Créer un flux de rapport de feuille de calcul](spreadsheet-feed-create.md)
>* [ Créez un  [!DNL Excel] modèle pour un flux de rapport de feuille de calcul](spreadsheet-feed-create-excel-template.md)
>* [Modifier les paramètres du flux de rapports de feuille de calcul](spreadsheet-feed-edit.md)
>* [ Afficher ou enregistrer un fichier de flux de rapport de feuille de calcul ](spreadsheet-feed-view-or-save.md)
>* [Actualisation manuelle des flux de rapports de feuille de calcul](spreadsheet-feed-refresh.md)
>* [Supprimer des flux de rapports de feuille de calcul](spreadsheet-feed-delete.md)
