---
title: Réauthentifier un [!DNL Google Analytics] source de données
description: Découvrez comment réauthentifier un [!DNL Google Analytics] source de données si vous modifiez le mot de passe associé ou si le certificat expire.
role: User, Admin
exl-id: 9233e004-8607-444a-ba99-f63cb83a8b7a
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# Réauthentifier un [!DNL Google Analytics] source de données

*Administrateurs de l’agence, responsables de compte de l’agence, gestionnaires de compte d’Adobe et administrateurs uniquement*

Si vous modifiez le mot de passe du compte de messagerie utilisé pour une source de données, ou si la variable [!DNL OAuth] le certificat du compte expire, puis toutes les connexions ouvertes au compte de messagerie sont fermées et vous devez vous authentifier à nouveau pour reprendre la synchronisation des données.

1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. Cochez la case en regard de la source de données que vous souhaitez réauthentifier.

1. Dans la barre d’outils située au-dessus du tableau de données, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit.png "Modifier").

1. Modifiez la variable [paramètres de source de données](data-source-settings.md):

   1. Dans le [!UICONTROL Connect to Google Analytics] , procédez comme suit.

      1. (Si nécessaire) Entrez une nouvelle adresse électronique à utiliser pour accéder aux données de cette source de données. L’adresse électronique doit être enregistrée auprès d’un [!DNL Google] et disposer des autorisations de &quot;lecture et analyse&quot; pour la variable [!DNL Google Analytics] compte . Voir [instructions pour attribuer des autorisations d’utilisateur dans [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >Pour vous assurer que uniquement [!DNL Google Analytics] Les propriétés et les vues sont disponibles dans Search, Social et Commerce. Connectez-vous à l’aide d’une adresse électronique qui a accès uniquement aux propriétés et aux vues.

   1. Cochez la case pour autoriser Search, Social et Commerce à accéder aux mesures du compte.

   1. Cliquez sur **[!UICONTROL Re-Authenticate]**.

1. Cliquez sur **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [A propos de la synchronisation [!DNL Google Analytics] mesures de conversion](data-source-about.md)
>* [Conditions préalables à la configuration d’un [!DNL Google Analytics] source de données](data-source-prerequisites.md)
>* [Configurez une [!DNL Google Analytics] vue comme source de données](data-source-configure.md)
>* [Modifier une [!DNL Google Analytics] source de données](data-source-edit.md)
>* [Suspension de la synchronisation d’une source de données](data-source-pause.md)
>* [[!DNL Google Analytics] paramètres de source de données](data-source-settings.md)
>* [Annexe : Disponible [!DNL Google Analytics] mesures](data-source-ga-metrics.md)
