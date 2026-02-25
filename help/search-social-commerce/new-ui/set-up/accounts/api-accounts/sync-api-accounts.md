---
title: (Nouvelle interface utilisateur) Synchroniser manuellement les données réseau et
description: Découvrez comment déclencher manuellement la synchronisation de votre structure de campagne et de vos entités de campagne pour les réseaux publicitaires pris en charge à partir de la nouvelle interface utilisateur.
feature: Search Campaign Management
source-git-commit: 5e384445a35f81275eefeac660b31c1acdc785f3
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Synchronisation manuelle des données réseau et publicitaire via la connexion API

<!-- EDIT ALL -- FROM LEGACY UI -->

Comptes *[!DNL Google Ads], [!DNL Microsoft Advertising] (anciennement [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] et [!DNL Baidu] existants uniquement*

La synchronisation est le processus par lequel Search, Social et Commerce collecte des informations mises à jour pour les comptes de réseau publicitaire connectés de chaque annonceur sur les [réseaux publicitaires pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). Ces données incluent la structure de la campagne de l’annonceur et les entités de la campagne, y compris la plupart de leurs attributs gérés ou signalés dans Search, Social et Commerce. Elle n’inclut pas les données de clic, ni les offres et les modificateurs d’offres saisis en dehors des moteurs de recherche, des réseaux sociaux et de Commerce, qui sont rassemblés séparément.

Search, Social et Commerce se synchronise automatiquement avec vos comptes de réseau publicitaire une fois par jour, ainsi qu’à chaque fois qu’il détecte une nouvelle campagne sur l’un de vos réseaux publicitaires. En outre, il envoie immédiatement au réseau publicitaire toutes les modifications apportées aux données de la campagne à partir de Search, Social et Commerce.

Vous pouvez demander manuellement la synchronisation de toutes les campagnes actives et en pause dans des comptes spécifiés<!--Not available as of 2/23:  or in specific active and paused campaigns -->. Cette tâche rassemble les entités du réseau publicitaire qui sont nouvelles ou modifiées.

Pour les campagnes comportant l’option « [!UICONTROL Auto Update] », l’opération de synchronisation génère et publie également les codes de suivi manquants ou qui doivent être modifiés dans les modèles de suivi ou les URL de destination. Les URL sont générées en fonction des paramètres des paramètres de tracking de la campagne ou des paramètres du compte. S’il existe des URL de suivi pour les éléments pertinents, elles ne sont pas régénérées, sauf si de nouvelles URL sont nécessaires (par exemple, si le type de correspondance de mot-clé, le texte créatif ou les paramètres de suivi du compte ont changé).

>[!NOTE]
>
>Chaque fois que vous [créez une feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), vous pouvez éventuellement effectuer une synchronisation avec le réseau publicitaire avant la création de la feuille d’envoi groupé.

## Synchroniser les campagnes dans un compte réseau publicitaire

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

1. Cochez la case en regard du nom du compte.

   <!-- As of 2/23, you can sync only one acct at a time:  Select the check box next to each account or campaign that you want to sync. You can sync up to 50 campaigns at a time. If you sync more than five accounts at a time, the job is broken into batches of up to five accounts each. -->

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL ... More Actions]** > **[!UICONTROL Sync]**.

   * Placez le curseur sur le nom du compte, cliquez sur **...**, puis sur **[!UICONTROL Edit]**.

Vous pouvez suivre le statut de la tâche de synchronisation dans la vue [!UICONTROL Workspace]. Le travail peut prendre
une heure ou plus à apparaître.

>[!MORELIKETHIS]
>
>* [Télécharger/créer un fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
