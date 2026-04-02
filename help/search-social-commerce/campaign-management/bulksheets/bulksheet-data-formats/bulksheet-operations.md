---
title: Opérations pouvant être effectuées dans des feuilles d’envoi groupé
description: Référencez des informations générales sur l’ajout, la modification et la suppression de données de campagne à l’aide de feuilles d’envoi groupé.
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/v0lNqlMXWFmw8O1Tr51d-WoHC-X2dxdSh-ZRKIPxGQY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 381
ht-degree: 0%

---

# Opérations pouvant être effectuées dans des feuilles d’envoi groupé

Vous pouvez ajouter, modifier et supprimer des données de campagne par le biais de feuilles d’envoi groupé pour les [réseaux publicitaires pris en charge](../bulksheet-about.md#bulksheet-functionality-by-network).

Incluez une ligne de données distincte pour chaque composant de campagne (campagne, groupe publicitaire, mot-clé ou publicité textuelle) que vous souhaitez ajouter, modifier ou supprimer, ou dont vous souhaitez ajouter, modifier ou supprimer les propriétés. Par exemple, si vous souhaitez créer une campagne avec un groupe publicitaire, un mot-clé et une publicité (quatre composants au total), vous avez besoin de quatre lignes de données distinctes. Toutefois, pour modifier le [!UICONTROL Ad Group Name] d’un groupe publicitaire (un composant), vous n’avez besoin que d’une seule ligne. De même, pour modifier quatre propriétés différentes pour un groupe publicitaire (un composant), vous n’avez besoin que d’une seule ligne.

Les règles suivantes s’appliquent à l’utilisation des composants de campagne et de leurs propriétés.

* Ajout :

   * Pour ajouter un composant, vous devez inclure tous les champs requis pour ajouter ce composant et éventuellement inclure des champs pour l’une des propriétés du composant.

   * Pour ajouter une propriété à un composant existant, comme le [!UICONTROL Ad Group End Date] d’un groupe publicitaire , incluez tous les champs requis pour modifier ce composant (groupe publicitaire) ainsi que le champ de la propriété ([!UICONTROL Ad Group End Date]).

* Pour modifier une propriété pour un composant existant, incluez tous les champs requis pour modifier ce composant, ainsi que le champ de la propriété.

  Si vous laissez le champ de propriété vide, la valeur existante est conservée.

* Suppression :

   * Pour supprimer un composant existant, incluez tous les champs requis pour modifier ce composant et modifier son statut en [!UICONTROL Deleted]. Par exemple, pour supprimer un groupe publicitaire [!DNL Google Ads], vous devez inclure les [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] avec une valeur de <i>[!UICONTROL Deleted]</i> et [!UICONTROL Ad Group ID].

   * (Valeurs [!UICONTROL Param1], [!UICONTROL Param2] et [!UICONTROL Param3] uniquement) Pour supprimer une valeur [!DNL paramN] existante pour un mot-clé, incluez tous les champs requis pour modifier le mot-clé et supprimez également la valeur [!DNL paramN] existante en saisissant la valeur `[delete]` (y compris les crochets) dans le champ correspondant.

   * (Champs de propriété autorisés) Pour supprimer une valeur de propriété existante pour un composant, incluez tous les champs requis pour modifier ce composant et supprimez également la valeur de propriété en saisissant la valeur `[delete]` (y compris les crochets). Les champs autorisés sont les suivants :

      * ([!UICONTROL Google Ads] uniquement) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] et [!DNL Microsoft Advertising] uniquement) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Lorsque vous incluez dans un champ une valeur qui n’est pas applicable à l’action, toute valeur saisie dans le champ est ignorée.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l&#39;aide de feuilles d&#39;envoi groupé](../bulksheet-about.md)
>* [Formats de fichiers de feuilles d’envoi groupé pris en charge](bulksheet-file-formats.md)
>* [Annexe - Erreurs de feuille d’envoi groupé](../bulksheet-errors.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](../bulksheet-download.md)
