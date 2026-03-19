---
title: Création et implémentation d’un segment personnalisé
description: Découvrez comment créer et implémenter un segment personnalisé pour effectuer le suivi des utilisateurs exposés aux publicités ou des utilisateurs qui visitent vos pages web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: f58e478ea2c1397b15c667c1415a7038b6ea5e5b
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# Création et implémentation d’un segment personnalisé

Vous pouvez collecter vos propres données d’audience propriétaires en créant et en implémentant un segment DSP personnalisé. Vous pouvez utiliser le segment pour effectuer le suivi a) des utilisateurs exposés aux publicités des ordinateurs de bureau et des appareils mobiles et b) des utilisateurs qui visitent des pages web spécifiques. Vous pouvez par la suite recibler les utilisateurs du segment avec des annonces supplémentaires ou empêcher les utilisateurs du segment de recevoir des annonces supplémentaires.

>[!NOTE]
>
>Pour suivre les ID des utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, conformément à la Loi sur la protection de la vie privée des consommateurs de Californie (CCPA), créez un [segment d’opposition à la vente de la CCPA](ccpa-opt-out-segment-create.md).

## Conditions préalables pour que les segments effectuent le suivi des ID5

*Fonction Beta*

* Avant de générer un segment pour suivre les utilisateurs associés aux ID5, signez un accord avec [!DNL ID5] et obtenez l’ID de partenaire de votre organisation. Pour obtenir des instructions, contactez l’équipe chargée de votre compte Adobe.

* Pour les mesures dans Adobe Analytics, vous devez :

   1. Renseignez tous les [prérequis pour l’implémentation [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) et assurez-vous que les [ID AMO et ID EF](/help/integrations/analytics/ids.md) sont renseignés dans vos URL de tracking.

   1. Ajoutez le paramètre suivant à vos pages web avant ou pendant le code [JavaScript requis pour  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) — n’importe où avant l’initialisation du dernier service d’événement.

      ```window.id5PartnerId=ID5_PartnerID;```

      Exemple :

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

      Consultez les sections « [Format des balises de suivi de conversion JavaScript version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md) » et « [Format des balises de suivi de conversion JavaScript version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md) » pour connaître le format complet des balises.

   1. Utilisez n’importe quel outil de débogage du navigateur pour vérifier que chaque appel est initié au domaine `lasteventf-tm.everesttech.net` et contient le paramètre `_les_id5` avec un ID5 chiffré comme valeur.

## Création et implémentation d’un segment personnalisé

1. Créez le segment :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Saisissez un **[!UICONTROL Segment Name]** unique.

   1. Pour le **[!UICONTROL Segment Type]**, sélectionnez *[!UICONTROL Custom]*.

   1. Saisissez le **[!UICONTROL Lookback Window]**, qui correspond au nombre de jours pendant lesquels le cookie d’un utilisateur reste dans le segment.

      La fenêtre par défaut est de 45 jours. Entrez une valeur comprise entre 1 et 365.

   1. Cliquez sur **[!UICONTROL Advanced]** pour développer les paramètres avancés, puis sélectionnez les types d’identifiants d’utilisateur suivis par la balise de segment :

      * *[!UICONTROL Cookies]:* (valeur par défaut) La balise de segment effectue le suivi des cookies.

      * [!UICONTROL Universal IDs (Beta)] :

         * *[!UICONTROL ID5]:* La balise de segment effectue le suivi des identifiants de [!DNL ID5]. Aucun frais n’est encouru pour les impressions diffusées aux identifiants universels.

        **[!UICONTROL Terms of Service]:** Conditions générales de service relatives à l’utilisation des ID universels. Vous ou un autre utilisateur du compte DSP devez accepter les conditions une seule fois avant de pouvoir utiliser les identifiants universels pour un nouveau type d’identifiant. Pour les clients qui disposent de contrats de service géré, l’équipe chargée de votre compte Adobe obtiendra votre consentement et acceptera les conditions au nom de votre entreprise. Pour lire les termes, cliquez sur **>**. Pour accepter les conditions, faites défiler l’écran jusqu’au bas des conditions et cliquez sur **[!UICONTROL Accept]**.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Copiez et implémentez des balises pour suivre le segment, si nécessaire :

   1. Revenez à **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Placez le curseur sur la ligne de segment et cliquez sur **[!UICONTROL Get Pixel]**.

      * Pour effectuer le suivi des visiteurs sur poste de travail et mobile sur une page web :

         1. Copiez la balise de suivi des pages vues intitulée « [!UICONTROL Desktop or mobile websites] ».

         1. (Balises pour les segments qui effectuent le suivi des ID de [!DNL ID5]) Dans la balise copiée, remplacez `ID5_PARTNER_ID` par l’ID de partenaire qui [!DNL ID5] affecté à votre organisation.

            Par exemple, si votre ID de partenaire ID5 est `abcde` et que la balise de segment générée est

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            remplacez ensuite `ID5_PARTNER_ID` par `abcde` dans la balise pour obtenir les éléments suivants :

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Votre organisation a reçu l’ID de partenaire lorsqu’elle a signé un accord avec [!DNL ID5]. Si vous ne connaissez pas votre ID de partenaire, contactez l’équipe chargée de votre compte Adobe.

            Cette étape n’est pas nécessaire pour que les balises effectuent le suivi des identifiants [!DNL ID5] pour les utilisateurs exposés à une annonce publicitaire sur des ordinateurs de bureau ou des appareils mobiles.

         1. Fournissez la balise à l’annonceur ou au contact du site web pour le déploiement.

            Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé de celui-ci.

      * Pour suivre les utilisateurs exposés à une annonce publicitaire sur des ordinateurs de bureau ou des appareils mobiles :

         1. Copiez la balise de suivi d’impression, qui est intitulée « [!UICONTROL Desktop or mobile ads] ».

         1. Ajoutez la balise à l’onglet [!UICONTROL Pixel] pour chaque annonce publicitaire pertinente ou à la section [!UICONTROL Event Pixels] des paramètres [[!UICONTROL Tracking] pour chaque emplacement pertinent](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Une fois qu’une balise de tracking est implémentée, vous pouvez utiliser le segment dans les cibles ou exclusions d’audience pour n’importe quel emplacement.

>[!TIP]
>
>Effectuez le suivi de la taille du segment à mesure que les utilisateurs sont suivis.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des audiences](audience-about.md)
>* [Modifier les informations sur le segment](segment-edit.md)
>* [Supprimer un segment](segment-delete.md)
>* [Affichage des pixels de suivi pour un segment](segment-view-pixels.md)
>* [Partager ou arrêter le partage d’un segment](segment-share.md)
>* [Création et implémentation d’un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Créer une audience réutilisable](reusable-audience-create.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
