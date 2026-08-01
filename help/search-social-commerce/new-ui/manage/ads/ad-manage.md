---
title: Gestion des publicités
description: Découvrez comment créer et gérer des annonces, y compris les types d’annonces disponibles.
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6a479ae0bb30d609b16a343efcec296137b9ab43
workflow-type: tm+mt
source-wordcount: 1733
ht-degree: 0%

---

# Gestion des publicités

*Fonction*

Comptes *[!DNL Google Ads], [!DNL LY Ads], [!DNL Microsoft Advertising], [!DNL Yandex] et [!DNL Baidu] existants uniquement*

Une publicité appartient à un groupe publicitaire et contient le contenu présenté aux utilisateurs, tel que le titre, la description, l’image ou d’autres éléments créatifs, selon le réseau publicitaire et le type de publicité.

Une fois que vous [rendez un compte de réseau publicitaire accessible via une connexion API](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md) et que Search, Social et Commerce a synchronisé les données du compte avec le réseau publicitaire, vous pouvez créer des annonces pour un [type de campagne pris en charge](/help/search-social-commerce/introduction/supported-inventory.md). Vous pouvez également modifier le statut des publicités.

Pour plus d’informations sur les fonctionnalités disponibles pour chaque réseau publicitaire, reportez-vous à [ Inventaire pris en charge ](/help/search-social-commerce/introduction/supported-inventory.md).

## À propos de la vue [!UICONTROL Ads] {#ad-view-about}

La vue [!UICONTROL Manage] > [!UICONTROL Ads] répertorie toutes les annonces dans la vue filtrée pour le compte d’annonceur sélectionné.

### Actions disponibles

* [Création d’une publicité](#ad-create)

* [Renommer une annonce depuis la ligne](#ad-rename)

* [Modifier les paramètres de l’annonce publicitaire](#ad-edit)

* [Modification du statut d’une annonce publicitaire ou suppression de celui-ci](#ad-status)

* [Gérer les rapports de vue de données à partir de la vue [!UICONTROL Ads]](#ad-reports)

## Types d’annonces disponibles {#ad-types}

Vous pouvez créer et gérer des types d’annonces pris en charge pour les groupes publicitaires au sein d’un compte réseau d’annonces synchronisé :

* **Annonces textuelles ou annonces textuelles développées** pour un groupe publicitaire dans une campagne qui cible le réseau de recherche. Les annonces textuelles peuvent inclure des paramètres de suivi facultatifs qui remplacent les paramètres au niveau du groupe d’annonces ou de la campagne. Selon le réseau publicitaire, vous pouvez créer des annonces textuelles étendues ou étendues ou des annonces textuelles standard.

* Publicités natives sur plusieurs appareils **audiences** pour [!DNL Microsoft Advertising] campagnes sur le [!DNL Microsoft Audience Network]. Vous disposez de deux options pour les annonces d’audience, en fonction des paramètres de la campagne :

  * Si la campagne est liée à une boutique de centre commercial, laissez le réseau publicitaire générer automatiquement des publicités basées sur les flux pour la campagne, à l’aide des informations sur les produits de la boutique. Vous n’avez pas besoin de créer des annonces basées sur des flux pour la campagne, mais vous devez créer des groupes publicitaires avec un ciblage utilisateur.

  * Si la campagne n’est pas liée à un compte de centre commercial, créez des annonces d’audience basées sur des images à l’aide du format d’annonce responsive, qui comprend plusieurs ressources de texte et d’image. Le réseau publicitaire rassemble les publicités en utilisant les combinaisons les plus efficaces d’éléments publicitaires et les affiche sur des sites comme [!DNL MSN], [!DNL Outlook.com] et [!DNL Microsoft Edge].

* **Annonces d’appel uniquement** pour les campagnes [!DNL Google Ads] sur le réseau de recherche. Les annonces d’appel uniquement sont des annonces textuelles comprenant un numéro de téléphone. Vous pouvez éventuellement utiliser un numéro de transfert [!DNL Google Ads] pour le compte rendu des performances d’appel avancé.

  >[!NOTE]
  >
  >Vous ne pouvez actuellement pas créer ni modifier des annonces réservées aux appels uniquement. Vous pouvez afficher, modifier le statut ou supprimer une annonce d’appel uniquement existante.

* **Annonces de recherche dynamique étendues** (désormais appelées uniquement « annonces de recherche dynamique » sur les réseaux publicitaires) pour [!DNL Google Ads] et [!DNL Microsoft Advertising] des groupes d’annonces de recherche dynamique dans les campagnes de recherche. Les annonces de recherche dynamique utilisent le contenu de votre site web plutôt que des mots-clés pour décider quand afficher vos annonces. Le réseau publicitaire génère dynamiquement le titre, choisit l’URL de la page de destination et l’URL d’affichage, et génère automatiquement l’URL finale.

  Pour plus d’informations sur les annonces de recherche dynamique, consultez les [[!DNL Google Ads] documentation](https://support.google.com/google-ads/answer/2471185) et [[!DNL Microsoft Advertising] documentation](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **Annonces multimédias** pour les campagnes de recherche [!DNL Microsoft Advertising]. Les annonces multimédias sont des annonces à grandes images qui s’affichent à des positions bien visibles sur la ligne principale et la barre latérale, et une seule annonce multimédia s’affiche par page. Ils peuvent inclure plusieurs ressources de texte et d’image, telles que des annonces responsive, et le réseau publicitaire assemble les annonces à l’aide des combinaisons d’éléments publicitaires les plus efficaces. Les annonces multimédias ne remplacent pas vos emplacements d’annonces publicitaires textuelles.

* Lignes de promotion pour **[!DNL Microsoft Advertising]annonces de produits (achats)** sur le réseau d’achats. Les annonces d’achats utilisent des produits dans votre flux de produits [!DNL Microsoft Merchant Center] existant, plutôt que des mots-clés, pour décider comment et où afficher vos annonces. Les URL de la copie de l’annonce publicitaire et de la page de destination sont générées automatiquement à partir des informations sur votre produit dans le flux. Vous pouvez toutefois configurer des lignes de promotion à inclure pour le groupe publicitaire.

  Pour plus d’informations sur les publicités de produit, consultez la [documentation Microsoft Advertising](https://help.ads.microsoft.com/#apex/3/en/51082).

* **Annonces de recherche réactives** pour les campagnes [!DNL Google Ads] et [!DNL Microsoft Advertising] sur le réseau de recherche. Le réseau publicitaire assemble dynamiquement des annonces de recherches réactives textuelles à partir d’un ensemble de titres et de descriptions d’annonces, favorisant des combinaisons qui fonctionnent bien ensemble. La publicité comprend jusqu’à trois titres, deux descriptions et une URL personnalisable à partir de l’URL de base et des champs facultatifs path1 et path2 . Vous pouvez éventuellement épingler les titres et descriptions des annonces à des postes spécifiques.

  >[!NOTE]
  >
  >[!DNL Google Ads] ne fournit pas de données en dehors de ses éditeurs natifs sur les combinaisons de texte affichées sous forme de publicités. Pour plus d’informations sur les rapports pour chaque combinaison de texte, consultez la documentation sur les [Google Ads ](https://support.google.com/google-ads/answer/7684791).

### Données de performances au niveau des annonces

Les données au niveau des annonces sont disponibles pour la plupart des types d’annonces.

Cependant, il n’est pas disponible pour [!DNL Google Ads] publicité de recherche dynamique (DSA), les campagnes Performance Max, Achats intelligents et [!DNL YouTube]. Attendez-vous à des incohérences entre le nombre total de données au niveau des annonces pour une campagne et le nombre total de données pour la campagne.

| Réseau publicitaire/Campagne/Type d’annonce | Disponibilité des données |
|---|---|
| [!DNL Google Ads] de la publicité de recherche dynamique (DSA) | Campagne, groupe publicitaire |
| Performances [!DNL Google Ads] max | Campagne |
| [!DNL Google Ads], achats intelligents | Campagne, groupe publicitaire |
| [!DNL Google Ads] [!DNL YouTube] | Campagne, groupe publicitaire |

## Création d’une publicité {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* Vous n’avez pas besoin de créer des annonces de produits pour les campagnes d’achat ; le réseau publicitaire les crée automatiquement. Toutefois, pour les campagnes d’achat [!DNL Microsoft Advertising], vous pouvez éventuellement définir des lignes de promotion à inclure dans les publicités.
>* Vous ne pouvez pas créer d’annonces [!DNL Google Ads] pour les appels uniquement.

>[!TIP]
>
>Pour créer un grand nombre d’annonces à la fois, utilisez [feuilles d’envoi groupé de campagne](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md).

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Cliquez sur **[!UICONTROL Create Ads]**.

1. À l’étape **[!UICONTROL Basic Settings]**, sélectionnez le réseau, le compte, la campagne, le groupe publicitaire et le type d’annonce.

   Pour plus d’informations sur les types d’annonces disponibles, voir « [Types d’annonces disponibles](#ad-types) ».

1. Spécifiez les paramètres restants pour une [annonce de texte Baidu](ad-settings-baidu-text.md), une [annonce de recherche dynamique étendue Google Ads](ad-settings-google-dsa.md) (appelée simplement « annonce de recherche dynamique » dans Google Ads), une [annonce de recherche réactive Google Ads](ad-settings-google-rsa.md), une [annonce de recherche dynamique étendue Microsoft Advertising](ad-settings-microsoft-dsa.md), une [annonce multimédia Microsoft Advertising](ad-settings-microsoft-multimedia.md), une [annonce de produit Microsoft Advertising Microsoft](ad-settings-microsoft-product.md), une [annonce responsive Advertising (audience)](ad-settings-microsoft-responsive.md), une [annonce de recherche réactive Microsoft](ad-settings-microsoft-rsa.md) ou des paramètres [annonce de texte Yandex](ad-settings-yandex-text.md).

   >[!NOTE]
   >
   >(Campagnes avec suivi des conversions Adobe Advertising) Si le compte ou les paramètres de campagne spécifient le suivi uniquement au niveau du mot-clé, alors Search, Social et Commerce ne génèrent pas de suivi pour les publicités.

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Si nécessaire, cliquez sur le **[!UICONTROL Edit]** ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") et modifiez les paramètres de l’annonce publicitaire.

1. Cliquez sur **[!UICONTROL Create]**.

1. <!-- Add link to where to generate this once available to users-->(Achats d’annonces dans des campagnes avec suivi des conversions Adobe Advertising ; facultatif) Pour effectuer le suivi des clics sur l’annonce, ajoutez manuellement une URL de suivi aux paramètres du compte, de la campagne ou du groupe de produits.

## Renommer une publicité {#ad-rename}

Renommez rapidement une publicité sans ouvrir les paramètres complets de la publicité.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Placez le curseur sur la ligne d’annonce et cliquez sur **[!UICONTROL ...]>[!UICONTROL Rename]**.

1. Modifiez le nom, puis cliquez sur **[!UICONTROL Apply]**.

## Modifier les paramètres de l’annonce publicitaire {#ad-edit}

>[!NOTE]
>
>* Les types d’annonces suivants sont *modifiables*, ce qui signifie que vous pouvez modifier la copie ou l’image de l’annonce et conserver le même ID d’annonce : tous les types d’annonces [!DNL Google Ads], à l’exception des annonces de recherche dynamique, et [!DNL Microsoft Advertising] annonces au format texte développé.
>* Toutes les autres publicités prises en charge sont *non modifiables*, ce qui signifie que la modification de la copie ou de l’image de la publicité supprime la publicité existante et en crée une nouvelle. Les performances de la nouvelle publicité peuvent être instables pendant quelques semaines, pendant que Search, Social et Commerce collecte suffisamment de données pour l’optimisation.
>* Vous ne pouvez pas modifier le contenu d’une publicité de produit, à l’exception de la ligne de promotion pour les publicités de produit [!DNL Microsoft Advertising]. Vous pouvez toutefois suspendre ou supprimer une publicité.
>* Vous ne pouvez pas modifier [!DNL Google Ads] publicités réservées aux appels uniquement. Vous pouvez toutefois en suspendre ou en supprimer un.
>* Vous ne pouvez modifier qu’une seule publicité à la fois.

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Cochez la case en regard de la publicité.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

1. Modifiez les paramètres restants d’une [annonce de texte Baidu](ad-settings-baidu-text.md), d’une [annonce de recherche dynamique étendue Google Ads](ad-settings-google-dsa.md) (désormais appelée uniquement « annonce de recherche dynamique » dans Google Ads), d’une [annonce de recherche réactive Google Ads](ad-settings-google-rsa.md), d’une [annonce de recherche dynamique étendue Microsoft Advertising](ad-settings-microsoft-dsa.md), d’une [annonce multimédia Microsoft Advertising](ad-settings-microsoft-multimedia.md), d’une [annonce de produit Microsoft Microsoft Advertising Microsoft responsive (audience)](ad-settings-microsoft-responsive.md), d’une [annonce de recherche réactive Advertising Advertising](ad-settings-microsoft-rsa.md) ou des paramètres [](ad-settings-yandex-text.md) annonce de texte Yandex](ad-settings-microsoft-product.md).[

1. Cliquez sur **[!UICONTROL Review and Save]**.

1. Si nécessaire, cliquez sur le **[!UICONTROL Edit]** ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier") et modifiez les paramètres de l’annonce publicitaire.

1. Cliquez sur **[!UICONTROL Update]**.

## Modifier le statut d’une publicité {#ad-status}

Modifiez rapidement le statut d’une publicité sans ouvrir les paramètres de publicité complets.

Vous pouvez suspendre toute publicité active sur un réseau publicitaire pris en charge afin de désactiver les enchères sur celui-ci. Vous pouvez ensuite reprendre les enchères en redéfinissant leur statut sur Actif.

Vous pouvez également supprimer toute publicité active ou en pause. Les publicités supprimées sont supprimées du réseau publicitaire. Ils sont toujours visibles lorsque vous les incluez dans le filtre de données, mais vous ne pouvez pas les modifier.

### Activer ou mettre en pause une publicité

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Cochez la case de la ligne d’annonce.

1. Dans la barre d’outils des actions en bloc, modifiez le statut :

   * Pour activer une publicité en pause, cliquez sur **[!UICONTROL Activate]**.

   * Pour mettre en pause une publicité active, cliquez sur **[!UICONTROL Pause]**.

### Suppression d’une publicité

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Cochez la case de la ligne d’annonce.

1. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## Gérer les rapports de vue de données à partir de la vue [!UICONTROL Ads] {#ad-reports}

Générez un rapport qui inclut les lignes de données pour une ou plusieurs publicités dans la vue [!UICONTROL Ads], puis téléchargez le rapport sous la forme d’un fichier de feuille de calcul Excel Microsoft (format XLXS). Le rapport inclut toutes les colonnes visibles dans la vue.

Vous pouvez supprimer n’importe quel rapport généré.

Consultez également les sections « [ (interface utilisateur héritée) Télécharger des données à partir d’une vue de gestion de campagne »](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md) et « [ (interface utilisateur héritée) Supprimer un rapport de données de performances ou un fichier de feuille d’envoi groupé du menu [!UICONTROL Downloads] »](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)

### Générer un rapport avec les lignes de données filtrées

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Indiquez les publicités dont vous souhaitez télécharger les données :

   * Pour télécharger des données relatives à des annonces spécifiques, cochez les cases en regard des annonces.

   * Pour télécharger des données pour toutes les publicités, il n’est pas nécessaire de cocher des cases. Toutes les publicités sont incluses par défaut.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans les paramètres de [!UICONTROL Grid Reports], saisissez un nom de rapport unique, puis cliquez sur **[!UICONTROL Generate]**.

   Par défaut, le fichier est nommé « ad_YYYYMMDD_NNNN », où « NNNN » correspond au numéro de tâche séquentiel (par exemple, « ad_20250402_1326 »).

   Le fichier est ajouté à la liste de [!UICONTROL Recently Generated].

1. (Facultatif) Pour télécharger le fichier une fois l’opération terminée, cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Télécharger un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Télécharger](/help/search-social-commerce/assets/download.png "Télécharger") en regard du nom du fichier.

   Le fichier est téléchargé conformément à la procédure normale de votre navigateur.

### Supprimer un rapport terminé

1. Dans le menu principal, cliquez sur **[!UICONTROL Manage]>[!UICONTROL Ads]**.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![ Télécharger le rapport ](/help/search-social-commerce/assets/download.png " Télécharger le rapport ") **[!UICONTROL Reports]**.

1. Dans la liste [!UICONTROL Recently Generated] de la boîte de dialogue [!UICONTROL Grid Reports], cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer") en regard du nom du fichier.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] paramètres de publicité texte](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] paramètres d’annonce de recherche dynamique développés](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] paramètres des annonces de recherches réactives](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] paramètres d’annonce de recherche dynamique développés](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] paramètres de publicité multimédia](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] paramètres de publicité du produit](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] paramètres d’annonce responsive (audience)](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] paramètres des annonces de recherches réactives](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] paramètres de publicité texte](ad-settings-yandex-text.md)
