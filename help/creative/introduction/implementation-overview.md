---
title: Présentation de l’implémentation de Adobe Advertising Creative
description: Découvrez le workflow de base pour l’implémentation de  [!DNL Creative].
feature: Creative Introduction
source-git-commit: fbd85ce99ab177c70b95bae42166265ef9053034
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 0%

---

# Présentation de l’implémentation de Adobe Advertising Creative

*Version bêta fermée*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

L’équipe des opérations [!DNL Creative] travaille avec chaque annonceur pour configurer ses contenus publicitaires et ses expériences créatives, en mettant en œuvre les expériences publicitaires sous la forme de publicités dans votre DSP ou en fournissant à votre équipe les balises publicitaires tierces à mettre en œuvre, ainsi qu’en validant les données initiales de coût, de clic et de conversion.

De manière continue, l’équipe du compte Adobe, l’équipe de l’agence ou l’annonceur (selon les conditions du service level agreement) doivent surveiller chaque expérience et la modifier si nécessaire pour atteindre les objectifs de l’annonceur.

## Tâches de configuration initiales pour les expériences [!DNL Creative]

L’équipe de mise en œuvre et/ou votre agence collaboreront avec vous pour effectuer les opérations suivantes :

1. Définissez vos objectifs de personnalisation (par exemple, si vous allez personnaliser les annonces pour la prospection ou le reciblage) ; toutes les données propriétaires, secondaires et tierces disponibles, y compris les ressources créatives et les segments d’audience ; ainsi que votre stratégie pour atteindre vos objectifs.<!-- and CRM data? used how/where? -->

1. (Nouveaux comptes d’annonceurs) Configurez des comptes d’administration :

   1. Configurez le compte de l’annonceur pour [!DNL Creative] et créez également un compte dans Advertising Search, Social et Commerce.

      La configuration du compte [!DNL Creative] se fait dans Advertising DSP, même si l’annonceur n’utilise pas le reste de DSP.

      De même, même si l’annonceur n’est pas un client [!DNL Search, Social, & Commerce], le compte [!DNL Search, Social, & Commerce] est utilisé pour créer des balises de suivi des conversions et configurer des colonnes de conversion dans [!DNL Creative].

   1. (Si nécessaire) Créez des comptes utilisateur pour que l’annonceur puisse afficher et gérer ses contenus publicitaires et ses expériences publicitaires, et générer des rapports.

1. (Facultatif) Si vous souhaitez créer des segments d’audience propriétaires à inclure en tant que cibles pour vos contenus publicitaires, créez les balises de l’une des manières suivantes :

   * [Créez des pixels de reciblage](/help/creative/pixels/retargeting-pixel-manage.md) pour recibler les annonces destinées aux visiteurs avec des attributs spécifiques sur des pages de destination ou de conversion spécifiques, puis générez des balises à insérer dans les pages web appropriées.

   * (Annonceurs avec DSP) Dans DSP, [créez des segments d’audience personnalisés](/help/dsp/audiences/custom-segment-create.md) pour suivre tous les visiteurs vers des pages de destination ou de conversion spécifiques, puis générez des balises à insérer dans les pages web appropriées.

   Les deux types de balises sont des balises d’image qui affichent une image transparente de 1 pixel sur 1 pixel (pixel), invisible pour les utilisateurs finaux, sur la page web à laquelle elles sont ajoutées. Vous pouvez ensuite configurer les contenus publicitaires d’une expérience publicitaire pour cibler des pixels ou des segments de reciblage spécifiques, de sorte que les éléments publicitaires pertinents s’affichent uniquement pour les utilisateurs qui ont déjà visité les pages du site associées au pixel ou au segment.

   Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de planifier le déploiement des balises ou d’être informé de celui-ci.

   **Remarque :** vous pouvez également utiliser vos audiences propriétaires de Adobe Audience Manager et d’Adobe Analytics en tant que cibles créatives. Une fois qu’un visiteur se qualifie pour une audience partagée depuis [!DNL Analytics], les informations sont exploitables en [!DNL Creative] en 24 à 48 heures environ. <!--Are times still true? -->

1. Configurez la hiérarchie des campagnes dans les DSP dans lesquels vous implémenterez vos expériences publicitaires. Utilisez un ciblage compatible avec le ciblage dans les expériences publicitaires que vous implémenterez dans les campagnes.

   Le comportement de ciblage hiérarchique peut varier en fonction du DSP. Advertising DSP applique le ciblage au niveau des annonces en plus (et non à la place) du ciblage au niveau des emplacements. Par exemple, si un emplacement cible des utilisateurs en Australie et qu’une annonce cible des utilisateurs au Japon, l’annonce cible la branche « Tout le monde » de l’expérience. Veillez à réfléchir à l’ensemble de la structure de la campagne.

1. Configurez les expériences publicitaires en fonction de vos objectifs publicitaires :

   * **Workflow d’automatisation :** l’équipe des opérations [!DNL Creative] peut créer des annonces dynamiques pour votre organisation à l’aide de modèles d’annonces publicitaires et de flux de données.

     Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. --><!-- I think this will be automatic based on their IMS organization. But I'm not sure if they need to be logged in via SSO using their Adobe login or if it will also work using their legacy DSP login. -->

   * **Workflow manuel :** configurer manuellement les expériences publicitaires :

      1. [Configurez des contenus publicitaires standard à utiliser dans vos expériences](/help/creative/creative-libraries/creative-add-standard.md) :

         * Pour les créatifs que [!DNL Creative] hébergera, chargez-les. Cela peut inclure des ressources d’image dans un compte Adobe Experience Manager.

         * Pour les contenus publicitaires hébergés sur un serveur de publicités tiers pris en charge, pointez sur les fichiers créatifs.

      1. (Facultatif) [Regroupez les contenus publicitaires en lots](/help/creative/creative-libraries/bundle-manage.md) que vous pouvez joindre à des expériences ciblées en une seule étape.

      1. Configurez les [expériences publicitaires](/help/creative/experiences/experience-about.md) :

         * Pour les [expériences publicitaires ciblées](/help/creative/experiences/experience-create-targeting.md), séquencez les contenus publicitaires et les cibles publicitaires facultatives.

           Les cibles d’annonces peuvent inclure les pixels de reciblage que vous créez dans [!DNL Creative], vos segments d’audience dans Adobe Experience Cloud (y compris dans DSP, Audience Manager ou [!DNL Analytics]), des cibles géographiques ou des déclencheurs de données spécifiques sur la page web (tels que SKU=01234567890123 ou Panier=vide).

         * Pour les [expériences publicitaires non ciblées](/help/creative/experiences/experience-create-no-targeting.md), créez des paramètres d’expérience généraux.

           Les cibles d’annonces peuvent inclure les pixels de reciblage que vous créez dans [!DNL Creative], vos segments d’audience dans Adobe Experience Cloud (y compris dans DSP, Audience Manager ou [!DNL Analytics]), des cibles géographiques ou des déclencheurs de données spécifiques sur la page web (tels que SKU=01234567890123 ou Panier=vide).













1. Configurez le suivi des conversions pour vos expériences publicitaires :


Configurez le suivi des conversions. Selon la mise en œuvre, cela peut impliquer l’ajout de :
balises de suivi des conversions vers les pages web de l’annonceur et/ou configuration d’une
goutte de flux pour les données de conversion que l’annonceur a collectées séparément.


Vous pouvez générer des balises de suivi de conversion Adobe Advertising dans Advertising Search, Social et Commerce ou dans Adobe Dynamic Tag Manager (anciennement appelé Dynamic Tag Manager).
Remarque : vous devez utiliser les balises de conversion JavaScript, et non les balises d’image.


Le service informatique de l’annonceur ou un autre groupe peut avoir besoin de programmer ou d’être informé
à propos du déploiement des balises.


(Facultatif) Dans Search, Social et Commerce, effectuez chaque conversion (propriété de transaction)
disponible sous la forme d’un jeu de colonnes individuel dans les vues de données et les rapports.


Une conversion (propriété de transaction) est répertoriée dans Search, Social et Commerce après à
au moins un événement de conversion a fait l’objet d’un suivi.


Si vous ne rendez pas des mesures spécifiques disponibles, toutes les conversions sont consolidées
dans un jeu de colonnes « Conversions ».


Validez les données qui font l’objet d’un suivi.


(Facultatif) Configurez la diffusion des rapports planifiés vers des adresses e-mail spécifiées.


Pour obtenir des instructions, reportez-vous au chapitre d’aide sur « Rapports ».


Configurez des campagnes publicitaires sur Advertising DSP ou un autre DSP et fournissez des JavaScript
ou des balises iframe pour les expériences publicitaires à l’annonceur, qui peut les implémenter en tant que
publicités tierces dans le DSP.


Surveillez les performances de vos expériences publicitaires terminées, en affichant des publicités prédéfinies
détails de performances pour des expériences individuelles ou création de rapports de performances personnalisés.


(Si nécessaire) Mettez à jour les expériences publicitaires en fonction des performances et des messages mis à jour.






>[!MORELIKETHIS]
>
>* [À propos de Adobe Advertising Creative](/help/creative/introduction/creative-about.md)
>* [Organisation de l’interface utilisateur](/help/creative/introduction/ui.md)
