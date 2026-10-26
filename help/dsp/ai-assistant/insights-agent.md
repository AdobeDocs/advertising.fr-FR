---
title: Créer des rapports à l’aide de l’assistant AI
description: Découvrez comment utiliser l’agent d’informations de l’assistant Adobe Advertising DSP AI pour interroger les mesures de campagne, générer des rapports et télécharger des fichiers CSV.
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
source-git-commit: ffe7424d4e225a95b279b06a7df3b85bf0cbcdbf
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%
---
# Créer des rapports à l’aide de l’assistant AI

*Fonction*

Utilisez l’agent d’informations de l’assistant d’IA pour obtenir des mesures et des rapports complets pour vos campagnes, composants de campagne, expériences Advertising Creative, annonceurs et cibles publicitaires, sans créer manuellement de rapport. Vous pouvez poser des questions simples sur une mesure spécifique, telle que les dépenses ou le CPA pour une campagne, ou demander un rapport plus complexe pour une dimension spécifique (telle qu’une campagne ou une audience unique) ou entre les dimensions (pour les répartitions pour chaque campagne et annonceur). Vous pouvez télécharger les résultats au format CSV.

>[!IMPORTANT]
>
>Les réponses générées par l&#39;IA peuvent être inexactes ou trompeuses. Vérifiez toujours les réponses et les sources avant de les utiliser pour les décisions qui affectent les coûts ou les efforts.

## Exemples de requêtes

* Combien a dépensé [Campaign Name] la semaine dernière ?

* Combien de conversions [Nom de la campagne] a-t-il obtenues ce mois-ci ?

* Afficher le CPA par package pour [Nom de la campagne].

* Quels sont les stages qui accusent un retard de plus de 20 % ?

* Comparez les dépenses nettes pour toutes les campagnes et tous les packages au cours des 15 derniers jours.

## Envoyer une requête

Vous pouvez poser plusieurs questions dans un seul message, mais un seul message à la fois. Attendez une réponse avant d’en envoyer une autre.

1. Dans le coin supérieur droit d&#39;une page, cliquez sur ![Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

1. Créez la requête :

   1. Effectuez l’une des opérations suivantes :

      * Saisissez votre propre requête.

      * Pour voir des exemples de requêtes :

        1. Cliquez sur **[!UICONTROL Insights]** pour développer la section.

        1. (Facultatif) Pour copier le texte d’un exemple de requête dans le champ de saisie :

           1. Cliquez sur l’exemple.

           1. (Facultatif) Modifiez le texte en fonction de vos besoins.

   1. (Facultatif) Pour concentrer votre requête sur une valeur de dimension spécifique (une campagne spécifique, par exemple), insérez éventuellement le curseur à l’endroit où vous souhaitez que la valeur de dimension apparaisse, cliquez sur ![Mentionner une entité](/help/dsp/assets/prompt-entity.png "Mentionner une entité"), sélectionnez la dimension, puis sélectionnez la valeur de dimension.

      Par exemple, pour la dimension [!UICONTROL Campaign], vous pouvez effectuer un choix dans une liste de toutes les campagnes pour lesquelles créer des rapports.

      Les dimensions disponibles sont les suivantes :

      * Entités de la campagne : [!UICONTROL Campaign], [!UICONTROL Package], [!UICONTROL Placement], [!UICONTROL Ad]
      * L&#39;annonceur : [!UICONTROL Advertiser]
      * Entités Advertising Creative : [!UICONTROL Experience]
      * Cibles publicitaires : [!UICONTROL Audience], [!UICONTROL City], [!UICONTROL Country], [!UICONTROL State], [!UICONTROL DMA], [!UICONTROL Retargeting Pixel], [!UICONTROL Device OS], [!UICONTROL Device Browser], [!UICONTROL Device Type], [!UICONTROL Zip Code]

   Pour plus d’informations sur les requêtes, voir « [ Bonnes pratiques relatives à l’écriture de requêtes et d’invites ](ai-assistant-about.md#writing-queries). »

1. Cliquez sur ![Envoyer la requête](/help/dsp/assets/submit-prompt.png "Envoyer la requête") ou appuyez sur la touche **Entrée** du clavier. Si l’agent demande des informations supplémentaires, fournissez les informations requises.

   Les premières lignes du rapport s’affichent avec des liens pour prévisualiser le rapport complet et télécharger le rapport.

   Quelques lignes du rapport généré s’affichent.

>[!TIP]
>
>Pour poser des questions sur un autre problème, ou sur un autre package ou emplacement, [démarrez une nouvelle conversation](#conversation-new).

## Téléchargez ou prévisualisez un rapport complet à partir du chatbox

* Pour télécharger une copie du rapport complet, cliquez sur ![Export](/help/dsp/assets/download.png "Export").

  Le fichier est téléchargé sous la forme d’un fichier de valeurs séparées par des virgules [!DNL Microsoft Excel] (.csv), conformément à la procédure normale de votre navigateur. Le nom du fichier est « DSP_Insights_Report_&lt;job_number> ».

* Pour prévisualiser le rapport complet dans un panneau latéral, cliquez sur ![Aperçu](/help/dsp/assets/agent-chat-preview.png "Aperçu"). Pour télécharger le rapport à partir de l’aperçu, cliquez sur ![Exporter](/help/dsp/assets/download.png "Exporter").

  Si vous téléchargez le rapport, il est téléchargé sous la forme d’un fichier de valeurs séparées par des virgules (.csv) [!DNL Microsoft Excel], conformément à la procédure normale de votre navigateur. Le nom du fichier est « DSP_Insights_Report_&lt;job_number> ».

## Démarrer une nouvelle conversation {#conversation-new}

Chaque conversation, ou thread de requête, est enregistré séparément afin que vous puissiez distinguer vos conversations précédentes.

1. Dans la partie supérieure du [chatbox](#ai-assistant-open), cliquez sur ![Démarrer une nouvelle conversation](/help/dsp/assets/new-selection.png "Démarrer une nouvelle conversation").

1. [Envoyer une requête](#query-submit).

## Développez et réduisez le bac de conversation

1. En haut de la [chatbox](#ai-assistant-open), cliquez sur ![Enter fullscreen](/help/dsp/assets/fullscreen.png "Enter fullscreen") pour passer en mode plein écran.

1. Pour rétablir le chatbox en mode Panneau, cliquez sur **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [À propos de l’assistant AI dans Advertising DSP](ai-assistant-about.md)
>* [Utiliser les conversations précédentes de l’assistant AI](previous-conversations.md)
