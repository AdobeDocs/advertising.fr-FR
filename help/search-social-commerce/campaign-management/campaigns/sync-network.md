---
title: Synchronisation manuelle des données réseau et
description: Découvrez comment déclencher manuellement la synchronisation de votre structure de campagne et des entités de campagne pour les réseaux publicitaires pris en charge.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Synchronisation manuelle des données réseau et

Comptes *[!DNL Google Ads], [!DNL Microsoft Advertising] (anciennement [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] et [!DNL Baidu] existants uniquement*

La synchronisation est le processus par lequel Search, Social et Commerce collecte des informations mises à jour pour les comptes de réseau publicitaire connectés de chaque annonceur sur les [réseaux publicitaires pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). Ces données incluent la structure de la campagne de l’annonceur et les entités de la campagne, y compris la plupart de leurs attributs gérés ou signalés dans Search, Social et Commerce. Elle n’inclut pas les données de clic, ni les offres et les modificateurs d’offres saisis en dehors des moteurs de recherche, des réseaux sociaux et de Commerce, qui sont rassemblés séparément.

Search, Social et Commerce se synchronise automatiquement avec vos comptes de réseau publicitaire une fois par jour, ainsi qu’à chaque fois qu’il détecte une nouvelle campagne sur l’un de vos réseaux publicitaires. En outre, il envoie immédiatement au réseau publicitaire toutes les modifications apportées aux données de la campagne à partir de Search, Social et Commerce.

Vous pouvez demander manuellement la synchronisation de toutes les campagnes actives et en pause dans des comptes spécifiés ou dans des campagnes actives et en pause spécifiques. Cette tâche rassemble les entités du réseau publicitaire qui sont nouvelles ou modifiées.

Pour les campagnes comportant l’option « [!UICONTROL Auto Upload] », l’opération de synchronisation génère et publie également les codes de suivi manquants ou qui doivent être modifiés dans les modèles de suivi ou les URL de destination. Les URL sont générées en fonction des paramètres des paramètres de tracking de la campagne ou des paramètres du compte. S’il existe des URL de suivi pour les éléments pertinents, elles ne sont pas régénérées, sauf si de nouvelles URL sont nécessaires (par exemple, si le type de correspondance de mot-clé, le texte créatif ou les paramètres de suivi du compte ont changé).

>[!NOTE]
>
>Chaque fois que vous [créez une feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), vous pouvez éventuellement effectuer une synchronisation avec le réseau publicitaire avant la création de la feuille d’envoi groupé.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]>[!UICONTROL Campaigns]**. Dans le sous-menu, sélectionnez **[!UICONTROL Accounts]** pour synchroniser toutes les campagnes de comptes spécifiques ou **[!UICONTROL Campaigns]** pour synchroniser des campagnes spécifiques.

1. (Facultatif) Filtrez la liste pour inclure des comptes ou des campagnes spécifiques.

1. Cochez la case en regard de chaque compte ou campagne à synchroniser. Vous pouvez synchroniser jusqu’à 50 campagnes à la fois. Si vous synchronisez plus de cinq comptes à la fois, la tâche est divisée en lots de cinq comptes maximum chacun.

1. Cliquez sur ![**Plus**](/help/search-social-commerce/assets/more.png " Plus") dans la barre d’outils, puis sélectionnez **[!UICONTROL Sync]**.

Vous pouvez suivre le statut de la tâche de synchronisation dans la vue [!UICONTROL Workspace]. Le travail peut prendre
une heure ou plus à apparaître.

>[!MORELIKETHIS]
>
>* [Télécharger/créer un fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
