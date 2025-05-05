---
title: Création d’une audience de correspondance de client  [!DNL Google Ads] à partir d’une liste de messagerie Adobe Campaign
description: Découvrez comment créer une audience de correspondance de clients  [!DNL Google Ads] à partir d’une liste de messagerie Adobe Campaign existante.
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---

# Création d’une audience de correspondance de client [!DNL Google Ads] à partir d’une liste de messagerie Adobe Campaign

*[!DNL Google Ads]comptes éligibles pour la correspondance client uniquement*

Vous pouvez créer une audience de correspondance de client [!DNL Google Ads] à partir d’une liste de messagerie dans Adobe Campaign en configurant un lien de compte et un workflow dans [!DNL Campaign].

Pour ce faire, vous devez accéder à votre instance [!DNL Campaign] et à un fichier XML contenant le workflow requis que votre équipe de compte d’Adobe vous donnera. Les instructions peuvent varier pour différentes versions de [!DNL Campaign]. Si nécessaire, votre équipe de compte d’Adobe peut vous aider à configurer le workflow dans [!DNL Campaign].

1. Obtenez les informations d’identification d’un compte SFTP fourni par Advertising Search, Social et Commerce.

1. Dans [!DNL Campaign], configurez la diffusion de la liste de messagerie vers Advertising Search, Social et Commerce :

   1. Créez un [compte externe](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html?lang=fr) pour lier votre compte SFTP fourni par Search, Social et Commerce :

      1. Dans le menu de gauche, accédez à **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Cliquez sur ![Créer un compte](/help/search-social-commerce/assets/campaign-create-account.png "Créer un compte").

      1. Saisissez le libellé du compte et sélectionnez **[!UICONTROL SFTP]** comme type de compte.

      1. Saisissez l’URL et le numéro de port du serveur SFTP [!DNL Adobe], ainsi que le nom de dossier, le nom d’utilisateur et le mot de passe de l’annonceur.

      1. Cliquez sur **[!UICONTROL Save]**.

   1. Dans [!DNL Campaign Client], installez le package de données qui inclut le workflow requis pour envoyer les données d&#39;email :

      1. Dans la barre de menus, accédez à **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Sélectionnez **[!UICONTROL Install a package from a file]**, puis cliquez sur **[!UICONTROL Next]**.

      1. Recherchez le fichier de package de données (`AMO_Workflow.xml`) sur l’appareil ou le réseau, puis cliquez sur **[!UICONTROL Next]**.

      1. Cliquez sur **[!UICONTROL Start]** et attendez que le workflow soit installé.

   1. Editez le workflow installé pour éditer éventuellement les filtres pour la requête de données et identifier le nouveau nom d&#39;audience et le compte SFTP externe :

      1. Accédez à **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** et ouvrez le package.

      1. (Facultatif) Modifiez l’un des filtres pour les données :

         * Dans le workflow, double-cliquez sur l’activité de requête (telle que ForkTransition 1).

         * Editez les expressions de filtre.

         * Cliquez sur **[!UICONTROL Finish]**.

      1. Nommez le segment :

         * Dans le workflow, double-cliquez sur l’activité **[!UICONTROL Data extraction (File)]**.

         * Sur l’onglet **[!UICONTROL Data extraction (File)]**, dans le champ **[!UICONTROL File name]**, saisissez le nom du segment avec l’extension &quot;`.added`&quot; (comme PaidSubscribers.added).

           Le nom du segment ne doit pas déjà exister. Le nom du segment est sensible à la casse et doit contenir des caractères ASCII, mais ne peut pas inclure de traits de soulignement (`_`).

           Cependant, si vous souhaitez ajouter le segment à un compte [!DNL Google Ad] spécifique, ajoutez le nom du segment avec un trait de soulignement et l’ [!UICONTROL User SE Account ID] (identifiant de recherche, de Social et de Commerce pour le compte [!DNL Google Ads], et non l’identifiant de compte du réseau) :

           `_<User SE Account ID>`

           Exemple : Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >Il s’agit d’une exception à la règle qui interdit les traits de soulignement dans le nom de fichier.

           Sinon, le segment est ajouté à tous les comptes [!DNL Google Ads] synchronisés par Search, Social et Commerce pour l’annonceur.

         * Laissez l’option sélectionnée sur **[!UICONTROL Generate an outbound transition]**.

         * Cliquez sur **[!UICONTROL Ok]**.

      1. Indiquez le compte externe auquel envoyer les données :

         * Dans le workflow, double-cliquez sur l’activité **[!UICONTROL File Transfer]**.

         * Sur l’onglet **[!UICONTROL File Transfer]**, dans la section **[!UICONTROL Remote server]**, sélectionnez l’option **[!UICONTROL Use an external account]**.

         * Dans le champ **[!UICONTROL External account]** , sélectionnez le libellé du compte externe que vous avez créé à l’étape 2.

         * Dans le champ **[!UICONTROL Server folder]** , sélectionnez la valeur du champ [!UICONTROL Account] pour le compte externe.

         * (Facultatif) Dans l’onglet **[!UICONTROL Schedule]**, spécifiez un autre planning pour le transfert de fichier.

           Par défaut, le workflow est exécuté à 00:00 (minuit), ce qui garantit le traitement de tous les enregistrements. Pour minimiser la latence, planifiez l’exécution du workflow au plus tard à 18h00.

         * Cliquez sur **[!UICONTROL Ok]**.

Search, Social et Commerce vérifie le répertoire toutes les 30 minutes (à NN:30 et NN:59 dans le fuseau horaire de l’annonceur), déplace les fichiers qu’il trouve vers un autre emplacement, puis crée automatiquement une audience à partir des données et la transmet à Google à 22h00 (22h00). Search, Social et Commerce continue à rechercher les mises à jour (ajouts et soustractions) de la liste des emails toutes les 30 minutes et met à jour l’audience sur [!DNL Google Ads] en conséquence à 22 h 00 tous les jours.

>[!NOTE]
>
>* Si vous chargez plusieurs versions d’un fichier entre les cycles de traitement, le fichier le plus récent est utilisé.
>
>* Search, Social et Commerce ne stocke aucune des données client de vos listes de messagerie utilisées pour créer ou modifier une audience [!DNL Google Ads].
>
>* [!DNL Google Ads] peut prendre un certain temps pour traiter les mises à jour d’une audience.
>
>* Consultez la [[!DNL Google Ads] documentation sur le fonctionnement et les limites de la correspondance client](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Créer [!DNL Google Ads]  des audiences de correspondance client à partir des  [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [Gérer les audiences de correspondance de client à l’aide des listes de données de client](audience-from-customer-data-list.md)
>* [Gérer les audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
