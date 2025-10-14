---
title: Ajouter des  [!DNL Analytics for Advertising] macros à [!DNL Google Campaign Manager 360] balises de publicité
description: Découvrez pourquoi et comment ajouter des  [!DNL Analytics for Advertising] macros à vos  [!DNL Google Campaign Manager 360] balises publicitaires
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Ajout de [!DNL Analytics for Advertising] macros à [!DNL Google Campaign Manager 360] balises publicitaires

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable à Advertising DSP uniquement*

Si vous utilisez des balises d’annonce [!DNL Google Campaign Manager 360] pour vos publicités Advertising DSP, ajoutez les paramètres [!DNL Analytics for Advertising] aux URL de votre page d’entrée à l’aide de la [`%p` macro](https://support.google.com/campaignmanager/table/6096962). Les paramètres enregistrent les paramètres de chaîne de requête AMO ID (`s_kwcid`) et `ef_id` dans l’URL de la page d’entrée, ce qui permet à l’Adobe Advertising d’envoyer des données de clic pour les publicités à Adobe Analytics.

Utilisez des macros pour [!DNL Campaign Manager 360] publicités vidéo et display pour les types suivants de mises en oeuvre de [!DNL Analytics for Advertising] :

* **Les annonceurs dont le code JavaScript [!DNL Adobe] [!DNL Analytics for Advertising] est implémenté sur leurs sites web** : le code JavaScript enregistre déjà les paramètres de chaîne de requête AMO ID (`s_kwcid`) et `ef_id`. Cependant, l’utilisation de macros étend le suivi pour inclure les conversions basées sur les clics lorsque les cookies tiers ne sont pas pris en charge. La bonne pratique consiste à ajouter les macros des sections suivantes à vos balises publicitaires afin de capturer des données de clics publicitaires supplémentaires qui ne sont pas capturées par le code JavaScript.

>[!NOTE]
>
>Le code JavaScript est une solution pour le suivi des clics uniquement lorsque les cookies sont toujours disponibles. Une fois les cookies arrêtés, la mise en oeuvre des macros suivantes est nécessaire.

* **Les annonceurs dont les sites web n’utilisent pas le code JavaScript [!DNL Analytics for Advertising] et utilisent à la place le transfert côté serveur [!DNL Analytics] pour les données de clic publicitaire uniquement** (sans données d’affichage publicitaire) : les macros suivantes sont requises pour signaler l’activité de clic sur site basée sur les publicités que vous achetez par le biais de l’Adobe Advertising.

## Ajout de macros à vos publicités [!DNL Google Campaign Manager 360]

Dans [!DNL Google Campaign Manager 360], ajoutez le paramètre suivant à l&#39;URL de la page d&#39;entrée pour chacune de vos publicités vidéo et display : `%pamo=!;`

Vous pouvez spécifier l&#39;URL de la landing page de plusieurs manières. Les instructions pour chaque option sont incluses dans les sous-sections suivantes.

Voici un exemple d’URL de page d’entrée formatée avec le suffixe .

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* Si l’URL de la page d’entrée contient un symbole de hachage (#), qui n’est pas courant, placez le paramètre `amo` avant le symbole de hachage.
>* Si aucun autre paramètre n’est inclus après le paramètre `amo`, ajoutez-y un paramètre (par exemple, &amp;a=b). Exemple : `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configuration du suffixe d’URL de page d’entrée au niveau des annonceurs

1. Voir les [&#x200B; instructions pour ouvrir les propriétés de l’annonceur &#x200B;](https://support.google.com/campaignmanager/answer/2829344).
1. Dans les paramètres [!UICONTROL Landing page URL suffix], incluez `%pamo!;` dans le champ [!UICONTROL URL suffix].

### Configuration du suffixe d’URL de page d’entrée de niveau Campaign

1. Voir les [instructions pour ouvrir les propriétés de campagne](https://support.google.com/campaignmanager/answer/2838056#set).
1. Dans les paramètres [!UICONTROL Landing page URL suffix], incluez `%pamo!;` dans le champ [!UICONTROL URL suffix].

### Configuration du suffixe d’URL de page d’entrée Creative

1. Ouvrez les propriétés de création.
1. Dans le paramètre [!UICONTROL Click tags] , incluez `%pamo!;` dans la colonne [!UICONTROL Landing page] pour la balise de clic.

## Déploiement de [!DNL Analytics for Advertising] macros dans DSP

Dans DSP, lorsque vous créez une publicité qui comprend le paramètre [!DNL Analytics for Advertising] (`amo`), les macros `ef_id` et `s_kwcid` sont automatiquement ajoutées à l’URL de clic. La bonne pratique consiste à vérifier la balise dans DSP pour s’assurer que les macros `ef_id` et `s_kwcid` sont présentes.

Voici un exemple d’une balise [!DNL Google Campaign Manager 360] [ins](https://support.google.com/campaignmanager/answer/6080468) telle qu’elle apparaît dans DSP.

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

Lorsqu&#39;un utilisateur clique sur la publicité, [!DNL Google Campaign Manager 360] voit `%pamo` dans le suffixe d&#39;URL et insère dynamiquement la valeur du paramètre `amo` dans l&#39;URL.

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Ajouter [!DNL Analytics for Advertising] Macros à [!DNL Flashtalking] Balises publicitaires](macros-flashtalking.md)
