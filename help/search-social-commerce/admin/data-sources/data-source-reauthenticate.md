---
title: Réauthentification d’une source de données  [!DNL Google Analytics]
description: Découvrez comment réauthentifier une source de données  [!DNL Google Analytics]  si vous modifiez le mot de passe associé ou si le certificat expire.
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# Réauthentification d’une source de données [!DNL Google Analytics]

*Administrateurs de l’agence, Responsables de compte de l’agence, Responsables de compte d’Adobe et Administrateurs uniquement*

Si vous modifiez le mot de passe du compte de messagerie utilisé pour une source de données ou si le certificat [!DNL OAuth] du compte expire, toutes les connexions ouvertes au compte de messagerie sont fermées et vous devez vous authentifier à nouveau pour reprendre la synchronisation des données.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Cochez la case en regard de la source de données que vous souhaitez réauthentifier.

1. Dans la barre d&#39;outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez les [paramètres de source de données](data-source-settings.md) :

   1. Dans la section [!UICONTROL Connect to Google Analytics], procédez comme suit.

      1. (Si nécessaire) Entrez une nouvelle adresse électronique à utiliser pour accéder aux données de cette source de données. L’adresse électronique doit être enregistrée sur un compte [!DNL Google] et disposer des autorisations de &quot;lecture et analyse&quot; pour le compte [!DNL Google Analytics]. Reportez-vous aux [instructions pour l’attribution des autorisations utilisateur dans [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Pour vous assurer que seules des propriétés et des vues [!DNL Google Analytics] spécifiques sont disponibles dans Search, Social et Commerce, connectez-vous à l’aide d’une adresse électronique qui n’a accès qu’à ces propriétés et vues.

   1. Cochez la case pour autoriser Search, Social et Commerce à accéder aux mesures du compte.

   1. Cliquez sur **[!UICONTROL Re-Authenticate]**.

1. Cliquez sur **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [ À propos de la synchronisation  [!DNL Google Analytics] mesures de conversion](data-source-about.md)
>* [ Conditions préalables à la configuration d’une  [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [ Configuration d’une  [!DNL Google Analytics] vue en tant que source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspendre la synchronisation d’une source de données](data-source-pause.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe - Disponible [!DNL Google Analytics] metrics](data-source-ga-metrics.md)
