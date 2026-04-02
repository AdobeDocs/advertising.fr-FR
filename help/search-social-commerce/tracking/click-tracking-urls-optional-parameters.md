---
title: Paramètres de tracking optionnels des URL de tracking des clics
description: Découvrez les paramètres de suivi facultatifs Search, Social et Commerce, ainsi que les paramètres de suivi spécifiques au réseau publicitaire que vous pouvez ajouter à vos URL de suivi des clics.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
TQID: https://experienceleague.adobe.com/6T2yZGYK-Mp97D0YRqPoS7Qyb5gp8jX-boK6KQjHB2E
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1074
ht-degree: 0%

---

# Paramètres de tracking optionnels des URL de tracking des clics

Comptes *[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan] et [!DNL Yandex] uniquement*

Au lieu d’utiliser uniquement les paramètres de suivi standard pour une URL finale ou une URL de destination, vous pouvez ajouter d’autres paramètres pour suivre des données spécifiques pour un compte de réseau publicitaire. Vous pouvez ajouter n’importe quelle combinaison des paramètres suivants dans les paramètres du compte ou de la campagne :

* Vous pouvez ajouter n’importe quelle chaîne de texte statique en tant que paramètre dans les URL de base du compte ou de la campagne.

* Vous pouvez ajouter des paramètres spécifiques à Adobe Advertising et au réseau publicitaire dans les URL de base pour que le compte/la campagne suive davantage de données :

   * Les paramètres Adobe Advertising sont semi-statiques. Adobe Advertising insère une valeur de données lorsqu’il charge l’URL de base sur le réseau publicitaire. Par exemple, lorsque vous ajoutez des `campaign={ef_campaign}` à l’URL de base, Adobe Advertising remplace `{ef_campaign}` par le nom réel de la campagne (tel que « Back-to-school-Campaign ») lorsqu’il charge l’URL.

     **Remarque :** une fois les valeurs insérées, elles restent statiques. Si vous déplacez un mot-clé ou une annonce publicitaire vers un autre groupe publicitaire, ou si vous déplacez le groupe publicitaire vers une autre campagne, le paramètre {ef_adgroup} ou {ef_campaign} n’est pas automatiquement mis à jour. Vous devez donc générer manuellement une nouvelle URL de destination ou une URL de base (finale).

   * Les paramètres spécifiques au réseau publicitaire sont dynamiques et le moteur de recherche insère une valeur de données lorsque l’utilisateur clique sur une publicité. Par exemple, lorsque vous ajoutez des `{param1}` à l’URL de base, le réseau publicitaire la remplace par la valeur {param1} réelle lorsqu’un utilisateur final clique sur la publicité.

>[!NOTE]
>
>* Séparez plusieurs paramètres par des virgules ou des esperluettes (`&`).
>* Les paramètres suivants ne sont pas sensibles à la casse.
>* Les caractères spéciaux dans les paramètres ajoutés sont remplacés comme suit dans l’URL de destination générée ou l’URL de base (finale) :
>  * `=` est remplacé par `%3D`
>  * `?` est remplacé par `%26`
>  * un espace vide est remplacé par `%2B`
>  Par exemple, lorsque vous ajoutez le paramètre `campaign={ef_campaign}` à l’URL de base http://www.example.com pour un mot-clé, l’URL de base de ce mot-clé est générée comme `http://www.example.com/campaign%3D{ef_campaign}`.

## Paramètres de suivi statique Search, Social et Commerce

Vous pouvez utiliser les paramètres suivants pour les comptes de n’importe quel réseau publicitaire et les combiner avec des paramètres pour un réseau publicitaire spécifique, si nécessaire. Certains de ces paramètres dupliquent les paramètres qui sont ajoutés automatiquement pour des réseaux publicitaires spécifiques lorsque la méthode de suivi du compte est « [!UICONTROL EF Direct] ».

Tous les paramètres suivants doivent être spécifiés sous la forme d’une paire clé-valeur ; vous pouvez inclure plusieurs paramètres pour une paire valeur. Par exemple, pour insérer le nom de la campagne, utilisez `<your_parameter_name>={ef_campaign}`, tel que `campaign={ef_campaign}`. Pour insérer le type de correspondance à l’aide des noms de type de correspondance spécifiés, utilisez `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, par exemple `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. Les types de correspondance non applicables n’apparaissent pas dans l’URL résultante.

| Paramètre | Description |
| ---- | ---- |
| <code>{custom_code}</code> | Pour insérer des données de la colonne « Paramètre d’URL personnalisé » dans un fichier de feuille d’envoi groupé chargé dans l’URL de suivi. {custom_code} ne peut être utilisé qu’à la fin de la valeur d’une ou de plusieurs paires clé-valeur dans l’URL de tracking. Exemples : <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Remarque :</b> pour insérer la valeur personnalisée du fichier de feuille d&#39;envoi groupé dans l&#39;URL de suivi, chargez le fichier de feuille d&#39;envoi groupé à l&#39;aide de l&#39;option « Générer les URL de suivi ». Pour plus d’informations sur l’utilisation des fichiers de feuilles d’envoi groupé, voir « [À propos de la gestion des données de campagne à l’aide des feuilles d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) ». |
| <code>{ef_uniqueid}</code> | Pour insérer l&#39;identifiant unique créé par Adobe Advertising : Ajouté automatiquement lorsque la méthode de tracking est « Redirection EF ». |
| <code>{ef_userid}</code> | Pour insérer l’ID utilisateur unique qu’Adobe Advertising attribue à l’annonceur. |
| <code>{ef_sid}</code> | Pour insérer l’identifiant numérique que Search, Social et Commerce attribue au réseau publicitaire : <i>[!UICONTROL 3]</i> pour [!DNL Google Ads], <i>[!UICONTROL 10]</i> pour [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> pour [!DNL Meta], <i>[!UICONTROL 86]</i> pour [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> pour [!DNL Naver], <i>[!UICONTROL 88]</i> pour [!DNL Baidu], <i>[!UICONTROL 90]</i> pour [!DNL Yandex], <i>[!UICONTROL 94]</i> pour [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> pour [!DNL Yahoo Native], <i>[!UICONTROL 106]</i> pour [!DNL Pinterest] (obsolète) ou pour (obsolète). |
| <code>{ef_searchengine}</code> | Pour insérer le nom du réseau publicitaire. |
| <code>{ef_campaign}</code> | Pour insérer le nom de la campagne. |
| <code>{ef_campaignid}</code> | Pour insérer l’identifiant de campagne. <b>Remarque :</b> l’identifiant d’une nouvelle campagne n’est pas créé tant que celle-ci n’est pas publiée sur le réseau publicitaire. Si le compte utilise les options « [!UICONTROL EF Redirect] » et « Chargement automatique », Adobe Advertising insère automatiquement l’identifiant de campagne dans les URL de destination appropriées ou les URL finales le lendemain. Si le compte n’utilise pas les options « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] » et que vous souhaitez insérer l’identifiant de campagne dans les URL de destination appropriées ou les URL finales, vous devez créer la campagne, télécharger un fichier de feuille d’envoi groupé pour la nouvelle campagne à l’aide de l’option « Générer les URL de suivi », puis publier le fichier sur le réseau publicitaire. |
| <code>{ef_adgroup}</code> | Pour insérer le nom du groupe publicitaire. |
| <code>{ef_adgroupid}</code> | Pour insérer l’ID de groupe publicitaire. <b>Remarque :</b> l’ID d’un nouveau groupe publicitaire n’est pas créé tant que le groupe publicitaire n’est pas publié sur le réseau publicitaire. Si le compte utilise les options « [!UICONTROL EF Redirect] » et « Chargement automatique », Adobe Advertising insère automatiquement l’identifiant du groupe publicitaire dans les URL de destination appropriées ou les URL finales le lendemain. Si le compte n’utilise pas les options [!UICONTROL EF Redirect] » et [!UICONTROL Auto Upload] » et que vous souhaitez insérer l’identifiant du groupe publicitaire dans les URL de destination appropriées ou les URL finales, vous devez créer le groupe publicitaire, télécharger un fichier de feuille d’envoi groupé pour le nouveau groupe publicitaire à l’aide de l’option « Générer des URL de suivi », puis publier le fichier sur le réseau publicitaire. |
| <code>{ef_keyword}</code> | Pour insérer le mot-clé. |
| <code>{ef_keywordid}</code> | Pour insérer l’ID de mot-clé. <b>Remarque :</b> l’ID d’un nouveau mot-clé n’est pas créé tant que le mot-clé n’est pas publié sur le réseau publicitaire. Si le compte utilise les options « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Adobe Advertising insère automatiquement l’identifiant du mot-clé dans les URL de destination appropriées ou les URL finales le lendemain. Si le compte n’utilise pas les options « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] » et que vous souhaitez insérer l’identifiant du mot-clé dans les URL de destination appropriées ou les URL finales, vous devez créer le mot-clé ; télécharger un fichier de feuille d’envoi groupé pour le nouveau mot-clé, à l’aide de l’option « Générer des URL de suivi ; », puis publier le fichier sur le réseau publicitaire. |
| <code>{ef_matchtype}</code> | Pour insérer le type de correspondance de mot-clé en tant que « Large », « Exact » ou « Expression ». Inclus automatiquement pour [!DNL Google Ads] et [!DNL Microsoft Advertising] avec la méthode de tracking « [!UICONTROL EF Redirect] ». |
| <code>{ef_adid}</code> | Pour insérer l’ID de publicité. <b>Remarque :</b> l’ID d’une nouvelle publicité n’est pas créé tant que celle-ci n’est pas publiée sur le réseau publicitaire. Si le compte utilise les options « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] », Adobe Advertising insère automatiquement l’ID d’annonce publicitaire dans les URL de destination appropriées ou les URL finales le lendemain. Si le compte n’utilise pas les options « [!UICONTROL EF Redirect] » et « [!UICONTROL Auto Upload] » et que vous souhaitez insérer l’ID d’annonce publicitaire dans les URL de destination appropriées ou les URL finales, vous devez créer l’annonce publicitaire, télécharger un fichier de feuille d’envoi groupé pour la nouvelle annonce publicitaire à l’aide de l’option « Générer des URL de suivi », puis publier le fichier sur le réseau publicitaire. |

## [!DNL Google Ads] des paramètres de tracking dynamique

Voir [&#128279;](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft Advertising] des paramètres de tracking dynamique

Voir [&#128279;](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo ! Paramètres de tracking dynamique des publicités japonaises

Voir [&#128279;](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] des paramètres de tracking dynamique

Voir [&#128279;](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi des conversions Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
