---
title: Conditions préalables à la configuration d’un [!DNL Google Analytics] source de données
description: Découvrez les étapes à suivre avant de configurer une [!DNL Google Analytics] source de données.
role: User, Admin
exl-id: cbb2ad6d-8494-4fa4-928c-238b25bda3a6
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Conditions préalables à la configuration d’un [!DNL Google Analytics] source de données

Avant de pouvoir configurer une [!DNL Google Analytics] source de données, vous devez définir le paramètre de chaîne de requête Search, Social, &amp; Commerce &quot;ef_id&quot; comme clé Principale à partir de laquelle transmettre les données. [!DNL Google Analytics] vers Search, Social et Commerce. Configurez la clé Principale pour chaque [!DNL Google Analytics] combinaison de comptes et de propriétés pour laquelle vous souhaitez synchroniser les données. D’autres personnes de votre entreprise peuvent avoir besoin d’effectuer ces tâches ; voir ci-dessous pour plus d’informations.

Si les URL de page d’entrée de vos publicités ou mots-clés n’incluent pas déjà les redirections Search, Social et Commerce, ajoutez-les d’abord.

## Condition préalable 1 : implémentation d’un jeton de chaîne de requête Search, Social, &amp; Commerce (&quot;ef_id&quot;) dans les URL de page d’entrée pour tous les comptes publicitaires applicables

Sur chaque clic de recherche payante pour les campagnes pertinentes, une `ef_id` doit être générée et ajoutée à l’URL de la page d’entrée en tant que chaîne de requête, telle que `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`, où `&ef_id=abcde:123456789:s` est le symbole d’ajout, `ef_id` clé et `ef_id` . Pour inclure un ef_id, les comptes et campagnes réseau publicitaires pertinents doivent avoir la variable [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot; et la variable [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

Pour les comptes et campagnes existants, ef_id est probablement déjà mis en oeuvre.

Si ef_id n’est pas inclus, demandez de l’aide à votre équipe de compte d’Adobe.

Lorsque toutes les conditions préalables sont remplies, la variable `ef_id` est utilisé comme clé Principale pour transmettre des données à partir de [!DNL Google Analytics] vers Search, Social et Commerce.

## Condition préalable 2 : capture du jeton de chaîne de requête Search, Social, &amp; Commerce (&quot;ef_id&quot;) dans une dimension personnalisée pour chaque dimension appropriée [!DNL Google Analytics] property

Répétez les tâches suivantes pour chaque [!DNL Google Analytics] combinaison de comptes et de propriétés pour laquelle vous souhaitez synchroniser les données. Voir [[!DNL Google Analytics] documentation sur la création et l’implémentation de dimensions personnalisées](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) pour obtenir de l’aide sur ces tâches.

1. Dans [!DNL Google Analytics], créez une dimension personnalisée nommée &quot;`ef_id`&quot;. Définissez la portée de la dimension sur [!DNL User]et définissez la dimension sur principale.

   >[!NOTE]
   >
   >Cette condition préalable nécessite une autorisation de modification pour les propriétés appropriées.

1. Mettez à jour votre [!DNL Google Analytics] code de suivi permettant de capturer la valeur du paramètre de chaîne de requête ef_id lorsqu’il est présent dans l’URL de la page d’entrée et de le stocker dans la dimension personnalisée ef_id.

   >[!NOTE]
   >
   >ef_id ne doit se trouver que dans les URL de page d’entrée.

   Par exemple, si l’URL de la landing page est `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`, puis la valeur de la dimension ef_id dans [!DNL Google Analytics] is `abcde:123456789:s`.

   >[!NOTE]
   >
   >Ce prérequis doit être rempli par un développeur qualifié.

>[!MORELIKETHIS]
>
>* [A propos de la synchronisation [!DNL Google Analytics] mesures de conversion](data-source-about.md)
>* [Configurez une [!DNL Google Analytics] vue comme source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspension de la synchronisation d’une source de données](data-source-pause.md)
>* [Réauthentifier un [!DNL Google Analytics] source de données](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe : Disponible [!DNL Google Analytics] mesures](data-source-ga-metrics.md)
