---
title: Codes d’erreur pour les envois  [!DNL FreeWheel]  publicités
description: Référencez les codes d’erreur renvoyés pour les envois publicitaires vers  [!DNL FreeWheel].
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 3%

---

# Codes d’erreur pour les envois d’annonces publicitaires [!DNL FreeWheel]

Les messages d’erreur pour les envois d’annonces ayant échoué peuvent provenir d’Advertising DSP ou de [!DNL FreeWheel]. Recherchez les messages d’erreur dans la colonne [!UICONTROL API Response] de la boîte de dialogue de [[!UICONTROL FreeWheel Status]](freewheel-check-status.md).

## Erreurs internes à Advertising DSP

| Message d’erreur | Description | Étapes suivantes |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] n’a pas encore répondu que l’envoi a réussi ou échoué. | Vérifiez à nouveau le statut dans 10 minutes. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] n&#39;accepte pas les publicités britanniques sans numéros d&#39;horloge attribués. | Attribuez un numéro d’horloge à la publicité, puis soumettez à nouveau la publicité. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | Le transcodeur n&#39;avait pas fini de transcoder la publicité lorsque vous avez tenté de l&#39;envoyer. | Patientez dix minutes, puis soumettez à nouveau la publicité. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | L’offre soumise n’est pas configurée en tant qu’offre programmatique garantie. [!DNL FreeWheel] accepte uniquement les offres garanties. | Configurez l’ID d’offre en tant qu’offre programmatique garantie. L’annonce publicitaire est automatiquement envoyée à [!DNL FreeWheel] lorsque vous enregistrez l’emplacement par défaut programmatique garanti à la fin du workflow d’ID d’offre. |
| [!DNL Invalid external_deal_id:] \&lt;id_transaction\> | L’ID d’opération envoyé n’existe pas ou n’est pas actif du côté d’Adobe. | Assurez-vous que l’offre est active, puis soumettez à nouveau l’annonce. |
| [!DNL \[public_id=]\&lt;offre\>] n’existe pas | L’ID d’opération envoyé n’existe pas à la fin de la [!DNL FreeWheel]. | Contactez votre représentant [!DNL FreeWheel] pour confirmer l’ID de l’offre. |
| [!DNL Ad with identifier] \&lt;*nom de la publicité*\> [!DNL was not found.] | La clé publicitaire envoyée n’existe pas ou n’est pas active du côté d’Adobe. | Recherchez la clé publicitaire appropriée, puis soumettez à nouveau la publicité. |
| [!DNL Pending Submission] | La soumission est toujours en attente. | Actualisez la page. |

{style="table-layout:auto"}

## Erreurs d’API [!DNL FreeWheel]

| Code | Signification | Description | Étapes suivantes |
|--- |--- |--- |--- |
| 401 | Non Autorisé | Identifiants d’accès incorrects, manquants ou non valides. | Contactez votre équipe de compte Adobe. |
| 403 | Interdit | Le serveur a compris la demande mais refuse de l’autoriser. | Contactez votre équipe de compte Adobe. |
| 404 | Introuvable | La ressource demandée n’est pas disponible. Si l’identifiant Creative est introuvable dans l’opération PUT, une erreur 404 est renvoyée. | Contactez votre équipe de compte Adobe. |
| 405 | Méthode Non Autorisée | Une requête a été effectuée à partir d’une ressource à l’aide d’une méthode de requête non prise en charge par cette ressource (par exemple, l’utilisation de GET sur une méthode nécessitant l’envoi de données par POST ou l’utilisation de PUT sur une ressource en lecture seule). | Contactez votre équipe de compte Adobe. |
| 408 | Délai d’expiration de la demande | Une temporisation s’est produite pendant le traitement de cette requête. Les délais d’expiration sont généralement dus à des demandes simultanées d’accès exclusif à certaines ressources. | Soumettez à nouveau la demande lorsque vous recevez ce statut. Si le problème persiste, contactez l’équipe chargée de votre compte Adobe. |
| 422 | Entité impossible à traiter | Ressource non valide. Cette erreur se produit lorsque le corps de la requête n’est pas valide ou que la ressource créée/mise à jour n’est pas valide (par exemple, si l’ID d’offre est introuvable). Consultez [ Erreurs de l’API 422 FreeWheel ](#freewheel-422-errors) pour plus d’informations. | Contactez votre équipe de compte Adobe. |
| 500 | Erreur de serveur interne | Erreur système de l’API. | Contactez votre équipe de compte Adobe. |

{style="table-layout:auto"}

## [!DNL FreeWheel] API 422 Erreurs {#freewheel-422-errors}

| Code | Code HTTP | Description |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | Les données de la requête n’ont pas un format json valide. Vérifiez le message d’erreur pour plus de détails. |
| DATA_VALIDATION_FAILURE | 422 | Il manque des champs obligatoires dans les données de la requête ou le type de données est non valide. Vérifiez le message d’erreur pour plus de détails. |
| DATA_DEAL_INVALID | 422 | Le contrat n’est pas configuré correctement ou n’existe pas. Vérifiez le message d’erreur pour plus de détails. |
| DATA_DEAL_GET_FAILURE | 422 | L’offre est introuvable ou sa configuration présente un problème. Vérifiez le message d’erreur pour plus de détails. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | L’URL de création n’est pas valide. Vérifiez le message d’erreur pour plus de détails. |
| DATA_CREATIVE_LINK_FAILURE | 422 | Le contenu créatif n’était pas lié aux nœuds d’unité publicitaire de la transaction. Vérifiez le message d’erreur pour plus de détails. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | Le contenu créatif n’a pas été mis à jour. Vérifiez le message d’erreur pour plus de détails. |
| DATA_DSP_GET_FAILURE | 422 | Le DSP n’existe pas dans le système. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | Le lien de la création avec les annonces publicitaires n’a pas été annulé. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | Le contenu publicitaire n’a pas été supprimé. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | L&#39;URL n&#39;a pas été détectée. |
| DATA_ENTITY_NOT_FOUND | 422 | La création n’existe pas. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Présentation de la configuration d’offres programmatiques garanties dans  [!DNL FreeWheel]](/help/dsp/inventory/freewheel-overview.md)
>* [Accepter une offre dans le [!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)
>* [Envoyer une annonce pour une offre programmatique garantie à  [!DNL FreeWheel]](/help/dsp/inventory/freewheel-submit.md)
>* [Consultez le statut des publicités pour une offre  [!DNL FreeWheel] PG](/help/dsp/inventory/freewheel-check-status.md)
