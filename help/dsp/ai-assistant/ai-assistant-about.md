---
title: À propos de l’assistant AI dans Advertising DSP
description: Découvrez comment utiliser l’assistant d’IA de DSP pour résoudre les problèmes liés aux packages et aux emplacements, créer des rapports et rechercher de l’aide sur l’utilisation du produit.
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
source-git-commit: 1c279c827b9e1f3d5cc9d3a031106730b3a365bd
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%
---
# À propos de l’assistant AI dans Advertising DSP

L’assistant AI dans DSP est une interface de conversation qui vous permet d’exécuter n’importe quel workflow agentique disponible dans DSP à partir d’une seule chatbox. Vous pouvez créer une nouvelle tâche ou demander de l’aide pour poursuivre une tâche précédente.

Votre historique des conversations est conservé pour tous les workflows, chaque conversation étant automatiquement nommée. Vos requêtes ne sont pas partagées avec d’autres utilisateurs.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Workflows pris en charge

Les workflows suivants peuvent vous aider à accomplir votre travail plus efficacement :

<!-- And links to all sections/pages -->

| Fonctionnalité | Description | Réponses |
| --- | --- | --- |
| [Dépannage](troubleshooting-agent.md) | (Fonction Beta) Diagnostiquer les problèmes de performances et de diffusion pour les packages et emplacements en direct.<ul><li>Stages uniquement : diagnostiquer les dépassements, les dépassements et les insuffisances de dépenses. L’agent évalue les facteurs de fréquence, d’enchères, de ciblage et de plafonnement budgétaire associés.</li><li>Packages uniquement : diagnostiquer les problèmes de performances, y compris une augmentation du CPA ou un retour sur dépenses publicitaires en baisse. L’agent ne diagnostique pas les mesures d’engagement telles que le taux de clics, le taux de clic ou les impressions.</li></ul>Chaque conversation couvre un diagnostic pour un package ou un emplacement. Après avoir reçu un résultat, démarrez une nouvelle conversation pour diagnostiquer un autre problème, un autre package ou un autre emplacement.<br><br>L’agent ne peut pas modifier les paramètres, ni créer ou modifier des campagnes ou des composants de campagne. Il ne peut pas non plus diagnostiquer les packages ou emplacements en pause, terminés, archivés ou planifiés. | La réponse inclut des facteurs qui limitent les performances et fournit des recommandations pour résoudre les problèmes. |
| [Informations](insights-agent.md) | (Fonction Beta) Obtenez des mesures de campagne et des rapports complets sans créer manuellement de rapport. Vous pouvez poser des questions simples sur une mesure spécifique, telle que les dépenses ou le CPA pour une campagne, ou demander un rapport plus complexe pour une dimension spécifique (telle qu’une campagne unique, un emplacement ou une audience) ou entre les dimensions (pour les répartitions par campagne et par annonceur). Vous pouvez télécharger les résultats au format CSV. | Les premières lignes du rapport s’affichent avec des liens pour prévisualiser le rapport complet et télécharger le rapport sous la forme d’un fichier de valeurs séparées par des virgules [!DNL Microsoft Excel] (.csv). |
| [Recherche de documentation du produit](documentation-search.md) | Recherchez du contenu conceptuel et pratique dans le [Guide d’](/help/dsp/home.md) et, pour les annonceurs qui utilisent Advertising Creative, le [Guide d’Advertising Creative](/help/creative/home.md). Les réponses reposent uniquement sur ce qui est documenté pour ces produits dans [&#128279;](https://experienceleague.adobe.com/fr/docs/advertising).<br><br>Demandez des informations sur la gestion des campagnes, l’optimisation, la gestion des audiences, les offres, les rapports et d’autres fonctionnalités des produits. | La réponse comprend des citations intégrées et une liste de [!UICONTROL Documentation Sources] extensible en bas. Cliquez sur une citation ou une liste de sources pour ouvrir la page correspondante.<br><br>La réponse peut également inclure des questions et des suggestions de suivi pour vous aider à affiner votre requête et à trouver plus d’informations. |

## Bonnes pratiques relatives à l’écriture de requêtes et d’invites {#writing-queries}

* **Soyez clair et précis**. Utilisez des questions complètes (« Comment s’abonner à l’inventaire à la demande ? »), des expressions de tâche (« S’abonner à l’inventaire à la demande ») ou des expressions de sujet (« Inventaire à la demande »).

* **Ne combinez pas différents types de requêtes dans la même requête** sauf si vous souhaitez qu’ils soient stockés dans la même conversation.

* **Incluez des périodes, le cas échéant** pour réduire les données souhaitées.

* **Correspondre aux termes de l’interface utilisateur** si possible pour les fonctionnalités du produit (telles que les « campagnes » ou les « offres »).

  Pour les actions courantes (telles que « ajouter », « joindre » ou « attribuer »), vous pouvez utiliser des synonymes.

* **Ajoutez des détails** pour limiter ou élargir les résultats. Affinez avec des questions de suivi si nécessaire.

* **Ne vous inquiétez pas de la ponctuation et de la majuscule** sauf quand elles affectent le sens.

>[!MORELIKETHIS]
>
>* [Créer des rapports à l’aide de l’assistant AI](insights-agent.md)
>* [Résolution des problèmes de performances et de diffusion à l’aide de l’assistant AI](troubleshooting-agent.md)
>* [Créer une audience réutilisable](/help/dsp/audiences/reusable-audience-create.md)
>* [Rechercher de la documentation sur les produits à l’aide de l’assistant AI](documentation-search.md)
>* [Utiliser les conversations précédentes de l’assistant AI](previous-conversations.md)
