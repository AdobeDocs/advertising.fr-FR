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
source-git-commit: 8bab50fe8bf737d208d059d89b2592e16bc40c69
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%
---
# À propos de l’assistant AI dans Advertising DSP

L’assistant AI dans DSP est une interface de conversation qui vous permet d’exécuter n’importe quel workflow agentique disponible dans DSP à partir d’une seule chatbox. Vous pouvez créer une nouvelle tâche ou demander de l’aide pour poursuivre une tâche précédente.

Votre historique des conversations est conservé pour tous les workflows, chaque conversation étant automatiquement nommée. Vos requêtes ne sont pas partagées avec d’autres utilisateurs.

<!-- Update this:  ![Example of a query and response](/help/dsp/assets/agent-chat-response.png "Example of a query and response") -->

## Workflows pris en charge

Les workflows suivants peuvent vous aider à accomplir votre travail plus efficacement :

<!-- And links to all sections/pages -->

| Fonctionnalité | Description | Exemples de requêtes | Réponses |
| --- | --- | --- | --- |
| [Dépannage](troubleshooting-agent.md) | Diagnostiquer les problèmes de performances et de diffusion pour un emplacement ou un package actif sélectionné.<ul><li>Stages uniquement : diagnostiquer les dépassements, les dépassements et les insuffisances de dépenses. L’agent évalue les facteurs de fréquence, d’enchères, de ciblage et de plafonnement budgétaire associés.</li><li>Packages uniquement : diagnostiquer les problèmes de performances, y compris une augmentation du CPA ou un retour sur dépenses publicitaires en baisse. L’agent ne diagnostique pas les mesures d’engagement telles que le taux de clics, le taux de clic ou les impressions.</li></ul>Chaque conversation couvre un diagnostic pour un package ou un emplacement. Après avoir reçu un résultat, démarrez une nouvelle conversation pour diagnostiquer un autre problème, un autre package ou un autre emplacement.<br><br>L’agent ne peut pas modifier les paramètres, ni créer ou modifier des campagnes ou des composants de campagne. Il ne peut pas non plus diagnostiquer les packages ou emplacements en pause, terminés, archivés ou planifiés. | Problèmes liés aux dépenses de placement :<ul><li>Mon placement a cessé de dépenser hier même si l&#39;affaire est active. Pourquoi ?</li><li>Pourquoi ce placement a-t-il été sous-utilisé au cours des 5 derniers jours ?</li><li>Nous sommes à mi-chemin du vol et nous accusons un retard important par rapport au rythme. Pourquoi ?</li></ul>Problèmes de performances des packages :<ul><li>Pourquoi l&#39;ACP a-t-elle augmenté pour ce paquet au cours de la semaine dernière ?</li><li>Pourquoi le retour sur dépenses publicitaires diminue-t-il pour ce package ?</li></ul> | La réponse inclut des facteurs qui limitent les performances et fournit des recommandations pour résoudre les problèmes. |
| [Informations](insights-agent.md) | Obtenez des mesures de campagne et des rapports complets sans créer manuellement de rapport. Vous pouvez poser des questions simples sur une mesure spécifique, telle que les dépenses ou le CPA pour une campagne, ou demander un rapport plus complexe pour une dimension spécifique (telle qu’une campagne unique, un emplacement ou une audience) ou entre les dimensions (pour les répartitions par campagne et par annonceur). Vous pouvez télécharger les résultats au format CSV. | <ul><li>Combien a dépensé [Campaign Name] la semaine dernière ?<li>Combien de conversions [Nom de la campagne] a-t-il obtenues ce mois-ci ?</li><li>Quels sont les stages qui accusent un retard de plus de 20 % ?</li></li>Afficher le CPA par package pour [Nom de la campagne]</li></ul> | Les premières lignes du rapport s’affichent avec des liens pour prévisualiser le rapport complet et télécharger le rapport sous la forme d’un fichier de valeurs séparées par des virgules [!DNL Microsoft Excel] (.csv). |
| [Recherche de documentation du produit](documentation-search.md) | Recherchez du contenu conceptuel et pratique dans le [Guide d’](/help/dsp/home.md) et, pour les annonceurs qui utilisent Advertising Creative, le [Guide d’Advertising Creative](/help/creative/home.md). Les réponses reposent uniquement sur ce qui est documenté pour ces produits dans [&#128279;](https://experienceleague.adobe.com/en/docs/advertising).<br><br>Demandez des informations sur la gestion des campagnes, l’optimisation, la gestion des audiences, les offres, les rapports et d’autres fonctionnalités des produits. | <ul><li>Comment joindre une annonce publicitaire à un emplacement ?</li><li>Quelles sont les options de ciblage disponibles dans Adobe DSP ?</li><li>Quelles sont les conséquences de l’utilisation des différentes options de fréquence dans les paramètres d’emplacement ?</li><li>Quels rapports contiennent des données au niveau des ménages ?</li><li>Comment créer une balise publicitaire pour une expérience [!DNL Creative] ?</li></ul> | La réponse comprend des citations intégrées et une liste de [!UICONTROL Documentation Sources] extensible en bas. Cliquez sur une citation ou une liste de sources pour ouvrir la page correspondante.<br><br>La réponse peut également inclure des questions et des suggestions de suivi pour vous aider à affiner votre requête et à trouver plus d’informations. |

## Ouvrir l’assistant d’IA {#ai-assistant-open}

* Dans le coin supérieur droit d&#39;une page, cliquez sur ![Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

## Développer le bac de conversation

1. En haut de la [chatbox](#ai-assistant-open), cliquez sur ![Enter fullscreen](/help/dsp/assets/fullscreen.png "Enter fullscreen") pour passer en mode plein écran.

1. Pour rétablir le chatbox en mode Panneau, cliquez sur **[!UICONTROL < Back>]**.

<!-- 

No ability to narrow down list of child entities for a selected parent as of 10/26/26.

## Submit a query {#query-submit}

1. [Open AI Assistant](#ai-assistant-open).

1. Build the query:

   * To see examples of queries by topic and optionally copy one to use:
   
     1. Click **[!UICONTROL Learn]**, **[!UICONTROL Troubleshoot]**, or **[!UICONTROL Insights]** to expand the section.
     
     1. (Optional) To copy the text of an example query into the input field:
     
        1. Click the example.
        
        1. (Optional) Edit the text to suit your needs. 

   * To enter your own query:
   
     1. (Insights and troubleshooting queries only; optional) To focus your query on a specific dimension value, such as a specific campaign, click ![Mention an entity](/help/dsp/assets/prompt-entity.png "Mention an entity"), select the dimension, and then select the dimension value.
     
        For example, for the dimension [!UICONTROL Campaign], you can select from a list of all your campaigns to report on.
        
        Available dimensions include:
        
        * Campaign entities: [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
        * The advertiser: [!UICONTROL Advertiser]
        * Advertising Creative entities: [!UICONTROL Experience]
        * Ad targets: [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

     1. Enter your query, and then click ![Submit query](/help/dsp/assets/submit.png "Submit query") or press the **Enter** key on your keyboard.
        
   You can ask multiple questions in one message, but only one message at a time. Wait for a response before sending another.

   >[!NOTE]
   >
   >* (Troubleshooting and insight queries) If you don't specify a date range, then the agent selects a reasonable default based on the type of issue. For example, if you ask about campaign metrics without specifying a date range, then the results are for the duration of the campaign.
   >* (Troubleshooting queries) If you have a target CPA in mind, then include it in your query (for example, "diagnose CPA against a target of $50"). If you don't specify one, then the agent uses a default target.

1. If AI Assistant asks for additional information, provide it.

1. (Product documentation queries only; optional) To open a page used as a data source for the response, do either of the following:

   * Click the numbered citation.

   * Click **[!UICONTROL Documentation Sources]** to show a list of all pages cited in the response, and then click the page link.

>[!IMPORTANT]
>
>AI-generated responses may be inaccurate or misleading. Always verify responses and sources before using them for decisions that affect cost or effort.

>[!TIP]
>
>To ask another query that you want to be saved as a separate thread, [start a new conversation](#conversation-new).

## (Insight queries) Download or preview a full report from the chatbox

* To download a copy of the full report, click ![Export](/help/dsp/assets/download.png "Export").

   The file is downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

* To preview the full report in a side panel, click ![Preview](/help/dsp/assets/agent-chat-preview.png "Preview"). To download the report from the preview, click ![Export](/help/dsp/assets/download.png "Export").

   If you download the report, it's downloaded as a [!DNL Microsoft Excel] comma-separated values file (.csv) according to your browser's normal procedure. The filename is "DSP_Insights_Report_<job_number>."

## Start a new conversation {#conversation-new}

Each conversation, or query thread, is saved separately so you can distinguish between your previous conversations.

1. At the top of the [chatbox](#ai-assistant-open), click ![Start a new conversation](/help/dsp/assets/new-selection.png "Start a new conversation").

1. [Submit a query](#query-submit).

 -->

<!--

## Work with previous conversations

### List previous conversations

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

### Open a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Click the conversation entry.

To repeat the same topic verbatim, copy the key details into a new conversation. Otherwise, you can ask AI Assistant to repeat a finite task within a specific conversation.

### Rename a previous conversation

1. At the top of the [chatbox](#ai-assistant-open), click ![Threads history](/help/dsp/assets/threads.png "Threads history").

1. Next to the conversation entry, click **[!UICONTROL ...] > [!UICONTROL Rename]**.

1. Edit the conversation name, and then click **[!UICONTROL Save]**.

-->

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
