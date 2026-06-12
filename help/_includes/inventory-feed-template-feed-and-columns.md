---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---
# Texte et modèle - Flux et colonnes

**[!UICONTROL Feed & Columns]:** un [fichier de flux](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md) ou un compte commerçant associé au modèle, ainsi que les colonnes (en-têtes) du fichier ou du compte sélectionné :

* *[!UICONTROL Feed File]:* Chargez un fichier ou sélectionnez un fichier dans la liste des fichiers de flux disponibles.

* *[!UICONTROL Google Merchant Center]:* Sélectionnez un [compte [!DNL Google Merchant Center] synchronisé](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Search, Social et Commerce créent uniquement des groupes de produits ; [!DNL Google Ads] génère automatiquement les annonces d’achats pour les groupes de produits. Les colonnes personnalisées ne sont pas prises en charge.

* *[!UICONTROL Microsoft Merchant Center]:* (modèles d’achat [!DNL Microsoft Advertising] uniquement) Sélectionnez un [compte  [!DNL Microsoft Merchant Center]  synchronisé](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). Search, Social et Commerce créent uniquement des groupes de produits ; [!DNL Microsoft Advertising] génère automatiquement les annonces de produits pour les groupes de produits. Les colonnes personnalisées ne sont pas prises en charge.

L’association du modèle à un fichier de flux ou à un compte marchand est facultative jusqu’à ce que vous soyez prêt à créer des annonces à l’aide du modèle.

Lorsque vous insérez une colonne de flux dans un champ de modèle, la valeur insérée est indiquée comme `[field_name]`, où « field_name » est le nom du champ spécifié, pour indiquer que la valeur est une variable.

>[!NOTE]
>
>* Si vous modifiez le fichier de flux ou le compte d’un modèle existant, vous devrez peut-être ajuster les paramètres du modèle si le nouveau fichier contient différents en-têtes.
>* Si le fichier de flux ou le compte associé au modèle est supprimé ou désactivé, l’association est également supprimée. Vous devez sélectionner un nouveau fichier de flux avant de pouvoir créer d’autres annonces à l’aide du modèle. Si le nouveau fichier de flux ou compte n’inclut pas les mêmes en-têtes que le fichier d’origine, vous devrez peut-être ajuster les paramètres du modèle en conséquence.
