---
title: Glossaire
description: Voir les définitions des termes clés.
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# Glossaire {#glossary}

*Version bêta fermée*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**clic publicitaire :** clic publicitaire qui entraîne une conversion.

**cible de transmission des données :** cibles de transmission des données permettent de sélectionner des éléments publicitaires en fonction des données fournies en temps réel par le DSP, l’éditeur ou le partenaire. Cela peut inclure des données tierces.

<!-- verify this -->Dans une expérience publicitaire, chaque cible de transfert de données peut inclure jusqu’à cinq paires clé-valeur ; vous spécifiez les clés et au moins une valeur dans le premier nœud cible à ce niveau, et les mêmes clés sont disponibles pour les nœuds cibles frères. Chacune des paires clé-valeur est ajoutée sous la forme d’une macro à la balise publicitaire pour cette expérience. Au moment de l’impression de la publicité, le DSP, l’éditeur ou le partenaire est chargé de remplacer les valeurs par des données spécifiques à cette impression. Les informations sont transmises à [!DNL Creative] afin qu’elles puissent afficher une expérience d’annonce publicitaire appropriée en fonction des règles définies dans l’expérience.

Par exemple, pour cibler un ou plusieurs contenus publicitaires possibles pour les visionneuses qui sont de sexe féminin et qui se trouvent dans le segment 1234, vous devez configurer les cibles de transmission de données `gender=female` et `segment=1234` pour le nœud cible. Le DSP qui sert l’impression renseigne la balise avec les informations de genre et de segment. L’un des contenus publicitaires associés s’affiche pour les visiteurs qui répondent aux exigences spécifiées.

**engagement transversal :** engagement publicitaire (tel que le défilement d’une annonce du carrousel ou le développement d’une annonce publicitaire) qui entraîne une conversion. Ce type d’événement est distinct du clic sur l’annonce pour accéder à une page de destination ou à un événement sur la page de destination.

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**affichage publicitaire :** impression d’annonce publicitaire, ou chaîne d’impressions, qui entraîne une conversion sans que l’utilisateur clique sur une annonce.
