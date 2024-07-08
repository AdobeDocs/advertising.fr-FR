---
title: Prise en charge de l’activation des ID universels
description: Découvrez la prise en charge de l’importation de segments d’ID universels, de la création de segments personnalisés pour suivre les identifiants universels et de la conversion d’autres identifiants utilisateur dans vos segments propriétaires en identifiants universels pour le ciblage sans cookie.
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: ea50b94ebc6d27fda9c0bd9f61da16750fa58f83
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# Prise en charge de l’activation des ID universels

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Fonctionnalité bêta*

DSP prend en charge les identifiants universels basés sur les personnes pour un ciblage sans cookie sur un seul appareil (et non sur plusieurs appareils) sur les formats numériques pris en charge par DSP.

* Vous pouvez envoyer manuellement vos [[!DNL LiveRamp] [!DNL RampIDs]] authentifiés directement à DSP l’aide du tableau de [!DNL LiveRamp] [!DNL Connect] bord. Voir «[ Importation manuelle de segments authentifiés depuis [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md) ».

* DSP pouvez ingérer vos segments propriétaires composés d’identifiants d’e-mail hachés intégrés à votre plateforme de données client (CDP) et les convertir en [!DNL LiveRamp] [!DNL RampIDs] et [!DNL Unified ID 2.0 (UID2.0)] ID. Pour plus d’informations sur les plateformes de données client prises en charge, les fonctionnalités disponibles pour chaque type d’ID universel pris en charge et les workflows associés, voir «[ À propos des sources](/help/dsp/audiences/sources/source-about.md) d’audience propriétaires ».

* Vous pouvez créer des segments personnalisés qui suivent les utilisateurs associés aux ID universels ID5 qui sont exposés à des publicités à partir d’ordinateurs de bureau et d’appareils mobiles et qui visitent des pages Web spécifiques. ID5 utilise un modèle probabiliste pour attribuer un ID dérivé de divers signaux utilisateur et signaux de navigateur. Pour obtenir des instructions, voir «[ Création et implémentation d’un segment](/help/dsp/audiences/custom-segment-create.md) personnalisé ».

* Les segments tiers de certains fournisseurs peuvent inclure automatiquement des identifiants universels en plus des utilisateurs suivis par des cookies ou des identifiants d’appareil. Par exemple, les segments de [!DNL Eyeota] peuvent inclure automatiquement des ID ID5, tandis que les segments de [!DNL Lotame] peuvent inclure des ID UID2.0. Les détails du segment incluent la taille pour chaque type. Les frais d’utilisation habituels pour chaque segment, qui sont indiqués à côté du nom du segment, s’appliquent ; aucuns frais supplémentaires ne sont facturés pour les ID ID5.

## Création de rapports par type d’ID universel

* **Rapports personnalisés :** les données de coût, d’impression, de clic, de conversion et de fréquence par type d’ID universel sont disponibles dans les rapports personnalisés.

* **[!DNL Analytics]Rapports :** les annonceurs [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) qui ont implémenté toutes les étapes requises peuvent voir les conversions d’affichage publicitaire par type d’ID universel dans [!DNL Analytics].

  >[!IMPORTANT]
  >
  >Pour une attribution de conversion correcte, assurez-vous que les URL de clics publicitaires de vos annonces incluent à la fois l’ID [EF et l’ID AMO.](/help/integrations/analytics/ids.md)

* **Détails du segment :** pour tous les types de segment, les détails du segment incluent la taille de l’audience par type d’ID universel et par le type d’appareil suivi par les cookies ou les ID d’appareil.

## Comment Target une audience d’ID universel dans vos emplacements

>[!NOTE]
>
>Vous ne pouvez pas modifier les types d’ID ciblés dans un emplacement réel. Si nécessaire, vous pouvez dupliquer un emplacement actif et modifier les types d’ID ciblés dans le nouvel emplacement.

Dans un emplacement nouveau, planifié ou suspendu, procédez comme suit :

1. Dans cette [!UICONTROL Geo-Targeting] section, indiquez les zones géographiques à cibler. Chaque partenaire d’ID universel autorise le ciblage des utilisateurs uniquement dans des zones géographiques spécifiques, et seuls les types d’ID éligibles sont disponibles dans les [!UICONTROL Targeting] paramètres.

1. Dans cette [!UICONTROL Audience Targeting] section, procédez comme suit :

   1. Dans le [!UICONTROL Included Audiences] paramètre, sélectionnez le segment pour lequel les données utilisateur ont été converties en ID universels.

      Vous pouvez inclure d’autres segments si vous le souhaitez.

   1. Dans les [!UICONTROL Targeting] paramètres :

      1. Sélectionnez le type d’identifiant universel à cibler.

         Le paramètre comprend les options «[!UICONTROL Legacy IDs] » et «[!UICONTROL Universal ID] , » qui peuvent inclure les sous-options «[!UICONTROL ID5] », «[!UICONTROL RampID] » et «[!UICONTROL Unified ID2.0] . » Les cibles géographiques sélectionnées déterminent les sous-options disponibles.

         Vous pouvez sélectionner à la fois «[!UICONTROL Legacy IDs] » et «[!UICONTROL Universal ID] , mais vous ne pouvez sélectionner qu’un seul type d’ID universel par emplacement. Lorsque vous sélectionnez à la fois les ID hérités et les ID universels, la préférence d’enchère est donnée aux ID universels.

      1. (Si nécessaire) Acceptez les conditions d’utilisation des identifiants universels.

         Avant de pouvoir convertir des données en un nouveau type d’ID, un utilisateur du compte DSP doit accepter les conditions d’utilisation. Les conditions ne doivent être acceptées qu’une seule fois par type d’ID et par compte.

Voir «[ Paramètres de](/help/dsp/campaign-management/placements/placement-settings.md) positionnement ».

## Bonnes pratiques pour les tests et la validation des données

Utilisez les meilleures pratiques suivantes pour [!DNL RampID]les segments basés sur et ID5, pour lesquels Adobe Analytics mesure est disponible.

* Environ 24 heures après l’activation d’un segment, vérifiez le nombre d’ID convertis pour le segment dans [!UICONTROL Audiences] > [!UICONTROL All Audiences]. Si le nombre d’ID est inattendu, contactez votre équipe de compte Adobe.

  Voir «[ Causes des écarts de données entre les ID de messagerie et les ID universels](#universal-ids-data-variances) » pour plus d’informations sur la façon dont le nombre de segments peut varier.

* Ne modifiez pas vos packages et emplacements existants. Toutefois, si vous ne disposez pas d’un budget supplémentaire pour tester les ID universels, réduisez les budgets d’origine pour financer les tests.

* Copiez vos packages et emplacements d’origine, ajustez les budgets en fonction de la taille du test, modifiez les audiences pour utiliser [!DNL RampID]des segments basés sur des segments (pour les utilisateurs authentifiés) ou ID5 (pour les utilisateurs non authentifiés), et vérifiez que les nouveaux packages et emplacements dépensent tous leurs budgets.

   * Pour comparer les performances des segments universels basés sur l’ID avec les performances des emplacements ciblant d’autres identificateurs d’audience, tels que les cookies ou les ID publicitaires mobiles, créez une campagne avec un emplacement séparé basé sur un ID universel et un emplacement basé sur un ID hérité.

     Pour un test de reciblage complet, ciblez à la fois les RampID pour les utilisateurs authentifiés et les ID5 pour les utilisateurs non authentifiés.

     Obtenir les meilleures performances ne devrait pas être la comparaison principale. Au lieu de cela, déterminez quels ID évoluent bien, ce qui pourrait informer ultérieurement votre optimisation et vos allocations budgétaires. L’objectif à long terme est de compenser les impressions perdues et le trafic du site lorsque les cookies sont obsolètes.

   * Pour comparer la portée totale du navigateur, ciblez les segments Universal ID et les segments hérités basés sur ID au même emplacement. Utilisez les mêmes paramètres de campagne que dans le cas d’utilisation précédent, sauf que vous n’avez pas besoin de diviser le budget de la campagne.

     La préférence d’enchère est donnée aux ID universels, mais les ID hérités reçoivent des offres lorsque les ID universels ne sont pas disponibles. Assurez-vous de comparer la portée dans différents navigateurs (y compris Chrome, Safari et Mozilla).

     >[!NOTE]
     >
     >Le plafonnement de fréquence s’applique à un identifiant individuel. Lorsqu’un utilisateur possède plusieurs types d’ID, vous risquez de l’atteindre plus que prévu.

* N’oubliez pas que la portée des segments d’audience authentifiés est naturellement inférieure à celle des segments basés sur des cookies et que l’utilisation d’options de ciblage supplémentaires réduit encore votre portée. Utilisez judicieusement le ciblage granulaire, notamment en joignant plusieurs cibles avec des instructions ET.

## Causes des écarts de données entre les ID de courrier électronique et les ID universels {#universal-ids-data-variances}

* Identifiants d’e-mail hachés traduits en ID ID5 :

  Le modèle probabiliste présente une variance d’erreur de +/- 5 %. Cela signifie qu’il peut surestimer ou sous-estimer le nombre d’audiences de 5 %.

* Identifiants d’email hachés traduits par [!DNL RampIDs]:

   * Lorsque plusieurs profils utilisent le même ID d’e-mail, le nombre de segments de DSP peut être inférieur au nombre de profils au sein de votre plateforme de données client. Par exemple, dans Adobe Photoshop, vous pouvez créer un compte d’entreprise et un compte personnel à l’aide d’un seul ID de messagerie. Mais si les deux profils appartiennent à la même personne, les profils correspondent à un identifiant e-mail et correspondant à un [!DNL RampID].

   * A [!DNL RampID] peut être mise à niveau vers une nouvelle valeur. Si [!DNL LiveRamp] ne reconnaît pas un ID de messagerie ou ne peut pas le mapper à un identifiant [!DNL RampID] existant dans sa base de données, il attribue un nouveau [!DNL RampID] à l’ID de messagerie. À l’avenir, lorsqu’ils pourront mapper l’ID de messagerie à un autre [!DNL RampID] ou recueillir plus d’informations sur le même ID de messagerie, ils mettront à niveau vers [!DNL RampID] une nouvelle valeur. [!DNL LiveRamp] se réfère à cette action comme la mise à niveau d’un « dérivé » [!DNL RampID] à un « maintenu » [!DNL RampID]. Toutefois, DSP n’obtient pas de mappages entre dérivés et maintenus [!DNL RampIDs] et ne peut donc pas supprimer la version précédente de RampID du segment DSP. Dans ce cas, le nombre de segments peut être supérieur au nombre de profils.

     Exemple : un utilisateur se connecte au [!DNL Adobe] site Web et visite la page Photoshop. S’il [!DNL LiveRamp] n’a pas d’informations existantes sur l’ID de courrier électronique, ils lui attribuent un dérivé [!DNL RampID], disons D123. Quinze jours plus tard, l’utilisateur visite la même page, mais [!DNL LiveRamp] a mis à niveau la [!DNL RampID] au cours de ces 15 jours et a réaffecté la à M123 [!DNL RampID] . Même si le segment « Photoshop Enthusiast » de la plateforme de données client n’a qu’un seul identifiant e-mail pour l’utilisateur, le segment DSP a deux RampID : D123 et M123.

## Dépannage

Si le nombre d’utilisateurs n’est pas visible ou si la taille de votre audience est faible, vérifiez les points suivants :

* Si vous utilisez [!DNL Flashtalking] des annonces or [!DNL Google Campaign Manager 360] , assurez-vous que les URL de clics de vos annonces sont ajoutées avec les macros correctes. Voir les macros pour [[!DNL Flashtalking] les publicités](/help/integrations/analytics/macros-flashtalking.md) et [[!DNL Google Campaign Manager 360] les publicités](/help/integrations/analytics/macros-google-campaign-manager.md).

* Assurez-vous que le code spécifique au partenaire d’ID universel correct est implémenté sur votre site Web pour correspondre aux événements sur site et aux expositions publicitaires. Travaillez avec votre ou [!DNL ID5] votre [!DNL LiveRamp] représentant au besoin.

* (Pour [!DNL RampIDs] et [!DNL UID 2.0] ID) Assurez-vous que votre [source de données DSP est correctement](/help/dsp/audiences/sources/source-manage.md#source-settings) configurée et que les nombres d’utilisateurs sont renseignés pour les segments d’audience générés.

* Si votre portée est inférieure aux attentes, vérifiez que la logique du segment d’audience n’est pas trop granulaire.

* Assurez-vous que vos paramètres de campagne, de package et de placement sont corrects.<!-- wording-->

Si vous ne parvenez pas à résoudre le problème, contactez l’équipe chargée de votre compte Adobe.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer la Audiences d’identification universelle](/help/dsp/audiences/sources/source-manage.md)
>* [Création et implémentation d’un segment personnalisé](/help/dsp/audiences/custom-segment-create.md)
>* [Importer manuellement des segments authentifiés à partir de [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Gestion de l’audience](/help/dsp/audiences/audience-about.md)
>* [Paramètres de positionnement](/help/dsp/campaign-management/placements/placement-settings.md)
