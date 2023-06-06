---
title: Configuration du suivi des clics basé sur les cookies
description: Découvrez comment configurer et valider les balises de suivi des clics.
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# Configuration du suivi des clics basé sur les cookies

Pour que Search, Social et Commerce effectuent le suivi des clics, les éléments suivants doivent être configurés et validés.

1. (Équipe du compte d’Adobe) Configurez l’annonceur comme client de pixel.

1. [Définissez les options de suivi correctes pour chacun des comptes et campagnes de réseau publicitaire de l’annonceur.](#set-up-click-tracking-options).

1. Si nécessaire, [générer des URL de suivi et les télécharger ;](#generate-upload-tracking-urls) pour certains éléments de campagne.

1. [Validez le format de quelques URL de suivi des clics et testez-les pour vérifier que la page d’entrée correcte s’ouvre.](#validate-tracking-urls).

## Configuration des options de suivi pour les comptes de réseau publicitaire et les campagnes {#set-up-click-tracking-options}

*Responsable de compte de l&#39;Agence, [!DNL Adobe] rôles utilisateur de gestionnaire de compte et d’administrateur uniquement*

1. Pour chaque compte réseau publicitaire, procédez comme suit :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Placez le curseur sur le nom du compte, puis cliquez sur ![Icône Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icône Menu"), puis sélectionnez **[!UICONTROL Edit]**.

   1. Cliquez sur **[!UICONTROL Set Account Tracking]**.

   1. Pour le [!UICONTROL Tracking Type] paramètre, sélectionnez **[!UICONTROL EF Redirect]**.

   1. (Pour permettre à Search, Social et Commerce d’échanger des données avec Adobe Analytics ou de suivre les conversions qui se produisent dans [!DNL Apple Safari]) Sélectionnez la variable [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. (Facultatif) Activez la variable **[!UICONTROL Auto Upload]** pour charger automatiquement les nouvelles URL de suivi vers le réseau publicitaire lors de la prochaine synchronisation de Search, Social et Commerce avec celui-ci. Cette valeur est héritée comme valeur par défaut pour toutes les campagnes du compte, mais elle peut être remplacée au niveau de la campagne.

1. Pour chaque campagne, procédez comme suit :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Placez le curseur sur le nom de la campagne, puis cliquez sur ![Icône Menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "Icône Menu"), puis sélectionnez **[!UICONTROL Edit]**.

   1. Cliquez sur **[!UICONTROL Set Campaign Tracking]**. Sélectionnez ensuite l’option pour **[!UICONTROL Override Account Tracking]**.

   1. Pour le [!UICONTROL Tracking Type] paramètre, sélectionnez **[!UICONTROL EF Redirect]**.

   1. (Pour permettre à Search, Social et Commerce d’échanger des données avec Adobe Analytics ou de suivre les conversions qui se produisent dans [!DNL Apple Safari]) Sélectionnez la variable [!UICONTROL Redirect Type] option **[!UICONTROL Token]**.

   1. (Facultatif) Activez la variable **[!UICONTROL Auto Upload]** pour charger automatiquement les nouvelles URL de suivi vers le réseau publicitaire lors de la prochaine synchronisation de Search, Social et Commerce avec celui-ci. Cette valeur est héritée comme valeur par défaut pour toutes les campagnes du compte, mais elle peut être remplacée au niveau de la campagne.

## Génération et chargement des URL de suivi {#generate-upload-tracking-urls}

Voir &quot;[Quand et comment générer des URL de suivi des clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

### Test du format des URL de suivi des clics {#validate-tracking-urls}

Vérifiez que la page d’entrée correcte s’ouvre pour l’URL de suivi des clics.

1. Reproduisez un clic publicitaire en envoyant du trafic vers l’environnement d’évaluation de l’annonceur :

   1. Dans un éditeur de texte, collez une URL de suivi des clics, modifiez l’URL de la page d’entrée pour qu’elle pointe vers la même page dans l’environnement d’évaluation de l’annonceur, puis collez la nouvelle URL dans la barre d’adresse de votre navigateur et appuyez sur la touche **[!DNL Enter]** clé.

   1. Recherchez le cookie dans les cookies stockés de votre navigateur.

   1. Effectuez une transaction sur le site d’évaluation et vérifiez que la page de succès déclenche le bon pixel. Les paramètres réels suivis par le pixel varient en fonction de l’annonceur et de l’URL de suivi. Dans l&#39;exemple suivant, l&#39;annonceur souhaite effectuer le suivi du nombre de nouvelles applications et du montant des nouvelles recettes :

      Pour un nouvel utilisateur final (avec un nouveau cookie), le pixel suivant doit être déclenché :

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Si le cookie n’est pas nouveau, le pixel suivant doit être déclenché :

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Répétez cette procédure pour plusieurs URL de suivi des clics dans le domaine.

1. Répétez l’étape 1 pour chaque domaine en utilisant une page d’entrée différente en conséquence.

1. Si nécessaire, vérifiez que Search, Social et Commerce peut afficher les pixels des identifiants de transaction (`ev_transid`) générés pendant le test.

>[!MORELIKETHIS]
>
>* [Quand et comment générer des URL de suivi des clics](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)

