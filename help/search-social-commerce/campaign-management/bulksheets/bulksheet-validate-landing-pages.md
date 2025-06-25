---
title: Validation des pages de destination dans des fichiers de feuille d’envoi groupé
description: Découvrez comment valider les URL de destination dans un fichier de feuille d’envoi groupé à compte unique.
exl-id: 191cb1bc-54a9-4c6c-a29c-f3cbae08e0d8
feature: Search Bulksheets
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---

# Validation des pages de destination dans des fichiers de feuille d’envoi groupé

*Comptes avec URL de destination uniquement*

Vous pouvez valider les pages de destination dans toutes les URL de destination dans un fichier de feuille d’envoi groupé à compte unique. Vous pouvez spécifier des expressions et des URL qui indiquent une page non valide et, éventuellement, signaler les redirections de page de destination comme des erreurs. Les recherches, les réseaux sociaux et Commerce recherchent les conditions spécifiées et les pages de destination manquantes (qui génèrent des erreurs HTTP 404 ou « Introuvable »).

Lorsqu’il détecte des erreurs, Search, Social et Commerce crée un fichier d’erreur de feuille d’envoi groupé qui inclut toutes les lignes de la feuille d’envoi groupé d’origine et les messages d’erreur de toutes les lignes avec une page de destination non valide. Les erreurs sont notées dans la colonne [!UICONTROL EF Errors] . La convention de nom de fichier est `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Vous pouvez ensuite télécharger le fichier, corriger les erreurs et charger le fichier corrigé, puis publier le fichier corrigé sur le compte réseau publicitaire.

>[!NOTE]
>
>* Cette fonctionnalité ne valide pas les valeurs de la colonne URL de base/URL finale.
>* Vous pouvez publier des fichiers de feuilles d’envoi groupé pendant leur validation, ou même si des erreurs sont détectées.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Bulksheets]**.

1. Cochez la case en regard de chaque fichier à valider.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Validate URLs]**.

1. Dans la boîte de dialogue, saisissez les informations dans les champs, puis cliquez sur **[!UICONTROL Apply]** :

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page(one per line)]:** texte dans le corps d’une page de destination qui indique que la page n’est pas valide. Pour spécifier plusieurs valeurs, saisissez-les sur des lignes distinctes.

   **[!UICONTROL Enter invalid landing pages(one per line):]** URL des pages non valides en tant que pages de destination. Pour spécifier plusieurs valeurs, saisissez-les sur des lignes distinctes.

   **[!UICONTROL User Agent:]** Méthode d’identification de l’agent de validation de la page de destination auprès du serveur web sur lequel la page de destination réside. La valeur par défaut est default, ce qui attribue les vues par l&#39;agent à un utilisateur anonyme [!DNL Mozilla Firefox]. Si le serveur web bloque les requêtes des utilisateurs [!DNL Mozilla Firefox] anonymes, saisissez le nom d’un autre agent. Par exemple, pour [!DNL Googlebot], saisissez `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** lorsqu’une page de destination est redirigée vers une autre page (par exemple, si la page de destination est manquante et que le site affiche une page de substitution), la colonne [!UICONTROL ER Errors] du fichier d’erreur de la page de destination indique l’URL vers laquelle la page de destination est redirigée.

Lorsque la tâche commence, une nouvelle ligne est ajoutée à la [!UICONTROL Bulksheets view]. Lorsque le fichier est créé, une notification par e-mail est envoyée avec un lien vers le fichier. Selon la quantité de données compilées, la notification par e-mail peut prendre plusieurs minutes ou plus. Vous pouvez télécharger le fichier pour le modifier, puis le charger à nouveau pour publication, ou vous pouvez publier le fichier en l’état. Cependant, si la génération du fichier échoue, un fichier d’erreur est répertorié sur la page [!UICONTROL Bulksheet Management] et une notification est envoyée par e-mail avec un lien vers le fichier d’erreur.

>[!NOTE]
>
>* La validation des fichiers volumineux prend plus de temps.
>* Les fichiers de feuilles d’envoi groupé pour plusieurs campagnes peuvent contenir jusqu’à 500 000 lignes de données. Si vous générez des données pour plusieurs campagnes et que les données combinées se composent de plus de 500 000 lignes, les données sont divisées par campagne en deux fichiers ou plus nommés `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, etc.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l&#39;aide de feuilles d&#39;envoi groupé](bulksheet-about.md)
>* [Supprimer les feuilles d’envoi groupé et les fichiers d’erreur chargés](bulksheet-delete.md)
>* [Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](bulksheet-post.md)
>* [Arrêter une tâche de feuille d’envoi groupé en cours](bulksheet-stop-job.md)
>* [Charger une feuille d’envoi groupé ou un fichier d’erreur corrigé](bulksheet-upload.md)
>* [Exporter un fichier de feuille d’envoi groupé généré ou chargé](bulksheet-export.md)
