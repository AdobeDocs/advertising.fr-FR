---
title: Création d’une audience  [!DNL Google Ads]  correspondance client à partir d’une liste d’emails Adobe Campaign
description: Découvrez comment créer une audience  [!DNL Google Ads]  correspondance client à partir d’une liste d’emails Adobe Campaign existante.
exl-id: 92812af2-ac31-48cd-badf-ea287799bddb
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/tEiqvHt1QzxhstsKGUsvKGgwm1JYIkv7mGr-Z8kPd0g
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 0%

---

# Création d’une audience de correspondance de clients [!DNL Google Ads] à partir d’une liste d’emails Adobe Campaign

*[!DNL Google Ads]les comptes éligibles à la correspondance client uniquement*

Vous pouvez créer une audience de correspondance de clients [!DNL Google Ads] à partir d’une liste d’e-mails dans Adobe Campaign en configurant un lien de compte et un workflow dans [!DNL Campaign].

Pour ce faire, vous devez accéder à votre instance [!DNL Campaign] et à un fichier XML contenant le workflow requis, qui vous sera fourni par l’équipe chargée de votre compte Adobe. Les instructions peuvent varier en fonction des différentes versions d’[!DNL Campaign]. Si nécessaire, l’équipe chargée de votre compte Adobe peut vous aider à configurer le workflow dans [!DNL Campaign].

1. Obtenez les informations d’identification d’un compte SFTP fourni par Advertising Search, Social et Commerce.

1. Dans [!DNL Campaign], configurez la diffusion de la liste d’e-mails vers Advertising Search, Social et Commerce :

   1. Créez un [compte externe](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/external-accounts.html) pour lier votre compte SFTP fourni par Search, Social et Commerce :

      1. Dans le menu de gauche, accédez à **\[Adobe Campaign v6\] > [!UICONTROL Platform] >[!UICONTROL External Accounts]**.

      1. Cliquez sur ![ Créer un compte ](/help/search-social-commerce/assets/campaign-create-account.png " Créer un compte ").

      1. Saisissez un libellé pour le compte et sélectionnez **[!UICONTROL SFTP]** comme type de compte.

      1. Saisissez l’URL et le numéro de port du serveur SFTP [!DNL Adobe], ainsi que le nom de dossier, le nom d’utilisateur et le mot de passe de l’annonceur.

      1. Cliquez sur **[!UICONTROL Save]**.

   1. Dans [!DNL Campaign Client], installez le package de données qui comprend le workflow requis pour envoyer les données d’e-mail :

      1. Dans la barre de menus, accédez à **[!UICONTROL Tools]> [!UICONTROL Advanced] >[!UICONTROL Import Package]**.

      1. Sélectionnez **[!UICONTROL Install a package from a file]**, puis cliquez sur **[!UICONTROL Next]**.

      1. Recherchez le fichier de package de données (`AMO_Workflow.xml`) sur l’appareil ou le réseau, puis cliquez sur **[!UICONTROL Next]**.

      1. Cliquez sur **[!UICONTROL Start]** et attendez que le workflow soit installé.

   1. Modifiez le workflow installé afin de modifier éventuellement les filtres de la requête de données et d’identifier le nouveau nom d’audience et le compte SFTP externe :

      1. Accédez à **[!UICONTROL Administration]> [!UICONTROL Configuration] > [!UICONTROL Package management] >[!UICONTROL Installed packages]** et ouvrez le package.

      1. (Facultatif) Modifiez l’un des filtres pour les données :

         * Dans le workflow, double-cliquez sur l’activité de requête (par exemple ForkTransition 1).

         * Modifiez les expressions de filtre.

         * Cliquez sur **[!UICONTROL Finish]**.

      1. Nommez le segment : .

         * Dans le workflow, double-cliquez sur le **[!UICONTROL Data extraction (File)]** de l’activité.

         * Sur l’onglet **[!UICONTROL Data extraction (File)]** , dans le champ **[!UICONTROL File name]** , saisissez le nom du segment avec l’extension « `.added` » (tel que PaidSubscribers.added).

           Le nom du segment ne doit pas déjà exister. Le nom du segment est sensible à la casse et doit comporter des caractères ASCII, mais ne peut pas inclure de traits de soulignement (`_`).

           Cependant, si vous souhaitez ajouter le segment à un compte [!DNL Google Ad] spécifique, ajoutez le nom du segment avec un trait de soulignement et le [!UICONTROL User SE Account ID] (identifiant de recherche, de réseaux sociaux et de Commerce pour le compte [!DNL Google Ads], et non l’identifiant du compte réseau) :

           `_<User SE Account ID>`

           Exemple : Paid_Subscribers_1234.added

           >[!NOTE]
           >
           >Il s’agit d’une exception à la règle qui interdit les traits de soulignement dans le nom du fichier.

           Sinon, le segment est ajouté à tous les comptes [!DNL Google Ads] que Search, Social et Commerce synchronisent pour l’annonceur.

         * Laissez l’option **[!UICONTROL Generate an outbound transition]** sélectionnée.

         * Cliquez sur **[!UICONTROL Ok]**.

      1. Indiquez le compte externe vers lequel envoyer les données :

         * Dans le workflow, double-cliquez sur le **[!UICONTROL File Transfer]** de l’activité.

         * Sur l’onglet **[!UICONTROL File Transfer]** , dans la section **[!UICONTROL Remote server]** , sélectionnez l’option à **[!UICONTROL Use an external account]**.

         * Dans le champ **[!UICONTROL External account]** , sélectionnez le libellé du compte externe que vous avez créé à l’étape 2.

         * Dans le champ **[!UICONTROL Server folder]** , sélectionnez la valeur du champ [!UICONTROL Account] pour le compte externe.

         * (Facultatif) Dans l’onglet **[!UICONTROL Schedule]** , spécifiez un planning différent pour le transfert du fichier.

           Par défaut, le workflow est exécuté à 00 :00 (minuit), ce qui garantit le traitement de tous les enregistrements. Pour minimiser la latence, planifiez l’exécution du workflow au plus tard à 18 :00.

         * Cliquez sur **[!UICONTROL Ok]**.

Search, Social et Commerce vérifie le répertoire toutes les 30 minutes (aux fuseaux horaires NN:30 et NN:59 de l’annonceur) et déplace tous les fichiers qu’il trouve vers un autre emplacement, puis crée automatiquement une audience à partir des données et la transmet à Google à 22 :00 (22 heures). Search, Social et Commerce continuent de rechercher des mises à jour (ajouts et soustractions) dans la liste d’e-mails toutes les 30 minutes et mettent à jour l’audience sur [!DNL Google Ads] en conséquence à 22 :00 par jour.

>[!NOTE]
>
>* Si vous chargez plusieurs versions d’un fichier entre des cycles de traitement, le fichier le plus récent est utilisé.
>
>* Search, Social et Commerce ne stockent aucune des données client de vos listes d’adresses e-mail utilisées pour créer ou modifier une audience [!DNL Google Ads].
>
>* [!DNL Google Ads] peut prendre un certain temps pour traiter les mises à jour d’une audience.
>
>* Consultez la [[!DNL Google Ads] documentation sur le fonctionnement et les limites de la correspondance client](https://support.google.com/displayvideo/answer/9539301).

>[!MORELIKETHIS]
>
>* [À propos des audiences](audience-about.md)
>* [Créer [!DNL Google Ads] des audiences de correspondance client à partir  [!DNL Adobe]  audiences](google-audience-from-adobe-audience.md)
>* [Gérer les audiences de correspondance de clients à l’aide de listes de données client](audience-from-customer-data-list.md)
>* [Gestion des audiences de remarketing dynamique](audience-dynamic-remarketing-manage.md)
