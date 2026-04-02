---
title: Paramètres de destination des rapports
description: Affichez les détails requis pour vos destinations de rapport, par type de destination.
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
TQID: https://experienceleague.adobe.com/VB5UY9vm147LQJMKKyGOlhZdNcq6mVDYTT0Ef4RcwVs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: cc3b7f3c-58f0-4ba4-b808-391002930fd4
  - id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 0%

---

# Paramètres de destination des rapports

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
>* [À propos des destinations de rapport](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [Créer une destination de rapport](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [Modification d’un [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [Supprimer une destination de rapport](/help/dsp/reports/report-destinations/report-destination-delete.md)
