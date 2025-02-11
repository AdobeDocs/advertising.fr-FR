---
title: Macros Advertising DSP
description: Référencez les macros disponibles pour le suivi général et pour effectuer le suivi des clics sur les publicités display tierces.
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Macros Advertising DSP

Une macro est une commande courte ou un raccourci pour une instruction et suit généralement le format `${MACRO_NAME}`. Les macros incluses dans le code créatif ou les URL de clic publicitaire se développent en une chaîne de code plus longue que le serveur de publicités peut comprendre. Le serveur de publicités DSP exécute des macros lorsque la publicité est diffusée ou que l’utilisateur clique dessus.

Les macros de serveur de publicités sont utiles pour transmettre des informations importantes à DSP ou à des serveurs de publicités tiers. Les macros sont le plus souvent utilisées lors du trafic de code créatif ou de métadonnées tiers et personnalisés (comme les pixels tiers).

Vous pouvez insérer manuellement une macro n’importe où, par exemple dans une balise VAST, dans n’importe quelle URL ou dans un pixel d’événement DSP ou tiers. Cependant, chaque client et partenaire DSP possède un format de balise publicitaire différent et les macros doivent être insérées à différents endroits dans la balise en conséquence. Chaque fois que vous travaillez avec un nouveau client ou partenaire, demandez-lui de la documentation sur l’emplacement où insérer les macros dans ses balises publicitaires qui font l’objet du trafic DSP.

## Macros de tracking générales

Utilisez les macros de suivi générales sur tous les types d’annonces et de balises pour transmettre des données spécifiques, selon les besoins.

| Macro | Description du remplacement | Type |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | Identifiant de compte. | nombre entier |
| `${TM_AD_ID}` | La clé publicitaire (adKey). | chaîne |
| `${TM_AD_ID_NUM}` | L’ID de la publicité. | nombre entier |
| `${TM_ADVERTISER_ID}` | ID de l’annonceur. | nombre entier |
| `${TM_CAMPAIGN_ID}` | La clé de la campagne. | chaîne |
| `${TM_CAMPAIGN_ID_NUM}` | Identifiant de campagne. | nombre entier |
| ` ${TM_CLICK_URL}` | L’URL de redirection, qui permet aux serveurs de publicités de suivre et de compter les clics publicitaires. Lorsque la publicité est diffusée, si l&#39;utilisateur clique dessus, la macro est activée et le clic est enregistré et comptabilisé à des fins de reporting. | chaîne |
| ` ${TM_CLICK_URL_URLENC}` | L’URL de redirection codée, qui permet aux serveurs de publicités de suivre et de compter les clics publicitaires. Lorsque la publicité est diffusée, si l&#39;utilisateur clique dessus, la macro est activée et le clic est enregistré et comptabilisé à des fins de reporting. N’utilisez pas cette macro, sauf si vous créez des annonces tierces et que votre fournisseur requiert un codage d’URL. | chaîne |
| `${TM_FEED_ID}` | Clé de l’emplacement du média (feedKey). | chaîne |
| `${TM_FEED_ID_NUM}` | Identifiant de l’emplacement du média. | nombre entier |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | Clé de site de l’emplacement. Obligatoire pour les dispositifs de suivi des clics [!DNL AppsFlyer] pour les annonces d’installation des applications mobiles.<!-- should map to placement_site_key column of placement_site table --> | chaîne |
| `${TM_PLACEMENT_ID}` | Clé de positionnement (cpKey). | chaîne |
| `${TM_PLACEMENT_ID_NUM}` | Identifiant d’emplacement. | nombre entier |
| `${TM_RANDOM}` | Cachebuster : un nombre aléatoire compris entre 1 et 1000000. | long |
| `${TM_SESSION_ID}` | L’identifiant de la session, qui correspond à une seule récupération de la balise d’annonce. | chaîne |
| `${TM_SITE_DOMAIN_URLENC}` | Sous-domaine de page analysé à partir de l’URL dans la demande d’offre ; encodé en URL. Non pris en charge pour les publicités dans la bannière et les clics à lire. | chaîne |
| ` ${TM_SITE_NAME}` | Nom du site de l’emplacement. | chaîne |
| `${TM_SITE_URL_URLENC}` | URL transmise dans la demande d’enchères ; encodée en URL. Non pris en charge pour les publicités dans la bannière et les clics à lire. | chaîne |
| `${TM_SITE_ID_NUM}` | Identifiant de site pour l’emplacement. | nombre entier |
| `${TM_TIMESTAMP}` | Horodatage Unix indiquant le nombre de secondes écoulées depuis minuit (00:00 UTC) le 1er janvier 1970. | long |
| ` ${TM_VIDEO_DURATION}` | Durée de la vidéo publicitaire en secondes. | nombre entier |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## Macros Spécifiques À Mobile

| Macro | Description du remplacement | Type |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | ([!DNL ComScore]) Identifiant de la plateforme, qui correspond au système d’exploitation de l’appareil :<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` lorsque la plateforme ne correspond à aucune des conditions ci-dessus</li></ul> | varchar(50) |
| `${CS_DEVICE_MODEL}` | ([!DNL ComScore]) Nom du modèle d’appareil, encodé en URL. | chaîne |
| `${CS_IMPLEMENTATION_TYPE}` | ([!DNL ComScore]) Environnement dans lequel la publicité a été diffusée :<ul><li>`a` = application mobile</li><li>`b` = site web mobile</li></ul> | chaîne (`a` ou `b`) |
| `${NS_PLATFORM_ID}` | ([!DNL Nielsen]) Identifiant de la plateforme, qui correspond au système d’exploitation de l’appareil :<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` lorsque la plateforme ne correspond à aucune des conditions ci-dessus</li></ul> | chaîne |
| `${NS_DEVICE_GROUPING}` | ([!DNL Nielsen]) Type d’appareil sur lequel la publicité a été visionnée :<ul><li>`TAB` = comprimé</li><li>`PHN` = mobile</li><li>`computer` = ordinateur</li></ul> | chaîne |
| `${UOO}` | ([!DNL Nielsen]) Que l’utilisateur se soit opposé ou non au suivi des publicités :<ul><li>`1` (indicateur DNT = 1) = l’utilisateur s’est opposé au suivi des publicités</li><li>`0` (indicateur DNT = 0) = l’utilisateur a choisi d’effectuer le suivi des publicités</li></ul> | entier (`0` ou `1`) |
| `${TM_BUNDLE}` | L’identifiant de lot de la boutique d’applications [!DNL iOS] ou [!DNL Android]. Exemples : com.zynga.wwf2.free ou id804379658 | chaîne |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` indique si le soumissionnaire détermine que la demande d’offre provient de l’Union européenne et nécessite l’application du RGPD :<ul><li>`1` = Le RGPD doit être appliqué.</li><li>`0` = Le RGPD ne doit pas être appliqué</li></ul>`gdpr_consent=${GDPR_CONSENT}` est la valeur de consentement transmise par le partenaire d’approvisionnement dans la demande d’offre entrante :<ul><li>Dans la plupart des cas, il s’agit d’une chaîne de consentement codée en base64url, ou daisybit (exemple : BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA)</li><li>`0` = aucun consentement</li><li>`1` = consentement</li></ul> | daisybit ou entier |

{style="table-layout:auto"}

## Clic sur les macros pour les publicités display tierces

Pour effectuer le suivi précis des clics sur les publicités à l’aide de balises d’affichage tierces, DSP requiert une macro de clic d’affichage. Une seule version de la macro est requise ; la macro appropriée dépend du type de balise.

| Macro | Description du remplacement | Type |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | URL de redirection qui permet aux serveurs de publicités de suivre et de compter les clics publicitaires sur la plateforme. | chaîne |
| `${TM_CLICK_URL_URLENC}` | L’URL de redirection qui permet aux serveurs de publicités nécessitant un codage d’URL de suivre et de compter les clics de publicités dans la plateforme. | chaîne |

{style="table-layout:auto"}

DSP insère automatiquement des macros de clics d’affichage dans une balise d’affichage tierce lorsque vous :

* Exporter les balises d’annonce publicitaire d’un <!-- [Needs PM confirmation.] --> de partenaire de serveur d’annonces
* Chargement en masse de [!DNL Flashtalking] ou [!DNL Google DoubleClick for Advertisers] ajout de balises directement dans DSP

Si une macro de clic est manquante lorsque vous créez une publicité display, DSP affiche un message d&#39;avertissement qui vous invite à insérer manuellement la macro de clic display appropriée dans la zone appropriée de la balise.

## Macros [!DNL Analytics for Advertising]

Pour obtenir des macros supplémentaires disponibles spécifiquement pour les clients [[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md), reportez-vous aux sections [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](/help/integrations/analytics/macros-flashtalking.md) et [Append [!DNL Analytics for Advertising] Macros to [!DNL Google Campaign Manager 360] Ad Tags](/help/integrations/analytics/macros-google-campaign-manager.md).

## Résolution des erreurs de macro

Lorsque vous ajoutez des macros à votre code, veillez à utiliser la syntaxe exacte de la macro. Lors de la validation des macros, DSP vérifie que la macro correspond exactement à l’une des macros valides.

Des erreurs sont générées si des caractères manquent au début ou à la fin du nom de la macro. Par exemple, un message d’erreur s’affiche si :

* Vous oubliez un ou plusieurs caractères au début du nom de la macro, tels que `${`. Si vous n’incluez pas la syntaxe complète, l’entrée n’est pas reconnue comme une macro valide.
* La macro ne se termine pas par un jeu de caractères valide, tel que `}`.

>[!MORELIKETHIS]
>
>* [Paramètres de publicité audio](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Paramètres des publicités TV connectées](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Afficher les paramètres de publicité](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Paramètres des annonces publicitaires mobiles](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Paramètres de publicité natifs](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Paramètres de publicité preroll](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [Paramètres universels des publicités vidéo](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
