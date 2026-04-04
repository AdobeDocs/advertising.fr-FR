---
title: Modifier une règle  [!DNL Google Ads]  valeur de conversion
description: Découvrez comment modifier  [!DNL Google Ads]  règles de valeur de conversion.
source-git-commit: efb4b80337b36b3b631898ca9ed66e99227468f1
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# Modification d’une règle de valeur de conversion [!DNL Google Ads]

Vous pouvez modifier une règle de valeur de conversion dans les comptes/campagnes pour lesquels les conversions sont suivies au niveau du compte individuel ou à un niveau inférieur. Vous ne pouvez pas modifier une règle pour un compte avec des conversions entre comptes qui sont suivies au niveau du compte principal.

1. Dans le menu principal, cliquez sur **[!UICONTROL Goals]>[!UICONTROL Conversion Value Rules]**.

   Par défaut, l’onglet **[!UICONTROL Campaign]** est sélectionné pour afficher toutes les règles au niveau de la campagne.

1. (Facultatif) Pour afficher toutes les règles au niveau du compte à la place, cliquez sur l’onglet **[!UICONTROL Account]** .

1. Cochez la case en regard de la règle.

1. Dans la barre d’outils d’actions en bloc,

   * Pour activer (activer) les règles en pause, cliquez sur (/help/search-social-commerce/assets/edit-new.png « Modifier).

1. Modifiez le [paramètres des règles de conversion](google-conversion-value-rule-settings.md).

   Vous ne pouvez pas modifier les types de conditions d’une règle existante, mais vous pouvez modifier les conditions et les ajustements de valeur.

   Vous devez configurer une condition principale et un ajustement de valeur. Vous pouvez éventuellement configurer une condition secondaire.

   **Remarque :** si vous ajoutez une condition secondaire, elle doit être du même type que les autres règles du compte. Par exemple, si la règle 1 d’autres règles du compte ont la condition secondaire « Emplacement », alors, lorsque les autres règles incluent une condition secondaire, la condition secondaire doit être « Emplacement ». Lorsque vous incluez une condition secondaire, celle-ci est jointe à la condition principale à l&#39;aide de l&#39;opérateur booléen ALL, de sorte que les deux conditions doivent être remplies pour lancer un ajustement de valeur.

1. Cliquez sur **[!UICONTROL Review and Save]** pour consulter les paramètres.

1. Cliquez sur **[!UICONTROL Save]**.

>[!MORELIKETHIS]
>
>* [À propos [!DNL Google Ads] des règles de valeur de conversion](about-google-conversion-value-rules.md)
>* [Créer une règle  [!DNL Google Ads]  valeur de conversion](create-google-conversion-value-rule.md)
>* [Modifier le statut d’une règle  [!DNL Google Ads]  valeur de conversion](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads] paramètres des règles de valeur de conversion](google-conversion-value-rule-settings.md)

