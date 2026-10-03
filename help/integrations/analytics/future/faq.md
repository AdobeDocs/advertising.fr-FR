---
title: Questions fréquentes
description: xxx
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%
---
# Questions fréquentes xxx

## titre

https://adobeadcloud.zendesk.com/agent/tickets/14214
Par défaut, Adobe Analytics signale tous les événements capturés dans chaque rapport. Les événements « [!UICONTROL Unspecified] » représentent des événements de fin de formulaire qui n’étaient pas connectés à Adobe Advertising. Par exemple, dans le rapport Ad Platform, les conversions organiques ou les conversions pilotées par une campagne par e-mail tombent dans la catégorie « non spécifié ».

Vous pouvez utiliser le filtre pour supprimer les événements non spécifiés des rapports en supprimant la coche de l’option « Inclure non spécifié (aucun) ». <!-- Not sure if this is in DSP or in Analytics Workspace -->

## titre

https://adobeadcloud.zendesk.com/agent/tickets/24323
Placez les balises d’événement Analytics aux mêmes endroits que les pixels Ad Cloud pour vous assurer que XXX correspond.

## titre

https://adobeadcloud.zendesk.com/agent/tickets/24323

Q : Lors de notre audit de sécurité interne, certaines fonctionnalités ont été signalées comme problème de sécurité que nous avons activé lorsque nous avons intégré Ad Cloud à notre installation Adobe Analytics existante.

L’intégration en question se fait entre AdCloud et Adobe Audience Manager. Cette fonctionnalité augmente le taux de correspondance de l’identifiant visiteur entre AdCloud et Adobe Audience Manager. Pour ce faire, il envoie des requêtes réseau à pagead.l.doubleclick.net, star-mini.c10r.facebook.com et pug88000nf.pubmatic.com afin de déterminer si ces services disposent d’un identifiant existant pour le visiteur qui peut être utilisé. Il s’agit des requêtes réseau qui ont été signalées comme risque de sécurité et qui se produisent pour tous les visiteurs du site.

Notre vérificateur nous demande de désactiver cette fonctionnalité. Que se passe-t-il si nous bloquons ces requêtes réseau ?

R : Nous avons vérifié auprès de notre produit et ils ont mentionné que les pixels en question ont pour but d’augmenter les taux de correspondance des cookies entre Ad Cloud, les partenaires d’inventaire/de fournisseur de services partagés spécifiques (par rapport à DSP) et AAM.  S’ils sont supprimés, le client peut constater un certain niveau de diminution du taux de correspondance entre AAC/AAM et les partenaires d’inventaire auxquels les pixels respectifs sont destinés, mais il ne s’attend pas à ce qu’il soit important.

Pour la recherche Ad Cloud, nous voyons que l’ID d’organisation CX Enterprise de l’annonceur est configuré pour Mathworks, mais notre équipe de produits ne voit pas la configuration de Mathworks pour activer les audiences dans Ad Cloud. Utilisez-vous Adobe Audience Manager pour envoyer des audiences vers Ad Cloud Search ? Dans le cas contraire, leur suppression n’aura aucun impact sur le workflow actuel. L’assistance clientèle d’AAM peut vous aider à supprimer ces pixels si vous ne souhaitez pas qu’ils soient déclenchés.

