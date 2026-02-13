---
title: Créer une audience réutilisable à l’aide de Generative AI
description: Découvrez comment créer des audiences réutilisables dans Adobe Advertising DSP à l’aide de l’agent d’audience assisté par l’IA. Décrivez votre audience cible dans des invites en langage naturel ; l'agent suggère des segments tiers et crée des expressions d'audience à utiliser comme cibles ou exclusions.
feature: DSP Audiences
hidefromtoc: true
hide: true
exl-id: 82c9f122-2bdd-409f-a4d6-1da21ecbe913
source-git-commit: 4eefcca15d4f84152278e7680917b9daed15f45d
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 0%

---

# Créer une audience réutilisable à l’aide de Generative AI

*Fonction Beta*

*Invites en anglais uniquement*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

Utilisez l’agent d’audience assisté par l’IA pour générer de nouvelles audiences réutilisables à l’aide de tous les segments tiers qui sont disponibles pour vous, en fonction de vos besoins déclarés. Vous pouvez utiliser vos audiences comme cibles ou exclusions pour plusieurs emplacements.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>Cette fonctionnalité est en mode Beta et peut faire l’objet de modifications. Assurez-vous que l’expression d’audience générée représente l’audience souhaitée avant de créer l’audience et de l’utiliser pour vos emplacements.

## Créer une audience réutilisable à l’aide de Generative AI

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

1. Saisissez un **[!UICONTROL Audience Name]** unique.

1. (Facultatif) Désélectionnez l’option à **[!UICONTROL Share with all advertisers in my account]**.

   Lorsque vous partagez une audience, celle-ci devient disponible en tant que cible ou exclusion pour tous les annonceurs du compte. Cependant, les segments individuels de l’audience ne sont disponibles que pour les utilisateurs et utilisatrices auxquels les segments sont partagés.

1. Cliquez sur **[!UICONTROL Save]**.

1. Créez l’audience :

   Pour les utilisateurs disposant d’autorisations bêta, l’option AI est l’option par défaut. Pour [assembler l’audience vous-même](/help/dsp/audiences/reusable-audience-create.md), cliquez sur le bouton « Basculer en mode manuel » en bas.

   1. Saisissez une ou plusieurs invites pour décrire les caractéristiques d&#39;audience que vous souhaitez inclure et exclure. Pour envoyer chaque invite, cliquez sur ![Envoyer une invite](/help/dsp/assets/submit-prompt.png "Envoyer une invite").

      Pour plus d’informations, consultez les sections « [Écriture d’invites](#writing-prompts) » et « [Bonnes pratiques pour créer une synthèse d’audience](#audience-brief-best-practices) ».

      Lorsque l’agent d’IA trouve les segments pertinents, il crée une expression d’audience en fonction de vos critères. Il vous demande également votre approbation avant de rechercher des segments correspondants pour assembler l’audience.

      Vous pouvez éventuellement ignorer la requête et continuer à spécifier des critères d’audience supplémentaires à la place.

   1. Lorsque l’agent d’IA présente une expression d’audience qui décrit de manière adéquate votre audience, demandez à l’agent d’IA de procéder à l’assemblage de l’audience.

      Vous pouvez saisir « continuer », « ok », « ok », « oui » ou un autre mot similaire.

   1. (Si nécessaire) Spécifiez des critères supplémentaires. Lorsque l’agent d’IA présente une expression d’audience qui répond à tous vos critères, demandez à l’agent d’IA de procéder à l’assemblage de l’audience.

1. Lorsque vous êtes satisfait(e) de l’audience assemblée, cliquez sur **[!UICONTROL Create]** pour créer l’audience spécifiée.

   >[!NOTE]
   >
   >Vous ne pouvez pas modifier l’audience par la suite à l’aide de l’agent AI. Au lieu de cela, [modifiez manuellement l’expression de l’audience](/help/dsp/audiences/reusable-audience-edit.md).

## Principes de base de la création d’invites {#writing-prompts}

### Que doit inclure une invite ?

* Utilisez un langage clair et descriptif pour décrire l’audience cible.

  En règle générale, les invites ne respectent pas la casse et la ponctuation n&#39;est pas nécessaire, sauf pour apporter de la clarté.

* Soyez spécifique et fournissez des détails sur toutes les caractéristiques d’audience que vous souhaitez inclure et sur toutes les caractéristiques que vous souhaitez spécifiquement exclure. Plus vous fournissez de détails, plus vous avez de chances d&#39;obtenir les résultats qui répondent à vos besoins.

* Identifiez les emplacements, les types d’appareils et les fournisseurs de données à inclure ou à exclure.

* Fournissez des détails de manière itérative pour affiner vos critères et l’expression d’audience générée avant d’enregistrer l’audience.

* En savoir plus sur les invites à travers l’expérimentation.

  L’agent d’audience n’enregistre pas automatiquement une expression d’audience générée en tant qu’audience. Vous ne pouvez enregistrer une audience qu’en cliquant sur le bouton [!UICONTROL Create], qui se trouve en dehors de la zone d’invite, afin d’annuler les modifications que vous ne souhaitez pas conserver.

Consultez « [&#x200B; Bonnes pratiques pour la création d’une synthèse destinée à une audience »](#audience-brief-best-practices) pour découvrir d’autres moyens d’optimiser les invites pour les audiences.

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### Que ne pouvez-vous pas inclure dans une invite ?

* Références à des expressions d’audience existantes.

* Texte dans d’autres langues que l’anglais.

### Exemples de réponses d’agent d’IA et de réponses

Lorsque l’agent d’IA a besoin d’une réponse de votre part, vous pouvez lui répondre à l’aide de mots-clés dans la requête ou en utilisant des termes courants équivalents.

#### Réponse de l’agent d’IA vous posant une question

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Votre réponse affirmative : « continue », « ok », « ok », « oui », ou un autre mot similaire

Vous pouvez également ignorer la requête et continuer à spécifier des critères d’audience supplémentaires à la place.

#### Réponse de l’agent AI vous demandant de choisir parmi plusieurs options.

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Votre réponse : `1`, `proceed`, `2`, `maximum reach`, etc.

Vous pouvez également ignorer la requête et continuer à spécifier des critères d’audience supplémentaires à la place.

## Bonnes pratiques relatives à la création d’une synthèse destinée à une audience {#audience-brief-best-practices}

Un briefing d’audience est une rédaction stratégique qui définit l’audience cible d’une campagne. Un résumé bien conçu aide l’agent d’audience DSP à identifier les segments les plus pertinents pour assembler votre audience cible.

### Composantes essentielles d’une synthèse efficace des audiences

Incluez autant de types d’attributs d’audience que possible à partir de la liste suivante dans votre résumé. Soyez précis quant aux attributs à exclure.

<!-- What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **Données démographiques**

  Inclut des attributs tels que la tranche d’âge, le sexe, la situation de famille, la composition du ménage (taille de la famille, présence d’enfants, ménages multigénérationnels).

* **Indicateurs socio-économiques**

  Établit la capacité financière en fonction des tranches de revenu des ménages (IHH), du niveau de scolarité, de la profession ou du titre de poste, de la situation d&#39;emploi et de la situation de propriétaire.

* **Paramètres géographiques**

  Définit la portée de la localisation, y compris le pays/les pays, la région (EMEA, APAC, NA), la densité de population (urbaine/suburbaine/rurale).

* **Centres d’intérêt et affinités**

  Identifie les passions et les préférences telles que les hobbies (sports, arts, activités de plein air), les modes de consommation des médias, les affinités avec la marque et les activités de style de vie (voyages, repas, divertissement).

* **Psychographie**

  Capture l’état d’esprit et les valeurs, y compris les aspirations (recherche du statut, amélioration de soi), les valeurs fondamentales (durabilité, innovation, tradition), les traits de personnalité (preneurs de risques, utilisateurs précoces) et les motivations d’achat.

* **Signaux Comportementaux**

  Actions observables, notamment le comportement d’achat (fréquence d’achat, préférences de canal, fidélité à la marque), le comportement en ligne (visites de site web, engagement sur le contenu, activité sur les médias sociaux) et le comportement hors ligne (visites de magasin, participation à un événement, adhésions).

* **Intention Sur Le Marché**

  Détermine le niveau de préparation à l’achat par le biais des catégories de produits/services faisant l’objet de recherches, du calendrier d’achat (immédiat, à court terme, à long terme) et des événements personnels pertinents déclenchant les décisions d’achat.

* **Étape de la vie**

  Compréhension de la phase actuelle, y compris le stade de la carrière (étudiant, débutant, à mi-carrière, cadre, retraité), le stade familial (nouveau-marié, nouveau-parent, nourrisson vide) et les transitions majeures de la vie.

### Exemple d’exposé d’audience bien structuré pour une campagne de prospection

Voici un exemple de brief d’audience fort pour une campagne de sensibilisation et d’essai pour un service d’abonnement à un kit de repas haut de gamme :

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [Dupliquer une audience réutilisable](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [Modifier une audience réutilisable](/help/dsp/audiences/reusable-audience-edit.md)
>* [Afficher les détails sur une audience réutilisable](/help/dsp/audiences/reusable-audience-view-details.md)
>* [Partage d’une audience réutilisable](/help/dsp/audiences/reusable-audience-share.md)
>* [Exporter une audience réutilisable](/help/dsp/audiences/reusable-audience-export.md)
>* [Copiez la clé de segment pour une audience réutilisable dans le presse-papiers](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [Supprimer une audience réutilisable](/help/dsp/audiences/reusable-audience-delete.md)
