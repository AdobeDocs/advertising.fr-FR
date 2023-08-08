---
source-git-commit: a1a8c1b563d419090ddbefacc55be869c1ee7bcf
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---
# Champ Suffixe de page d’entrée dans les paramètres de compte GGL et MS, les paramètres de campagne et certains paramètres d’annonce

**[!UICONTROL Landing Page Suffix]:** ([!DNL Google Ads] et [!DNL Microsoft Advertising] Comptes uniquement ; facultatif) Tout paramètre à ajouter à la fin des URL finales pour effectuer le suivi des informations ; incluez tous les paramètres dont votre entreprise doit effectuer le suivi. Exemple : `param1=value1&param2=value2`

Les comptes qui utilisent le suivi de conversion d’Adobe Advertising doivent inclure l’identifiant de clic du réseau publicitaire (`gclid` pour [!DNL Google Ads] ou `msclkid` pour [!DNL Microsoft Advertising]) dans le suffixe.

Les comptes avec une intégration Adobe Analytics doivent utiliser le paramètre s_kwcid . Si le compte dispose d’une implémentation s_kwcid côté serveur, le paramètre est ajouté automatiquement lorsqu’un utilisateur clique sur une publicité. Dans le cas contraire, vous devez l’ajouter manuellement à cet emplacement. Voir [Formats de suffixes requis pour Google Ads](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et [Formats de suffixes requis pour Microsoft Advertising](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

**Remarques :**

* Ce champ n’est pas mis à jour par la variable [!UICONTROL Auto Upload] paramètre de suivi.

* Les suffixes de page d’entrée aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur du réseau publicitaire.
