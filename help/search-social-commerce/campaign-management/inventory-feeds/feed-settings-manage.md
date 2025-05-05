---
title: Configuration des paramètres des données de flux
description: Découvrez comment configurer les paramètres qui contrôlent le traitement des données de flux.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Configuration des paramètres des données de flux

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Vous pouvez configurer la gestion des groupes publicitaires, des mots-clés et des publicités dans les fichiers de données de flux, ainsi que le traitement des données dans les fichiers FTP, via les paramètres du flux.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Settings]**.

1. Spécifiez les [paramètres de données de flux](#feed-data-settings) :

   1. Dans la section [!UICONTROL Obsolete Item Auto-Processing] , sélectionnez les informations dans les champs.

   1. (Les annonceurs téléchargent des données par FTP ou via un lien direct vers un compte de centre commercial) Dans la section [!UICONTROL FTP/GMC Account Auto-Processing], sélectionnez des informations dans les champs.

   1. Dans la section [!UICONTROL Miscellaneous Auto-Processing] , sélectionnez les informations dans les champs.

1. Cliquez sur **[!UICONTROL Save]**.

## Paramètres des données de flux {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** applique tous les paramètres [!UICONTROL Obsolete Item Auto-processing] à :

* *[!UICONTROL Ad Groups Only]:* supprimer uniquement les groupes d’annonces.

* *[!UICONTROL Keywords Only]:* Mots-clés obsolètes et groupes de produits uniquement.

* *[!UICONTROL Ad Variations Only]* (valeur par défaut) : Publicités obsolètes uniquement.

* *[!UICONTROL Keywords and Ad Variations]:* Mots-clés/cibles de produits/groupes de produits obsolètes et publicités obsolètes.

>[!NOTE]
>
>* Pour les [!DNL Google Ads] publicités commerciales, seul le groupe de produits de niveau inférieur est affecté.
>* Pour les comptes [!DNL Yandex], les tâches de traitement automatique des éléments obsolètes sont toujours effectuées sur les variations de publicité, quel que soit ce paramètre.

**[!UICONTROL When the Scheduled End Date is reached]:** (Données publiées manuellement uniquement) Que faire des éléments de ligne dans un fichier de flux publié avec une date et une heure de fin spécifiées une fois l’heure de fin arrivée :

* *[!UICONTROL Delete]* (valeur par défaut) : supprimez tous les composants pertinents à l’heure de fin spécifiée. Vous ne pouvez pas inverser cette opération.

* *[!UICONTROL Pause]:* Mettez en pause tous les composants pertinents lorsque l’heure de fin spécifiée arrive. Vous pouvez réactiver les composants ultérieurement, si nécessaire.

* *[!UICONTROL None]:* Ne modifiez pas l’état des composants pertinents.

**[!UICONTROL Missing line items in a manually uploaded feed]:** Que faire des éléments existants lorsqu’ils ne sont pas inclus dans un nouveau fichier de flux qui a été chargé manuellement ou lorsqu’ils ne sont pas mappés à des campagnes ou des groupes d’annonces existants selon les paramètres Mapper uniquement du modèle :

* *[!UICONTROL Delete]:* Supprimez les composants existants.

* *[!UICONTROL Pause]:* Mettez en pause les composants existants. Ils sont réactivés si un nouveau fichier de flux contient l’un des mêmes éléments de ligne et ils conservent leurs scores d’historique et de qualité. **Remarque :** Si tous les groupes de produits enfants d’un groupe de produits parent sont manquants, le groupe de produits parent est supprimé car vous ne pouvez pas suspendre les groupes de produits.

* *[!UICONTROL None]* (valeur par défaut) : ne modifiez pas les composants existants.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Que faire des éléments existants lorsque 1) ils ne sont pas inclus a) dans un nouveau fichier de flux qui a été chargé dans un répertoire FTP ou b) dans un compte de centre commercial la prochaine fois que Search, Social et Commerce se synchronise avec eux, ou 2) lorsqu’ils ne sont pas associés à des campagnes ou groupes publicitaires existants selon les paramètres [!UICONTROL Map Only] du modèle.

* *[!UICONTROL Delete]:* Supprimez les composants existants.

* *[!UICONTROL Pause]:* Mettez en pause les composants existants. Elles sont réactivées si de nouvelles données contiennent l’un des mêmes éléments de ligne et conservent leur historique et leur note de qualité. **Remarque :** Si tous les groupes de produits enfants d’un groupe de produits parent sont manquants, le groupe de produits parent est supprimé car vous ne pouvez pas suspendre les groupes de produits.

* *[!UICONTROL None]* (valeur par défaut) : ne modifiez pas les composants existants.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Que faire des éléments de ligne qui incluent un niveau de stock lorsque :

* (Pour les flux dont les valeurs en stock sont numériques uniquement dans la colonne spécifiée) Le niveau de stock est inférieur ou égal à une quantité spécifiée. La quantité par défaut est zéro (0).

* (Pour les flux avec des valeurs textuelles dans la colonne spécifiée) La valeur de [!UICONTROL Availability] est &quot;[!UICONTROL out of stock]&quot; ; la valeur n’est pas sensible à la casse. **Remarque :** **Dans les modèles de flux, indiquez des colonnes de niveau de stock basées sur du texte à l’aide de la case à cocher pour &quot;[!UICONTROL This column has non-numeric values]&quot;.

Sélectionnez l’action pour les deux cas :

* *[!UICONTROL Delete]* (valeur par défaut) Supprimer les composants.

* *[!UICONTROL Pause]:* Mettez les composants en pause. Lorsque les données sont mises à jour, les composants sont réactivés si les valeurs numériques de stock dépassent la quantité spécifiée ou si l’[!UICONTROL Availability] est &quot;[!UICONTROL in stock]&quot; ou &quot;[!UICONTROL preorder]&quot;. Les composants conservent leur historique et leur note de qualité.

Le niveau de stock de chaque élément de ligne provient d’une colonne dans le fichier de flux, comme indiqué dans le champ &quot;[!UICONTROL Stock Level]&quot; pour chaque modèle.

>[!TIP]
>
>* Pour les produits ou services pour lesquels vous prévoyez de reverrouiller ou d’augmenter la disponibilité, vous devez suspendre les groupes publicitaires, les mots-clés et les publicités plutôt que de les supprimer et de les recréer. La pause leur permet de conserver leurs scores de qualité.
>* Si vous activez le traitement automatique obsolète pour les groupes d’annonces et que les nouvelles données incluent un niveau de stock pour le groupe d’annonces, il est utile de supprimer ou de suspendre le groupe d’annonces uniquement lorsque le niveau de stock spécifié se trouve au niveau de la catégorie plutôt qu’au niveau de la marque/de l’article. Par exemple, si vous avez un groupe publicitaire &quot;convertibles&quot;, le niveau de stock du groupe publicitaire doit être le total de tous les modèles convertibles individuels représentés dans le groupe publicitaire.

**[!UICONTROL Propagate feed data through all applicable templates]:** (Les annonceurs chargent des fichiers de données par FTP ou un compte de centre commercial) propage automatiquement les nouvelles données par le biais des modèles applicables. L’option est sélectionnée par défaut. Si vous désactivez cette option, vous pouvez toujours propager manuellement les données pour n’importe quel fichier de flux ou compte, ou pour n’importe quel modèle.

>[!NOTE]
>
>* Pour les fichiers FTP, le service de flux recherche les mises à jour dans le répertoire FTP toutes les deux heures (heures paires dans le fuseau horaire PST). Cette option traite tous les fichiers qui ont été chargés depuis la dernière vérification.
>* Pour les comptes de centre commercial, Search, Social et Commerce se synchronise avec le compte tous les jours vers 06h00 dans le fuseau horaire de l’annonceur. Cette option traite toutes les données qui ont été mises à jour depuis la dernière synchronisation.
>* Les données propagées sont disponibles à partir des onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads] jusqu’à ce que les données soient publiées sur le réseau publicitaire ou dans la vue [!UICONTROL Bulksheets].

**[!UICONTROL Post to the SE]:** (Les annonceurs téléchargent des fichiers de données par FTP ou un compte de centre commercial) crée automatiquement des fichiers de feuille d’envoi groupé dans les formats appropriés pour les réseaux publicitaires pertinents une fois que de nouvelles données sont propagées par le biais des modèles applicables. Cette option supprime également les données des onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads], sauf si des sous-composants comportent des erreurs.

Cette option est désactivée par défaut. Pour activer cette option, cochez la case, puis indiquez si les fichiers de feuille d’envoi groupé doivent être publiés sur les réseaux publicitaires :

* *[!UICONTROL Immediately]* (valeur par défaut) : publie les fichiers de feuille en vrac sur les réseaux publicitaires appropriés une fois les données propagées par le biais des modèles. Les fichiers de feuille d’envoi groupé restent disponibles dans la vue [!UICONTROL Bulksheets] pendant 30 jours.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:**&#x200B; Ne publie pas les fichiers de feuille d’envoi groupé sur les réseaux publicitaires appropriés, mais les répertorie dans la vue [!UICONTROL Bulksheets], à partir de laquelle vous pouvez les publier ultérieurement. Les fichiers de feuille d’envoi groupé restent disponibles dans la vue [!UICONTROL Bulksheets] pendant 30 jours. Si le fichier de feuille d’envoi groupé fait plus de 10 Mo mais moins de 2 Go, il est au format ZIP ; il n’est pas nécessaire de le décompresser pour le publier. &#x200B;** Conseil :** Si vous n’avez pas encore validé vos pages d’entrée, utilisez cette option afin de pouvoir les valider à partir de la vue [!UICONTROL Bulksheets] avant de publier les données sur le réseau publicitaire.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** exclut la publication d’expressions de mots-clés contenant plus d’un nombre spécifié de mots sur le réseau publicitaire. Lorsque cette option est sélectionnée, les expressions de mots-clés contenant plus de mots sont propagées et répertoriées dans l’onglet [!UICONTROL Keywords], mais elles ne sont pas publiées lorsque vous tentez de publier les données.

Cette option est désactivée par défaut, de sorte que tous les mots-clés soient publiés, quel que soit le nombre de mots inclus dans l’expression. Si vous sélectionnez cette option, sélectionnez le nombre maximal de mots à publier (de 3 à 10).

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propager les données de flux par le biais de modèles](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Données de campagne de publication générées à partir de flux vers les réseaux publicitaires](propagated-data-post.md)
