---
title: Opérations que vous pouvez effectuer dans des feuilles d’envoi groupées
description: Référencez des informations générales sur l’ajout, la modification et la suppression de données de campagne à l’aide de feuilles d’envoi groupées.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# Opérations que vous pouvez effectuer dans des feuilles d’envoi groupées

Vous pouvez ajouter, modifier et supprimer des données de campagne au moyen de feuilles d’envoi groupé pour [réseaux publicitaires pris en charge](../bulksheet-about.md#bulksheet-functionality-by-network).

Incluez une ligne de données distincte pour chaque composant de campagne (campagne, groupe publicitaire, mot-clé ou publicité texte) que vous souhaitez ajouter, modifier ou supprimer ; ou dont vous souhaitez ajouter, modifier ou supprimer des propriétés. Par exemple, si vous souhaitez créer une campagne avec un groupe publicitaire, un mot-clé et une publicité (quatre composants au total), vous avez besoin de quatre lignes de données distinctes. Pour modifier la variable [!UICONTROL Ad Group Name] pour un groupe d’annonces (un composant), il suffit toutefois d’une seule ligne. De même, pour modifier quatre propriétés différentes pour un groupe d’annonces (un composant), vous n’avez besoin que d’une ligne.

Les règles suivantes s’appliquent à l’utilisation des composants de campagne et de leurs propriétés.

* Ajouter :

   * Pour ajouter un composant, incluez tous les champs requis pour l’ajout de ce composant, ainsi que éventuellement des champs pour l’une des propriétés du composant.

   * Pour ajouter une propriété pour un composant existant, par exemple : [!UICONTROL Ad Group End Date] pour un groupe publicitaire, incluez tous les champs nécessaires pour modifier ce composant (groupe publicitaire) plus le champ pour la propriété ([!UICONTROL Ad Group End Date]).

* Pour modifier une propriété d’un composant existant, incluez tous les champs requis pour modifier ce composant, ainsi que le champ de la propriété.

   Si vous laissez le champ de propriété vide, la valeur existante est conservée.

* Suppression :

   * Pour supprimer un composant existant, incluez tous les champs requis pour le modifier et modifiez son état en [!UICONTROL Deleted]. Par exemple, pour supprimer une [!DNL Google Ads] groupe publicitaire, vous devez inclure la variable [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] avec la valeur <i>[!UICONTROL Deleted]</i>, et [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2], et [!UICONTROL Param3] uniquement) Pour supprimer une valeur existante [!DNL paramN] pour un mot-clé, incluez tous les champs nécessaires à la modification du mot-clé et supprimez également la valeur existante. [!DNL paramN] en saisissant la valeur `[delete]` (y compris les crochets) dans le champ correspondant.

   * (Champs de propriété autorisés) Pour supprimer une valeur de propriété existante pour un composant, incluez tous les champs requis pour modifier ce composant et supprimez également la valeur de propriété en saisissant la valeur . `[delete]` (y compris les crochets). Les champs autorisés sont les suivants :

      * ([!UICONTROL Google Ads] uniquement) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] et [!DNL Microsoft® Advertising] uniquement) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>Lorsque vous insérez une valeur dans un champ qui n’est pas applicable à l’action, toute valeur saisie dans le champ est ignorée.

>[!MORELIKETHIS]
>
>* [A propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](../bulksheet-about.md)
>* [Formats de fichiers de feuille d’envoi groupé pris en charge](bulksheet-file-formats.md)
>* [Annexe : Erreurs de feuilles d’envoi groupé](../bulksheet-errors.md)
>* [Téléchargement/création d’un fichier de feuille d’envoi groupé](../bulksheet-download.md)

