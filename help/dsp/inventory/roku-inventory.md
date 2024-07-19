---
title: Utilisation de [!DNL Roku] Inventaire
description: Découvrez DSP partenariat avec [!DNL Roku], y compris les options d’inventaire, les fournisseurs de suivi tiers approuvés et les bonnes pratiques pour les emplacements spécifiques à  [!DNL Roku].
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: e7a1aa80-d7f0-4a4e-96b1-6b362a32106e
source-git-commit: f3099c84fe2d6b1610ddf4ca07d59b119718afee
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# Utilisation de l’inventaire [!DNL Roku]

Advertising DSP fournit des fonctionnalités pour la publicité sur [!DNL Roku].

## Correspondance d’audiences

Le partenariat [!DNL Roku] et DSP associe vos audiences [!DNL DSP] à [!DNL Roku] ID pour le ciblage d’audience déterministe 1:1 sur l’inventaire [!DNL Roku].

## [!DNL Roku] Options d’inventaire

Vous pouvez : a) configurer des ID d’opération privés directement avec [!DNL Roku], puis saisir les données d’ID d’opération dans DSP ou b) accéder à la galerie [!DNL On Demand] pour vous abonner aux profils [!DNL Roku] :

>[!NOTE]
>
>L’inventaire [!DNL Roku] n’est pas disponible sur les marchés et les exchanges ouverts.

* Pour vos offres privées, [ configurez les informations sur les ID d’opération dans DSP](/help/dsp/inventory/deal-id-create.md), puis ciblez &quot;[!UICONTROL Roku Network - Audience]&quot; et &quot;[!UICONTROL The Roku Channel - Audience]&quot; dans [!DNL Roku] emplacements.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Vous pouvez [vous abonner à l’inventaire  [!DNL Roku]  suivant dans la  [!DNL On Demand] Galerie](/help/dsp/inventory/on-demand-inventory-subscribe.md), puis cibler toutes les offres approuvées dans [!DNL Roku] emplacements :

   * &quot;[!UICONTROL Roku Network - Audience]&quot; pour l’inventaire dans l’écosystème [!DNL Roku] avec des partenaires de contenu de qualité, tels que [!DNL The CW], [!DNL ABC] et [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel - Audience]&quot; pour le contenu de l’application [!DNL Roku] détenu et exploité (O&amp;O).

### Avantages de la personnalisation des marchés privés avec [!DNL Roku]

Les offres privées vous permettent de personnaliser les paramètres de l’opération en fonction de vos besoins.

* **Prix négocié :** Collaborez avec l’équipe commerciale de [!DNL Roku] pour négocier et structurer un contrat qui répond aux besoins de votre campagne.

* **Priorité d’échelle :** les marchés privés (PMP) reçoivent une priorité plus élevée que les offres toujours actives (telles que [!DNL On Demand] ).

* **Gestion des fréquences :** La fréquence par défaut de [!DNL Roku] est d’une (1) et par 30 minutes par utilisateur, mais vous pouvez personnaliser la fréquence par heure, jour, semaine, mois ou période de vol complète.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Ciblage de données :** [!DNL Roku] les audiences sont créées à partir de [!DNL Roku] signaux d’appareil et de télévision, de données suivies par [!DNL The Roku Channel] (telles que l’affinité du genre TV, le comportement de la télévision en continu et l’état d’abonnement au câble), ainsi que de données supplémentaires provenant du système de gestion de la relation client (CRM) [!DNL Roku].

* **[!DNL Roku]Ciblage de contenu :** les offres privées peuvent cibler les applications par genre, application de la liste bloquée de l’application, événements saisonniers et de tentpôle, et les programmes dans [!DNL The Roku Channel] uniquement.

## [!DNL Roku] Emplacements

Dans DSP campagnes, [créez [!DNL Roku] emplacements spécifiques](/help/dsp/campaign-management/placements/placement-create.md) à l’aide du type d’emplacement &quot;[!UICONTROL Connected TV (Roku)]&quot;. Incluez [!DNL Roku] emplacements dans des modules spécifiques [!DNL Roku] avec des objectifs définis.

Chaque emplacement [!DNL Roku] doit cibler au moins une transaction ou une source [!DNL Roku]. Pour utiliser la correspondance d’audience de DSP avec [!DNL Roku], incluez un ou plusieurs segments d’audience pouvant être mis en correspondance avec le jeu de données déterministe [!DNL Roku] (inclus).

### [!DNL Roku] - Fournisseurs de suivi tiers approuvés

[!DNL Roku] emplacements peuvent inclure des pixels d’événement tiers et des pixels de conversion provenant des fournisseurs suivants : [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk] et [!DNL Research Now].

### Bonnes pratiques par stratégie de placement

Voici les pratiques recommandées pour les emplacements spécifiques à [!DNL Roku].

Pour optimiser la portée incrémentielle :

* Supprimez les audiences exposées sur [!DNL Roku O&O] en excluant les audiences que vous avez déjà atteintes à l’aide de [!DNL The Roku Channel].

* Supprimez les audiences exposées sur [!DNL All Roku] en excluant les audiences que vous avez déjà atteintes sur la plateforme [!DNL Roku].

Pour la configuration la plus rapide :

* Ciblez les offres existantes et toujours actives pour [!DNL The Roku Channel] dans [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) afin d’accéder rapidement à l’inventaire [!DNL Roku] détenu et exploité.
* Ciblez les offres existantes et toujours actives pour [!DNL Roku Network] dans [[!DNL On Demand] Inventory](/help/dsp/inventory/on-demand-inventory-subscribe.md) afin d’atteindre rapidement une échelle sur la plateforme [!DNL Roku].

Pour une échelle maximale :

* Personnalisez un marché privé [!DNL Roku] pour accéder en priorité à l’offre [!DNL Roku] à un prix négocié.

>[!MORELIKETHIS]
>
>* [Créer manuellement des détails sur l’identifiant de transaction](/help/dsp/inventory/deal-id-create.md)
> * [Abonner et demander l’accès à [!DNL On Demand] Premium Offres d’inventaire](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Créer un emplacement](/help/dsp/campaign-management/placements/placement-create.md)
