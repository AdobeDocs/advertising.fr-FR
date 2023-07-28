---
title: Statuts des données générées à partir de flux
description: Découvrez les états des données générées à partir des flux de données d’inventaire.
exl-id: 8e5e7649-a16b-4634-896a-7c216185b367
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Statuts des données générées à partir de flux

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Chaque composant peut avoir l’un des états suivants :

* *[!UICONTROL New]:* Le composant n’existe pas sur le réseau publicitaire et n’a pas été publié sur le réseau publicitaire. Vous pouvez toujours modifier ses paramètres si nécessaire en cliquant sur le nom du composant. Lorsque vous êtes prêt à publier les données, cliquez sur **[!UICONTROL Post to SE]** et indiquez les données à envoyer.

* *[!UICONTROL Posted]:* (Campagnes et groupes publicitaires uniquement) La campagne ou le groupe publicitaire a été partiellement publié sur le réseau publicitaire, mais certains composants n’ont pas été publiés en raison d’erreurs. L’état de validation de chaque mot-clé et de chaque publicité indique les informations qui doivent être corrigées. Si nécessaire, vous pouvez modifier les paramètres du composant en cliquant sur le nom du composant.

* *[!UICONTROL Active]:* Le composant est déjà principal sur le réseau publicitaire et vous ne pouvez pas modifier ses paramètres ici. Les composants principaux peuvent inclure des sous-composants qui sont [!UICONTROL New], qui peut être publié si les données sont valides.

* *[!UICONTROL Paused]:* Le composant est déjà en pause sur le réseau publicitaire, et vous ne pouvez pas modifier ses paramètres ici. Les composants en pause peuvent inclure des sous-composants qui sont [!UICONTROL New], qui peut être publié si les données sont valides.

* *[!UICONTROL Deleted]:* Le composant a déjà été supprimé sur le réseau publicitaire et vous ne pouvez pas modifier ses paramètres ici. Les composants supprimés peuvent inclure des sous-composants [!UICONTROL New], qui peut être publié si les données sont valides.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Affichage des données générées à partir de flux](propagated-data-view.md)
>* [Modification des données générées à partir de flux](propagated-data-edit.md)
>* [Données de campagne de publication générées à partir de flux vers les réseaux publicitaires](propagated-data-post.md)
>* [Arrêt d’une tâche de publication pour les données de flux d’inventaire](stop-job.md)
