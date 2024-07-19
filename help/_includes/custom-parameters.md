---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---
# Champ Paramètres personnalisés dans les paramètres de campagne GGL et MS, les paramètres du groupe publicitaire MS et les paramètres de publicité multimédia et réactive MS

**[!UICONTROL Custom Parameters]:** (Facultatif ; applicable aux campagnes d’audience uniquement pour [!DNL Microsoft Advertising]) Paires de nom et de valeur pour trois paramètres personnalisés au maximum. La longueur maximale des noms est de 16 caractères alphanumériques ; la longueur maximale des valeurs est de 200 caractères, paramètres incorporés compris.

Vous pouvez inclure vos noms de paramètre personnalisés dans les modèles de suivi pour l’entité et ses entités enfants. Lorsqu’un utilisateur clique sur une publicité appropriée, le réseau de publicités remplace le nom du paramètre par la valeur de paramètre définie. Par exemple, si vous créez un paramètre client `{_color}=red` et que votre modèle de suivi comprend `http://tracker.example.com/?color={_color}&u={lpurl}`, &quot;rouge&quot; est inséré dans le paramètre de couleur lorsqu’un utilisateur clique sur une publicité.

Paramètres personnalisés au niveau du groupe publicitaire ou ([!DNL Microsoft Advertising] uniquement) au niveau de la campagne de remplacement
paramètres personnalisés portant le même nom.
