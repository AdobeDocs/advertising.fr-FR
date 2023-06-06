---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# Champ Type de suivi dans les paramètres du compte et de l’opération

**[!UICONTROL Tracking Type]:** Méthode de génération des URL :

* *[!UICONTROL EF Redirect]* (valeur par défaut) : Pour les clients qui souhaitent utiliser le service de suivi de conversion Adobe Advertising. Cette méthode génère des identifiants de suivi des clics uniques et redirige les utilisateurs vers le serveur Adobe Advertising à des fins de suivi avant de les envoyer à la page d’entrée du client.

   Cette méthode propose des options de suivi par défaut que vous pouvez éventuellement personnaliser et vous pouvez également spécifier des paramètres à ajouter à chaque URL.

* *[!UICONTROL No EF Redirect]:* Pour les clients qui souhaitent utiliser uniquement leurs propres codes de suivi des clics. Search, Social et Commerce ne fournit pas d’ID de suivi des clics ni de codes de redirection. Pour les comptes comportant des URL de destination, chaque URL de destination est identique à l’URL de base.

   **Remarques :**

   * Seul le gestionnaire de compte d’agence, le gestionnaire de compte d’Adobe et les utilisateurs administrateurs peuvent modifier cette valeur.
   * Si vous modifiez la méthode de suivi, vous devez régénérer les URL de suivi pour le compte.
   * Les options de suivi au niveau de la campagne remplacent les paramètres au niveau du compte.
