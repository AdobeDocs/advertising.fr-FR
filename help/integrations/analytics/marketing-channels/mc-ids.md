---
title: Utilisation d'identifiants d'Adobe Advertising pour créer des  [!DNL Marketing Channels] règles
description: Découvrez comment utiliser les ID d’Adobe Advertising pour créer des règles de traitement pour [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Utilisation d’identifiants d’Adobe Advertising pour créer des règles de traitement [!DNL Marketing Channels]

*Annonceurs avec une intégration Adobe Advertising-Adobe Analytics uniquement*

Vous pouvez utiliser des ID d’Adobe Advertising ([AMO ID et EF ID](../ids.md)) pour configurer des règles de traitement [!DNL Marketing Channels] dans Adobe Analytics. Utilisez des identifiants d’Adobe Advertising pour les règles spécifiques à vos campagnes d’Adobe Advertising.

## AMO ID dans les règles de traitement

L’AMO ID est le code de suivi principal utilisé pour signaler les données d’Adobe Advertising dans [!DNL Analytics]. L’AMO ID est une concaténation de valeurs dynamiques gérées par Adobe pour fournir des rapports granulaires dans [!DNL Analytics]. Il est stocké dans une dimension [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=fr) ou rVar (AMO ID). L’AMO ID peut être défini dans [!DNL Analytics] de deux façons :

* Suivi des clics publicitaires : Adobe Advertising définit le paramètre de chaîne de requête `s_kwcid` dans un lien et [!DNL Analytics] sélectionne le paramètre à partir de l’URL de la page d’entrée lorsqu’un clic publicitaire se produit.
* Suivi des affichages publicitaires ([!DNL DSP] uniquement) : le service Last Event détecte un affichage publicitaire côté serveur et envoie l’AMO ID à [!DNL Analytics]. Dans ce cas, l’URL ne contient pas de paramètre `s_kwcid`.

Les valeurs dynamiques des AMO ID indiquent le canal marketing suivi :

* Le préfixe de l’AMO ID peut être utilisé pour identifier le canal de niveau supérieur dans [!DNL Marketing Channels].

* Les expressions de caractères dans le corps de l’AMO ID indiquent un type de campagne plus spécifique.

* Le suffixe &quot;vt&quot; est présent pour le trafic d’affichage publicitaire [!DNL DSP] et peut être utilisé pour créer des canaux de clics publicitaires et d’affichages publicitaires distincts [!DNL DSP].

Le reste de l’AMO ID peut être ignoré.

| [!UICONTROL AMO ID] | Canal | Logique de règle |
|--------|---------|--------------------|
| !ctv (suffixe) | [!UICONTROL DSP Connected TV View-through] | Se termine par |
| !d ! (body) | [!UICONTROL Display Network] | Contient |
| !g ! (body) | [!UICONTROL Google Search] | Contient |
| !s ! (body) | [!UICONTROL Search Partner] | Contient |
| !u ! (body) | [!UICONTROL Smart Shopping Campaign] | Contient |
| !ytv ! (body) | [!UICONTROL YouTube Video Ad] | Contient |
| !yts ! (body) | [!UICONTROL YouTube Search Ad] | Contient |
| !vp ! (body) | [!UICONTROL Google Video Partners] | Contient |
| !vt (suffixe) | [!UICONTROL DSP View-through] | Se termine par |
| AL ! (préfixe) | [!UICONTROL Paid Search] | Commence par |
| AC ! (préfixe) | [!UICONTROL DSP] | Commence par |

### Exemples de règles de traitement qui utilisent l’AMO ID

La règle de traitement [!DNL Marketing Channels] pour le canal [!UICONTROL Paid Search] peut se présenter comme suit :

![Exemple de [!UICONTROL Paid Search] règle](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

La règle de traitement [!DNL Marketing Channels] pour le canal [!UICONTROL YouTube Video Ads] peut se présenter comme suit :

![Exemple de [!UICONTROL YouTube Video Ads] règle](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Veillez à exécuter vos règles par ordre de précision. Si les deux règles ci-dessus s’exécutaient dans l’ordre, le trafic des publicités vidéo [!DNL YouTube] tomberait tous sous le canal [!UICONTROL Paid Search] car l’AMO ID commencerait tous les deux par &quot;AL!&quot;. et contiennent &quot;!ytv!&quot;.

## Identifiant EF dans les règles de traitement

L’AMO EF ID (EF ID) est le deuxième code de suivi utilisé dans l’intégration [!DNL Analytics for Advertising]. Son principal objectif est de suivre et de transmettre des données d’événement [!DNL Analytics] dans Adobe Advertising. Chaque fois qu’un clic publicitaire ou un affichage publicitaire se produit, un identifiant EF unique est généré, même s’il s’agit exactement de la même publicité pour le même visiteur. L’identifiant EF n’est pas utilisé dans l’interface utilisateur de création de rapports [!DNL Analytics], car il dépasse généralement les 500 000 valeurs uniques par limite de variable dans [!DNL Analytics], ce qui le rend inutilisable pour la création de rapports. Les mesures et métadonnées d’Adobe Advertising ne sont pas appliquées à l’identifiant EF ; elles le sont uniquement à l’AMO ID. La granularité supplémentaire du suivi est requise pour l’optimisation des campagnes dans Adobe Advertising. Les deux identifiants sont donc requis.

Bien que la dimension Identifiant EF ne soit pas utilisée directement dans les rapports [!DNL Analytics], l’identifiant EF peut s’avérer utile pour créer des canaux marketing. Le suffixe d’identifiant EF indique le canal (affichage ou recherche) et si la visite a été pilotée par un clic publicitaire ou un affichage publicitaire. Le délimiteur dans l’identifiant EF est un deux-points, plutôt que le point d’exclamation dans l’AMO ID.

| Suffixe d’identifiant EF | Canal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Exemples de règles de traitement qui utilisent l’identifiant EF

#### Afficher la règle de clic publicitaire

Créez un canal de marketing des clics publicitaires en capturant uniquement les clics publicitaires. Comme l’AMO ID est le même pour les clics publicitaires et les affichages publicitaires, cette règle utilise la variable EF ID et le paramètre de chaîne de requête `ef_id`.

Il arrive que les clics publicitaires fassent l’objet d’un suivi via l’URL (valeur par défaut). Dans d’autres cas, les clics publicitaires sont suivis par le biais du service Last Event côté serveur, et par conséquent l’URL ne contient pas le paramètre `ef_id` . La règle recherche donc les conditions dans lesquelles la variable EF ID ou le paramètre de chaîne de requête `ef_id` se termine par &quot;:d&quot;. Utilisez l’opérateur &quot;`Any`&quot; car vous souhaitez que cette règle soit déclenchée pour l’une ou l’autre des conditions.

![Exemple de règle de clic publicitaire display](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Règle d’affichage publicitaire

Pour créer un canal d’affichage publicitaire, créez une règle dans laquelle l’identifiant EF se termine par &quot;:i&quot;. Comme le visiteur n’a pas cliqué sur la publicité, le suivi des affichages publicitaires n’inclut pas les `ef_id` ou `s_kwcid` dans l’URL. Par conséquent, la règle ne nécessite qu’une seule condition.

![Exemple de règle d&#39;affichage publicitaire](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Principes fondamentaux de [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [ Pourquoi les données de canal peuvent varier entre l’Adobe Advertising et  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Utilisation de  [!DNL Analytics Marketing Channels]  avec des données d’Adobe Advertising](mc-ac-data.md)
>* [Vidéo : Utilisation de [!DNL Marketing Channels] pour la création de rapports d’Adobe Advertising](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=fr)
>* [ID d’Adobe Advertising utilisés par [!DNL Analytics]](/help/integrations/analytics/ids.md)
