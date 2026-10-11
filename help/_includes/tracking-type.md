---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%
---
# Champ Type de tracking dans les paramètres du compte et de la campagne

**[!UICONTROL Tracking Type]:** Méthode de génération des URL :

* *[!UICONTROL EF Redirect]* (valeur par défaut) : pour les clients qui souhaitent utiliser le service de suivi des conversions Adobe Advertising. Cette méthode génère des identifiants de suivi des clics uniques et redirige les utilisateurs vers le serveur Adobe Advertising à des fins de suivi avant de les envoyer à la page de destination du client.

  Cette méthode comporte des options de tracking par défaut que vous pouvez éventuellement personnaliser. Vous pouvez également spécifier des paramètres à ajouter à chaque URL.

* *[!UICONTROL No EF Redirect]:* pour les clients qui souhaitent utiliser uniquement leurs propres codes de suivi des clics. Search, Social et Commerce ne fournissent pas d’ID de suivi des clics ni de codes de redirection. Pour les comptes avec des URL de destination, chaque URL de destination est identique à l’URL de base.

  **Remarques :**

  * Seuls le gestionnaire de compte d’agence, le gestionnaire de compte Adobe et les utilisateurs administrateurs peuvent modifier cette valeur.
  * Si vous modifiez la méthode de tracking, vous devez régénérer les URL de tracking pour le compte.
  * Les options de tracking au niveau de la campagne remplacent les paramètres au niveau du compte.
