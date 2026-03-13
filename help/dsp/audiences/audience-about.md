---
title: À propos de la gestion de l’audience dans Advertising DSP
description: Découvrez les fonctionnalités de gestion de l’audience.
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: ddd55586ed895962b8f6da0390a3d76fe43ca1ca
workflow-type: tm+mt
source-wordcount: '1322'
ht-degree: 0%

---

# À propos de la gestion de l’audience dans Advertising DSP

Dans DSP, vous pouvez créer et gérer des segments d’audience et des ensembles d’audiences, que vous pouvez utiliser comme cibles pour vos emplacements :

* Collectez vos propres données d’audience propriétaires en créant et en implémentant des segments DSP. Vous pouvez par la suite recibler les utilisateurs du segment avec des annonces ou empêcher les utilisateurs du segment de recevoir des annonces. Vous pouvez créer les types de segments suivants :

   * [Segments personnalisés](/help/dsp/audiences/custom-segment-create.md) pour effectuer le suivi a) des utilisateurs exposés aux publicités des ordinateurs de bureau et des appareils mobiles et b) des utilisateurs qui visitent des pages web spécifiques. La balise de suivi peut effectuer le suivi des utilisateurs basés sur des cookies ou des utilisateurs associés aux ID5 universels.

   * [Segments d’opposition à la vente de l’ACPCP](/help/dsp/audiences/ccpa-opt-out-segment-create.md) pour effectuer le suivi des identifiants des utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, conformément à la Loi sur la protection de la vie privée des consommateurs de Californie (CCPA). Vous pouvez récupérer les rapports mensuels des ID utilisateur à partir des requêtes d’opposition à la vente des informations personnelles.

     Pour plus d’informations sur la prise en charge par Adobe Advertising des demandes d’opposition à la vente du CCPA, consultez [Prise en charge d’Adobe Advertising pour la Loi sur la protection de la vie privée des consommateurs de Californie : prise en charge de l’opposition du consommateur](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

* (Fonction Beta) [Obtention et utilisation d’ID universels pour le ciblage sans cookie](/help/dsp/audiences/universal-ids.md) :

   * Envoyez manuellement vos segments authentifiés [!DNL LiveRamp] [!DNL RampID] directement à DSP.

   * Autorisez DSP à importer des segments propriétaires à partir de votre plateforme de données client et à les traduire en types d’identifiants universels pris en charge.

   * Incluez des segments tiers qui contiennent des identifiants universels dans vos cibles d’emplacement sans étapes supplémentaires.

* Créez une bibliothèque d’audiences [audiences réutilisables](/help/dsp/audiences/reusable-audience-create.md). Les audiences enregistrées sont composées de l’un des segments d’audience disponibles et de l’autre de vos audiences enregistrées. Toutes les modifications apportées à une audience enregistrée sont automatiquement appliquées à tous les emplacements qui ciblent ou excluent l’audience et à toutes les autres audiences qui incluent l’audience enregistrée.

  Les audiences enregistrées permettent aux planificateurs de médias de regrouper les audiences selon les besoins, en incluant et en excluant plusieurs segments à l’aide d’une logique booléenne complexe. La taille (ciblée) de chaque segment individuel et la taille globale de l’audience active sont indiquées au fur et à mesure que vous créez une audience. Les personnes en charge de l&#39;exécution des campagnes peuvent alors simplement sélectionner une ou plusieurs audiences enregistrées comme cibles d&#39;emplacement plutôt que de configurer manuellement les cibles d&#39;audience pour chaque emplacement.

D’autres types d’audience sont également disponibles pour le ciblage des emplacements.

## Importation de segments de données propriétaires et tiers

Vous disposez de nombreuses options pour importer des segments de données propriétaires et tiers dans DSP, à l’aide de l’interface utilisateur de DSP et/ou par le biais de services d’importation personnalisés.

* DSP peut extraire votre Adobe Audience Manager et d’autres audiences [!DNL Adobe] pour le ciblage. Pour connaître les conditions préalables et les instructions, voir « [Importation de segments Adobe Audience Manager pour le ciblage publicitaire](/help/integrations/audience-manager/import-audiences.md).

* DSP peut traduire des segments de données propriétaires à partir de plateformes de données client prises en charge en segments avec des ID universels à l’aide de la [fonctionnalité Sources](/help/dsp/audiences/sources/source-about.md). Vous pouvez également [envoyer manuellement vos segments authentifiés [!DNL LiveRamp] [!DNL RampID] directement à DSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md).

* DSP peut importer vos autres segments de données propriétaires directement à partir de votre plateforme de gestion des données (DMP) et les fournir à n’importe quel ensemble d’annonceurs, si nécessaire.

* DSP peut importer des segments tiers personnalisés, y compris des combinaisons complexes de segments tiers. Vous pouvez fournir les segments à n’importe quel ensemble d’annonceurs, si nécessaire.

Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

## Audiences disponibles en tant que cibles d’emplacement

Vous pouvez cibler vos emplacements sur tous les types d’audiences suivants.

* Toutes les audiences créées par l’utilisateur qui ont été enregistrées dans DSP.

* Tous les segments d’audience créés par l’utilisateur ou l’utilisatrice qui ont été créés dans DSP :

   * Segments personnalisés pour les utilisateurs et utilisatrices qui ont visité des pages web spécifiques et les utilisateurs et utilisatrices exposés aux impressions d’annonces spécifiques.

     Aucun frais n’est encouru pour les impressions diffusées aux identifiants universels.

   * Segments d’audience d’opposition à la vente de la CCPA pour les utilisateurs qui ont soumis des requêtes d’opposition à la vente sur votre site web, conformément à la Loi sur la protection de la vie privée des consommateurs de Californie (CCPA).

* Tous les segments de données propriétaires importés, y compris les segments qui ont été traduits en identifiants universels.

  Des frais supplémentaires sont facturés pour les impressions remises aux cartes d’identité universelles. Consultez « [ À propos des sources d’audience propriétaires »](/help/dsp/audiences/sources/source-about.md) pour obtenir des taux.

* Tous vos segments de données tiers personnalisés importés.

* (Emplacements ciblant les États-Unis uniquement) [Tous les segments de données tiers disponibles pour les clients DSP de plus de 30 fournisseurs](/help/dsp/audiences/third-party-data-providers.md) dont [!DNL eXelate], ([!DNL Eyeota]), ([!DNL LiveRamp]), [!DNL Lotame], [!DNL Neustar], et bien d’autres.

  Vous pouvez cibler des segments spécifiques, qui ciblent les utilisateurs en fonction des données d’audience (par exemple, les utilisateurs avec des données démographiques spécifiques, des intérêts ou des intentions, et/ou des profils comportementaux). Vous pouvez effectuer une navigation par fournisseur de données et par catégorie, rechercher des segments par nom ou identifiant de segment, ou filtrer les résultats par fournisseur de données, taille du segment actif, nombre de navigateurs web ou nombre d’appareils.

  Les segments tiers entraînent des frais supplémentaires, qui sont indiqués en regard de chaque nom de segment.

* (Annonceurs sous Adobe Experience Platform et [!DNL Real-Time CDP], Adobe Audience Manager ou Adobe Analytics qui utilisent uniquement les balises de conversion Adobe Advertising JavaScript) Tous les segments d’audience propriétaires, secondaires ou tiers disponibles, créés dans [!DNL Real-Time CDP], créés dans Audience Manager ou publiés sur Adobe Experience Cloud à partir d’Audience Manager ou d’[!DNL Analytics].

  Le prix d’utilisation des segments est prénégocié et n’est pas visible dans DSP.

  Les segments provenant de [!DNL Analytics] sont disponibles environ une heure après leur création ou leur publication en tant qu’audiences Experience Cloud. Les segments provenant directement d’Audience Manager ou de [!DNL Real-Time CDP] sont disponibles dans les 24 heures suivant leur partage.

  >[!NOTE]
  >
  >Pour plus d’informations sur la configuration et la collecte de données pour les segments dans ces solutions[](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html) consultez la documentation de [Audience Manager](https://experienceleague.adobe.com/docs/analytics.html), [Analytics [!DNL Real-Time CDP] et ](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html)the.

## Données de taille d’audience

Dans Audiences > Toutes les audiences et dans la section Ciblage des audiences des paramètres d’emplacement, vous pouvez filtrer chaque liste de segments par plage de tailles, y compris des plages distinctes pour des types d’appareils spécifiques ou des types d’identifiants universels.

![filtrer par taille d’audience](/help/dsp/assets/audience-size-filter.png)

Vous pouvez également afficher les données détaillées sur la taille des audiences :

* La taille de l’audience dédupliquée active sur tous les segments sélectionnés et les audiences enregistrées s’affiche et vous pouvez afficher les détails par type d’appareil (navigateur, mobile ou télévision connectée).

  ![taille d’audience combinée](/help/dsp/assets/audience-size.png)

* Pour les segments individuels, la taille de l’audience active et CPM (le cas échéant) s’affichent en regard du nom du segment.

  ![taille de segment individuelle](/help/dsp/assets/audience-size-segment.png)

* Vous pouvez afficher plus de détails sur un segment individuel ou une audience enregistrée, y compris la taille par navigateur, mobile, télévision connectée et partenaire de type ID universel. Pour les audiences enregistrées, la taille totale de l’audience active est le total dédupliqué.

  ![détails du segment individuel ou de l’audience enregistrée](/help/dsp/assets/audience-size-segment-details.png)

## Les vues Audiences

### La Vue Toutes Les Audiences

Dans la vue [!UICONTROL All Audiences], ou Bibliothèque d’audiences, vous pouvez enregistrer et gérer des audiences réutilisables, qui incluent des groupes de segments d’audience et même d’autres audiences enregistrées. Vous pouvez utiliser des audiences comme cibles à plusieurs emplacements. Le nombre d’emplacements dans lesquels chaque audience est utilisée est indiqué en regard du nom de l’emplacement.

Vous pouvez modifier, cloner, supprimer, exporter ou partager n’importe quelle audience.

### La Vue Segments

Dans la vue [!UICONTROL Segments], tous les utilisateurs peuvent créer des segments personnalisés supplémentaires.

La vue [!UICONTROL Segments] répertorie également les types de segment suivants :

* Tous les segments personnalisés créés par l’utilisateur ou l’utilisatrice sont disponibles.

  Vous pouvez afficher les balises de suivi de n’importe quel segment personnalisé que vous avez créé et partager ces segments avec d’autres utilisateurs. Vous pouvez également modifier ou supprimer les segments personnalisés que vous avez créés.

  Vous ne pouvez pas modifier ni partager des segments personnalisés que d’autres utilisateurs ont partagés avec vous.

* Tous les segments propriétaires importés en l’état qui sont disponibles pour l’utilisateur.

  Vous ne pouvez pas modifier ni partager des segments propriétaires qui ont été partagés avec vous. Contactez l’équipe chargée de votre compte Adobe si vous devez partager des segments propriétaires avec d’autres utilisateurs.

* Tous les segments tiers personnalisés disponibles pour l’utilisateur.

  Vous ne pouvez pas modifier ni partager des segments tiers qui ont été partagés avec vous. Contactez l’équipe chargée de votre compte Adobe si vous devez partager des segments tiers avec d’autres utilisateurs.

### La Vue Sources

Dans la vue [!UICONTROL Sources], vous pouvez configurer des sources pour les segments propriétaires dans les plateformes de données client prises en charge que vous souhaitez convertir en segments contenant des types d’identifiants universels spécifiés. Les paramètres source incluent une clé source générée automatiquement, que vous fournirez à votre plateforme de données client pour établir la connexion.

Pour plus d’informations sur les plateformes de données client prises en charge, les types d’ID universels pris en charge et les workflows pour configurer des connexions à chaque plateforme de données client, consultez la section « [À propos des sources](/help/dsp/audiences/sources/source-about.md) ».

Les segments traduits peuvent être inclus dans les audiences réutilisables et dans les paramètres d’emplacement pour le ciblage sans cookie.

>[!MORELIKETHIS]
>
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [Créer une audience réutilisable](reusable-audience-create.md)
>* [Créer et implémenter un segment personnalisé](custom-segment-create.md)
>* [Création et implémentation d’un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [À Propos Des Sources D’Audience Propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences Universal ID](/help/dsp/audiences/sources/source-manage.md)
>* [Importer manuellement des segments authentifiés depuis  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
