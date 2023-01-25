---
title: Utilisation [!DNL Marketing Channels] avec Adobe des données Advertising
description: Découvrez comment utiliser les données Adobe Advertising dans [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: c9403a03-58aa-4633-bb97-51afc30843ad
source-git-commit: 1c13874967ec4ad264e5fa6a5e0dfeb6120f53cc
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# Utilisation [!DNL Analytics Marketing Channels] avec Adobe des données Advertising

*Annonceurs avec une intégration Advertising-Adobe Analytics Adobe uniquement*

En utilisant Adobe Advertising et [!DNL Analytics Marketing Channels] rapports, vous pouvez obtenir des informations précieuses sur l’influence de vos médias numériques sur l’activité du site.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

L’illustration suivante montre comment Adobe Advertising et [!DNL Marketing Channels] effectuer le suivi des visites individuelles qui constituent le parcours d’un visiteur. Rapports Adobe Advertising dans [!DNL Analytics] sont limitées à la publicité payante des canaux d’affichage, de recherche, sociaux et de commerce qui fait l’objet d’un trafic via Adobe Advertising, à l’aide de l’AMO ID. Cependant, [!DNL Marketing Channels] effectue le suivi de tous les canaux configurés dans la variable [!DNL Marketing Channels] Règles de traitement.

![Présentation de la publicité Adobe et [!DNL Marketing Channels] effectuer le suivi des visites individuelles dans le parcours d’un visiteur ;](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Lors de la première visite, l’utilisateur est entré sur le site web par le biais d’une campagne par e-mail, a exécuté dix pages vues, puis est parti. Lors de la seconde visite, l’utilisateur est entré sur le site par le biais d’une annonce publicitaire, a exécuté dix pages vues, puis est parti. Lors de la troisième visite, l’utilisateur est entré sur le site par le biais d’une recherche naturelle, a exécuté cinq pages vues, a exécuté une conversion de 250 €, puis a exécuté la gauche. Notez la différence entre le suivi [!DNL Marketing Channels] et Adobe Advertising. Le seul canal suivi par Adobe Advertising dans ce parcours est [!UICONTROL Display]. Adobe Advertising effectue le suivi de la publicité [!UICONTROL Display] visite de canal et attribue les données d’engagement suivantes (telles que les pages vues) et les conversions à l’influence de cette publicité. [!DNL Marketing Channels], en revanche, donne une vue complète de tous les canaux.

Comme l’AMO ID persiste tout au long du parcours du visiteur, vous pouvez utiliser les données AMO ID pour déterminer l’influence de la publicité par Adobe sur d’autres canaux marketing. AMO ID [persiste pendant 60 jours par défaut.](/help/integrations/analytics/overview.md), mais vous pouvez configurer la persistance selon vos besoins.

## Comment combiner des données de canal marketing et de publicité d’Adobe pour analyser les performances multimédia

Within [!DNL Analytics], vous pouvez combiner les données de publicité payante persistantes Adobe Advertising et le [!DNL Marketing Channels] données de visite complètes afin de mieux analyser les performances de vos médias afin de mieux influencer le parcours client.

L’analyse suivante utilise les données Adobe Advertising pour montrer différentes versions de l’impact d’une publicité display sur la conversion du site. Les trois colonnes utilisent les mêmes mesures de conversion, mais chaque colonne raconte une histoire différente :

* La colonne 1 examine les données AMO ID qui persistent dans le parcours du visiteur. La colonne 1 indique que 641 Applications Start étaient, à un moment donné, liées à une publicité Adobe Advertising, soit par un affichage publicitaire, soit par un événement de clic publicitaire. Cette vue ne prend aucune autre valeur [!DNL Marketing Channels] en tenant compte de l’attribution.

* Dans le [!DNL Marketing Channels] Toutefois, le jeu de données 641 Applications Starts est attribué à d’autres canaux marketing. Les deux dernières colonnes contiennent les 641 Applications Starts et limitent les données à la variable [!UICONTROL Display Click-Through] et [!UICONTROL Display View-Through] canaux, affichant les conversions survenant dans un modèle d’attribution Dernière touche.

![exemple d’impact d’une publicité display sur la conversion d’un site](/help/integrations/assets/a4adc-mc-display-impact.png)

Vous pouvez aller plus loin dans cette analyse. Vous pouvez ventiler davantage la ligne Adobe Advertising par canal marketing pour voir où les conversions Adobe Advertising sont attribuées aux 641 Applications Start. Vous savez déjà que cinq de ces conversions sont attribuées à un clic publicitaire avec affichage Dernière touche et que 19 sont attribuées à un affichage publicitaire avec affichage Dernière touche. Cela laisse 617 Applications démarrées attribuées à d’autres canaux marketing. Vous pouvez faire glisser et déposer la dimension Canal Dernière touche au-dessus de l’élément de ligne DSP de publicité pour afficher l’attribution du canal pour le reste des Applications Commence et afficher l’impact cross-canal du canal d’affichage.

![Comment ajouter la dimension Canal Dernière touche](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Vous pouvez maintenant voir comment les autres applications commencent sont attribuées. Le courrier électronique est crédité pour les demandes 357 Last Touch Applications pour lesquelles un AMO ID a persisté. Grâce à ce type d’analyse, vous pouvez voir l’impact des publicités affichées Adobe Advertising sur tous les canaux. Avec un seul jeu de données et un seul modèle d’attribution, ce type d’informations ne serait pas disponible.

![exemple de l’impact cross-canal des canaux d’affichage](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Vous pouvez améliorer davantage l’analyse en utilisant un graphique empilé défini sur &quot;100 % empilé&quot; pour afficher les données de tendances au fil du temps. Cette visualisation facilite le suivi des canaux marketing Dernière touche les plus affectés par vos campagnes marketing display.

![exemple de l’impact cross-canal de tendance des canaux d’affichage](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Principes fondamentaux de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Utilisation d’identifiants Adobe Advertising pour créer [!DNL Marketing Channels] Règles de traitement](mc-ids.md)
>* [Pourquoi les données de canal peuvent-elles varier entre la publicité Adobe et [!DNL Marketing Channels]](mc-data-variances.md)
>* [Vidéo : Utilisation [!DNL Marketing Channels] pour la création de rapports Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Présentation de [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

