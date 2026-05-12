---
title: Créer une audience réutilisable
description: Découvrez comment créer des audiences réutilisables composées de segments d’audience et d’autres audiences enregistrées. Vous pouvez éventuellement utiliser un agent d’audience assisté par l’IA en décrivant votre audience cible dans des invites en langage naturel ; l’agent suggère des segments tiers et crée des expressions d’audience à utiliser comme cibles ou exclusions.
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a4b509995f362ed81e00485409b0c729b5130e35
workflow-type: tm+mt
source-wordcount: 1667
ht-degree: 0%

---

# Créer une audience réutilisable

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Vous pouvez enregistrer et gérer des audiences réutilisables, qui sont des groupes de segments d’audience et même d’autres audiences enregistrées, que vous pouvez utiliser comme cibles ou exclusions pour plusieurs emplacements. Créez des audiences manuellement ou utilisez l’agent d’audience assisté par l’IA pour générer de nouvelles audiences réutilisables à l’aide de tous les segments propriétaires et tiers qui sont disponibles pour vous, selon vos besoins déclarés.

>[!NOTE]
>
>(Annonceurs pour lesquels DSP convertit des ID d’e-mail hachés en segments LiveRampID) Les segments d’ID de rampe propriétaires qui ne sont pas joints à un emplacement actif, planifié ou en pause sont suspendus. Dans la liste des segments, le segment est marqué comme étant « En pause automatique ».

## Création manuelle d’une audience réutilisable

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

1. Dans les paramètres [!UICONTROL New Audience] :

   1. Saisissez un **[!UICONTROL Audience Name]** unique.

   1. (Facultatif) Désélectionnez l’option à **[!UICONTROL Share with all advertisers in my account]**.

      Lorsque vous partagez une audience, celle-ci devient disponible en tant que cible ou exclusion pour tous les annonceurs du compte. Cependant, les segments individuels de l’audience ne sont disponibles que pour les utilisateurs et utilisatrices auxquels les segments sont partagés. Par exemple, si vous partagez une audience contenant des segments Adobe Analytics avec un annonceur qui n’est pas mappé au même compte [!DNL Analytics], le segment n’est pas prévisualisé dans cette audience pour cet annonceur. Seuls les segments disponibles pour cet annonceur sont prévisualisés dans l’audience.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Cliquez sur le bouton **[!UICONTROL Switch to manual mode]** dans le panneau de droite.

   L’option AI est la valeur par défaut.

1. Créez l’audience :

   >[!NOTE]
   >
   >À mesure que vous créez l’audience, les [données détaillées sur la taille de l’audience](audience-about.md) sont mises à jour dans le panneau de droite

   * Pour créer manuellement la logique du segment, à l’aide des segments disponibles dans les onglets [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments] et [!UICONTROL Saved Audiences]](audience-settings.md) procédez comme suit.

      * (Facultatif) Recherchez un nom, une description ou un chemin de segment.

        Les résultats de recherche incluent des segments basés sur les termes exacts que vous utilisez. Lorsque vous saisissez plusieurs termes, tous les termes doivent être trouvés pour un segment.

      * Pour ajouter le premier segment, localisez le segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

      * Pour ajouter un segment à un groupe de segments existant :

         1. Cliquez sur le groupe de segments dans le panneau de droite.

         1. (Facultatif) Modifiez la logique de groupe en *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, selon les besoins.

            *[!UICONTROL Exclude All]* n’est pas disponible pour le premier groupe de segments. Pour une audience qui comprend uniquement des exclusions, créez-la sous la forme *[!UICONTROL Include Any]*, puis, au sein d’un emplacement, sélectionnez-la dans le menu Audiences exclues .

         1. Recherchez le nouveau segment dans le panneau de gauche, puis cochez la case en regard du nom du segment.

            Le groupe de segments est automatiquement mis à jour avec le nouveau segment.

      * Pour ajouter un nouveau groupe de segments :

         1. Cliquez sur **[!UICONTROL + New Group]** dans le panneau de droite.

            1. (Facultatif) Modifiez la logique entre le groupe précédent et le nouveau groupe en *[!UICONTROL And]* ou *[!UICONTROL Or]*, selon les besoins.

            1. Recherchez les segments du nouveau groupe dans le panneau de gauche, puis cochez les cases en regard des noms de segment.

            1. (Facultatif) Modifiez la logique de groupe en *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* ou *[!UICONTROL Exclude All]*, selon les besoins.

   * Pour utiliser la logique de segment à partir d’une audience existante :

      1. Copiez la logique de segment de l’audience existante de l’une des manières suivantes :

         * Dans la vue Toutes les audiences, placez le curseur sur la ligne d’audience, puis cliquez sur **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Dans les paramètres de l’audience existante, en haut du panneau logique des segments, cliquez sur **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * Dans un éditeur de texte, créez manuellement la logique du segment à l’aide des identifiants de segment alphanumériques et de la [syntaxe booléenne](audience-segment-logic-syntax.md), puis copiez-la dans le presse-papiers.

      1. Cliquez sur **[!UICONTROL paste in an audience rule to begin building]**, collez la logique de segment existante dans le champ de saisie, puis cliquez sur **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Si l’audience inclut déjà une logique de segment, coller une nouvelle logique de segment remplace la logique existante.

1. Cliquez sur **[!UICONTROL Create]**.

## Créer une audience réutilisable à l’aide de l’IA générative

*Fonction*

*Prise en charge en anglais uniquement*

>[!NOTE]
>
>Cette fonctionnalité est en mode Beta et peut faire l’objet de modifications. Assurez-vous que l’expression d’audience générée représente l’audience souhaitée avant de créer l’audience et de l’utiliser pour vos emplacements.

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. Dans le menu principal, cliquez sur **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. Au-dessus du tableau de données, cliquez sur **[!UICONTROL Create]**.

1. Dans les paramètres [!UICONTROL New Audience] :

   1. Saisissez un **[!UICONTROL Audience Name]** unique.

   1. (Facultatif) Désélectionnez l’option à **[!UICONTROL Share with all advertisers in my account]**.

      Lorsque vous partagez une audience, celle-ci devient disponible en tant que cible ou exclusion pour tous les annonceurs du compte. Cependant, les segments individuels de l’audience ne sont disponibles que pour les utilisateurs et utilisatrices auxquels les segments sont partagés. Par exemple, si vous partagez une audience contenant des segments Adobe Analytics avec un annonceur qui n’est pas mappé au même compte [!DNL Analytics], le segment n’est pas prévisualisé dans cette audience pour cet annonceur. Seuls les segments disponibles pour cet annonceur sont prévisualisés dans l’audience.

   1. Cliquez sur **[!UICONTROL Save]**.

1. Créez l’audience :

   1. Saisissez une ou plusieurs invites pour décrire les caractéristiques d&#39;audience que vous souhaitez inclure et exclure. Pour envoyer chaque invite, cliquez sur ![Envoyer une invite](/help/dsp/assets/submit-prompt.png "Envoyer une invite").

      Pour plus d’informations, consultez les sections « [Écriture d’invites](#writing-prompts) » et « [Bonnes pratiques pour créer un brief d’audience](#audience-brief-best-practices) ».

      Le cas échéant, l’agent suggère des filtres de segment supplémentaires pour vous aider à créer un briefing d’audience plus efficace. Vous pouvez accepter ou rejeter les suggestions.

      Lorsque l’agent d’audience trouve les segments pertinents, il crée une expression d’audience booléenne en fonction de vos critères. Il vous demande également votre approbation avant de rechercher des segments correspondants pour assembler l’audience. Vous pouvez éventuellement ignorer la requête et continuer à spécifier des critères d’audience supplémentaires à la place.

   1. Lorsque l’agent d’audience présente une expression d’audience qui décrit adéquatement votre audience, demandez à l’agent d’audience de procéder à l’assemblage de l’audience.

      Vous pouvez saisir « continuer », « ok », « ok », « oui » ou un autre mot similaire. L’agent répertorie tous les segments suggérés pour chaque caractéristique (comme « Parents »). Développez une caractéristique pour afficher les détails des segments individuels suggérés pour cette caractéristique.

   1. (Si nécessaire) Spécifiez des critères supplémentaires. Lorsque l’agent d’audience présente une expression d’audience qui répond à tous vos critères, dites à l’agent d’audience de procéder à l’assemblage de l’audience.

      Pour assembler l’audience, saisissez « continuer », « ok », « oui » ou un autre mot similaire. L’agent répertorie tous les segments suggérés pour chaque caractéristique (comme « Parents »). Développez une caractéristique pour afficher les détails des segments individuels suggérés pour cette caractéristique.

1. Lorsque vous êtes satisfait(e) de l’audience assemblée, cliquez sur **[!UICONTROL Create]** pour créer l’audience spécifiée.

   >[!NOTE]
   >
   >Vous ne pouvez pas modifier l’audience par la suite à l’aide de l’agent d’audience. Au lieu de cela, [modifiez manuellement l’expression de l’audience](/help/dsp/audiences/reusable-audience-edit.md).

### Principes de base de l’écriture d’invites {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### Que doit inclure une invite ?

* Utilisez un langage clair et descriptif pour décrire l’audience cible.

   * Vous pouvez saisir des phrases complètes ou simplement une chaîne de caractéristiques. La ponctuation n&#39;est pas nécessaire, sauf lorsque cela est nécessaire pour des raisons de clarté.

   * En règle générale, les invites ne respectent pas la casse.

   * L’agent d’audience reconnaît les synonymes les plus courants.

* Soyez spécifique et fournissez des détails sur toutes les caractéristiques d’audience que vous souhaitez inclure et sur toutes les caractéristiques que vous souhaitez spécifiquement exclure. Plus vous fournissez de détails, plus vous avez de chances d&#39;obtenir les résultats qui répondent à vos besoins.

* Identifiez les emplacements, les types d’appareils et les fournisseurs de données à inclure ou à exclure.

* Fournissez des détails de manière itérative pour affiner vos critères et l’expression d’audience générée avant d’enregistrer l’audience.

* En savoir plus sur les invites à travers l’expérimentation.

  Si votre invite n’est pas claire, l’agent d’audience demandera simplement une autre invite, afin que vous puissiez réessayer.

  L’agent d’audience n’enregistre pas automatiquement une expression d’audience générée en tant qu’audience. Vous ne pouvez enregistrer une audience qu’en cliquant sur le bouton [!UICONTROL Create], qui se trouve en dehors de la zone d’invite, afin d’annuler les modifications que vous ne souhaitez pas conserver.

Consultez la rubrique « [Bonnes pratiques pour créer un résumé d’audience](#audience-brief-best-practices) » pour découvrir d’autres moyens d’optimiser les invites pour les audiences.

<!--
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### Que ne pouvez-vous pas inclure dans une invite ?

* Références à des expressions d’audience existantes.

* Texte dans d’autres langues que l’anglais.

#### Exemples de réponses de l’agent d’audience et de réponses

Lorsque l’agent d’audience a besoin d’une réponse de votre part, vous pouvez lui répondre à l’aide de mots-clés dans la requête ou de synonymes courants.

#### Un agent d’audience vous pose une question

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

Votre réponse affirmative : « continue », « ok », « ok », « oui », ou un autre mot similaire

Vous pouvez également ignorer la requête et continuer à spécifier des critères d’audience supplémentaires à la place.

##### Un agent d’audience vous demande de choisir parmi plusieurs options.

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

Votre réponse : `1`, `proceed`, `2`, `maximum reach`, etc.

Vous pouvez également ignorer la requête et continuer à spécifier des critères d’audience supplémentaires à la place.

### Bonnes pratiques pour créer un briefing d’audience {#audience-brief-best-practices}

Un briefing d’audience est une rédaction stratégique qui définit l’audience cible d’une campagne. Un résumé bien conçu aide l’agent d’audience DSP à identifier les segments les plus pertinents pour assembler votre audience cible.

#### Composants essentiels d’une note d’audience efficace

Incluez autant de types d’attributs d’audience que possible à partir de la liste suivante dans votre résumé. Soyez précis quant aux attributs à exclure.

<!--
 What about these:

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

#### Exemple de brief d’audience bien structuré pour une campagne de prospection

Voici un exemple de brief d’audience fort pour une campagne de sensibilisation et d’essai pour un service d’abonnement à un kit de repas haut de gamme :

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [À propos de la gestion des audiences](audience-about.md)
>* [Paramètres de l’audience](audience-settings.md)
>* [Syntaxe de la logique de segment d’audience](audience-segment-logic-syntax.md)
>* [Fournisseurs de données tiers disponibles](third-party-data-providers.md)
>* [Créer et implémenter un segment personnalisé](custom-segment-create.md)
>* [Création et implémentation d’un [!UICONTROL CCPA Opt-Out-of-Sale] segment](ccpa-opt-out-segment-create.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
