---
title: Mise en oeuvre [!DNL Naver] comptes de suivi uniquement
description: Découvrez comment configurer des campagnes de suivi pour vos [!DNL Naver] afin que vous puissiez suivre, créer des rapports et visualiser les performances des publicités que vous achetez directement depuis le réseau publicitaire.
source-git-commit: c4848da6c5489a5128a0424eef6a12f2c51caa12
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# Mise en oeuvre [!DNL Naver] comptes de suivi uniquement

*[!DNL Naver]comptes uniquement*

Vous pouvez créer des campagnes de suivi pour vos [!DNL Naver] afin que vous puissiez suivre, créer des rapports et visualiser les performances des publicités que vous achetez directement depuis le réseau publicitaire. Search, Social et Commerce ne synchronise pas les données avec le réseau publicitaire, ne télécharge pas automatiquement le suivi et n’envoie pas d’offres pour le compte.

Les campagnes de suivi répliquent vos campagnes, groupes publicitaires et mots-clés existants. Une fois que vous avez créé la structure de compte dans Search, Social et Commerce et ajouté le suivi aux campagnes d’origine dans le réseau publicitaire, vous pouvez charger des mesures de trafic réseau quotidiennes pour vos mots-clés ou annonces. Search, Social et Commerce peuvent ensuite attribuer vos conversions à vos publicités et mots-clés.

Vous pouvez effectuer le suivi des mesures de performances sur l’ensemble de vos campagnes et pour n’importe quelle campagne, groupe publicitaire ou mot-clé/publicité. Vous pouvez également inclure des informations les concernant dans les rapports les plus basiques, avancés et d’assistance, ainsi que des données pour vos autres réseaux publicitaires. La prise en charge de l’exportation des mesures vers Adobe Analytics n’est pas disponible, mais Search, Social et Commerce peuvent se synchroniser. [mesures dont vous effectuez le suivi dans [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) dans Search, Social et Commerce.

>[!NOTE]
>
>Vous ne pouvez pas ajouter de campagnes de suivi à un portfolio à des fins d’optimisation.

1. Créez des campagnes de suivi dans Search, Social et Commerce :

   1. Créer [détails factices du compte réseau](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Si vous disposez de plusieurs comptes dans un seul réseau publicitaire, consolidez-les dans un seul compte du [!UICONTROL Accounts] vue.

      [!DNL Naver] ne fournit pas de prise en charge d’API pour charger les paramètres de suivi vers le réseau publicitaire. Vous pouvez toutefois générer des paramètres de suivi à l’aide de feuilles d’envoi groupées et les ajouter manuellement au réseau publicitaire (par étape 2). Pour générer les paramètres de suivi, vous devez utiliser le[!UICONTROL EF Redirect]&quot; méthode de suivi. Vous pouvez éventuellement ajouter les paramètres d’ajout de votre choix.

      Search, Social et Commerce comprennent automatiquement le paramètre `ev_cl={ef_uniqueid}` dans les URL de suivi générées dans les feuilles d’envoi groupées du compte. Cet identifiant unique est utilisé pour faire correspondre les données de campagne à n’importe quel coût et cliquer sur les données que vous chargez.

   1. Configurez les campagnes à suivre :

      1. Dans le réseau publicitaire, créez un fichier de feuille d’envoi groupé contenant toutes les entités, ainsi que leurs entités parentes requises, dont vous souhaitez effectuer le suivi dans Search, Social et Commerce pour le compte.

         Vous pouvez inclure des données sur les mots-clés, y compris les campagnes et les groupes publicitaires parents.

      1. Si nécessaire, modifiez le fichier de feuille d’envoi groupé afin qu’il suive la section Recherche, Social et Commerce. [format de feuille d’envoi groupé requis pour [!DNL Naver] comptes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. Dans Search, Social et Commerce, [charger le fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Remarque : Search, Social et Commerce ne publie pas les données dans le compte de réseau publicitaire.

1. Configurez le suivi des campagnes :

   1. Dans Search, Social et Commerce, [téléchargement d’un nouveau fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) à l’aide de l’option &quot;[!UICONTROL Generate Tracking URLs].&quot;
   En utilisant le[!UICONTROL Generate Tracking URLs]&quot; renseigne la variable [!UICONTROL Destination URL] pour chaque mot-clé avec le code de suivi de recherche, Social et Commerce précédé du préfixe [!UICONTROL Base URL] .

   Voici un exemple de l’URL de destination avec suivi :

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Copiez le [!UICONTROL Destination URL] des valeurs du fichier de feuille d’envoi groupé téléchargé correspondant aux paramètres de mots-clés appropriés sur le réseau.

      Vous pouvez ajouter les URL aux entités concernées en chargeant le fichier sur le réseau au sein de l’éditeur du réseau publicitaire. Dans ce cas, vous devrez peut-être supprimer certaines colonnes, en fonction des exigences de données du réseau. Sinon, vous devez saisir les URL manuellement sur le réseau.


1. Téléchargez régulièrement des données sur les clics et les coûts agrégées quotidiennement à partir du réseau publicitaire pour les mots-clés ou les publicités de marque au niveau du groupe publicitaire dont vous effectuez le suivi, puis [charger les données de clics et de coûts](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) pour rechercher, Social et Commerce dans le [format requis](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Incluez la hiérarchie complète du compte et toutes les mesures que vous souhaitez inclure. Search, Social et Commerce associe les données transférées aux données des campagnes existantes.

1. (Facultatif) Si vous utilisez les balises du service de suivi de conversion Adobe Advertising dans vos pages web pour suivre les conversions qui ne sont pas suivies sur le réseau publicitaire, envoyez alors des fichiers de flux contenant des données de conversion agrégées quotidiennement à ajouter à vos campagnes de suivi.

   Pour plus d’informations, contactez votre équipe de compte d’Adobe.

Toutes les données de suivi chargées sont disponibles à partir de [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] dans le [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups], et [!UICONTROL Keywords] vues. Il est également disponible pour les rapports dans la [!UICONTROL Insights & Reports] vue.

>[!MORELIKETHIS]
>
>* [Annexe : Données de feuille d’envoi groupé requises pour [!DNL Naver] comptes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Chargement des mesures de trafic et de conversion pour [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Exigences de données de mesure pour [!DNL Naver] comptes de suivi uniquement](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Formats de suivi des clics pour [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)

