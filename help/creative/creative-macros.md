---
title: Macros disponibles pour le tracking des URL
description: Référencez les macros que vous pouvez ajouter à vos URL de page de destination, URL de tracking et contenus publicitaires tiers.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
TQID: https://experienceleague.adobe.com/J5jfIECrL29NngVOulEgHKZBHYqBmoz4680HzEzhIng
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 3c3bffe0c28bb24c0df9385f9cc91be1376a66d2
workflow-type: tm+mt
source-wordcount: 319
ht-degree: 0%

---

# Macros disponibles pour le tracking des URL

<!-- More feature metadata???  -->

Vous pouvez inclure l’une des macros suivantes dans vos contenus publicitaires tiers, dans les URL de suivi tierces pour vos expériences et dans les URL de page de destination pour votre propre utilisation.

Certaines des macros disponibles, ou leurs équivalents, sont automatiquement incluses dans les balises d’expérience.

<!--
 Later: 

| Macro | Description | Automatically in experience tags for Advertising DSP? | Automatically in experience tags for [!DNL Google Campaign Manager 360]? |
| --- | --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Tracks and reports the campaign ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ebuy!` |
| `${TM_SITE_ID_NUM}` | Tracks and reports the site ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%esid!` |
| `${TM_PLACEMENT_ID_NUM}` | Tracks and reports the placement ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%epid!` |
| `${TM_AD_ID_NUM}` | Tracks and reports the ad ID from the DSP | Yes | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%eaid!` |
| `${TM_CREATIVE_ID_NUM}` | Tracks and reports the creative ID from the DSP | N/A | No, but tags include the equivalent [!DNL Google Campaign Manager 360] macro `%ecid!` |
| `${TM_SESSION_ID}` | Tracks and reports the impression ID from the DSP. If a value isn't returned, Advertising Creative generates one. | Yes | &mdash; |
| `${TM_ACC_EXPERIENCE_ID}` | Tracks and reports the Advertising Creative experience ID | &mdash; | &mdash; |
| `${TM_ACC_CREATIVE_ID}` | Tracks and reports the Advertising Creative creative ID | &mdash; | &mdash; |
| `${TM_RANDOM}` | A random number between 1 and 1000000 | &mdash; | &mdash; |
| `${TM_TIMESTAMP}` | The Unix Timestamp (in seconds) | &mdash; | &mdash; |
| `${TM_CLICK_URL_URLENC}` | (For third-party ads from vendors who require URL encoding) The encoded click redirect URL, which enables ad servers to track and count ad clicks. When the ad is served and the user clicks on it, the macro is activated, and the click is recorded and counted for reporting purposes. | Yes | &mdash; |
| `${TC_1}` | Custom tracking code 1. | &mdash; | &mdash; |
| `${TC_2}` | Custom tracking code 2. | &mdash; | &mdash; |
| `${TC_3}` | Custom tracking code 3. | &mdash; | &mdash; |
| `${TC_4}` | Custom tracking code 4. | &mdash; | &mdash; |
| `${TC_5}` | Custom tracking code 5. | &mdash; | &mdash; |
| `${GDPR_ENFORCED}` | Whether GDPR enforcement is required for the bid request. Values: **1** = GDPR should be enforced, **0** = GDPR should not be enforced. | &mdash; | &mdash; |
| `${GDPR_CONSENT}` | The GDPR consent value received from the supply partner in the bid request. Typically: **1** = consent provided, **0** = no consent provided. | &mdash; | &mdash; |
-->

| Macro | Description | Automatiquement dans les balises d’expérience pour Advertising DSP ? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Effectue le suivi et génère des rapports sur l’identifiant de campagne à partir du DSP | Oui |
| `${TM_SITE_ID_NUM}` | Effectue le suivi et génère des rapports sur l’ID de site à partir du DSP | Oui |
| `${TM_PLACEMENT_ID_NUM}` | Effectue le suivi et génère des rapports sur l’ID d’emplacement à partir du DSP | Oui |
| `${TM_AD_ID_NUM}` | Effectue le suivi et génère des rapports sur l’ID d’annonce publicitaire à partir du DSP | Oui |
| `${TM_CREATIVE_ID_NUM}` | Effectue le suivi et génère des rapports sur l’ID de contenu créatif à partir du DSP | S.O. |
| `${TM_SESSION_ID}` | Effectue le suivi et génère des rapports sur l’ID de session associé à la demande de publicité. Si une valeur n’est pas renvoyée, Advertising Creative en génère une. | Oui |
| `${TM_ACC_EXPERIENCE_ID}` | Effectue le suivi et génère des rapports sur l’Experience ID Advertising Creative | — |
| `${TM_ACC_CREATIVE_ID}` | Effectue le suivi et génère des rapports sur l’ID de contenu créatif Advertising Creative | — |
| `${TM_RANDOM}` | Nombre généré de manière aléatoire compris entre 1 et 1 000 000. Généralement utilisé pour le démantèlement de cache. | — |
| `${TM_TIMESTAMP}` | Date et heure UNIX® (en secondes) | — |
| `${TM_CLICK_URL_URLENC}` | (Pour les annonces tierces provenant de fournisseurs qui nécessitent un codage d’URL) L’URL de redirection de clics codée, qui permet aux serveurs de publicités de suivre et de compter les clics publicitaires. Lorsqu’un utilisateur clique sur la publicité, la macro est activée, et le clic est enregistré et comptabilisé à des fins de création de rapports. | Oui |
| `${TC_1}` | Code de suivi personnalisé 1. | — |
| `${TC_2}` | Code de suivi personnalisé 2. | — |
| `${TC_3}` | Code de suivi personnalisé 3. | — |
| `${TC_4}` | Code de suivi personnalisé 4. | — |
| `${TC_5}` | Code de suivi personnalisé 5. | — |
| `${GDPR_ENFORCED}` | Indique si l’application du RGPD est requise pour la demande d’offre. Valeurs : **1** = le RGPD doit être appliqué, **0** = le RGPD ne doit pas être appliqué. | — |
| `${GDPR_CONSENT}` | Valeur de consentement RGPD reçue du partenaire d’approvisionnement dans la demande d’offre. En règle générale : **1** = consentement fourni, **0** = aucun consentement fourni. | — |

>[!MORELIKETHIS]
>
>* [Ajouter des contenus publicitaires standard à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Paramètres de création standard](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [Paramètres d’expérience ciblés*[Paramètres d’expérience non ciblés](/help/creative/experiences/experience-settings-no-targeting.md)
