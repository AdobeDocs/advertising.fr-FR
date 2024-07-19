---
title: Synchronisation manuelle des données du réseau publicitaire
description: Découvrez comment déclencher manuellement la synchronisation de votre structure de campagne et des entités de campagne pour les réseaux publicitaires pris en charge.
exl-id: 185c6a01-c2e8-4bbb-a9dd-0a8200eb4792
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# Synchronisation manuelle des données du réseau publicitaire

*[!DNL Google Ads], [!DNL Microsoft Advertising] (anciennement [!DNL Bing Ads]), [!DNL Yahoo! Japan Ads], [!DNL Yandex] et comptes [!DNL Baidu] existants uniquement*

La synchronisation est le processus par lequel Search, Social et Commerce rassemble des informations mises à jour pour les comptes réseau d’annonces connectés de chaque annonceur sur les [réseaux d’annonces pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). Ces données comprennent la structure de campagne et les entités de campagne de l’annonceur, y compris la plupart de ses attributs qui sont gérés ou signalés dans Search, Social et Commerce. Elle n’inclut pas les données de clic, ni les offres et les modificateurs d’offre entrés en dehors de Search, Social et Commerce, qui sont regroupés séparément.

Search, Social et Commerce se synchronise automatiquement (se synchronise) avec vos comptes de réseau publicitaire une fois par jour, ainsi que chaque fois qu’il détecte une nouvelle campagne sur l’un de vos réseaux publicitaires. En outre, elle envoie immédiatement toutes les modifications apportées aux données de campagne depuis Search, Social et Commerce vers le réseau publicitaire.

Vous pouvez demander manuellement la synchronisation de toutes les campagnes actives et en pause dans des comptes spécifiés ou dans des campagnes actives et en pause spécifiques. Cette tâche rassemble sur le réseau publicitaire les entités nouvelles ou modifiées.

Pour les campagnes avec l’option &quot;[!UICONTROL Auto Upload]&quot;, l’opération de synchronisation génère et publie également les codes de suivi manquants ou qui doivent être modifiés dans les modèles de suivi ou les URL de destination. Les URL sont générées en fonction des paramètres définis dans les paramètres de tracking des paramètres du compte ou de la campagne. S’il existe des URL de suivi pour les éléments pertinents, elles ne sont pas regénérées tant que de nouvelles URL ne sont pas nécessaires (par exemple, si le type de correspondance du mot-clé, le texte créatif ou les paramètres de suivi du compte ont changé).

>[!NOTE]
>
>Chaque fois que vous [créez une feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md), vous pouvez éventuellement vous synchroniser avec le réseau publicitaire avant la création de la feuille d’envoi groupé.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]>[!UICONTROL Campaigns]**. Dans le sous-menu, sélectionnez **[!UICONTROL Accounts]** pour synchroniser toutes les campagnes dans des comptes spécifiques ou **[!UICONTROL Campaigns]** pour synchroniser des campagnes spécifiques.

1. (Facultatif) Filtrez la liste pour inclure des comptes ou des campagnes spécifiques.

1. Cochez la case en regard de chaque compte ou campagne à synchroniser. Vous pouvez synchroniser jusqu’à 50 campagnes simultanément. Si vous synchronisez plus de cinq comptes à la fois, la tâche est divisée en lots de cinq comptes au maximum.

1. Cliquez sur **![Plus](/help/search-social-commerce/assets/more.png "Plus")** dans la barre d’outils, puis sélectionnez **[!UICONTROL Sync]**.

Vous pouvez suivre l’état de la tâche de synchronisation dans la vue [!UICONTROL Workspace]. La tâche peut être effectuée
une heure ou plus s’affiche.

>[!MORELIKETHIS]
>
>* [Télécharger/créer un fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)
