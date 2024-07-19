---
title: Validation des landing pages dans des fichiers de feuille d’envoi groupé
description: Découvrez comment valider les URL de destination dans un fichier de feuille d’envoi groupé à un seul compte.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Validation des landing pages dans des fichiers de feuille d’envoi groupé

*Comptes avec URL de destination uniquement*

Vous pouvez valider les landing pages dans toutes les URL de destination dans un fichier de feuille d’envoi groupé à un seul compte. Vous pouvez spécifier des expressions et des URL qui indiquent une page non valide et éventuellement signaler les redirections de page d’entrée comme des erreurs. Search, Social et Commerce recherche les conditions spécifiées et les pages d’entrée manquantes (qui entraînent des erreurs HTTP 404 ou &quot;Not Found&quot;).

Lorsqu’il détecte des erreurs, Search, Social et Commerce crée un fichier d’erreur de feuille d’envoi groupé qui inclut toutes les lignes de la feuille d’envoi groupé d’origine et les messages d’erreur pour toutes les lignes comportant une page d’entrée non valide. Les erreurs sont notées dans la colonne [!UICONTROL EF Errors]. La convention de nom de fichier est `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Vous pouvez ensuite télécharger le fichier, corriger les erreurs et charger le fichier corrigé, puis publier le fichier corrigé sur le compte réseau publicitaire.

>[!NOTE]
>
>* Cette fonction ne valide pas les valeurs de la colonne URL de base/URL finale.
>* Vous pouvez publier des fichiers de feuille d’envoi groupé pendant leur validation, ou même si des erreurs sont détectées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Cochez la case en regard de chaque fichier à valider.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Validate URLs]**.

1. Dans la boîte de dialogue, saisissez des informations dans les champs, puis cliquez sur **[!UICONTROL Apply]** :

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** Texte dans le corps d’une landing page indiquant que la page n’est pas valide. Pour spécifier plusieurs valeurs, saisissez-les sur des lignes distinctes.

   **[!UICONTROL Enter invalid landing pages(one per line):]** URL des pages non valides en tant que pages d’entrée. Pour spécifier plusieurs valeurs, saisissez-les sur des lignes distinctes.

   **[!UICONTROL User Agent:]** Comment l’agent de validation de page d’entrée est identifié sur le serveur web sur lequel réside la page d’entrée. La valeur par défaut est default, qui attribue les vues par l’agent à un utilisateur anonyme [!DNL Mozilla Firefox]. Si le serveur web bloque les demandes des utilisateurs anonymes [!DNL Mozilla Firefox], saisissez le nom d&#39;un autre agent. Par exemple, pour [!DNL Googlebot], saisissez `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** Lorsqu’une landing page est redirigée vers une autre page (par exemple, si la landing page est manquante et que le site affiche une page de remplacement), la colonne [!UICONTROL ER Errors] du fichier d’erreur de la landing page indique l’URL vers laquelle la landing page est redirigée.

Lorsque la tâche démarre, une nouvelle ligne est ajoutée à la [!UICONTROL Bulksheets view]. Une fois le fichier créé, une notification par e-mail est envoyée avec un lien vers le fichier. Selon la quantité de données compilées, la notification par email peut prendre plusieurs minutes ou plus. Vous pouvez télécharger le fichier pour le modifier, puis le charger à nouveau pour le publier, ou publier le fichier tel quel. Toutefois, si la génération du fichier échoue, un fichier d’erreur est répertorié sur la page [!UICONTROL Bulksheet Management] et une notification par e-mail est envoyée avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>* La validation des fichiers volumineux prend plus de temps.
>* Les fichiers de feuilles d’envoi groupé pour plusieurs campagnes peuvent contenir jusqu’à 500 000 lignes de données. Si vous générez des données pour plusieurs campagnes et que les données combinées se composent de plus de 500 000 lignes, les données sont fractionnées par campagne en deux fichiers ou plus nommés `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, etc.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](bulksheet-about.md)
>* [Supprimer les feuilles d’envoi groupées et les fichiers d’erreur chargés](bulksheet-delete.md)
>* [ Publier des feuilles d’envoi groupées ou des fichiers d’erreur corrigés](bulksheet-post.md)
>* [Arrêter une tâche de feuille d’envoi groupé en cours](bulksheet-stop-job.md)
>* [Télécharger une feuille d’envoi groupé ou un fichier d’erreur corrigé](bulksheet-upload.md)
>* [Exporter un fichier de feuille d’envoi groupé généré ou téléchargé](bulksheet-export.md)
