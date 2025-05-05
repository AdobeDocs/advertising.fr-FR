---
title: Prise en charge de l’activation des ID universels
description: Découvrez la prise en charge de l’importation de vos segments d’ID universels, de la création de segments personnalisés pour effectuer le suivi des identifiants universels et de la conversion d’autres identifiants d’utilisateur dans vos segments propriétaires en identifiants universels pour un ciblage sans cookie.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 202f4ae8e6633672b7af12937f0b35da5052f7fc
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# Prise en charge de l’activation des ID universels

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Fonctionnalité Beta*

DSP prend en charge les identifiants universels basés sur les personnes pour le ciblage sans cookie d’un seul appareil (et non multi-appareils) dans les formats numériques pris en charge par DSP.

* Vous pouvez envoyer manuellement votre [[!DNL LiveRamp] [!DNL RampIDs]] authentifié directement à DSP à l’aide du tableau de bord [!DNL LiveRamp] [!DNL Connect]. Voir &quot;[Importation manuelle de segments authentifiés à partir de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)&quot;.

* DSP pouvez ingérer vos segments propriétaires composés d’ID d’email haché créés dans votre plateforme de données client (CDP) et les convertir en [!DNL LiveRamp] [!DNL RampIDs] et [!DNL Unified ID 2.0 (UID2.0)] ID. Pour plus d’informations sur les plateformes de données client prises en charge, les fonctionnalités disponibles pour chaque type d’ID universel pris en charge et les workflows associés, voir &quot;[À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)&quot;.

* Vous pouvez créer des segments personnalisés qui effectuent le suivi des utilisateurs associés aux ID universels ID 5 qui sont exposés à des publicités provenant d’ordinateurs de bureau et d’appareils mobiles et qui visitent des pages web spécifiques. ID5 utilise un modèle probabiliste pour attribuer un ID dérivé de divers signaux de l’utilisateur et des signaux du navigateur. Pour obtenir des instructions, voir &quot;[Création et implémentation d’un segment personnalisé](/help/dsp/audiences/custom-segment-create.md)&quot;.

* Les segments tiers de certains fournisseurs peuvent inclure automatiquement des identifiants universels en plus des utilisateurs suivis par des cookies ou des identifiants d’appareil. Par exemple, les segments de [!DNL Eyeota] peuvent automatiquement inclure des identifiants ID5 et les segments de [!DNL Lotame] peuvent inclure des identifiants UID2.0. Les détails du segment incluent la taille de chaque type. Les frais d’utilisation habituels pour chaque segment, indiqués en regard du nom du segment, s’appliquent ; aucun frais supplémentaire n’est facturé pour les ID 5.

## Reporting par type d’ID universel

* **Rapports personnalisés :** Les données de coût, d’impression, de clic, de conversion et de fréquence par type d’identifiant universel sont disponibles dans les rapports personnalisés.

* **[!DNL Analytics]rapports :** les annonceurs ayant [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) implémenté toutes les étapes requises peuvent afficher les conversions d’affichage publicitaire par type d’identifiant universel dans [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Pour une attribution de conversion correcte, veillez à ce que les URL de clics publicitaires comprennent à la fois l’ [EF ID et l’ AMO ID](/help/integrations/analytics/ids.md).

* **Détails du segment :** Pour tous les types de segments, les détails du segment incluent la taille de l’audience par type d’identifiant universel et par type d’appareil suivi par des cookies ou des identifiants d’appareil.

## Comment cibler une audience d’ID universelle dans vos emplacements

>[!NOTE]
>
>Vous ne pouvez pas modifier les types d’ID ciblés dans un emplacement en direct. Si nécessaire, vous pouvez dupliquer un emplacement en direct et modifier les types d’ID ciblés dans le nouvel emplacement.

Dans un nouvel emplacement, planifié ou en pause, procédez comme suit :

1. Dans la section [!UICONTROL Geo-Targeting] , spécifiez les zones géographiques à cibler. Chaque partenaire d’ID universel permet le ciblage des utilisateurs uniquement dans des zones géographiques spécifiques, et seuls les types d’ID éligibles sont disponibles dans les paramètres [!UICONTROL Targeting].

1. Dans la section [!UICONTROL Audience Targeting] , procédez comme suit :

   1. Dans le paramètre [!UICONTROL Included Audiences] , sélectionnez le segment pour lequel les données utilisateur ont été converties en identifiants universels.

      Vous pouvez inclure d’autres segments si vous le souhaitez.

   1. Dans les paramètres [!UICONTROL Targeting] :

      1. Sélectionnez le type d’identifiant universel à cibler.

         Le paramètre inclut les options &quot;[!UICONTROL Legacy IDs]&quot; et &quot;[!UICONTROL Universal ID]&quot;, qui peuvent inclure les sous-options &quot;[!UICONTROL ID5]&quot;, &quot;[!UICONTROL RampID]&quot; et &quot;[!UICONTROL Unified ID2.0]&quot;. Les cibles géographiques sélectionnées déterminent les sous-options disponibles.

         Vous pouvez sélectionner à la fois &quot;[!UICONTROL Legacy IDs]&quot; et &quot;[!UICONTROL Universal ID]&quot;, mais vous ne pouvez sélectionner qu’un seul type d’ID universel par emplacement. Lorsque vous sélectionnez à la fois des ID hérités et des ID universels, la préférence d’offre est accordée aux ID universels.

      1. (Si nécessaire) Acceptez les conditions d’utilisation des identifiants universels.

         Avant de pouvoir convertir des données en un nouveau type d’ID, un utilisateur du compte DSP doit accepter les conditions d’utilisation. Les termes ne doivent être acceptés qu’une seule fois par type d’identifiant et par compte.

Voir &quot;[Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md)&quot;.

## Bonnes pratiques relatives aux tests et à la validation des données

Utilisez les bonnes pratiques suivantes pour les segments basés sur [!DNL RampID] et les segments basés sur l’ID5, pour lesquels la mesure Adobe Analytics est disponible.

* Environ 24 heures après l’activation d’un segment, vérifiez le nombre d’identifiants convertis pour le segment dans [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Si le nombre d’identifiants est inattendu, contactez votre équipe de compte d’Adobe.

  Voir &quot;[Écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances)&quot; pour plus d’informations sur la manière dont les comptes de segments peuvent varier.

* Ne modifiez pas vos packages et emplacements existants. Cependant, si vous n’avez pas de budget incrémentiel pour tester les identifiants universels, réduisez les budgets d’origine pour financer les tests.

* Copiez vos packages et emplacements d’origine, ajustez les budgets en fonction de la taille du test, modifiez les audiences pour utiliser des segments basés sur [!DNL RampID] (pour les utilisateurs authentifiés) ou des segments basés sur l’ID5 (pour les utilisateurs non authentifiés), et vérifiez que les nouveaux modules et emplacements dépensent l’intégralité de leur budget.

   * Pour comparer les performances des segments universels basés sur des identifiants aux performances des emplacements ciblant d’autres identifiants d’audience, tels que les cookies ou les identifiants de publicité mobile, créez une campagne avec un emplacement universel distinct basé sur des identifiants et un emplacement hérité basé sur des identifiants.

     Pour un test de reciblage complet, ciblez les RampID pour les utilisateurs authentifiés et les ID5 pour les utilisateurs non authentifiés.

     Obtenir les meilleures performances ne devrait pas être la principale comparaison. Déterminez plutôt les identifiants qui évoluent correctement, ce qui peut influencer votre optimisation et vos allocations budgétaires ultérieurement. L’objectif à long terme est de compenser les impressions perdues et le trafic du site lorsque les cookies sont obsolètes.

   * Pour comparer la portée totale du navigateur, ciblez les segments universels basés sur les identifiants et les segments hérités basés sur les identifiants au même emplacement. Utilisez les mêmes paramètres de campagne que le cas d’utilisation précédent, sauf que vous n’avez pas besoin de fractionner le budget de l’opération.

     La préférence d’offre est accordée aux identifiants universels, mais les identifiants hérités reçoivent des offres lorsque les identifiants universels ne sont pas disponibles. Veillez à comparer la portée dans différents navigateurs (notamment Chrome, Safari et Mozilla).

     >[!NOTE]
     >
     >La limitation de fréquence s’applique à un ID individuel. Lorsqu’un utilisateur possède plusieurs types d’ID, vous pouvez l’atteindre plus que prévu.

* N’oubliez pas que la portée des segments d’audience authentifiés est naturellement plus petite que celle des segments basés sur des cookies et que l’utilisation d’options de ciblage supplémentaires réduit votre portée. Soyez judicieux lorsque vous utilisez un ciblage granulaire, en particulier en associant plusieurs cibles à des instructions ET.

## Écarts de données entre les ID de courrier électronique et les ID universels {#universal-ids-data-variances}

### Niveaux d’écart acceptables

Le taux de traduction des adresses électroniques hachées vers les ID universels doit être supérieur à 90 % ; le taux de traduction de [!DNL RampIDs] en particulier doit être de 95 % si toutes les adresses électroniques hachées sont uniques. Par exemple, si vous envoyez 100 adresses électroniques hachées à partir de votre plateforme de données client, elles doivent être traduites vers au moins 95 [!DNL RampIDs] ou plus de 90 autres types d’identifiants universels. Un taux de traduction plus faible peut indiquer un problème. Voir &quot;[Causes de la variance] (#universal-ids-data-variances-causes&quot; pour obtenir des explications possibles.

Pour [!DNL RampIDs], contactez votre équipe de compte d’Adobe pour plus d’informations si les taux de traduction sont inférieurs à 70 %.

### Causes d’écart {#universal-ids-data-variances-causes}

* Tous les segments :

  Le nombre de segments par appareil utilise un modèle probabiliste, qui présente une variance d’erreur de +/- 5 %. Cela signifie qu’il peut surestimer ou sous-estimer le nombre d’audiences de 5 %.

* ID d’email haché traduits en [!DNL RampIDs] :

   * Lorsque plusieurs profils utilisent le même ID d’adresse électronique, le nombre de segments DSP peut être inférieur au nombre de profils dans votre plateforme de données client. Dans Adobe Photoshop, par exemple, vous pouvez créer un compte de société et un compte personnel à l’aide d’un seul ID de courrier électronique. Mais si les deux profils appartiennent à la même personne, alors les profils correspondent à un ID d&#39;email et correspondant à un [!DNL RampID].

   * Un [!DNL RampID] peut être mis à niveau vers une nouvelle valeur. Si [!DNL LiveRamp] ne reconnaît pas un ID d&#39;email ou ne peut pas le mapper à un [!DNL RampID] existant dans sa base de données, il affecte un nouvel [!DNL RampID] à l&#39;ID d&#39;email. À l’avenir, lorsqu’ils pourront mapper l’ID d’email à un autre [!DNL RampID] ou recueillir plus d’informations sur le même ID d’email, ils mettront à niveau [!DNL RampID] vers une nouvelle valeur. [!DNL LiveRamp] fait référence à cette action comme une mise à niveau d&#39;un [!DNL RampID] &quot;dérivé&quot; vers un [!DNL RampID] &quot;conservé&quot;. Cependant, DSP n’obtient pas de mappages entre les [!DNL RampIDs] dérivés et gérés et ne peut donc pas supprimer la version précédente de l’RampID du segment DSP. Dans ce cas, le nombre de segments peut être supérieur au nombre de profils.

     Exemple : un utilisateur se connecte au site web [!DNL Adobe] et consulte la page Photoshop. Si [!DNL LiveRamp] ne contient aucune information existante sur l’ID d’email, il lui attribue un [!DNL RampID] dérivé, par exemple D123. Quinze jours plus tard, l’utilisateur consulte la même page, mais [!DNL LiveRamp] a mis à niveau [!DNL RampID] pendant ces 15 jours et a réaffecté [!DNL RampID] à M123. Même si le segment de la plateforme de données client &quot;Photoshop Enthusiast&quot; ne comporte qu’un seul e-mail pour l’utilisateur, le segment DSP comporte deux RampID : D123 et M123.

## Dépannage

Si vous ne voyez pas le nombre d’utilisateurs ou si les tailles de votre audience sont faibles, vérifiez les points suivants :

* Si vous utilisez [!DNL Flashtalking] ou [!DNL Google Campaign Manager 360] publicités, assurez-vous que les URL de clics publicitaires de vos publicités sont ajoutées avec les macros correctes. Voir les macros pour les [[!DNL Flashtalking] publicités](/help/integrations/analytics/macros-flashtalking.md) et les [[!DNL Google Campaign Manager 360] publicités](/help/integrations/analytics/macros-google-campaign-manager.md).

* Assurez-vous que le code approprié et universel propre au partenaire d’ID est implémenté sur votre site web pour faire correspondre les événements sur site et les expositions publicitaires. Contactez votre représentant [!DNL LiveRamp] ou [!DNL ID5] si nécessaire.

* (Pour les [!DNL RampIDs] et [!DNL UID 2.0] ID) Assurez-vous que votre [source de données DSP est configurée correctement](/help/dsp/audiences/sources/source-manage.md#source-settings) et que le nombre d’utilisateurs est renseigné pour les segments d’audience générés.

* Si votre portée est inférieure à ce que vous attendez, vérifiez que la logique du segment d’audience n’est pas trop granulaire.

* Assurez-vous que vos paramètres de campagne, de package et de placement sont corrects.<!-- wording-->

Si vous ne parvenez pas à résoudre le problème, contactez votre équipe de compte d’Adobe.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universels](/help/dsp/audiences/sources/source-manage.md)
>* [Créer et implémenter un segment personnalisé](/help/dsp/audiences/custom-segment-create.md)
>* [ Importation manuelle de segments authentifiés à partir de  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [À propos de la gestion de l’audience](/help/dsp/audiences/audience-about.md)
>* [Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md)
