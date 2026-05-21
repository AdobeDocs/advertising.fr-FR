---
title: (Nouvelle interface utilisateur) Accès FTP aux rapports
description: Découvrez comment recevoir des rapports à un emplacement FTP en lecture seule.
feature: Search Reports
source-git-commit: 639037683053009ce653dee6d7c1e4eb80abf4d8
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Accès FTP aux rapports

Vous pouvez éventuellement recevoir des rapports à un emplacement FTP en lecture seule, à partir duquel vous pouvez récupérer les fichiers pour d’autres processus automatisés (par exemple, pour analyser les données avec un autre programme). Tous les rapports de base, à l’exception de [!UICONTROL Search Engine Account Report], et tous les rapports avancés peuvent être envoyés vers un emplacement FTP sous la forme de fichiers TSV compressés (valeur par défaut) ou de fichiers CSV, avec une extension de fichier .ZIP. Tous les en-têtes de fichier TSV ou CSV sont inclus et ne peuvent pas être supprimés.

L’accès FTP aux rapports nécessite l’accès à un compte FTP spécifié et vous devez configurer des modèles de rapport à l’aide d’une convention de nommage et d’un planning spécifiques.

## Configuration d’un compte FTP pour l’accès aux rapports

* Contactez l’équipe chargée de votre compte Adobe pour configurer un compte FTP afin d’accéder aux rapports.

  L’équipe vous fournit votre nom d’utilisateur et votre mot de passe.

## Configurer des modèles de rapport pour la diffusion FTP

Pour générer des rapports dans le répertoire FTP désigné, créez un modèle de rapport [report](report-templates-manage.md) avec les conventions de nommage et le planning suivants.

>[!NOTE]
>
>Tous les rapports avancés et tous les rapports de base, à l’exception du [!UICONTROL Search Engine Account Report], peuvent être diffusés vers un emplacement FTP.

1. Dans le modèle de rapport, incluez les informations suivantes n’importe où dans le nom du modèle :

   * `FTP` (en majuscules).

   * (Facultatif) L’un des trois systèmes de dates, en utilisant la syntaxe sensible à la casse suivante, y compris les crochets :

      * `[TODAY]` — Pour inclure la date, l&#39;heure et la minute d&#39;exécution du rapport. Comme l’heure exacte est incluse, le même modèle peut être exécuté plusieurs fois par jour sans remplacer le rapport précédent.

      * `[SDATE]` — Pour inclure la date de début de la période du rapport.

      * `[EDATE]` — Pour inclure la date de fin de la période du rapport.

   * (Facultatif) `[CSV]` (en lettres majuscules et entre crochets) de créer des fichiers au format CSV plutôt qu’au format TSV par défaut.

   Exemple : `[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]` créez un fichier tel que 202305051656-Portfolio-FTP-20230428-20110504.csv.

1. Planifiez l’exécution du rapport à une heure spécifique.

   Les rapports sont envoyés au compte FTP dans l’heure qui suit leur achèvement.

>[!NOTE]
>
>* Pour envoyer les rapports terminés par e-mail, il vous suffit d’entrer les adresses de tous les destinataires de l’e-mail lorsque vous générez le rapport ou le modèle.
>* Les rapports sont exécutés selon leurs plannings spécifiés et sont envoyés au compte FTP dans l’heure qui suit leur achèvement.

## Accès aux rapports dans un référentiel FTP

Pour accéder à vos rapports, connectez-vous à l’un des hôtes FTP suivants en utilisant la connexion de votre compte FTP (`amo<userID>rpt`, tel que amo1234rpt) et un mot de passe ou une clé de connexion privée si elle est configurée :

* Clients internationaux : `ftp3.adobe.net`
* Clients américains : `ftp5.adobe.net`

>[!NOTE]
>
>Le référentiel de rapports est en lecture seule et est purgé tous les 15 jours.

>[!MORELIKETHIS]
>
>* [Gérer les modèles de rapport](/help/search-social-commerce/new-ui/reports/report-templates-manage.md)
