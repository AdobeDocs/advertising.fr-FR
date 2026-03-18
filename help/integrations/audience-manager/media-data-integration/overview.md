---
title: Présentation de l’envoi de données d’exposition aux médias DSP vers Adobe Audience Manager
description: Découvrez comment utiliser les pixels d’événement Audience Manager pour capturer des données au niveau de l’impression et du clic à partir de campagnes Advertising DSP
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: 7fa058da06edadf9b98aa49b0e5a1110ea68808c
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Présentation de l’envoi de données d’exposition aux médias DSP vers Adobe Audience Manager

*Annonceurs avec Advertising DSP uniquement*

*Publicitaires avec une intégration Adobe Advertising-Adobe Audience Manager uniquement*

Les clients Advertising DSP disposant de Adobe Audience Manager peuvent utiliser les pixels d’événement Audience Manager pour capturer des données au niveau de l’impression et des clics à partir de campagnes DSP. Les pixels d’événement envoient les données sous forme de signaux exploitables à Audience Manager. Ces signaux activent divers cas d’utilisation de DSP, tels qu’une segmentation plus avancée, la gestion des fréquences, l’analyse marketing et les informations sur les rapports.

DSP ne vous facture pas pour envoyer ces signaux à Audience Manager. Cependant, vous payez les coûts d’ingestion Audience Manager standard en fonction des appels au serveur, conformément à votre contrat Audience Manager. Audience Manager supprime les événements en double qui sont suivis de deux manières différentes, de sorte que chaque événement ne soit chargé qu’une seule fois.

>[!NOTE]
>
> Audience Manager prend également en charge la capture de données à partir des fichiers journaux du serveur de publicités, ce qui offre moins de flexibilité. Ce processus n’est pas abordé dans cette documentation.

## avantages du Principal

* Les données DSP campaign sont transmises à Audience Manager en temps réel et vous pouvez les utiliser pour créer des caractéristiques basées sur des règles que vous utilisez pour définir des segments.

* Les segments sont disponibles pour ciblage immédiatement après la qualification de la caractéristique de l’utilisateur et du segment, ce qui renforce les efforts de ciblage en temps réel.

* Vous pouvez exploiter les données de la campagne pour des cas d’utilisation tels que le capping de la fréquence pour les créatifs, le reciblage des utilisateurs exposés à des campagnes précédentes et l’analyse du comportement du site en aval et des points d’entrée.

* Les données agrégées fournissent une vue unifiée des performances de la campagne, permettent d’identifier les chemins de conversion personnalisés et peuvent être utilisées pour améliorer la séquence d’événements menant aux conversions par le biais d’Audience Manager [!DNL Audience Optimization Reports] ou d’une [[!DNL Audience Analytics] intégration à Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Suivi des données

Les pixels d’événement d’impression et de clic Audience Manager sont basés sur des cookies. Les pixels ne capturent pas les événements qui se produisent dans des environnements sans cookies, tels que les applications mobiles et la télévision connectée (CTV).<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### Pixels de suivi d’impression

Audience Manager effectue le suivi des données d’impression pour une publicité lorsque vous joignez un pixel de suivi d’événement transparent de 1 xl pixels à la publicité. Le pixel d’événement est chargé chaque fois que la publicité est diffusée à un utilisateur et chargée par le navigateur web. Le pixel est chargé à partir d’un sous-domaine spécifique au client de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), qui est un domaine hérité pour Audience Manager et qui contient des paramètres sous la forme de paires clé-valeur. L’appel d’événement collecte les données d’impression et de conversion et les envoie aux serveurs de collecte de données d’Audience Manager.

### pixels de suivi des clics

Audience Manager effectue le suivi des clics de la même manière que les impressions, sauf qu’il ne charge pas le pixel d’événement transparent chaque fois que la publicité est diffusée. Au lieu de cela, les données relatives aux clics sont suivies dans l’URL de clics publicitaires. La publicité pointe vers un sous-domaine spécifique au client de [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), qui est un domaine hérité pour Audience Manager, pour traitement par les serveurs de collecte de données Audience Manager. Le serveur redirige ensuite l’utilisateur vers la page de destination prévue. L’URL contient des paramètres en tant que paires clé-valeur.

>[!NOTE]
>
>Si votre entreprise utilise le suivi des clics [!DNL Analytics], vous n’aurez peut-être pas besoin du suivi des clics Audience Manager. Adobe Analytics capture les signaux de clic et peut les envoyer à Audience Manager par le biais du [&#x200B; transfert côté serveur &#x200B;](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Collectez les données de clics et d’impressions des campagnes Advertising DSP](collect.md)
>* [Cas pratiques](use-cases.md)
