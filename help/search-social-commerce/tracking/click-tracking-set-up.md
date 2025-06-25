---
title: Configuration du suivi des clics basé sur les cookies
description: Découvrez comment configurer et valider les balises de suivi des clics.
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# Configuration du suivi des clics basé sur les cookies

Pour que le suivi des clics puisse être effectué sur Search, Social et Commerce, les éléments suivants doivent être configurés et validés.

1. (Équipe du compte Adobe) Configurez l’annonceur en tant que client pixel.

1. [Spécifiez les options de suivi correctes pour chacun des comptes et des campagnes du réseau publicitaire de l’annonceur](#set-up-click-tracking-options).

1. Le cas échéant, [générez des URL de tracking et chargez-les](#generate-upload-tracking-urls) pour certains éléments de la campagne.

1. [Validez le format de certaines des URL de suivi des clics et testez-les pour vérifier que la page de destination correcte s’ouvre](#validate-tracking-urls).

## Configurer des options de tracking pour les comptes et campagnes de réseau publicitaire {#set-up-click-tracking-options}

*Rôles de gestionnaire de compte d’agence, de gestionnaire de compte [!DNL Adobe] et d’utilisateur administrateur uniquement*

1. Pour chaque compte de réseau publicitaire, procédez comme suit :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. Placez le curseur sur le nom du compte, cliquez sur ![icône de menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "icône de menu"), puis sélectionnez **[!UICONTROL Edit]**.

   1. Cliquez sur **[!UICONTROL Set Account Tracking]**.

   1. Pour le paramètre [!UICONTROL Tracking Type], sélectionnez **[!UICONTROL EF Redirect]**.

   1. (Pour permettre à Search, Social et Commerce d’échanger des données avec Adobe Analytics ou de suivre les conversions qui se produisent dans [!DNL Apple Safari]) Sélectionnez l’option [!UICONTROL Redirect Type] **[!UICONTROL Token]**.

   1. (Facultatif) Activez l’option **[!UICONTROL Auto Upload]** pour charger automatiquement les nouvelles URL de tracking dans le réseau publicitaire la prochaine fois que Search, Social et Commerce s’y synchronisera. Cette valeur est héritée comme valeur par défaut pour toutes les campagnes du compte, mais peut être remplacée au niveau de la campagne.

1. Pour chaque campagne, procédez comme suit :

   1. Dans le menu principal, cliquez sur **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. Dans les sous-menus, cliquez sur **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. Placez le curseur sur le nom de la campagne, cliquez sur ![icône de menu](/help/search-social-commerce/assets/arrow-dropdown-menu.png "icône de menu"), puis sélectionnez **[!UICONTROL Edit]**.

   1. Cliquez sur **[!UICONTROL Set Campaign Tracking]**. Sélectionnez ensuite l’option à **[!UICONTROL Override Account Tracking]**.

   1. Pour le paramètre [!UICONTROL Tracking Type], sélectionnez **[!UICONTROL EF Redirect]**.

   1. (Pour permettre à Search, Social et Commerce d’échanger des données avec Adobe Analytics ou de suivre les conversions qui se produisent dans [!DNL Apple Safari]) Sélectionnez l’option [!UICONTROL Redirect Type] **[!UICONTROL Token]**.

   1. (Facultatif) Activez l’option **[!UICONTROL Auto Upload]** pour charger automatiquement les nouvelles URL de tracking dans le réseau publicitaire la prochaine fois que Search, Social et Commerce s’y synchronisera. Cette valeur est héritée comme valeur par défaut pour toutes les campagnes du compte, mais peut être remplacée au niveau de la campagne.

## Générer et charger les URL de tracking {#generate-upload-tracking-urls}

Voir « [ Quand et comment générer des URL de suivi des clics ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) ».

### Tester le format des URL de suivi des clics {#validate-tracking-urls}

Vérifiez que la page de destination appropriée s’ouvre pour l’URL de suivi des clics.

1. Reproduisez un clic publicitaire en envoyant du trafic à l’environnement d’évaluation de l’annonceur :

   1. Dans un éditeur de texte, collez une URL de suivi des clics, modifiez l’URL de la page de destination afin qu’elle pointe vers la même page dans l’environnement d’évaluation de l’annonceur, puis collez la nouvelle URL dans la barre d’adresse de votre navigateur et appuyez sur la touche **[!DNL Enter]**.

   1. Recherchez le cookie dans les cookies stockés par votre navigateur.

   1. Effectuez une transaction sur le site d’évaluation et vérifiez que la page de succès déclenche le pixel correct. Les paramètres réels suivis par le pixel varient selon l’annonceur et l’URL de suivi. Dans l’exemple suivant, l’annonceur souhaite suivre le nombre de nouvelles demandes et le montant des nouveaux revenus :

      Pour un nouvel utilisateur final (avec un nouveau cookie), le pixel suivant doit être déclenché :

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Si le cookie n’est pas frais, le pixel suivant doit être déclenché :

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. Répétez l’opération pour plusieurs URL de suivi des clics dans le domaine.

1. Répétez l’étape 1 pour chaque domaine, en utilisant une page de destination différente en conséquence.

1. Si nécessaire, vérifiez que Search, Social et Commerce peuvent afficher les pixels pour les ID de transaction (`ev_transid`) générés lors du test.

>[!MORELIKETHIS]
>
>* [Quand et comment générer des URL de suivi des clics ](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
