---
title: Quand les composants de compte sont-ils créés ou supprimés par les flux d’inventaire ?
description: Découvrez les situations qui créent et suppriment des composants de compte lorsque vous validez des flux d’inventaire.
exl-id: 39a3cc2c-f956-4a89-a69d-687a27a38a1e
feature: Search Inventory Feeds
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '848'
ht-degree: 0%

---

# Quand les composants de compte sont-ils créés ou supprimés par les flux d’inventaire ?

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Lorsqu’un fichier de flux d’inventaire est propagé par le biais d’un modèle, les composants de compte sont créés et supprimés comme suit.

>[!NOTE]
>
>Les publicités en double ne sont jamais créées dans un groupe publicitaire.

| Scénario | Exemple | Action |
|----|----|----|
| Les données de flux incluent une nouvelle valeur pour une colonne utilisée dans un nom de campagne, un nom de groupe publicitaire, un mot-clé ou un groupe de produits. | Fichiers précédents :<br>Campaign=Hats<br>Campaign=Gloves<br><br>New file:<br>Campaign=Shoes | Une campagne, un groupe publicitaire, un mot-clé ou un groupe de produits est créé s’il n’existe pas sur le réseau publicitaire. |
| Les données de flux contiennent une nouvelle valeur pour une colonne utilisée dans une publicité. | Fichier précédent : une annonce publicitaire incluait price=20<br><br>Nouveau fichier : pour la même annonce, price=10 | Lorsque la copie de l’annonce publicitaire pour [!DNL Microsoft Advertising] annonces textuelles, [!DNL Yahoo! Japan ads] ou [!DNL Yandex] est modifiée, l’annonce publicitaire existante est supprimée et une nouvelle annonce est créée.<br><br>Lorsque la copie d’annonce est modifiée pour d’autres types d’annonce ou lorsque la colonne applicable est utilisée pour un paramètre d’annonce [!DNL Google Ads] ({param1} ou {param2}) dans une annonce, l’annonce existante est mise à jour. |
| Les paramètres du modèle pour la campagne, le groupe publicitaire, le mot-clé ou le groupe de produits ont changé depuis la dernière propagation. | Paramètre précédent :Keyword=[Mot-clé]<br><br>Nouveau paramètre : Mot-clé=&lt;Couleur>[Mot-clé] | Une campagne, un groupe publicitaire, un mot-clé ou un groupe de produits est créé s’il n’existe pas sur le réseau publicitaire. |
| Les paramètres de modèle d’une annonce publicitaire ont été modifiés depuis la dernière propagation. | Paramètre précédent : Ad description=« Achetez [category] maintenant. »<br><br>Nouveau paramètre : description de l’annonce publicitaire=« Achetez [brand] maintenant. » | Lorsque la copie de l’annonce publicitaire pour [!DNL Microsoft Advertising] annonces textuelles, [!DNL Yahoo! Japan ads] ou [!DNL Yandex] est modifiée, l’annonce publicitaire existante est supprimée et une nouvelle annonce est créée.<br><br>Lorsque la copie publicitaire est modifiée pour d’autres types d’annonces ou lorsque la modification reflète une modification de la colonne utilisée pour un seul paramètre d’annonce [!DNL Google Ads] ({param1} ou {param2}) dans une annonce, l’annonce existante est mise à jour. |
| Les nouvelles données de flux n’incluent pas de ligne pour une campagne ou un groupe publicitaire existant. | s.o. | Les campagnes et groupes publicitaires existants restent en l’état. |
| Les nouvelles données de flux n’incluent pas de ligne pour un groupe publicitaire, une annonce, un mot-clé ou un groupe de produits existant. | s.o. | Le groupe publicitaire, l’annonce publicitaire, le mot-clé ou le groupe de produits existant reste en l’état, est mis en pause ou est supprimé, conformément aux paramètres des données de [flux](feed-settings-manage.md#feed-data-settings). |
| Les nouvelles données de flux d’un groupe de produits parent existant n’incluent pas de lignes pour ses groupes de produits enfants existants. | s.o. | Le groupe de produits parent existant reste en l’état ou est supprimé, conformément aux [paramètres des données de flux](feed-settings-manage.md#feed-data-settings). <b>Remarque :</b> si les paramètres de données de flux sont configurés pour mettre en pause les éléments de ligne manquants, le groupe de produits parent est toujours supprimé, car vous ne pouvez pas mettre en pause les groupes de produits. |
| Les nouvelles données de flux comprennent une ligne pour un groupe publicitaire, une publicité, un mot-clé ou un groupe de produits qui était a) dans les données précédentes, mais qui était b) omis depuis et qui a été mis en pause conformément aux [ paramètres des données de flux ](feed-settings-manage.md#feed-data-settings). | s.o. | Le groupe publicitaire, l’annonce publicitaire, le mot-clé ou le groupe de produits existant est réactivé, sans perdre d’historique ni de score de qualité. |
| Les nouvelles données de flux comprennent une ligne pour un groupe publicitaire, une publicité, un mot-clé ou un groupe de produits qui était a) dans les données précédentes, mais qui était b) omis depuis et qui a été supprimé conformément aux [ paramètres des données de flux ](feed-settings-manage.md#feed-data-settings). | s.o. | Un groupe publicitaire, une annonce, un mot-clé ou un groupe de produits est créé. |
| Vous avez désactivé l’option au niveau de la campagne ou du groupe publicitaire sur « [!UICONTROL Delete negative keywords when omitted from list] ». | La liste des mots-clés négatifs inclut « coupé » et « voiture de sport ».<br><br>Le groupe publicitaire comprend déjà le mot-clé négatif « SUV ». | Tous les mots-clés négatifs existants qui ne figurent pas sur la liste restent en l’état. |
| Vous avez activé l’option au niveau de la campagne ou du groupe publicitaire sur « [!UICONTROL Delete negative keywords when omitted from list] ». Il existe également des mots-clés négatifs qui ne figurent pas dans la liste. | La liste des mots-clés négatifs inclut « coupé » et « voiture de sport ».<br><br>Le groupe publicitaire comprend déjà le mot-clé négatif « SUV ». | Tous les mots-clés négatifs non spécifiés précédemment créés à l’aide du modèle sont supprimés lorsqu’un fichier de flux est propagé dans le modèle. Cependant, tous les mots-clés négatifs non spécifiés créés à l’aide d’autres moyens (tels que dans les feuilles d’envoi groupé simples, les vues [!UICONTROL Campaigns] ou dans l’éditeur publicitaire du réseau publicitaire) restent en l’état. |
| La date de fin planifiée pour les composants d’un fichier de flux publié se produit. | s.o. | Les campagnes existantes restent en l’état. Les groupes d’annonces, les annonces publicitaires et les mots-clés existants restent en l’état, sont suspendus ou sont supprimés, conformément aux paramètres des données de [flux](feed-settings-manage.md#feed-data-settings). |
| Le niveau de stock d’un article chute en dessous d’un minimum spécifié dans les paramètres [données de flux](feed-settings-manage.md#feed-data-settings). | Fichier précédent : stock=10<br><br>Nouveau fichier : stock=0 | Les campagnes existantes restent en l’état. Les groupes publicitaires, les publicités, les mots-clés et les groupes de produits existants sont suspendus ou supprimés, selon les paramètres des [données de flux](feed-settings-manage.md#feed-data-settings). |
| Le niveau de stock d’un article remonte au-dessus d’un minimum spécifié dans les [ paramètres des données de flux ](feed-settings-manage.md#feed-data-settings). | Fichier précédent : stock=0<br><br> Nouveau fichier : stock=10 | Lorsque les publicités, mots-clés ou groupes de produits existants sont mis en pause, ils sont réactivés, sans perdre d’historique ni de score de qualité. Lorsqu’il n’existe aucune publicité, aucun mot-clé ou groupe de produits (par exemple, s’ils ont été supprimés précédemment parce que le niveau de stock était inférieur au minimum), de nouveaux mots sont créés. |

>[!MORELIKETHIS]
>
>* [À propos de l’automatisation de la gestion des annonces à l’aide des flux d’inventaire](inventory-feeds-about.md)
