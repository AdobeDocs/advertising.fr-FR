---
title: Conditions préalables à la configuration d’une source de données  [!DNL Google Analytics]
description: Découvrez les étapes à suivre avant de configurer une source de données  [!DNL Google Analytics] .
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# Conditions préalables à la configuration d’une source de données [!DNL Google Analytics]

Avant de pouvoir configurer une source de données [!DNL Google Analytics], vous devez définir le paramètre de chaîne de requête Search, Social, &amp; Commerce &quot;ef_id&quot; comme clé primaire pour transmettre les données de [!DNL Google Analytics] à Search, Social et Commerce. Configurez la clé primaire de chaque combinaison de compte et de propriété [!DNL Google Analytics] pour laquelle vous souhaitez synchroniser les données. D’autres personnes de votre entreprise peuvent avoir besoin d’effectuer ces tâches ; voir ci-dessous pour plus d’informations.

Si les URL de page d’entrée de vos publicités ou mots-clés n’incluent pas déjà les redirections Search, Social et Commerce, ajoutez-les d’abord.

## Condition préalable 1 : implémentation d’un jeton de requête Search, Social, &amp; Commerce (&quot;ef_id&quot;) dans les URL de page d’entrée pour tous les comptes publicitaires applicables

À chaque clic de recherche payante pour les campagnes appropriées, un `ef_id` unique doit être généré et ajouté à l’URL de la page d’entrée en tant que chaîne de requête, telle que `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, où `&ef_id=abcde:123456789:s` est le symbole d’ajout, la clé `ef_id` et la valeur `ef_id`. Pour inclure un ef_id, les comptes et campagnes réseau publicitaires pertinents doivent avoir le [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; et le [!UICONTROL Redirect Type] &quot;[!UICONTROL Token]&quot;.

Pour les comptes et campagnes existants, ef_id est probablement déjà mis en oeuvre.

Si ef_id n’est pas inclus, demandez de l’aide à votre équipe de compte d’Adobe.

Lorsque toutes les conditions préalables sont remplies, `ef_id` est utilisé comme clé primaire pour transmettre les données de [!DNL Google Analytics] à Search, Social et Commerce.

## Condition préalable 2 : capture du jeton de requête Search, Social, &amp; Commerce (&quot;ef_id&quot;) dans une dimension personnalisée pour chaque propriété [!DNL Google Analytics] appropriée.

Répétez les tâches suivantes pour chaque combinaison de compte et de propriété [!DNL Google Analytics] pour laquelle vous souhaitez synchroniser les données. Consultez la [[!DNL Google Analytics] documentation sur la création et l’implémentation de dimensions personnalisées](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) pour obtenir de l’aide sur ces tâches.

1. Dans [!DNL Google Analytics], créez une dimension personnalisée nommée &quot;`ef_id`&quot;. Définissez la portée de la dimension sur [!DNL User] et la dimension sur active.

   >[!NOTE]
   >
   >Cette condition préalable nécessite une autorisation de modification pour les propriétés appropriées.

1. Mettez à jour votre code de suivi [!DNL Google Analytics] pour capturer la valeur du paramètre de chaîne de requête ef_id lorsqu’il est présent dans l’URL de la page d’entrée et le stocker dans la dimension personnalisée ef_id.

   >[!NOTE]
   >
   >ef_id ne doit se trouver que dans les URL de page d’entrée.

   Par exemple, si l’URL de la page d’entrée est `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, la valeur de la dimension ef_id dans [!DNL Google Analytics] est `abcde:123456789:s`.

   >[!NOTE]
   >
   >Ce prérequis doit être rempli par un développeur qualifié.

>[!MORELIKETHIS]
>
>* [ À propos de la synchronisation  [!DNL Google Analytics] mesures de conversion](data-source-about.md)
>* [ Configuration d’une  [!DNL Google Analytics] vue en tant que source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier une [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe - Disponible [!DNL Google Analytics] metrics](data-source-ga-metrics.md)
