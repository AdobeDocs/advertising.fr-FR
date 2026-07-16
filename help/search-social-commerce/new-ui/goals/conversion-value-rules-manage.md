---
title: (Nouvelle interface utilisateur) Gestion  [!DNL Google Ads]  règles de valeur de conversion
description: Découvrez comment afficher et gérer les règles  [!DNL Google Ads]  valeur de conversion dans Search, Social et Commerce.
feature: Conversions
feature_v2:
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: a2f79fa9-a8fe-4c1c-961e-75dc3c47f954
source-git-commit: e36a2b66a8dc4c485c7139b44eaf375615826b2b
workflow-type: tm+mt
source-wordcount: 1854
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gérer [!DNL Google Ads] règles de valeur de conversion

*Fonction*

[!DNL Google Ads] [règles de valeur de conversion](https://support.google.com/google-ads/answer/10518330) vous permettent d’ajuster les valeurs des événements de conversion en fonction des informations de l’utilisateur, y compris le type d’appareil, l’emplacement et le segment d’audience. Vous pouvez utiliser des règles pour les enchères basées sur la valeur dans les campagnes de recherche, d’affichage, d’achat et de performances maximales avec les enchères intelligentes Google. Pour les campagnes avec les stratégies d’enchères Maximiser les conversions et Retour sur les dépenses publicitaires cible , [!DNL Google Ads] algorithmes commencent à préférer les conversions de valeur supérieure.

Les règles de valeur de conversion au niveau de la campagne remplacent les règles au niveau du compte. Lorsqu’une conversion satisfait à plusieurs règles de valeur de conversion, une seule des règles est appliquée. En règle générale, la règle la plus spécifique est appliquée. Consultez toutefois la [[!DNL Google Ads] documentation sur les priorités pour les différents types de conditions de règle](https://support.google.com/google-ads/answer/10520348).

## Vue et fonctionnalité [!UICONTROL Conversion Value Rules]

Search, Social et Commerce synchronise automatiquement les règles de valeur de conversion de vos comptes [!DNL Google Ads]. Toutes les règles créées dans l’interface [!DNL Google Ads] sont synchronisées dans les 24 heures et sont disponibles dans la vue [!UICONTROL Goals] > [!UICONTROL Conversion Value Rules] .

Certains comptes peuvent gérer leurs règles de valeur de conversion :

* Dans les comptes pour lesquels les conversions sont suivies au niveau du compte individuel ou de la campagne, vous pouvez [créer](#google-conversion-value-rule-create), [modifier](#google-conversion-value-rule-edit) et [modifier le statut](#google-conversion-value-rule-change-status) de vos règles au niveau du compte et de la campagne.

  Les comptes peuvent être liés aux [[!DNL Google Ads] comptes du responsable](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md), mais ils ne peuvent pas utiliser le suivi des conversions entre comptes (pour lequel les conversions sont suivies sur tous les comptes du compte du responsable).

* Dans les comptes qui utilisent le suivi des conversions entre comptes, vos règles au niveau du compte et de la campagne sont héritées du compte du responsable et sont en lecture seule.

## Règles de valeur de conversion avec les portfolios Search, Social et Commerce

Lorsque le compte de l’annonceur est configuré pour charger les objectifs Search, Social et Commerce vers [!DNL Google Ads] et que vous incluez une campagne qui utilise une règle de valeur de conversion dans un portfolio avec un objectif , [!DNL Google Ads] applique la règle de valeur de conversion à la valeur de conversion d’origine spécifiée dans l’objectif . Par conséquent, les données de conversion dans Search, Social et Commerce diffèrent des données de conversion dans [!DNL Google Ads].

Supposons, par exemple, que l’objectif utilise une mesure de conversion unique « Leads » et donne aux conversions provenant d’appareils mobiles un poids de 10 et aux conversions provenant d’appareils non mobiles un poids de 10. Search, Social et Commerce comptabilise un événement de l’un des types d’appareils comme une (1) conversion et attribue à la valeur de conversion la valeur 10. Cependant, supposons qu’une campagne de ce portefeuille utilise une règle de valeur de conversion « Si l’appareil est mobile, multipliez par 2 ». Lorsqu’un événement Leads mobile est suivi pour cette campagne, [!DNL Google Ads] attribue également au nombre de conversions la valeur un (1), mais à la valeur de conversion (10 x 2) = 20.

Pour obtenir plus d’informations sur vos règles, y compris les valeurs de conversion d’origine avant l’application des règles, consultez le rapport [&#x200B; règles de valeur de conversion dans  [!DNL Google Ads]](https://support.google.com/google-ads/answer/10519848).

## Créer une règle de valeur de conversion [!DNL Google Ads] {#google-conversion-value-rule-create}

Vous pouvez créer des règles de valeur de conversion au niveau du compte et de la campagne dans des comptes [!DNL Google Ads] pour lesquels les conversions sont suivies au niveau du compte individuel ou à un niveau inférieur. Vous ne pouvez pas créer de règles pour les comptes avec des conversions entre comptes qui font l’objet d’un suivi au niveau du compte principal.

Chaque règle comprend jusqu’à deux conditions, ainsi que l’ajustement de la valeur de conversion à appliquer lorsque les conditions sont remplies. Toutes les règles d’un compte doivent utiliser le même type de conditions principales et secondaires (facultatives). Par exemple, si la règle 1 inclut la condition principale « Audience » et la condition secondaire « Emplacement », toutes les autres règles du compte doivent avoir la condition principale « Audience ». Lorsque les autres règles incluent une condition secondaire, elle doit être « Emplacement ».

Vous pouvez créer plusieurs règles au niveau de la campagne pour chaque campagne. Cependant, [!DNL Google Ads] ne permet pas encore de créer des règles au niveau du compte en dehors de l’éditeur de [!DNL Google Ads] lorsqu’une règle au niveau du compte existe déjà. Pour créer des règles supplémentaires au niveau du compte, connectez-vous directement à [!DNL Google Ads] et utilisez l’éditeur de [!DNL Google Ads].

**Remarque :** les règles de valeur de conversion au niveau de la campagne remplacent les règles au niveau du compte, et une seule règle peut être appliquée à une conversion. Pour plus d’informations, voir [comment [!DNL Google Ads] détermine quelle règle est appliquée à une conversion lorsque celle-ci remplit les conditions de plusieurs règles](https://support.google.com/google-ads/answer/10520348).

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Par défaut, l’onglet **[!UICONTROL Campaign]** est sélectionné pour afficher toutes les règles au niveau de la campagne.

1. (Facultatif) Pour créer une règle au niveau du compte à la place, cliquez sur l’onglet **[!UICONTROL Account]** .

1. Dans la barre d’outils, cliquez sur **[!UICONTROL Create Campaign Rule]** (dans l’onglet [!UICONTROL Campaign] ) ou **[!UICONTROL Create Account Rule]** (dans l’onglet [!UICONTROL Account] ).

1. Sélectionnez le réseau publicitaire et le compte. Pour les règles au niveau de la campagne, sélectionnez également la campagne. Cliquez ensuite sur **[!UICONTROL Next]**.

1. Configurez le [paramètres des règles de conversion](#google-ads-conversion-value-rule-settings).

   Vous devez configurer une condition principale et un ajustement de valeur. Vous pouvez éventuellement configurer une condition secondaire.

   Dans une condition, plusieurs cibles ou exclusions sont reliées à l&#39;aide de l&#39;opérateur booléen `OR`, de sorte que toute option peut être respectée pour lancer un ajustement de valeur. Lorsque vous incluez une condition secondaire, celle-ci est jointe à la condition principale à l&#39;aide de la `ALL` d&#39;opérateur booléenne. Les deux conditions doivent donc être remplies pour lancer un ajustement de valeur. Exemple : si \[L’emplacement est Algérie OU Tunisie\] ET \[L’appareil est mobile OU tablette\], ajoutez 1,5.

   **Remarque :** toutes les règles d’un compte doivent utiliser le même type de conditions principales et secondaires (facultatives). Par exemple, si la règle 1 inclut la condition principale « Audience » et la condition secondaire « Emplacement », toutes les autres règles du compte doivent avoir la condition principale « Audience ». Lorsque les autres règles incluent une condition secondaire, elle doit être « Emplacement ».

1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

1. Cliquez sur **[!UICONTROL Save]**.

## Modification d’une règle de valeur de conversion [!DNL Google Ads] {#google-conversion-value-rule-edit}

Vous pouvez modifier une règle de valeur de conversion dans les comptes/campagnes pour lesquels les conversions sont suivies au niveau du compte individuel ou à un niveau inférieur. Vous ne pouvez pas modifier une règle pour un compte avec des conversions entre comptes qui sont suivies au niveau du compte principal.

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Par défaut, l’onglet **[!UICONTROL Campaign]** est sélectionné pour afficher toutes les règles au niveau de la campagne.

1. (Facultatif) Pour afficher toutes les règles au niveau du compte à la place, cliquez sur l’onglet **[!UICONTROL Account]** .

1. Cochez la case en regard de la règle.

1. Dans la barre d’outils des actions en bloc, cliquez sur (/help/search-social-commerce/assets/edit-new.png « Modifier).

1. Modifiez le [paramètres des règles de conversion](#google-ads-conversion-value-rule-settings).

   Vous ne pouvez pas modifier les types de conditions d’une règle existante, mais vous pouvez modifier les conditions et les ajustements de valeur.

   Vous devez configurer une condition principale et un ajustement de valeur. Vous pouvez éventuellement configurer une condition secondaire.

   **Remarque :** si vous ajoutez une condition secondaire, elle doit être du même type que les autres règles du compte. Par exemple, si la règle 1 d’autres règles du compte ont la condition secondaire « Emplacement », alors, lorsque les autres règles incluent une condition secondaire, la condition secondaire doit être « Emplacement ». Lorsque vous incluez une condition secondaire, celle-ci est jointe à la condition principale à l&#39;aide de la `ALL` d&#39;opérateur booléenne. Les deux conditions doivent donc être remplies pour lancer un ajustement de valeur.

1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

1. Cliquez sur **[!UICONTROL Save]**.

## Modifier le statut d’une règle de valeur de conversion [!DNL Google Ads] {#google-conversion-value-rule-change-status}

Vous pouvez suspendre, activer ou supprimer une règle de valeur de conversion dans les comptes et campagnes pour lesquels les conversions sont suivies au niveau du compte individuel.

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Par défaut, l’onglet **[!UICONTROL Campaign]** est sélectionné pour afficher toutes les règles au niveau de la campagne.

1. (Facultatif) Pour afficher toutes les règles au niveau du compte à la place, cliquez sur l’onglet **[!UICONTROL Account]** .

1. Cochez la case en regard de chaque ligne à modifier.

1. Dans la barre d’outils d’actions en bloc,

   * Pour activer (activer) les règles en pause, cliquez sur **[!UICONTROL ...]>[!UICONTROL Activate]**.

   * Pour suspendre les règles actives, cliquez sur **[!UICONTROL ...]>[!UICONTROL Pause]**.

   * Pour supprimer des règles actives ou en pause, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer").

1. Dans le message de confirmation, cliquez sur **[!UICONTROL Confirm]**.

## [!DNL Google Ads] des paramètres des règles de valeur de conversion {#google-conversion-value-rule-settings}

| Section | Paramètre | Description |
|---|---|---|
| [!UICONTROL Select Campaign] | [!UICONTROL Network] | Le réseau publicitaire. |
| | [!UICONTROL Account] | Compte réseau publicitaire. |
| | [!UICONTROL Campaign] | (Règles de valeur de conversion au niveau de la campagne uniquement) La campagne publicitaire. |
| [!UICONTROL Conditions] > [!UICONTROL Primary Condition] | \[Type de condition\] | (Lecture seule pour les règles existantes) Type de condition qui doit être remplie pour déclencher un ajustement de valeur :<ul><li>*[!UICONTROL Device]:* pour cibler tous les types d’appareils ou certains types d’appareils.</li><li>*[!UICONTROL Location]:* Cibler tous les pays et territoires ou cibler et exclure des emplacements spécifiques.</li><li>*[!UICONTROL Audiences]:* pour cibler toutes les audiences ou des audiences spécifiques</li></ul>**Remarque :** toutes les règles d’un compte doivent utiliser le même type de conditions principales et secondaires (facultatives). Par exemple, si la règle 1 inclut la condition principale « Audience » et la condition secondaire « Emplacement », toutes les autres règles du compte doivent avoir la condition principale « Audience ». Lorsque les autres règles incluent une condition secondaire, elle doit être « Emplacement ». |
| | \[Type de condition\] > [!UICONTROL Device] et [!UICONTROL Device Level] | (Conditions de l’appareil uniquement) Types d’appareils à cibler :<ul><li>*[!UICONTROL All devices]:** pour cibler tous les types d’appareils.</li><li>*[!UICONTROL Select devices]:* Pour spécifier un ou plusieurs types d’appareils à cibler : *[!UICONTROL Desktop]:*, *[!UICONTROL Mobile]* et *[!UICONTROL Tablet]:*.</li></ul>Dans une condition, plusieurs cibles sont reliées à l’aide de l’opérateur booléen `OR`, de sorte que toute option peut être respectée pour lancer un ajustement de valeur. Exemple : si \[Appareil est Mobile OU Tablette\], alors Ajoutez 1.5. |
| | \[Type de condition\] > [!UICONTROL Location] et [!UICONTROL Location Level] | (Conditions d’emplacement uniquement) Cibles et exclusions d’emplacement :<ul><li>*[!UICONTROL All countries and territories]:* pour cibler tous les pays et emplacements ou pour cibler et exclure des emplacements spécifiques.</li><li>*[!UICONTROL Enter a location]:* pour cibler et exclure des emplacements spécifiques.</li></ul><ul><li>Pour développer un emplacement ou un sous-emplacement, cliquez sur `>` après le nom.</li><li>Pour ajouter une cible, sélectionnez-la une fois pour afficher une coche verte.</li><li>Pour exclure une cible, sélectionnez-la une seconde fois pour afficher une **[!UICONTROL X]** rouge.</li><li>Pour supprimer une cible ou une exclusion, effectuez l’une des opérations suivantes :<ul><li>Cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer") en regard de l’élément dans la colonne [!UICONTROL Selections].</li><li>Sélectionnez la cible jusqu’à ce qu’aucune coche ou [!UICONTROL X] ne s’affiche.</li></ul></li></ul>Dans une condition, plusieurs cibles ou exclusions sont reliées à l&#39;aide de l&#39;opérateur booléen `OR`, de sorte que toute option peut être respectée pour lancer un ajustement de valeur. Exemple : si \[L’emplacement est Algérie OU Tunisie\], alors ajoutez 1,5. |
| | \[Type de condition\] > [!UICONTROL Audience] et [!UICONTROL Audience Level] | (Conditions d’audience uniquement) L’audience cible :<ul><li>*[!UICONTROL All audience segments]:* pour cibler tous les segments d’audience [!DNL Google Ads].</li><li>*[!UICONTROL Enter audience segments]:* pour cibler des segments d’audience [!DNL Google Ads] spécifiques.</li></ul><ul><li>Pour développer une catégorie ou une sous-catégorie dans ses segments, cliquez sur `>` après le nom.</li><li>Pour ajouter une cible, sélectionnez-la.</li><li>Pour supprimer une cible, désélectionnez-la ou cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer") en regard de l’élément dans la colonne [!UICONTROL Selection].</li></ul>Dans une condition, plusieurs cibles ou exclusions sont reliées à l&#39;aide de l&#39;opérateur booléen OU, de sorte que toute option peut être respectée pour lancer un ajustement de valeur. Exemple : si \[l’audience est une audience de voyage de bonne affaire OU de vacances en famille\], alors ajoutez 1.5.<br><br>**Remarque :** une fois que vous avez enregistré une cible d’audience, vous pouvez ajouter d’autres audiences, mais vous ne pouvez pas les supprimer en dehors de l’éditeur de [!DNL Google Ads]. Si vous devez supprimer une cible d’audience, connectez-vous directement à [!DNL Google Ads] et utilisez l’éditeur de [!DNL Google Ads]. |
| [!UICONTROL Conditions] > [!UICONTROL Secondary Condition] | \[Type de condition\] | (Facultatif ; lecture seule pour les règles existantes) Type de condition qui doit être remplie pour déclencher un ajustement de valeur. Lorsque vous incluez une condition secondaire, celle-ci est jointe à la condition principale à l&#39;aide de la `ALL` d&#39;opérateur booléenne. Les deux conditions doivent donc être remplies pour lancer un ajustement de valeur. Exemple : si \[L’emplacement est Algérie OU Tunisie\] ET \[L’appareil est mobile OU tablette\], ajoutez 1.5.<br><br>Consultez les entrées pour les conditions principales pour les descriptions.<br><br>**Remarque :** toutes les règles d’un compte doivent utiliser le même type de conditions principales et de conditions secondaires (facultatives). Par exemple, si la règle 1 inclut la condition principale « Audience » et la condition secondaire « Emplacement », toutes les autres règles du compte doivent avoir la condition principale « Audience ». Lorsque les autres règles incluent une condition secondaire, elle doit être « Emplacement ». |
| [!UICONTROL Value Adjustment] | [!UICONTROL Adjustment Operation] et [!UICONTROL Adjustment Value] | Indiquez le type d&#39;ajustement, puis entrez une valeur positive :<ul><li>*[!UICONTROL Add]:* Ajoute la valeur spécifiée à la valeur de conversion transmise. La valeur doit être supérieure à zéro (0).</li><li>*[!UICONTROL Multiply]:* Multiplie la valeur de conversion transmise par la valeur spécifiée. La valeur doit être comprise entre 0,5 et 10.</li></ul> |

<!--
>[!MORELIKETHIS]
>
>* 
-->
