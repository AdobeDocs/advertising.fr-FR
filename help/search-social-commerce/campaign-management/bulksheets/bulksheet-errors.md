---
title: Erreurs de feuilles d’envoi groupé
description: Raisons potentielles de référence de chaque erreur de feuille d’envoi groupé.
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# Erreurs de feuilles d’envoi groupé

Search, Social et Commerce génère deux types de fichiers d’erreur lors des opérations de feuille d’envoi groupé :

* **Erreurs SE :** Lorsqu’un fichier est publié mais que le réseau publicitaire n’accepte pas toutes les données, un fichier d’erreur appelé `<uploaded file name>_se_errors.<extension used for the bulksheet>` est créé. Lorsque certaines lignes ont été acceptées, mais pas toutes, le fichier d’erreur affiche les lignes qui n’ont pas été publiées et une explication de chaque erreur afin que vous puissiez la corriger. Les erreurs sont incluses dans la colonne &quot;[!UICONTROL SE Error Message]&quot;.

>[!NOTE]
>
>Si vous publiez des [!DNL Google Ads] publicités qui enfreignent les politiques publicitaires du réseau publicitaire mais peuvent être admissibles à des exemptions, ces publicités sont automatiquement republiées avec des demandes d’exemption. Si la demande d’exemption échoue, les informations sur la violation sont incluses dans le fichier d’erreur.

* **Erreurs EF :** Lorsque l’opération de feuille d’envoi groupé ne peut pas charger ni traiter un fichier ou des lignes individuelles dans le fichier, elle crée un fichier d’erreur appelé `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Si le problème concerne des lignes individuelles, ces lignes sont incluses,
avec une explication de chaque erreur afin que vous puissiez la corriger. Les erreurs sont incluses dans la colonne &quot;[!UICONTROL EF Error Message]&quot;.

## [!UICONTROL SE Error] messages

Les erreurs dans la colonne [!UICONTROL SE Error] proviennent directement du réseau publicitaire.

## [!UICONTROL EF Error] messages

Les erreurs suivantes peuvent être incluses dans la colonne [!UICONTROL EF Error] des fichiers [!UICONTROL EF Errors].

### Télécharger/créer des erreurs

| Catégorie | Message | Description |
|----|----|----|
| Général | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | L’opération a complètement échoué en raison d’une erreur non classée ou non gérée. Si le problème persiste, contactez votre équipe de compte d’Adobe pour enquêter sur la cause. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Les solutions Search, Social et Commerce n’ont pas pu se synchroniser avec le réseau publicitaire avant de créer la feuille d’envoi groupé. Aucune feuille d’envoi groupé n’a donc été créée. Si le problème persiste, contactez votre équipe de compte d’Adobe. |

### Erreurs de chargement

| Catégorie | Message | Description |
|----|----|----|
| Général | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | L&#39;opération a complètement échoué. Si le problème persiste, contactez votre équipe de compte d’Adobe. |
| Toutes les entités | [!UICONTROL Invalid Fields.] \[champs non valides et erreur\] | Les données spécifiées sont manquantes ou non valides. |
|  | [!UICONTROL Invalid Reference Given] | L’identifiant de l’entité sur le réseau publicitaire, ou l’identifiant d’une entité parente (comme l’identifiant de compte), ne correspond pas à une entité dans Search, Social et Commerce. Cela peut se produire lorsque vous avez modifié l’ID dans la feuille d’envoi groupé. |
|  | [!UICONTROL &lt;Entity> is deleted or expired] | L’entité a expiré ou a été supprimée et vous ne pouvez pas en modifier les propriétés. L’entité peut être supprimée lorsqu’une personne a modifié manuellement l’état. |
|  | [!UICONTROL &lt;Entity> status should be Active or Paused] | (Nouvelles entités) Une nouvelle entité peut uniquement être &quot;Actif&quot; ou &quot;En pause&quot;. |
|  | [!UICONTROL Duplicate Entries are present] | Plusieurs lignes sont incluses pour la même entité, avec des attributs différents dans chaque ligne. Consolidation des modifications sur une seule ligne. |
|  | [!UICONTROL Invalid AMO ID given] | L’AMO ID de la ligne n’existe pas. Cela peut se produire si vous avez modifié l’identifiant dans la feuille d’envoi groupé. |
|  | [!UICONTROL Invalid row given] | La ligne ne contient pas suffisamment d’informations pour déterminer le type d’entité. Modifiez la ligne pour inclure tous les champs requis pour le type d’entité. |
| Comptes | [!UICONTROL Provide Valid Account Details] | (Feuilles d’envoi groupées pour plusieurs comptes) Les identifiants de compte ne sont pas inclus dans toutes les lignes. Entrez des valeurs pour l’une des combinaisons de colonnes suivantes pour chaque ligne : a) &quot;[!UICONTROL AMO ID]&quot; ou b) &quot;[!UICONTROL Account Name]&quot; et &quot;[!UICONTROL Platform]&quot;. |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search, Social et Commerce n’a pas accès au compte de réseau publicitaire. Vous ne pouvez donc pas créer ni modifier les données de campagne. Assurez-vous que les informations d’identification du compte de recherche sont correctes et que le compte est activé. |
| Campagne | [!UICONTROL Invalid Shopping Country specified] | (Campagnes d’achat) La valeur du champ &quot;[!UICONTROL Sales Country]&quot; n’est pas valide. Consultez la liste des pays valides [pour [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) et [pour [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| Tous les composants de campagne | [!UICONTROL Campaign creation failed] | La campagne parente n’a pas été créée. Cette entité n’a donc pas été créée. Assurez-vous que toutes les entités parentes contiennent tous les champs requis. |
| Groupe publicitaire | [!UICONTROL Campaign Row missing] | La campagne parente spécifiée n’existe pas. Le groupe publicitaire n’a donc pas été créé. Créez la campagne parente dans une nouvelle ligne. |
|  | [!UICONTROL New adgroup has both keywords and placement] | Un groupe publicitaire peut contenir des mots-clés ou des emplacements, mais pas les deux. Créez des groupes d’annonces distincts pour les mots-clés et les emplacements. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) Le groupe publicitaire n’a pas été créé, car il ne contient pas au moins un mot-clé. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) Le groupe publicitaire n’a pas été créé, car il n’inclut pas au moins une publicité. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) Le groupe publicitaire n’a pas été créé, car il n’inclut pas au moins une publicité. |
| Tous les composants de groupe publicitaire | [!UICONTROL Adgroup creation failed] | Le groupe d’annonces parent n’a pas été créé. Cette entité n’a donc pas pu être créée. Cela peut être dû à une erreur dans les champs du groupe publicitaire ou à l’échec de la campagne parente. Assurez-vous que toutes les entités parentes contiennent tous les champs requis. |
|  | [!UICONTROL Adgroup Row Missing] | Le groupe publicitaire parent spécifié n’existe pas. L’entité n’a donc pas pu être créée. Créez le groupe publicitaire parent dans une nouvelle ligne. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | Le champ &quot;[!UICONTROL Tracking Template]&quot; est uniquement destiné aux comptes qui utilisent des URL finales/avancées. Supprimez la valeur jusqu’à ce que vous ayez migré le compte pour utiliser les URL finales/avancées. |
| Publicité | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type>] | (Types d’annonces autres que le texte, le texte étendu, le produit, l’installation de l’application et la recherche dynamique) Vous ne pouvez modifier que l’état et l’URL de ce type d’annonce. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Chaque groupe d’annonces peut inclure jusqu’à 50 annonces, et cette feuille d’envoi groupé en inclut plus de 50. Réduire le nombre de publicités. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | La publicité se trouve dans une entité parent expirée ou supprimée, vous ne pouvez donc pas la modifier. |
| Mot-clé | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagne ou le groupe publicitaire parent est supprimé ou expiré, vous ne pouvez donc pas modifier l’entité. |
| Emplacement | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagne ou le groupe publicitaire parent est supprimé ou expiré, vous ne pouvez donc pas modifier l’entité. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Publicités Google) Vous pouvez enchérir sur des emplacements uniquement dans les campagnes du réseau de recherche uniquement ou uniquement sur le réseau de contenu, mais pas sur les campagnes qui ciblent à la fois les réseaux de recherche et de contenu. |
| Groupe de produits d’achat | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Chaque niveau de groupe de produits doit inclure un groupe &quot;[!UICONTROL Everything Else]&quot;. Vous ne pouvez pas supprimer manuellement un groupe &quot;[!UICONTROL Everything Else]&quot; ; il est automatiquement supprimé lorsque vous supprimez tous les autres groupes de produits au même niveau. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagne ou le groupe publicitaire parent est supprimé ou expiré, vous ne pouvez donc pas modifier l’entité. |
| Lien de site | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] uniquement) Le message est inexact ; chaque campagne peut comporter jusqu’à quatre liens de site (et non pas 10), et cette feuille d’envoi groupé en inclut plus de quatre. Supprimez certains liens de site. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | La campagne parente a expiré ou a été supprimée, de sorte que vous ne pouvez pas modifier le lien de site. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) Impossible de créer le lien de site, car la publicité n’a pas été créée. |
| Cible de l’emplacement | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | La campagne ou le groupe publicitaire parent est supprimé ou arrivé à expiration. Vous ne pouvez donc pas modifier les cibles d’emplacement. |
| Exclusions | [!UICONTROL Other than status is modified] | Vous ne pouvez modifier que l’état d’une exclusion (&quot;[!UICONTROL Active]&quot; ou &quot;[!UICONTROL Deleted]&quot;). |
| Cibles/audiences de la liste de remarketing Google | [!UICONTROL Invalid Audience given] | ([!DNL Google Ads] campagnes uniquement) La cible RLSA ne correspond pas à une RLSA existante (audience). Corrigez les valeurs des colonnes &quot;[!UICONTROL Audience]&quot; et &quot;[!UICONTROL RLSA Target]&quot;. |

### Post errors

Les erreurs suivantes se produisent uniquement dans les fichiers [!UICONTROL EF Errors]. La plupart des erreurs de publication proviennent du réseau publicitaire et sont incluses dans un fichier SE Errors.

| Catégorie | Message | Description |
|----|----|----|
| Général | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | L&#39;opération a complètement échoué. Si le problème persiste, contactez votre équipe de compte d’Adobe. |
| Toutes les entités | [!UICONTROL Entity] est publié sur le réseau publicitaire | L’entité a été publiée sur le réseau publicitaire, mais elle n’a pas été synchronisée simultanément avec Search, Social et Commerce. Les données d’entité ne sont donc pas immédiatement disponibles dans Search, Social et Commerce. Le processus de synchronisation est maintenant déclenché automatiquement.<br><br>Lorsque de grandes quantités de données sont synchronisées, les données peuvent ne pas être disponibles dans Search, Social et Commerce pendant plusieurs heures ou plus. |
| | [!UICONTROL Skipping &lt;ENTITY> creation since &lt;PARENT ENTITY> creation failed.] | L’entité parente n’a pas pu être créée. Cette entité enfant n’a donc pas été créée. |

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l’aide de feuilles d’envoi groupées](bulksheet-about.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](bulksheet-download.md)
>* [Valider les landing pages dans les fichiers de feuille d’envoi groupé](bulksheet-validate-landing-pages.md)
>* [Télécharger un fichier de feuille d’envoi groupé ou un fichier d’erreur corrigé](bulksheet-upload.md)
>* [ Publier des feuilles d’envoi groupées ou des fichiers d’erreur corrigés](bulksheet-post.md)
