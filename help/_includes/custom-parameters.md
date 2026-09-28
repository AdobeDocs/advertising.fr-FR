---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%
---
# Champ Paramètres personnalisés dans les paramètres de campagnes GGL et MS, les paramètres de groupes d’annonces MS et les paramètres d’annonces multimédias et responsive MS

**[!UICONTROL Custom Parameters]:** (facultatif ; applicable aux campagnes d’audience uniquement pour [!DNL Microsoft Advertising]) Paires de noms et de valeurs pour un maximum de trois paramètres personnalisés. La longueur maximale des noms est de 16 caractères alphanumériques ; la longueur maximale des valeurs est de 200 caractères, y compris les paramètres incorporés.

Vous pouvez inclure vos noms de paramètres personnalisés dans les modèles de suivi pour l’entité et ses entités enfants. Lorsqu’un utilisateur clique sur une annonce publicitaire appropriée, le réseau publicitaire remplace le nom du paramètre par la valeur du paramètre défini. Par exemple, si vous créez un paramètre client `{_color}=red` et que votre modèle de suivi inclut des `http://tracker.example.com/?color={_color}&u={lpurl}`, le terme « rouge » est inséré dans le paramètre de couleur lorsqu’un utilisateur clique sur une publicité.

Les paramètres personnalisés au niveau du groupe publicitaire ou ([!DNL Microsoft Advertising] uniquement) de la publicité remplacent ceux de la campagne
paramètres personnalisés portant le même nom.
