---
title: Gérer les classifications de libellés
description: Découvrez comment utiliser les classifications d’étiquettes pour regrouper les composants de votre compte.
feature: Search Label Classifications
source-git-commit: 44f83bcf32d671ad96a420827d16d8f1ec39049e
workflow-type: tm+mt
source-wordcount: '1514'
ht-degree: 0%

---

# Gérer les classifications de libellés

Les classifications d’étiquettes vous permettent de regrouper vos composants de compte en ensembles significatifs. Par exemple, vous pouvez créer une classification d&#39;étiquettes parente appelée « Geo », créer une valeur d&#39;étiquette différente pour chaque zone géographique (par exemple « Royaume-Uni » et « Japon ») dans la classification, puis affecter les valeurs d&#39;étiquette à vos [unités d&#39;enchères](/help/search-social-commerce/glossary.md#a-b) ou campagnes parentes. Vous pouvez ensuite inclure n’importe quelle valeur d’étiquette dans une colonne distincte dans vos vues et rapports, et faire pivoter vos rapports sur différents groupes et valeurs de classification.

## Composants des classifications d’étiquettes

### Classifications des libellés

Chaque annonceur peut avoir jusqu’à 30 classifications de libellés, qui sont des catégories de niveau supérieur. Une fois que vous avez créé une classification de libellés, vous pouvez créer des valeurs de libellé spécifiques pour la classification.

### Valeurs des libellés

Chaque classification de libellé peut contenir jusqu’à 2 000 valeurs. Une fois que vous avez créé des valeurs d’étiquette spécifiques pour une classification, vous pouvez les affecter à des campagnes, des groupes publicitaires, des mots-clés, des annonces, des emplacements et des groupes de produits [à partir des vues de gestion de campagne](#classification-values-assign-campaign-management) ou [à l’aide de feuilles d’envoi groupé](#classification-values-assign-bulksheets).

Chaque entité éligible peut avoir des valeurs de libellé pour plusieurs classifications, mais une seule valeur de libellé par classification. Les valeurs des libellés sont héritées par les entités enfants mais peuvent être remplacées. La valeur affectée au niveau le plus bas remplace toujours les valeurs affectées aux niveaux parents.

## La vue Classifications des libellés

La vue [!UICONTROL Reports] > [!UICONTROL Labels Classifications] comprend les sous-vues [!UICONTROL Classifications] et [!UICONTROL Label Values]. Par défaut, les données s’affichent pour vos classifications et valeurs de libellés au niveau des mots-clés, mais vous pouvez éventuellement afficher les données pour vos classifications et valeurs au niveau des annonces.

## Actions disponibles

* Affichez les données pour les classifications de libellés.

* Affichez les données pour les valeurs de classification de vos étiquettes.

* [Créer une classification de libellé](#classification-create).

* Attribuez des valeurs de classification aux composants de compte [à partir des vues de gestion de campagne](#classification-values-assign-campaign-management) ou [à l’aide de feuilles d’envoi groupé](#classification-values-assign-bulksheets).

* [Supprimez les valeurs de classification de libellé des composants de compte](#classification-values-remove).

* [Supprimer les valeurs de classification de libellé](#classification-values-delete).

* [Supprimer les classifications de libellés](#classification-delete).

## Créer une classification de libellé {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. Cliquez sur **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. Dans le coin supérieur droit, cliquez sur **[!UICONTROL Create Classification]**.

1. Saisissez un nom de classification de libellé unique, puis cliquez sur **[!UICONTROL Create]**.

   Le nom doit être unique pour le compte de l’annonceur et comporter [caractères ASCII compris entre 32 et 126](https://www.asciitable.com/). La longueur maximale est de 27 caractères codés sur un seul octet. Le nom ne peut pas être identique au nom d&#39;une colonne de rapport existante ou d&#39;une colonne de feuille d&#39;envoi groupé existante. Voir les noms des colonnes de la feuille d’envoi groupé pour [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md), [LY Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md), [Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md), [Yahoo ! Affichez les &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md) Réseau et [Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md).

## Attribuer des valeurs de classification aux composants de compte à partir des vues de gestion de campagne {#classification-values-assign-campaign-management}

Vous pouvez affecter et supprimer des valeurs de classification pour les entités de recherche suivantes des vues de gestion de campagne : campagne, groupe publicitaire, mot-clé, publicité, emplacement, groupe de produits au niveau de l&#39;unité et cible de recherche dynamique. Si nécessaire, vous pouvez créer des classifications et des valeurs de classification au cours du processus d’affectation. Chaque classification de libellé peut contenir jusqu’à 2 000 valeurs.

Chaque entité peut avoir une valeur de libellé par classification. Par exemple, Shoes_Campaign peut avoir une valeur Color de « red » et une valeur Geo de « Los Angeles », mais pas plusieurs valeurs pour Color ou Geo.

Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

>[!NOTE]
>
>Vos mots-clés et votre texte publicitaire pour certains réseaux publicitaires et types de campagne sont [non modifiables](/help/search-social-commerce/campaign-management/faqs-campaigns.md), ce qui signifie que leur modification supprime l’entité existante et en crée une nouvelle. Lorsqu&#39;une entité existante est supprimée de cette manière, la classification des libellés n&#39;est pas affectée à la nouvelle entité.

1. Ouvrez la vue d’entité à partir du menu **[!UICONTROL Manage]** ou **[!UICONTROL Target]** .

1. Cochez la case en regard de chaque ligne pertinente.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**.

1. Pour chaque valeur de classification applicable, procédez comme suit :

   1. Dans la colonne **[!UICONTROL Classifications]** , indiquez la classification :

      * Pour utiliser une classification existante, cliquez sur son nom pour la développer.

      * Pour créer une classification, cliquez sur [!UICONTROL +] dans l’en-tête de colonne. Dans le champ de saisie, saisissez le nom de la classification, puis cliquez sur ![Enregistrer](/help/search-social-commerce/assets/save-checkmark.png "Enregistrer") pour enregistrer immédiatement la classification. Pour utiliser la nouvelle classification, cliquez sur son nom pour la développer.

        Le nom doit comporter [caractères ASCII compris entre 32 et 126](https://www.asciitable.com/) et la longueur maximale est de 27 caractères codés sur un seul octet.

   1. Dans la colonne **[!UICONTROL Value Name]** , indiquez la valeur de la classification sélectionnée :

      * Pour utiliser une valeur existante, sélectionnez-la.

      * Pour créer une valeur, cliquez sur [!UICONTROL +] dans l’en-tête de colonne. Dans le champ de saisie, saisissez la valeur, puis cliquez sur ![Enregistrer](/help/search-social-commerce/assets/save-checkmark.png "Enregistrer") pour enregistrer immédiatement la valeur et la sélectionner par défaut.

        La longueur maximale est de 100 caractères et peut inclure des caractères ASCII et non-ASCII.

1. Cliquez sur **+[!UICONTROL Assign Now]**.

## Affectation de valeurs de classification à des composants de compte à l’aide de feuilles d’envoi groupé {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

Vous pouvez associer des classifications d’étiquettes à des valeurs pour les entités de recherche suivantes à l’aide de feuilles d’envoi groupé : campagne, groupe publicitaire, mot-clé, annonce, emplacement, groupe de produits au niveau de l’unité et cible de recherche dynamique. Chaque classification de libellé peut contenir jusqu’à 2 000 valeurs.

Chaque entité peut avoir une valeur de libellé par classification. Par exemple, Shoes_Campaign peut avoir une valeur Color de « red » et une valeur Geo de « Los Angeles », mais pas plusieurs valeurs pour Color ou Geo.

Les valeurs de libellé sont héritées par les entités enfants. Par conséquent, ne saisissez pas de valeurs pour les entités enfants, sauf si vous souhaitez remplacer les valeurs héritées.

>[!NOTE]
>
>Vos mots-clés et votre texte publicitaire pour certains réseaux publicitaires et types de campagne sont [non modifiables](/help/search-social-commerce/campaign-management/faqs-campaigns.md), ce qui signifie que leur modification supprime l’entité existante et en crée une nouvelle. Lorsqu&#39;une entité existante est supprimée de cette manière, la classification des libellés n&#39;est pas affectée à la nouvelle entité.

1. [Téléchargez une feuille d’envoi groupé](/help/search-social-commerce/new-ui/set-up/bulksheets/download.md) qui comprend les entités auxquelles vous souhaitez affecter des valeurs de classification de libellés :

   * Dans l’onglet [!UICONTROL Rows and Columns] , développez la liste [!UICONTROL Campaign] dans le volet [!UICONTROL Bulksheet Columns] .

   * Développez la liste des [!UICONTROL Label Classification].

   * Sélectionnez chaque classification pour laquelle vous souhaitez inclure une colonne dans le fichier de feuille d’envoi groupé.

     Par exemple, si vous incluez les classifications d’étiquettes « Couleur » et « Géo », la feuille groupée inclut les colonnes « Couleur » et « Géo ».

1. Ouvrez le fichier dans un éditeur et ajoutez des valeurs de libellé aux colonnes de classification de libellé pour les entités auxquelles les associer. La longueur maximale de chaque valeur est de 100 caractères et peut inclure des caractères ASCII et non ASCII.

   Voir les exemples de valeurs dans la section suivante.

   Outre l’ajout de valeurs, vous pouvez également supprimer des valeurs existantes en les supprimant des lignes appropriées. Pour supprimer des valeurs à la fois d&#39;une entité parent et de ses entités enfant, soit a) incluez uniquement la ligne d&#39;entité parent et supprimez la valeur de classification existante, soit b) incluez à la fois l&#39;entité parent et ses entités enfant et supprimez la valeur de classification existante de toutes les lignes parent et enfant.

1. [Chargez le fichier](/help/search-social-commerce/new-ui/set-up/bulksheets/upload.md) pour créer les associations.

Les valeurs de libellé chargées sont visibles dans les vues d’entité appropriées.

### Exemple de valeurs de classification de libellé à charger dans des feuilles d’envoi groupé

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

## Supprimer les valeurs de classification de libellé des composants de compte {#classification-values-remove}

La suppression d’une valeur de classification supprime l’association avec le composant de compte et tous ses composants enfants. Les données de rapport pour la valeur de classification ne sont plus disponibles pour ces composants. La suppression d’une valeur de classification ne supprime pas la valeur ni les composants de compte.

>[!NOTE]
>
>Pour supprimer une valeur d’une classification d’étiquettes, voir « [Supprimer des valeurs de classification d’étiquettes](#classification-values-delete) ».

1. Ouvrez la vue d’entité à partir du menu **[!UICONTROL Manage]** ou **[!UICONTROL Target]** .

1. Cochez la case en regard de chaque ligne pertinente.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**.

1. Cochez la case en regard de chaque valeur de classification à supprimer des entités sélectionnées.<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   Pour sélectionner toutes les valeurs attribuées, cliquez sur **[!UICONTROL Select All]**. Pour désélectionner toutes les valeurs affectées, cliquez sur **[!UICONTROL Deselect All]**.

1. Cliquez sur **[!UICONTROL Unassign Selected]**.

## Supprimer les valeurs de classification de libellé {#classification-values-delete}

La suppression des valeurs de classification d’étiquettes les rend indisponibles pour une utilisation ultérieure et les données de rapport ne sont plus disponibles pour les valeurs. Toutes les affectations entre les valeurs et leurs classifications de libellés parents et composants de compte spécifiques sont supprimées, mais les classifications de libellés parents et les composants de campagne ne sont pas supprimés.

>[!NOTE]
>
>Pour simplement dissocier une valeur de classification d’un composant de compte, voir « [Supprimer les valeurs de classification de libellé des composants de compte](#classification-values-remove) ».

1. Cliquez sur **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. Cliquez sur l’onglet **[!UICONTROL Label Values]** .

1. (Facultatif) Filtrez la liste pour inclure des valeurs d’étiquette spécifiques.

1. Cochez la case en regard de chaque valeur de libellé à supprimer.

   Vous pouvez supprimer jusqu’à 200 lignes à la fois.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Supprimer les classifications de libellés

La suppression d’une classification supprime toutes les associations entre ses valeurs enfants et ses composants de compte. Une classification supprimée et ses valeurs ne sont pas disponibles pour une utilisation ultérieure. Les données de rapport pour les valeurs de classification ne sont plus disponibles.

>[!NOTE]
>
>Pour simplement dissocier une valeur de classification d’un composant de compte, voir « [Supprimer les valeurs de classification de libellé des composants de compte](#classification-values-remove) ».

1. Cliquez sur **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**.

1. (Facultatif) Filtrez la liste pour inclure des classifications d’étiquettes spécifiques.

1. Cochez la case en regard de chaque classification de libellés à supprimer.

   Vous pouvez supprimer jusqu’à 200 lignes à la fois.

   Pour obtenir des conseils sur la sélection de plusieurs lignes, reportez-vous à « [Sélectionner plusieurs lignes](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) ».

1. Dans la barre d’outils des actions en bloc, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.
