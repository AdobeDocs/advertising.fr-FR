---
source-git-commit: d1e2e92532b1f930420436c66c687676a2b7de6a
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---
# Identifiants d’éléments d’expérience Adobe Advertising

L’ID d’EF est un jeton unique utilisé par Adobe Advertising pour associer l’activité à une exposition de publicité ou de clic en ligne au niveau du navigateur ou de l’appareil concerné. Les identifiants EF servent principalement de clés pour envoyer des données [!DNL Analytics] et des données Customer Journey Analytics à Adobe Advertising à des fins de création de rapports et d’optimisation des enchères dans Adobe Advertising.

Par [!DNL Analytics], l’identifiant de l’EF est stocké dans [une dimension  [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) ou [!DNL rVar] ([!DNL eVar] réservé) (identifiant de l’EF Adobe Advertising).

Pour Customer Journey Analytics, l’ID d’élément d’enregistrement est stocké dans la propriété `trackingIdentities` de l’objet `conversionDetails`, qui fait partie du [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] .
