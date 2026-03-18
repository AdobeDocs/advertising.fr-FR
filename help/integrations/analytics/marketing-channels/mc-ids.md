---
title: Utilisation des Adobe Advertising ID pour créer  [!DNL Marketing Channels]  règles
description: Découvrez comment utiliser les Adobe Advertising ID pour créer des règles de traitement pour  [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0b95d99a1370a047642f8d1e4bbafe35ad5187f6
workflow-type: tm+mt
source-wordcount: '752'
ht-degree: 0%

---

# Utilisation des Adobe Advertising ID pour la création de règles de traitement des [!DNL Marketing Channels]

*Publicitaires avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Vous pouvez utiliser les identifiants Adobe Advertising ([AMO ID et EF ID](../ids.md)) pour configurer les règles de traitement des [!DNL Marketing Channels] dans Adobe Analytics. Utilisez les Adobe Advertising ID pour les règles spécifiques à vos campagnes Adobe Advertising.

## ID AMO dans les règles de traitement

L’ID AMO est le code de suivi principal utilisé pour signaler les données Adobe Advertising dans [!DNL Analytics]. L’ID AMO est une concaténation de valeurs dynamiques gérées par Adobe afin de fournir des rapports granulaires dans [!DNL Analytics]. Il est stocké dans une dimension [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=fr) ou rVar (AMO ID). L’AMO ID peut être défini dans [!DNL Analytics] de deux manières :

* Suivi des clics publicitaires : Adobe Advertising définit le paramètre de chaîne de requête `s_kwcid` dans un lien et [!DNL Analytics] sélectionne le paramètre dans l’URL de la page de destination en cas de clic publicitaire.
* Suivi des affichages publicitaires ([!DNL DSP] uniquement) : le service Last Event détecte un affichage publicitaire côté serveur et envoie l’AMO ID à [!DNL Analytics]. Dans ce cas, l’URL ne contient pas de paramètre `s_kwcid`.

Les valeurs dynamiques dans les ID AMO indiquent le canal marketing qui a été suivi :

* Le préfixe dans l’AMO ID peut être utilisé pour identifier le canal de niveau supérieur dans [!DNL Marketing Channels].

* Les expressions de caractères dans le corps de l’ID AMO indiquent un type de campagne plus spécifique.

* Le suffixe « vt » est présent pour [!DNL DSP] trafic d’affichage publicitaire et peut être utilisé pour créer des canaux d’[!DNL DSP] d’affichage publicitaire et d’affichage publicitaire distincts.

Le reste de l’AMO ID peut être ignoré.

| [!UICONTROL AMO ID] | Canal | Logique de règle |
|--------|---------|--------------------|
| !ctv (suffixe) | [!UICONTROL DSP Connected TV View-through] | Se Termine Par |
| !d ! (corps) | [!UICONTROL Display Network] | Contient |
| !g ! (corps) | [!UICONTROL Google Search] | Contient |
| !s ! (corps) | [!UICONTROL Search Partner] | Contient |
| !u ! (corps) | [!UICONTROL Smart Shopping Campaign] | Contient |
| !ytv ! (corps) | [!UICONTROL YouTube Video Ad] | Contient |
| !yts ! (corps) | [!UICONTROL YouTube Search Ad] | Contient |
| !vp ! (corps) | [!UICONTROL Google Video Partners] | Contient |
| !vt (suffixe) | [!UICONTROL DSP View-through] | Se Termine Par |
| AL ! (préfixe) | [!UICONTROL Paid Search] | Commence Par |
| AC ! (préfixe) | [!UICONTROL DSP] | Commence Par |

### Exemples de règles de traitement utilisant l’ID AMO

La règle de traitement des [!DNL Marketing Channels] pour le canal [!UICONTROL Paid Search] peut se présenter comme suit :

![Exemple de règle de [!UICONTROL Paid Search]](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

La règle de traitement des [!DNL Marketing Channels] pour le canal [!UICONTROL YouTube Video Ads] peut se présenter comme suit :

![Exemple de règle de [!UICONTROL YouTube Video Ads]](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Veillez à exécuter vos règles dans l’ordre de spécificité. Si les deux règles ci-dessus s’exécutaient dans l’ordre, le trafic publicitaire vidéo [!DNL YouTube] tomberait tous sous le canal [!UICONTROL Paid Search], car l’AMO ID commencerait tous deux par « AL ». et contiennent «!ytv! ».

## Identifiant de l’élément de formulaire dans les règles de traitement

L’ID EF AMO (ID EF) est le deuxième code de suivi utilisé dans l’intégration [!DNL Analytics for Advertising]. Son principal objectif est de suivre et de transmettre des données d’événement [!DNL Analytics] dans Adobe Advertising. Chaque fois qu’un clic publicitaire ou une affichage publicitaire se produit, un identifiant d’événement publicitaire unique est généré, même s’il s’agit exactement de la même publicité pour le même visiteur. L’ID EF n’est pas utilisé dans l’interface utilisateur de création de rapports [!DNL Analytics], car il dépasse généralement les 500 000 valeurs uniques par limite de variable dans [!DNL Analytics], ce qui le rend inutilisable pour la création de rapports. Les mesures et métadonnées d’Adobe Advertising ne s’appliquent pas à l’ID d’environnement de travail, mais uniquement à l’ID AMO. La granularité ajoutée du tracking est requise pour l’optimisation des campagnes dans Adobe Advertising. Les deux identifiants sont donc requis.

Bien que la dimension Identifiant de l’événement ne soit pas utilisée directement dans les rapports [!DNL Analytics], l’identifiant de l’événement peut s’avérer utile dans la création de canaux marketing. Le suffixe de l’ID de l’EF indique le canal (affichage ou recherche) et si la visite a été effectuée par un clic publicitaire ou une vue publicitaire. Le délimiteur de l’ID EF est un signe deux-points plutôt que le point d’exclamation de l’ID AMO.

| Suffixe de l’ID EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exemples de règles de traitement qui utilisent l’identifiant d’entité de traitement

#### Afficher la règle de clic publicitaire

Créez un canal marketing Afficher les clics publicitaires en capturant uniquement les clics publicitaires. Comme l’ID AMO est le même pour les clics publicitaires et les affichages publicitaires, cette règle utilise la variable EF ID et le paramètre de chaîne de requête `ef_id`.

Parfois, les clics publicitaires sont suivis via l’URL (valeur par défaut). Dans d’autres cas, les clics publicitaires sont suivis via le service Last Event du côté serveur. Par conséquent, l’URL ne contient pas le paramètre `ef_id`. La règle vérifie donc les conditions dans lesquelles la variable EF ID ou le paramètre de chaîne de requête `ef_id` se termine par « :d ». Utilisez l’opérateur « `Any` », car vous souhaitez que cette règle soit déclenchée pour l’une ou l’autre des conditions.

![Exemple de règle de clic publicitaire sur l’affichage](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Afficher la règle d&#39;affichage publicitaire

Pour créer un canal d&#39;affichage publicitaire, créez une règle dans laquelle l&#39;identifiant EF se termine par « :i ». Comme le visiteur n’a pas cliqué sur l’annonce publicitaire, le suivi des affichages publicitaires n’inclut pas le `ef_id` ou le `s_kwcid` dans l’URL. La règle ne nécessite donc qu’une seule condition.

![Exemple de règle d’affichage publicitaire](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Principes fondamentaux de  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Pourquoi les données de canal peuvent varier entre Adobe Advertising et  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilisation [!DNL Analytics Marketing Channels] avec des données Adobe Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation  [!DNL Marketing Channels]  rapports Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=fr)
>* [Adobe Advertising ID utilisés par  [!DNL Analytics]](/help/integrations/analytics/ids.md)
