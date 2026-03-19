---
title: Utilisation  [!DNL Marketing Channels]  données Adobe Advertising
description: Découvrez comment utiliser les données Adobe Advertising dans  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 4db751aae61eaf8abdc5e3afca3b4027f0eddf26
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Utilisation de [!DNL Analytics Marketing Channels] avec des données Adobe Advertising

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

En utilisant à la fois les rapports Adobe Advertising et [!DNL Analytics Marketing Channels], vous pouvez bénéficier d’une insight précieuse sur la manière dont vos médias numériques influencent l’activité du site.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

L’illustration suivante montre comment Adobe Advertising et [!DNL Marketing Channels] effectuent le suivi des visites individuelles qui composent le parcours d’un visiteur. Les rapports Adobe Advertising dans [!DNL Analytics] se limitent aux canaux d’affichage, de recherche, des réseaux sociaux et du commerce payants qui font l’objet d’un trafic via Adobe Advertising à l’aide de l’AMO ID. Toutefois, [!DNL Marketing Channels] suit tous les canaux configurés dans les règles de traitement [!DNL Marketing Channels].

![Comment Adobe Advertising et [!DNL Marketing Channels] effectuent le suivi des visites individuelles dans le parcours d’un visiteur](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Lors de sa première visite, l’utilisateur est entré sur le site web par le biais d’une campagne par e-mail, a exécuté dix pages vues, puis est parti. Lors de la deuxième visite, l’utilisateur est entré sur le site par le biais d’une publicité display, a effectué dix pages vues, puis est reparti. Lors de la troisième visite, l’utilisateur est entré sur le site par le biais d’une recherche naturelle, a affiché cinq pages vues, a effectué une conversion de 250 $ et s’est retrouvé à gauche. Notez la différence de tracking entre [!DNL Marketing Channels] et Adobe Advertising. Le seul canal suivi par Adobe Advertising dans ce parcours est [!UICONTROL Display]. Adobe Advertising effectue le suivi de la visite du canal [!UICONTROL Display] et attribue les données d’engagement suivantes (telles que les pages vues) et les conversions à l’influence de cette publicité. [!DNL Marketing Channels], en revanche, donne une vue complète de tous les canaux.

Étant donné que l’AMO ID persiste dans le parcours du visiteur, vous pouvez utiliser les données de l’AMO ID pour voir comment Adobe Advertising influence d’autres canaux marketing. L’ID AMO [persiste pendant 60 jours par défaut](/help/integrations/analytics/overview.md), mais vous pouvez configurer la persistance selon vos besoins.

## Comment combiner les données Adobe Advertising et des canaux marketing pour analyser les performances des médias

Dans [!DNL Analytics], vous pouvez combiner les données de publicité payante persistantes d’Adobe Advertising et les données de visite complètes [!DNL Marketing Channels] pour mieux analyser les performances de vos médias afin de mieux influencer le parcours client.

L’analyse suivante utilise les données Adobe Advertising pour montrer différentes versions de l’impact d’une publicité display sur la conversion d’un site. Les trois colonnes utilisent les mêmes mesures de conversion, mais chaque colonne raconte une histoire différente :

* La colonne 1 examine les données d’ID AMO qui sont persistantes dans le parcours du visiteur. La colonne 1 indique que 641 démarrages d’applications étaient, à un moment donné, liés à une publicité Adobe Advertising, par le biais d’un affichage publicitaire ou d’un clic publicitaire. Cette vue ne prend en compte aucune autre attribution de [!DNL Marketing Channels].

* Toutefois, dans le jeu de données [!DNL Marketing Channels], les démarrages d’applications 641 sont attribués à d’autres canaux marketing. Les deux dernières colonnes prennent les démarrages d’applications 641 et limitent les données aux canaux [!UICONTROL Display Click-Through] et [!UICONTROL Display View-Through], montrant les conversions qui se produisent dans un modèle d’attribution Dernière touche.

![exemple de la manière dont une publicité display affecte la conversion d’un site](/help/integrations/assets/a4adc-mc-display-impact.png)

Vous pouvez pousser cette analyse un peu plus loin. Vous pouvez ventiler davantage la ligne Adobe Advertising par canal marketing pour voir où les conversions Adobe Advertising sont attribuées aux démarrages d’applications 641. Vous savez déjà que cinq de ces conversions sont attribuées à un dernier clic d’affichage tactile et 19 à un dernier clic d’affichage tactile. Il reste encore 617 démarrages d’applications attribués à d’autres canaux marketing. Vous pouvez faire glisser et déposer la dimension Canal Dernière touche en haut de l’élément de ligne Advertising DSP afin d’afficher l’attribution du canal pour le reste des démarrages d’applications et montrer l’impact cross-canal du canal d’affichage.

![comment ajouter la dimension Canal Dernière touche ](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Maintenant, vous pouvez voir comment les démarrages d&#39;applications restants sont attribués. L’e-mail est crédité de 357 démarrages d’applications Last Touch pour lesquels un AMO ID a persisté. Grâce à ce type d’analyse, vous pouvez voir l’impact des publicités display d’Adobe Advertising sur tous les canaux. Avec un seul jeu de données et modèle d’attribution, ce type d’insight ne serait pas disponible.

![exemple de l’impact cross-canal des canaux d’affichage](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Vous pouvez améliorer davantage l’analyse en utilisant un graphique de pile défini sur « 100 % empilé » pour afficher les données de tendance au fil du temps. Cette visualisation facilite la surveillance des canaux marketing Dernière touche qui sont plus lourdement affectés par vos campagnes marketing Affichage.

![exemple de l’impact cross-canal de tendance des canaux d’affichage](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Principes fondamentaux de  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilisation des Adobe Advertising ID pour la création [!DNL Marketing Channels] le traitement des règles](mc-ids.md)
>* [Pourquoi les données de canal peuvent varier entre Adobe Advertising et  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Vidéo : Utilisation  [!DNL Marketing Channels]  rapports pour Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Présentation de  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
