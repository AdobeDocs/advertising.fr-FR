---
title: Créer une règle  [!DNL Google Ads]  valeur de conversion
description: Découvrez comment créer  [!DNL Google Ads]  règles de valeur de conversion.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 0%

---

# Créer une règle de valeur de conversion [!DNL Google Ads]

Vous pouvez créer des règles de valeur de conversion au niveau du compte et de la campagne dans des comptes [!DNL Google Ads] pour lesquels les conversions sont suivies au niveau du compte individuel ou à un niveau inférieur. Vous ne pouvez pas créer de règles pour les comptes avec des conversions entre comptes qui font l’objet d’un suivi au niveau du compte principal.

Chaque règle comprend jusqu’à deux conditions, ainsi que l’ajustement de la valeur de conversion à appliquer lorsque les conditions sont remplies. Toutes les règles d’un compte doivent utiliser le même type de conditions principales et secondaires (facultatives). Par exemple, si la règle 1 inclut la condition principale « Audience » et la condition secondaire « Emplacement », toutes les autres règles du compte doivent avoir la condition principale « Audience ». Lorsque les autres règles incluent une condition secondaire, elle doit être « Emplacement ».

Vous pouvez créer plusieurs règles au niveau de la campagne pour chaque campagne. Cependant, [!DNL Google Ads] ne permet pas encore de créer des règles au niveau du compte en dehors de l’éditeur de [!DNL Google Ads] lorsqu’une règle au niveau du compte existe déjà. Pour créer des règles supplémentaires au niveau du compte, connectez-vous directement à [!DNL Google Ads] et utilisez l’éditeur de [!DNL Google Ads].

**Remarque :** les règles de valeur de conversion au niveau de la campagne remplacent les règles au niveau du compte, et une seule règle peut être appliquée à une conversion. Pour plus d’informations, voir [comment [!DNL Google Ads] détermine quelle règle est appliquée à une conversion lorsque celle-ci remplit les conditions de plusieurs règles](https://support.google.com/google-ads/answer/10520348).

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Par défaut, l’onglet **[!UICONTROL Campaign]** est sélectionné pour afficher toutes les règles au niveau de la campagne.

1. (Facultatif) Pour créer une règle au niveau du compte à la place, cliquez sur l’onglet **[!UICONTROL Account]** .

1. Dans la barre d’outils, cliquez sur ![Créer](/help/search-social-commerce/assets/add.png "Créer").<!-- Upload newer icon -->

1. Sélectionnez le réseau publicitaire et le compte. Pour les règles au niveau de la campagne, sélectionnez également la campagne. Cliquez ensuite sur **[!UICONTROL Next]**.

1. Configurez le [paramètres des règles de conversion](google-conversion-value-rule-settings.md).

   Vous devez configurer une condition principale et un ajustement de valeur. Vous pouvez éventuellement configurer une condition secondaire.

   Dans une condition, plusieurs cibles ou exclusions sont reliées à l&#39;aide de l&#39;opérateur booléen OU, de sorte que toute option peut être respectée pour lancer un ajustement de valeur. Lorsque vous incluez une condition secondaire, celle-ci est jointe à la condition principale à l&#39;aide de l&#39;opérateur booléen ALL, de sorte que les deux conditions doivent être remplies pour lancer un ajustement de valeur. Exemple : si \[L’emplacement est Algérie OU Tunisie\] ET \[L’appareil est mobile OU tablette\], ajoutez 1,5.

   **Remarque :** toutes les règles d’un compte doivent utiliser le même type de conditions principales et secondaires (facultatives). Par exemple, si la règle 1 inclut la condition principale « Audience » et la condition secondaire « Emplacement », toutes les autres règles du compte doivent avoir la condition principale « Audience ». Lorsque les autres règles incluent une condition secondaire, elle doit être « Emplacement ».

1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [À propos [!DNL Google Ads] des règles de valeur de conversion](about-google-conversion-value-rules.md)
>* [Modifier une règle  [!DNL Google Ads]  valeur de conversion](edit-google-conversion-value-rule.md)
>* [Modifier le statut d’une règle  [!DNL Google Ads]  valeur de conversion](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] paramètres des règles de valeur de conversion](google-conversion-value-rule-settings.md)

