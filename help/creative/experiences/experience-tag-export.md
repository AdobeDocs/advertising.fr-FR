---
title: Exporter et implémenter une balise d’expérience publicitaire pour une expérience en direct
description: Découvrez comment exporter une balise d’expérience publicitaire et éventuellement la charger dans une campagne Advertising DSP.
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: e79becc860143b749ec96134e7b224649686c672
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Exporter et implémenter une balise d’expérience publicitaire pour une expérience en direct

*Version bêta fermée*

Une fois qu’une balise publicitaire pour une taille de contenu créatif ou une durée vidéo spécifiques est disponible pour une expérience [en direct](experience-about.md#experience-statuses), vous pouvez générer et copier la balise dans des formats JavaScript, iframe et vidéo pour une implémentation sur Advertising DSP ou d’autres DSP. Les balises pour DSP incluent toutes les macros requises pour DSP.

Les annonceurs qui utilisent Advertising DSP ont la possibilité de charger les balises directement dans une campagne Advertising DSP sous la forme de publicités avec le type « affichage standard » ou « vidéo universelle ».

>[!NOTE]
>
>* Lorsque vous créez une expérience avec le ciblage d’arborescence de décision, [!DNL Creative] crée automatiquement une balise d’annonce publicitaire pour chaque taille de contenu créatif applicable (contenus créatifs non vidéo) ou durée de la vidéo (contenus créatifs vidéo).
>* Lorsque vous créez une expérience sans ciblage d’arborescence de décision, vous devez [créer manuellement une balise d’annonce publicitaire](experience-tag-create-manually.md) pour chaque taille de contenu créatif applicable (contenus non vidéo) ou durée de la vidéo (contenus vidéo).
>* Les balises Experience sont dynamiques. Il n’est pas nécessaire de mettre à jour les balises si vous modifiez une expérience.
>* Assurez-vous que les campagnes dans lesquelles vous implémenterez une expérience publicitaire incluent un ciblage compatible avec l’expérience. Le comportement de ciblage hiérarchique peut varier en fonction du DSP. Dans Advertising DSP, le ciblage au niveau des annonces s’applique en plus du ciblage au niveau de l’emplacement (et non à la place de celui-ci).

1. Dans le menu principal, cliquez sur **[!UICONTROL Creative]** > **[!UICONTROL Experiences]**.

1. Effectuez l’une des opérations suivantes <!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * En mode Carte, cliquez sur **[!UICONTROL ...]** en regard du nom de l’expérience, puis cliquez sur **[!UICONTROL Tag Manager]**.

   * En mode Tableau, maintenez le curseur sur la ligne, cliquez sur **[!UICONTROL More]**, puis sur **[!UICONTROL Tag Manager]**.

1. Placez le curseur sur la ligne de la balise publicitaire applicable et cliquez sur ![Exporter les balises publicitaires](/help/creative/assets/export.png "Exporter les balises publicitaires") **[!UICONTROL Export ad tags]** ou **[!UICONTROL ... More] > &#x200B;** [!UICONTROL Export ad tags]**.

>[!NOTE]
>
>Pour les expériences publicitaires vidéo standard, attendez que la colonne [!UICONTROL Tag Status] affiche « [!UICONTROL Ready] », qui indique que toutes les vidéos de l’expérience ont été transcodées. Toutes les vidéos publicitaires sont automatiquement transcodées par DSP. Vous pouvez toutefois appliquer le transcodage [pour un autre DSP](experience-tag-video-transcoding.md) à n’importe quelle balise d’expérience publicitaire vidéo.

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. (Facultatif) Dans l’onglet [!UICONTROL Macros] , spécifiez jusqu’à cinq macros personnalisées à inclure dans la balise . Pour chaque macro à inclure :

   1. Cochez une case.<!-- Explain more -->

   1. Saisissez la macro personnalisée.<!-- Explain more -->

1. Cliquez sur **[!UICONTROL Next]** dans le coin supérieur droit ou sur **[!UICONTROL Generate ad tags]** dans le menu de gauche.

1. Sélectionnez le type de balise :

   * (Expériences non vidéo) ** *JavaScript<!-- sic -->* **&#x200B; ou &#x200B;** *IFRAME* ** <!-- sic -->.

   * (Expériences vidéo) **&#x200B; *Vidéo* &#x200B;**.

1. Dans la liste [!UICONTROL Destinations], sélectionnez l’emplacement où vous allez créer des annonces pour l’expérience.

   * *Générique :* pour les publicités que vous allez créer dans d’autres DSP. **Remarque :** vous devrez peut-être inclure manuellement [macros supplémentaires](/help/creative/creative-macros.md) si nécessaire.

   * *Adobe AdCloud :* pour les publicités que vous allez créer dans Advertising DSP.

   * *CM360 Google :* pour les publicités que vous allez créer dans [!DNL Google Campaign Manager 360]. **Remarque :** vous devrez peut-être inclure manuellement [macros supplémentaires](/help/creative/creative-macros.md) si nécessaire.

1. Cliquez sur **[!UICONTROL Generate tags]**.

1. Copiez ou téléchargez les balises :

   * Pour copier une balise pour une seule taille d’annonce (annonces non vidéo) ou pour une seule durée (annonces vidéo), développez la ligne de balise, placez le curseur sur la ligne, puis cliquez sur ![Copier](/help/creative/assets/copy.png "Copier") **[!UICONTROL Copy]**.<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * Pour télécharger toutes les balises générées sous forme de fichier vers l’emplacement de téléchargement par défaut de votre navigateur, cliquez sur ![Télécharger les balises](/help/creative/assets/download.png "Télécharger les balises").

   Vous pouvez ouvrir le fichier dans un éditeur de texte pour copier chaque balise. Pour les balises JavaScript, la balise est placée entre les balises `<script></script>` et `<noscript></noscript>`. Pour les balises iframe, la balise est placée entre des balises `<iframe></iframe>`.

1. Implémentez les balises pour le DSP approprié :

   * Pour les DSP autres qu’Advertising DSP, fournissez les balises à la personne qui créera les publicités dans DSP.

   * Pour Advertising DSP :

      1. Cliquez sur **[!UICONTROL Next]** dans le coin supérieur droit ou sur **[!UICONTROL DSP link]** dans le menu de gauche.

      1. Sélectionnez la campagne sur laquelle vous souhaitez charger la balise de publicité.

      1. Cliquez sur **[!UICONTROL Assign Tags]**.

         DSP s’ouvre dans la vue [!UICONTROL Ads] de la campagne sélectionnée.

      1. Dans la vue [!UICONTROL Create ads], passez en revue les balises d’annonce publicitaire, sélectionnez chaque balise pour laquelle vous souhaitez créer une annonce, puis cliquez sur **[!UICONTROL Create]**.

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [Créez manuellement une balise d’annonce publicitaire pour une taille de contenu créatif applicable](experience-tag-create-manually.md)
>* [Affecter des contenus publicitaires à une balise publicitaire pour des expériences sans ciblage](experience-tag-assign-creatives.md)
>* [Renommer une balise publicitaire](experience-tag-rename.md)
>* [Personnalisation des options de transcodage pour une balise d’expérience d’annonce vidéo](experience-tag-video-transcoding.md)
