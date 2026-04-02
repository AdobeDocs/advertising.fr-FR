---
title: Afficher les informations sur les enchères pour une transaction privée
description: Découvrez comment utiliser les informations sur les enchères pour analyser la composition des transactions d’une transaction privée.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: bbb99f6a-0276-4eb8-9607-75500d5634d9
TQID: https://experienceleague.adobe.com/KtjLaASMlY0toMM1hvcWchd-D8kJzdvNBwfeGOGyyYE
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# Afficher les informations sur les enchères pour une transaction privée

Informations sur les enchères est un outil de dépannage qui vous permet d’analyser la composition des transactions privées garanties et non garanties. Grâce aux visualisations de données, cet outil affiche la tendance et les proportions relatives des valeurs reçues pour les [&#x200B; attributs clés des enchères &#x200B;](#auction-attributes) au cours d’une période spécifique.

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
