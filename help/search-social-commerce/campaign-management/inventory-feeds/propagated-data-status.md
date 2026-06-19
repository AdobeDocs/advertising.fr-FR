---
title: Statuts des données générées à partir des flux
description: Découvrez les statuts des données générées à partir des flux de données d’inventaire.
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/3QPUheA0wIhk8aVqCcqeTGbgz9FdMUHstnpm5V8AXgE
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# Statuts des données générées à partir des flux

comptes *[!DNL Google Ads], [!DNL LY Ads] (actions de suppression uniquement), [!DNL Microsoft Advertising] et [!DNL Yandex] uniquement*

Chaque composant peut avoir l’un des statuts suivants :

* *[!UICONTROL New]:* le composant n’existe pas sur le réseau publicitaire et n’a pas été publié sur le réseau publicitaire. Vous pouvez toujours modifier ses paramètres si nécessaire en cliquant sur le nom du composant. Lorsque vous êtes prêt à publier les données, cliquez sur **[!UICONTROL Post to SE]** et spécifiez les données à envoyer.

* *[!UICONTROL Posted]:* (Campagnes et groupes publicitaires uniquement) La campagne ou le groupe publicitaire a été partiellement publié sur le réseau publicitaire, mais certains composants n’ont pas été publiés en raison d’erreurs. L’état de validation de chaque mot-clé et publicité indique les informations à corriger. Si nécessaire, vous pouvez modifier les paramètres du composant en cliquant sur son nom.

* *[!UICONTROL Active]:* Le composant est déjà actif sur le réseau publicitaire et vous ne pouvez pas modifier ses paramètres ici. Les composants actifs peuvent inclure des sous-composants [!UICONTROL New], qui peuvent être publiés si les données sont valides.

* *[!UICONTROL Paused]:* Le composant est déjà en pause sur le réseau publicitaire et vous ne pouvez pas modifier ses paramètres ici. Les composants en pause peuvent inclure des sous-composants [!UICONTROL New], qui peuvent être publiés si les données sont valides.

* *[!UICONTROL Deleted]:* Le composant a déjà été supprimé du réseau publicitaire et vous ne pouvez pas modifier ses paramètres ici. Les composants supprimés peuvent inclure des sous-composants [!UICONTROL New], qui peuvent être publiés si les données sont valides.

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](inventory-feeds-about.md)
>* [Afficher les données générées à partir des flux](propagated-data-view.md)
>* [Modifier les données générées à partir des flux](propagated-data-edit.md)
>* [Publier les données de campagne générées à partir des flux sur les réseaux publicitaires](propagated-data-post.md)
>* [Arrêter un traitement de validation des données de flux de stock](stop-job.md)
