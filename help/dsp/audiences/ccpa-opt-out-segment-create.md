---
title: Création et implémentation d’un segment d’opt-out de vente du CCPA
description: Découvrez comment créer et mettre en oeuvre un segment pour effectuer le suivi des identifiants d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# Création et implémentation d’un segment d’opt-out de vente du CCPA

Vous pouvez créer un segment pour effectuer le suivi des ID d’utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, en vertu du California Consumer Privacy Act (CCPA). Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente des informations personnelles du CCPA.

Une fois la balise de pixel de segment implémentée, Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

>[!NOTE]
>
>* Pour plus d’informations sur la manière de communiquer les demandes d’opposition à la vente des informations personnelles à Adobe Advertising à l’aide de l’API Adobe Experience Platform Privacy Service, voir [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Pour effectuer le suivi des utilisateurs qui visitent des pages web à des fins non liées au suivi des événements d’opposition à la vente des informations personnelles (CCPA), ainsi que des utilisateurs exposés aux publicités provenant d’appareils de bureau, mobiles et CTV, créez un [segment personnalisé](/help/dsp/audiences/custom-segment-create.md).

1. Créez le segment :

   1. Dans le menu principal, cliquez sur **Audiences > Segments**.

   1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Saisissez un **[!UICONTROL Segment Name]** unique.

      Nom de segment recommandé : &quot;&lt;*Votre nom d’annonceur*> - Droit d’opposition (opt-out) à la vente (CCPA)&quot; (par exemple &quot;Acme - CCPA - Droit d’opposition à la vente&quot;)

   1. Pour le [!UICONTROL Segment Type], sélectionnez **[!UICONTROL CCPA Opt-out of sale]**.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Copiez et implémentez une balise pixel pour effectuer le suivi du segment :

   1. Revenez à **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Dans la ligne de segment, placez le curseur sur le nouveau segment et cliquez sur **[!UICONTROL Get pixel]**.

   1. Copiez le pixel de l’image (commençant par `<img src="https://rtd-tm.everesttech.net"`) pour collecter les identifiants utilisateur des visiteurs de bureau et mobiles dans une page web.

   1. Fournissez la balise au contact de l’annonceur ou du site web pour le déploiement à l’aide du mécanisme utilisé par l’entreprise pour suivre les demandes d’opposition à la vente des informations personnelles (telles que l’utilisation d’une plateforme de gestion du consentement) de la CCPA.

      Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement de la balise ou d’être informé de ce déploiement.

      Une fois le pixel implémenté, l’Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

      Bien que la logique et le choix de l’implémentation dépendent de l’annonceur, voici un exemple de la manière dont un annonceur peut déclencher le pixel :

      1. Un consommateur arrive sur la page d&#39;accueil de l&#39;annonceur.
      1. Le consommateur trouve et clique sur le bouton &quot;Option de désinscription (opt-out) du CCPA&quot; de l’annonceur.
      1. Le consommateur reçoit une liste des prestataires avec lesquels l&#39;annonceur travaille.
      1. Le consommateur coche la case pour refuser de vendre des données à Adobe Advertising.

         Cette action déclenche le déclenchement du pixel et la collecte de l’ID de cookie du consommateur dans le segment &quot;[!UICONTROL CCPA Opt-out of sale]&quot; spécifié.

>[!MORELIKETHIS]
>
>* [Prise en charge des Adobes Advertising pour le California Consumer Privacy Act : prise en charge de l’exclusion des consommateurs](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [À propos de [!UICONTROL CCPA Opt-out-of-Sale] segments et rapports](ccpa-opt-out-about.md)
>* [Récupérer les rapports d’exclusion de la vente pour les consommateurs](ccpa-opt-out-segment-report-retrieve.md)
>* [Créer et implémenter un segment personnalisé](custom-segment-create.md)
>* [À propos de la gestion de l’audience](audience-about.md)
