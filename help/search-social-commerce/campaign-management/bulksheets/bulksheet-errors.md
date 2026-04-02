---
title: Erreurs de feuilles d’envoi groupé
description: Référencez les raisons potentielles de chaque erreur de feuille d’envoi groupé.
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/7jGIKXI-Un6mnstJlPDqk0q4yB6k3tEsqHngD1cCyEw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1137
ht-degree: 1%

---

# Erreurs de feuilles d’envoi groupé

Search, Social et Commerce génèrent deux types de fichiers d’erreur lors des opérations de feuilles d’envoi groupé :

* **Erreurs SE :** lorsqu’un fichier est publié mais que le réseau publicitaire n’accepte pas toutes les données, un fichier d’erreur appelé `<uploaded file name>_se_errors.<extension used for the bulksheet>` est créé. Lorsque certaines lignes ont été acceptées, mais pas toutes, le fichier d’erreur affiche les lignes qui n’ont pas été publiées et une explication de chaque erreur afin que vous puissiez la corriger. Les erreurs sont incluses dans la colonne « [!UICONTROL SE Error Message] ».

>[!NOTE]
>
>Si vous publiez des publicités [!DNL Google Ads] qui enfreignent les politiques publicitaires du réseau publicitaire, mais qui peuvent être admissibles à des exemptions, alors ces publicités sont automatiquement republiées avec des demandes d&#39;exemption. Si la demande d’exemption échoue, les informations sur la violation sont incluses dans le fichier d’erreur.

* **Erreurs EF :** lorsque l’opération de feuille d’envoi groupé ne peut pas charger ni traiter un fichier ou des lignes individuelles dans le fichier, elle crée un fichier d’erreur appelé `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. Si le problème concerne des lignes individuelles, ces lignes sont incluses,
avec une explication de chaque erreur afin que vous puissiez la corriger. Les erreurs sont incluses dans la colonne « [!UICONTROL EF Error Message] ».

## [!UICONTROL SE Error] des messages

Les erreurs dans la colonne [!UICONTROL SE Error] proviennent directement du réseau publicitaire.

## [!UICONTROL EF Error] des messages

Les erreurs suivantes peuvent être incluses dans la colonne [!UICONTROL EF Error] des fichiers [!UICONTROL EF Errors].

### Erreurs de téléchargement/création

| Catégorie | Message | Description |
|----|----|----|
| Général | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | L&#39;opération a complètement échoué en raison d&#39;une erreur non classée ou non gérée. Si le problème persiste, contactez l’équipe chargée de votre compte Adobe pour en étudier la cause. |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Search, Social et Commerce n’ont pas pu être synchronisés avec le réseau publicitaire avant la création de la feuille d’envoi groupé, aucune feuille d’envoi groupé n’a donc été créée. Si le problème persiste, contactez l’équipe chargée de votre compte Adobe. |

### Erreurs de chargement

| Catégorie | Message | Description |
|----|----|----|
| Général | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | L’opération a complètement échoué. Si le problème persiste, contactez l’équipe chargée de votre compte Adobe. |
| Toutes les entités | [!UICONTROL Invalid Fields.] \[champs non valides et erreur\] | Les données spécifiées sont manquantes ou non valides. |
|  | [!UICONTROL Invalid Reference Given] | L’ID de l’entité sur le réseau publicitaire ou un ID d’entité parent (tel que l’ID de compte) ne correspond pas à une entité dans Search, Social et Commerce. Cela peut se produire lorsque vous avez modifié l’ID dans la feuille d’envoi groupé. |
|  | [!UICONTROL <Entity> is deleted or expired] | L’entité a expiré ou a été supprimée, et vous ne pouvez pas modifier ses propriétés. L&#39;entité peut être supprimée lorsqu&#39;une personne a modifié manuellement le statut. |
|  | [!UICONTROL <Entity> status should be Active or Paused] | (Nouvelles entités) Une nouvelle entité ne peut être que « Active » ou « Paused ». |
|  | [!UICONTROL Duplicate Entries are present] | Plusieurs lignes sont incluses pour la même entité, avec des attributs différents dans chaque ligne. Consolidez les modifications dans une seule ligne. |
|  | [!UICONTROL Invalid AMO ID given] | L&#39;ID AMO pour la ligne n&#39;existe pas. Cela peut se produire si vous avez modifié l’ID dans la feuille d’envoi groupé. |
|  | [!UICONTROL Invalid row given] | La ligne ne contient pas suffisamment d’informations pour déterminer le type d’entité. Modifiez la ligne afin d’inclure tous les champs obligatoires pour le type d’entité. |
| Comptes | [!UICONTROL Provide Valid Account Details] | (Feuilles d’envoi groupé pour plusieurs comptes) Les identifiants de compte ne sont pas inclus dans toutes les lignes. Entrez des valeurs pour l&#39;une des combinaisons de colonnes suivantes pour chaque ligne : a) « [!UICONTROL AMO ID] » ou b) « [!UICONTROL Account Name] » et « [!UICONTROL Platform] ». |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search, Social et Commerce n’ont pas accès au compte du réseau publicitaire. Vous ne pouvez donc pas créer ni modifier les données de la campagne. Assurez-vous que les informations d’identification du compte de recherche sont correctes et que le compte est activé. |
| Campagne | [!UICONTROL Invalid Shopping Country specified] | (Campagnes d’achat) La valeur du champ « [!UICONTROL Sales Country] » n’est pas valide. Consultez une liste de pays valides [par [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) et [par [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| Tous les composants de la campagne | [!UICONTROL Campaign creation failed] | La campagne parent n’a pas été créée, donc cette entité n’a pas été créée. Assurez-vous que toutes les entités parentes contiennent tous les champs obligatoires. |
| Groupe publicitaire | [!UICONTROL Campaign Row missing] | La campagne parent spécifiée n’existe pas. Le groupe publicitaire n’a donc pas été créé. Créez la campagne parente dans une nouvelle ligne. |
|  | [!UICONTROL New adgroup has both keywords and placement] | Un groupe publicitaire peut contenir des mots-clés ou des emplacements, mais pas les deux. Créez des groupes publicitaires distincts pour les mots-clés et les emplacements. |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) Le groupe publicitaire n&#39;a pas été créé car il ne contient pas au moins un mot-clé. |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex]) Le groupe publicitaire n&#39;a pas été créé parce qu&#39;il n&#39;inclut pas au moins une annonce. |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex]) Le groupe publicitaire n&#39;a pas été créé parce qu&#39;il n&#39;inclut pas au moins une annonce. |
| Tous les composants du groupe publicitaire | [!UICONTROL Adgroup creation failed] | Le groupe publicitaire parent n&#39;a pas été créé. Cette entité n&#39;a donc pas pu être créée. Cela peut être dû à une erreur dans les champs du groupe publicitaire ou à l’échec de la campagne parente. Assurez-vous que toutes les entités parentes contiennent tous les champs obligatoires. |
|  | [!UICONTROL Adgroup Row Missing] | Le groupe publicitaire parent spécifié n&#39;existe pas. L&#39;entité n&#39;a donc pas pu être créée. Créez le groupe publicitaire parent sur une nouvelle ligne. |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | Le champ « [!UICONTROL Tracking Template] » concerne uniquement les comptes qui utilisent des URL finales/avancées. Supprimez la valeur jusqu’à ce que vous ayez migré le compte pour utiliser les URL finales/avancées. |
| Annonce publicitaire | [!UICONTROL Cannot modify attributes other than status code and url for <ad type>] | (Types d’annonces autres que texte, texte développé, produit, installation d’application et recherche dynamique) Vous ne pouvez modifier que le statut et l’URL de ce type d’annonce. |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | Chaque groupe d’annonces peut inclure jusqu’à 50 annonces, et cette feuille d’envoi groupé en inclut plus de 50. Réduisez le nombre de publicités. |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | L’annonce publicitaire se trouve dans une entité parent expirée ou supprimée. Vous ne pouvez donc pas la modifier. |
| Mot-clé | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagne ou le groupe publicitaire parent est supprimé ou a expiré. Vous ne pouvez donc pas modifier l’entité. |
| Placement | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagne ou le groupe publicitaire parent est supprimé ou a expiré. Vous ne pouvez donc pas modifier l’entité. |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google Ads) Vous pouvez enchérir sur des emplacements uniquement dans des campagnes sur le réseau de recherche uniquement ou sur le réseau de contenu uniquement, mais pas sur des campagnes qui ciblent à la fois les réseaux de recherche et de contenu. |
| Groupe de produits d’achat | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | Chaque niveau du groupe de produits doit inclure un groupe « [!UICONTROL Everything Else] ». Vous ne pouvez pas supprimer manuellement un groupe « [!UICONTROL Everything Else] » ; il est automatiquement supprimé lorsque vous supprimez tous les autres groupes de produits au même niveau. |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | La campagne ou le groupe publicitaire parent est supprimé ou a expiré. Vous ne pouvez donc pas modifier l’entité. |
| Lien du site | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] uniquement) Le message est inexact. Chaque campagne peut inclure jusqu’à quatre (et non pas dix) liens de site, et cette feuille d’envoi groupé en comprend plus de quatre. Supprimez certains liens de site. |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | La campagne parente a expiré ou a été supprimée. Vous ne pouvez donc pas modifier le lien du site. |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) Impossible de créer le lien du site, car l&#39;annonce n&#39;a pas été créée. |
| Cible de l’emplacement | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | La campagne ou le groupe publicitaire parent est supprimé ou a expiré. Vous ne pouvez donc pas modifier les cibles d’emplacement. |
| Exclusions | [!UICONTROL Other than status is modified] | Vous ne pouvez modifier que le statut d&#39;une exclusion (« [!UICONTROL Active] » ou « [!UICONTROL Deleted] »). |
| Cibles/audiences de la liste de remarketing Google | [!UICONTROL Invalid Audience given] | (Campagnes [!DNL Google Ads] uniquement) La cible RLSA ne correspond pas à un RLSA existant (audience). Corrigez les valeurs dans les colonnes « [!UICONTROL Audience] » et « [!UICONTROL RLSA Target] ». |

### Erreurs de publication

Les erreurs suivantes se produisent dans les fichiers [!UICONTROL EF Errors] uniquement. La plupart des erreurs de publication proviennent du réseau publicitaire et sont incluses dans un fichier d&#39;erreurs SE.

| Catégorie | Message | Description |
|----|----|----|
| Général | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | L’opération a complètement échoué. Si le problème persiste, contactez l’équipe chargée de votre compte Adobe. |
| Toutes les entités | [!UICONTROL Entity] est publié sur le réseau publicitaire | L’entité a été publiée sur le réseau publicitaire, mais elle n’a pas été synchronisée en même temps sur Search, Social et Commerce, de sorte que les données d’entité ne sont pas immédiatement disponibles dans Search, Social et Commerce. Le processus de synchronisation est désormais automatiquement déclenché.<br><br>Lorsque de grandes quantités de données sont synchronisées, les données peuvent ne pas être disponibles dans Search, Social et Commerce pendant plusieurs heures ou plus. |
| | [!UICONTROL Skipping <ENTITY> creation since <PARENT ENTITY> creation failed.] | L&#39;entité parent n&#39;a pas pu être créée. Cette entité enfant n&#39;a donc pas été créée. |

>[!MORELIKETHIS]
>
>* [À propos de la gestion des données de campagne à l&#39;aide de feuilles d&#39;envoi groupé](bulksheet-about.md)
>* [Télécharger/créer un fichier de feuille d’envoi groupé](bulksheet-download.md)
>* [Valider les pages de destination dans les fichiers de feuille d’envoi groupé](bulksheet-validate-landing-pages.md)
>* [Charger un fichier de feuille d’envoi groupé ou un fichier d’erreur corrigé](bulksheet-upload.md)
>* [Publier des feuilles d’envoi groupé ou des fichiers d’erreur corrigés](bulksheet-post.md)
