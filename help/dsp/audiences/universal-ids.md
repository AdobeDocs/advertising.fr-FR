---
title: Prise en charge de l’activation des identifiants universels
description: Découvrez la prise en charge de l’importation de vos segments d’ID universels, de la création de segments personnalisés pour effectuer le suivi des ID universels et de la conversion d’autres identifiants d’utilisateur de vos segments propriétaires en ID universels pour le ciblage sans cookie.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
TQID: https://experienceleague.adobe.com/A4fMoTW9gHD1i9Gdg1FALrBlz0XxMqhHOp9YO6kf3BQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: 1610
ht-degree: 0%

---

# Prise en charge de l’activation des identifiants universels

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

DSP prend en charge les identifiants universels basés sur les personnes pour le ciblage sans cookie sur un seul appareil (et non sur plusieurs appareils) à travers les formats numériques pris en charge par DSP.

* Vous pouvez envoyer manuellement vos [[!DNL LiveRamp] [!DNL RampIDs]] authentifiés directement à DSP à l&#39;aide du tableau de bord [!DNL LiveRamp] [!DNL Connect]. Voir « [ Importer manuellement des segments authentifiés depuis  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md) ».

* DSP peut ingérer vos segments propriétaires créés dans votre plateforme de données client (CDP) et les convertir en [!DNL RampIDs] [!DNL LiveRamp] et en ID de [!DNL Unified ID 2.0 (UID2.0)]. Pour plus d’informations sur les plateformes de données client et les types d’identifiants utilisateur pris en charge, les fonctionnalités disponibles pour chaque type d’identifiant universel pris en charge et les workflows associés, consultez la section « [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md) ».

* En Australie, les annonceurs peuvent importer des segments propriétaires contenant des identifiants universels [!DNL AdFixus] à l’aide d’une source d’audience [!UICONTROL AdFixus ID]. DSP ne convertit pas entre les ID [!DNL AdFixus] et d’autres types d’ID universels. Voir « [Importer des segments propriétaires depuis [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md) ».

* Vous pouvez créer des segments personnalisés qui effectuent le suivi des utilisateurs associés aux identifiants universels ID5 qui sont exposés aux publicités provenant des ordinateurs de bureau et des appareils mobiles et qui visitent des pages web spécifiques. ID5 utilise un modèle probabiliste pour attribuer un identifiant dérivé de divers signaux utilisateur et signaux navigateur. Pour obtenir des instructions, voir « [Créer et implémenter un segment personnalisé](/help/dsp/audiences/custom-segment-create.md) ».

* Les segments tiers de certains fournisseurs peuvent automatiquement inclure des identifiants universels en plus des utilisateurs suivis par des cookies ou des identifiants d’appareil. Par exemple, les segments provenant de l’adresse [!DNL Eyeota] peuvent automatiquement inclure des identifiants ID5, et les segments provenant de l’adresse [!DNL Lotame] peuvent inclure des identifiants UID2.0. Les détails du segment incluent la taille de chaque type. Les frais d’utilisation habituels pour chaque segment, qui sont indiqués en regard du nom du segment, s’appliquent ; aucun frais supplémentaire n’est facturé pour les ID5.

## Reporting par type d’identifiant universel

* **Rapports personnalisés :** les données de coût, d’impression, de clic, de conversion et de fréquence par type d’identifiant universel sont disponibles dans les rapports personnalisés.

* Rapports **[!DNL Analytics]:** annonceurs avec des [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) qui ont implémenté toutes les étapes requises peuvent afficher les conversions d’affichage publicitaire par type d’identifiant universel dans [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Pour une attribution de conversion appropriée, assurez-vous que les URL de clics pour vos publicités incluent à la fois l’ID [EF ID et l’ID AMO](/help/integrations/analytics/ids.md).

* **Détails du segment :** pour tous les types de segment, les détails de segment incluent la taille de l’audience par type d’identifiant universel et par type d’appareil suivi par des cookies ou des identifiants d’appareil.

## Comment cibler une audience d’ID universel dans vos emplacements

>[!NOTE]
>
>Vous ne pouvez pas modifier les types d’identifiants ciblés dans un emplacement actif. Si nécessaire, vous pouvez dupliquer un emplacement actif et modifier les types d’identifiants ciblés dans le nouvel emplacement.

Dans un nouvel emplacement, planifié ou en pause, procédez comme suit :

1. Dans la section [!UICONTROL Geo-Targeting] , indiquez les zones géographiques à cibler. Chaque partenaire d’ID universel permet le ciblage des utilisateurs et utilisatrices uniquement dans des zones géographiques spécifiques. Seuls les types d’ID éligibles sont disponibles dans les paramètres d’[!UICONTROL Targeting].

1. Dans la section [!UICONTROL Audience Targeting], procédez comme suit :

   1. Dans le paramètre [!UICONTROL Included Audiences] , sélectionnez le segment pour lequel les données utilisateur ont été converties en identifiants universels (tels que les identifiants [!DNL RampIDs] ou [!DNL UID2]) ou qui contient des identifiants [!DNL AdFixus] importés.

      Vous pouvez inclure des segments supplémentaires si vous le souhaitez.

   1. Dans les paramètres [!UICONTROL Targeting] :

      1. Sélectionnez le type d’identifiant universel à cibler.

         Le paramètre inclut les options « [!UICONTROL Legacy IDs] » et « [!UICONTROL Universal ID] », qui peuvent inclure les sous-options « [!UICONTROL AdFixus] », « [!UICONTROL ID5] », « [!UICONTROL RampID] » et « [!UICONTROL Unified ID2.0] ». Les cibles géographiques sélectionnées déterminent les sous-options disponibles.

         Vous pouvez sélectionner « [!UICONTROL Legacy IDs] » et « [!UICONTROL Universal ID] », mais vous ne pouvez sélectionner qu’un seul type d’ID universel par emplacement. Lorsque vous sélectionnez à la fois des identifiants hérités et universels, la préférence d’enchères est donnée aux identifiants universels.

      1. (Si nécessaire) Acceptez les conditions générales de l’accord de service pour l’utilisation des identifiants universels.

         Avant de pouvoir convertir des données en un nouveau type d’ID, un utilisateur disposant d’un compte DSP doit accepter les conditions d’utilisation. Les conditions ne doivent être acceptées qu&#39;une seule fois par type d&#39;identifiant, par compte.

Voir « [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md) ».

## Bonnes pratiques de test et de validation des données pour les segments basés sur [!DNL RampID] et les segments basés sur ID5

Utilisez les bonnes pratiques suivantes pour les segments basés sur [!DNL RampID] et les segments basés sur ID5, pour lesquels la mesure Adobe Analytics est disponible.

* Environ 24 heures après l’activation d’un segment, vérifiez le nombre d’identifiants convertis pour le segment dans [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Si le nombre d’identifiants est inattendu, contactez l’équipe chargée de votre compte Adobe.

  Pour plus d’informations sur les variations possibles du nombre de segments, reportez-vous à « [Variances de données entre les ID d’e-mail et les ID universels](#universal-ids-data-variances) ».

* Ne modifiez pas vos packages et emplacements existants. Cependant, si vous ne disposez pas d’un budget incrémentiel pour tester les identifiants universels, réduisez les budgets d’origine pour financer les tests.

* Copiez vos packages et emplacements d’origine, ajustez les budgets en fonction de la taille du test, modifiez les audiences pour utiliser des segments basés sur [!DNL RampID] (pour les utilisateurs authentifiés) ou des segments basés sur ID5 (pour les utilisateurs non authentifiés) et vérifiez que les nouveaux packages et emplacements dépensent l’intégralité de leurs budgets.

   * Pour comparer les performances des segments basés sur l’ID universel avec celles des emplacements ciblant d’autres identifiants d’audience, tels que les cookies ou les identifiants publicitaires mobiles, créez une campagne avec un emplacement basé sur l’ID universel distinct et un emplacement basé sur l’ID hérité.

     Pour un test de reciblage complet, ciblez les RampID pour les utilisateurs authentifiés et les ID5S pour les utilisateurs non authentifiés.

     Obtenir les meilleures performances ne devrait pas être la principale comparaison. Au lieu de cela, déterminez quels identifiants sont correctement mis à l’échelle, ce qui pourrait informer votre optimisation et vos allocations budgétaires ultérieurement. L’objectif à long terme est de rattraper les impressions perdues et le trafic sur le site lorsque les cookies sont obsolètes.

   * Pour comparer la portée totale du navigateur, ciblez les segments basés sur l’ID universel et les segments basés sur l’ID hérité dans le même emplacement. Utilisez les mêmes paramètres de campagne que le cas d’utilisation précédent, mais sans fractionner le budget de la campagne.

     La préférence d’enchères est donnée aux identifiants universels, mais les identifiants hérités reçoivent des enchères lorsque les identifiants universels ne sont pas disponibles. Veillez à comparer la portée dans différents navigateurs (y compris Chrome, Safari et Mozilla).

     >[!NOTE]
     >
     >Le capping de la fréquence s’applique à un identifiant individuel. Lorsqu’un utilisateur possède plusieurs types d’ID, vous pouvez atteindre cet utilisateur plus facilement que vous ne le pensiez.

* N’oubliez pas que la portée des segments d’audience authentifiés est naturellement plus petite que celle des segments basés sur des cookies et que l’utilisation d’options de ciblage supplémentaires réduit davantage votre portée. Soyez judicieux dans l’utilisation du ciblage granulaire, en particulier en joignant plusieurs cibles avec des instructions AND.

## Écarts de données entre les ID d’e-mail et les ID universels {#universal-ids-data-variances}

Cette section s’applique uniquement aux ID d’e-mail traduits en ID universels.

### Niveaux de variance acceptables

Le taux de traduction des adresses e-mail hachées en identifiants universels doit être supérieur à 90 %. Le taux de traduction pour les [!DNL RampIDs] en particulier doit être de 95 % si toutes les adresses e-mail hachées sont uniques. Par exemple, si vous envoyez 100 adresses e-mail hachées à partir de votre plateforme de données client, elles doivent être traduites en au moins 95 [!DNL RampIDs] ou plus de 90 autres types d’identifiants universels. Un taux de traduction inférieur peut indiquer un problème. Voir « [Causes des écarts]&#x200B;(#universal-ids-data-variances-causes) » pour d’autres explications.

Par [!DNL RampIDs], contactez votre équipe de compte Adobe pour plus d’informations si les taux de traduction sont inférieurs à 70 %.

### Causes des écarts {#universal-ids-data-variances-causes}

* Tous les segments :

  Le nombre de segments par appareil utilise un modèle probabiliste, qui présente une variance d’erreur de +/- 5 %. Cela signifie qu&#39;il peut surestimer ou sous-estimer le nombre de profils des audiences de 5 %.

* ID d’e-mail hachés traduits en [!DNL RampIDs] :

   * Lorsque plusieurs profils utilisent le même ID d’e-mail, le nombre de segments DSP peut être inférieur au nombre de profils dans votre plateforme de données client. Par exemple, dans Adobe Photoshop, vous pouvez créer un compte d’entreprise et un compte personnel à l’aide d’un seul ID d’e-mail. Cependant, si les deux profils appartiennent à la même personne, ils sont mappés à un ID d’e-mail et, de manière correspondante, à un [!DNL RampID].

   * Une [!DNL RampID] peut être mise à niveau vers une nouvelle valeur. Si [!DNL LiveRamp] ne reconnaît pas un ID d’e-mail ou ne peut pas le mapper à un [!DNL RampID] existant dans sa base de données, il attribue un nouveau [!DNL RampID] à l’ID d’e-mail. À l’avenir, lorsqu’ils pourront mapper l’ID d’e-mail à un autre [!DNL RampID] ou collecter davantage d’informations sur le même ID d’e-mail, ils mettront à niveau le [!DNL RampID] vers une nouvelle valeur. [!DNL LiveRamp] appelle cette action la mise à niveau d’un [!DNL RampID] « dérivé » vers un [!DNL RampID] « conservé ». Cependant, DSP n’obtient pas de mappages entre les [!DNL RampIDs] dérivés et conservés et ne peut donc pas supprimer la version précédente de l’ID de rampe du segment DSP. Dans ce cas, le nombre de segments peut être supérieur au nombre de profils.

     Exemple : un utilisateur se connecte au site web [!DNL Adobe] et visite la page Photoshop . Si [!DNL LiveRamp] ne dispose d’aucune information existante sur l’ID d’e-mail, alors ils lui attribuent un [!DNL RampID] dérivé, tel que D123. Quinze jours plus tard, l’utilisateur visite la même page, mais [!DNL LiveRamp] a mis à niveau le [!DNL RampID] au cours de ces 15 jours et a réaffecté le [!DNL RampID] au M123. Bien que le segment « Photoshop Enthusiast » de la plateforme de données client ne dispose que d’un seul ID d’e-mail pour l’utilisateur, le segment DSP comporte deux ID de rampe : D123 et M123.

## Dépannage

Si vous ne voyez pas de nombre d’utilisateurs ou d’utilisatrices, ou si la taille de votre audience est faible, vérifiez les points suivants :

* Si vous utilisez des annonces [!DNL Flashtalking] ou [!DNL Google Campaign Manager 360], assurez-vous que les URL de clics publicitaires de vos annonces sont accompagnées des macros appropriées. Voir les macros pour [[!DNL Flashtalking] annonces](/help/integrations/analytics/macros-flashtalking.md) et [[!DNL Google Campaign Manager 360] annonces](/help/integrations/analytics/macros-google-campaign-manager.md).

* (Pour les identifiants [!DNL RampIDs] et [!DNL UID 2.0]) Assurez-vous que le code correct et universel spécifique au partenaire ID est implémenté sur votre site web pour correspondre aux événements sur site et aux expositions publicitaires. Collaborez avec votre [!DNL LiveRamp] ou représentant [!DNL ID5], au besoin.

* (Pour les identifiants [!DNL RampIDs] et [!DNL UID 2.0]) Assurez-vous que la source de données [DSP est correctement configurée](/help/dsp/audiences/sources/source-manage.md#source-settings) et que le nombre d’utilisateurs est renseigné pour les segments d’audience générés.

* (Pour les identifiants de [!DNL AdFixus]) Vérifiez que la source de [!UICONTROL AdFixus ID] est correctement configurée et qu’[!DNL AdFixus] s’agit de segments en flux continu.

* Si votre portée est inférieure à ce que vous attendiez, vérifiez que la logique du segment d’audience n’est pas trop granulaire.

* Vérifiez que les paramètres de votre campagne, de votre package et de votre emplacement sont corrects.

Si vous ne parvenez pas à résoudre le problème, contactez l’équipe chargée de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](/help/dsp/audiences/sources/source-manage.md)
>* [Créer et implémenter un segment personnalisé](/help/dsp/audiences/custom-segment-create.md)
>* [Importer manuellement des segments authentifiés depuis  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Importer des segments propriétaires depuis [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
