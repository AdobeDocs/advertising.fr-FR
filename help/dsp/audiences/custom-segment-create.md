---
title: Création et implémentation d’un segment personnalisé
description: Découvrez comment créer et mettre en oeuvre un segment personnalisé pour effectuer le suivi des utilisateurs exposés aux publicités ou des utilisateurs qui visitent vos pages web.
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 2fe54fbcd9711e714246f074ede086910b538b80
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# Création et implémentation d’un segment personnalisé

Vous pouvez collecter vos propres données d’audience propriétaires en créant et en implémentant un segment DSP personnalisé. Vous pouvez utiliser ce segment pour effectuer le suivi a) des utilisateurs exposés aux publicités provenant d’ordinateurs de bureau et de périphériques mobiles et b) des utilisateurs qui visitent des pages web spécifiques. Vous pouvez ensuite recibler les utilisateurs du segment avec des publicités supplémentaires ou empêcher les utilisateurs du segment de recevoir des publicités supplémentaires.

>[!NOTE]
>
>Pour effectuer le suivi des ID d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, en vertu de la California Consumer Privacy Act (CCPA), créez une [Segment d’exclusion de la vente du CCPA](ccpa-opt-out-segment-create.md).

## Conditions préalables pour les segments permettant d’effectuer le suivi des ID5

*Fonction bêta*

* Avant de générer un segment pour effectuer le suivi des utilisateurs associés aux ID 5, vous devez signer un accord avec [!DNL ID5] et obtenir l’ID de partenaire de votre entreprise. Contactez votre équipe de compte d’Adobe pour obtenir des instructions.

* Pour la mesure dans Adobe Analytics, vous devez :

   1. Compléter tout [conditions préalables à la mise en oeuvre [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md), et assurez-vous que la variable [AMO ID et EF ID](/help/integrations/analytics/ids.md) sont renseignées dans vos URL de suivi.

   1. Ajoutez le paramètre suivant à vos pages web avant ou dans la variable [Code JavaScript requis pour [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md) — n’importe où avant l’initialisation du dernier service d’événement.

      ```window.id5PartnerId=Your_ID5_PartnerID;```

      Exemple :

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

   1. Utilisez n’importe quel outil de débogage de navigateur pour vérifier que chaque appel est lancé vers le domaine. `lasteventf-tm.everesttech.net` et contient le paramètre `_les_id5` avec un ID5 crypté comme valeur.

## Création et implémentation d’un segment personnalisé

1. Créez le segment :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Saisissez une variable **[!UICONTROL Segment Name]**.

   1. Pour le **[!UICONTROL Segment Type]**, sélectionnez *[!UICONTROL Custom]*.

   1. Saisissez le **[!UICONTROL Lookback Window]**: nombre de jours pendant lesquels le cookie d’un utilisateur reste dans le segment.

      La fenêtre par défaut est de 45 jours. Saisissez une valeur comprise entre 1 (1) et 365.

   1. Cliquez sur **[!UICONTROL Advanced]** pour développer les paramètres avancés, puis sélectionnez les types d’identifiants utilisateur suivis par la balise de segment :

      * *[!UICONTROL Cookies]:* (Par défaut) La balise de segment effectue le suivi des cookies.

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* La balise de segment effectue le suivi [!DNL ID5] ID. Les impressions diffusées aux identifiants universels n’engendrent aucuns frais.

        **[!UICONTROL Terms of Service]:** Les conditions d’utilisation des identifiants universels. Vous ou un autre utilisateur du compte DSP devez accepter les termes une fois avant de pouvoir utiliser des identifiants universels pour un nouveau type d’identifiant. Pour les clients disposant de contrats de service géré, votre équipe de compte d’Adobe obtiendra votre consentement et acceptera les conditions pour le compte de votre organisation. Pour lire les termes, cliquez sur **>**. Pour accepter les termes, faites défiler l’écran jusqu’au bas des termes et cliquez sur **[!UICONTROL Accept]**.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Copiez et implémentez des balises pour effectuer le suivi du segment, selon les besoins :

   1. Revenir à **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Placez le curseur sur la ligne de segment et cliquez sur **[!UICONTROL Get Pixel]**.

      * Pour effectuer le suivi des visiteurs de bureau et mobiles sur une page web :

         1. Copiez la balise de suivi des pages vues, étiquetée &quot;[!UICONTROL Desktop or mobile websites].&quot;

         1. (Balises pour les segments qui effectuent le suivi [!DNL ID5] ID) Dans la balise copiée, remplacez `ID5_PARTNER_ID` avec l’identifiant du partenaire qui [!DNL ID5] affectée à votre organisation.

            Par exemple, si l’ID de partenaire ID5 est `abcde` et la balise de segment générée est

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            replace `ID5_PARTNER_ID` avec `abcde` dans la balise pour obtenir ce qui suit :

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            Votre entreprise a reçu l’identifiant du partenaire lorsqu’elle a signé un accord avec [!DNL ID5]. Si vous ne connaissez pas votre identifiant de partenaire, contactez votre équipe de compte d’Adobe.

            Cette étape n’est pas nécessaire pour le suivi des balises. [!DNL ID5] Identifiants pour les utilisateurs exposés à une unité publicitaire sur un ordinateur de bureau ou des appareils mobiles.

         1. Fournissez la balise au contact de l’annonceur ou du site web pour le déploiement.

            Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement de la balise ou d’être informé de ce déploiement.

      * Pour effectuer le suivi des utilisateurs exposés à une unité publicitaire sur un ordinateur de bureau ou sur des appareils mobiles :

         1. Copiez la balise de suivi d’impression, étiquetée &quot;[!UICONTROL Desktop or mobile ads].&quot;

         1. Ajoutez la balise à l’une des options suivantes : [!UICONTROL Pixel] pour chaque publicité appropriée ou au [!UICONTROL Event Pixels] de la [[!UICONTROL Tracking] paramètres pour chaque emplacement approprié](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

Une fois qu’une balise de suivi est implémentée, vous pouvez utiliser le segment dans les cibles ou exclusions d’audience pour n’importe quel emplacement.

>[!TIP]
>
>Suivez la taille du segment lorsque les utilisateurs sont suivis.

>[!MORELIKETHIS]
>
>* [Gestion de l’audience](audience-about.md)
>* [Modifier les informations sur le segment](segment-edit.md)
>* [Suppression d’un segment](segment-delete.md)
>* [Affichage des pixels de suivi pour un segment](segment-view-pixels.md)
>* [Partage ou arrêt du partage d’un segment](segment-share.md)
>* [Créez et implémentez une [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Création d’une audience réutilisable](reusable-audience-create.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
