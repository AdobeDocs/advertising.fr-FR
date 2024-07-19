---
title: Quand les composants de compte sont-ils créés ou supprimés par les flux de stock ?
description: Découvrez les situations dans lesquelles créer et supprimer des composants de compte lorsque vous publiez des flux d’inventaire.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '853'
ht-degree: 0%

---

# Quand les composants de compte sont-ils créés ou supprimés par les flux de stock ?

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Lorsqu’un fichier de flux d’inventaire est propagé par un modèle, les composants de compte sont créés et supprimés comme suit.

>[!NOTE]
>
>Les publicités en double ne sont jamais créées dans un groupe publicitaire.

| Scénario | Exemple | Action |
|----|----|----|
| Les données de flux incluent une nouvelle valeur pour une colonne utilisée dans le nom d’une campagne, le nom du groupe publicitaire, le mot-clé ou le groupe de produits. | Fichiers précédents :<br>Campaign=Hats<br>Campaign=Gants<br><br>Nouveau fichier :<br>Campaign=Chaussures | Une nouvelle campagne, un nouveau groupe publicitaire, un nouveau mot-clé ou un nouveau groupe de produits est créé s’il n’existe pas sur le réseau publicitaire. |
| Les données de flux contiennent une nouvelle valeur pour une colonne utilisée dans une publicité. | Fichier précédent : une publicité inclus price=20<br><br>Nouveau fichier : pour la même publicité, price=10 | Lorsque la copie de publicité pour [!DNL Microsoft Advertising] publicités textuelles étendues, [!DNL Yahoo! Japan ads] ou [!DNL Yandex] publicités est modifiée, la publicité existante est supprimée et une nouvelle est créée.<br><br>Lorsque la copie de la publicité est modifiée pour d’autres types de publicité ou lorsque la colonne applicable est utilisée pour un paramètre de publicité [!DNL Google Ads] ({param1} ou {param2}) dans une publicité, la publicité existante est mise à jour. |
| Les paramètres du modèle pour la campagne, le groupe publicitaire, le mot-clé ou le groupe de produits ont changé depuis la dernière propagation. | Paramètre précédent : Keyword=[Keyword]<br><br>Nouveau paramètre : Keyword=&lt;Color>[Keyword] | Une nouvelle campagne, un nouveau groupe publicitaire, un nouveau mot-clé ou un nouveau groupe de produits est créé s’il n’existe pas sur le réseau publicitaire. |
| Les paramètres du modèle d’une publicité ont changé depuis la dernière propagation. | Paramètre précédent : description de la publicité=&quot;Achetez [catégorie] maintenant.&quot;<br><br>Nouveau paramètre : Ad description=&quot;Buy [brand] now.&quot; | Lorsque la copie de publicité pour [!DNL Microsoft Advertising] publicités textuelles étendues, [!DNL Yahoo! Japan ads] ou [!DNL Yandex] publicités est modifiée, la publicité existante est supprimée et une nouvelle est créée.<br><br>Lorsque la copie de la publicité est modifiée pour d’autres types de publicité ou lorsque la modification reflète une modification dans la colonne utilisée pour un seul paramètre de publicité [!DNL Google Ads] ({param1} ou {param2}) dans une publicité, la publicité existante est mise à jour. |
| Les nouvelles données de flux n’incluent pas de ligne pour une campagne ou un groupe publicitaire existant. | n/a | Les campagnes et groupes publicitaires existants restent inchangés. |
| Les nouvelles données de flux n’incluent pas de ligne pour un groupe publicitaire, une publicité, un mot-clé ou un groupe de produits existant. | n/a | Le groupe publicitaire, la publicité, le mot-clé ou le groupe de produits existant reste tel quel, est suspendu ou est supprimé, selon les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). |
| Les nouvelles données de flux pour un groupe de produits parent existant n’incluent pas de lignes pour ses groupes de produits enfants existants. | n/a | Le groupe de produits parent existant reste en l’état ou est supprimé, selon les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). <b>Remarque :</b> Si les paramètres des données de flux sont configurés pour suspendre les éléments de ligne manquants, le groupe de produits parent est toujours supprimé car vous ne pouvez pas suspendre les groupes de produits. |
| Les nouvelles données de flux incluent une ligne pour un groupe publicitaire, une publicité, un mot-clé ou un groupe de produits qui était a) dans les données précédentes mais b) a été omis depuis et a été suspendue conformément aux [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). | n/a | Le groupe publicitaire, la publicité, le mot-clé ou le groupe de produits existant est réactivé, sans perdre d’historique ni le score de qualité. |
| Les nouvelles données de flux incluent une ligne pour un groupe publicitaire, une publicité, un mot-clé ou un groupe de produits qui était a) dans les données précédentes mais b) a été omis depuis et a été supprimé conformément aux [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). | n/a | Un groupe publicitaire, une publicité, un mot-clé ou un groupe de produits est alors créé. |
| Vous avez désactivé l’option de niveau campagne ou groupe publicitaire sur &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot;. | La liste des mots-clés négatifs inclut &quot;coupé&quot; et &quot;voiture de sport&quot;.<br><br>Le groupe publicitaire comprend déjà le mot-clé négatif &quot;SUV&quot;. | Tous les mots-clés négatifs existants qui ne figurent pas sur la liste restent inchangés. |
| Vous avez activé l’option de niveau campagne ou groupe publicitaire sur &quot;[!UICONTROL Delete negative keywords when omitted from list]&quot; et les mots-clés négatifs qui ne figurent pas sur la liste existent. | La liste des mots-clés négatifs inclut &quot;coupé&quot; et &quot;voiture de sport&quot;.<br><br>Le groupe publicitaire comprend déjà le mot-clé négatif &quot;SUV&quot;. | Les mots-clés négatifs non spécifiés précédemment créés à l’aide du modèle sont supprimés lorsqu’un fichier de flux est propagé par le modèle. Cependant, tous les mots-clés négatifs non spécifiés créés par d’autres moyens (par exemple dans des feuilles d’envoi groupées ordinaires, les vues [!UICONTROL Campaigns] ou dans l’éditeur de publicités du réseau publicitaire) restent inchangés. | | La date de fin planifiée des composants d’un fichier de flux publié se produit. | n/a | Les campagnes existantes restent inchangées. Les groupes publicitaires, publicités et mots-clés existants restent tels quels, sont suspendus ou sont supprimés, selon les [ paramètres de données de flux](feed-settings-manage.md#feed-data-settings). |
| Le niveau de stock d’un élément se situe en dessous d’un minimum spécifié dans les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). | Fichier précédent : stock=10<br><br>Nouveau fichier : stock=0 | Les campagnes existantes restent inchangées. Les groupes d’annonces, publicités, mots-clés et groupes de produits existants sont suspendus ou supprimés, selon les [ paramètres de données de flux ](feed-settings-manage.md#feed-data-settings). |
| Le niveau de stock d’un élément remonte au-dessus d’un minimum spécifié dans les [paramètres de données de flux](feed-settings-manage.md#feed-data-settings). | Fichier précédent : stock=0<br><br> Nouveau fichier : stock=10 | Lorsque les publicités, mots-clés ou groupes de produits existants sont suspendus, ils sont réactivés, sans perdre d’historique ni le score de qualité. Lorsqu’il n’existe aucune publicité, mot-clé ou groupe de produits (s’ils ont été supprimés précédemment car le niveau de stock était inférieur au minimum), de nouveaux groupes sont créés. |

>[!MORELIKETHIS]
>
>* [À propos de l’automatisation de la gestion des publicités à l’aide de flux d’inventaire](inventory-feeds-about.md)
