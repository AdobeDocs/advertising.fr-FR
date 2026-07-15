---
title: (Nouvelle interface utilisateur) Valider les pages de destination dans des fichiers de feuille d’envoi groupé
description: Découvrez comment valider les URL de destination dans un fichier de feuille d’envoi groupé à compte unique dans la nouvelle interface utilisateur Search, Social et Commerce.
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: f22a0f3f1884066faca71c6e8bb760253366b30e
workflow-type: tm+mt
source-wordcount: 585
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Valider les pages de destination dans des fichiers de feuille d’envoi groupé

*Comptes avec URL de destination uniquement*

Vous pouvez valider les pages de destination dans toutes les URL de destination dans un fichier de feuille d’envoi groupé à compte unique. Vous pouvez spécifier des expressions et des URL qui indiquent une page non valide et, éventuellement, signaler les redirections de page de destination comme des erreurs. Les recherches, les réseaux sociaux et Commerce recherchent les conditions spécifiées et les pages de destination manquantes (qui génèrent des erreurs HTTP 404 ou « Introuvable »).

Lorsqu’il détecte des erreurs, Search, Social et Commerce crée un fichier d’erreur de feuille d’envoi groupé qui inclut toutes les lignes de la feuille d’envoi groupé d’origine et les messages d’erreur de toutes les lignes avec des pages de destination non valides. Les erreurs sont notées dans la colonne [!UICONTROL EF Errors] . La convention de nom de fichier est `<bulksheet name>__lpv_errors.<extension used for the bulksheet>`.

Vous pouvez ensuite télécharger le fichier, corriger les erreurs et charger le fichier corrigé, puis publier le fichier corrigé sur le compte réseau publicitaire.

>[!NOTE]
>
>* Cette fonctionnalité ne valide pas les valeurs de la colonne URL de base/URL finale.
>* Vous pouvez publier des fichiers de feuilles d’envoi groupé pendant leur validation, ou même si des erreurs sont détectées.

>[!IMPORTANT]
>
>La prise en charge des caractères non-ASCII dans la validation des pages de destination a été temporairement suspendue. Si les URL de votre page de destination contiennent des caractères non-ASCII, contactez le support technique pour obtenir de l’aide.

1. Dans le menu principal, cliquez sur **[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**.

1. Cochez la case en regard de chaque fichier à valider.

   >[!NOTE]
   >
   >Vous ne pouvez valider que les feuilles d&#39;envoi groupé FE à compte unique qui ne sont pas en cours. Si vous sélectionnez une feuille d’envoi groupé pour plusieurs comptes ou une feuille d’envoi groupé en cours de traitement, ces fichiers sont exclus.

1. Dans la barre d’actions, cliquez sur **[!UICONTROL Validate URLs]**.

1. Dans la boîte de dialogue, saisissez les informations dans les champs, puis cliquez sur **[!UICONTROL Apply]** :

   **[!UICONTROL Enter case-sensitive text or phrases that indicate an invalid page (one per line):]** Texte dans le corps d’une page de destination qui indique que la page n’est pas valide. Pour spécifier plusieurs valeurs, saisissez-les sur des lignes distinctes.

   **[!UICONTROL Enter invalid landing pages (one per line):]** URL des pages non valides en tant que pages de destination. Pour spécifier plusieurs valeurs, saisissez-les sur des lignes distinctes.

   **[!UICONTROL User Agent:]** Méthode d’identification de l’agent de validation de la page de destination auprès du serveur web sur lequel la page de destination réside. La valeur par défaut est `default`, ce qui attribue les vues par l’agent à un utilisateur [!DNL Mozilla Firefox] anonyme. Si le serveur web bloque les requêtes des utilisateurs [!DNL Mozilla Firefox] anonymes, saisissez le nom d’un autre agent. Par exemple, pour [!DNL Googlebot], saisissez `Googlebot/2.1;+http://www.google.com/bot.html`.

   **[!UICONTROL Report redirects as errors]:** lorsqu’une page de destination est redirigée vers une autre page (par exemple, si la page de destination est manquante et que le site affiche une page de substitution), la colonne [!UICONTROL EF Errors] du fichier d’erreur de la page de destination indique l’URL vers laquelle la page de destination est redirigée.

Lorsque la tâche commence, une nouvelle ligne est ajoutée à la vue [!UICONTROL Bulksheets]. Lorsque les notifications par e-mail pour les feuilles d’envoi groupé sont [ activées dans [!UICONTROL Notification Center]](/help/search-social-commerce/new-ui/notifications-manage.md), une notification par e-mail avec un lien vers le fichier est envoyée lors de la création du fichier. Selon la quantité de données compilées, la notification par e-mail peut prendre plusieurs minutes ou plus. Vous pouvez télécharger le fichier pour le modifier, puis le charger à nouveau pour publication, ou vous pouvez publier le fichier en l’état.

>[!NOTE]
>
>* La validation des fichiers volumineux prend plus de temps.
>* Les fichiers de feuilles d’envoi groupé pour plusieurs campagnes peuvent contenir jusqu’à 500 000 lignes de données. Si vous générez des données pour plusieurs campagnes et que les données combinées se composent de plus de 500 000 lignes, les données sont fractionnées par campagne en deux fichiers ou plus nommés `<bulksheet name>_1.tsv`, `<bulksheet name>_2.tsv`, etc.

>[!MORELIKETHIS]
>
>* [ (nouvelle interface utilisateur) À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupé](about.md)
>* [(Nouvelle interface utilisateur) Chargez une feuille d’envoi groupé ou un fichier d’erreur corrigé](upload.md)
>* [(Nouvelle interface utilisateur) Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](post.md)
>* [(Nouvelle interface utilisateur) Supprimer les feuilles d’envoi groupé et les fichiers d’erreur chargés](delete.md)
>* [(nouvelle interface utilisateur) Arrêter un traitement groupé en cours](stop-job.md)
