---
title: Ajout  [!DNL Analytics for Advertising]  macros aux balises  [!DNL Google Campaign Manager 360] ’annonces
description: Découvrez pourquoi et comment ajouter  [!DNL Analytics for Advertising]  macros à vos balises  [!DNL Google Campaign Manager 360]  publicité
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 0b95d99a1370a047642f8d1e4bbafe35ad5187f6
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Ajout de macros [!DNL Analytics for Advertising] aux balises d’annonces [!DNL Google Campaign Manager 360]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable à Advertising DSP uniquement*

Si vous utilisez les balises d’annonce publicitaire de [!DNL Google Campaign Manager 360] pour vos annonces Advertising DSP, ajoutez [!DNL Analytics for Advertising] paramètres à vos URL de page de destination à l’aide de la macro [`%p`](https://support.google.com/campaignmanager/table/6096962). Les paramètres enregistrent l’ID AMO (`s_kwcid`) et `ef_id` les paramètres de chaîne de requête dans l’URL de la page de destination, ce qui permet à Adobe Advertising d’envoyer des données de clic pour les publicités à Adobe Analytics.

Utilisez des macros pour [!DNL Campaign Manager 360] les publicités vidéo et d’affichage pour les types d’implémentation [!DNL Analytics for Advertising] suivants :

* **Annonceurs avec le code [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript implémenté sur leurs sites web** : le code JavaScript enregistre déjà les paramètres AMO ID (`s_kwcid`) et `ef_id` chaîne de requête. Toutefois, l’utilisation de macros étend le suivi pour inclure les conversions basées sur les clics lorsque les cookies tiers ne sont pas pris en charge. Il est recommandé d’ajouter les macros des sections suivantes à vos balises d’annonces afin de capturer des données de clic publicitaire supplémentaires qui ne sont pas capturées par le code JavaScript.

>[!NOTE]
>
>Le code JavaScript est une solution permettant le suivi des clics uniquement tant que des cookies sont disponibles. Une fois les cookies arrêtés, la mise en œuvre des macros suivantes sera nécessaire.

* **Annonceurs dont les sites web n’utilisent pas le code JavaScript [!DNL Analytics for Advertising] et comptent plutôt sur [!DNL Analytics] transfert côté serveur pour les données de clic publicitaire uniquement** (sans données de vue publicitaire) : les macros suivantes sont nécessaires pour signaler l’activité de clic sur site pilotée par les publicités que vous achetez via Adobe Advertising.

## Ajouter les macros à vos publicités [!DNL Google Campaign Manager 360]

Dans [!DNL Google Campaign Manager 360], ajoutez au paramètre suivant à l’URL de la page de destination pour chacune de vos publicités vidéo et d’affichage : `%pamo=!;`

Vous pouvez spécifier l’URL de la page de destination de plusieurs façons. Les instructions relatives à chaque option sont incluses dans les sous-sections suivantes.

Voici un exemple d&#39;URL de page de destination formatée avec le suffixe .

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* Si l’URL de la page de destination comprend un symbole de hachage (#), ce qui n’est pas courant, placez le paramètre `amo` avant le symbole de hachage.
>* Si aucun autre paramètre n’est inclus après le paramètre `amo`, ajoutez un paramètre (par exemple, &amp;a=b) après celui-ci. Exemple : `https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configurer le suffixe d’URL de page de destination au niveau de l’annonceur

1. Voir les [instructions pour ouvrir les propriétés de l’annonceur](https://support.google.com/campaignmanager/answer/2829344).
1. Dans les paramètres de [!UICONTROL Landing page URL suffix], incluez `%pamo!;` dans le champ [!UICONTROL URL suffix] .

### Configurer le suffixe d’URL de la page de destination au niveau de la campagne

1. Voir les [instructions pour ouvrir les propriétés de la campagne](https://support.google.com/campaignmanager/answer/2838056#set).
1. Dans les paramètres de [!UICONTROL Landing page URL suffix], incluez `%pamo!;` dans le champ [!UICONTROL URL suffix] .

### Configurer le suffixe d’URL de page de destination de niveau créatif

1. Ouvrez les propriétés de création.
1. Dans le paramètre [!UICONTROL Click tags] , incluez les `%pamo!;` dans la colonne [!UICONTROL Landing page] de la balise de clic.

## Développement [!DNL Analytics for Advertising] macros dans DSP

Dans DSP, lorsque vous créez une publicité qui inclut le paramètre [!DNL Analytics for Advertising] (`amo`), les macros `ef_id` et `s_kwcid` sont automatiquement ajoutées à l’URL de clic. La bonne pratique consiste à vérifier la balise dans DSP pour s’assurer que les macros `ef_id` et `s_kwcid` sont présentes.

Voici un exemple de balise [!DNL Google Campaign Manager 360] [ins](https://support.google.com/campaignmanager/answer/6080468) telle qu’elle apparaît dans DSP.

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

Lorsqu’un utilisateur clique sur la publicité, [!DNL Google Campaign Manager 360] voit `%pamo` dans le suffixe de l’URL et insère dynamiquement la valeur du paramètre de `amo` dans l’URL.

>[!MORELIKETHIS]
>
>* [Présentation de  [!DNL Analytics for Advertising]](overview.md)
>* [Adobe Advertising ID utilisés par  [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad Tags](macros-flashtalking.md)
