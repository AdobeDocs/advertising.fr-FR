---
title: Paramètres de destination du rapport
description: Affichez les détails requis pour vos destinations de rapport, par type de destination.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# Paramètres de destination du rapport

Les détails requis pour les destinations de rapports autres que les e-mails varient selon le type de destination.

>[!NOTE]
>
> Vous pouvez également diffuser vos rapports personnalisés aux destinataires des e-mails, qui n’ont pas besoin d’une destination de rapport enregistrée. Vous pouvez spécifier des destinataires d’e-mail, au lieu des destinations enregistrées, dans les paramètres du rapport.

## [!UICONTROL S3]

**[!UICONTROL Name]:** Nom permettant d’identifier la destination.

**[!UICONTROL S3 Bucket URL]:** chemin d’accès complet au dossier sur le compartiment [!DNL Amazon Simple Storage Service] (S3) vers lequel le rapport est chargé. Exemple : `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** identifiant de clé d’accès au compartiment ([!DNL Amazon S3]) (fourni par [!DNL Amazon]).

**[!UICONTROL Secret Access Key]:** clé d’accès secrète au compartiment ([!DNL Amazon S3]) (fournie par [!DNL Amazon]).

## [!UICONTROL FTP]

**[!UICONTROL Name]:** Nom permettant d’identifier la destination.

**[!UICONTROL Server]:** nom d’hôte du serveur.

**[!UICONTROL Port]:** numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** nom d’utilisateur pour la connexion au serveur.

**[!UICONTROL Password]:** mot de passe de connexion au serveur.

**[!UICONTROL Path (Optional)]:** chemin d’accès au serveur vers lequel les fichiers sont chargés.

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** Nom permettant d’identifier la destination.

**[!UICONTROL Server]:** nom d’hôte du serveur.

**[!UICONTROL Port]:** numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** nom d’utilisateur pour la connexion au serveur.

**[!UICONTROL Password]:** mot de passe de connexion au serveur.

**[!UICONTROL Path (Optional)]:** chemin d’accès au serveur vers lequel les fichiers sont chargés.

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** Nom permettant d’identifier la destination.

**[!UICONTROL Server]:** nom d’hôte du serveur.

**[!UICONTROL Port]:** numéro de port à utiliser sur le serveur. La valeur par défaut est *[!UICONTROL 21]*.

**[!UICONTROL Username]:** nom d’utilisateur pour la connexion au serveur.

**[!UICONTROL Password]:** mot de passe de connexion au serveur.

**[!UICONTROL Path (Optional)]:** chemin d’accès au serveur vers lequel les fichiers sont chargés.

>[!MORELIKETHIS]
>
>* [À propos des [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Créer un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Modification d’un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Supprimer un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
