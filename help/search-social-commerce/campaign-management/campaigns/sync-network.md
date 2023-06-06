---
title: Synchronisation manuelle des données du réseau publicitaire
description: Découvrez comment déclencher manuellement la synchronisation de votre structure de campagne et des entités de campagne pour les réseaux publicitaires pris en charge.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# Synchronisation manuelle des données du réseau publicitaire

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft® Advertising] (anciennement [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], et [!DNL Yandex] comptes uniquement*

La synchronisation est le processus par lequel Search, Social et Commerce rassemble les informations mises à jour des comptes réseau publicitaires de chaque annonceur sur [réseaux publicitaires pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). Ces données comprennent la structure de campagne et les entités de campagne de l’annonceur, y compris la plupart de leurs attributs qui sont gérés ou signalés dans Search, Social et Commerce. Elle n’inclut pas les données de clic, ni les offres et les modificateurs d’offre entrés en dehors de Search, Social et Commerce, qui sont regroupés séparément.

Search, Social et Commerce se synchronise automatiquement (se synchronise) avec vos comptes de réseau publicitaire une fois par jour, ainsi que chaque fois qu’il détecte une nouvelle campagne sur l’un de vos réseaux publicitaires. En outre, elle envoie immédiatement toutes les modifications apportées aux données de campagne depuis Search, Social et Commerce vers le réseau publicitaire.

Vous pouvez demander manuellement la synchronisation de toutes les campagnes principales et suspendues dans des comptes spécifiés ou dans des campagnes principales et suspendues spécifiques. Cette tâche rassemble sur le réseau publicitaire les entités nouvelles ou modifiées.

Pour les campagnes avec le[!UICONTROL Auto Upload]&quot;, l’opération de synchronisation génère et publie également les codes de suivi manquants ou qui doivent être modifiés dans les modèles de suivi ou les URL de destination. Les URL sont générées en fonction des paramètres définis dans les paramètres de tracking des paramètres du compte ou de la campagne. S’il existe des URL de suivi pour les éléments pertinents, elles ne sont pas regénérées tant que de nouvelles URL ne sont pas nécessaires (par exemple, si le type de correspondance du mot-clé, le texte créatif ou les paramètres de suivi du compte ont changé).

>[!NOTE]
>
>À tout moment [création d’une feuille d’envoi groupée](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), vous pouvez éventuellement vous synchroniser avec le réseau publicitaire avant la création de la feuille d’envoi groupé.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]>[!UICONTROL Campaigns]**. Dans le sous-menu, sélectionnez l’une des options suivantes : **[!UICONTROL Accounts]** pour synchroniser toutes les campagnes dans des comptes spécifiques ou **[!UICONTROL Campaigns]** pour synchroniser des campagnes spécifiques.

1. (Facultatif) Filtrez la liste pour inclure des comptes ou des campagnes spécifiques.

1. Cochez la case en regard de chaque compte ou campagne à synchroniser. Vous pouvez synchroniser jusqu’à 50 campagnes à la fois. Si vous synchronisez plus de cinq comptes à la fois, la tâche est divisée en lots allant jusqu’à cinq comptes chacun.

1. Cliquez sur **![Plus](/help/search-social-commerce/assets/more.png "Plus")** dans la barre d’outils, puis sélectionnez **[!UICONTROL Sync]**.

Vous pouvez suivre l’état de la tâche de synchronisation dans la [!UICONTROL Workspace] vue. L’affichage de la tâche peut prendre une heure ou plus.

>[!MORELIKETHIS]
>
>* [Téléchargement/création d’un fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)

