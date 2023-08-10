---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---
# Définition du suffixe d’URL final

<!-- Used in many places; in inventory feed templates, it's actually called "Campaign Final URL Suffix," but leaving this generic anyway since it's a paragraph-level include file -->

**[!UICONTROL Final URL Suffix]:** ([!DNL Google Ads] et [!DNL Microsoft Advertising] Comptes uniquement ; facultatif) Tout paramètre à ajouter à la fin des URL finales pour effectuer le suivi des informations ; incluez tous les paramètres dont votre entreprise doit effectuer le suivi. Exemple :`param1=value1&param2=value2`

Dans les comptes qui utilisent le suivi de conversion d’Adobe Advertising, le suffixe doit inclure l’identifiant de clic du réseau publicitaire (`msclkid` pour [!DNL Microsoft Advertising]; `gclid` pour [!DNL Google Ads]).

Les comptes avec une intégration Adobe Analytics doivent utiliser la variable [AMO ID](/help/integrations/analytics/ids.md) . Si le compte dispose d’une mise en oeuvre AMO ID côté serveur, le paramètre est automatiquement ajouté lorsqu’un utilisateur clique sur une publicité. Dans le cas contraire, vous devez l’ajouter manuellement à cet emplacement. Voir [formats de suffixes requis pour [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) et [formats de suffixes requis pour [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

>[!NOTE]
>
>* Ce champ n’est pas mis à jour par la variable [!UICONTROL Auto Upload] paramètre de suivi.
>* Les suffixes d’URL finaux aux niveaux inférieurs remplacent le suffixe au niveau du compte. Pour faciliter la maintenance, utilisez uniquement le suffixe au niveau du compte, sauf si un suivi différent pour les composants de compte individuels est nécessaire. Pour configurer un suffixe au niveau du groupe publicitaire ou inférieur, utilisez l’éditeur du réseau publicitaire.
