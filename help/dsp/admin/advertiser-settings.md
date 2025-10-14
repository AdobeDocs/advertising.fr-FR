---
title: Paramètres du compte publicitaire
description: Voir les descriptions des paramètres d’annonceur disponibles.
role: User, Admin
source-git-commit: 1f8a76e060612cdcc8ee3709bdf49654faf31b57
workflow-type: tm+mt
source-wordcount: '943'
ht-degree: 0%

---

# Paramètres du compte publicitaire

*Non disponible pour les utilisateurs en lecture seule*

<!-- Not published -->

## [!UICONTROL General] Settings

**[!UICONTROL Advertiser Name]:** nom de l’annonceur.

**[!UICONTROL Category]:** catégorie dans laquelle l’entreprise de l’annonceur opère. La catégorie est communiquée aux éditeurs lorsque vous enchérissez sur le stock. Veillez à choisir une catégorie qui correspond à vos publicités, faute de quoi les éditeurs peuvent les rejeter.

>[!NOTE]
>
>Si vous sélectionnez *[!UICONTROL Other]*, l’annonceur ne peut pas accéder au [!DNL On Demand Inventory] DSP.

**[!UICONTROL Advertiser URL]:** page d’accueil de l’annonceur ou URL du site web principal (commençant par `http://` ou `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Nouveaux comptes d’annonceur uniquement) Met tous les flux d’échange privé configurés pour le compte DSP de l’organisation à la disposition de l’annonceur.

### [!UICONTROL Adobe IMS IDs]

Les annonceurs qui disposent de produits Adobe Experience Cloud supplémentaires peuvent partager des données entre certains produits à l’aide de l’identifiant unique de l’organisation pour Experience Cloud. Vous pouvez configurer des intégrations de produits spécifiques dans la section [!UICONTROL Integrations] .

**[!UICONTROL Account IMS org and ID]:** (annonceurs avec des produits Experience Cloud supplémentaires mis sous licence par le biais d’un compte Experience Cloud avec plusieurs annonceurs ; facultatif) ID d’organisation Experience Cloud de l’annonceur.

**[!UICONTROL Advertiser IMS org and ID]:** (annonceurs disposant de licences directes pour des produits Experience Cloud supplémentaires ; facultatif) ID d’organisation Experience Cloud de l’annonceur.

### [!UICONTROL Integrations]

(Facultatif) Produits Experience Cloud supplémentaires liés au compte DSP. Les produits doivent être associés au même identifiant d’organisation Experience Cloud que celui fourni dans la section [!UICONTROL Adobe IMS IDs] .

**[!UICONTROL Attribution services]** > **[!UICONTROL Adobe Media Optimizer]:** (annonceurs avec des [!DNL Advertising Search, Social, & Commerce] ou qui utilisent des pixels de conversion Adobe Advertising) Compte [!DNL Search, Social, & Commerce] avec lequel DSP échange des données d’attribution.

**[!UICONTROL Report suites]** > **[!UICONTROL Adobe Analytics]:** (annonceurs avec Adobe Analytics ; facultatif ; applicable uniquement aux données collectées à l’aide des balises de suivi de conversion Adobe Advertising qui incluent un [!DNL EF Redirect] et un jeton uniquement) Une ou plusieurs suites de rapports [!DNL Analytics] auxquelles DSP envoie les données qu’il collecte auprès des éditeurs et des partenaires côté offre. Analytics envoie également vers DSP les données qu’il collecte sur le site du client.

Pour que les données apparaissent dans les suites de rapports, le paramètre au niveau de l’annonceur [!DNL Search, Social, & Commerce] approprié doit être activé. En outre, le compte [!DNL Analytics] de l’annonceur doit être configuré pour recevoir des données d’Adobe Advertising.

>[!WARNING]
>
>Si vous supprimez une suite de rapports précédemment liée, DSP n’échange plus de données avec cette suite. Attendez-vous à voir des fluctuations de données.

Pour plus d’informations sur l’intégration d’à [!DNL Analytics], consultez « [&#x200B; Présentation d’ [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) ».

**[!UICONTROL Audiences]** > **[!UICONTROL Adobe Analytics Cloud]:** (annonceurs avec Adobe Audience Manager ou Adobe Analytics ; facultatif) Compte Audience Manager ou [!DNL Analytics] à partir duquel DSP extrait les métadonnées de segment, les données de hiérarchie et les données d’audience uniques pour toutes les audiences Adobe de l’annonceur. Cela inclut les données pour :

* Segments Audience Manager
* [!DNL Analytics] les segments publiés sur Adobe Experience Cloud
* Segments créés à l’aide de l’[!DNL Audience Library] Adobe Experience Cloud
* Segments créés dans Adobe Experience Platform et envoyés à Adobe Advertising via Audience Manager

La synchronisation initiale prend environ 24 heures. Ensuite, les données sont synchronisées en temps réel, avec un délai d’une à deux secondes.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Settings

Vous pouvez éventuellement configurer des cibles par défaut pour les nouveaux emplacements de l’annonceur. Les utilisateurs peuvent remplacer les cibles par défaut pour tout nouvel emplacement.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** pays par défaut pour le géociblage de chaque emplacement. Les utilisateurs peuvent changer de pays et paramétrer un géociblage plus spécifique pour chaque emplacement.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** audiences ou segments à supprimer par défaut. Les utilisateurs peuvent modifier les exclusions pour chaque emplacement.

### [!UICONTROL Media Quality]

<!-- See placement settings for specs on applicable ad/device types -->

#### [!UICONTROL Contextual Filtering]

Types de filtres contextuels [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39] à appliquer. Vous pouvez remplacer les paramètres au niveau de l’annonceur au [niveau de l’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (facultatif) Un ou plusieurs types de contexte d&#39;inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (facultatif) Un ou plusieurs types d’attributs d’inventaire à cibler par défaut. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (facultatif) Un ou plusieurs types d’attributs d’inventaire à bloquer par défaut. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (facultatif) Degré de contenu pour adultes pour lequel les annonces doivent être bloquées par défaut : *[!UICONTROL Do Not Block]* (par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Alcohol Content]:** (facultatif) Degré de teneur en alcool pour lequel bloquer les publicités par défaut : *[!UICONTROL Do Not Block]* (par défaut), *[!UICONTROL Standard]* ou *[!UICONTROL Strict]*. Des frais supplémentaires peuvent s’appliquer.

#### [!UICONTROL Pre-Bid Fraud Blocking] {#prebid-fraud-blocking}

Types de sites à bloquer en fonction du trafic frauduleux et des activités suspectes mesurées par [!DNL DoubleVerify], [!DNL Integral Ad Science] et [!DNL Peer39]. Vous pouvez remplacer les paramètres au niveau de l’annonceur au [niveau de l’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Par défaut, bloque tout le trafic 100 % non valide, y compris le trafic sur les appareils détournés, pour les nouveaux emplacements. Des frais supplémentaires peuvent s’appliquer.

**[!UICONTROL Also block sites with]:** (facultatif) niveau supplémentaire de fraude et de trafic non valide qui entraîne le blocage des publicités par défaut par DSP : *[!UICONTROL None]* (la valeur par défaut, qui ne bloque pas le trafic supplémentaire), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* ou *[!UICONTROL >25% Average Fraud/IVT levels]*. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (facultatif) Un ou plusieurs types de fraude qui entraînent le blocage des publicités par défaut par DSP : *[!UICONTROL Fraud]* (qui bloque tous les sites comportant une fraude), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* et/ou *[!UICONTROL Fraud: Zero Ads]*. Des frais supplémentaires peuvent s’appliquer.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (facultatif) Type d’activité suspecte de site web ou d’application qui entraîne le blocage des annonces par défaut par DSP : *[!UICONTROL None]* (valeur par défaut, qui ne bloque pas les annonces en raison d’une activité suspecte), *[!UICONTROL Suspicious Activity - High Risk]* ou *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Des frais supplémentaires peuvent s’appliquer.

#### [!UICONTROL Pre-Bid Viewability]

Les filtres de visibilité de pré-enchères facultatifs par [!DNL DoubleVerify] et [!DNL Integral Ad Science] à appliquer aux emplacements. Les valeurs par défaut au niveau de l’annonceur sont sélectionnées pour les nouveaux emplacements. Vous pouvez remplacer les paramètres au niveau de l’annonceur au [niveau de l’emplacement](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-viewability}

###### Vidéo

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Include URL's whose average video viewability rate is]**. Avec cette option, sélectionnez les critères.

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Impressions with Insufficient IAB Viewability Data]**

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Include URL's whose average completion & fully viewable rate is]**. Avec cette option, sélectionnez les critères.

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Include URL's whose average player size composition is]**. Avec cette option, sélectionnez les critères.

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Impressions with Insufficient Player Size Statistics]**

###### Affichage

**&#x200B; &#x200B;**&#x200B;[!UICONTROL Only target URL's or Apps that have historically achieved a display viewability rate of]**. Avec cette option, sélectionnez les critères.

* **[!UICONTROL Impressions with Insufficient IAB Viewability Performance Data]**

* **[!UICONTROL Include Apps and URL's whose average entire creative (100% of pixels) viewable duration is]**. Avec cette option, sélectionnez les critères.

* **[!UICONTROL Impressions with Insufficient BXD Performance Data]**

##### [!UICONTROL Integral Ad Science] {#ias-viewability}

Un filtre **[!UICONTROL Video Viewability Targets]** facultatif et un filtre **[!UICONTROL Display Viewability Targets]** facultatif. Des frais supplémentaires peuvent s’appliquer.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** par défaut, quel niveau de [[!DNL Ads.txt] filtrage de pré-enchères](https://iabtechlab.com/ads-txt-about/) utiliser en exploitant la liste [!DNL Authorized Digital Sellers] de chaque éditeur :
* *[!UICONTROL Opt out of ads.txt (default)]* : Pour acheter des stocks auprès de tous les vendeurs.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]* : pour donner la priorité à l’achat de stocks auprès des vendeurs directs et des revendeurs autorisés d’un domaine.
* *[!UICONTROL Ads.txt sellers only]* : Pour acheter des stocks uniquement auprès des vendeurs directs et des revendeurs autorisés d&#39;un domaine.
* *[!UICONTROL Ads.txt sellers only]* : Pour acheter des stocks uniquement auprès des vendeurs directs autorisés d&#39;un domaine.

Vous pouvez remplacer le paramètre au niveau de l’annonceur au [&#x200B; niveau de l’emplacement &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** active par défaut un filtre de post-enchères en temps réel pour s’assurer que les publicités sont diffusées sur les sites ciblés par l’annonceur. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Suitability]

**[!UICONTROL DoubleVerify Account]:** (clients [!DNL DoubleVerify] uniquement ; facultatif) identifiant de segment [!DNL DoubleVerify Authentic Brand Safety] associé au compte [!DNL DoubleVerify] de l’organisation à utiliser par défaut pour tous les emplacements. La spécification d’un ID bloque les impressions après l’enchère à l’aide des règles de sécurité de marque personnalisées configurées pour l’ID de segment spécifié. DSP facture votre compte pour l’utilisation de l’identifiant de segment.

L’identifiant doit commencer par « 51 » et se composer de huit chiffres. Vous pouvez modifier ou supprimer l’ID au niveau de l’annonceur au niveau de l’emplacement.

>[!MORELIKETHIS]
>
>* [Créer un compte publicitaire](/help/dsp/admin/advertiser-create.md)

<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
