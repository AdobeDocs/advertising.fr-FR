---
title: Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Google Campaign Manager 360] Balises publicitaires
description: Découvrez pourquoi et comment ajouter [!DNL Analytics for Advertising] des macros à vos [!DNL Google Campaign Manager 360] balises publicitaires
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: 703cda43e96dfa9d80bbce2d64192fc461d5dbae
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Google Campaign Manager 360] Balises publicitaires

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

*Applicable aux DSP Advertising uniquement*

Si vous utilisez des balises de publicité de [!DNL Google Campaign Manager 360] pour vos publicités Advertising DSP, ajoutez [!DNL Analytics for Advertising] des paramètres des URL de votre landing page à l’aide de la variable [`%p` macro](https://support.google.com/campaignmanager/table/6096962). Les paramètres enregistrent l’AMO ID (`s_kwcid`) et `ef_id` paramètres de chaîne de requête dans l’URL de la page d’entrée, ce qui permet à l’Adobe Advertising d’envoyer des données de clic pour les publicités à Adobe Analytics.

Utilisez des macros pour [!DNL Campaign Manager 360] publicités display et vidéo pour les types suivants de [!DNL Analytics for Advertising] Implémentations :

* **Les annonceurs qui utilisent la variable [!DNL Adobe] [!DNL Analytics for Advertising] Code JavaScript implémenté sur leurs sites web**: le code JavaScript enregistre déjà l’AMO ID (`s_kwcid`) et `ef_id` paramètres de chaîne de requête. Cependant, l’utilisation de macros étend le suivi pour inclure les conversions basées sur les clics lorsque les cookies tiers ne sont pas pris en charge. Il est recommandé d’ajouter les macros des sections suivantes à vos balises publicitaires afin de capturer des données de clics publicitaires supplémentaires qui ne sont pas capturées par le biais du code JavaScript.

>[!NOTE]
>
>Le code JavaScript est une solution pour le suivi des clics uniquement lorsque des cookies sont toujours disponibles. Une fois les cookies arrêtés, la mise en oeuvre des macros suivantes est nécessaire.

* **Annonceurs dont les sites web n’utilisent pas la variable [!DNL Analytics for Advertising] Code JavaScript et s’appuient sur [!DNL Analytics] transfert côté serveur pour les données de clic publicitaire uniquement** (sans aucune donnée d’affichage publicitaire) : les macros suivantes sont requises pour signaler les activités de clics sur site effectuées à partir de publicités achetées via Adobe Advertising.

## Ajout de macros à la fonction [!DNL Google Campaign Manager 360] Publicités

Within [!DNL Google Campaign Manager 360], ajoutez le paramètre suivant à l’URL de la page d’entrée pour chacune de vos publicités vidéo et display : `%pamo=!;`

Vous pouvez spécifier l&#39;URL de la landing page de plusieurs manières. Les instructions pour chaque option sont incluses dans les sous-sections suivantes.

Voici un exemple d’URL de page d’entrée formatée avec le suffixe .

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* Si l’URL de la page d’entrée contient un symbole de hachage (#), qui n’est pas courant, placez la variable `amo` avant le symbole de hachage.
>* Si aucun autre paramètre n’est inclus après l’événement `amo` , puis ajoutez un paramètre (par exemple, &amp;a=b) après. Exemple :`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### Configuration du suffixe d’URL de page d’entrée au niveau des annonceurs

1. Voir [instructions pour ouvrir les propriétés de l’annonceur](https://support.google.com/campaignmanager/answer/2829344).
1. Dans le [!UICONTROL Landing page URL suffix] paramètres, inclure `%pamo!;` dans le [!UICONTROL URL suffix] champ .

### Configuration du suffixe d’URL de page d’entrée de niveau Campaign

1. Voir [instructions pour ouvrir les propriétés de la campagne](https://support.google.com/campaignmanager/answer/2838056#set).
1. Dans le [!UICONTROL Landing page URL suffix] paramètres, inclure `%pamo!;` dans le [!UICONTROL URL suffix] champ .

### Configuration du suffixe d’URL de page d’entrée Creative

1. Ouvrez les propriétés de création.
1. Dans le [!UICONTROL Click tags] paramètre, inclure `%pamo!;` dans le [!UICONTROL Landing page] pour la balise de clic.

## Comment [!DNL Analytics for Advertising] Les macros sont développées en DSP

Dans DSP, lorsque vous créez une publicité qui comprend la variable [!DNL Analytics for Advertising] paramètre (`amo`), la variable `ef_id` et `s_kwcid` les macros sont automatiquement ajoutées à l’URL de clic. La bonne pratique consiste à vérifier la balise dans DSP pour vous assurer que la variable `ef_id` et `s_kwcid` des macros sont présentes.

Voici un exemple d’une [!DNL Google Campaign Manager 360] [balise ins](https://support.google.com/campaignmanager/answer/6080468) comme il apparaît dans DSP.

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

Lorsqu’un utilisateur clique sur la publicité, [!DNL Google Campaign Manager 360] see `%pamo` dans le suffixe d’URL et insère dynamiquement la valeur de la variable `amo` dans l’URL.

>[!MORELIKETHIS]
>
>* [Présentation de [!DNL Analytics for Advertising]](overview.md)
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Ajouter [!DNL Analytics for Advertising] Macros vers [!DNL Flashtalking] Balises publicitaires](macros-flashtalking.md)
