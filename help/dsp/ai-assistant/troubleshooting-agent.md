---
title: Résoudre les problèmes de performances et de diffusion à l’aide de l’assistant AI
description: Utilisez l’agent de dépannage de l’assistant Adobe Advertising DSP AI pour diagnostiquer les problèmes de dépenses, de fréquence et de diffusion pour les packages et emplacements DSP.
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
source-git-commit: 41d3ab985831a1432e775277384661643a9f55c4
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%
---
# Résolution des problèmes de performances et de diffusion à l’aide de l’assistant AI


*Fonction*

L&#39;agent de dépannage d&#39;AI Assistant identifie les facteurs qui limitent les performances des packages et des emplacements en direct et fournit des instructions et des recommandations étape par étape basées sur les données historiques pour résoudre les problèmes. L’agent de dépannage peut vous aider à diagnostiquer les types de problèmes de performances et de diffusion suivants :

* (Emplacements uniquement) Questions relatives aux dépenses, y compris les dépenses excessives, les dépenses insuffisantes et l’incapacité de dépenser. L&#39;agent évalue les facteurs de fréquence, d&#39;enchères, de ciblage et de plafonnement budgétaire associés dans le cadre du diagnostic.

* (Packages uniquement) Problèmes de performances, notamment une augmentation du CPA ou un retour sur dépenses publicitaires en baisse. L’agent ne diagnostique pas les mesures d’engagement telles que le taux de clics, le taux de clic ou les impressions.

Chaque conversation couvre un seul diagnostic pour un seul package ou emplacement. Une fois que l&#39;agent a obtenu un résultat, commencez une nouvelle conversation pour poser des questions sur un autre problème ou sur un autre package ou emplacement.

L’agent ne peut pas modifier les paramètres, créer ou modifier des campagnes ou des composants de campagne, ni diagnostiquer des problèmes pour un emplacement ou un package en pause, terminé, archivé ou planifié.

>[!IMPORTANT]
>
>Les réponses générées par l&#39;IA peuvent être inexactes ou trompeuses. Vérifiez toujours les réponses et les sources avant de les utiliser pour les décisions qui affectent les coûts ou les efforts.

## Exemples de requêtes

### Résolution des problèmes liés aux dépenses d’emplacement

* Mon placement a cessé de dépenser hier même si l&#39;affaire est active. Pourquoi ?

* Pourquoi ce placement a-t-il été sous-utilisé au cours des 5 derniers jours ?

* Nous sommes à mi-chemin du vol et nous accusons un retard important par rapport au rythme. Pourquoi ?

### Résolution des problèmes de performances des packages

* Pourquoi l&#39;ACP a-t-elle augmenté pour ce paquet au cours de la semaine dernière ?

* Pourquoi le retour sur dépenses publicitaires diminue-t-il pour ce package ?

## Envoyer une requête à partir de l’assistant AI

Vous pouvez poser plusieurs questions dans un seul message, mais un seul message à la fois. Attendez une réponse avant d’en envoyer une autre.

1. Dans le coin supérieur droit d&#39;une page, cliquez sur ![Chat](/help/dsp/assets/agent-chat.png "Agentic chat").

1. Créez la requête :

   * Saisissez votre propre requête.

   * Pour afficher des exemples de requêtes, cliquez sur **[!UICONTROL Troubleshoot]** pour développer la section.

     1. (Facultatif) Pour copier le texte d’un exemple de requête dans le champ de saisie :

        1. Cliquez sur l’exemple.

        1. (Facultatif) Modifiez le texte en fonction de vos besoins.

   Pour plus d’informations sur les requêtes, voir « [&#x200B; Bonnes pratiques relatives à l’écriture de requêtes et d’invites &#x200B;](ai-assistant-about.md#writing-queries). »

   >[!NOTE]
   >
   >* Si vous ne spécifiez pas de période, l’agent sélectionne une valeur par défaut raisonnable en fonction du type de problème. Par exemple, si vous posez des questions sur les mesures de campagne sans spécifier de période, les résultats concernent la durée de la campagne.
   >* Si vous avez une CPA cible en tête, incluez-la dans votre requête (par exemple, « Diagnostiquer une CPA par rapport à une cible de 50 $ »). Si vous n’en spécifiez pas, l’agent utilise une cible par défaut.

1. Cliquez sur ![Envoyer la requête](/help/dsp/assets/submit-prompt.png "Envoyer la requête") ou appuyez sur la touche **Entrée** du clavier.

1. Si l’assistant AI vous demande des informations supplémentaires, indiquez-les.

>[!TIP]
>
>Pour poser des questions sur un autre problème, ou sur un autre package ou emplacement, [démarrez une nouvelle conversation](#conversation-new).

## Envoyer une requête à partir de la vue [!UICONTROL Packages] ou [!UICONTROL Placements]

Vous pouvez poser plusieurs questions dans un seul message, mais un seul message à la fois. Attendez une réponse avant d’en envoyer une autre.

1. Dans le menu principal, cliquez sur **[!UICONTROL Campaigns]**.

1. Cliquez sur le nom de la campagne.

1. Effectuez l’une des opérations suivantes :

   * (Pour les packages) Dans la vue [!UICONTROL Packages], cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]** en regard du nom du package.

   * (Pour les emplacements) Dans le sous-menu, cliquez sur **[!UICONTROL Placements]**. En regard du nom de l’emplacement, cliquez sur **[!UICONTROL ...]** > **[!UICONTROL Troubleshooting Agent]**.

1. Créez la requête :

   * Saisissez votre propre requête.

   * Pour afficher des exemples de requêtes, cliquez sur **[!UICONTROL Troubleshoot]** pour développer la section.

     1. (Facultatif) Pour copier le texte d’un exemple de requête dans le champ de saisie :

        1. Cliquez sur l’exemple.

        1. (Facultatif) Modifiez le texte en fonction de vos besoins.

   Pour plus d’informations sur les requêtes, voir « [&#x200B; Bonnes pratiques relatives à l’écriture de requêtes et d’invites &#x200B;](ai-assistant-about.md#writing-queries). »

   >[!NOTE]
   >
   >* Si vous ne spécifiez pas de période, l’agent sélectionne une valeur par défaut raisonnable en fonction du type de problème. Par exemple, si vous posez des questions sur les mesures de campagne sans spécifier de période, les résultats concernent la durée de la campagne.
   >* Si vous avez une CPA cible en tête, incluez-la dans votre requête (par exemple, « Diagnostiquer une CPA par rapport à une cible de 50 $ »). Si vous n’en spécifiez pas, l’agent utilise une cible par défaut.

1. Cliquez sur ![Envoyer la requête](/help/dsp/assets/submit-prompt.png "Envoyer la requête") ou appuyez sur la touche **Entrée** du clavier.

1. Si l’assistant AI vous demande des informations supplémentaires, indiquez-les.

>[!TIP]
>
>Pour poser des questions sur un autre problème, ou sur un autre package ou emplacement, [démarrez une nouvelle conversation](#conversation-new).

## Démarrer une nouvelle conversation {#conversation-new}

Chaque conversation (ou thread de requête) est enregistré séparément afin que vous puissiez distinguer vos conversations précédentes.

1. Dans la partie supérieure du [chatbox](#ai-assistant-open), cliquez sur ![Démarrer une nouvelle conversation](/help/dsp/assets/new-selection.png "Démarrer une nouvelle conversation").

1. [Envoyer une requête](#query-submit).

## Développez et réduisez le bac de conversation

1. En haut de la [chatbox](#ai-assistant-open), cliquez sur ![Enter fullscreen](/help/dsp/assets/fullscreen.png "Enter fullscreen") pour passer en mode plein écran.

1. Pour rétablir le chatbox en mode Panneau, cliquez sur **[!UICONTROL < Back>]**.

>[!MORELIKETHIS]
>
>* [À propos de l’assistant AI dans Advertising DSP](ai-assistant-about.md)
>* [Utiliser les conversations précédentes de l’assistant AI](previous-conversations.md)
