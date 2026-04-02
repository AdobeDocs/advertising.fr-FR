---
title: Conditions préalables à la configuration d’une source  [!DNL Google Analytics]  données
description: Découvrez les étapes à suivre avant de configurer une source  [!DNL Google Analytics]  données.
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/viBRqiwqJm2BabtLP7b3h1TMTjkeITeSVA1vMMmbrPY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2: id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 0%

---

# Conditions préalables à la configuration d’une source de données [!DNL Google Analytics]

Avant de pouvoir configurer une source de données [!DNL Google Analytics], vous devez établir le paramètre de chaîne de requête Search, Social et Commerce « ef_id » comme clé primaire pour transmettre des données de [!DNL Google Analytics] à Search, Social et Commerce. Configurez la clé primaire pour chaque combinaison de compte et de propriété [!DNL Google Analytics] pour laquelle vous souhaitez synchroniser les données. D’autres personnes de votre entreprise peuvent avoir besoin d’effectuer ces tâches ; voir ci-dessous pour plus d’informations.

Si les URL de page de destination de vos publicités ou mots-clés n’incluent pas déjà des redirections Search, Social et Commerce, ajoutez-les d’abord.

## Condition préalable 1 : implémentez un jeton Search, Social et Commerce (paramètre de chaîne de requête « ef_id ») dans les URL de page de destination pour tous les comptes publicitaires applicables

Lors de chaque clic de référencement payant pour les campagnes appropriées, un `ef_id` unique doit être généré et ajouté à l’URL de la page de destination sous la forme d’une chaîne de requête, telle que `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, où `&ef_id=abcde:123456789:s` correspond au symbole d’ajout, à la clé de `ef_id` et à la valeur de `ef_id`. Pour inclure un ef_id, les comptes et campagnes de réseau publicitaire pertinents doivent avoir le [!UICONTROL Tracking Type] « [!UICONTROL EF Redirect] » et le [!UICONTROL Redirect Type] « [!UICONTROL Token] ».

Pour les comptes et campagnes existants, l’ef_id est probablement déjà implémenté.

Si l’ef_id n’est pas inclus, demandez de l’aide à l’équipe de votre compte Adobe.

Une fois toutes les conditions préalables remplies, la `ef_id` est utilisée comme clé primaire pour transmettre des données de [!DNL Google Analytics] à Search, Social et Commerce.

## Condition préalable 2 : capturez le jeton Search, Social et Commerce (paramètre de chaîne de requête « ef_id ») dans une dimension personnalisée pour chaque propriété [!DNL Google Analytics] appropriée.

Répétez les tâches suivantes pour chaque combinaison de compte et de propriété [!DNL Google Analytics] pour laquelle vous souhaitez synchroniser les données. Pour obtenir de l’aide sur ces tâches[[!DNL Google Analytics]  consultez la ](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) documentation sur la création et l’implémentation de dimensions personnalisées .

1. Dans [!DNL Google Analytics], créez une dimension personnalisée nommée « `ef_id` ». Définissez l’étendue de la dimension sur [!DNL User], puis définissez la dimension sur active.

   >[!NOTE]
   >
   >Cette condition préalable nécessite des autorisations de modification pour les propriétés appropriées.

1. Mettez à jour votre code de suivi [!DNL Google Analytics] pour capturer la valeur du paramètre de chaîne de requête ef_id lorsqu’il est présent dans l’URL de la page de destination et stockez-le dans la dimension personnalisée ef_id.

   >[!NOTE]
   >
   >L’ef_id ne doit se trouver que dans les URL de page de destination.

   Par exemple, si l’URL de la page de destination est `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, la valeur de la dimension ef_id dans [!DNL Google Analytics] est `abcde:123456789:s`.

   >[!NOTE]
   >
   >Cette condition préalable doit être remplie par un développeur qualifié.

>[!MORELIKETHIS]
>
>* [À propos de la synchronisation [!DNL Google Analytics] des mesures de conversion](data-source-about.md)
>* [Configurer une [!DNL Google Analytics] vue comme source de données](data-source-configure.md)
>* [Modifier une source  [!DNL Google Analytics]  données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une source  [!DNL Google Analytics]  données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres des sources de données](data-source-settings.md)
>* [Annexe - Mesures  [!DNL Google Analytics]  disponibles](data-source-ga-metrics.md)
