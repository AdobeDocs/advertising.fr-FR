---
title: Principes fondamentaux de  [!DNL Marketing Channels]
description: Découvrez les informations clés sur  [!DNL Analytics Marketing Channels]  que les utilisateurs et  [!DNL Analytics for Advertising]  utilisatrices doivent comprendre.
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: e0436d3840fc138bad6ee3e3599cffd2385750cd
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Principes fondamentaux de la [!DNL Analytics Marketing Channels]

Cette page fournit des informations clés sur les [!DNL Analytics Marketing Channels] que [!DNL Analytics for Advertising] utilisateurs doivent comprendre.

Pour obtenir une documentation complète sur les [!DNL Marketing Channels], voir « [Prise en main de  [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html?lang=fr) ».

## Présentation de [!DNL Marketing Channels]

[!DNL Marketing Channels] sont des fonctionnalités essentielles d’Adobe Analytics. [!DNL Marketing Channels] rapports montrent comment les clients accèdent à votre site web par la fenêtre de création de rapports et comment chaque canal affecte le chiffre d’affaires ou le comportement sur site.

Prenons l’exemple suivant d’un parcours de visites croisées. Chaque visite de votre site web est indiquée par le canal marketing à partir duquel le visiteur a rejoint le site. La première visite, également appelée canal Première touche, est l’e-mail. L’affichage lors de la deuxième visite est un canal participant, et la recherche naturelle est considérée comme le canal Dernière touche. Si vous utilisez [!UICONTROL Last Touch Attribution] dans [!UICONTROL Attribution IQ], Recherche naturelle recevra un crédit complet pour l’événement de conversion de 250 $. À l’aide du service Experience Cloud ID, vous pouvez lier ces visites individuelles afin d’afficher un parcours par un seul visiteur.

![Exemple de parcours de conversion entre visites dans les canaux marketing](/help/integrations/assets/a4adc-mc-sample-journey.png)

En utilisant des règles de traitement [!UICONTROL Marketing Channels], vous pouvez créer des ensembles de logiques pour déterminer les canaux qui génèrent le trafic et pour suivre chaque canal au fur et à mesure que les utilisateurs et utilisatrices accèdent à votre site. Par exemple, le canal [!UICONTROL Email] serait indiqué par un code de suivi unique généré lors des clics qui, une fois enregistré par Adobe Analytics, catégoriserait la visite comme provenant d’une campagne marketing par e-mail.

## Règles de traitement et définition des canaux marketing

Chaque fois qu’un utilisateur ou une utilisatrice accède à un site web, il ou elle le fait par le biais d’une URL sur laquelle il ou elle clique ou qu’il saisit directement dans la barre d’adresse. Lorsque l’utilisateur accède au site web, [!DNL Analytics] suit les informations qui peuvent être utilisées pour déterminer le canal qui a motivé la visite.

Souvent, les professionnels du marketing ajoutent des codes de suivi de paramètres de chaîne de requête aux URL des canaux pour suivre l’impact du canal sur leur site. Vous pouvez configurer des règles de traitement [!DNL Marketing Channels] pour écouter les paramètres et valeurs de suivi spécifiques afin de déterminer le canal sans suivi supplémentaire. Par exemple, si toutes les URL de campagne par e-mail suivent le format `www.adobe.com?cid=email…` (où l’URL contient le paramètre de chaîne de requête et la valeur `cid=email`), vous pouvez créer une règle pour écouter ce code de suivi et pour regrouper la visite dans le canal [!UICONTROL Email].

Les autres canaux ne disposent pas de chemins d’URL traçables et ont besoin d’une logique supplémentaire pour l’identification. Par exemple, le [!UICONTROL Earned Social], dans lequel un utilisateur clique sur un lien qu’un autre utilisateur a partagé de manière organique sur un réseau social, est un canal important à suivre. Cependant, le marketeur ne peut pas ajouter de code de suivi de paramètre de chaîne de requête à l&#39;URL partagée. Dans ce cas, vous pouvez créer une règle de traitement pour écouter le domaine référent des réseaux sociaux ciblés et l’absence de codes de suivi payants pour déterminer le canal. Les visites qui répondent à ces exigences sont ensuite suivies en tant que visites gagnées dans le rapport Canaux marketing.

Adobe recommande de travailler avec votre équipe d’analyse pour créer un ensemble complet de règles de traitement des [!DNL Marketing Channels] afin de suivre tous les canaux pertinents pour votre entreprise. Cela vous permet de créer des rapports d’attribution puissants.

Pour comprendre comment Adobe Advertising peut contribuer aux signaux nécessaires à la création de canaux marketing personnalisés, consultez la section « [&#x200B; Utilisation des Adobe Advertising ID pour créer [!DNL Marketing Channels] traiter des règles &#x200B;](mc-ids.md) ».

>[!MORELIKETHIS]
>
>* [Utilisation des Adobe Advertising ID pour la création [!DNL Marketing Channels] le traitement des règles](mc-ids.md)
>* [Pourquoi les données de canal peuvent varier entre Adobe Advertising et  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilisation [!DNL Analytics Marketing Channels] avec des données Adobe Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation  [!DNL Marketing Channels]  rapports pour Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=fr)
>* [Présentation de  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
