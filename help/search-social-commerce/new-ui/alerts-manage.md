---
title: (Nouvelle interface utilisateur) Gérer les alertes personnalisées
description: Découvrez comment créer, configurer, mettre en pause, activer, supprimer, afficher et exporter des alertes et des modèles d’alerte personnalisés.
feature: Search Alerts
source-git-commit: 0fddeb8f01bd7c310544973ae2aff78339eb2144
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# (Nouvelle interface utilisateur) Gérer les alertes personnalisées

Créez des modèles d’alerte pour déterminer à quel moment un portfolio, une campagne ou un groupe publicitaire répond à des conditions spécifiques, telles qu’une mesure de performances, au cours d’une période spécifiée, puis générez une alerte. Des alertes sont disponibles pour un seul annonceur. Les alertes incluent toutes les colonnes dans la vue par défaut correspondante. Par exemple, les alertes au niveau de la campagne incluent toutes les colonnes de la vue [!UICONTROL Campaigns] par défaut.

Vous pouvez créer des modèles d’alerte à partir de l’onglet [!UICONTROL Alert Templates] du panneau [!UICONTROL Custom Alerts] ou du haut d’une page.

Lorsqu’une instance d’alerte est déclenchée pour un modèle d’alerte :

* Les destinataires spécifiés reçoivent un e-mail de notification. Lorsque l’alerte contient jusqu’à 1 000 enregistrements, l’e-mail de notification inclut un fichier [CSV](/help/search-social-commerce/glossary.md#c-d) avec les données de l’alerte, y compris les données de toutes les entités qui ont déclenché l’alerte.

* L’alerte est répertoriée dans l’onglet [!UICONTROL Triggered Alerts] du panneau [!UICONTROL Custom Alert Templates].<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## La vue [!UICONTROL Custom Alerts]

Pour ouvrir le panneau [!UICONTROL Custom Alerts], cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée") en haut à droite.

Le panneau [!UICONTROL Custom Alerts] comprend la vue [!UICONTROL Alert Templates], qui répertorie tous les modèles d’alerte créés pour le compte et à partir desquels vous pouvez créer, modifier, suspendre, réactiver et supprimer des modèles d’alerte. La vue [!UICONTROL Triggered Alerts] répertorie les instances d’alerte générées.

## Actions disponibles

* [Affichage des alertes déclenchées](#alert-view)

* [Affichage de modèles d’alerte personnalisés](#alert-template-view)

* [Création d’un modèle d’alerte personnalisé](#alert-template-create)

* [Modification d’un modèle d’alerte personnalisé](#alert-template-edit)

* [Mettre en pause un modèle d’alerte personnalisé](#alert-template-pause)

* [Activation d’un modèle d’alerte personnalisé](#alert-template-activate)

* [Suppression d’un modèle d’alerte personnalisé](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## Affichage des alertes déclenchées {#alert-view}

1. Dans l’angle supérieur droit d’une page, cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée").

1. Cliquez sur l’onglet **[!UICONTROL Triggered Alerts]** .

1. (Facultatif) Filtrez la liste pour inclure des alertes pour un type d’entité spécifique ou recherchez une chaîne de texte dans le nom du modèle. Les requêtes de recherche ne respectent pas la casse.

## Affichage de modèles d’alerte personnalisés {#alert-template-view}

1. Dans l’angle supérieur droit d’une page, cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée") pour ouvrir l’onglet [!UICONTROL Alert Templates] .

1. (Facultatif) Filtrez la liste pour inclure des alertes pour un type d’entité spécifique ou recherchez une chaîne de texte dans le nom du modèle. Les requêtes de recherche ne respectent pas la casse.

1. (Facultatif) Pour afficher tous les critères d’un modèle d’alerte, cliquez sur le nombre de critères (par exemple, ![Bouton Exemple de critères d’alerte personnalisés](/help/search-social-commerce/assets/custom-alert-criteria.png "Bouton Exemple de critères d’alerte personnalisés").

## Création d’un modèle d’alerte personnalisé {#alert-template-create}

Les nouveaux modèles d’alerte ont le statut « [!UICONTROL Active] ».

1. Effectuez l’une des opérations suivantes :

   * Dans l’angle supérieur droit d’une page, cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée") > **[!UICONTROL Create Custom Alert]**.

   Dans l’angle supérieur droit d’une page, cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée") > **[!UICONTROL View Custom Alerts]** pour ouvrir l’onglet [!UICONTROL Alert Templates] . Cliquez sur **[!UICONTROL Create Alert]**.

1. Spécifiez les [paramètres d’alerte](#alert-template-settings) sur les onglets **[!UICONTROL Entity]**, **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** et **[!UICONTROL Scheduling and Delivery]**.

   Vous pouvez passer d’un onglet à l’autre en cliquant sur son nom (par exemple, « Filtres ») ou en cliquant sur **[!UICONTROL Next]** en bas à droite.

1. Dans l’onglet [!UICONTROL Summary] , cliquez sur **[!UICONTROL Create Alert]**.

## Modification d’un modèle d’alerte personnalisé {#alert-template-edit}

1. Dans l’angle supérieur droit, cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée") > **[!UICONTROL View Custom Alerts]** pour ouvrir l’onglet [!UICONTROL Alert Templates] .

1. (Facultatif) Filtrez la liste pour inclure des alertes pour un type d’entité spécifique ou recherchez une chaîne de texte dans le nom du modèle. Les requêtes de recherche ne respectent pas la casse.

1. En regard du nom du modèle, cliquez sur ![Modifier](/help/search-social-commerce/assets/edit-new.png "Modifier").

1. Dans la fenêtre de [!UICONTROL Edit Custom Alert], modifiez les [paramètres d’alerte](#alert-template-settings) sur les onglets **[!UICONTROL Date Range]**, **[!UICONTROL Filters]** et **[!UICONTROL Scheduling and Delivery]**.

   Vous pouvez passer d’un onglet à l’autre en cliquant sur son nom (par exemple, « Filtres ») ou en cliquant sur **[!UICONTROL Next]** en bas à droite.

1. Dans l’onglet [!UICONTROL Summary] , cliquez sur **[!UICONTROL Update Alert]**.

## Mettre en pause un modèle d’alerte personnalisé {#alert-template-pause}

1. Dans l’angle supérieur droit, cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée") > **[!UICONTROL View Custom Alerts]** pour ouvrir l’onglet [!UICONTROL Alert Templates] .

1. (Facultatif) Filtrez la liste pour inclure des alertes pour un type d’entité spécifique ou recherchez une chaîne de texte dans le nom du modèle. Les requêtes de recherche ne respectent pas la casse.

1. Dans la ligne du modèle, sélectionnez *[!UICONTROL Paused]*.

## Activation d’un modèle d’alerte personnalisé {#alert-template-activate}

1. Dans l’angle supérieur droit, cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée") > **[!UICONTROL View Custom Alerts]** pour ouvrir l’onglet [!UICONTROL Alert Templates] .

1. (Facultatif) Filtrez la liste pour inclure des alertes pour un type d’entité spécifique ou recherchez une chaîne de texte dans le nom du modèle. Les requêtes de recherche ne respectent pas la casse.

1. Dans la ligne du modèle, sélectionnez *[!UICONTROL Active]*.

## Suppression d’un modèle d’alerte personnalisé {#alert-template-delete}

Vous ne pouvez supprimer que les modèles d’alerte que vous avez créés.

1. Dans l’angle supérieur droit, cliquez sur ![Alerte personnalisée](/help/search-social-commerce/assets/custom-alert.png "Alerte personnalisée") > **[!UICONTROL View Custom Alerts]** pour ouvrir l’onglet [!UICONTROL Alert Templates] .

1. (Facultatif) Filtrez la liste pour inclure des alertes pour un type d’entité spécifique ou recherchez une chaîne de texte dans le nom du modèle. Les requêtes de recherche ne respectent pas la casse.

1. Dans la ligne du modèle, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete-new.png "Supprimer").

1. Dans la zone du message de confirmation, cliquez sur **[!UICONTROL Delete]**.

## Paramètres du modèle d’alerte personnalisé {#alert-template-settings}

| Tabulation | Paramètre | Description |
|--- |--- |--- |
|  | [!UICONTROL Name] | Nom de l’alerte. Il doit contenir au moins cinq caractères. |
| [!UICONTROL Date Range] | [!UICONTROL Select Entity] | Type d’entité à évaluer : <i>[!UICONTROL Portfolio]</i>, <i>[!UICONTROL Campaign]</i> ou <i>[!UICONTROL Ad Group]</i>. |
| [!UICONTROL Date Range] | [!UICONTROL Period] | Période pour laquelle il convient d’évaluer les conditions de l’alerte. Les mesures sont évaluées de manière agrégée sur l’ensemble de la période. Les options vont de *[!UICONTROL Yesterday]* à *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] | \[Filtres définis\] | Conditions de déclenchement de l’alerte à l’heure spécifiée dans l’onglet [!UICONTROL Scheduling and Delivery] . Les colonnes disponibles varient selon le type d’entité. Tous les filtres sont liés à l’aide de la fonction booléenne ET, ce qui signifie que toutes les conditions spécifiées doivent être remplies.<ul><li><p>Pour ajouter un filtre, procédez comme suit :<p><ol><li><p>(Facultatif) Pour filtrer les noms des colonnes par chaîne de texte, saisissez la chaîne de recherche dans le champ de saisie [!UICONTROL ADD FILTER].</p></li><li><p>Dans la liste des colonnes, sélectionnez un nom de colonne.</p></li><li><p>Définissez le filtre sur la colonne :</p></li><ul><li><p>(Filtres sans champs de saisie) Cliquez sur ![Flèche vers le bas](/help/search-social-commerce/assets/arrow-down-expand.png "Flèche vers le bas") en regard du deuxième menu, puis cochez les cases en regard de chaque valeur à inclure.</p></li><li><p>(Tous les autres filtres avec champs de saisie) Sélectionnez un opérateur dans le deuxième menu, puis saisissez la valeur applicable.</p><p>Par exemple, si vous avez sélectionné la colonne « Clics » et que vous souhaitez renvoyer uniquement les lignes contenant plus de 100 clics, sélectionnez « supérieur à » et saisissez 100 dans le champ de saisie.</p><p>Selon le type de données, les opérateurs disponibles peuvent inclure <i>supérieur à</i>, <i>inférieur à</i>, <i>égal à</i>, <i>contient</i>, <i>ne contient pas</i>, <i>commence par</i>, <i>se termine par</i>, <i>aucune valeur</i>, <i>a une valeur</i>, <i>avant</i>, <i>après</i> ou <i>aucune date</i>.</p><p>**Remarque :** les valeurs de texte ne respectent pas la casse. Par exemple, si vous filtrez par campagnes avec « loan » dans le nom, les résultats peuvent inclure « Consumer Loans » et « loan applications » (demandes de prêt).</p></li></ol><li><p>Pour supprimer un filtre, cliquez sur ![Supprimer](/help/search-social-commerce/assets/delete.png "Supprimer") en regard de la définition du filtre.</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[when\] | Fréquence à laquelle l’alerte vérifie les filtres de condition spécifiés et, lorsque toutes les conditions sont remplies, envoie des notifications par e-mail :<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*Jour de la semaine*> à &lt;*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*Jour NN*> à &lt;*NN*> `[AM\|PM]`]</p></li></ul>**Remarque :** cette valeur n&#39;affecte pas la période d&#39;évaluation. |
|  | [!UICONTROL Email Recipients] | (Modifiable uniquement par le créateur du modèle d’alerte ; en lecture seule pour tous les autres) Utilisateurs enregistrés de Search, Social et Commerce auxquels envoyer des notifications lorsqu’une alerte est déclenchée. Par défaut, le nom de votre compte utilisateur est sélectionné. Vous pouvez éventuellement ajouter ou supprimer des utilisateurs ayant accès aux données de l’annonceur.<br><br>Lorsque l’alerte comprend jusqu’à 1 000 enregistrements, une version CSV de l’alerte est jointe à l’e-mail. |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
