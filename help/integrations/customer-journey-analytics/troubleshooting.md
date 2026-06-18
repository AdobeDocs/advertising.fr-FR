---
title: Dépannage des données Adobe Advertising dans Customer Journey Analytics
description: Découvrez comment résoudre les problèmes liés aux données Adobe Advertising dans Customer Journey Analytics.
feature: Integration with Adobe Customer Journey Analytics
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 33382b092be521df814a81aad3c7ae661d853174
workflow-type: tm+mt
source-wordcount: 620
ht-degree: 0%

---

# Dépannage des données Adobe Advertising dans Customer Journey Analytics

Vous trouverez ci-dessous des problèmes de données potentiels et leurs causes.

## Rapports de synthèse

+++ Aucune donnée de rapport de synthèse n’est disponible dans Customer Journey Analytics pour Advertising DSP ou Advertising Search, Social et Commerce.

Vérifiez les points suivants :

* Le flux d’Adobe Advertising vers Customer Journey Analytics est activé. Vérifiez auprès de l’équipe chargée de votre compte Adobe.

* Votre jeu de données de dimension/classification/recherche Adobe Advertising et votre jeu de données de résumé sont inclus dans votre connexion Customer Journey Analytics.

* Vos dimensions Adobe Advertising et mesures récapitulatives sont incluses dans votre vue de données Customer Journey Analytics.

* Customer Journey Analytics Workspace référence la vue de données appropriée.

Si vous vérifiez tous les paramètres ci-dessus mais que vous ne voyez toujours pas de données récapitulatives, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support).

+++

+++ Les données de rapports récapitulatives sont disponibles dans Customer Journey Analytics pour l’annonceur 1, mais pas pour l’annonceur 2.

Vérifiez que le flux d’Adobe Advertising vers Customer Journey Analytics est activé pour l’annonceur 2. Vérifiez auprès de l’équipe chargée de votre compte Adobe.

Si le flux est activé pour un annonceur, mais que vous ne voyez toujours pas de données récapitulatives, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support).

+++

+++ (Utilisateurs Search, Social et Commerce) Les données de rapports de synthèse sont disponibles dans Customer Journey Analytics pour un compte [!DNL Google Ads], [!DNL Meta Ads] ou [!DNL Microsoft Advertising], mais pas pour un autre compte.

Vérifiez que le flux d’Adobe Advertising vers Customer Journey Analytics est activé pour le compte réseau publicitaire spécifique. Vérifiez auprès de l’équipe chargée de votre compte Adobe.

Si le flux est activé pour un compte, mais que vous ne voyez toujours pas de données récapitulatives, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support). Incluez le [!UICONTROL Account ID] du compte réseau publicitaire.
.

+++

+++ Les données de rapports de synthèse dans Customer Journey Analytics Workspace sont différentes de celles d’Advertising DSP ou d’Advertising Search, Social et Commerce, ou les données de synthèse sont manquantes pour certaines campagnes et entités de campagne.

Vérifiez les points suivants :

* Vous utilisez les mêmes périodes dans les rapports [!DNL Workspace] et Adobe Advertising.

* Les filtres et les segments appliqués dans [!DNL Workspace] et le rapport Adobe Advertising ne provoquent pas de différences dans les données.

Si vous êtes sûr d’une incohérence des données, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support). Incluez le [!UICONTROL Account ID] du compte réseau publicitaire.
. Insérez des captures d’écran et des feuilles de calcul pour montrer les preuves de l’incohérence. Votre équipe de compte Adobe peut corriger rétroactivement le flux de données pour résoudre l’incohérence, si nécessaire.

+++

## Reporting au niveau des événements

+++ Les données de conversion (telles que `Page Views`) ne sont pas disponibles pour une dimension de rapport (telle que `Campaign`) dans CJA Customer Journey Analytics Workspace.

Vérifiez les points suivants, en commençant par les éléments qui présentent le moins d’obstacles à la vérification :

* Les mesures de conversion applicables sont les événements web/en ligne qu’Adobe Advertising peut attribuer aux dimensions.

* Vous utilisez la vue de données correcte.

* Adobe Advertising effectue le suivi des clics publicitaires et des affichages publicitaires sur le site approprié. <!-- Link to validation instructions in the user guide -->

* Dans la connexion Customer Journey Analytics du jeu de données de classifications, les valeurs des paramètres [!DNL Key] et [!DNL Matching Key] sont correctes : [!DNL Key] : `Tracking Code` (_customername.adLens2.trackingCode), [!DNL Matching Key] : `Tracking Code` (event._experience.adcloud.conversionDetails.trackingCode)

* Le service [!DNL Adobe Advertising] est ajouté au flux de données Adobe Experience Platform, le schéma mappé du flux de données est `XDM ExperienceEvent Schema` et le groupe de champs `Adobe Advertising Cloud ExperienceEvent Full Extension` est ajouté au schéma.

* Les paramètres Adobe Advertising sont correctement configurés dans l’extension WebSDK et publiés.

Si vous vérifiez tous les paramètres ci-dessus mais que vous ne voyez toujours pas les données de conversion, ouvrez un ticket d’assistance pour votre organisation à l’adresse [&#128279;](https://experienceleague.adobe.com/home?support-tab=home#support). Incluez le [!UICONTROL Account ID] du compte réseau publicitaire.

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [Aperçu](overview.md)
>* [Adobe Advertising ID utilisés par  [!DNL Customer Journey Analytics]](ids.md)
>* [Conditions préalables](prerequisites.md)
>* [Configurer la collecte, le transfert et la création de rapports de données](set-up.md)
>* [Mesures et dimensions Adobe Advertising dans Customer Journey Analytics](advertising-data-in-cja.md)
>* (Utilisateurs Adobe Analytics) [Collectez des données historiques pour les ID AMO et les ID EF à utiliser dans Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
