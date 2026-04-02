---
title: '[!DNL Google Analytics] des paramètres des sources de données'
description: Référencez les paramètres requis pour les sources  [!DNL Google Analytics]  données.
role: User, Admin
exl-id: 78422c2c-ed58-410e-8996-882759ed5556
feature: Search Data Sources
TQID: https://experienceleague.adobe.com/EvCJTrEFxRU87kUlKCZ-rN3jtNVjSkVGmrHCNsPMElw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 799
ht-degree: 0%

---

# [!DNL Google Analytics] des paramètres des sources de données

| Section | Paramètre | Description |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | Identifiant du compte [!DNL Google Analytics] à partir duquel les données sont extraites. Toutes les utilisations de l’API pour extraire des données sont facturées au compte spécifié. Le compte doit accorder des autorisations de type « Lecture et analyse » à l’adresse e-mail spécifiée.<br><br>Pour trouver votre identifiant, connectez-vous à [!DNL Google Analytics]. Dans le coin supérieur gauche, cliquez sur **[!DNL All accounts]** pour ouvrir une liste de vos comptes. L’identifiant de chaque compte se trouve sous le nom du compte. |
| | [!UICONTROL Google Analytics Login] | Indiquez l’adresse de connexion/e-mail à utiliser pour accéder aux données de cette source de données. Le nom d’utilisateur doit être enregistré sur un compte [!DNL Google] et disposer des autorisations « Lecture et analyse » pour le compte [!DNL Google Analytics]. Reportez-vous aux [instructions pour l’attribution des autorisations utilisateur dans [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).<br><br><b>Remarque :</b> si vous modifiez le mot de passe de ce compte de connexion, toutes les connexions ouvertes au compte seront fermées. Pour reprendre la synchronisation des données, revenez à cette page et [réauthentifiez](data-source-reauthenticate.md). |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | (Lecture seule ; comptes connectés uniquement) Nom du compte. |
| | [!UICONTROL Google Analytics Property] | Propriété (site web, application mobile ou appareil) à partir de laquelle collecter les données pour le compte [!DNL Google Analytics].<br><br> Pour intégrer des mesures pour plusieurs propriétés, configurez une source de données distincte pour chaque propriété. |
| | [!UICONTROL Google Analytics View] | Vue contenant le jeu de données auquel vous souhaitez accéder. Si la propriété comporte plusieurs vues, envisagez d’extraire la vue non filtrée au niveau le plus élevé, qui contient toutes les données.<br><br>Pour intégrer des mesures pour plusieurs vues pour la même propriété, configurez une source de données distincte pour chaque vue. Assurez-vous que les vues n’incluent pas de données qui se chevauchent. |
| | [!UICONTROL Google Analytics Dimension] | La dimension personnalisée [!DNL Google Analytics] qui est renseignée avec la valeur du paramètre de chaîne de requête « ef_id » d’Adobe Advertising. Si la dimension appropriée n’apparaît pas dans la liste, contactez votre équipe d’implémentation [!DNL Google Analytics].<br><br>ef_id est utilisé comme clé primaire pour transmettre des données de [!DNL Google Analytics] à Adobe Advertising. |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | Toutes les mesures disponibles pour la propriété et la vue [!DNL Google Analytics] spécifiées qui ne sont pas importées pour la source de données, organisées par catégorie. La liste comprend le nom convivial importé et le nom du serveur principal (en commençant par « ga »). pour chaque mesure. Le bouton [!UICONTROL Refresh] actualise la liste avec toutes les nouvelles mesures dans [!DNL Google Analytics].<br><br>Pour importer une mesure disponible, faites-la glisser dans la section [!UICONTROL Selected Metrics].<br><br>Voir « [Mesures disponibles [!DNL Google Analytics] dans Advertising Cloud](data-source-ga-metrics.md) ». |
| | Mesures sélectionnées | Toutes les mesures pour la propriété et la vue [!DNL Google Analytics] spécifiées qui sont importées pour la source de données, ainsi que le statut de validation de chaque mesure. La liste comprend le nom convivial importé et le nom du serveur principal (commençant par « `ga.` ») pour chaque mesure. Chaque source de données peut inclure quatre mesures de trafic par défaut que vous ne pouvez pas supprimer ([!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] et [!UICONTROL Session Duration]) et jusqu’à 16 mesures valides supplémentaires ou sans données. Vous pouvez modifier la liste des mesures à tout moment.<br><br>Pour importer une mesure, sélectionnez-la dans le volet [!UICONTROL Available Metrics] et faites-la glisser ici.<br><br><b>Attention:</b> [!DNL Google Analytics] permet jusqu’à 10 mesures dans un seul flux de données. Chacune de vos sources de données dans Search, Social et Commerce peut inclure jusqu’à deux flux avec un total de 20 mesures, mais l’utilisation d’un second flux double vos appels API à [!DNL Google Analytics]. Si vous disposez de nombreuses mesures, sélectionnez uniquement celles que vous souhaitez utiliser dans les objectifs pour l’optimisation. Vous pouvez consulter vos quotas pour ce projet dans [le [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). En savoir plus sur les [quotas et limites d’appel pour les requêtes API vers [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).<br><br><b>Remarques :</b><br><ul><li>Le nom convivial est importé en tant que nom d’affichage d’une mesure dans la vue [!UICONTROL Admin] > [!UICONTROL Transactions Properties] et est ajouté avec « <code>_ga:&lt;metric_tag configuré dans le champ Balise de mesure></code>» (par exemple, « Pageviews_ga:UK »). Vous pouvez éventuellement modifier le nom d’affichage de vos objectifs et mesures personnalisés, mais les noms d’affichage de toutes les mesures courantes sont remplacés chaque jour par les noms conviviaux dans [!DNL Google Analytics], ajoutés avec les balises spécifiées.</li><li>Les pages vues, les sessions, le taux de rebond (calculé sous la forme de rebonds/sessions) et la durée de session sont automatiquement pris en compte dans les algorithmes d’offres du portefeuille. Vous pouvez ajouter manuellement n’importe quelle autre mesure à un objectif de portefeuille.</li><li>Lorsque vous supprimez une mesure de la source de données, Adobe Advertising conserve les données historiques conformément à la [politique de conservation des données](/help/search-social-commerce/reports/data-used-for-reports.md) habituelle.</li></ul> |
| Balise de mesure | Balise de mesure | Balise à ajouter à chaque mesure de [!DNL Google Analytics] sélectionnée dans Adobe Advertising, précédée de « <code>_ga :</code>» (par exemple, « Pageviews_tag:&lt;metric_tag> »). La balise peut contenir entre 2 et 5 caractères alphanumériques et doit être unique pour l’annonceur.<br><br>Cette balise vous permet d’identifier la source de données pour chaque mesure. Cette balise est particulièrement importante lorsque vous configurez plusieurs sources de données, car chaque source de données inclut certains noms de mesures identiques (notamment [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces] et [!UICONTROL Session Duration], ainsi que d’autres mesures potentielles). L’ajout de balises de mesure différentes empêche les noms de mesure en double.<br><br>Par exemple, si vous configurez des intégrations distinctes pour la propriété UK et la propriété JP, vous pouvez utiliser « UK » et « JP » comme balises de mesure. Les mesures de [!UICONTROL Pageviews] des deux propriétés apparaissent alors dans Adobe Advertising sous les noms « Pageviews_ga :UK » et « Pageviews_ga :JP ». |

>[!MORELIKETHIS]
>
>* [À propos de la synchronisation [!DNL Google Analytics] des mesures de conversion](data-source-about.md)
>* [Conditions préalables à la configuration d’une source  [!DNL Google Analytics]  données](data-source-prerequisites.md)
>* [Configurer une [!DNL Google Analytics] vue comme source de données](data-source-configure.md)
>* [Modifier une source  [!DNL Google Analytics]  données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une source  [!DNL Google Analytics]  données](data-source-reauthenticate.md)
>* [Annexe - Mesures  [!DNL Google Analytics]  disponibles](data-source-ga-metrics.md)
