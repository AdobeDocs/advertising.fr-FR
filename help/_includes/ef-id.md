---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---
# Identifiants d’éléments d’expérience Adobe Advertising

## Identifiants d’éléments d’expérience Adobe Advertising

L’ID d’EF est un jeton unique utilisé par Adobe Advertising pour associer l’activité à une exposition de publicité ou de clic en ligne au niveau du navigateur ou de l’appareil concerné. Les identifiants EF servent principalement de clés pour envoyer des données [!DNL Analytics] et des données Customer Journey Analytics à Adobe Advertising à des fins de création de rapports et d’optimisation des enchères dans Adobe Advertising.

Par [!DNL Analytics], l’identifiant de l’EF est stocké dans [une dimension  [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] ([!DNL eVar] réservé) (identifiant de l’EF Adobe Advertising).

Pour Customer Journey Analytics, l’ID d’élément d’enregistrement est stocké dans la propriété `trackingIdentities` de l’objet `conversionDetails`, qui fait partie de [l’[!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension]](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension) .

### Formats des ID EF {#ef-id-formats}

Consultez la section [Formats des éléments de dimension ID d’EF](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-ef-id#dimension-items) dans le « Guide des composants d’Adobe Analytics ».

>[!NOTE]
>
>Les identifiants d’éléments d’expérience sont sensibles à la casse. Si une implémentation d’[!DNL Analytics] ou de Customer Journey Analytics force le suivi des URL à être écrit en minuscules, alors Adobe Advertising ne reconnaît pas l’ID d’EF. Cela a un impact sur les enchères et les rapports Adobe Advertising, mais n’a aucun impact sur les rapports Adobe Advertising dans [!DNL Analytics] ou Customer Journey Analytics.

<!-- Legacy content:

#### [!DNL Google Ads] search ads

```
{gclid}:G:s
```

where:

* `gclid` is the [!DNL Google Click ID] (GCLID).
* `s` is the network type ("s" for search).

#### [!DNL Microsoft Advertising] search ads

```
{msclkid}:G:s
```

where:

* `msclkid` is the [!DNL Microsoft Click ID] (MSCLKID).
* `s` is the network type ("s" for search).

#### Display ads and search ads on other search engines 

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

where:

* <*Adobe Advertising visitor ID*> is a unique ID per visitor (such as UhKVaAAABCkJ0mDt). Also called the *surfer ID*.

* <*timestamp*> is the time in the format YYYYMMDDHHMMSS (such as 20190821192533 for Year 2019, Month 08, Day 21, Time 19:25:33).

* <*channel type*> is the channel type responsible for the click or exposure:

    * `d` for a click on a DSP display ad (display click-through)
    * `i` for an impression of a DSP display ad (display view-through)
    * `s` for a click on a Search ad (search click-through).

Example `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

-->
