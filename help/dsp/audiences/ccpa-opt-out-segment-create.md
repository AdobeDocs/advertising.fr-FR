---
title: Créer et mettre en œuvre un segment d’opposition à la vente du CCPA
description: Découvrez comment créer et implémenter un segment pour effectuer le suivi des identifiants d’utilisateurs à partir des requêtes d’opposition à la vente des consommateurs.
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
TQID: https://experienceleague.adobe.com/NYXgnUkEw4uSilL8LO8qlRPp5AVAjXeXNS0pVeIZl3Y
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: c193c532-b70e-4556-bde7-857186cbe140
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# Créer et mettre en œuvre un segment d’opposition à la vente du CCPA

Vous pouvez créer un segment pour effectuer le suivi des identifiants des utilisateurs à partir des demandes d’opposition à la vente des consommateurs sur votre site web, conformément à la Loi sur la protection de la vie privée des consommateurs de Californie (CCPA). Les utilisateurs restent indéfiniment dans les segments d’opposition à la vente du CCPA.

Une fois la balise de pixel de segment implémentée, Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

>[!NOTE]
>
>* Pour plus d’informations sur la manière de communiquer les requêtes de désinscription de la CCPA à Adobe Advertising à l’aide de l’API Adobe Experience Platform Privacy Service, consultez [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* Pour suivre les utilisateurs qui visitent des pages web à des fins non liées au suivi des événements d’opposition à la vente du CCPA, ainsi que les utilisateurs exposés à des publicités provenant d’appareils de bureau, mobiles et de télévision, créez un [segment personnalisé](/help/dsp/audiences/custom-segment-create.md).

1. Créez le segment :

   1. Dans le menu principal, cliquez sur **Audiences > Segments**.

   1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

   1. Saisissez un **[!UICONTROL Segment Name]** unique.

      Nom de segment recommandé : « *Nom de votre annonceur*> - CCPA Opt-out of Sale » (par exemple, « Acme - CCPA Opt-out of Sale »)

   1. Pour le [!UICONTROL Segment Type], sélectionnez **[!UICONTROL CCPA Opt-out of sale]**.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Copiez et implémentez une balise pixel pour suivre le segment :

   1. Revenez à **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. Dans la ligne de segment, placez le curseur sur le nouveau segment et cliquez sur **[!UICONTROL Get pixel]**.

   1. Copiez le pixel de l’image (en commençant par `<img src="https://rtd-tm.everesttech.net"`) pour collecter les identifiants des visiteurs ordinateurs de bureau et mobiles dans une page web.

   1. Fournissez la balise à l’annonceur ou au contact du site web pour déploiement à l’aide du mécanisme utilisé par l’entreprise pour suivre les demandes d’opposition à la vente du CCPA (par exemple l’utilisation d’une plateforme de gestion du consentement).

      Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé de celui-ci.

      Une fois le pixel implémenté, Adobe Advertising commence à collecter un pool d’identifiants pour le compte de l’annonceur.

      Bien que le choix et la logique de l’implémentation dépendent de l’annonceur, voici un exemple de la manière dont un annonceur peut déclencher le pixel :

      1. Un consommateur arrive sur la page d’accueil de l’annonceur.
      1. Le consommateur trouve et clique sur le bouton « Désinscription de la vente du CCPA » de l’annonceur.
      1. Le consommateur reçoit une liste des fournisseurs de services avec lesquels l&#39;annonceur travaille.
      1. Le client coche la case pour refuser de vendre des données à Adobe Advertising.

         Cette action déclenche le déclenchement du pixel et la collecte de l’ID de cookie du client dans le segment « [!UICONTROL CCPA Opt-out of sale] » spécifié.

>[!MORELIKETHIS]
>
>* [Prise en charge par Adobe Advertising de la Loi sur la confidentialité des consommateurs de Californie : prise en charge du droit d’opposition des consommateurs](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [À propos [!UICONTROL CCPA Opt-out-of-Sale] segments et des rapports](ccpa-opt-out-about.md)
>* [Récupérer les rapports d’opposition à la vente des clients](ccpa-opt-out-segment-report-retrieve.md)
>* [Créer et implémenter un segment personnalisé](custom-segment-create.md)
>* [À propos de la gestion des audiences](audience-about.md)
