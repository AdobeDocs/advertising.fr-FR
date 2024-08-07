---
title: Gestion des modèles d’annonces pour les flux d’inventaire
description: Découvrez la gestion des modèles d’annonces grâce auxquels vos données d’inventaire peuvent être traitées pour gérer la structure du compte et diffuser des publicités dynamiques.
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# Gestion des modèles d’annonces pour les flux d’inventaire

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] (actions de suppression uniquement) et [!DNL Yandex] comptes uniquement*

Avant ou après le chargement des données, vous pouvez créer des modèles d’annonces spécifiques au moteur de recherche par le biais desquels vos données peuvent être traitées. Vous pouvez créer des modèles pour les annonces textuelles et les annonces textuelles étendues, les [!DNL Google Ads] et les [!DNL Microsoft Advertising] annonces responsives de recherche, ainsi que pour les [!DNL Google Ads] et [!DNL Microsoft Advertising] annonces d&#39;achats.

Vous pouvez associer chaque modèle à un fichier de flux, un compte [!DNL Google Merchant Center] ou un compte [!DNL Microsoft Merchant Center], et vous pouvez associer plusieurs modèles au même fichier ou compte de flux. Un modèle d’annonce peut inclure des variables qui sont remplacées par des colonnes de données réelles provenant d’un fichier chargé ou d’un compte. Dans la plupart des cas, les variables peuvent également inclure [un groupe de modificateurs](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) que vous configurez dans Search, Social et Commerce pour créer plusieurs publicités, mots-clés, campagnes ou groupes d’annonces pour chaque ligne applicable du fichier de données. Les options de modèle vous permettent de créer une nouvelle structure de compte (campagnes, groupes publicitaires, mots-clés) pour les publicités ou de les mapper à la structure de compte existante.

En plus de créer de nouveaux modèles à partir de zéro, vous pouvez éventuellement créer de nouveaux modèles en clonant des modèles existants et en éditant des modèles existants.

Une fois que vous avez créé un modèle et que vous l’avez associé à un fichier de flux de données ou à un compte de centre commercial, vous pouvez propager les données du fichier par le biais du modèle afin de créer des données de campagne et une structure de compte, créant éventuellement un fichier de feuille d’envoi groupé à des fins de révision ou de publication immédiate sur le réseau publicitaire.

Tout modèle peut être activé, mis en pause ou supprimé. Les données de flux ne peuvent être propagées automatiquement que par le biais de modèles actifs. Vous pouvez toutefois propager manuellement les données par le biais d’un modèle suspendu.

## Créer, cloner ou modifier un modèle de flux

Créez des modèles distincts pour les annonces textuelles étendues/étendues, les annonces responsives sur le Réseau de Recherche, les [!DNL Google Ads] annonces d&#39;achats et les [!DNL Microsoft Advertising] annonces d&#39;achats.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

1. Effectuez l’une des opérations suivantes :

   * Pour créer entièrement un modèle, cliquez sur **[!UICONTROL Create/Clone]** dans la barre d’outils située au-dessus du tableau de données, puis sélectionnez le réseau publicitaire approprié.

   * Pour cloner un modèle existant :

      1. Cochez la case en regard du modèle que vous souhaitez copier.

      1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Create/Clone]**, puis sélectionnez le réseau publicitaire approprié.

   * (Pour modifier un modèle existant) En regard du nom du modèle, cliquez sur ![Afficher/modifier les paramètres](/help/search-social-commerce/assets/settings.png "Afficher/modifier les paramètres").

1. Spécifiez les paramètres pour le [modèle de publicité textuelle](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), le [[!DNL Google Ads] modèle de publicité d’achat](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md) ou le [[!DNL Microsoft Advertising] modèle de publicité d’achat](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md) :

   1. Dans la partie supérieure de la fenêtre des paramètres du modèle, indiquez le nom du modèle et le compte approprié.

      Lorsque vous clonez un modèle existant, renommez le nouveau modèle afin que les publicités créées à partir du nouveau modèle ne soient pas associées aux publicités créées à partir du modèle source.

   1. (Facultatif) Dans la colonne de gauche, indiquez le fichier de flux de produit ou le compte du centre commercial dont les données seront propagées par le biais du modèle :

      * (Pour les fichiers de flux de produit) Pour sélectionner un fichier précédemment téléchargé, cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-dropdown.png "Flèche vers le bas") et sélectionnez un fichier dans la liste des fichiers de flux disponibles. Pour charger un nouveau fichier, indiquez-le en saisissant le chemin d’accès complet et le nom de fichier ou en cliquant sur **[!UICONTROL Browse]** pour localiser le fichier sur votre appareil ou votre réseau, puis cliquez sur **[!UICONTROL Upload]**.

      * (Pour un compte de centre commercial synchronisé) Sélectionnez le nom du compte.

      Les colonnes du fichier ou du compte sélectionné s’affichent.

   1. Dans l’onglet **[!UICONTROL Account Structure]**, spécifiez les paramètres de structure du compte.

   1. (Publicités textuelles uniquement) Cliquez sur l’onglet **[!UICONTROL Keywords]** et spécifiez les paramètres des mots-clés.

   1. (Publicités de recherche de texte et réactives uniquement) Cliquez sur l’onglet **[!UICONTROL Ads]** et effectuez l’une des opérations suivantes :

      >[!NOTE]
      >
      >* Vous pouvez inclure jusqu’à quatre modèles de variation de publicité par modèle de publicité textuelle standard, cinq modèles de variation de publicité par modèle de publicité textuelle étendu/étendu et trois modèles de variation de publicité par modèle de publicité de recherche réactive.
      >* Chaque groupe d’annonces peut inclure jusqu’à trois annonces de recherche réactive activées.
      >* Vous ne pouvez pas modifier les variations de publicités textuelles standard existantes, et les modèles existants ne génèrent plus de publicités textuelles standard.
      >* Si vous modifiez un modèle de variation de publicité, les publicités existantes peuvent être supprimées et de nouvelles peuvent être créées lorsque vous propagez les données par le modèle, [ selon le type de publicité et le réseau publicitaire](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * Pour ajouter une variation publicitaire, procédez comme suit :

         1. Cliquez sur **[!UICONTROL Add Ad Variation]** pour créer une publicité textuelle, **[!UICONTROL Add ETA Variation]** pour créer une publicité textuelle étendue ou **[!UICONTROL Add RSA Variation]** pour créer une publicité textuelle réactive.

            Une fois que vous avez spécifié le type de publicité, vous pouvez créer uniquement ce type avec le modèle .

         1. Spécifiez les paramètres de publicité.

            Pour les annonces responsives sur le Réseau de Recherche, vous pouvez inclure 3 à 15 titres et 2 à 4 descriptions.

         1. (Facultatif) Pour préremplir tous les autres champs de copie de publicité avec le texte des champs de copie de publicité d’origine, cochez la case en regard de **[!UICONTROL Prefill]**.

         1. (Facultatif) Pour ajouter un autre ensemble de copies d’annonces à une publicité, qui peut être utilisé si l’une des lignes de la copie d’annonce d’origine dépasse la longueur maximale une fois que des paramètres dynamiques sont remplacés par des données lors de la propagation, cliquez sur **[!UICONTROL Add Alternate]**, puis ajoutez les valeurs alternatives.

            >[!NOTE]
            >
            >* Si l’option [!UICONTROL Prefill] est sélectionnée, les champs alternatifs sont préremplis avec les champs originaux et vous pouvez les modifier si nécessaire.
            >* Seuls les champs de copie de publicité qui dépassent la longueur maximale sont remplacés par la valeur alternative. Par exemple, si seul un titre ou un titre d’origine est trop long, la variation de publicité générée utilise le titre ou titre de remplacement et la ou les descriptions d’origine. Par conséquent, assurez-vous que l’autre copie de publicité est logique lorsqu’elle est combinée à la copie de publicité d’origine.
            >* Si la copie de publicité d’origine répond aux exigences de longueur du moteur de recherche, la copie de publicité alternative est ignorée.
            >* Vous pouvez spécifier jusqu’à quatre champs de remplacement pour chaque champ de copie de publicité.

         * Pour modifier une variation de publicité, procédez comme suit :

            1. Modifiez les paramètres de la publicité.

               Pour les annonces responsives sur le Réseau de Recherche, vous pouvez inclure 3 à 15 titres et 2 à 4 descriptions.

            1. (Facultatif) Pour préremplir tous les autres champs de copie de publicité avec le texte des champs de copie de publicité d’origine, cochez la case en regard de **[!UICONTROL Prefill]**.

            1. (Facultatif) Pour ajouter un autre ensemble de copies d’annonces à une publicité, qui peut être utilisé si l’une des lignes de la copie d’annonce d’origine dépasse la longueur maximale une fois que des paramètres dynamiques sont remplacés par des données lors de la propagation, cliquez sur **[!UICONTROL Add Alternate]**, puis ajoutez les valeurs alternatives.

               >[!NOTE]
               >
               >* Si l’option [!UICONTROL Prefill] est sélectionnée, les champs alternatifs sont préremplis avec les champs originaux et vous pouvez les modifier si nécessaire.
               >* Seuls les champs de copie de publicité qui dépassent la longueur maximale sont remplacés par la valeur alternative. Par exemple, si seul un titre ou un titre d’origine est trop long, la variation de publicité générée utilise le titre ou titre de remplacement et la ou les descriptions d’origine. Par conséquent, assurez-vous que l’autre copie de publicité est logique lorsqu’elle est combinée à la copie de publicité d’origine.
               >* Si la copie de publicité d’origine répond aux exigences de longueur du moteur de recherche, la copie de publicité alternative est ignorée.
               >* Vous pouvez spécifier jusqu’à quatre champs de remplacement pour chaque champ de copie de publicité.

         * Pour supprimer une variation de publicité, cliquez sur **[!UICONTROL Remove ETA Variation]** (pour les publicités textuelles étendues) ou **[!UICONTROL Remove RSA Variation]** (pour les publicités de recherche réactive) en regard de la variation de publicité, le cas échéant.

   1. (Modèles d’achat uniquement) Cliquez sur l’onglet **[!UICONTROL Product Groups]** , puis spécifiez des informations sur les groupes de produits que vous souhaitez cibler.

   1. (Facultatif) Cliquez sur l’onglet **[!UICONTROL Feed Filters]**, puis spécifiez les lignes du fichier de flux à propager.

   1. (Facultatif) Cliquez sur **[!UICONTROL Label Classifications tab]**, puis spécifiez les valeurs de classification d’étiquette à attribuer aux différents composants de campagne créés :

      1. Cochez la case en regard de **[!DNL \[Component\] Label Classifications]**.

      1. Pour chaque classification d’étiquette à affecter au composant, procédez comme suit :

         1. Cliquez sur **[!UICONTROL Add Label Classification]**.

         1. Sélectionnez la classification des étiquettes, puis sélectionnez une valeur existante ou saisissez une nouvelle valeur.

1. Enregistrez le modèle :

   * Pour simplement enregistrer le modèle, cliquez sur **[!UICONTROL Save]**, puis de nouveau sur **[!UICONTROL Save]**.

   * Pour enregistrer le modèle et propager le fichier de données spécifié par son intermédiaire, cliquez sur **[!UICONTROL Save]**, puis sur **[!UICONTROL Save & Propagate]**.

## Modifier l’état des modèles de flux

Vous pouvez activer n’importe quel modèle de flux de données suspendu ou suspendre tout modèle de flux de données actif.

>[!NOTE]
>
>Vous pouvez propager manuellement les données par le biais d’un modèle suspendu, mais les données ne sont pas propagées automatiquement par ce modèle.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

1. Cochez la case en regard de chaque modèle dont vous souhaitez modifier l’état.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Change Status]**, puis sur **[!UICONTROL Activate]** ou **[!UICONTROL Pause]**.

## Suppression de modèles de flux

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** pour accéder à l’onglet [!UICONTROL Templates].

1. Cochez la case en regard de chaque modèle à supprimer.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [À propos de l’automatisation de la gestion des publicités à l’aide de flux d’inventaire](../inventory-feeds-about.md)
>* [Paramètres de modèle de publicité textuelle et de recherche réactive](template-text-rsa.md)
>* [[!DNL Google Ads]  Paramètres du modèle d&#39;annonce d&#39;achat ](template-google-shopping.md)
>* [[!DNL Microsoft Advertising]  Paramètres du modèle d&#39;annonce d&#39;achat ](template-microsoft-shopping.md)
>* [Propager les données de flux par le biais de modèles](../feed-data-propagate.md)
