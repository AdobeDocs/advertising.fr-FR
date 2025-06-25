---
title: Gestion des modèles de publicité pour les flux d’inventaire
description: Découvrez la gestion des modèles d’annonces publicitaires grâce auxquels vos données d’inventaire peuvent être traitées pour gérer la structure du compte et diffuser des annonces dynamiques.
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Gestion des modèles de publicité pour les flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Avant ou après le chargement des données, vous pouvez créer des modèles d’annonce spécifiques au moteur de recherche grâce auxquels vos données peuvent être traitées. Vous pouvez créer des modèles pour les annonces textuelles et les annonces textuelles développées/étendues, les annonces [!DNL Google Ads] et [!DNL Microsoft Advertising] de recherches réactives, ainsi que pour les annonces d’achats [!DNL Google Ads] et [!DNL Microsoft Advertising].

Vous pouvez associer chaque modèle à un fichier de flux, un compte [!DNL Google Merchant Center] ou un compte [!DNL Microsoft Merchant Center], et vous pouvez associer plusieurs modèles au même fichier de flux ou compte. Un modèle de publicité peut inclure des variables qui sont remplacées par des colonnes de données réelles d’un fichier chargé ou d’un compte. Dans la plupart des cas, les variables peuvent également inclure [un groupe de modificateurs](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) que vous configurez dans Search, Social et Commerce pour créer plusieurs annonces, mots-clés, campagnes ou groupes d’annonces pour chaque ligne applicable dans le fichier de données. Les options de modèle vous permettent de créer une nouvelle structure de compte (campagnes, groupes publicitaires, mots-clés) pour les publicités ou de mapper les publicités à la structure de compte existante.

Outre la création de modèles à partir de zéro, vous avez la possibilité de créer des modèles en clonant des modèles existants et en les modifiant.

Une fois que vous avez créé un modèle et que vous l’avez associé à un fichier de flux de données ou à un compte de centre commercial, vous pouvez propager les données du fichier à travers le modèle afin de créer des données de campagne et une structure de compte, en créant éventuellement un fichier de feuille d’envoi groupé à réviser ou à publier immédiatement sur le réseau publicitaire.

Tout modèle peut être activé, mis en pause ou supprimé. Les données de flux ne peuvent être automatiquement propagées que par le biais de modèles actifs. Cependant, vous pouvez propager manuellement les données par le biais d’un modèle en pause.

## Créer, cloner ou modifier un modèle de flux

Créez des modèles distincts pour les annonces textuelles et les annonces textuelles développées/étendues, les annonces de recherches réactives, les annonces d’achats [!DNL Google Ads] et les annonces d’achats [!DNL Microsoft Advertising].

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Effectuez l’une des opérations suivantes :

   * Pour créer entièrement un modèle, cliquez sur **[!UICONTROL Create/Clone]** dans la barre d’outils au-dessus du tableau de données, puis sélectionnez le réseau publicitaire applicable.

   * Pour cloner un modèle existant :

      1. Cochez la case en regard du modèle que vous souhaitez copier.

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create/Clone]**, puis sélectionnez le réseau publicitaire approprié.

   * (Pour modifier un modèle existant) En regard du nom du modèle, cliquez sur ![Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Afficher/modifier les paramètres").

1. Spécifiez les paramètres du [modèle d’annonce de texte](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] modèle d’annonce d’achat](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md) ou [[!DNL Microsoft Advertising] modèle d’annonce d’achat](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md) :

   1. En haut de la fenêtre des paramètres du modèle, indiquez le nom du modèle et le compte applicable.

      Lorsque vous clonez un modèle existant, renommez le nouveau modèle afin que les publicités créées à partir du nouveau modèle ne soient pas associées aux publicités créées à partir du modèle source.

   1. (Facultatif) Dans la colonne de gauche, indiquez le fichier de flux de produits ou le compte de centre commercial dont les données seront propagées à travers le modèle :

      * (Pour les fichiers de flux de produit) Pour sélectionner un fichier chargé précédemment, cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flèche vers le bas") et sélectionnez un fichier dans la liste des fichiers de flux disponibles. Pour charger un nouveau fichier, spécifiez-le en saisissant le chemin d’accès complet et le nom du fichier ou en cliquant sur **[!UICONTROL Browse]** pour localiser le fichier sur votre appareil ou réseau, puis cliquez sur **[!UICONTROL Upload]**.

      * (Pour un compte de centre commercial synchronisé) Sélectionnez le nom du compte.

      Les colonnes du fichier ou du compte sélectionné s’affichent.

   1. Dans l’onglet **[!UICONTROL Account Structure]** , spécifiez les paramètres de structure du compte.

   1. (Annonces de texte uniquement) Cliquez sur l’onglet **[!UICONTROL Keywords]** et spécifiez les paramètres de mot-clé.

   1. (Annonces de recherche de texte et responsive uniquement) Cliquez sur l’onglet **[!UICONTROL Ads]** et effectuez l’une des opérations suivantes :

      >[!NOTE]
      >
      >* Vous pouvez inclure jusqu’à quatre modèles de variation d’annonce publicitaire par modèle d’annonce publicitaire standard, cinq modèles de variation d’annonce publicitaire par modèle d’annonce publicitaire de texte développé/étendu et trois modèles de variation d’annonce publicitaire par modèle d’annonce publicitaire de recherche responsive.
      >* Chaque groupe d’annonces peut inclure jusqu’à trois annonces responsive sur le Réseau de Recherche activées.
      >* Vous ne pouvez pas modifier le texte standard et ses variations, et les modèles existants ne génèrent plus de texte standard.
      >* Si vous modifiez un modèle de variation publicitaire, les publicités existantes peuvent être supprimées et de nouvelles publicités peuvent être créées lorsque vous propagez des données dans le modèle, [en fonction du type de publicité et du réseau publicitaire](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * Pour ajouter une variation d’annonce publicitaire, procédez comme suit :

         1. Cliquez sur **[!UICONTROL Add Ad Variation]** pour créer une publicité texte, **[!UICONTROL Add ETA Variation]** pour créer une publicité texte développée/étendue ou **[!UICONTROL Add RSA Variation]** pour créer une publicité texte réactive.

            Une fois que vous avez spécifié le type d’annonce, vous ne pouvez créer que ce type d’annonce avec le modèle.

         1. Spécifiez les paramètres de l’annonce publicitaire.

            Pour les annonces de recherches réactives, vous pouvez inclure 3 à 15 titres et 2 à 4 descriptions.

         1. (Facultatif) Pour préremplir tous les autres champs de copie publicitaire avec du texte provenant des champs de copie publicitaire d’origine, cochez la case en regard de **[!UICONTROL Prefill]**.

         1. (Facultatif) Pour ajouter un autre ensemble de copies d’annonce à une annonce, qui peut être utilisé si l’une des lignes de la copie d’annonce d’origine dépasse la longueur maximale une fois que des paramètres dynamiques ont été remplacés par des données pendant la propagation, cliquez sur **[!UICONTROL Add Alternate]**, puis ajoutez les autres valeurs.

            >[!NOTE]
            >
            >* Si l’option [!UICONTROL Prefill] est sélectionnée, les champs secondaires sont préremplis avec les champs d’origine et vous pouvez les modifier si nécessaire.
            >* Seuls les champs de la copie publicitaire qui dépassent la longueur maximale sont remplacés par la valeur alternative. Par exemple, si seul un titre ou un titre d’origine est trop long, la variation publicitaire générée utilise le titre ou le titre secondaire et la ou les descriptions d’origine. Par conséquent, assurez-vous que la copie alternative de l’annonce publicitaire a du sens lorsqu’elle est combinée avec la copie originale de l’annonce.
            >* Si la copie de l’annonce originale répond aux exigences de longueur du moteur de recherche, la copie de l’annonce alternative est ignorée.
            >* Vous pouvez spécifier jusqu’à quatre alternatives pour chaque champ de copie publicitaire.

         * Pour modifier une variation d’annonce publicitaire, procédez comme suit :

            1. Modifiez les paramètres de la publicité.

               Pour les annonces de recherches réactives, vous pouvez inclure 3 à 15 titres et 2 à 4 descriptions.

            1. (Facultatif) Pour préremplir tous les autres champs de copie publicitaire avec du texte provenant des champs de copie publicitaire d’origine, cochez la case en regard de **[!UICONTROL Prefill]**.

            1. (Facultatif) Pour ajouter un autre ensemble de copies d’annonce à une annonce, qui peut être utilisé si l’une des lignes de la copie d’annonce d’origine dépasse la longueur maximale une fois que des paramètres dynamiques ont été remplacés par des données pendant la propagation, cliquez sur **[!UICONTROL Add Alternate]**, puis ajoutez les autres valeurs.

               >[!NOTE]
               >
               >* Si l’option [!UICONTROL Prefill] est sélectionnée, les champs secondaires sont préremplis avec les champs d’origine et vous pouvez les modifier si nécessaire.
               >* Seuls les champs de la copie publicitaire qui dépassent la longueur maximale sont remplacés par la valeur alternative. Par exemple, si seul un titre ou un titre d’origine est trop long, la variation publicitaire générée utilise le titre ou le titre secondaire et la ou les descriptions d’origine. Par conséquent, assurez-vous que la copie alternative de l’annonce publicitaire a du sens lorsqu’elle est combinée avec la copie originale de l’annonce.
               >* Si la copie de l’annonce originale répond aux exigences de longueur du moteur de recherche, la copie de l’annonce alternative est ignorée.
               >* Vous pouvez spécifier jusqu’à quatre alternatives pour chaque champ de copie publicitaire.

         * Pour supprimer une variation d’annonce, cliquez sur **[!UICONTROL Remove ETA Variation]** (pour les annonces textuelles développées/étendues) ou **[!UICONTROL Remove RSA Variation]** (pour les annonces de recherches réactives) en regard de la variation d’annonce, selon le cas.

   1. (Modèles d’achat uniquement) Cliquez sur l’onglet **[!UICONTROL Product Groups]**, puis spécifiez des informations sur les groupes de produits que vous souhaitez cibler.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Feed Filters]** , puis spécifiez les lignes du fichier de flux à propager.

   1. (Facultatif) Cliquez sur le **[!UICONTROL Label Classifications tab]**, puis spécifiez les valeurs de classification de libellés à affecter aux différents composants de campagne créés :

      1. Cochez la case en regard de **[!DNL \[Component\] Label Classifications]**.

      1. Pour chaque classification de libellé à affecter au composant, procédez comme suit :

         1. Cliquez sur **[!UICONTROL Add Label Classification]**.

         1. Sélectionnez la classification de libellés, puis sélectionnez une valeur existante ou saisissez une nouvelle valeur.

1. Enregistrez le modèle :

   * Pour simplement enregistrer le modèle, cliquez sur **[!UICONTROL Save]**, puis cliquez de nouveau sur **[!UICONTROL Save]**.

   * Pour enregistrer le modèle et propager le fichier de données spécifié à travers celui-ci, cliquez sur **[!UICONTROL Save]**, puis sur **[!UICONTROL Save & Propagate]**.

## Modifier le statut des modèles de flux

Vous pouvez activer n’importe quel modèle de flux de données en pause ou suspendre n’importe quel modèle de flux de données actif.

>[!NOTE]
>
>Vous pouvez propager manuellement les données par le biais d’un modèle en pause, mais les données ne sont pas automatiquement propagées par celui-ci.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Cochez la case en regard de chaque modèle dont vous souhaitez modifier le statut.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Change Status]**, puis sur **[!UICONTROL Activate]** ou **[!UICONTROL Pause]**.

## Supprimer les modèles de flux

1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour ouvrir l’onglet [!UICONTROL Templates] .

1. Cochez la case en regard de chaque modèle à supprimer.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [À propos de l’automatisation de la gestion des annonces à l’aide des flux d’inventaire](../inventory-feeds-about.md)
>* [Paramètres d’annonce de texte et de modèle d’annonce de recherche responsive](template-text-rsa.md)
>* [[!DNL Google Ads] paramètres du modèle d’annonce publicitaire](template-google-shopping.md)
>* [[!DNL Microsoft Advertising] paramètres du modèle d’annonce publicitaire](template-microsoft-shopping.md)
>* [Propager les données de flux par le biais de modèles](../feed-data-propagate.md)
