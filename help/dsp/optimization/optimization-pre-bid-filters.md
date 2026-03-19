---
title: Filtres de pré-enchères au niveau de l’emplacement et utilisation
description: Référencez les filtres de pré-enchères au niveau de l’emplacement disponibles et découvrez comment les utiliser.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: dad30b0bd24c0286c1de6520471cb90707046ff3
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Filtres de pré-enchères au niveau de l’emplacement et utilisation

| Filtre de pré-enchères | Description | Quand utiliser ce filtre |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Définit un seuil de prédiction minimal pour la probabilité qu’une enchère puisse entraîner un clic publicitaire. Par exemple, si vous définissez le seuil sur 0,1 %, vous enchérissez sur les enchères uniquement lorsque la probabilité prévue d’un clic est supérieure ou égale à 0,1 %.<br><br><b>Remarque :</b> les filtres sont appliqués avant les objectifs d’optimisation. Par conséquent, des filtres très stricts peuvent empêcher les dépenses. | À utiliser lorsque vous avez un objectif d’indicateur de performance clé minimum pour le taux de clic publicitaire (CTR) et que vous ne souhaitez pas dépenser votre budget lorsque le CTR est inférieur au seuil. Ce filtre peut être assez restrictif. Il est donc important de définir des objectifs réalistes. Selon d&#39;autres restrictions sur le placement, un objectif de 0,03 à 0,07 % est généralement un bon point de départ. Vous pouvez l’optimiser au niveau du site selon vos besoins afin d’améliorer les mesures.<br><br>Si votre objectif est d’obtenir un CTR minimum et le meilleur CPM possible, la configuration recommandée est de combiner un filtre [!UICONTROL Click Through Rate] avec l’objectif d’optimisation « [!UICONTROL Lowest CPM] ». Si votre objectif est un CPM maximum sans réel avantage à surpasser, et un CTR minimum, alors l’association d’un filtre [!UICONTROL Click Through Rate] avec l’objectif d’optimisation « [!UICONTROL Always Max Bid + Highest CTR] » peut être plus appropriée. |
| [!UICONTROL 100% Completion Rate] | Définit un taux d&#39;achèvement minimal requis qui doit être atteint avant que vous enchérissiez sur une impression. | Utilisez ce filtre lorsque l’objectif principal de la campagne est le taux d’achèvement. Tenez compte des autres paramètres de ciblage, mais 65 % est le pourcentage de départ recommandé. |
| [!UICONTROL Player Size - Adobe] | Définit la taille minimale requise pour le lecteur à l’aide des données de DSP. Vous pouvez enchérir sur une impression lorsque le seuil de [!UICONTROL Player Size] est atteint. | Utilisez pour vous assurer que vous diffusez un inventaire complet des lecteurs d’épisodes à l’aide de données provenant de DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Définit une taille de lecteur minimale requise, à l’aide des données de [!DNL Moat] ou [!DNL Integral Ad Science] ([!DNL IAS]). Vous pouvez enchérir sur une impression lorsque le seuil de [!UICONTROL Player Size] est atteint. | Utilisez pour vous assurer que vous diffusez un inventaire complet des lecteurs d’épisodes à l’aide de données [!DNL Moat] ou [!DNL IAS] à l’échelle de la plateforme.<br><br><b>Remarque :</b> utilisez ce filtre uniquement lorsque la campagne est configurée pour utiliser des données [!DNL Moat] ou [!DNL IAS]. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Définit un pourcentage de visibilité minimal requis à l’aide des mesures et des nombres de visibilité de DSP. Vous pouvez enchérir sur une impression lorsque le seuil spécifié est atteint.<br><br><b>Remarques :</b><ul><li>Si le paramètre de [!UICONTROL Viewability Sensitivity] de la campagne est « [!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)] », la norme de mesure de visibilité [!DNL Media Rating Council] (MRC) est utilisée pour la campagne. Si le paramètre [!UICONTROL Viewability Sensitivity] est défini sur « [!UICONTROL Strict (100% of ad in view & audio on for 50% duration)] », la norme de mesure de visibilité [!DNL GroupM] est utilisée pour la campagne.</li><li>Les définitions de mesure d’Adobe diffèrent des définitions tierces. Il peut donc y avoir de légères incohérences avec les données tierces.</li></ul> | La bonne pratique consiste à faire correspondre l’objectif d’optimisation et les paramètres de filtre de pré-enchères avec le paramètre [!UICONTROL Viewability Sensitivity] de la campagne. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Comment DSP optimise vos campagnes](optimization-how-dsp-optimizes-campaigns.md)
>* [ Paramètres du package ](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres d’emplacement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Paramètres de Campaign](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Objectifs d’optimisation et utilisation](optimization-goals.md)
