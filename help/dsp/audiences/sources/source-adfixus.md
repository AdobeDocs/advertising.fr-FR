---
title: Importez les segments propriétaires depuis  [!DNL AdFixus]
description: 'Découvrez comment importer dans DSP vos segments propriétaires constitués  [!DNL AdFixus] ’identifiants universels [!DNL AdFixus] '
feature: DSP Audiences
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 0%

---

# Importer des segments propriétaires depuis [!DNL AdFixus]

*Applicable aux annonceurs en Australie uniquement*

Utilisez l’intégration d’Advertising DSP à [!DNL AdFixus] pour importer vos identifiants universels [!DNL AdFixus] avec des mappages de segments pour la publicité ciblée. [!DNL AdFixus] Les identifiants sont disponibles uniquement en Australie. DSP ne modifie pas les ID [!DNL AdFixus] en d’autres types d’ID et ne convertit pas les autres types d’ID en ID [!DNL AdFixus]. DSP ne facture pas de frais pour l’importation des identifiants.

Une fois que vous avez importé vos segments [!DNL AdFixus] dans DSP, vous pouvez cibler les emplacements sur des identifiants [!DNL AdFixus] et sur des segments propriétaires spécifiques depuis [!DNL AdFixus]. Vous pouvez également ajouter des segments [!DNL AdFixus] aux audiences réutilisables. Les détails de tout segment incluent le nombre d’identifiants de [!DNL AdFixus] applicables.

Vous pouvez afficher l’impression, le clic, la fréquence et d’autres mesures pour les utilisateurs disposant d’identifiants [!DNL AdFixus] dans les rapports personnalisés. Les annonceurs avec [!DNL Analytics for Advertising] peuvent également afficher les données d’affichage publicitaire pour les identifiants [!DNL AdFixus] d’Adobe Analytics, ainsi que les données d’Adobe Analytics dans DSP.

1. Utilisez des [!DNL AdFixus] pour convertir les données propriétaires de votre organisation en segments avec des identifiants [!DNL AdFixus].

   Pour ce faire, un compte distinct avec [!DNL AdFixus] et une clé de licence active est nécessaire. Vous devez également implémenter du code spécifique à [!DNL AdFixus] pour les propriétés et domaines de votre site web. Utiliser directement les [!DNL AdFixus] pour générer des segments avec des identifiants.

1. (Annonceurs avec [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)) Configurez le suivi pour la mesure des [!DNL Analytics] :

   1. (Si vous ne l’avez pas déjà fait) Remplissez toutes les [conditions préalables à l’implémentation [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) ainsi que l’[AMO ID et l’EF ID dans vos URL de tracking](/help/integrations/analytics/ids.md).

   1. Déployez du code spécifique à [!DNL AdFixus] sur vos pages web pour faire correspondre les conversions à partir des identifiants [!DNL AdFixus] sur les navigateurs web de bureau et mobiles (mais pas sur les applications mobiles) aux affichages publicitaires.

1. Importez vos segments de [!DNL AdFixus] propriétaires :

   1. [Créez une source d’audience](source-manage.md) de [!UICONTROL Type] **[!UICONTROL AdFixus ID]**. Vous devez accepter les conditions générales du contrat de service.

      Les paramètres source incluent une clé source générée automatiquement.

   1. Partagez la clé source avec votre équipe [!DNL AdFixus] afin qu’elle puisse diffuser les segments requis vers DSP.

1. Vérifiez dans la section [!UICONTROL First Party Segments] de votre bibliothèque d’audiences (disponible lorsque vous créez ou modifiez une audience à partir de [!UICONTROL Audiences] > [!UICONTROL All Audiences] ou dans les paramètres d’emplacement) que le segment est renseigné. Comparez le nombre d’identifiants de [!DNL AdFixus] au nombre d’identifiants d’utilisateur dans [!DNL AdFixus].

   Les segments sont disponibles dans DSP dès leur création.

Les segments sont actualisés et disponibles pour le ciblage toutes les trois heures, bien que le nombre indiqué dans DSP soit actualisé toutes les 24 heures. **Remarque :** l’inclusion dans un segment expire après une période d’expiration spécifiée, que vous configurez dans [!DNL AdFixus]. Actualisez vos segments en les poussant à nouveau depuis [!DNL AdFixus] avant l’expiration.

>[!MORELIKETHIS]
>
>* [À propos des sources d’audience propriétaires](/help/dsp/audiences/sources/source-about.md)
>* [Gérer les sources d’audience pour activer les audiences d’ID universel](source-manage.md)
>* [Connexion &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=fr)
>* Adobe Experience Platform [Présentation du catalogue des destinations](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html?lang=fr)
>* [Prise en charge de l’activation des identifiants universels](/help/dsp/audiences/universal-ids.md)
>* [À propos de la gestion des audiences](/help/dsp/audiences/audience-about.md)
