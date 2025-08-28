---
source-git-commit: 47b5d399d4a5daa8832456abc32fff68e694abe9
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---
# Identifiants d’éléments d’expérience Adobe Advertising

## Identifiants d’éléments d’expérience Adobe Advertising

L’identifiant d’événement est un jeton unique utilisé par Adobe Advertising pour associer une activité à une exposition publicitaire ou à un clic en ligne. L’identifiant de l’annonce publicitaire est stocké dans [une dimension  [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=fr) ou [!DNL rVar] ([!DNL eVar] réservé) (identifiant de l’annonce publicitaire Adobe Advertising) et suit chaque clic publicitaire ou exposition publicitaire au niveau du navigateur ou de l’appareil concerné. Les identifiants EF servent principalement de clés pour envoyer des données [!DNL Analytics] à Adobe Advertising à des fins de création de rapports et d’optimisation des enchères dans Adobe Advertising.

### Formats d’ID EF {#ef-id-formats}

>[!NOTE]
>
>Les identifiants d’éléments d’expérience sont sensibles à la casse. Si une implémentation [!DNL Analytics] force le suivi des URL à passer en minuscules, alors Adobe Advertising ne reconnaît pas l’identifiant de l’EF. Cela a un impact sur les enchères et les rapports Adobe Advertising, mais n’a aucun impact sur les rapports Adobe Advertising dans [!DNL Analytics].

#### [!DNL Google Ads] des annonces de recherche

```
{gclid}:G:s
```

où :

* `gclid` est le [!DNL Google Click ID] (GCLID).
* `s` est le type de réseau (« s » pour la recherche).

#### [!DNL Microsoft Advertising] des annonces de recherche

```
{msclkid}:G:s
```

où :

* `msclkid` est le [!DNL Microsoft Click ID] (MSCLKID).
* `s` est le type de réseau (« s » pour la recherche).

#### Affichage des annonces et des annonces de recherche sur d’autres moteurs de recherche

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

où :

* &lt;*Identifiant visiteur Adobe Advertising*> est un identifiant unique par visiteur (par exemple, UhKVaAAABCkJ0mDt). Également appelé *surfer ID*.

* &lt;*timestamp*> correspond à l’heure au format AAAAMMJJHHMMSS (par exemple 20190821192533 pour l’année 2019, le mois 08, le jour 21, l’heure 19:25:33).

* &lt;*channel type*> est le type de canal responsable du clic ou de l’exposition :

   * `d` d’un clic sur une publicité display DSP (affichage clic publicitaire)
   * `i` d’impression d’une publicité display DSP (affichage publicitaire)
   * `s` un clic sur une publicité de recherche (clic publicitaire de recherche).

Exemple de `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
