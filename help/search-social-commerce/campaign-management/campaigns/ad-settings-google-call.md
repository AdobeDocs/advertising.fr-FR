---
title: '[!DNL Google Ads] des paramètres de publicité d’appel uniquement'
description: Référencez les paramètres des annonces  [!DNL Google Ads]  appel uniquement.
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/KtnceFJbgZ-jPcNzl1c6XychNzr4tOIs5B9mMbXegxo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 333
ht-degree: 0%

---

# [!DNL Google Ads] des paramètres de publicité d’appel uniquement

Vous pouvez créer des annonces textuelles accessibles uniquement par appel pour les campagnes qui utilisent le réseau de recherche.

Search, Social et Commerce effectuent le suivi des annonces d’appels uniquement à l’aide du suffixe de page de destination au niveau du compte et du modèle de suivi, mais vous pouvez éventuellement remplacer le suivi au niveau du compte au niveau de l’annonce dans [!DNL Google Ads] Manager.

Voir l’aide [!DNL Google Ads] pour connaître les [limites publicitaires par compte](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** Nom de l’entreprise. La longueur maximale est de 25 caractères ou 12 caractères codés sur deux octets.

**[!UICONTROL Country]:** (facultatif) Pays dans lequel l’entreprise est située.

**[!UICONTROL Phone Number]:** Numéro de téléphone de l’entreprise. Exemples : (124) 123-4567, 12345678901, +441234567890.

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** première et deuxième lignes du corps de l’annonce publicitaire. La longueur maximale de chaque ligne est de 35 caractères ou 17 caractères codés sur deux octets.

La syntaxe de substitution des mots-clés n&#39;est pas prise en compte dans la longueur maximale. Par exemple, « `{Description1: Free Account Analysis!}` » est traité comme 22 caractères (uniquement la partie « Analyse de compte gratuite »).

>[!NOTE]
>
>Les champs de description ne peuvent pas inclure de numéros de téléphone.

**[!UICONTROL Display URL]:** URL affichée dans la publicité. L’URL d’affichage doit correspondre à un domaine associé à votre entreprise, mais la publicité n’envoie pas de personnes vers une page de destination.

La longueur maximale est de 35 caractères codés sur un octet ou 17 caractères codés sur deux octets. La syntaxe de substitution des mots-clés n&#39;est pas prise en compte dans la longueur maximale. Par exemple, « `{DisplayURL: example.com}` » est traité comme 11 caractères (uniquement la partie « example.com »).

**[!UICONTROL Verification URL]:** (facultatif) Page web sur laquelle le numéro de téléphone de votre publicité s’affiche sous forme de texte, afin que [!DNL Google Ads] puissiez vérifier que le numéro de téléphone est valide. Il doit avoir le même domaine que l’URL d’affichage de la publicité.

**[!UICONTROL Is Tracked]:** active le suivi des appels et les conversions d’appel uniquement.

**[!UICONTROL Count calls as phone call conversions]:** (Lorsque « [!UICONTROL Is Tracked] » est sélectionné, facultatif) Attribue tous les appels qui résultent de l’annonce à un type spécifique de conversion d’appel téléphonique, lorsqu’il est spécifié. Sinon, [!DNL Google Ads] crée une action de conversion par défaut appelée « [!UICONTROL Calls from ads] » une fois qu’elle enregistre au moins une conversion à partir de vos numéros de transfert, puis lui attribue des appels.

**[!UICONTROL Count Action]:** (lorsque « [!UICONTROL Count calls as phone call conversions] » est sélectionné ; facultatif) Action de conversion existante à laquelle les appels sont attribués.

Vous pouvez créer et gérer des actions de conversion dans [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [À propos des publicités](ad-about.md)
>* [Gérer les publicités](ad-manage.md)
>* [[!DNL Google Ads] paramètres d’annonce de recherche dynamique développés](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] paramètres des annonces de recherches réactives](ad-settings-google-rsa.md)
