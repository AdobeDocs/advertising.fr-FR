---
title: Diagnostiquer les problèmes de performances et de diffusion à l’aide de la [!UICONTROL Troubleshooting Agent] assistée par l’IA
description: Découvrez comment utiliser l’agent de dépannage assisté par l’IA pour diagnostiquer les problèmes de dépenses, de fréquence et de diffusion pour les packages et emplacements DSP.
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 31ddb7928ca4e43132087b73829af55ae6315b0d
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%
---
# Diagnostiquer les problèmes de performances et de diffusion à l’aide de la [!UICONTROL Troubleshooting Agent] assistée par l’IA

Le [!UICONTROL Troubleshooting Agent] assisté par l’IA identifie les facteurs qui limitent les performances et fournit des recommandations pour résoudre les problèmes. Le [!UICONTROL Troubleshooting Agent] peut :

* Aide pour diagnostiquer les problèmes de performances et de diffusion pour un package ou un emplacement actif sélectionné :

  * (Emplacements uniquement) Questions relatives aux dépenses, y compris les dépenses excessives, les dépenses insuffisantes et l’incapacité de dépenser. L&#39;agent évalue les facteurs de fréquence, d&#39;enchères, de ciblage et de plafonnement budgétaire associés dans le cadre du diagnostic.

  * (Packages uniquement) Problèmes de performances, notamment une augmentation du CPA ou un retour sur dépenses publicitaires en baisse. L’agent ne diagnostique pas les mesures d’engagement telles que le taux de clics, le taux de clic ou les impressions.

  Chaque conversation couvre un seul diagnostic pour un seul package ou emplacement. Une fois que l&#39;agent a obtenu un résultat, commencez une nouvelle conversation pour poser des questions sur un autre problème ou sur un autre package ou emplacement.

  L’agent ne peut pas modifier les paramètres, ni créer ou modifier des campagnes ou des composants de campagne. Il ne peut pas non plus diagnostiquer les problèmes d&#39;un emplacement ou d&#39;un package en pause, terminé, archivé ou planifié.

* Recherchez du contenu conceptuel et pratique dans le [Guide d’](/help/dsp/home.md) et (les annonceurs avec Advertising Creative) le [Guide d’Advertising Creative](/help/creative/home.md), de la même manière que l’[interface de conversation agentique](/help/dsp/agent-chat.md). Vous pouvez poser des questions sur la gestion des campagnes, l’optimisation, la gestion des audiences, les offres, les rapports et d’autres fonctionnalités de produit.

>[!IMPORTANT]
>
>Les réponses générées par l&#39;IA peuvent être inexactes ou trompeuses. Vérifiez toujours les réponses et les sources avant de les utiliser pour les décisions qui affectent les coûts ou les efforts.

## Exemples de requêtes

>[!NOTE]
>
>Il n’est pas nécessaire de spécifier de période. Si vous n’en incluez pas, l’agent choisit une valeur par défaut raisonnable en fonction du type de problème.

### Stages : problèmes de dépenses

* Mon placement a cessé de dépenser hier même si l&#39;affaire est active. Pourquoi ?

* Pourquoi ce placement a-t-il été sous-utilisé au cours des 5 derniers jours ?

* Nous sommes à mi-chemin du vol et nous accusons un retard important par rapport au rythme. Pourquoi ?

### Packages : problèmes de performances

* Pourquoi l&#39;ACP a-t-elle augmenté pour ce paquet au cours de la semaine dernière ?

* Pourquoi le retour sur dépenses publicitaires diminue-t-il pour ce package ?

>[!TIP]
>
>Si vous avez une CPA cible en tête, incluez-la dans votre requête (par exemple, « Diagnostiquer une CPA par rapport à une cible de 50 $ »). Si vous n’en spécifiez pas, l’agent utilise une cible par défaut.

### Fonctionnalités du produit :

* Comment créer un emplacement ?

* Quelles sont les options de ciblage disponibles dans Adobe DSP ?

* Comment joindre une annonce publicitaire à un emplacement ?

* Quelles sont les conséquences de l’utilisation des différentes options de fréquence dans les paramètres d’emplacement ?

* Quand dois-je utiliser chaque type d’objectif d’optimisation ?

* Pourquoi les emplacements programmatiques garantis (PG) ne servent-ils pas d’impressions ?

* Quels rapports contiennent des données au niveau des ménages ?

* Quelle est la différence entre une expérience ciblée et une expérience non ciblée dans [!DNL Creative] ?

* Comment créer une balise publicitaire pour une expérience [!DNL Creative] ?

## Envoi d’une requête pour un package actif ou un emplacement

Vous pouvez poser plusieurs questions dans un seul message, mais un seul message à la fois. Attendez une réponse avant d’en envoyer une autre.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Effectuez l’une des opérations suivantes :

   * (Pour les packages) Dans la vue [!UICONTROL Packages], cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** en regard du nom du package.

   * (Pour les emplacements) Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Saisissez votre requête et cliquez sur ![Invite Envoyer](/help/dsp/assets/submit-prompt.png "Invite Envoyer").

   <!-- For more information, see "[Writing prompts](#writing-prompts)." -->

   Pour les requêtes de performances et de diffusion, la réponse inclut les facteurs qui limitent les performances et fournit des recommandations pour résoudre les problèmes.

   Pour les requêtes de documentation, la réponse inclut des citations intégrées et une liste **[!UICONTROL Documentation Sources]** en bas. Des questions et suggestions de suivi peuvent également apparaître.

1. (Requêtes de documentation uniquement ; facultatif) Pour ouvrir une page utilisée comme source de données, effectuez l’une des opérations suivantes :

   * Cliquez sur la citation numérotée.

   * Cliquez sur **[!UICONTROL Documentation Sources]** pour afficher la liste de toutes les pages citées dans la réponse, puis cliquez sur le lien de la page.

1. (Facultatif) Évaluez la réponse à l’aide de l’icône pouces vers le haut ou pouces vers le bas.

>[!TIP]
>
>Pour poser des questions sur un autre problème, ou sur un autre package ou emplacement, commencez une nouvelle conversation.
