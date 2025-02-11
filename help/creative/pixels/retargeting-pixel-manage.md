---
title: Gestion des pixels de reciblage
description: Découvrez comment créer et implémenter des pixels de reciblage à utiliser comme cibles pour les expériences publicitaires.
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: 147f47fcdc504fba67a6894edaa9249662131e05
workflow-type: tm+mt
source-wordcount: '936'
ht-degree: 0%

---

# Gestion des pixels de reciblage

*Version bêta fermée*

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

Vous pouvez créer un pixel de reciblage pour identifier les visiteurs sur les pages de destination ou de conversion d’un annonceur à l’aide de cookies utilisateur ou d’identifiants universels et pour capturer des attributs spécifiques suivis par les pages pour ces visiteurs. Le pixel suit l’événement le plus récent que le visiteur a effectué sur la page. Une fois le pixel créé, vous pouvez générer une balise de pixel à insérer dans les pages web appropriées pour commencer à suivre les visiteurs.<!-- Note to self: surfer id=cookie or universal ID -->

Vous pouvez ensuite utiliser le pixel comme cible pour toute création dans une expérience publicitaire afin d’afficher les annonces uniquement aux utilisateurs avec des attributs spécifiés qui ont précédemment visité les pages web associées au pixel. Par exemple, vous pouvez cibler les visiteurs et visiteuses qui regardent des chaussures rouges en taille 10, si les pages web effectuent le suivi de ces valeurs d’attribut.<!-- better example? Make sure they match attribute examples below -->

Les profils de reciblage sont stockés pendant 180 jours.

Exemple de pixel :

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative] ne prend actuellement en charge les identifiants universels que pour Advertising DSP. Une version ultérieure prendra en charge les identifiants universels des DSP tiers.<!-- Clarify this and reword as needed -->
>* Vous pouvez également utiliser vos audiences propriétaires de Adobe Audience Manager et Adobe Analytics en tant que [ cibles créatives pour vos expériences](/help/creative/experiences/experience-settings-targeting.md).
>* Lorsque vous utilisez une expérience en tant qu&#39;annonce dans un emplacement Advertising DSP, vous pouvez cibler l&#39;emplacement sur toutes les audiences disponibles dans DSP. Vous pouvez également [créer des balises de segment d’audience personnalisées](/help/dsp/audiences/custom-segment-create.md) pour suivre tous les visiteurs vers des pages de destination spécifiques, puis utiliser ces segments comme cibles créatives pour un emplacement.
>* Les visiteurs et visiteuses de site web qui se sont désinscrits du suivi pour le ciblage publicitaire ne reçoivent pas d’annonces avec du contenu créatif personnalisé basé sur un segment d’audience ou un profil de reciblage.

## Créer un pixel de reciblage

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Creative]**, puis sélectionnez > **[!UICONTROL Retargeting Pixel]**.

1. Spécifiez les [paramètres de pixel de reciblage](#retargeting-pixel-settings).

1. Cliquez sur **[!UICONTROL Save]**.

1. [Générez la balise pixel](#retargeting-pixel-generate) à fournir à l’annonceur ou au contact du site web.

   La balise de pixel de reciblage doit être la dernière action sur la page.<!-- verify here and below -->

   Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé de celui-ci.

## Modification d’un pixel de reciblage

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Placez le curseur sur le nom du pixel et cliquez sur **[!UICONTROL Edit]**.

1. Modifiez le [paramètres des pixels de reciblage](#retargeting-pixel-settings).

1. Cliquez sur **[!UICONTROL Save]**.

1. [Générez la balise pixel](#retargeting-pixel-generate) pour fournir à l’annonceur ou au contact du site web afin qu’ils puissent remplacer la balise d’origine.

   La balise de pixel de reciblage doit être la dernière action sur la page de destination.

   Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé de celui-ci.

## Générer une balise pour un pixel de reciblage {#retargeting-pixel-generate}

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Placez le curseur sur le nom du pixel et cliquez sur **[!UICONTROL Generate Tag]**.

1. Cliquez sur **[!UICONTROL Copy to Clipboard]** pour copier la balise dans le presse-papiers de votre ordinateur, à partir duquel vous pouvez coller le texte dans un fichier à enregistrer.

1. Dans la balise pixel, spécifiez une valeur pour chaque attribut dans les sections `<img src>` et `<script src>` en remplaçant chaque « `Insert <attribute>` » par une valeur. Spécifiez un ID de partenaire ID5 si la balise capture un ID universel.

   Si vous ajoutez manuellement des attributs supplémentaires, vous devez inclure le codage d’URL.

   Par exemple, si vous avez inclus les attributs « category », « color » et « size », ainsi que les identifiants universels d’ID5 de capture, la balise pixel inclura les paramètres suivants : `&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` et `&id5pid=--Insert ID5_PARTNER_ID--`. Pour cibler les utilisateurs qui sélectionnent des sandales rouges de taille 10, par exemple, vous devez définir les paramètres des balises image et script sur `&ut1=sandals&ut2=red&ut3=10`, ainsi que saisir l’ID5 du partenaire dans la balise script, tel que `&id5pid=0123456789`.

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. Fournissez la balise de pixel remplie à l’annonceur ou au contact du site web, ainsi qu’une liste des pages de destination pertinentes dans lesquelles l’insérer.

   La balise de pixel de reciblage doit être la dernière action sur la page de destination.

   Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé de celui-ci.

## Supprimer un pixel de reciblage

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**.

1. Placez le curseur sur le nom du pixel et cliquez sur **[!UICONTROL Delete]**.

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Paramètres des pixels de reciblage {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** Nom du pixel. **Remarque :** la balise pixel inclura l’identifiant du pixel (`pxId=<ID>`), et non le nom du pixel.

**[!UICONTROL Advertiser]:** (Lecture seule pour les pixels existants) Annonceur pour lequel le pixel est suivi.

**[!UICONTROL Attribute 1]:** attribut à inclure dans la balise pixel, tel que « SKU », « catégorie », « taille » ou d’autres attributs de la page ou du produit affiché sur la page. Spécifiez une valeur pour l’attribut dans la balise pixel avant de l’insérer dans les pages web appropriées.

Lorsque vous ciblez des expériences publicitaires sur des utilisateurs exposés au pixel, les paramètres de ciblage spécifient les valeurs d’attribut qui doivent être présentes pour afficher les éléments créatifs.

**[!UICONTROL Attribute 2]**, **[!UICONTROL Attribute 3]**, **[!UICONTROL Attribute 4]**, **[!UICONTROL Attribute 5]:** (facultatif) Attributs supplémentaires à inclure dans la balise pixel. Spécifiez une valeur pour chaque attribut supplémentaire dans la balise pixel avant de l’insérer dans les pages web appropriées.

Lorsque vous ciblez des expériences publicitaires sur des utilisateurs exposés au pixel, les paramètres de ciblage spécifient les valeurs d’attribut qui doivent être présentes pour afficher les éléments créatifs.

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** (fonctionnalité Beta ; nouveaux pixels uniquement ; facultatif) Types d’identifiants universels pour la balise de pixel à suivre :

* *[!UICONTROL ID5]:* La balise pixel suit les identifiants de [!DNL ID5]. Aucun frais n’est encouru pour les impressions diffusées aux identifiants universels.

* *[!UICONTROL Ramp ID]:* la balise de pixel suit le [!DNL Ramp IDs]. Aucun frais n’est encouru pour les impressions diffusées aux identifiants universels.

Pour utiliser cette fonctionnalité, vous ou un autre utilisateur du compte DSP devez accepter les conditions d’utilisation de l’ID universel une seule fois avant de pouvoir utiliser les ID universels pour un nouveau type d’ID. Pour les clients qui disposent de contrats de service géré, l’équipe chargée de votre compte Adobe obtiendra votre consentement et acceptera les conditions au nom de votre entreprise. Pour lire les termes, cliquez sur **[!UICONTROL Terms of Service]**. Pour accepter les conditions, faites défiler l’écran jusqu’au bas des conditions et cliquez sur **[!UICONTROL Accept]**.

>[!MORELIKETHIS]
>
>* [Paramètres d’expérience publicitaire ciblée](/help/creative/experiences/experience-settings-targeting.md)
>* [À propos des expériences publicitaires](/help/creative/experiences/experience-about.md)
