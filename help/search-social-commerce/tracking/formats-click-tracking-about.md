---
title: À propos des formats d’URL de suivi des clics pour le service de suivi de conversion Adobe Advertising
description: Découvrez les formats de suivi des clics pour les réseaux publicitaires pris en charge.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 0%

---

# À propos des formats d’URL de suivi des clics pour le service de suivi de conversion Adobe Advertising

Les modèles de suivi, les suffixes de page d’entrée (suffixes d’URL finales) et les URL de destination pour les comptes publicitaires et les campagnes qui utilisent le service de suivi de conversion Advertising Adobe ont le format suivant :

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

où :

* `http://pixel.everesttech.net` redirige l’utilisateur vers les serveurs de pixels Adobe Advertising.

* `<advertiser_ID>` est une variable de l’identifiant utilisateur unique attribué à l’annonceur dans Adobe Advertising.

* `<token passing parameter>` est une variable de l’une des valeurs suivantes :

   * `cq?` ou `rq` indique que la transmission de jeton est activée.

   * `c?` ou `r` indique que la transmission de jeton est désactivée.

* `<ad network ID>` est une variable de l’identifiant numérique pour le réseau publicitaire spécifié, tel que *3* pour [!DNL Google Ads], *10* pour [!DNL Microsoft Advertising], *45* pour [!DNL Meta], *86* pour [!DNL Yahoo! Display Network], *87* pour [!DNL Naver], *88* pour [!DNL Baidu], *90* pour [!DNL Yandex], *94* pour [!DNL Yahoo! Japan Ads], *105* pour [!DNL Yahoo Native] (obsolète) ou *106* pour [!DNL Pinterest] (obsolète).

* `<tracking ID>` est une variable d’une chaîne d’identifiant de suivi générée par le système qui identifie un mot-clé, une publicité ou un emplacement unique dans le compte. La chaîne varie selon le réseau publicitaire.

* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés. Pour les comptes avec des URL de destination, cette valeur est une URL. Pour les comptes avec modèles de suivi, cette valeur est un paramètre (tel que `{lpurl}`) qui représente l’URL finale.

Consultez les pages distinctes indiquant la variable [[!DNL Baidu] formats](formats-click-tracking-baidu.md), [[!DNL Google Ads] formats](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formats](formats-click-tracking-microsoft.md), [[!DNL Naver] formats](formats-click-tracking-naver.md), [[!DNL Yahoo! Display Network] formats](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formats](formats-click-tracking-yahoo-japan.md), et [[!DNL Yandex] formats](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Formats de suivi des clics pour [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Formats de suivi des clics pour [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Naver]](formats-click-tracking-naver.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yahoo! Japan Ads]](formats-click-tracking-yahoo-japan.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yahoo! Display Network]](formats-click-tracking-yahoo-display-network.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur [!DNL Yandex]](formats-click-tracking-yandex.md)

