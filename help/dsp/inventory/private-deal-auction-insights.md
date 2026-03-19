---
title: Afficher les informations sur les enchères pour une transaction privée
description: Découvrez comment utiliser les informations sur les enchères pour analyser la composition des transactions d’une transaction privée.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: bbb99f6a-0276-4eb8-9607-75500d5634d9
source-git-commit: 54f69e4c0fa20b918a037cc5d2003d67db889913
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# Afficher les informations sur les enchères pour une transaction privée

Informations sur les enchères est un outil de dépannage qui vous permet d’analyser la composition des transactions privées garanties et non garanties. Grâce aux visualisations de données, cet outil affiche la tendance et les proportions relatives des valeurs reçues pour les [ attributs clés des enchères ](#auction-attributes) au cours d’une période spécifique.

1. Dans le menu principal, cliquez sur **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. Dans la ligne d&#39;opération, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Auction Insights]**.

>[!NOTE]
>
>Informations sur les enchères sont également disponibles via l’outil de [!UICONTROL Inspector] des emplacements. Pour les ouvrir, [ouvrez le [!UICONTROL Inspector]](/help/dsp/campaign-management/reports/placement-details-view.md) d&#39;emplacement sur le [!UICONTROL Inventory tab], puis cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Auction Insights]** dans la ligne d&#39;opération.

## Attributs d&#39;enchères {#auction-attributes}

Des graphiques en aires sont disponibles pour les attributs d&#39;enchères suivants :

* **Type d’annonce publicitaire :** type d’annonce publicitaire demandé dans la mise aux enchères (tel que Affichage ou Audio).

* **Navigateur :** navigateur à l’origine de la mise aux enchères (Chrome ou Firefox, par exemple).

* **OS :** système d’exploitation (SE) d’où provient la mise aux enchères (Android ou iOS, par exemple).

* **Type d’appareil :** appareil d’où provient la mise aux enchères (téléphone mobile ou bureau, par exemple).

* **Durée de l’annonce publicitaire :** durée maximale de l’annonce publicitaire demandée aux enchères (15 s ou 30 s, par exemple).

* **Sécurisé :** indique si la mise aux enchères nécessite une ressource de création d’URL HTTPS sécurisée. Valeurs : <i>Sécurisé</i> ou <i>Non sécurisé</i>.

* **Type MIME :** type MIME de contenu publicitaire demandé dans la mise aux enchères (mp4 ou mov, par exemple).

![informations sur les enchères](/help/dsp/assets/auction-insights.png)

>[!NOTE]
>
>Vous pouvez appliquer des filtres pour des valeurs d’attribut spécifiques afin d’affiner vos résultats.

>[!MORELIKETHIS]
>
>* [À propos de l&#39;inventaire privé](private-inventory-about.md)
>* [Spécifier des emplacements et des annonces pour un ID d’offre](deal-id-attach-placements.md)
>* [Afficher un rapport détaillé pour une affaire](deal-view-report.md)
>* [Types de rapports de performances dans les vues de gestion de campagnes](/help/dsp/campaign-management/reports/campaign-reports-about.md)
