---
title: Affectation de valeurs de classification à des composants de compte à l’aide de feuilles d’envoi groupées
description: Découvrez comment utiliser des feuilles d’envoi groupé pour affecter des valeurs de classification aux composants du compte.
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Affectation de valeurs de classification à des composants de compte à l’aide de feuilles d’envoi groupées

Vous pouvez associer des classifications d’étiquettes aux valeurs des entités de recherche suivantes à l’aide de feuilles d’envoi groupées : campagne, groupe publicitaire, mot-clé, publicité, emplacement, groupe de produits au niveau de l’unité et cible de recherche dynamique. Chaque classification d’étiquettes peut comporter jusqu’à 2 000 valeurs.

Chaque entité peut avoir une valeur d’étiquette par classification. Par exemple, Shoes_Campaign peut avoir une valeur Color de &quot;red&quot; et une valeur Geo de &quot;Los Angeles&quot;, mais il ne peut pas avoir plusieurs valeurs pour Color ou Geo.

Les valeurs d’étiquette sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

>[!NOTE]
>
>Les mots-clés et la copie de publicités pour certains réseaux publicitaires et types de campagne sont [non modifiable](/help/search-social-commerce/campaign-management/faqs-campaigns.md), ce qui signifie que leur modification supprime l’entité existante et en crée une nouvelle. Lorsqu’une entité existante est ainsi supprimée, la classification de libellés n’est pas affectée à la nouvelle entité.

1. [Téléchargez une feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) qui comprend les entités auxquelles vous souhaitez affecter des valeurs de classification d’étiquettes :

   * Sur l’onglet [!UICONTROL Rows and Columns] , développez la liste [!UICONTROL Campaign] dans le volet [!UICONTROL Bulksheet Columns].

   * Développez la liste [!UICONTROL Label Classification].

   * Sélectionnez chaque classification pour laquelle vous souhaitez inclure une colonne dans le fichier de feuille d’envoi groupé.

     Par exemple, si vous incluez les classifications de libellés &quot;Couleur&quot; et &quot;Géo&quot;, la feuille d’envoi groupée comprend les colonnes &quot;Couleur&quot; et &quot;Géo&quot;.

1. Ouvrez le fichier dans un éditeur et ajoutez des valeurs d’étiquette aux colonnes de classification des étiquettes pour les entités auxquelles les associer. La longueur maximale de chaque valeur est de 100 caractères. Elle peut contenir des caractères ASCII et non ASCII.

   Voir les exemples de valeurs dans la section suivante.

   Outre l’ajout de valeurs, vous pouvez également supprimer des valeurs existantes en les supprimant des lignes correspondantes. Pour supprimer des valeurs d’une entité parente et de ses entités enfants, a) incluez uniquement la ligne d’entité parente et supprimez la valeur de classification existante ou b) incluez l’entité parente et ses entités enfants, et supprimez la valeur de classification existante de toutes les lignes parentes et enfants.

1. [Téléchargez le fichier](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) pour créer les associations.

Les valeurs de libellé transférées sont visibles dans les vues d’entité appropriées.

## Exemple de valeurs de classification d’étiquettes à charger dans les feuilles d’envoi groupées

Cet exemple comprend des colonnes pour les classifications d’étiquettes &quot;Couleur&quot; et &quot;Géographie&quot;. Pour vos propres feuilles d’envoi groupé, remplacez les colonnes par vos propres noms de classification d’étiquettes.

| Compte | Campagne | Groupe publicitaire | Mot-clé | Publicité | Emplacement | Étiquettes | Couleur | Géo |
|---|---|---|---|---|---|---|---|---|
| Act1 | C1 | | | | | | Vert | |
| Act1 | C1 | AG1 | | | | | | |
| Act1 | C1 | AG1 | K1 | | | | | UK |
| Act1 | C1 | AG1 | K2 | | | | Rouge | AU |
| Act1 | C1 | AG1 | K3 | | | | bleu | DE |
| Act1 | C1 | AG1 | | A1 | | | | |
| Act1 | C1 | AG1 | | A1 | | | Rouge | |
| Act1 | C1 | AG1 | | | P1 | | Rouge | AU |
| Act1 | C1 | AG1 | | | P2 | | bleu | DE |

>[!MORELIKETHIS]
>
>* [À propos des classifications d’étiquettes](classification-about.md)
>* [Créer une classification d’étiquettes](classification-create.md)
>* [Attribuer des valeurs de classification aux composants de compte à partir des vues de gestion de campagne](classification-values-assign-campaign-management.md)
>* [Supprimer les valeurs de classification d’étiquette des composants de compte](classification-values-remove.md)
>* [&#x200B; Supprimer des valeurs de classification d’étiquettes](classification-values-delete.md)
>* [Supprimer des classifications d’étiquettes](classification-delete.md)
