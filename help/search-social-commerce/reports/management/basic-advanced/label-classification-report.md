---
title: '[!UICONTROL Label Classification Report]'
description: En savoir plus sur le [!UICONTROL Label Classification Report].
exl-id: 847fa384-b9c6-446f-9ebf-da7679ed35ae
feature: Search Reports, Search Basic Reports
TQID: https://experienceleague.adobe.com/75t5C8Cz-EE5vsPYYXHWHSE-6ZDhwSQaEgtAdirYHQU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# [!UICONTROL Label Classification Report]

Le [!UICONTROL Label Classification Report] comprend des données de coût, de clic et (éventuellement) de conversion par classification de libellé au niveau des mots-clés ou des annonces agrégées sur les réseaux publicitaires, les comptes, les campagnes ou les groupes publicitaires. Par défaut, les données incluent une ligne pour chaque classification de libellés au niveau des mots-clés applicable pour les mots-clés, les annonces et les emplacements qui ont reçu des impressions pour chaque unité de temps dans la période spécifiée. Les lignes sont dans l’ordre croissant, d’abord par date de début pour l’unité de temps, puis par classification de libellés, et enfin par valeur de libellé, par défaut.

Vous pouvez afficher les données des 36 mois précédents.

>[!NOTE]
>
>* Le compte rendu des performances par classification de libellé au niveau de l’annonce n’est pas disponible pour les campagnes d’annonces de recherche dynamique (DSA) [!DNL Microsoft Advertising].
>* Plusieurs classifications de libellés peuvent s’appliquer à la même entité, de sorte que le total de chaque mesure peut être supérieur au total réel de l’entité. Par exemple, supposons qu’un mot-clé « chaussures en daim » possède deux valeurs d’étiquette, « daim » et « chaussures », et que le mot-clé ait reçu 100 clics. La colonne Clics affichait « 100 » pour chacune de ces valeurs d’étiquette. Le total des deux lignes était donc « 200 ».
>* Toute modification apportée aux classifications d’étiquettes et aux valeurs d’étiquettes enfants d’une entité est visible en une heure environ.

## Colonnes par défaut

Pour la description de toutes les colonnes par défaut et personnalisées, voir « [Colonnes de rapport pour les rapports de base et avancés](basic-advanced-report-columns.md) ».

* [!UICONTROL Label Classification]
* [!UICONTROL Label Value]
* [!UICONTROL Start Date]
* [!UICONTROL End Date]
* [!UICONTROL Impressions]
* [!UICONTROL Cost]
* [!UICONTROL Clicks]
* [!UICONTROL CPC]
* [!UICONTROL Avg Position]
* [!UICONTROL Impr. (Abs. Top) %]
* [!UICONTROL Impr. (Top) %]

>[!MORELIKETHIS]
>
>* [À propos des rapports de base et avancés](basic-advanced-report-about.md)
>* [Générer un rapport de base ou avancé](basic-advanced-report-generate.md)
>* [Paramètres de rapport de base et avancés](basic-advanced-report-settings.md)
