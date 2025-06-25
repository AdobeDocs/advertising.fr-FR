---
title: Questions fréquentes sur les campagnes
description: Voir les réponses aux questions sur la gestion des campagnes et les vues de données des campagnes.
exl-id: 999e5aba-f556-4b34-bb92-5931d5e0dd72
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1585'
ht-degree: 0%

---

# Questions fréquentes sur la gestion de campagnes

## Informations générales

+++Puis-je déplacer des campagnes et des composants d’un compte à un autre ?

Ne déplacez pas et ne copiez pas une campagne ou un composant de campagne doté d’un identifiant unique vers un compte doté d’un identifiant différent. Cela entraîne des erreurs de données.
+++

+++Quand les données de clics sont-elles mises à jour à partir des réseaux publicitaires ?

Le processus d&#39;extraction des données de clics de la veille des moteurs de recherche commence à 06:00 dans le fuseau horaire de l&#39;annonceur.

En outre, [!DNL Google Ads] mesures de performances au niveau de la campagne sur le réseau de recherche pour la journée en cours sont extraites à 8 h et à 16 h dans le fuseau horaire de l’annonceur.
+++

+++Quelles actions entraînent la perte de l’historique des mots-clés et des publicités ?

>[!NOTE]
>
>(Annonceurs disposant de portefeuilles) Attendez-vous à ce que les performances des nouvelles combinaisons de mots-clés et de types de correspondance soient variables, tandis que Search, Social et Commerce collecte des données pour créer des modèles à leur intention.

**Actions dans les vues [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns], dans le processus de publication de feuilles d’envoi groupé et dans le propre éditeur du réseau publicitaire :**

Le mot-clé ou l’annonce publicitaire existant est supprimé et un autre est créé lorsque :

* ([!DNL Baidu], [!DNL Google Ads] et [!DNL Yandex]) Vous modifiez un nom de mot-clé.

* ([!DNL Google Ads], [!DNL Microsoft Advertising] et [!DNL Yandex]) Vous pouvez modifier le type de correspondance d’un mot-clé.

* Vous déplacez un mot-clé entre les groupes publicitaires.

* ([!DNL Google Ads] les annonces de recherche dynamique, [!DNL Microsoft Advertising] les annonces textuelles développées et tous les types d’annonces sur d’autres réseaux publicitaires pris en charge) Vous modifiez la copie de l’annonce (titre/description) ou une image publicitaire.

* Vous déplacez une annonce publicitaire entre des groupes publicitaires.

**Événements dans le processus de validation du flux de stock de produits :**

Une annonce ou un mot-clé existant est supprimé et un autre est créé lorsque :

* Un fichier de flux contient une nouvelle valeur pour une colonne utilisée dans une variation publicitaire.

* Les paramètres de modèle d’une annonce publicitaire ont été modifiés depuis la dernière propagation.

* Un nouveau fichier de flux comprend une ligne pour une publicité ou un mot-clé qui a) se trouvait dans un fichier précédent, mais qui b) a été omis depuis et a été suspendu ou supprimé en fonction des paramètres de données de flux.

Selon les [paramètres des données de flux](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), une annonce publicitaire ou un mot-clé existant peut être supprimé lorsque :

* Un nouveau fichier de flux n’inclut pas de ligne pour une annonce publicitaire ou un mot-clé existant.

* La date de fin planifiée pour les composants d’un fichier de flux publié se produit.

* Le niveau de stock d’un article tombe en dessous d’un minimum spécifié dans les paramètres des données de flux.
+++

+++(campagnes [!DNL Google Ads]) Les modifications apportées aux noms d’affichage de mes conversions suivies par [!DNL Google] ont été annulées.

Si vous modifiez les noms d’affichage des mesures de conversion dans Search, Social et Commerce, vos modifications sont remplacées par les noms configurés dans [!DNL Google Ads]. Apportez les modifications de nom désirées dans [!DNL Google Ads].
+++

+++(Campagnes Google Ads) Puis-je utiliser un budget partagé pour les campagnes des portfolios ?

Pour obtenir de meilleurs résultats, n’ajoutez pas de campagnes [!DNL Google Ads] à un budget partagé [!DNL Google Ads] si elles se trouvent dans des portfolios optimisés configurés sur « [!UICONTROL Auto adjust campaign budget limits] ». Si vous le faites, [!DNL Google Ads] remplace les budgets de campagne optimisés pour Search, Social et Commerce, ce qui peut entraîner des inefficacités d’offres.
+++

+++(campagnes [!DNL Google Ads]) Puis-je envoyer des utilisateurs mobiles et non mobiles vers différentes pages de destination ?

Vous pouvez utiliser les paramètres de [!DNL ValueTrack] [!DNL Google Ads] `{ifmobile}` et `{ifnotmobile}` pour déterminer le nom de domaine de la page de destination de l’une des deux façons suivantes, en fonction de vos sites :

* Incluez la désignation de mobile comme serveur hôte à l’aide de `{ifmobile:m}{ifnotmobile:www}`.

  Par exemple, `http://{ifmobile:m}{ifnotmobile:www}.example.com` redirige les utilisateurs mobiles vers m.example.com et les utilisateurs non mobiles vers www.example.com.

* Incluez la désignation mobile comme domaine de niveau supérieur à l’aide de `{ifmobile:mobi}{ifnotmobile:com}`.

  Par exemple, `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` redirige les utilisateurs mobiles vers www.example.mobi et les autres vers www.example.com.

Dans les deux cas, les URL de base avec suivi Search, Social et Commerce incluent les balises `{}` non codées et tous les paramètres supplémentaires ajoutés à l’URL de base.

>[!NOTE]
>
>N’utilisez pas d’URL complète comme valeur pour les paramètres ifnotmobile et ifmobile. Utilisez uniquement la partie variable de l’URL (par exemple, « m » contre « www » ou « mobi » contre « com »).

+++

+++([!DNL Google Ads] des campagnes sur le réseau de recherche) Pour quelles données s’affiche-t-on aujourd’hui ?

[!DNL Google Ads] mesures de performances au niveau de la campagne sur le réseau de recherche pour la journée en cours sont extraites à 8 h et à 16 h dans le fuseau horaire de l’annonceur.

Dans l’onglet [!UICONTROL Campaigns] de la vue [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] et de la vue [!UICONTROL Optimization] > [!UICONTROL Portfolios], lorsque vous créez un rapport sur [!UICONTROL Today] ou une période personnalisée qui inclut le jour en cours, les données incluent les données synchronisées les plus récemment.

>[!NOTE]
>
>Les données relatives aux clics, impressions et conversions sont retardées de trois heures et ne sont pas terminées tant que les données ne sont pas extraites.

+++

+++Quelle est la différence entre un modèle de tracking et un suffixe de page de destination ?

Utilisez un suffixe de page de destination uniquement pour les réseaux publicitaires qui prennent en charge le suivi parallèle. Dans Search, Social et Commerce, les modèles de suivi et les suffixes de page de destination doivent inclure un identifiant de clic provenant du réseau publicitaire, mais les modèles de suivi incluent des paramètres de suivi supplémentaires.

Pour plus d’informations sur le chargement des modèles de suivi et des suffixes de page de destination lorsqu’un utilisateur clique sur une annonce, consultez la FAQ suivante sur la [prise en charge du suivi parallèle](#parallel-tracking).

+++

+++([!DNL Google Ads] et [!DNL Microsoft Advertising]) Search, Social et Commerce prennent-ils en charge le suivi parallèle des publicités dans [!DNL Google Ads] ou [!DNL Microsoft Advertising] ? {#parallel-tracking}

Le suivi parallèle envoie directement les clients de votre publicité à votre URL finale, qui peut inclure des paramètres ajoutés à partir d’un suffixe d’URL final, ou « suffixe de page de destination ». L’URL de votre modèle de suivi (avec des paramètres supplémentaires pour la mesure des clics) est chargée séparément en arrière-plan. Votre page de destination est donc chargée plus rapidement.

Search, Social et Commerce prennent en charge le suivi parallèle des campagnes de recherche et d’achat à l’aide de l’identifiant de clic du réseau publicitaire (`msclkid` par [!DNL Microsoft Advertising] ; `gclid` par [!DNL Google Ads]). Utilisez un [!UICONTROL Landing Page Suffix] [au niveau du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) ou [au niveau de la campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) (appelé « [!DNL final URL suffix] » dans les réseaux publicitaires), qui est ajouté aux URL des pages de destination pour effectuer le suivi des clics sur les annonces enfants des navigateurs qui prennent en charge le suivi parallèle. Consultez les sections [Formats de suffixes requis pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et [Formats de suffixes requis pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Lorsque l’utilisateur consulte votre publicité sur un navigateur qui ne prend pas en charge le suivi parallèle, le réseau publicitaire utilise le suivi séquentiel. Les clients sont d’abord envoyés à l’URL de votre modèle de suivi, qui peut les rediriger vers des serveurs de suivi intermédiaires avant de les rediriger vers l’URL finale (qui peut inclure des paramètres supplémentaires dans un suffixe de page de destination). Tous les modèles de suivi d’un compte de réseau publicitaire doivent inclure le même paramètre d’identifiant de clic que celui utilisé dans le [!UICONTROL Landing Page Suffix]. Voir les [formats des modèles de suivi pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et les [formats des modèles de suivi pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Pourquoi les URL de tracking de mes publicités incluent-elles « `&EV_HASH={<hash>}` » ?

Lorsque vous téléchargez des publicités à l’aide d’un [flux d’inventaire de produits](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) pour un compte avec la redirection de pixels Search, Social et Commerce et avec un suivi au niveau des mots-clés et de la création, Search, Social et Commerce ajoute le paramètre de hachage et la valeur au modèle de suivi ou à l’URL de destination de la publicité afin d’identifier qu’elle a été créée à l’aide de la fonction de flux d’inventaire.
+++

## Flux d’inventaire

+++(Flux d’inventaire des produits) Dois-je suspendre ou supprimer les publicités obsolètes ou concernant un produit dont le niveau de stock est inférieur à un minimum spécifié ?

Cela dépend des exigences commerciales de l&#39;annonceur.

Lorsque vous mettez des annonces en pause, elles sont réactivées si vous soumettez à nouveau la même annonce ou si le niveau de stock dépasse le minimum. Vous pouvez ainsi conserver l’historique de l’annonce publicitaire.

Lorsque vous supprimez et soumettez à nouveau des annonces, de nouvelles annonces sont créées et des données historiques doivent être accumulées pour les nouvelles annonces. Toutefois, si vous ne prévoyez pas de soumettre à nouveau des publicités supprimées, il n’est pas important de disposer de données historiques.
+++

+++(Flux d’inventaire de produits) Si je supprime un modèle d’annonce publicitaire, puis en crée un nouveau identique, les éléments manquants du fichier de flux suivant sont-ils en pause (lorsque les paramètres du fichier de flux sont configurés pour cela) ?

Si le fichier de flux suivant contient des éléments de ligne manquants et que vous n’avez pas validé ces éléments de ligne à partir du nouveau modèle via un fichier de flux précédent, les éléments de ligne manquants ne sont pas reconnus comme « manquants ». Ils ne sont donc pas créés. Pour éviter cela, propagez le fichier de flux précédent à travers le nouveau modèle et publiez les données avant de propager et de publier les données d’un nouveau fichier.
+++

+++(flux d’inventaire des produits) Puis-je mettre à jour les prix de mes produits sans affecter le score de qualité d’une annonce publicitaire ?

Pour les campagnes [!DNL Google Ads], oui : les variables [!DNL Google Ads] `{Param 1}` et `{Param 2}` vous permettent d’insérer dynamiquement des valeurs numériques dans une variation publicitaire sans supprimer ni recréer la publicité, et donc sans affecter le score de qualité.

Pour utiliser une variable de `{Param 1}` ou de `{Param 2}` pour vos données de prix, mappez la colonne de prix de votre fichier de données à cette variable dans les modèles de flux appropriés, puis incluez la variable dans vos modèles de variation d’annonce.

Par exemple, si la colonne est appelée « Prix », ouvrez le modèle de flux qui crée les annonces, cliquez dans le champ de saisie à côté de **[!UICONTROL Param 1]**, puis cliquez sur la colonne **[!UICONTROL Price]** dans la liste [!UICONTROL Feeds/Available Columns], qui insère `[Price]` comme valeur de [!UICONTROL Param 1]. Ensuite, dans le modèle de variation publicitaire au bas du modèle de flux, insérez `{param1:default text}`, où « texte par défaut » correspond au texte à utiliser si la colonne de paramètres du fichier de flux est vide pour une ligne de publicité.

Lorsque vous envoyez des données, les champs de données des colonnes [!UICONTROL Param1] et [!UICONTROL Param2] peuvent contenir jusqu’à 25 caractères, y compris des données numériques, des symboles et des codes de devise, ainsi que les caractères non numériques suivants : `, . % + - /`
+++

+++Mes campagnes générées à partir de flux d’inventaire comportent de nombreuses transactions orphelines.

Si les [ paramètres des données de flux ](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) sont configurés pour supprimer des publicités dans diverses situations, les conversions différées qui se produisent après des clics sur la publicité peuvent entraîner des [ transactions orphelines ](/help/search-social-commerce/glossary.md#o-p). La bonne pratique consiste à suspendre les publicités au lieu de les supprimer. Si une publicité n’a toujours pas reçu de chiffre d’affaires après un long moment, vous pouvez la supprimer via une feuille d’envoi groupé ou la vue de gestion des publicités.
+++

## Problèmes de performances liés au compte et à la campagne

+++Certaines de mes campagnes dépensent plus ou moins que les budgets de la campagne.

* Cela est normal dans un portfolio optimisé configuré avec l’option « [!UICONTROL Auto-adjust campaign budget limits] ». Lorsque cette option est activée, vous pouvez dépenser jusqu’à *N* fois le budget de chaque campagne, où *N* est la valeur du paramètre « [!UICONTROL Multiple] ». Cette option permet à la fonctionnalité d’optimisation d’ajuster les dépenses des campagnes individuelles selon les besoins, tout en dirigeant l’ensemble du portefeuille pour atteindre sa cible.
* Si [!DNL Google Ads] campagnes utilisent un budget partagé, [!DNL Google Ads] ajuste les dépenses de chaque campagne selon les besoins afin de dépenser l’intégralité du budget partagé.
+++
