---
title: Métadonnées C2PA dans Creative Studio
description: Découvrez comment les métadonnées C2PA sont automatiquement associées au contenu généré ou modifié avec l’IA générative dans Creative Studio.
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: d335c890ccc3ff8b2d391881660a71d10fcba53a
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# Métadonnées C2PA dans [!UICONTROL Creative Studio]

[!UICONTROL Creative Studio] associe automatiquement les métadonnées C2PA au contenu généré ou modifié avec l’IA générative, de sorte que la provenance de votre contenu publicitaire soit enregistrée en tant que métadonnées invisibles et durables. Les métadonnées respectent les normes de la [ Coalition for Content Provenance and Authenticity ](https://c2pa.org/) (C2PA).

## Types de contenu et leur portée {#cc-content-types}

| Type de contenu | Pris en charge ? | Service d’IA qui génère le contenu | Modèle qui génère les informations d’identification |
| --- | --- | --- | --- |
| Images | Oui. Les métadonnées C2PA sont jointes lorsque les images sont générées ou modifiées avec l’IA générative et conservées par le biais d’opérations de recadrage et de redimensionnement effectuées par l’assistant AI. | [!DNL Adobe Firefly C2PA] | [!DNL Gemini Flash] |

## Actions qui joignent des métadonnées C2PA

Le tableau suivant résume le moment où des métadonnées C2PA sont jointes, en fonction de l’action d’image effectuée dans l’assistant IA dédiée à l’[!UICONTROL Creative Studio].

| Action | Description | Métadonnées C2PA jointes ? | Exemple de cas d’utilisation |
| --- | --- | --- | --- |
| **Générer une image** | Créer une image à l’aide d’une invite de texte | Toujours, car l’image est générée par l’IA générative. | Vous utilisez une invite de texte pour générer une nouvelle image d’arrière-plan ou un nouveau logo pour un modèle d’annonce publicitaire.<br><br>Vous utilisez une invite de texte pour remplacer l’image par défaut dans un concept d’annonce par une ressource téléchargée à partir de votre bibliothèque.<br><br>Vous utilisez une invite de texte pour générer des variantes d’une image d’arrière-plan dans un modèle d’annonce publicitaire. |

## Que se passe-t-il lorsque votre contenu est déplacé ? {#cc-content-moves}

La chaîne de provenance complète est conservée lorsqu’un utilisateur télécharge un fichier image ou qu’il est envoyé pour être diffusé dans une publicité.

## Que comprennent les métadonnées C2PA ?

Pour chaque génération ou modification de GenAI, les éléments suivants sont inclus dans les métadonnées C2PA. Si une ressource est modifiée plusieurs fois, chaque opération apparaît dans les métadonnées C2PA.

* Nom et informations de version du système d’IA utilisé ([!DNL Adobe Firefly C2PA])
* Modèle d’IA utilisé ([!DNL Gemini Flash])
* Utilisation : s’il a été généré ou modifié à l’aide de GenAI
* Date et heure de création et/ou de modification du contenu avec les outils d’IA génératifs
* Identifiant unique (qui peut être utilisé pour distinguer chaque utilisation de l’IA générative)

## Comment puis-je afficher les métadonnées C2PA d’une image ?

Pour afficher l’historique complet des ressources d’une image, procédez comme suit :

* Ouvrez le fichier image dans un outil de contrôle de l’authenticité du contenu, tel que https://contentauthenticity.adobe.com/inspect ou https://verify.contentauthenticity.org/.

* Affichez les métadonnées de l’image.

* Affichez le code de l’image à l’aide de l’outil d’inspection du code de votre navigateur (souvent appelé [!DNL Inspect]).

![Exemple de métadonnées C2PA pour une image](/help/creative/assets/cs-content-credentials-example.png "Métadonnées C2PA pour une image")

## Ressources supplémentaires

* [Directives d’utilisation relatives à l’IA [!DNL Adobe] générative](https://www.adobe.com/fr/legal/licenses-terms/adobe-gen-ai-user-guidelines.html)

>[!MORELIKETHIS]
>
>* [À propos de Creative Studio](/help/creative/creative-studio/creative-studio-about.md)
