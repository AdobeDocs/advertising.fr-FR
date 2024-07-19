---
title: Paramètres de destination du rapport
description: Consultez les détails requis pour les destinations de votre rapport, par type de destination.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Paramètres de destination du rapport

Les détails requis pour les destinations de rapport hors courrier électronique varient en fonction du type de destination.

>[!NOTE]
>
> Vous pouvez également envoyer vos rapports personnalisés aux destinataires par e-mail, qui ne nécessitent pas de destination de rapport enregistrée. Dans les paramètres du rapport, vous pouvez spécifier des destinataires de courrier électronique plutôt que des destinations enregistrées.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Nom qui vous aide à identifier la destination.

**[!UICONTROL S3 Bucket URL]:** chemin d’accès complet au dossier du compartiment [!DNL Amazon Simple Storage Service] (S3) vers lequel le rapport est téléchargé. Exemple : `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** ID de clé d’accès au compartiment ([!DNL Amazon S3]) (fourni par [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** Clé d’accès secrète au compartiment ([!DNL Amazon S3]) (fournie par [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Nom qui vous aide à identifier la destination.

**[!UICONTROL Server]:** nom d’hôte du serveur.

**[!UICONTROL Port]:** numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** nom d’utilisateur pour se connecter au serveur.

**[!UICONTROL Password]:** mot de passe pour se connecter au serveur.

**[!UICONTROL Path (Optional)]:** Chemin d’accès au serveur vers lequel les fichiers sont chargés.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Nom qui vous aide à identifier la destination.

**[!UICONTROL Server]:** nom d’hôte du serveur.

**[!UICONTROL Port]:** numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** nom d’utilisateur pour se connecter au serveur.

**[!UICONTROL Password]:** mot de passe pour se connecter au serveur.

**[!UICONTROL Path (Optional)]:** Chemin d’accès au serveur vers lequel les fichiers sont chargés.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Nom qui vous aide à identifier la destination.

**[!UICONTROL Server]:** nom d’hôte du serveur.

**[!UICONTROL Port]:** numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** nom d’utilisateur pour se connecter au serveur.

**[!UICONTROL Password]:** mot de passe pour se connecter au serveur.

**[!UICONTROL Path (Optional)]:** Chemin d’accès au serveur vers lequel les fichiers sont chargés.

>[!MORELIKETHIS]
>
>* [À propos de [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Créer un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Modifier un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Supprimer un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
