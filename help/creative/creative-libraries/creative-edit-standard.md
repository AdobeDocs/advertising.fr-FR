---
title: Modification de contenus publicitaires standard dans une bibliothèque de contenus publicitaires
description: Découvrez comment modifier les paramètres des contenus publicitaires standard (non dynamiques) dans une bibliothèque de contenus publicitaires.
feature: Creative Standard Creatives
exl-id: 333ab2ea-293a-44e2-89e7-06782578318f
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# Modification de contenus publicitaires standard dans une bibliothèque de contenus publicitaires

*Version bêta fermée*

Vous pouvez modifier certains paramètres pour chaque type de contenu créatif standard. Vous pouvez modifier plusieurs contenus publicitaires<!-- or creative variations --> du même type (HTML simple avec une seule landing page, HTML5 statique avec plusieurs landing pages, HTML5 flexible, image ou tiers<!-- , or dynamic -->) uniquement.

Pour les créatifs HTML5 flexibles et HTML5 statiques, vous pouvez charger un nouveau fichier modèle avec une disposition différente, mais le même ensemble de noms d’attributs. Pour les contenus publicitaires HTML5 simples, vous pouvez modifier n’importe quel attribut ou ajouter des images en chargeant un nouveau modèle avec les nouveaux attributs ou images. Dans tous les cas, le modèle doit être un fichier local au format ZIP d’une taille maximale de 2 Mo.

Lorsque vous modifiez un contenu créatif inclus dans une offre groupée<!-- or creative variation --> vos modifications sont automatiquement appliquées à toutes les expériences qui incluent l’offre groupée, sauf que les pages de destination et URL de suivi personnalisées spécifiées au niveau de l’expérience restent applicables à l’offre groupée associée à cette expérience.

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des bibliothèques spécifiques.

1. Cliquez sur le nom de la bibliothèque.

1. Dans l’onglet **[!UICONTROL Creatives]** > **[!UICONTROL Standard Ads]** , sélectionnez les contenus publicitaires :

   * (Facultatif) [Personnalisez la vue](/help/creative/introduction/customize-data-views.md) pour inclure des contenus publicitaires spécifiques.

   * Pour modifier un élément créatif unique :

      * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom du contenu créatif, puis cliquez sur **[!UICONTROL Edit]**.

      * Dans la vue Tableau, placez le curseur sur la ligne et cliquez sur **[!UICONTROL Edit]**.

   * Pour modifier un ou plusieurs contenus publicitaires, cochez la case correspondant à chacun des contenus publicitaires que vous souhaitez modifier. Dans la barre d’outils des actions en bloc, cliquez sur **[!UICONTROL Edit]**.

     Pour sélectionner toutes les lignes, cochez la case globale dans le coin supérieur gauche.

1. Modifiez les [paramètres de création d’image](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image), [paramètres de création HTML5](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5), [paramètres de création HTML5 flexibles](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) ou [paramètres de création tiers](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party). <!-- , or [dynamic creative settings](/help/creative/creative-libraries/creative-settings-dynamic.md) -->

   Lorsque vous modifiez plusieurs contenus publicitaires en même temps :

   * Vous pouvez modifier les paramètres de chaque élément créatif en même temps ou individuellement. Par défaut, tous les contenus publicitaires sélectionnés sont sélectionnés et les paramètres que vous spécifiez s’appliquent à tous les contenus publicitaires sélectionnés. Pour modifier les paramètres de contenus publicitaires spécifiques, désélectionnez chaque contenu publicitaire inapplicable avant de modifier les champs ; répétez l’opération pour d’autres contenus publicitaires si nécessaire.

   * Certains paramètres sont appliqués à tous les contenus publicitaires sélectionnés.

   >[!NOTE]
   >
   >* (Contenus publicitaires HTML5 flexibles uniquement) Vous ne pouvez modifier les attributs que pour les contenus publicitaires uniques.<!-- May never be implemented: Also, when you update the template for a parent creative with child variations, the variations are updated with any changes to the template layout, but the attribute values for the variation aren't changed. -->

<!-- Not there as of 1/16/25. If we do add it, verify the applicable ad types:   
1. (Flexible HTML5 [or third-party should be possible, but not so] creatives; optional) Once you've made your changes, click ![]() to preview the new creative. 
-->

1. Cliquez sur **Enregistrer**.

<!-- Not there as of 1/16/25. If we do add it, add back in:
1. (Flexible HTML5 or third-party creatives; optional) Regenerate the thumbnail within the table view or cards view if the change isn't visible immediately.
-->

>[!MORELIKETHIS]
>
>* [Ajouter des contenus publicitaires standard à une bibliothèque de contenus publicitaires](creative-add-standard.md)
>* [Paramètres de création standard](/help/creative/creative-libraries/creative-settings-standard.md)
>* [Prévisualisation d’une création](/help/creative/creative-libraries/creative-preview.md)
