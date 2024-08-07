---
title: Questions fréquentes sur les campagnes
description: Reportez-vous aux réponses aux questions concernant la gestion de campagne et les vues de données de campagne.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Questions fréquentes sur la gestion de campagne

## Informations générales

+++Puis-je déplacer des campagnes et des composants d’un compte à un autre ?

Ne déplacez pas ou ne copiez pas un composant de campagne ou de campagne, qui possède un identifiant unique, vers un compte avec un identifiant de compte différent. Cela entraîne des erreurs de données.
+++

+++Quand les données de clic sont-elles mises à jour à partir des réseaux publicitaires ?

Le processus d’extraction des données de clics de la veille à partir des moteurs de recherche commence à 06h00 dans le fuseau horaire de l’annonceur.

En outre, les mesures de performances au niveau de la campagne [!DNL Google Ads] sur le réseau de recherche pour la journée en cours sont extraites à 8 h et 16 h dans le fuseau horaire de l’annonceur.
+++

+++Quelles actions entraînent la perte d’historique des mots-clés et des publicités ?

>[!NOTE]
>
>(Publicitaires avec portefeuilles) Attendez-vous à ce que les performances des nouvelles combinaisons de mots-clés et de types de correspondance soient volatiles pendant que Search, Social et Commerce rassemble les données pour créer des modèles à leur place.

**Actions dans les vues [!UICONTROL Search] > [!UICONTROL Campaigns], dans le processus de publication de la feuille d’envoi groupé et dans l’éditeur du réseau publicitaire :**

Le mot-clé ou la publicité existante est supprimé et un autre est créé lorsque :

* ([!DNL Baidu], [!DNL Google Ads] et [!DNL Yandex]) Vous modifiez un nom de mot-clé.

* ([!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Yandex]) Vous modifiez le type de correspondance d’un mot-clé.

* Vous déplacez un mot-clé entre les groupes publicitaires.

* ([!DNL Google Ads] annonces de recherche dynamique, [!DNL Microsoft Advertising] annonces textuelles étendues et tous les types d’annonces sur d’autres réseaux publicitaires pris en charge) Vous modifiez la copie de la publicité (titre/titre ou description) ou une image publicitaire.

* Vous déplacez une publicité entre les groupes publicitaires.

**Événements dans le processus de publication du flux d’inventaire des produits :**

Une publicité ou un mot-clé existant est supprimé et un autre est créé lorsque :

* Un fichier de flux contient une nouvelle valeur pour une colonne utilisée dans une variation publicitaire.

* Les paramètres du modèle d’une publicité ont changé depuis la dernière propagation.

* Un nouveau fichier de flux comprend une ligne pour une publicité ou un mot-clé qui a) se trouvait dans un fichier précédent mais b) a été omis depuis et a été mis en pause ou supprimé selon les paramètres des données du flux.

Selon les [ paramètres de données de flux ](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), une publicité existante ou un mot-clé peut être supprimé lorsque :

* Un nouveau fichier de flux n’inclut pas de ligne pour une publicité ou un mot-clé existant.

* La date de fin planifiée des composants d’un fichier de flux publié se produit.

* Le niveau de stock d’un élément se situe en dessous d’un minimum spécifié dans les paramètres des données de flux.
+++

+++([!DNL Google Ads] campagnes) Les modifications apportées aux noms d’affichage pour mes conversions trackées [!DNL Google] ont été annulées.

Si vous modifiez les noms d’affichage des mesures de conversion dans Search, Social et Commerce, vos modifications sont remplacées par les noms configurés dans [!DNL Google Ads]. Apportez tous les changements de nom dans [!DNL Google Ads].
+++

+++(Campagnes Google Ads) Puis-je utiliser un budget partagé pour les campagnes dans les portefeuilles ?

Pour de meilleurs résultats, n’ajoutez pas de campagnes [!DNL Google Ads] à un budget partagé [!DNL Google Ads] s’ils se trouvent dans des portefeuilles optimisés configurés sur &quot;[!UICONTROL Auto adjust campaign budget limits]&quot;. Dans ce cas, [!DNL Google Ads] remplace les budgets de campagne optimisés Search, Social et Commerce, ce qui peut entraîner des inefficacités des offres.
+++

+++([!DNL Google Ads] campagnes) Puis-je envoyer des utilisateurs mobiles et non mobiles vers différentes pages d’entrée ?

Vous pouvez utiliser les [!DNL Google Ads] [!DNL ValueTrack] paramètres `{ifmobile}` et `{ifnotmobile}` pour déterminer le nom de domaine de la page d’entrée de l’une des deux façons, selon le cas pour vos sites :

* Incluez la désignation mobile comme serveur hôte utilisant `{ifmobile:m}{ifnotmobile:www}`.

  Par exemple, `http://{ifmobile:m}{ifnotmobile:www}.example.com` amène les utilisateurs mobiles à m.example.com et les utilisateurs non mobiles à www.example.com.

* Incluez la désignation mobile comme domaine de niveau supérieur à l’aide de `{ifmobile:mobi}{ifnotmobile:com}`.

  Par exemple, `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` amène les utilisateurs mobiles à www.example.mobi et les utilisateurs non mobiles à www.example.com.

Dans les deux cas, les URL de base avec suivi Search, Social et Commerce incluent les balises `{}` non codées et tous les paramètres supplémentaires ajoutés à l’URL de base.

>[!NOTE]
>
>N’utilisez pas d’URL complète comme valeur pour les paramètres ifnotmobile et ifmobile ; utilisez uniquement la partie variable de l’URL (par exemple &quot;m&quot; contre &quot;www&quot; ou &quot;mobi&quot; contre &quot;com&quot;).

+++

+++([!DNL Google Ads] campagnes sur le réseau de recherche) Quelles données s’affichent pour aujourd’hui ?

[!DNL Google Ads] les mesures de performances au niveau de la campagne sur le réseau de recherche pour la journée en cours sont extraites à 8 h et 16 h dans le fuseau horaire de l’annonceur.

Dans l’onglet [!UICONTROL Campaigns] de la vue [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] et de la vue [!UICONTROL Optimization] > [!UICONTROL Portfolios], lorsque vous créez un rapport sur [!UICONTROL Today] ou une plage de dates personnalisée qui inclut le jour en cours, les données incluent les données synchronisées le plus récemment.

>[!NOTE]
>
>Les données relatives aux clics, aux impressions et aux conversions sont retardées de trois heures et ne sont pas terminées avant l’extraction de données suivante.

+++

+++Quelle est la différence entre un modèle de suivi et un suffixe de landing page ?

Utilisez un suffixe de page d’entrée uniquement pour les réseaux publicitaires qui prennent en charge le suivi parallèle. Dans Search, Social et Commerce, les modèles de suivi et les suffixes de page d’entrée doivent inclure un identifiant de clic provenant du réseau publicitaire, mais les modèles de suivi incluent des paramètres de suivi supplémentaires.

Pour plus d’informations sur le chargement de modèles de suivi et de suffixes de page d’entrée lorsqu’un utilisateur clique sur une publicité, reportez-vous aux questions fréquentes suivantes sur la [prise en charge du suivi parallèle](#parallel-tracking) .

+++

+++([!DNL Google Ads] et [!DNL Microsoft Advertising]) Search, Social et Commerce prennent-ils en charge le suivi parallèle des publicités dans [!DNL Google Ads] ou [!DNL Microsoft Advertising] ? {#parallel-tracking}

Le suivi parallèle envoie directement les clients de votre publicité à votre URL finale, qui peut inclure des paramètres ajoutés à un suffixe d’URL final ou &quot;suffixe de page d’entrée&quot;. L’URL de votre modèle de suivi (avec des paramètres supplémentaires pour la mesure des clics) est chargée séparément en arrière-plan. Par conséquent, votre landing page est chargée plus rapidement.

Search, Social et Commerce prend en charge le suivi parallèle des campagnes de recherche et d’achat à l’aide de l’identifiant de clic du réseau publicitaire (`msclkid` pour [!DNL Microsoft Advertising] ; `gclid` pour [!DNL Google Ads]). Utilisez un [niveau-compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) ou [niveau-campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (appelé &quot;[!DNL final URL suffix]&quot; dans les réseaux publicitaires), qui est ajouté aux URL de page d’entrée pour effectuer le suivi des clics sur les publicités enfants à partir de navigateurs qui prennent en charge le suivi parallèle. Voir les [ formats de suffixes requis pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et les [ formats de suffixes requis pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Lorsqu&#39;un utilisateur consulte votre publicité sur un navigateur qui ne prend pas en charge le suivi parallèle, le réseau publicitaire utilise à la place le suivi séquentiel : les clients sont d&#39;abord envoyés à l&#39;URL de votre modèle de suivi, ce qui peut rediriger les clients vers les serveurs de suivi intermédiaires avant de les rediriger vers l&#39;URL finale (qui peut inclure des paramètres supplémentaires dans un suffixe de page d&#39;entrée). Tous les modèles de suivi pour un compte de réseau publicitaire doivent inclure le même paramètre d’identifiant de clic que celui utilisé dans [!UICONTROL Landing Page Suffix]. Voir les [ formats de modèle de suivi pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et les [ formats de modèle de suivi pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Pourquoi les URL de suivi de mes publicités incluent &quot;`&EV_HASH={<hash>}`&quot; ?

Lorsque vous chargez des publicités à l’aide d’un [flux d’inventaire de produits](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) pour un compte avec la redirection de pixel Search, Social et Commerce et avec un suivi de niveau mots-clés et créatif, Search, Social et Commerce ajoute le paramètre de hachage et la valeur au modèle de suivi ou à l’URL de destination de l’annonce pour identifier qu’elle a été créée à l’aide de la fonction de flux d’inventaire.
+++

## Flux de stock

+++(Flux d’inventaire des produits) Dois-je suspendre ou supprimer les publicités obsolètes ou pour un produit dont le niveau de stock est inférieur à un minimum spécifié ?

Cela dépend des besoins commerciaux de l’annonceur.

Lorsque vous suspendez des publicités, elles sont réactivées si vous renvoyez la même publicité ou si le niveau de stock dépasse le minimum. Vous pouvez ainsi conserver l’historique de la publicité.

Lorsque vous supprimez des publicités et les soumettez à nouveau, de nouvelles publicités sont créées et des données historiques doivent être cumulées pour les nouvelles publicités. Toutefois, si vous ne prévoyez pas de soumettre à nouveau des publicités supprimées, il n’est pas important de disposer de données historiques.
+++

+++(Flux d’inventaire des produits) Si je supprime un modèle d’annonce, puis en crée un nouveau, identique, les éléments manquants dans le fichier de flux suivant sont-ils suspendus (lorsque les paramètres du fichier de flux sont configurés pour le faire) ?

Si des éléments de ligne sont manquants dans le fichier de flux suivant et que vous n’avez pas précédemment publié ces éléments à partir du nouveau modèle via un fichier de flux précédent, les éléments de ligne manquants ne sont pas reconnus comme &quot;manquants&quot; et ils ne sont donc pas créés. Pour éviter cela, propagez le fichier de flux précédent par le biais du nouveau modèle et publiez les données avant de propager et de publier les données d’un nouveau fichier.
+++

+++(Flux d’inventaire des produits) Puis-je mettre à jour les prix de mes produits sans affecter le score de qualité d’une publicité ?

Pour les campagnes [!DNL Google Ads], oui : les variables [!DNL Google Ads] `{Param 1}` et `{Param 2}` vous permettent d’insérer dynamiquement des valeurs numériques dans une variation publicitaire sans supprimer ni recréer la publicité, et donc sans affecter le score de qualité.

Pour utiliser une variable `{Param 1}` ou `{Param 2}` pour vos données de prix, mappez la colonne de prix de votre fichier de données avec cette variable dans les modèles de flux appropriés, puis incluez la variable dans vos modèles de variation publicitaire.

Par exemple, si la colonne est appelée &quot;Prix&quot;, ouvrez le modèle de flux qui crée les publicités, cliquez dans le champ de saisie en regard de **[!UICONTROL Param 1]**, puis cliquez sur la colonne **[!UICONTROL Price]** de la liste [!UICONTROL Feeds/Available Columns], qui insère `[Price]` comme valeur pour [!UICONTROL Param 1]. Ensuite, dans le modèle de variation publicitaire au bas du modèle de flux, insérez `{param1:default text}`, où &quot;texte par défaut&quot; est du texte à utiliser si la colonne de paramètre du fichier de flux est vide pour une ligne de publicité.

Lorsque vous envoyez des données, les champs de données des colonnes [!UICONTROL Param1] et [!UICONTROL Param2] peuvent contenir jusqu’à 25 caractères, y compris des données numériques, des symboles de devise et des codes de devise, ainsi que les caractères non numériques suivants : `, . % + - /`
+++

+++Mes campagnes générées à partir de flux de stock comportent de nombreuses transactions orphelines.

Si les [ paramètres de données de flux ](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) sont configurés pour supprimer des publicités dans diverses situations, toutes les conversions différées qui surviennent après des clics sur la publicité peuvent entraîner des [transactions orphelines](/help/search-social-commerce/glossary.md#o-p). La bonne pratique consiste à suspendre les publicités au lieu de les supprimer. Si une publicité n’a encore reçu aucune recette au bout d’un certain temps, vous pouvez la supprimer par le biais d’une feuille d’envoi groupé ou de la vue de gestion des publicités.
+++

## Problèmes de performances liés aux comptes et aux campagnes

+++Certaines de mes campagnes dépensent plus ou moins que les budgets de campagne.

* Cela est normal dans un portfolio optimisé configuré avec l’option &quot;[!UICONTROL Auto-adjust campaign budget limits]&quot;. Lorsque cette option est activée, vous pouvez dépenser jusqu’à *N* fois le budget de chaque campagne, où *N* est la valeur du paramètre &quot;[!UICONTROL Multiple]&quot;. Cette option permet à la fonctionnalité d’optimisation d’ajuster les dépenses pour les campagnes individuelles si nécessaire, tout en guidant l’ensemble du portefeuille pour atteindre ses objectifs.
* Si [!DNL Google Ads] campagnes utilisent un budget partagé, [!DNL Google Ads] adapte les dépenses pour les campagnes individuelles si nécessaire pour dépenser l&#39;intégralité du budget partagé.
+++
