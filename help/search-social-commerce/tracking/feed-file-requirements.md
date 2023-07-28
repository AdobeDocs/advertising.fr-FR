---
title: Exigences liées aux fichiers de flux de conversion
description: Référencez les exigences relatives aux fichiers de flux de conversion.
exl-id: 7d865802-0ab9-4965-9618-6bc0667f4939
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '359'
ht-degree: 0%

---

# Exigences liées aux fichiers de flux de conversion

Vous trouverez ci-dessous les exigences relatives au format de fichier, aux champs de données obligatoires et facultatifs, au nom de fichier et au protocole de transfert de fichier pour les fichiers de flux.

## Format du fichier

Le fichier de données doit être au format texte plat (TXT), valeurs séparées par des virgules (CSV) ou valeurs séparées par des tabulations (TSV). Le fichier peut se composer d’une rangée d’en-tête et de rangées de données avec des valeurs séparées par des tabulations, des virgules ou un autre caractère (mais pas des espaces) :

* **Ligne d’en-tête :** (Facultatif) La première ligne du fichier est un en-tête qui spécifie les noms de champ (ou noms de colonne) requis dans un ordre spécifique, séparés par des tabulations ou des virgules. Les noms de colonne requis incluent les propriétés de transaction dont le suivi par Adobe Advertising est effectué en tant que conversions.

* **Lignes de données :** Chaque ligne suivante inclut des champs de données dans le même ordre que l’en-tête et séparés par des tabulations ou des virgules. Si le premier enregistrement n’est pas un en-tête, chaque ligne de données doit inclure tous les champs possibles, dans un ordre spécifié. Les valeurs de tous les identifiants et propriétés de transaction doivent être alphanumériques.

  Lorsque plusieurs clics sur une ou plusieurs publicités conduisent à une transaction, vous devez déterminer l’identifiant de clic et l’identifiant de suivi auxquels attribuer la transaction. Un identifiant unique étant signalé pour chaque transaction, vous pouvez mettre à jour des transactions individuelles.

## Convention d’appellation des fichiers

Le nom de fichier doit inclure la date et être cohérent. Par exemple, si vous utilisez le format YYYYMMDD.txt, un fichier envoyé le 15 mai 2011 doit être nommé 20110515.txt.

## Protocole de transfert de fichiers

Envoyez le fichier via le protocole de transfert SFTP, à l’aide du port 22. Vous devrez fournir vos informations de clé publique.  Votre équipe de compte d’Adobe ou l’équipe de mise en oeuvre vous indiqueront l’emplacement du serveur, ainsi que les informations d’identification requises pour que votre système puisse transférer les fichiers.

>[!TIP]
>
>Les flux de données de conversion sont traités plusieurs fois par jour. Chargez le flux quotidien dès que possible après minuit, heure locale, afin que l’Adobe Advertising puisse traiter vos données et les rendre disponibles dans l’interface utilisateur de création de rapports tôt le matin.

>[!MORELIKETHIS]
>
>* [Exigences de données pour les flux de données à l’aide des ID EF](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
>* [Exigences de données pour les flux de données à l’aide d’un ID de transaction](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
