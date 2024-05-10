---
title: Accès FTP aux rapports
description: Découvrez comment recevoir des rapports à un emplacement FTP en lecture seule.
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# Accès FTP aux rapports

Vous pouvez éventuellement recevoir des rapports à un emplacement FTP en lecture seule, à partir duquel vous pouvez récupérer les fichiers pour des processus automatisés supplémentaires (par exemple, pour analyser les données avec un autre programme). Tous les rapports de base sauf [!UICONTROL Search Engine Account Report] et tous les rapports avancés peuvent être diffusés vers un emplacement FTP sous la forme de fichiers TSV compressés (valeur par défaut) ou CSV, avec une extension de fichier .ZIP. Les en-têtes de fichier TSV ou CSV sont inclus et ne peuvent pas être supprimés.

L’accès FTP aux rapports nécessite l’accès à un compte FTP spécifié. Vous devez également configurer des modèles de rapport à l’aide d’une convention d’affectation des noms et d’un calendrier spécifiques.

## Configuration d’un compte FTP pour l’accès aux rapports

* Contactez votre équipe de compte d’Adobe pour configurer un compte FTP pour l’accès aux rapports.

  L’équipe vous fournit votre nom d’utilisateur et votre mot de passe.

## Configurer des modèles de rapport pour une diffusion FTP

Pour générer des rapports dans votre répertoire FTP désigné, créez une [modèle de rapport](templates/template-create.md) avec les conventions d’affectation des noms et la planification suivantes.

>[!NOTE]
>
>Tous les rapports avancés et tous les rapports de base, à l’exception de [!UICONTROL Search Engine Account Report] peut être diffusé vers un emplacement FTP.

1. Dans le modèle de rapport, incluez les informations suivantes n’importe où dans le nom du modèle :

   * `FTP` (en majuscules).

   * (Facultatif) L’une des trois dates système, en utilisant la syntaxe sensible à la casse suivante, y compris les crochets :

      * `[TODAY]` — Pour inclure la date, l’heure et la minute d’exécution du rapport. Comme cela inclut l’heure exacte, le même modèle peut être exécuté plusieurs fois par jour sans remplacer le rapport précédent.

      * `[SDATE]` — Pour inclure la date de début de la période du rapport.

      * `[EDATE]` — Pour inclure la date de fin de la période du rapport.

   * (Facultatif) `[CSV]` (en majuscules et entre crochets) pour créer des fichiers au format CSV plutôt qu’au format TSV par défaut.

   Exemple : `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` crée un fichier tel que 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Planifiez l’exécution du rapport à une heure spécifique.

   Les rapports sont envoyés au compte FTP dans l’heure qui suit leur exécution.

>[!NOTE]
>
>* Pour envoyer par email des rapports terminés, il vous suffit de saisir les adresses de tous les destinataires de l&#39;email lors de la génération du rapport ou du modèle.
>* Les rapports sont exécutés conformément aux calendriers spécifiés et sont envoyés au compte FTP dans l’heure qui suit leur exécution.

## Accès aux rapports dans un référentiel FTP

Pour accéder à vos rapports, connectez-vous à l’un des hôtes FTP suivants à l’aide de la connexion à votre compte FTP (`amo<userID>rpt`, par exemple amo1234rpt) et un mot de passe ou une clé de connexion privée si celle-ci est configurée :

* Clients internationaux : `ftp3.adobe.net`
* Clients des États-Unis : `ftp5.adobe.net`

>[!NOTE]
>
>Le référentiel des rapports est en lecture seule et purgé tous les 15 jours.


>[!MORELIKETHIS]
>
>* [Créer un modèle de rapport](/help/search-social-commerce/reports/automation/templates/template-create.md)
