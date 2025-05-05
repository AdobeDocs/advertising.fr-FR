---
title: Gestion de l’audience dans Advertising DSP
description: Découvrez les fonctionnalités de gestion de l’audience.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 31f20bcfb79265326f515218a02d8a4fa3efd586
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# Gestion de l’audience dans Advertising DSP

Dans DSP, vous pouvez créer et gérer des segments d’audience et des ensembles d’audiences, que vous pouvez utiliser comme cibles pour vos emplacements :

* Collectez vos propres données d’audience propriétaires en créant et en implémentant DSP segments. Vous pouvez ensuite recibler les utilisateurs du segment avec des publicités ou empêcher les utilisateurs du segment de recevoir des publicités. Vous pouvez créer les types de segments suivants :

   * [ Segments personnalisés ](/help/dsp/audiences/custom-segment-create.md) pour effectuer le suivi a) des utilisateurs exposés aux publicités depuis des ordinateurs de bureau et des appareils mobiles et b) des utilisateurs qui visitent des pages web spécifiques. La balise de suivi peut effectuer le suivi des utilisateurs basés sur des cookies ou des utilisateurs associés aux identifiants universels ID5.

   * [Segments d’opposition à la vente des informations personnelles du CCPA](/help/dsp/audiences/ccpa-opt-out-segment-create.md) pour effectuer le suivi des ID des utilisateurs des demandes d’opposition à la vente des informations personnelles des clients sur votre site web, conformément au California Consumer Privacy Act (CCPA). Vous pouvez récupérer les rapports mensuels des identifiants d’utilisateur à partir des demandes d’opposition à la vente.

     Pour plus d’informations sur la prise en charge des Adobes Advertising pour les demandes d’opposition à la vente des produits CCPA, voir [Prise en charge des Adobes Advertising pour le California Consumer Privacy Act : prise en charge de l’opposition des consommateurs](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Fonctionnalité Beta) [Obtenez et utilisez des identifiants universels pour le ciblage sans cookie ](/help/dsp/audiences/universal-ids.md) :

   * Envoyez manuellement vos segments [!DNL LiveRamp] [!DNL RampID] authentifiés directement à DSP.

   * Permet DSP d’importer des segments propriétaires à partir de votre plateforme de données client et de les convertir en types d’ID universels pris en charge.

   * Incluez des segments tiers contenant des identifiants universels dans vos cibles d’emplacement sans aucune étape supplémentaire.

* Créez une bibliothèque d’audiences de [audiences réutilisables](/help/dsp/audiences/reusable-audience-create.md). Les audiences enregistrées sont composées de l’un de vos segments d’audience disponibles et de l’une de vos autres audiences enregistrées. Toute modification apportée à une audience enregistrée est automatiquement appliquée à tous les emplacements qui ciblent ou excluent l’audience et à toutes les autres audiences qui incluent l’audience enregistrée.

  Les audiences enregistrées permettent aux planificateurs de médias de regrouper les audiences selon les besoins, en incluant et en excluant plusieurs segments à l’aide d’une logique booléenne complexe. La taille de chaque segment et la taille totale de l’audience sont indiqués au fur et à mesure que vous créez une audience. Les exécutants de Campaign peuvent alors simplement sélectionner une ou plusieurs audiences enregistrées comme cibles d’emplacement plutôt que de configurer manuellement les cibles d’audience pour chaque emplacement.

D’autres types d’audience sont également disponibles pour le ciblage des emplacements.

## Importation de segments de données propriétaires et tiers

Vous disposez de nombreuses options pour importer des segments de données propriétaires et tiers dans DSP, à l’aide de l’interface utilisateur DSP et/ou par le biais de services d’importation personnalisés.

* DSP peut extraire vos audiences Adobe Audience Manager et [!DNL Adobe] pour le ciblage. Pour connaître les conditions préalables et les instructions, voir &quot;[Importation de segments Adobe Audience Manager pour le ciblage des publicités](/help/integrations/audience-manager/import-audiences.md).

* DSP peut convertir des segments de données propriétaires des plateformes de données clients prises en charge en segments avec des ID universels à l’aide de la [fonctionnalité Sources](/help/dsp/audiences/sources/source-about.md). Vous pouvez également [envoyer manuellement vos segments authentifiés [!DNL LiveRamp] [!DNL RampID] directement vers DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP pouvez importer vos autres segments de données propriétaires directement à partir de votre plateforme de gestion des données (DMP) et les fournir à tout ensemble d’annonceurs, si nécessaire.

* DSP peut importer des segments tiers personnalisés, y compris des combinaisons complexes de segments tiers. Vous pouvez fournir les segments à n’importe quel groupe d’annonceurs, si nécessaire.

Pour plus d’informations, contactez votre équipe de compte d’Adobe.

## Audiences disponibles en tant que cibles de placement

Vous pouvez cibler vos emplacements sur tous les types d’audiences suivants.

* Tous les jeux d’audiences créés par l’utilisateur qui ont été enregistrés dans DSP.

* Tous les segments d’audience créés par l’utilisateur qui ont été créés dans DSP :

   * Segments personnalisés pour les utilisateurs qui ont consulté des pages web spécifiques et qui ont été exposés à des impressions de publicités spécifiques.

     Les impressions diffusées aux identifiants universels n’engendrent aucuns frais.

   * Segments d’audience d’opposition à la vente des informations personnelles du CCPA pour les utilisateurs qui ont soumis des demandes d’opposition à la vente des informations personnelles sur votre site web, en vertu du California Consumer Privacy Act (CCPA).

* Tous les segments de données propriétaires importés, y compris les segments qui ont été traduits en identifiants universels.

  Des frais supplémentaires sont facturés pour les impressions diffusées aux identifiants universels. Voir &quot;[À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)&quot; pour connaître les taux.

* Tous les segments de données tiers personnalisés importés.

* (Emplacements ciblant uniquement les États-Unis) [Tous les segments de données tiers disponibles pour DSP clients de plus de 30 fournisseurs](/help/dsp/audiences/third-party-data-providers.md), y compris [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]),[!DNL Lotame], [!DNL Neustar], et bien plus encore.

  Vous pouvez cibler des segments spécifiques, qui ciblent les utilisateurs en fonction des données d’audience (par exemple, les utilisateurs avec des données démographiques, des centres d’intérêt ou des intentions spécifiques et/ou des profils comportementaux). Vous pouvez naviguer par fournisseur de données et par catégorie, rechercher des segments par nom ou identifiant de segment, ou filtrer les résultats par fournisseur de données, taille totale des segments, nombre de navigateurs Web ou nombre d’appareils.

  Les segments tiers engendrent des frais supplémentaires, indiqués en regard de chaque nom de segment.

* (Publicitaires avec Adobe Experience Platform et [!DNL Real-Time CDP], Adobe Audience Manager ou Adobe Analytics qui utilisent uniquement les balises de conversion JavaScript d’Adobe Advertising) Tous les segments d’audience propriétaires, de deuxième ou de troisième niveau disponibles créés dans [!DNL Real-Time CDP], créés dans Audience Manager ou publiés sur Adobe Experience Cloud à partir d’Audience Manager ou de [!DNL Analytics].

  Les tarifs d’utilisation des segments sont pré-négociés et ne sont pas visibles dans DSP.

  Les segments de [!DNL Analytics] sont disponibles environ une heure après leur création ou leur publication en tant qu’audiences Experience Cloud. Les segments provenant directement d’Audience Manager ou de [!DNL Real-Time CDP] sont disponibles dans les 24 heures suivant leur partage.

  >[!NOTE]
  >
  >Pour plus d’informations sur la configuration et la collecte de données pour les segments dans ces solutions, consultez la documentation de [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=fr), [Analytics](https://experienceleague.adobe.com/docs/analytics.html?lang=fr) et [the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html?lang=fr).

## Données sur la taille de l’audience

Dans Audiences > Toutes les audiences et dans la section Ciblage de l’audience des paramètres de placement, vous pouvez filtrer chaque liste de segments par plage de tailles, y compris la plage totale et les plages distinctes pour des types d’appareils spécifiques ou des types d’identifiants universels.

![filtrer par taille d’audience](/help/dsp/assets/audience-size-filter.png)

Vous pouvez également consulter des données détaillées sur la taille de l’audience :

* La taille totale et active de l’audience dédupliquée sur tous les segments sélectionnés et les audiences enregistrées s’affiche. Vous pouvez afficher les détails par type d’appareil (navigateur, mobile ou télévision connectée).

  ![la taille d’audience combinée](/help/dsp/assets/audience-size.png)

* Pour les segments individuels, la taille totale de l’audience et le CPM (le cas échéant) s’affichent en regard du nom du segment.

  ![taille de segment individuel](/help/dsp/assets/audience-size-segment.png)

* Vous pouvez afficher plus de détails sur un segment individuel ou une audience enregistrée, y compris la taille par navigateur, mobile, télévision connectée et partenaire de type d’identifiant universel. Pour les audiences enregistrées, la taille totale est le total dédupliqué.

  ![le segment individuel ou les détails de l’audience enregistrée](/help/dsp/assets/audience-size-segment-details.png)

## Audiences vues

### Vue Toutes les audiences

Dans la vue [!UICONTROL All Audiences], ou la bibliothèque d’audiences, vous pouvez enregistrer et gérer des audiences réutilisables, qui incluent des groupes de segments d’audience et même d’autres audiences enregistrées. Vous pouvez utiliser les audiences comme cibles pour plusieurs emplacements. Le nombre d’emplacements dans lesquels chaque audience est utilisée est indiqué en regard du nom de l’emplacement.

Vous pouvez modifier, cloner, supprimer, exporter ou partager une audience.

### Vue Segments

Dans la vue [!UICONTROL Segments], tous les utilisateurs peuvent créer des segments personnalisés supplémentaires.

La vue [!UICONTROL Segments] répertorie également les types de segments suivants :

* Tous les segments personnalisés créés par l’utilisateur sont disponibles pour l’utilisateur.

  Vous pouvez afficher les balises de suivi pour l’un des segments personnalisés que vous avez créés et les partager avec d’autres utilisateurs. Vous pouvez également modifier ou supprimer les segments personnalisés que vous avez créés.

  Vous ne pouvez pas modifier ni partager des segments personnalisés que d’autres utilisateurs ont partagés avec vous.

* Tous les segments propriétaires importés en l’état sont disponibles pour l’utilisateur.

  Vous ne pouvez pas modifier ni partager les segments propriétaires qui ont été partagés avec vous. Contactez votre équipe de compte d’Adobe si vous devez partager des segments propriétaires avec d’autres utilisateurs.

* Tous les segments tiers personnalisés sont disponibles pour l’utilisateur.

  Vous ne pouvez pas modifier ni partager des segments tiers qui ont été partagés avec vous. Contactez votre équipe de compte d’Adobe si vous devez partager des segments tiers avec d’autres utilisateurs.

### Vue Sources

Dans la vue [!UICONTROL Sources], vous pouvez configurer des sources pour les segments propriétaires dans les plateformes de données clients prises en charge que vous souhaitez convertir en segments contenant des types d’ID universels spécifiés. Les paramètres de la source incluent une clé source générée automatiquement que vous fournirez à votre plateforme de données client pour établir la connexion.

Pour plus d’informations sur les plateformes de données client prises en charge, les types d’ID universels pris en charge et les processus de configuration des connexions à chaque plateforme de données client, voir &quot;[À propos des sources](/help/dsp/audiences/sources/source-about.md)&quot;.

Les segments traduits peuvent être inclus dans les audiences réutilisables et dans les paramètres de placement pour un ciblage sans cookie.

>[!MORELIKETHIS]
>
>* [Prise en charge de l’activation des ID universels](/help/dsp/audiences/universal-ids.md)
>* [Création d’une audience réutilisable](reusable-audience-create.md)
>* [Créer et implémenter un segment personnalisé](custom-segment-create.md)
>* [Créer et implémenter un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universels](/help/dsp/audiences/sources/source-manage.md)
>* [ Importation manuelle de segments authentifiés à partir de  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md)
