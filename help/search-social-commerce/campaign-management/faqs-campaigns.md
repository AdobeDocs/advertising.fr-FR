---
title: Questions fréquentes sur les campagnes
description: Reportez-vous aux réponses aux questions sur la gestion de campagne et les vues de données de campagne.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# Questions fréquentes sur la gestion de campagne

## Informations générales

+++Puis-je déplacer des campagnes et des composants d’un compte à un autre ?

Ne déplacez pas ou ne copiez pas un composant de campagne ou de campagne, qui possède un identifiant unique, vers un compte avec un identifiant de compte différent. Cela entraînera des erreurs de données.
+++

+++Quand les données de clic sont-elles mises à jour à partir des réseaux publicitaires ?

Le processus d’extraction des données de clics de la veille à partir des moteurs de recherche commence à 06h00 dans le fuseau horaire de l’annonceur.

En outre, [!DNL Google Ads] les mesures de performances au niveau de la campagne sur le réseau de recherche pour la journée en cours sont extraites à 8h00 et 16h00 dans le fuseau horaire de l’annonceur.
+++

+++Quelles actions entraînent la perte de leur historique pour les mots-clés et les publicités ?

>[!NOTE]
>
>(Publicitaires avec portefeuilles) Attendez-vous à ce que les performances des nouvelles combinaisons de mots-clés et de types de correspondance soient volatiles pendant que Search, Social et Commerce rassemble les données pour créer de nouveaux modèles.

**Actions dans [!UICONTROL Search] > [!UICONTROL Campaigns] vues, dans le processus de publication de la feuille d’envoi groupé et dans le propre éditeur du réseau publicitaire :**

Le mot-clé ou la publicité existante est supprimé et un autre est créé lorsque :

* ([!DNL Baidu], [!DNL Google Ads], et [!DNL Yandex]) Vous modifiez le nom d’un mot-clé.

* ([!DNL Google Ads], [!DNL Microsoft Advertising], et [!DNL Yandex]) Vous modifiez le type de correspondance d’un mot-clé.

* Vous déplacez un mot-clé entre les groupes publicitaires.

* ([!DNL Google Ads] annonces de recherche dynamique, [!DNL Microsoft Advertising] publicités textuelles étendues et tous les types d’annonces sur d’autres réseaux publicitaires pris en charge) Vous modifiez une copie de publicité (titre/titre ou description) ou une image publicitaire.

* Vous déplacez une publicité entre les groupes publicitaires.

**Événements dans le processus de publication du flux d’inventaire des produits :**

Une publicité ou un mot-clé existant est supprimé et un autre est créé lorsque :

* Un fichier de flux contient une nouvelle valeur pour une colonne utilisée dans une variation publicitaire.

* Les paramètres du modèle d’une publicité ont changé depuis la dernière propagation.

* Un nouveau fichier de flux comprend une ligne pour une publicité ou un mot-clé qui a) se trouvait dans un fichier précédent mais b) a été omis depuis et a été mis en pause ou supprimé selon les paramètres des données du flux.

Selon le [paramètres de données de flux](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings), une publicité existante ou un mot-clé peut être supprimé dans les cas suivants :

* Un nouveau fichier de flux n’inclut pas de ligne pour une publicité ou un mot-clé existant.

* La date de fin planifiée des composants d’un fichier de flux publié se produit.

* Le niveau de stock d’un élément se situe en dessous d’un minimum spécifié dans les paramètres des données de flux.
+++

+++([!DNL Google Ads] campagnes) Modifications des noms d’affichage de mes [!DNL Google]Les conversions trackées ont été annulées.

Si vous modifiez les noms d’affichage des propriétés de transaction dans Search, Social et Commerce, vos modifications sont remplacées par les noms configurés dans [!DNL Google Ads]. Apportez toute modification au nom dans [!DNL Google Ads].
+++

+++(Campagnes Google Ads) Puis-je utiliser un budget partagé pour les campagnes dans les portefeuilles ?

Pour de meilleurs résultats, n’ajoutez pas [!DNL Google Ads] campagnes vers une [!DNL Google Ads] budget partagé s’ils se trouvent dans des portfolios optimisés configurés sur &quot;[!UICONTROL Auto adjust campaign budget limits].&quot; Si vous le faites, [!DNL Google Ads] remplace les budgets de campagne optimisés Search, Social et Commerce, ce qui peut entraîner des inefficacités des offres.
+++

+++([!DNL Google Ads] campagnes) Puis-je envoyer des utilisateurs mobiles et non mobiles vers différentes landing pages ?

Vous pouvez utiliser la variable [!DNL Google Ads] [!DNL ValueTrack] parameters `{ifmobile}` et `{ifnotmobile}` pour déterminer le nom de domaine de la landing page de l’une des deux manières, selon le cas pour vos sites :

* Inclure la désignation mobile comme serveur hôte à l’aide de `{ifmobile:m}{ifnotmobile:www}`.

   Par exemple : `http://{ifmobile:m}{ifnotmobile:www}.example.com` emmène les utilisateurs mobiles à m.example.com et les utilisateurs non-mobiles à www.example.com.

* Inclure la désignation mobile comme domaine de niveau supérieur à l’aide de `{ifmobile:mobi}{ifnotmobile:com}`.

   Par exemple : `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` emmène les utilisateurs mobiles à www.example.mobi et les utilisateurs non mobiles à www.example.com.

Dans les deux cas, les URL de base avec suivi Search, Social et Commerce incluent le code non codé. `{}` balises et tous les paramètres supplémentaires ajoutés à l’URL de base.

>[!NOTE]
>
>Ne pas utiliser d’URL complète comme valeur pour les paramètres ifnotmobile et ifmobile ; utilisez uniquement la partie variable de l’URL (par exemple &quot;m&quot; contre &quot;www&quot; ou &quot;mobi&quot; contre &quot;com&quot;).

+++

+++([!DNL Google Ads] campagnes sur le réseau de recherche) Quelles données sont affichées aujourd’hui ?

[!DNL Google Ads] les mesures de performances au niveau de la campagne sur le réseau de recherche pour la journée en cours sont extraites à 8h00 et 16h00 dans le fuseau horaire de l’annonceur.

Dans le [!UICONTROL Campaigns] dans les deux [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] et le [!UICONTROL Optimization] > [!UICONTROL Portfolios] affichage, lorsque vous créez un rapport sur [!UICONTROL Today] Pour une période personnalisée qui inclut le jour en cours, les données comprennent les données les plus récemment extraites.

>[!NOTE]
>
>Les données relatives aux clics, aux impressions et aux conversions sont retardées de trois heures et ne sont pas terminées avant l’extraction de données suivante.

+++

+++([!DNL Google Ads] et [!DNL Microsoft Advertising]) Search, Social et Commerce prennent-ils en charge le suivi parallèle des publicités dans [!DNL Google Ads] ou [!DNL Microsoft Advertising]?

Le suivi parallèle envoie les clients directement de votre publicité vers l’URL finale, et l’URL de votre modèle de suivi (avec mesure des clics) est chargée en arrière-plan ; par conséquent, votre landing page est chargée plus rapidement.

Search, Social et Commerce prend en charge le suivi parallèle des campagnes de recherche et d’achat à l’aide de l’identifiant de clic du réseau publicitaire (`msclkid` pour [!DNL Microsoft Advertising]; `gclid` pour [!DNL Google Ads]). Utilisez une [au niveau du compte](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) ou [niveau de campagne](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] (appelé &quot;[!DNL final URL suffix]&quot; dans les réseaux publicitaires), qui est ajouté aux URL des pages d’entrée pour effectuer le suivi des clics sur les annonces enfants à partir des navigateurs qui prennent en charge le suivi parallèle. Voir [formats de suffixes requis pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et [formats de suffixes requis pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

Lorsqu’un utilisateur consulte votre publicité sur un navigateur qui ne prend pas en charge le suivi parallèle, le réseau publicitaire utilise le suivi séquentiel à la place : les clients sont d’abord envoyés vers l’URL de votre modèle de suivi, qui peut rediriger les clients vers les serveurs de suivi intermédiaires avant de les rediriger vers l’URL finale. Tous les modèles de suivi pour un compte de réseau publicitaire doivent inclure le même paramètre d’identifiant de clic que celui utilisé dans la variable [!UICONTROL Landing Page Suffix]. Voir [Formats de modèle de suivi pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et le [Formats de modèle de suivi pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++Pourquoi les URL de suivi de mes publicités incluent-elles &quot;`&EV_HASH={<hash>}`?&quot;

Lorsque vous chargez des publicités à l’aide d’une [flux d’inventaire des produits](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) pour un compte avec la redirection de pixel Search, Social et Commerce et avec un suivi au niveau des mots-clés et des créations, alors Search, Social et Commerce ajoute le paramètre de hachage et la valeur au modèle de suivi de l’annonce ou à l’URL de destination pour identifier qu’elle a été créée à l’aide de la fonction de flux d’inventaire.
+++

## Flux de stock

+++(Flux d’inventaire des produits) Dois-je suspendre ou supprimer les publicités obsolètes ou pour un produit dont le niveau de stock est inférieur à un minimum spécifié ?

Cela dépend des besoins commerciaux de l’annonceur.

Lorsque vous suspendez des publicités, elles sont réactivées si vous renvoyez la même publicité ou si le niveau de stock dépasse le minimum. Vous pouvez ainsi conserver l’historique de la publicité.

Lorsque vous supprimez des publicités et les soumettez à nouveau, de nouvelles publicités sont créées et des données historiques doivent être cumulées. Toutefois, si vous ne prévoyez pas de soumettre à nouveau des publicités supprimées, il n’est pas important de disposer de données historiques.
+++

+++(Flux d’inventaire des produits) Si je supprime un modèle d’annonce, puis en crée un nouveau, identique, les éléments manquants dans le fichier de flux suivant sont-ils suspendus (lorsque les paramètres du fichier de flux sont configurés pour le faire) ?

Si des éléments de ligne sont manquants dans le fichier de flux suivant et que vous n’avez pas précédemment publié ces éléments à partir du nouveau modèle via un fichier de flux précédent, les éléments de ligne manquants ne sont pas reconnus comme &quot;manquants&quot; et ils ne sont donc pas créés. Pour éviter cela, propagez le fichier de flux précédent par le biais du nouveau modèle et publiez les données avant de propager et de publier les données d’un nouveau fichier.
+++

+++(Flux d’inventaire des produits) Puis-je mettre à jour les prix de mes produits sans affecter le score de qualité d’une publicité ?

Pour [!DNL Google Ads] campagnes, oui : Le [!DNL Google Ads] `{Param 1}` et `{Param 2}` vous permettent d’insérer dynamiquement des valeurs numériques dans une variation publicitaire sans supprimer ni recréer la publicité, et donc sans affecter le score de qualité.

Pour utiliser une `{Param 1}` ou `{Param 2}` pour les données de prix, mappez la colonne de prix de votre fichier de données avec cette variable dans les modèles de flux appropriés, puis incluez la variable dans vos modèles de variation publicitaire.

Par exemple, si la colonne est appelée &quot;Prix&quot;, ouvrez le modèle de flux qui crée les publicités, cliquez dans le champ de saisie en regard de **[!UICONTROL Param 1]**, puis cliquez sur le bouton **[!UICONTROL Price]** dans la colonne [!UICONTROL Feeds/Available Columns] list, qui insère `[Price]` comme valeur de [!UICONTROL Param 1]. Ensuite, dans le modèle de variation publicitaire au bas du modèle de flux, insérez `{param1:default text}`, où &quot;texte par défaut&quot; est du texte à utiliser si la colonne de paramètre du fichier de flux est vide pour une ligne de publicité.

Lorsque vous envoyez des données, les champs de données de la variable [!UICONTROL Param1] et [!UICONTROL Param2] Les colonnes peuvent contenir jusqu’à 25 caractères, dont des données numériques, des symboles de devise et des codes de devise, ainsi que les caractères non numériques suivants : `, . % + - /`
+++

+++Mes campagnes générées à partir de flux de stock comportent de nombreuses transactions orphelines.

Si la variable [paramètres de données de flux](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) sont configurés pour supprimer des publicités dans diverses situations, puis toute conversion différée qui se produit après des clics sur la publicité peut entraîner [transactions orphelines](/help/search-social-commerce/glossary.md#o-p). La bonne pratique consiste à suspendre les publicités au lieu de les supprimer. Si une publicité n’a toujours pas reçu de recettes après une longue période, vous pouvez la supprimer par le biais d’une feuille d’envoi groupée ou de la vue de gestion des publicités.
+++

## Problèmes de performances liés aux comptes et aux campagnes

+++Certaines de mes campagnes dépensent plus ou moins que les budgets de campagne.

* Cela est normal dans un portfolio optimisé configuré avec le[!UICONTROL Auto-adjust campaign budget limits]&quot;. Lorsque cette option est activée, vous pouvez dépenser jusqu’à *N* représente le budget de chaque campagne, où *N* est la valeur de la variable[!UICONTROL Multiple]&quot;. Cette option permet à la fonctionnalité d’optimisation d’ajuster les dépenses pour les campagnes individuelles si nécessaire, tout en guidant l’ensemble du portefeuille pour atteindre ses objectifs.
* If [!DNL Google Ads] les campagnes utilisent un budget partagé, puis [!DNL Google Ads] ajuste les dépenses pour les campagnes individuelles si nécessaire afin de dépenser l’intégralité du budget partagé.
+++
