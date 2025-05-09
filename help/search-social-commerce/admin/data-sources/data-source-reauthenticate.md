---
title: Réauthentifier une source  [!DNL Google Analytics]  données
description: Découvrez comment réauthentifier une source  [!DNL Google Analytics]  données si vous modifiez le mot de passe associé ou si le certificat expire.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Réauthentifier une source de données [!DNL Google Analytics]

*Administrateurs d’agence, Gestionnaires de compte d’agence, Gestionnaires de compte Adobe et Administrateurs uniquement*

Si vous modifiez le mot de passe du compte de messagerie utilisé pour une source de données ou si le certificat [!DNL OAuth] du compte expire, toutes les connexions ouvertes au compte de messagerie sont fermées et vous devez vous réauthentifier pour reprendre la synchronisation des données.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Cochez la case en regard de la source de données que vous souhaitez réauthentifier.

1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez les [paramètres de la source de données](data-source-settings.md) :

   1. Dans la section [!UICONTROL Connect to Google Analytics], procédez comme suit.

      1. (Si nécessaire) Saisissez une nouvelle adresse e-mail à utiliser pour accéder aux données de cette source de données. L’adresse e-mail doit être enregistrée sur un compte [!DNL Google] et disposer des autorisations « Lecture et analyse » pour le compte [!DNL Google Analytics]. Reportez-vous aux [instructions pour l’attribution des autorisations utilisateur dans [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Pour vous assurer que seules des propriétés et des vues de [!DNL Google Analytics] spécifiques sont disponibles dans Search, Social et Commerce, connectez-vous à l’aide d’une adresse e-mail qui n’a accès qu’à ces propriétés et vues.

   1. Cochez la case pour autoriser Search, Social et Commerce à accéder aux mesures du compte.

   1. Cliquez sur **[!UICONTROL Re-Authenticate]**.

1. Cliquez sur **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [À propos de la synchronisation [!DNL Google Analytics] des mesures de conversion](data-source-about.md)
>* [Conditions préalables à la configuration d’une source  [!DNL Google Analytics]  données](data-source-prerequisites.md)
>* [Configurer une [!DNL Google Analytics] vue comme source de données](data-source-configure.md)
>* [Modifier une source  [!DNL Google Analytics]  données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [[!DNL Google Analytics] paramètres des sources de données](data-source-settings.md)
>* [Annexe - Mesures  [!DNL Google Analytics]  disponibles](data-source-ga-metrics.md)
