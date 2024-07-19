---
title: Paramètres de suivi facultatifs des URL de suivi des clics
description: Découvrez les paramètres de suivi facultatifs Search, Social et Commerce et les paramètres de suivi spécifiques au réseau publicitaire que vous pouvez ajouter à vos URL de suivi des clics.
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: f633f2af545f034b08b378653b4b967710402a03
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# Paramètres de suivi facultatifs des URL de suivi des clics

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan] et [!DNL Yandex] comptes uniquement*

Au lieu d’utiliser uniquement les paramètres de suivi standard pour une URL finale ou une URL de destination, vous pouvez ajouter d’autres paramètres pour effectuer le suivi de données spécifiques pour un compte de réseau publicitaire. Vous pouvez ajouter n’importe quelle combinaison des paramètres suivants dans les paramètres du compte ou dans les paramètres de l’opération :

* Vous pouvez ajouter n’importe quelle chaîne de texte statique en tant que paramètre dans les URL de base du compte/de la campagne.

* Vous pouvez ajouter des paramètres spécifiques à l’Adobe Advertising et au réseau publicitaire dans les URL de base pour que le compte/la campagne effectue le suivi d’autres données :

   * Les paramètres d’Adobe Advertising sont semi-statiques. Adobe Advertising insère une valeur de données lorsqu’il charge l’URL de base sur le réseau publicitaire. Par exemple, lorsque vous ajoutez `campaign={ef_campaign}` à l’URL de base, l’Adobe Advertising remplace `{ef_campaign}` par le nom réel de la campagne (par exemple &quot;Campagne de retour à l’école&quot;) lorsqu’il charge l’URL.

     **Remarque :** Une fois les valeurs insérées, elles restent statiques. Si vous déplacez un mot-clé ou une publicité vers un autre groupe publicitaire, ou déplacez le groupe publicitaire vers une autre campagne, le paramètre {ef_adgroup} ou {ef_campaign} n’est pas automatiquement mis à jour. Vous devez donc générer manuellement une nouvelle URL de destination ou une URL de base (finale).

   * Les paramètres spécifiques au réseau publicitaire sont dynamiques et le moteur de recherche insère une valeur de données lorsque l’utilisateur clique sur une publicité. Par exemple, lorsque vous ajoutez `{param1}` à l’URL de base, le réseau publicitaire le remplace par la valeur {param1} réelle lorsqu’un utilisateur final clique sur la publicité.

>[!NOTE]
>
>* Séparez plusieurs paramètres par des virgules ou des esperluettes (`&`).
>* Les paramètres suivants ne sont pas sensibles à la casse.
>* Les caractères spéciaux des paramètres ajoutés sont remplacés comme suit dans l’URL de destination ou l’URL de base (finale) générée :
>  * `=` est remplacé par `%3D`
>  * `?` est remplacé par `%26`
>  * un espace vide est remplacé par `%2B`
>  Par exemple, lorsque vous ajoutez le paramètre `campaign={ef_campaign}` à l’URL de base http://www.example.com pour un mot-clé, l’URL de base de ce mot-clé est générée sous la forme `http://www.example.com/campaign%3D{ef_campaign}`.

## Paramètres de suivi statique de recherche, Social et Commerce

Vous pouvez utiliser les paramètres suivants pour les comptes sur n’importe quel réseau publicitaire et les combiner avec des paramètres pour un réseau publicitaire spécifique, si nécessaire. Certains de ces paramètres dupliquent les paramètres ajoutés automatiquement pour des réseaux publicitaires spécifiques lorsque la méthode de suivi du compte est &quot;[!UICONTROL EF Direct]&quot;.

Tous les paramètres suivants doivent être spécifiés sous la forme d’une paire clé-valeur. Vous pouvez inclure plusieurs paramètres pour une paire valeur. Par exemple, pour insérer le nom de la campagne, utilisez `<your_parameter_name>={ef_campaign}`, par exemple `campaign={ef_campaign}`. Pour insérer le type de correspondance à l’aide de noms de type de correspondance spécifiés, utilisez `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`, par exemple `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. Les types de correspondance non applicables n’apparaissent pas dans l’URL qui en résulte.

| Paramètre | Description |
| ---- | ---- |
| <code>{custom_code}</code> | Pour insérer des données de la colonne &quot;Paramètre d’URL personnalisé&quot; dans un fichier de feuille d’envoi groupé chargé dans l’URL de suivi. {custom_code} ne peut être utilisé qu&#39;à la fin de la valeur d&#39;une ou de plusieurs paires clé-valeur dans l&#39;URL de suivi. Exemples : <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>Remarque :</b> Pour insérer la valeur personnalisée du fichier de feuille d’envoi groupé dans l’URL de suivi, téléchargez le fichier de feuille d’envoi groupé à l’aide de l’option &quot;Générer les URL de suivi&quot;. Pour plus d’informations sur l’utilisation des fichiers de feuille d’envoi groupé, voir &quot;[À propos de la gestion des données de campagne à l’aide des feuilles d’envoi groupées](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)&quot;. |
| <code>{ef_uniqueid}</code> | Pour insérer l’identifiant unique créé par Adobe Advertising. Ajout automatique lorsque la méthode de suivi est &quot;Redirection EF&quot;. |
| <code>{ef_userid}</code> | Pour insérer l’identifiant utilisateur unique attribué par l’Adobe Advertising à l’annonceur. |
| <code>{ef_sid}</code> | Pour insérer l’identifiant numérique attribué par Search, Social et Commerce au réseau publicitaire : <i>[!UICONTROL 3]</i> pour [!DNL Google Ads], <i>[!UICONTROL 10]</i> pour [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> pour [!DNL Meta], <i>[!UICONTROL 86]</i> pour [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> pour [!DNL Naver], <i>[!UICONTROL 88]</i> pour [!DNL Baidu], <i>[!UICONTROL 90]</i> pour [!DNL Yandex], <i>[!UICONTROL 94]</i> pour [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i>} pour [!DNL Yahoo Native] (obsolète) ou <i>[!UICONTROL 106]</i> pour [!DNL Pinterest] (obsolète). |
| <code>{ef_searchengine}</code> | Pour insérer le nom du réseau publicitaire. |
| <code>{ef_campaign}</code> | Pour insérer le nom de la campagne. |
| <code>{ef_campaignid}</code> | Pour insérer l’identifiant de campagne. <b>Remarque :</b> L’identifiant d’une nouvelle campagne n’est pas créé tant que la campagne n’a pas été publiée sur le réseau publicitaire. Si le compte utilise les options &quot;[!UICONTROL EF Redirect]&quot; et &quot;Chargement automatique&quot;, Adobe Advertising insère automatiquement l’identifiant de campagne dans les URL de destination ou les URL finales appropriées le lendemain. Si le compte n’utilise pas les options &quot;[!UICONTROL EF Redirect]&quot; et [!UICONTROL Auto Upload]&quot; et que vous souhaitez insérer l’identifiant de campagne dans les URL de destination ou les URL finales appropriées, vous devez créer la campagne, télécharger un fichier de feuille d’envoi groupé pour la nouvelle campagne, à l’aide de l’option &quot;Générer les URL de suivi&quot;, puis publier le fichier sur le réseau publicitaire. |
| <code>{ef_adgroup}</code> | Pour insérer le nom du groupe publicitaire. |
| <code>{ef_adgroupid}</code> | Pour insérer l’identifiant du groupe publicitaire. <b>Remarque :</b> L’identifiant d’un nouveau groupe publicitaire n’est pas créé tant que le groupe publicitaire n’a pas été publié sur le réseau publicitaire. Si le compte utilise les options &quot;[!UICONTROL EF Redirect]&quot; et &quot;Chargement automatique&quot;, Adobe Advertising insère automatiquement l’identifiant du groupe publicitaire dans les URL de destination ou les URL finales appropriées le lendemain. Si le compte n’utilise pas les options [!UICONTROL EF Redirect] et [!UICONTROL Auto Upload]&quot; et que vous souhaitez insérer l’identifiant du groupe publicitaire dans les URL de destination ou les URL finales appropriées, vous devez créer le groupe publicitaire, télécharger un fichier de feuille d’envoi groupé pour le nouveau groupe publicitaire, à l’aide de l’option &quot;Générer les URL de suivi&quot;, puis publier le fichier sur le réseau publicitaire. |
| <code>{ef_keyword}</code> | Pour insérer le mot-clé. |
| <code>{ef_keywordid}</code> | Pour insérer l’ID de mot-clé. <b>Remarque :</b> L’identifiant d’un nouveau mot-clé n’est pas créé tant que le mot-clé n’a pas été publié sur le réseau publicitaire. Si le compte utilise les options &quot;[!UICONTROL EF Redirect]&quot; et [!UICONTROL Auto Upload]&quot;, Adobe Advertising insère automatiquement l’ID de mot-clé dans les URL de destination ou les URL finales appropriées le lendemain. Si le compte n’utilise pas les options &quot;[!UICONTROL EF Redirect]&quot; et [!UICONTROL Auto Upload]&quot; et que vous souhaitez insérer l’ID de mot-clé dans les URL de destination ou les URL finales appropriées, vous devez créer le mot-clé ; téléchargez un fichier de feuille d’envoi pour le nouveau mot-clé, à l’aide de l’option &quot;Générer les URL de suivi&quot;, puis publiez le fichier sur le réseau publicitaire. |
| <code>{ef_matchtype}</code> | Pour insérer le type de correspondance du mot-clé &quot;Large&quot;, &quot;Exact&quot; ou &quot;Expression&quot;. Incluse automatiquement pour [!DNL Google Ads] et [!DNL Microsoft Advertising] avec la méthode de suivi &quot;[!UICONTROL EF Redirect]&quot;. |
| <code>{ef_adid}</code> | Pour insérer l’identifiant de publicité. <b>Remarque : </b> L’identifiant d’une nouvelle publicité n’est pas créé tant que la publicité n’a pas été publiée sur le réseau publicitaire. Si le compte utilise les options &quot;[!UICONTROL EF Redirect]&quot; et [!UICONTROL Auto Upload]&quot;, Adobe Advertising insère automatiquement l’ID de publicité dans les URL de destination ou les URL finales appropriées le lendemain. Si le compte n’utilise pas les options &quot;[!UICONTROL EF Redirect]&quot; et [!UICONTROL Auto Upload]&quot; et que vous souhaitez insérer l’ID de publicité dans les URL de destination ou les URL finales appropriées, vous devez créer la publicité, télécharger un fichier de feuille d’envoi groupé pour la nouvelle publicité, à l’aide de l’option &quot;Générer les URL de suivi&quot;, puis publier le fichier sur le réseau publicitaire. |

## [!DNL Google Ads] paramètres de suivi dynamique

Voir [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft Advertising] paramètres de suivi dynamique

Voir [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo ! Paramètres de suivi dynamique des annonces japonaises

Voir [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] paramètres de suivi dynamique

Voir [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [À propos des formats d’URL de suivi des clics pour le service de suivi de conversion d’Adobe Advertising](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
