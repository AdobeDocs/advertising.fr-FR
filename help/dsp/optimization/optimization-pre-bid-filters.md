---
title: Filtres de pré-offre au niveau de l’emplacement et comment les utiliser
description: Référencez les filtres de pré-enchère au niveau de l’emplacement disponibles et découvrez comment les utiliser.
feature: DSP Optimization
exl-id: 34a15666-7ca2-416d-9064-8638ca81e5b3
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Filtres de pré-offre au niveau de l’emplacement et comment les utiliser

| Filtre avant offre | Description | Quand utiliser ce filtre |
| ---------------| ----------- | ---------------------- |
| [!UICONTROL Click Through Rate] | Définit un seuil de prédiction minimal pour la probabilité qu’une enchère puisse entraîner un clic publicitaire. Par exemple, si vous définissez le seuil sur 0,1 %, vous enchérissez uniquement sur les enchères lorsque la probabilité prévue d’un clic est supérieure ou égale à 0,1 %.<br><br><b>Remarque :</b> Les filtres sont appliqués avant les objectifs d’optimisation. Par conséquent, des filtres très stricts peuvent empêcher les dépenses. | Utilisez cette option lorsque vous disposez d’un objectif IPC minimal pour le taux de clics publicitaires (CTR) et que vous ne souhaitez pas dépenser votre budget lorsque le CTR est inférieur au seuil. Ce filtre peut être très restrictif, il est donc important de définir des objectifs réalistes. Selon d’autres restrictions sur l’emplacement, un objectif de 0,03 à 0,07 % est généralement un bon point de départ. Vous pouvez l’optimiser au niveau du site, si nécessaire, afin d’améliorer les mesures.<br><br>Si votre objectif est d’obtenir un CTR minimal et le meilleur CPM possible, la configuration recommandée consiste à combiner un filtre [!UICONTROL Click Through Rate] avec l’objectif d’optimisation &quot;[!UICONTROL Lowest CPM]&quot;. Si votre objectif est un CPM maximal sans avantage réel pour l’excès de performances et un CTR minimal, l’association d’un filtre [!UICONTROL Click Through Rate] à l’objectif d’optimisation &quot;[!UICONTROL Always Max Bid + Highest CTR]&quot; peut être plus appropriée. |
| [!UICONTROL 100% Completion Rate] | Définit un taux d’achèvement minimal requis qui doit être atteint avant que vous n’enchériez sur une impression. | Utilisez ce filtre lorsque le principal objectif de la campagne est les taux d&#39;achèvement. Facteur dans d’autres paramètres de ciblage, mais 65 % est le pourcentage de départ recommandé. |
| [!UICONTROL Player Size - Adobe] | Définit la taille minimale requise du lecteur à l’aide des données de DSP. Vous pouvez enchérir sur une impression lorsque le seuil [!UICONTROL Player Size] est atteint. | Utilisez pour vous assurer que vous effectuez une diffusion sur l’inventaire du lecteur d’épisodes complet à l’aide des données de DSP. |
| [!UICONTROL Player Size 3rdParty (Moat/IAS)] | Définit une taille minimale de lecteur requise, à l’aide des données de [!DNL Moat] ou [!DNL Integral Ad Science] ([!DNL IAS]). Vous pouvez enchérir sur une impression lorsque le seuil [!UICONTROL Player Size] est atteint. | Utilisez pour vous assurer que vous effectuez une diffusion sur l’inventaire complet du lecteur d’épisodes à l’aide de données [!DNL Moat] ou [!DNL IAS] à l’échelle de la plateforme.<br><br><b>Remarque : </b> Utilisez ce filtre uniquement lorsque la campagne est configurée pour utiliser les données [!DNL Moat] ou [!DNL IAS]. |
| [!UICONTROL Viewability Adobe (MRC or [!DNL GroupM])] | Définit un pourcentage minimal requis de visibilité, à l’aide DSP nombres et mesures de visibilité. Vous pouvez enchérir sur une impression lorsque le seuil spécifié est atteint.<br><br><b>Notes :</b><ul><li>Si le paramètre [!UICONTROL Viewability Sensitivity] de la campagne est &quot;[!UICONTROL Standard (50% of ad in view for 2 consecutive seconds)]&quot;, la norme de mesure de visibilité [!DNL Media Rating Council] (MRC) est utilisée pour la campagne. Si le paramètre [!UICONTROL Viewability Sensitivity] est &quot;[!UICONTROL Strict (100% of ad in view & audio on for 50% duration)]&quot;, la norme de mesure de la visibilité [!DNL GroupM] est utilisée pour la campagne.</li><li>Les définitions des mesures d’Adobe diffèrent des définitions tierces. Il peut donc y avoir de légères incohérences avec les données tierces.</li></ul> | La bonne pratique consiste à correspondre à l’objectif d’optimisation et à tous les paramètres de filtre pré-enchère avec le paramètre [!UICONTROL Viewability Sensitivity] de la campagne. |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [Comment DSP optimise vos campagnes](optimization-how-dsp-optimizes-campaigns.md)
>* [Paramètres du module](/help/dsp/campaign-management/packages/package-settings.md)
>* [Paramètres de placement](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Paramètres de campagne](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Objectifs d’optimisation et comment les utiliser](optimization-goals.md)
