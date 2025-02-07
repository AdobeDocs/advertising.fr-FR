---
title: Présentation du Adobe Advertising Creative d’implémentation
description: Découvrez le workflow de base pour l’implémentation de  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Présentation du Adobe Advertising Creative d’implémentation

*Version bêta fermée*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

L’équipe des opérations [!DNL Creative] travaille avec chaque annonceur pour configurer ses contenus publicitaires et ses expériences créatives, en mettant en œuvre les expériences publicitaires sous la forme de publicités au sein de votre DSP ou en fournissant à votre équipe les balises publicitaires tierces à mettre en œuvre, ainsi qu’en validant les données initiales de coût, de clic et de conversion.

De manière continue, l’équipe du compte d’Adobe, l’équipe de l’agence ou l’annonceur (selon les conditions du service level agreement) doivent surveiller chaque expérience et la modifier si nécessaire pour atteindre les objectifs de l’annonceur.

## Tâches de configuration initiales pour [!DNL Creative] Campagnes <!-- Experiences? "Campaigns" may be confusing now. -->

L’équipe de mise en œuvre et/ou votre agence collaboreront avec vous pour effectuer les opérations suivantes :

1. Définissez vos objectifs de personnalisation (par exemple, si vous allez personnaliser les annonces pour la prospection ou le reciblage) ; toutes les données propriétaires, secondaires et tierces disponibles, y compris les ressources créatives, les segments d’audience et la <!-- used how/where? --> de données CRM ; ainsi que votre stratégie pour atteindre vos objectifs.

1. (Nouveaux comptes d’annonceurs) Configurez des comptes d’administration :

   1. Configurez le compte de l’annonceur pour [!DNL Creative]<!-- and/or DSP? --> et créez également un compte dans Advertising Search.

      La configuration du compte [!DNL Creative] se fait dans Advertising DSP, même si l’annonceur n’est pas un client DSP.

      De même, même si l’annonceur n’est pas un client [!DNL Search], le compte [!DNL Search] est utilisé pour créer des balises de suivi des conversions et configurer des colonnes de conversion dans [!DNL Creative].

   1. (Si nécessaire) Créez des comptes utilisateur pour que l’annonceur puisse afficher et gérer ses contenus publicitaires et ses expériences publicitaires, et générer des rapports.

1. (Facultatif) Si vous souhaitez créer des segments d’audience propriétaires à inclure en tant que cibles pour vos contenus publicitaires, créez les balises de l’une des manières suivantes :

   * [Créez des pixels de reciblage](/help/creative/pixels/retargeting-pixel-manage.md) pour recibler les annonces destinées aux visiteurs avec des attributs spécifiques sur des pages de destination ou de conversion spécifiques, puis générez des balises à insérer dans les pages web appropriées.

   * (Annonceurs avec DSP) Au sein de DSP, [créez des segments d’audience personnalisés](/help/dsp/audiences/custom-segment-create.md) pour effectuer le suivi de tous les visiteurs vers des pages de destination ou de conversion spécifiques, puis générez des balises à insérer dans les pages web appropriées.

   Les deux types de balises sont des balises d’image qui affichent une image transparente de 1 pixel sur 1 pixel (pixel), invisible pour les utilisateurs finaux, sur la page web à laquelle elles sont ajoutées. Vous pouvez ensuite configurer les contenus publicitaires d’une expérience publicitaire pour cibler des pixels ou des segments de reciblage spécifiques, de sorte que les éléments publicitaires pertinents s’affichent uniquement pour les utilisateurs qui ont déjà visité les pages du site associées au pixel ou au segment.

   Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé de celui-ci.

   **Remarque :** vous pouvez également utiliser vos audiences propriétaires de Adobe Audience Manager et d’Adobe Analytics en tant que cibles créatives. Une fois qu’un visiteur se qualifie pour une audience partagée depuis [!DNL Analytics], les informations sont exploitables en [!DNL Creative] en 24 à 48 heures environ. <!--Still true? And what about AAM and DSP? -->

1. Configurez les expériences publicitaires en fonction de vos objectifs publicitaires :

   * **Workflow d’automatisation :** l’équipe des opérations [!DNL Creative] peut créer des annonces dynamiques pour votre organisation à l’aide de modèles d’annonces publicitaires et de flux de données.

     Pour plus d’informations, adressez-vous à l’équipe chargée de votre compte Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **Workflow manuel :** configurer manuellement les expériences publicitaires :

      1. Configurez les contenus publicitaires à utiliser dans vos expériences :

         * Pour les créatifs que [!DNL Creative] hébergerez, chargez-les.<!-- Add x-ref and reword if necessary to cover all cases -->

         * Pour les contenus publicitaires hébergés sur un serveur de publicités tiers pris en charge, [pointez vers les fichiers créatifs](/help/creative/creative-libraries/creative-third-party-manage.md).

      1. (Facultatif) [Regroupez les contenus publicitaires en lots](/help/creative/creative-libraries/bundle-manage.md) que vous pouvez joindre à des expériences en une seule étape.

      1. Séquencer les contenus publicitaires et les cibles d’annonces facultatives en tant qu’[expériences publicitaires](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done -->

     Les cibles d’annonces peuvent inclure les pixels de reciblage que vous créez dans [!DNL Creative], vos segments d’audience dans Adobe Experience Cloud (y compris dans DSP, Audience Manager ou [!DNL Analytics]), des cibles géographiques ou des déclencheurs de données spécifiques sur la page web (tels que SKU=01234567890123 ou Panier=vide).&lt;!— Je ne vois pas les segments d’audience disponibles, et je vois les cibles de rayon (qui ne fonctionnent pas) mais pas d’autres cibles géographiques — vérifiez toutes ces cibles. —>

1. Configurez le suivi des conversions pour vos expériences publicitaires :


Configurez le suivi des conversions. Selon la mise en œuvre, cela peut impliquer l’ajout de :
balises de suivi des conversions vers les pages web de l’annonceur et/ou configuration d’une
goutte de flux pour les données de conversion que l’annonceur a collectées séparément.


Vous pouvez générer des balises de suivi des conversions Advertising Cloud dans Advertising Cloud
Recherchez ou dans le gestionnaire dynamique de balises d’Adobe (anciennement appelé gestionnaire dynamique de balises).
Remarque : vous devez utiliser les balises de conversion JavaScript, et non les balises d’image.


Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de programmer ou d’être informé
à propos du déploiement des balises.


(Facultatif) Dans Advertising Cloud Search, effectuez chaque conversion (propriété de transaction)
disponible sous la forme d’un jeu de colonnes individuel dans les vues de données et les rapports.


Une conversion (propriété transaction) est répertoriée dans Advertising Cloud Search après à .
au moins un événement de conversion a fait l’objet d’un suivi.


Si vous ne rendez pas des mesures spécifiques disponibles, toutes les conversions sont consolidées
dans un jeu de colonnes « Conversions ».


Validez les données qui font l’objet d’un suivi.


(Facultatif) Configurez la diffusion des rapports planifiés vers des adresses e-mail spécifiées.


Pour obtenir des instructions, reportez-vous au chapitre d’aide sur « Rapports ».


Configurez des campagnes publicitaires sur Advertising Cloud DSP ou un autre DSP et fournissez des JavaScript
ou des balises iframe pour les expériences publicitaires à l’annonceur, qui peut les implémenter en tant que
publicités de tiers dans le DSP.


Surveillez les performances de vos expériences publicitaires terminées, en affichant des publicités prédéfinies
détails de performances pour des expériences individuelles ou création de rapports de performances personnalisés.


(Si nécessaire) Mettez à jour les expériences publicitaires en fonction des performances et des messages mis à jour.






>[!MORELIKETHIS]
>
>* [À propos du Adobe Advertising Creative ](/help/creative/introduction/creative-about.md)
>* [Organisation de l’interface utilisateur](/help/creative/introduction/ui.md)
