---
title: '[!DNL Google Ads] appel uniquement et paramètres de publicité'
description: Référencez les paramètres pour les  [!DNL Google Ads] annonces Appel uniquement.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads] paramètres de publicité d’appel uniquement

Vous pouvez créer des publicités textuelles avec appel uniquement pour les campagnes qui utilisent le réseau de recherche.

Search, Social et Commerce effectuent le suivi des publicités avec appel uniquement à l’aide du suffixe de page d’entrée et du modèle de suivi au niveau du compte, mais vous pouvez éventuellement remplacer le suivi au niveau du compte au niveau de la publicité dans [!DNL Google Ads] Manager.

Voir l’ [!DNL Google Ads] aide pour [ limites de publicité par compte](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** Nom de l’entreprise. La longueur maximale est de 25 caractères ou 12 caractères sur deux octets.

**[!UICONTROL Country]:** (facultatif) pays dans lequel se trouve l’entreprise.

**[!UICONTROL Phone Number]:** Numéro de téléphone de l’entreprise. Exemples : (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2] :** première et deuxième lignes du corps de la publicité. La longueur maximale de chaque ligne est de 35 caractères ou 17 caractères codés sur deux octets.

La syntaxe de substitution de mot-clé ne compte pas dans la longueur maximale. Par exemple, &quot;`{Description1: Free Account Analysis!}`&quot; est traité comme 22 caractères (uniquement la partie &quot;Analyse de compte libre\!&quot;).

>[!NOTE]
>
>Les champs de description ne peuvent pas inclure de numéros de téléphone.

**[!UICONTROL Display URL]:** URL affichée dans la publicité. L’URL d’affichage doit correspondre à un domaine associé à votre entreprise, mais l’annonce n’envoie pas de personnes vers une page d’entrée.

La longueur maximale est de 35 caractères sur un ou 17 caractères sur deux octets. La syntaxe de substitution de mot-clé ne compte pas dans la longueur maximale. Par exemple, &quot;`{DisplayURL: example.com}`&quot; est traité comme 11 caractères (uniquement la partie &quot;example.com&quot;).

**[!UICONTROL Verification URL]:** (Facultatif) Page web sur laquelle le numéro de téléphone de votre publicité apparaît sous forme de texte, de sorte que [!DNL Google Ads] puisse vérifier que le numéro de téléphone est valide. Il doit avoir le même domaine que l’URL d’affichage de la publicité.

**[!UICONTROL Is Tracked]:** active le suivi des appels et les conversions des appels uniquement.

**[!UICONTROL Count calls as phone call conversions]:** (Lorsque &quot;[!UICONTROL Is Tracked]&quot; est sélectionné ; facultatif) Attribue tous les appels qui résultent de la publicité à un type spécifique de conversion d’appel téléphonique, lorsqu’un appel est spécifié. Sinon, [!DNL Google Ads] crée une action de conversion par défaut appelée &quot;[!UICONTROL Calls from ads]&quot; une fois qu’il enregistre au moins une conversion à partir de vos numéros de transfert, puis attribue des appels à cette dernière.

**[!UICONTROL Count Action]:** (Lorsque &quot;[!UICONTROL Count calls as phone call conversions]&quot; est sélectionné ; facultatif) Action de conversion existante à laquelle les appels sont attribués.

Vous pouvez créer et gérer des actions de conversion dans [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [A propos des publicités](ad-about.md)
>* [Gérer les publicités](ad-manage.md)
>* [[!DNL Google Ads]  Paramètres d’annonce de recherche dynamique étendue ](ad-settings-google-dsa.md)
>* [[!DNL Google Ads]  Paramètres de publicité de recherche réactive ](ad-settings-google-rsa.md)
