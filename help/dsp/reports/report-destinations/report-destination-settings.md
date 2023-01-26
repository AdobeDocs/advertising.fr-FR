---
title: Paramètres de destination du rapport
description: Consultez les détails requis pour les destinations de votre rapport, par type de destination.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Paramètres de destination du rapport

Les détails requis pour les destinations de rapport hors courrier électronique varient en fonction du type de destination.

>[!NOTE]
>
> Vous pouvez également envoyer vos rapports personnalisés aux destinataires par e-mail, qui ne nécessitent pas de destination de rapport enregistrée. Dans les paramètres du rapport, vous pouvez spécifier des destinataires de courrier électronique plutôt que des destinations enregistrées.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Un nom qui vous aide à identifier la destination.

**[!UICONTROL S3 Bucket URL]:** Chemin d’accès complet au dossier sur la [!DNL Amazon Simple Storage Service] (S3) vers lequel le rapport sera chargé. Exemple : `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** L’identifiant de clé d’accès à ([!DNL Amazon S3]) (fourni par [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** Clé d’accès secrète à la fonction ([!DNL Amazon S3]) (fourni par [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Un nom qui vous aide à identifier la destination.

**[!UICONTROL Server]:** Nom d’hôte du serveur.

**[!UICONTROL Port]:** Numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nom d’utilisateur auquel se connecter au serveur.

**[!UICONTROL Password]:** Mot de passe de connexion au serveur.

**[!UICONTROL Path (Optional)]:** Chemin d’accès au serveur vers lequel les fichiers seront chargés.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Un nom qui vous aide à identifier la destination.

**[!UICONTROL Server]:** Nom d’hôte du serveur.

**[!UICONTROL Port]:** Numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nom d’utilisateur auquel se connecter au serveur.

**[!UICONTROL Password]:** Mot de passe de connexion au serveur.

**[!UICONTROL Path (Optional)]:** Chemin d’accès au serveur vers lequel les fichiers seront chargés.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Un nom qui vous aide à identifier la destination.

**[!UICONTROL Server]:** Nom d’hôte du serveur.

**[!UICONTROL Port]:** Numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** Nom d’utilisateur auquel se connecter au serveur.

**[!UICONTROL Password]:** Mot de passe de connexion au serveur.

**[!UICONTROL Path (Optional)]:** Chemin d’accès au serveur vers lequel les fichiers seront chargés.

>[!MORELIKETHIS]
>
>* [A propos [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Créez un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Modifier une [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Suppression d’une [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)

