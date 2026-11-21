---
title: Quand les composants de compte sont-ils créés ou supprimés par les flux d’inventaire ?
description: Découvrez les situations qui créent et suppriment des composants de compte lorsque vous validez des flux d’inventaire.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
TQID: 'https://experienceleague.adobe.com/lo1FGJlZyyrO49IVCt308TaH65Eq-ZgRTafKSMTomHI'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: f286be7c-8102-5b20-b4ca-1aadd651703f
    internal-label: Search Inventory Feeds
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: f2335fa20fd8685b13b5bcebe63c21c7e3600551
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 0%
---
# Quand les composants de compte sont-ils créés ou supprimés par les flux d’inventaire ?

*[!DNL Google Ads], [!DNL LY Ads] (actions de suppression uniquement), [!DNL Microsoft Advertising] et [!DNL Yandex] comptes uniquement*

Lorsqu’un fichier de flux d’inventaire est propagé par le biais d’un modèle, les composants de compte sont créés et supprimés comme suit.

>[!NOTE]
>
>Les publicités en double ne sont jamais créées dans un groupe publicitaire.

| Scénario | Exemple | Action |
|----|----|----|
| Les données de flux incluent une nouvelle valeur pour une colonne utilisée dans un nom de campagne, un nom de groupe publicitaire, un mot-clé ou un groupe de produits. | Fichiers précédents :<br>Campaign=Hats<br>Campaign=Gloves<br><br>Nouveau fichier :<br>Campaign=Shoes | Une campagne, un groupe publicitaire, un mot-clé ou un groupe de produits est créé s’il n’existe pas sur le réseau publicitaire. |
| Les données de flux contiennent une nouvelle valeur pour une colonne utilisée dans une publicité. | Fichier précédent : une publicité incluait un prix=20<br><br>Nouveau fichier : pour la même publicité, un prix=10 | Lorsque la copie de l’annonce pour [!DNL LY Ads], [!DNL Microsoft Advertising] annonces textuelles développées ou [!DNL Yandex] annonces est modifiée, l’annonce existante est supprimée et une nouvelle annonce est créée.<br><br>Lorsque la copie de publicité est modifiée pour d&#39;autres types de publicité ou lorsque la colonne applicable est utilisée pour un paramètre de publicité [!DNL Google Ads] ({param1} ou {param2}) dans une publicité, la publicité existante est mise à jour. |
| Les paramètres du modèle pour la campagne, le groupe publicitaire, le mot-clé ou le groupe de produits ont changé depuis la dernière propagation. | Paramètre précédent:Keyword=[Mot-clé]<br><br>Nouveau paramètre : Mot-clé=&lt;Color>[Mot-clé] | Une campagne, un groupe publicitaire, un mot-clé ou un groupe de produits est créé s’il n’existe pas sur le réseau publicitaire. |
| Les paramètres de modèle d’une annonce publicitaire ont été modifiés depuis la dernière propagation. | Paramètre précédent : Description de l’annonce=« Achetez [la catégorie] maintenant.« <br><br>Nouveau paramètre : Description de l’annonce=« Achetez [la marque] maintenant. » | Lorsque la copie de l’annonce pour [!DNL LY Ads], [!DNL Microsoft Advertising] annonces textuelles développées ou [!DNL Yandex] annonces est modifiée, l’annonce existante est supprimée et une nouvelle annonce est créée.<br><br>Lorsque la copie d&#39;annonce est modifiée pour d&#39;autres types d&#39;annonce ou lorsque la modification reflète une modification dans la colonne utilisée pour un seul paramètre d&#39;annonce [!DNL Google Ads] ({param1} ou {param2}) dans une annonce, l&#39;annonce existante est mise à jour. |
| Les nouvelles données de flux n’incluent pas de ligne pour une campagne ou un groupe publicitaire existant. | s.o. | Les campagnes et groupes publicitaires existants restent en l’état. |
| Les nouvelles données de flux n’incluent pas de ligne pour un groupe publicitaire, une annonce, un mot-clé ou un groupe de produits existant. | s.o. | Le groupe publicitaire, la publicité, le mot-clé ou le groupe de produits existant reste en l&#39;état, est suspendu ou supprimé, selon les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). |
| Les nouvelles données de flux d’un groupe de produits parent existant n’incluent pas de lignes pour ses groupes de produits enfants existants. | s.o. | Le groupe de produits parent existant reste en l&#39;état ou est supprimé, conformément aux [paramètres des données de flux](feed-settings-manage.md#feed-data-settings). <b>Remarque :</b> Si les paramètres des données de flux sont configurés pour mettre en pause les éléments de ligne manquants, le groupe de produits parent est toujours supprimé, car vous ne pouvez pas mettre en pause les groupes de produits. |
| Les nouvelles données de flux incluent une ligne pour un groupe publicitaire, une publicité, un mot-clé ou un groupe de produits qui était a) dans les données précédentes, mais b) qui a été omis depuis et qui a été suspendu selon les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). | s.o. | Le groupe publicitaire, l’annonce publicitaire, le mot-clé ou le groupe de produits existant est réactivé, sans perdre d’historique ni de score de qualité. |
| Les nouvelles données de flux incluent une ligne pour un groupe publicitaire, une publicité, un mot-clé ou un groupe de produits qui était a) dans les données précédentes, mais b) qui a été omis depuis et qui a été supprimé conformément aux [paramètres des données de flux](feed-settings-manage.md#feed-data-settings). | s.o. | Un groupe publicitaire, une annonce, un mot-clé ou un groupe de produits est créé. |
| Vous avez désactivé l&#39;option au niveau de la campagne ou du groupe publicitaire sur « [!UICONTROL Delete negative keywords when omitted from list] ». | La liste des mots-clés négatifs comprend « coupé » et « voiture de sport ».<br><br>Le groupe publicitaire comprend déjà le mot-clé négatif « SUV ». | Tous les mots-clés négatifs existants qui ne figurent pas sur la liste restent en l’état. |
| Vous avez activé l&#39;option au niveau de la campagne ou du groupe publicitaire sur « [!UICONTROL Delete negative keywords when omitted from list] » et il existe des mots-clés négatifs qui ne figurent pas dans la liste. | La liste des mots-clés négatifs comprend « coupé » et « voiture de sport ».<br><br>Le groupe publicitaire comprend déjà le mot-clé négatif « SUV ». | Tous les mots-clés négatifs non spécifiés précédemment créés à l’aide du modèle sont supprimés lorsqu’un fichier de flux est propagé dans le modèle. Cependant, tous les mots-clés négatifs non spécifiés créés à l’aide d’autres moyens (tels que dans les feuilles d’envoi groupé simples, les vues [!UICONTROL Campaigns] ou dans l’éditeur publicitaire du réseau publicitaire) restent en l’état. |
| La date de fin planifiée pour les composants d’un fichier de flux publié se produit. | s.o. | Les campagnes existantes restent en l’état. Les groupes publicitaires, publicités et mots-clés existants restent en l’état, sont suspendus ou sont supprimés, selon les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). |
| Le niveau de stock d&#39;un article tombe en dessous d&#39;un minimum spécifié dans les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). | Fichier précédent : stock=10<br><br>Nouveau fichier : stock=0 | Les campagnes existantes restent en l’état. Les groupes publicitaires, les publicités, les mots-clés et les groupes de produits existants sont suspendus ou supprimés, selon les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). |
| Le niveau de stock d’un article repasse au-dessus d’un minimum spécifié dans les [paramètres des données de flux](feed-settings-manage.md#feed-data-settings). | Fichier précédent : stock=0<br><br> Nouveau fichier : stock=10 | Lorsque les publicités, mots-clés ou groupes de produits existants sont mis en pause, ils sont réactivés, sans perdre d’historique ni de score de qualité. Lorsqu’il n’existe aucune publicité, aucun mot-clé ou groupe de produits (par exemple, s’ils ont été supprimés précédemment parce que le niveau de stock était inférieur au minimum), de nouveaux mots sont créés. |

>[!MORELIKETHIS]
>
>* [À propos de l&#39;automatisation de la gestion des annonces à l&#39;aide des flux d&#39;inventaire](inventory-feeds-about.md)
