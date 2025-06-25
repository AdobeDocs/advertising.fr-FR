---
title: Configurer les paramètres des données de flux
description: Découvrez comment configurer les paramètres qui contrôlent le traitement des données de flux.
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# Configurer les paramètres des données de flux

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Vous pouvez configurer la manière de gérer les groupes d’annonces, les mots-clés et les annonces dans les fichiers de données de flux, ainsi que la manière de traiter les données dans les fichiers FTP en particulier, via les paramètres de flux.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Settings]**.

1. Spécifiez les [paramètres des données de flux](#feed-data-settings) :

   1. Dans la section [!UICONTROL Obsolete Item Auto-Processing], sélectionnez les informations dans les champs.

   1. (Annonceurs téléchargeant des données par FTP ou par le biais d’un lien direct vers un compte de centre commercial) Dans la section [!UICONTROL FTP/GMC Account Auto-Processing], sélectionnez les informations dans les champs.

   1. Dans la section [!UICONTROL Miscellaneous Auto-Processing], sélectionnez les informations dans les champs.

1. Cliquez sur **[!UICONTROL Save]**.

## Paramètres des données de flux {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** applique tous les paramètres [!UICONTROL Obsolete Item Auto-processing] à :

* *[!UICONTROL Ad Groups Only]:* groupes publicitaires obsolètes uniquement.

* *[!UICONTROL Keywords Only]:* Mots-clés et groupes de produits obsolètes uniquement.

* *[!UICONTROL Ad Variations Only]* (valeur par défaut) : publicités obsolètes uniquement.

* *[!UICONTROL Keywords and Ad Variations]:* Mots-clés obsolètes/cibles de produit/groupes de produits et publicités obsolètes.

>[!NOTE]
>
>* Pour les annonces d’achats [!DNL Google Ads], seul le groupe de produits de niveau inférieur est affecté.
>* Pour les comptes [!DNL Yandex], les tâches de traitement automatique des éléments obsolètes sont toujours effectuées sur les variations d’annonces, quel que soit ce paramètre.

**[!UICONTROL When the Scheduled End Date is reached]:** (données publiées manuellement uniquement) Que faire des lignes d’un fichier de flux publiées avec une date et une heure de fin spécifiées une fois l’heure de fin atteinte :

* *[!UICONTROL Delete]* (valeur par défaut) : supprimez tous les composants pertinents lorsque l’heure de fin spécifiée arrive. Vous ne pouvez pas annuler cette opération.

* *[!UICONTROL Pause]:* Mettre en pause tous les composants pertinents lorsque l’heure de fin spécifiée arrive. Vous pouvez réactiver les composants ultérieurement, si nécessaire.

* *[!UICONTROL None]:* ne modifiez pas le statut des composants appropriés.

**[!UICONTROL Missing line items in a manually uploaded feed]:** que faire des éléments existants lorsqu’ils ne sont pas inclus dans un nouveau fichier de flux qui a été chargé manuellement ou lorsqu’ils ne sont pas mappés à des campagnes ou des groupes publicitaires existants selon les paramètres Mapper uniquement dans le modèle :

* *[!UICONTROL Delete]:* les composants existants.

* *[!UICONTROL Pause]:* Mettre en pause les composants existants. Ils sont réactivés si un nouveau fichier de flux contient l’un des mêmes éléments de ligne et ils conservent leurs scores d’historique et de qualité. **Remarque :** si tous les groupes de produits enfants d&#39;un groupe de produits parent sont manquants, le groupe de produits parent est supprimé car vous ne pouvez pas le suspendre.

* *[!UICONTROL None]* (valeur par défaut) : ne modifiez pas les composants existants.

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** Que faire des éléments existants lorsque 1) ils ne sont pas inclus a) dans un nouveau fichier de flux qui a été chargé dans un répertoire FTP ou b) dans un compte de centre commercial la prochaine fois que Search, Social et Commerce s’y synchronise, ou 2) lorsqu’ils ne sont pas mappés à des campagnes ou des groupes publicitaires existants selon les paramètres [!UICONTROL Map Only] du modèle.

* *[!UICONTROL Delete]:* les composants existants.

* *[!UICONTROL Pause]:* Mettre en pause les composants existants. Elles sont réactivées si les nouvelles données contiennent l’un des mêmes éléments de ligne et conservent leur historique et leur score de qualité. **Remarque :** si tous les groupes de produits enfants d&#39;un groupe de produits parent sont manquants, le groupe de produits parent est supprimé car vous ne pouvez pas le suspendre.

* *[!UICONTROL None]* (valeur par défaut) : ne modifiez pas les composants existants.

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** Que faire des lignes contenant un niveau de stock lorsque :

* (Pour les flux dont les valeurs de stock sont uniquement numériques dans la colonne spécifiée) Le niveau de stock est égal ou inférieur à une quantité spécifiée. La quantité par défaut est zéro (0).

* (Pour les flux avec des valeurs de texte dans la colonne spécifiée) La valeur de [!UICONTROL Availability] est « [!UICONTROL out of stock] » ; elle n’est pas sensible à la casse. **Remarque :** **dans les modèles de flux, indiquez les colonnes de niveau de stock textuelles à l’aide de la case à cocher correspondant à « [!UICONTROL This column has non-numeric values] ».

Sélectionnez l’action pour les deux cas :

* *[!UICONTROL Delete]* (valeur par défaut) Supprimer les composants.

* *[!UICONTROL Pause]:* Mettre les composants en pause. Lorsque les données sont mises à jour, les composants sont réactivés si les valeurs numériques de stock dépassent la quantité spécifiée ou si la [!UICONTROL Availability] est « [!UICONTROL in stock] » ou « [!UICONTROL preorder] ». Les composants conservent leur historique et leur score de qualité.

Le niveau de stock de chaque ligne provient d&#39;une colonne du fichier de flux, comme indiqué dans le champ « [!UICONTROL Stock Level] » de chaque modèle.

>[!TIP]
>
>* Pour les produits ou services pour lesquels vous prévoyez de réapprovisionner ou d’augmenter la disponibilité, vous devez suspendre les groupes publicitaires, les mots-clés et les annonces plutôt que de les supprimer et de les recréer. La mise en pause leur permet de conserver leurs scores de qualité.
>* Si vous activez le traitement automatique obsolète pour les groupes publicitaires et que les nouvelles données incluent un niveau de stock pour le groupe publicitaire, il est utile de supprimer ou de suspendre le groupe publicitaire uniquement lorsque le niveau de stock spécifié se trouve au niveau de la catégorie plutôt qu’au niveau de la marque/de l’article. Par exemple, si vous disposez d’un groupe publicitaire « convertible », le niveau de stock du groupe publicitaire doit correspondre au total de tous les modèles convertibles individuels représentés dans le groupe publicitaire.

**[!UICONTROL Propagate feed data through all applicable templates]:** (les annonceurs chargent des fichiers de données par FTP ou par un compte de centre commercial) propage automatiquement les nouvelles données par le biais des modèles applicables. L’option est sélectionnée par défaut. Si vous désactivez cette option, vous pouvez toujours propager manuellement les données de n’importe quel fichier de flux ou compte, ou de n’importe quel modèle.

>[!NOTE]
>
>* Pour les fichiers FTP, le service de flux vérifie les mises à jour du répertoire FTP toutes les deux heures (heures paires dans le fuseau horaire PST). Cette option traite tous les fichiers chargés depuis la dernière vérification.
>* Pour les comptes de centre commercial, Search, Social et Commerce se synchronise quotidiennement avec le compte vers 6 h 00 dans le fuseau horaire de l’annonceur. Cette option traite toutes les données mises à jour depuis la dernière synchronisation.
>* Les données propagées sont disponibles à partir des onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads] jusqu’à ce qu’elles soient publiées sur le réseau publicitaire ou dans la vue [!UICONTROL Bulksheets].

**[!UICONTROL Post to the SE]:** (les annonceurs téléchargent les fichiers de données via FTP ou un compte de centre commercial) Crée automatiquement des fichiers de feuilles d’envoi groupé dans les formats appropriés pour les réseaux publicitaires appropriés après la propagation de nouvelles données par le biais des modèles applicables. Cette option supprime également les données des onglets [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords] et [!UICONTROL Ads], sauf si des sous-composants comportent des erreurs.

Cette option est désactivée par défaut. Pour activer cette option, activez la case à cocher puis indiquez si vous souhaitez publier des fichiers de feuilles d&#39;envoi groupé sur les réseaux publicitaires :

* *[!UICONTROL Immediately]* (valeur par défaut) : publie les fichiers de feuille d’envoi groupé sur les réseaux publicitaires appropriés une fois les données propagées à travers les modèles. Les fichiers de feuille d’envoi groupé restent disponibles dans la vue [!UICONTROL Bulksheets] pendant 30 jours.

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:** ne publie pas les fichiers de feuille d’envoi groupé sur les réseaux publicitaires appropriés, mais les répertorie dans la vue [!UICONTROL Bulksheets], à partir de laquelle vous pouvez les publier ultérieurement. Les fichiers de feuille d’envoi groupé restent disponibles dans la vue [!UICONTROL Bulksheets] pendant 30 jours. Lorsque le fichier de feuille d’envoi groupé fait plus de 10 Mo, mais moins de 2 Go, le fichier est au format ZIP ; il n’est pas nécessaire de décompresser le fichier pour le publier. **Conseil :** si vous n’avez pas encore validé vos pages de destination, utilisez cette option pour pouvoir les valider à partir de la vue [!UICONTROL Bulksheets] avant de publier les données sur le réseau publicitaire.

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** Empêche de publier sur le réseau publicitaire des expressions de mots-clés comportant plus d&#39;un nombre spécifié de mots. Lorsque cette option est sélectionnée, les phrases de mots-clés contenant plus de mots que le nombre maximal sont propagées et répertoriées dans l’onglet [!UICONTROL Keywords] , mais elles ne sont pas publiées lorsque vous essayez de publier les données.

Cette option est désactivée par défaut afin que tous les mots-clés soient publiés, quel que soit le nombre de mots inclus dans l’expression. Si vous sélectionnez cette option, sélectionnez le nombre maximal de mots à publier (entre 3 et 10).

>[!MORELIKETHIS]
>
>* [À propos des flux d’inventaire](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [Propager les données de flux par le biais de modèles](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [Publier les données de campagne générées à partir des flux sur les réseaux publicitaires](propagated-data-post.md)
