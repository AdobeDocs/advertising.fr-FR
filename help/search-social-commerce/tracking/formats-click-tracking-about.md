---
title: À propos des formats d’URL de suivi des clics pour le service de suivi de conversion Adobe Advertising
description: Découvrez les formats de suivi des clics pour les réseaux publicitaires pris en charge.
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# À propos des formats d’URL de suivi des clics pour le service de suivi de conversion Adobe Advertising

Les modèles de suivi, les suffixes de page d’entrée (suffixes d’URL finales) et les URL de destination pour les comptes publicitaires et les campagnes qui utilisent le service de suivi de conversion d’Adobe Advertising ont le format suivant :

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

où :

* `http://pixel.everesttech.net` redirige l’utilisateur vers les serveurs de pixels d’Adobe Advertising.

* `<advertiser_ID>` est une variable de l’identifiant utilisateur unique attribué à l’annonceur dans Adobe Advertising.

* `<token passing parameter>` est une variable pour l’une des variables suivantes :

   * `cq?` ou `rq` indique que le transfert de jeton est activé.

   * `c?` ou `r` indique que le transfert de jeton est désactivé.

* `<ad network ID>` est une variable de l&#39;identifiant numérique du réseau publicitaire spécifié, tel que *3* pour [!DNL Google Ads], *10* pour [!DNL Microsoft Advertising], *45* pour [!DNL Meta], *86* pour [!DNL Yahoo! Display Network], *87* pour [!DNL Naver], 16}88 *pour [!DNL Baidu],* 90 *pour [!DNL Yandex],* 94 *pour [!DNL Yahoo! Japan Ads],* 105 *pour [!DNL Yahoo Native] (obsolète) ou* 106{26 9} pour [!DNL Pinterest] (obsolète).**

* `<tracking ID>` est une variable pour une chaîne d’identifiant de suivi générée par le système qui identifie un mot-clé, une publicité ou un emplacement unique dans le compte. La chaîne varie selon le réseau publicitaire.

* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés. Pour les comptes avec des URL de destination, cette valeur est une URL. Pour les comptes avec modèles de suivi, cette valeur est un paramètre (tel que `{lpurl}`) qui représente l’URL finale.

Consultez les pages distinctes indiquant les [[!DNL Baidu] formats](formats-click-tracking-baidu.md), [[!DNL Google Ads] formats](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formats](formats-click-tracking-microsoft.md), [[!DNL Naver] formats](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] formats](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formats](formats-click-tracking-yahoo-japan.md) et [[!DNL Yandex] formats](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Formats de suivi des clics pour [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Formats de suivi des clics pour [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Naver]](formats-click-tracking-naver.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yandex]](formats-click-tracking-yandex.md)
