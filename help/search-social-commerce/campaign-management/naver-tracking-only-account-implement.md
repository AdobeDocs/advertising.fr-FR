---
title: Implémentation  [!DNL Naver]  comptes de tracking uniquement
description: Découvrez comment configurer des campagnes de tracking pour vos comptes  [!DNL Naver]  que vous puissiez suivre, générer des rapports et visualiser les performances des publicités que vous achetez directement à partir du réseau publicitaire.
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# Implémenter des comptes de suivi [!DNL Naver] uniquement

Comptes *[!DNL Naver]uniquement*

Vous pouvez créer des campagnes de suivi pour vos comptes [!DNL Naver] afin de suivre, de générer des rapports et de visualiser les performances des publicités que vous achetez directement à partir du réseau publicitaire. Search, Social et Commerce ne synchronisent pas les données avec le réseau publicitaire, ne chargent pas automatiquement le suivi et ne font pas d’enchères pour le compte.

Les campagnes de tracking répliquent vos campagnes, groupes publicitaires et mots-clés existants. Une fois la structure de compte créée dans Search, Social et Commerce et le suivi ajouté aux campagnes d’origine dans le réseau publicitaire, vous pouvez charger des mesures de trafic réseau quotidien pour vos mots-clés ou publicités. Search, Social et Commerce peuvent ensuite attribuer vos conversions à vos publicités et mots-clés.

Vous pouvez effectuer le suivi des mesures de performances pour toutes vos campagnes et pour n’importe quelle campagne, groupe publicitaire ou mot-clé/publicité. Vous pouvez également inclure des informations à leur sujet dans la plupart des rapports de base, avancés et d’assistance, ainsi que des données pour vos autres réseaux publicitaires. La prise en charge de l’exportation des mesures vers Adobe Analytics n’est pas disponible, mais Search, Social et Commerce peuvent synchroniser [les mesures dont vous effectuez le suivi [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) dans Search, Social et Commerce.

>[!NOTE]
>
>Vous ne pouvez pas ajouter de campagnes de suivi à un portfolio à des fins d’optimisation.

1. Créez des campagnes de tracking dans Search, Social et Commerce :

   1. Créer [détails de compte réseau factice](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). Si vous disposez de plusieurs comptes au sein d’un seul réseau publicitaire, consolidez-les en un seul compte dans la vue [!UICONTROL Accounts].

      [!DNL Naver] ne fournit pas de prise en charge d’API pour charger les paramètres de suivi sur le réseau publicitaire. Cependant, vous pouvez générer des paramètres de tracking à l’aide de feuilles d’envoi groupé et les ajouter manuellement dans le réseau publicitaire (voir Étape 2). Pour générer les paramètres de tracking, vous devez utiliser la méthode de tracking « [!UICONTROL EF Redirect] ». Vous pouvez éventuellement ajouter les paramètres d’ajout de votre choix.

      Search, Social et Commerce incluent automatiquement le paramètre `ev_cl={ef_uniqueid}` dans toutes les URL de tracking qu’il génère dans les feuilles d’envoi groupé pour le compte. Cet identifiant unique est utilisé pour faire correspondre les données de la campagne à tout coût et cliquer sur les données que vous chargez.

   1. Configurez les campagnes pour effectuer le suivi :

      1. Dans le réseau publicitaire, créez un fichier de feuille d’envoi groupé contenant toutes les entités, ainsi que leurs entités parentes requises, que vous souhaitez que Search, Social et Commerce effectuent le suivi pour le compte.

         Vous pouvez inclure des données sur les mots-clés, y compris les campagnes parentes et les groupes publicitaires.

      1. Modifiez le fichier de feuille d’envoi groupé, si nécessaire, afin qu’il suive le format de feuille d’envoi groupé Search, Social et Commerce [format requis pour les comptes  [!DNL Naver] &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. Dans Search, Social et Commerce, [téléchargez le fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >Remarque : Search, Social et Commerce ne publient pas les données sur le compte du réseau publicitaire.

1. Paramétrer le tracking des campagnes :

   1. Dans Search, Social et Commerce, [téléchargez un nouveau fichier de feuille d’envoi groupé](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) en utilisant l’option « [!UICONTROL Generate Tracking URLs] ».

   L’utilisation de l’option « [!UICONTROL Generate Tracking URLs] » renseigne le champ [!UICONTROL Destination URL] de chaque mot-clé avec le code de suivi Search, Social et Commerce précédé de la valeur [!UICONTROL Base URL].

   Voici un exemple de l’URL de destination avec tracking :

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. Copiez les valeurs [!UICONTROL Destination URL] du fichier de feuille d’envoi groupé téléchargé dans les paramètres de mots-clés appropriés sur le réseau.

      Vous pouvez ajouter les URL aux entités pertinentes en chargeant le fichier sur le réseau dans l’éditeur du réseau publicitaire. Dans ce cas, vous devrez peut-être supprimer certaines colonnes, en fonction des exigences en matière de données du réseau. Sinon, vous devez saisir les URL manuellement sur le réseau.

1. Téléchargez régulièrement des données sur les clics et les coûts agrégées quotidiennement à partir du réseau publicitaire pour les mots-clés ou les publicités de marque au niveau du groupe publicitaire que vous suivez, puis [téléchargez les données sur les clics et les coûts](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) vers Search, Social et Commerce au [format requis](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   Incluez la hiérarchie de compte complète et les mesures que vous souhaitez inclure. Les balises Search, Social et Commerce font correspondre les données chargées aux données des campagnes existantes.

1. (Facultatif) Si vous utilisez les balises du service de suivi des conversions Adobe Advertising dans vos pages web pour suivre les conversions qui ne sont pas suivies sur le réseau publicitaire, envoyez des fichiers de flux contenant des données de conversion agrégées par jour à ajouter à vos campagnes de suivi.

   Pour plus d’informations, contactez l’équipe chargée de votre compte Adobe.

Toutes les données de suivi chargées sont disponibles à partir de [!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] dans les vues [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups] et [!UICONTROL Keywords]. Elle est également disponible pour les rapports dans la vue [!UICONTROL Insights & Reports].

>[!MORELIKETHIS]
>
>* [Annexe - Données de feuille d’envoi groupé requises pour  [!DNL Naver]  comptes](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [Chargement des mesures de trafic et de conversion pour les comptes  [!DNL Naver]  suivi uniquement](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [Exigences en matière de données métriques pour les comptes  [!DNL Naver]  suivi uniquement](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [Formats de suivi des clics pour  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
