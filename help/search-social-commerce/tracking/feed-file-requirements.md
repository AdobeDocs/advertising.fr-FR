---
title: Exigences relatives aux fichiers de flux de conversion
description: Référencez les exigences relatives aux fichiers de flux de conversion.
exl-id: abc28394-3e00-447f-a04e-078fa9883a64
feature: Search Tracking
TQID: https://experienceleague.adobe.com/y5kEsTB71WWQE6RGYdsIq0GFuZI037tRbRQTwuOP8aM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 0%

---

# Exigences relatives aux fichiers de flux de conversion

Vous trouverez ci-dessous les exigences relatives au format de fichier, aux champs de données obligatoires et facultatifs, au nom de fichier et au protocole de transfert de fichier pour les fichiers de flux.

## Format de fichier

Le fichier de données doit être au format texte plat (TXT), valeurs séparées par des virgules (CSV) ou valeurs séparées par des tabulations (TSV). Le fichier peut se composer d’une ligne d’en-tête et de lignes de données avec des valeurs séparées par des tabulations, des virgules ou un autre caractère (mais pas des espaces) :

* **Ligne d’en-tête :** (facultatif) la première ligne du fichier est un en-tête qui spécifie les noms de champ (ou de colonne) dans un ordre spécifique, séparés par des tabulations ou des virgules. Les noms de colonne obligatoires incluent les mesures de conversion suivies par Adobe Advertising en tant que conversions.

* **Lignes de données :** chaque ligne suivante inclut des champs de données dans le même ordre que l’en-tête et séparés par des tabulations ou des virgules. Si le premier enregistrement n’est pas un en-tête, chaque ligne de données doit inclure tous les champs possibles, dans un ordre spécifié. Les valeurs de tous les identifiants et de toutes les mesures de conversion doivent être alphanumériques.

  Lorsque plusieurs clics sur une ou plusieurs publicités entraînent une transaction, vous devez déterminer l’identifiant de clic et l’identifiant de suivi auxquels attribuer la transaction. Étant donné qu&#39;un ID unique est indiqué pour chaque transaction, vous pouvez mettre à jour des transactions individuelles.

## Convention de dénomination des fichiers

Le nom du fichier doit inclure la date et être cohérent. Par exemple, si vous utilisez le format AAAAMMJJ.txt, un fichier envoyé le 15 mai 2011 doit être nommé 20110515.txt.

## Protocole de transfert de fichier

Envoyez le fichier via le protocole de transfert SFTP, à l’aide du port 22. Vous devrez fournir vos informations de clé publique.  L’équipe du compte Adobe ou l’équipe d’implémentation vous fournit l’emplacement du serveur ainsi que les informations d’identification requises pour que votre système transfère les fichiers.

>[!TIP]
>
>Les flux de données de conversion sont traités plusieurs fois par jour. Chargez le flux quotidien dès que possible après minuit:00 heure locale, afin qu’Adobe Advertising puisse traiter vos données et les rendre disponibles dans l’interface utilisateur de création de rapports tôt le matin.

>[!MORELIKETHIS]
>
>* [Exigences en matière de données pour les flux de données utilisant des identifiants EF](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Exigences de données pour les flux de données utilisant un ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
