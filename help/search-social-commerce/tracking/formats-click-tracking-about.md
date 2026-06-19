---
title: À propos des formats d’URL de suivi des clics pour le service de suivi des conversions d’Adobe Advertising
description: Découvrez les formats de suivi des clics pour les réseaux publicitaires pris en charge.
exl-id: b6f225d5-2268-4b2a-9927-063155ba0dc5
feature: Search Tracking
TQID: https://experienceleague.adobe.com/pVSEKmf45CqsfXMbj8HGDltdgV3wUV2UsAzP94vkijg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# À propos des formats d’URL de suivi des clics pour le service de suivi des conversions d’Adobe Advertising

Les modèles de tracking, les suffixes de page de destination (suffixes d’URL finaux) et les URL de destination pour les comptes publicitaires et les campagnes qui utilisent le service de tracking des conversions d’Adobe Advertising ont le format suivant :

`http://pixel.everesttech.net/<advertiser_ID>/<token passing parameter>?ev_sid=<ad network ID>&<tracking ID>&url=<the landing page>`

où :

* `http://pixel.everesttech.net` redirige l’utilisateur vers les serveurs de pixels d’Adobe Advertising.

* `<advertiser_ID>` est une variable pour l’ID utilisateur unique attribué à l’annonceur dans Adobe Advertising.

* `<token passing parameter>` est une variable pour l’un des éléments suivants :

   * `cq?` ou `rq` indique que la transmission du jeton est activée.

   * `c?` ou `r` indique que la transmission du jeton est désactivée.

* `<ad network ID>` est une variable pour l’ID numérique du réseau publicitaire spécifié, par exemple *3* pour [!DNL Google Ads], *10* pour [!DNL Microsoft Advertising], *45* pour [!DNL Meta], *86* pour [!DNL Yahoo DSP], *87*, [!DNL Naver]88 *,* 90[!DNL Baidu] pour *,* 94[!DNL Yandex] pour *(anciennement*), [!DNL LY Ads]105[!DNL Yahoo! Japan Ads] pour *(obsolète) ou* 106[!DNL Yahoo Native] pour ** [!DNL Pinterest] (obsolète).

* `<tracking ID>` est une variable pour une chaîne d’identifiant de suivi générée par le système qui identifie un mot-clé, une publicité ou un emplacement unique dans le compte. La chaîne varie en fonction du réseau publicitaire.

* `<the landing page>` est une variable qui représente l’URL de votre site vers laquelle les utilisateurs finaux sont dirigés. Pour les comptes avec des URL de destination, cette valeur est une URL. Pour les comptes avec modèles de tracking, cette valeur est un paramètre (tel que `{lpurl}`) qui représente l’URL finale.

Consultez les pages distinctes indiquant les [[!DNL Baidu] formats](formats-click-tracking-baidu.md), [[!DNL Google Ads] formats](formats-click-tracking-google.md), [[!DNL Microsoft Advertising] formats](formats-click-tracking-microsoft.md), [[!DNL Naver] formats](formats-click-tracking-naver.md), [[!DNL Yahoo DSP] formats](formats-click-tracking-yahoo-display-network.md), [[!DNL Yahoo! Japan Ads] formats](formats-click-tracking-yahoo-japan.md) et [[!DNL Yandex] formats](formats-click-tracking-yandex.md).

>[!MORELIKETHIS]
>
>* [Formats de suivi des clics pour les publicités sponsorisées sur  [!DNL Baidu]](formats-click-tracking-baidu.md)
>* [Formats de suivi des clics pour  [!DNL Google Ads]](formats-click-tracking-google.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur  [!DNL LY Ads]](formats-click-tracking-yahoo-japan.md)
>* [Formats de suivi des clics pour  [!DNL Microsoft Advertising]](formats-click-tracking-microsoft.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur  [!DNL Naver]](formats-click-tracking-naver.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur  [!DNL Yahoo DSP]](formats-click-tracking-yahoo-display-network.md)
>* [Formats de suivi des clics pour les publicités sponsorisées sur  [!DNL Yandex]](formats-click-tracking-yandex.md)
