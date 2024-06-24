---
title: Prise en charge de l’activation des ID universels
description: Découvrez la prise en charge de l’importation de vos segments d’ID universels, de la création de segments personnalisés pour effectuer le suivi des identifiants universels et de la conversion d’autres identifiants d’utilisateur dans vos segments propriétaires en identifiants universels pour un ciblage sans cookie.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: db21fa1ed9daab9070fa1ce7740dd5dbaa0f3a2f
workflow-type: tm+mt
source-wordcount: '1392'
ht-degree: 0%

---

# Prise en charge de l’activation des ID universels

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Fonction bêta*

DSP prend en charge les identifiants universels basés sur les personnes pour le ciblage sans cookie d’un seul appareil (et non multi-appareils) dans les formats numériques pris en charge par DSP.

* Vous pouvez envoyer manuellement votre authentification [[!DNL LiveRamp] [!DNL RampIDs]] directement pour DSP à l’aide de la fonction [!DNL LiveRamp] [!DNL Connect] tableau de bord. Voir &quot;[Importation manuelle de segments authentifiés depuis [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).&quot;

* DSP peut ingérer vos segments propriétaires, composés d’ID de courrier électronique haché créés dans votre plateforme de données client (CDP) et les convertir en [!DNL LiveRamp] [!DNL RampIDs] et [!DNL Unified ID 2.0 (UID2.0)] ID. Pour plus d’informations sur les plateformes de données client prises en charge, les fonctionnalités disponibles pour chaque type d’ID universel pris en charge et les workflows associés, voir &quot;[À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md).&quot;

* Vous pouvez créer des segments personnalisés qui effectuent le suivi des utilisateurs associés aux ID universels ID 5 qui sont exposés à des publicités provenant d’ordinateurs de bureau et d’appareils mobiles et qui visitent des pages web spécifiques. ID5 utilise un modèle probabiliste pour attribuer un ID dérivé de divers signaux de l’utilisateur et des signaux du navigateur. Pour obtenir des instructions, voir &quot;[Création et implémentation d’un segment personnalisé](/help/dsp/audiences/custom-segment-create.md).&quot;

* Les segments tiers de certains fournisseurs peuvent inclure automatiquement des identifiants universels en plus des utilisateurs suivis par des cookies ou des identifiants d’appareil. Par exemple, les segments de [!DNL Eyeota] peuvent inclure automatiquement des ID5 et des segments provenant de [!DNL Lotame] peuvent inclure des UID2.0 ID. Les détails du segment incluent la taille de chaque type. Les frais d’utilisation habituels pour chaque segment, indiqués en regard du nom du segment, s’appliquent ; aucun frais supplémentaire n’est facturé pour les ID 5.

## Reporting par type d’ID universel

* **Rapports personnalisés :** Les données de coût, d’impression, de clic, de conversion et de fréquence par type d’identifiant universel sont disponibles dans les rapports personnalisés.

* **[!DNL Analytics]rapports :** Annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) qui ont mis en oeuvre toutes les étapes requises peuvent afficher les conversions d’affichage publicitaire par type d’ID universel dans [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Pour une attribution de conversion correcte, veillez à ce que les URL de clics publicitaires incluent les deux [Identifiant EF et AMO ID](/help/integrations/analytics/ids.md).

* **Détails du segment :** Pour tous les types de segments, les détails du segment incluent la taille de l’audience par type d’identifiant universel et par type d’appareil suivi par des cookies ou des identifiants d’appareil.

## Comment cibler une audience d’ID universelle dans vos emplacements

>[!NOTE]
>
>Vous ne pouvez pas modifier les types d’ID ciblés dans un emplacement en direct. Si nécessaire, vous pouvez dupliquer un emplacement en direct et modifier les types d’ID ciblés dans le nouvel emplacement.

Dans un nouvel emplacement, planifié ou en pause, procédez comme suit :

1. Dans le [!UICONTROL Geo-Targeting] , définissez les zones géographiques à cibler. Chaque partenaire d’ID universel permet un ciblage des utilisateurs uniquement dans des zones géographiques spécifiques, et seuls les types d’ID éligibles sont disponibles dans la variable [!UICONTROL Targeting] paramètres.

1. Dans le [!UICONTROL Audience Targeting] , procédez comme suit :

   1. Dans le [!UICONTROL Included Audiences] , sélectionnez le segment pour lequel les données utilisateur ont été converties en identifiants universels.

      Vous pouvez inclure d’autres segments si vous le souhaitez.

   1. Dans le [!UICONTROL Targeting] settings :

      1. Sélectionnez le type d’identifiant universel à cibler.

         Le paramètre comprend les options &quot;[!UICONTROL Legacy IDs]&quot; et &quot;[!UICONTROL Universal ID],&quot; qui peut inclure les sous-options &quot;[!UICONTROL ID5],&quot;[!UICONTROL RampID],&quot; et &quot;[!UICONTROL Unified ID2.0].&quot; Les cibles géographiques sélectionnées déterminent les sous-options disponibles.

         Vous pouvez sélectionner les deux[!UICONTROL Legacy IDs]&quot; et &quot;[!UICONTROL Universal ID],&quot; mais vous ne pouvez sélectionner qu’un seul type d’ID universel par emplacement. Lorsque vous sélectionnez à la fois des ID hérités et des ID universels, la préférence d’offre est accordée aux ID universels.

      1. (Si nécessaire) Acceptez les conditions d’utilisation des identifiants universels.

         Avant de pouvoir convertir des données en un nouveau type d’ID, un utilisateur du compte DSP doit accepter les conditions d’utilisation. Les termes ne doivent être acceptés qu’une seule fois par type d’identifiant et par compte.

Voir &quot;[Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).&quot;

## Bonnes pratiques relatives aux tests et à la validation des données

Suivez les bonnes pratiques suivantes pour [!DNL RampID]Segments basés sur ID5 et segments basés sur ID, pour lesquels la mesure Adobe Analytics est disponible.

* Environ 24 heures après l’activation d’un segment, vérifiez le nombre d’identifiants convertis pour le segment dans [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Si le nombre d’identifiants est inattendu, contactez votre équipe de compte d’Adobe.

  Voir &quot;[Causes des écarts de données entre les ID de courrier électronique et les ID universels](#universal-ids-data-variances)&quot; pour plus d’informations sur la manière dont le nombre de segments peut varier.

* Ne modifiez pas vos packages et emplacements existants. Cependant, si vous n’avez pas de budget incrémentiel pour tester les identifiants universels, réduisez les budgets d’origine pour financer les tests.

* Copiez vos packages et emplacements d’origine, ajustez les budgets en fonction de la taille du test, modifiez les audiences à utiliser [!DNL RampID]Segments basés sur (pour les utilisateurs authentifiés) ou sur ID5 (pour les utilisateurs non authentifiés), et vérifiez que les nouveaux modules et emplacements dépensent l’intégralité de leur budget.

   * Pour comparer les performances des segments universels basés sur des identifiants aux performances des emplacements ciblant d’autres identifiants d’audience, tels que les cookies ou les identifiants de publicité mobile, créez une campagne avec un emplacement universel distinct basé sur des identifiants et un emplacement hérité basé sur des identifiants.

     Pour un test de reciblage complet, ciblez les RampID pour les utilisateurs authentifiés et les ID5 pour les utilisateurs non authentifiés.

     Obtenir les meilleures performances ne devrait pas être la principale comparaison. Déterminez plutôt les identifiants qui évoluent correctement, ce qui peut influencer votre optimisation et vos allocations budgétaires ultérieurement. L’objectif à long terme est de compenser les impressions perdues et le trafic du site lorsque les cookies sont obsolètes.

   * Pour comparer la portée totale du navigateur, ciblez les segments universels basés sur les identifiants et les segments hérités basés sur les identifiants au même emplacement. Utilisez les mêmes paramètres de campagne que le cas d’utilisation précédent, sauf que vous n’avez pas besoin de fractionner le budget de l’opération.

     La préférence d’offre est accordée aux identifiants universels, mais les identifiants hérités reçoivent des offres lorsque les identifiants universels ne sont pas disponibles. Assurez-vous de comparer la portée dans différents navigateurs (notamment Chrome, Safari et Mozilla).

     >[!NOTE]
     >
     >La limitation de fréquence s’applique à un ID individuel. Lorsqu’un utilisateur possède plusieurs types d’ID, vous pouvez l’atteindre plus que prévu.

* N’oubliez pas que la portée des segments d’audience authentifiés est naturellement plus petite que celle des segments basés sur des cookies et que l’utilisation d’options de ciblage supplémentaires réduit votre portée. Soyez judicieux lorsque vous utilisez un ciblage granulaire, en particulier en associant plusieurs cibles à des instructions ET.

## Causes des écarts de données entre les ID de courrier électronique et les ID universels {#universal-ids-data-variances}

* ID de courrier électronique haché traduits en ID5 :

  Le modèle probabiliste présente une variance d’erreur de +/- 5 %. Cela signifie qu’il peut surestimer ou sous-estimer le nombre d’audiences de 5 %.

* ID de courrier électronique haché convertis en [!DNL RampIDs]:

   * Lorsque plusieurs profils utilisent le même ID d’adresse électronique, le nombre de segments DSP peut être inférieur au nombre de profils dans votre plateforme de données client. Dans Adobe Photoshop, par exemple, vous pouvez créer un compte de société et un compte personnel à l’aide d’un seul ID de courrier électronique. Mais si les deux profils appartiennent au même segment, ils correspondent à un ID d’email et correspondant à un [!DNL RampID].

   * A [!DNL RampID] peut être mis à niveau vers une nouvelle valeur. If [!DNL LiveRamp] ne reconnaît pas un ID d’adresse électronique ou ne peut pas le mapper à un ID existant ; [!DNL RampID] dans sa base de données, puis il affecte une nouvelle [!DNL RampID] à l’ID d’adresse électronique. À l’avenir, lorsqu’ils pourront mapper l’e-mail à un autre [!DNL RampID] ou peuvent recueillir plus d’informations sur le même ID d’e-mail, ils mettent à niveau la variable [!DNL RampID] à une nouvelle valeur. [!DNL LiveRamp] fait référence à cette action comme mise à niveau à partir d’un &quot;dérivé&quot; [!DNL RampID] à un &quot;conservé&quot; [!DNL RampID]. Cependant, DSP n’obtient pas de mappages entre les mappages dérivés et gérés. [!DNL RampIDs] et ne peut donc pas supprimer la version précédente de l’ID RampID du segment DSP. Dans ce cas, le nombre de segments peut être supérieur au nombre de profils.

     Exemple : un utilisateur se connecte au [!DNL Adobe] et visite la page Photoshop. If [!DNL LiveRamp] ne contient aucune information existante sur l’ID d’adresse électronique, puis il lui affecte un [!DNL RampID], par exemple D123. Quinze jours plus tard, l’utilisateur consulte la même page, mais [!DNL LiveRamp] a mis à niveau la variable [!DNL RampID] pendant ces 15 jours et a réaffecté la fonction [!DNL RampID] au M123. Même si le segment de la plateforme de données client &quot;Photoshop Enthusiast&quot; ne comporte qu’un seul e-mail pour l’utilisateur, le segment DSP comporte deux RampID : D123 et M123.

## Dépannage

Si vous ne voyez pas le nombre d’utilisateurs ou si les tailles de votre audience sont faibles, vérifiez les points suivants :

* Si vous utilisez [!DNL Flashtalking] ou [!DNL Google Campaign Manager 360] publicités, puis assurez-vous que les URL de clics publicitaires de vos publicités sont ajoutées avec les macros correctes. Voir les macros pour [[!DNL Flashtalking] publicités](/help/integrations/analytics/macros-flashtalking.md) et [[!DNL Google Campaign Manager 360] publicités](/help/integrations/analytics/macros-google-campaign-manager.md).

* Assurez-vous que le code approprié et universel propre au partenaire d’ID est implémenté sur votre site web pour faire correspondre les événements sur site et les expositions publicitaires. Travaillez avec votre [!DNL LiveRamp] ou [!DNL ID5] le cas échéant.

* (Pour [!DNL RampIDs] et [!DNL UID 2.0] ID) Assurez-vous que la variable [DSP source de données est correctement configurée](/help/dsp/audiences/sources/source-manage.md#source-settings)et que les comptes d’utilisateurs sont renseignés pour les segments d’audience générés.

* Si votre portée est inférieure à ce que vous attendez, vérifiez que la logique du segment d’audience n’est pas trop granulaire.

Si vous ne parvenez pas à résoudre le problème, contactez votre équipe de compte d’Adobe.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gestion des sources d’audience pour activer les audiences d’ID universelles](/help/dsp/audiences/sources/source-manage.md)
>* [Création et implémentation d’un segment personnalisé](/help/dsp/audiences/custom-segment-create.md)
>* [Importation manuelle de segments authentifiés depuis [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
