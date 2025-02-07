---
title: Glossaire
description: Voir les définitions des termes clés.
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '286'
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

**engagement transversal :** engagement publicitaire (tel que regarder une vidéo ou développer une publicité) qui entraîne une conversion.

<!-- or flexible html5 creative variation? -->
**variation d’une création HTML 5 flexible :** dérivation d’une ressource de création HTML 5 flexible dans votre [!UICONTROL Creative Libraries], générée lorsque vous affectez la création à une expérience et modifiez l’un des attributs par défaut dans l’expérience.

<!-- Not sure if this will be implemented, and how:
You can view all derived creatives, including not only the base creatives you've added but also each child creative derivation, in the card view in [!UICONTROL Creative] > [!UICONTROL Libraries]. In the toolbar, click __?__ , and then select Derived Creatives. [Clarify how to tell which have variations. I can't find any now.]
-->

**affichage publicitaire :** impression d’annonce publicitaire, ou chaîne d’impressions, qui entraîne une conversion sans que l’utilisateur clique sur une annonce.
