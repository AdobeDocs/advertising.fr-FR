---
title: Affectation de valeurs de classification à des composants de compte à l’aide de feuilles d’envoi groupé
description: Découvrez comment utiliser des feuilles d’envoi groupé pour affecter des valeurs de classification aux composants de compte.
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# Affectation de valeurs de classification à des composants de compte à l’aide de feuilles d’envoi groupé

Vous pouvez associer des classifications d’étiquettes à des valeurs pour les entités de recherche suivantes à l’aide de feuilles d’envoi groupé : campagne, groupe publicitaire, mot-clé, annonce, emplacement, groupe de produits au niveau de l’unité et cible de recherche dynamique. Chaque classification de libellé peut contenir jusqu’à 2 000 valeurs.

Chaque entité peut avoir une valeur de libellé par classification. Par exemple, Shoes_Campaign peut avoir une valeur Color de « red » et une valeur Geo de « Los Angeles », mais pas plusieurs valeurs pour Color ou Geo.

Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

>[!NOTE]
>
>Vos mots-clés et votre texte publicitaire pour certains réseaux publicitaires et types de campagne sont [non modifiables](/help/search-social-commerce/campaign-management/faqs-campaigns.md), ce qui signifie que leur modification supprime l’entité existante et en crée une nouvelle. Lorsqu&#39;une entité existante est supprimée de cette manière, la classification des libellés n&#39;est pas affectée à la nouvelle entité.

1. [Téléchargez une feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) qui comprend les entités auxquelles vous souhaitez affecter des valeurs de classification de libellés :

   * Dans l’onglet [!UICONTROL Rows and Columns] , développez la liste [!UICONTROL Campaign] dans le volet [!UICONTROL Bulksheet Columns] .

   * Développez la liste des [!UICONTROL Label Classification].

   * Sélectionnez chaque classification pour laquelle vous souhaitez inclure une colonne dans le fichier de feuille d’envoi groupé.

     Par exemple, si vous incluez les classifications d’étiquettes « Couleur » et « Géo », la feuille groupée inclut les colonnes « Couleur » et « Géo ».

1. Ouvrez le fichier dans un éditeur et ajoutez des valeurs de libellé aux colonnes de classification de libellé pour les entités auxquelles les associer. La longueur maximale de chaque valeur est de 100 caractères et peut inclure des caractères ASCII et non ASCII.

   Voir les exemples de valeurs dans la section suivante.

   Outre l’ajout de valeurs, vous pouvez également supprimer des valeurs existantes en les supprimant des lignes appropriées. Pour supprimer des valeurs à la fois d&#39;une entité parent et de ses entités enfant, soit a) incluez uniquement la ligne d&#39;entité parent et supprimez la valeur de classification existante, soit b) incluez à la fois l&#39;entité parent et ses entités enfant et supprimez la valeur de classification existante de toutes les lignes parent et enfant.

1. [Chargez le fichier](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) pour créer les associations.<!-- Update once the new bulksheet UI is GA -->

Les valeurs de libellé chargées sont visibles dans les vues d’entité appropriées.

## Exemple de valeurs de classification de libellé à charger dans des feuilles d’envoi groupé

Cet exemple inclut des colonnes pour les classifications de libellés « Color » et « Geo ». Pour vos propres feuilles d’envoi groupé, remplacez les noms de classification d’étiquettes par des colonnes.

| Compte | Campagne | Groupe publicitaire | Mot-clé | Annonce publicitaire | Placement | Étiquettes | Couleur | Géo |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 | | | | | | Vert | |
| Acct1 | C1 | AG1 | | | | | | |
| Acct1 | C1 | AG1 | K1 | | | | | UK |
| Acct1 | C1 | AG1 | K2 | | | | Rouge | AU |
| Acct1 | C1 | AG1 | K3 | | | | Bleu | DE |
| Acct1 | C1 | AG1 | | A1 | | | | |
| Acct1 | C1 | AG1 | | A1 | | | Rouge | |
| Acct1 | C1 | AG1 | | | P1 | | Rouge | AU |
| Acct1 | C1 | AG1 | | | P2 | | Bleu | DE |

>[!MORELIKETHIS]
>
>* [À propos des classifications de libellés](classification-about.md)
>* [Créer une classification de libellé](classification-create.md)
>* [Attribuer des valeurs de classification aux composants de compte à partir des vues de gestion de campagne](classification-values-assign-campaign-management.md)
>* [Supprimer les valeurs de classification de libellé des composants de compte](classification-values-remove.md)
>* [Supprimer les valeurs de classification de libellé](classification-values-delete.md)
>* [Supprimer les classifications de libellés](classification-delete.md)
