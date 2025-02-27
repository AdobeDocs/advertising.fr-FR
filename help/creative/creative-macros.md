---
title: Macros disponibles pour le tracking des URL
description: Référencez les macros que vous pouvez ajouter à vos URL de page de destination, URL de tracking et contenus publicitaires tiers.
feature: Creative Experiences, Creative Experiences
exl-id: d0cbbb21-467d-4ed1-bc6e-ded1b045b98b
source-git-commit: fe3e991f1fba2944e7a3f8e4930c48c7dbd28770
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Macros disponibles pour le tracking des URL

*Version bêta fermée*

<!-- More feature metadata??? -->

Vous pouvez inclure l’une des macros suivantes dans vos contenus publicitaires tiers, dans les URL de suivi tierces pour vos expériences et dans les URL de page de destination pour votre propre utilisation.

Certaines des macros disponibles, ou leurs équivalents, sont automatiquement incluses dans les balises d’expérience.

<!-- Later: 

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

-->

| Macro | Description | Automatiquement dans les balises d’expérience pour Advertising DSP ? |
| --- | --- | --- |
| `${TM_CAMPAIGN_ID_NUM}` | Effectue le suivi et génère des rapports sur l’identifiant de campagne à partir du DSP | Oui |
| `${TM_SITE_ID_NUM}` | Effectue le suivi et génère des rapports sur l’ID de site à partir du DSP | Oui |
| `${TM_PLACEMENT_ID_NUM}` | Effectue le suivi et génère des rapports sur l’ID d’emplacement à partir du DSP | Oui |
| `${TM_AD_ID_NUM}` | Effectue le suivi et génère des rapports sur l’ID d’annonce publicitaire à partir du DSP | Oui |
| `${TM_CREATIVE_ID_NUM}` | Effectue le suivi et génère des rapports sur l’ID de contenu créatif à partir du DSP | S.O. |
| `${TM_SESSION_ID}` | Effectue le suivi et génère des rapports sur l’ID d’impression à partir du DSP. Si une valeur n’est pas renvoyée, Advertising Creative en génère une. | Oui |
| `${TM_ACC_EXPERIENCE_ID}` | Effectue le suivi et génère des rapports sur l’Experience ID Advertising Creative | — |
| `${TM_ACC_CREATIVE_ID}` | Effectue le suivi et génère des rapports sur l’ID de contenu créatif Advertising Creative | — |
| `${TM_RANDOM}` | Un nombre aléatoire compris entre 1 et 1000000 | — |
| `${TM_TIMESTAMP}` | Date et heure UNIX® (en secondes) | — |
| `${TM_CLICK_URL_URLENC}` | (Pour les annonces tierces provenant de fournisseurs qui nécessitent un codage d’URL) L’URL de redirection de clics codée, qui permet aux serveurs de publicités de suivre et de compter les clics publicitaires. Lorsque l’utilisateur clique sur la publicité, la macro est activée et le clic est enregistré et comptabilisé à des fins de création de rapports. | Oui |

>[!MORELIKETHIS]
>
>* [Ajouter des contenus publicitaires standard à une bibliothèque de contenus publicitaires](/help/creative/creative-libraries/creative-add-standard.md#creative-add-third-party)
>* [Paramètres de création standard](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party)
>* [Paramètres d’expérience ciblés](/help/creative/experiences/experience-settings-targeting.md)
>*[Paramètres d’expérience non ciblés](/help/creative/experiences/experience-settings-no-targeting.md)
