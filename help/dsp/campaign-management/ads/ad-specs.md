---
title: Spécifications des publicités
description: Référencez les spécifications publicitaires générales et spécifiques à l’éditeur.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---

# Spécifications des types de publicité pris en charge

## Publicités vidéo (pré-défilement, CTV et vidéo universelle)

### Screens pris en charge

Les publicités sont diffusées par défaut sur les appareils de bureau, mobiles et de télévision connectés. Le ciblage des périphériques est disponible pour ajuster la diffusion.

### Serveurs publicitaires tiers pris en charge

Vous pouvez utiliser des feuilles de balises de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, voir &quot;[Partenaires certifiés du service d’annonces](certified-ad-servers.md)&quot;.

### Conditions requises pour l’Assets vidéo haute définition (obligatoire)

**Type de balise vidéo :** JavaScript VPAID 2.0 ou VAST (CTV). Toutes les unités publicitaires VPAID doivent se conformer à la [spécification VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) telle que définie par l’Interactive Advertising Bureau (IAB).

**Codec vidéo :** MP4/H.264

**Résolution :** 1 280 x 720 pour 720p, 1 920 x 1 080 pour 1 080p

**Débit :** 1 500 à 2 500 Kbit/s pour 720p, 2 500 à 3 500 Kbit/s pour 1 080p

**H.264 Profil/Niveau :** Profil élevé, niveau 3.1 pour 720p ; profil élevé, niveau 4.0 pour 1080p

**Taux d’images vidéo :** 29,970 ips (communément appelé 30 ips) pour les pays NTSC, 25 ips pour les pays PAL, 23,976 ips (communément appelé 24 ips) pour le contenu d’affichage de film

**Espace colorimétrique vidéo :** 4:2:0 sous-échantillonnage de la chroma YUV

**Entrelacement vidéo :** Analyse progressive, c’est-à-dire non entrelacée. Pas de mouvement à l’intérieur du champ (cadres de fusion) ni d’entrelacement.

**Leaders (Slate):** Non autorisé

**Codec audio :** AAC-LC ou HE-AACv1

**Débit audio :** 128-192 Kbit/s pour AAC-LC, 64-128 Kbit/s pour HE-AACv1

**Canal audio :** Combinaison stéréo 2 canaux

**Taux d’échantillonnage audio :** 44,1 kHercules ou 48 kHercules, selon le matériau source

**Niveaux audio :** 24 LKFS (+/- 2.0 dB) aux États-Unis selon l’ATSC A/85 ; 23 LUFS (+/- 1.0) dans l’UE selon l’EBU R128

#### Exigences supplémentaires de l’éditeur pour les publicités télévisées connectées

* **Réseau A+E :** Voir les [spécifications de publicité](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf) du réseau A+E

* **Discovery:** Voir [spécifications de publicité](/help/dsp/assets/discovery-networks-ad-specs.pdf) de Discovery.

* **Disney (y compris Hulu):** Voir les [spécifications de publicité](https://hulu.disneyadsales.com/ad-products/video-commercial/) de Disney.

* **HBO Max :** Voir les [spécifications de publicité](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx) de HBO Max.

* **NBCUnival:**

   * [Vidéo numérique](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Pic](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount :** Voir les [spécifications de publicité](https://www.paramount.com/digital-ads) de Paramount.

## Publicités affichées

### Screens pris en charge

Les publicités sont diffusées par défaut sur les ordinateurs de bureau et les appareils mobiles. Le ciblage des périphériques est disponible pour ajuster la diffusion.

### Types de fichiers pris en charge

**Image :** GIF, JPG/JPEG, PNG

**HTML5:** Types de fichiers image : GIF, JPG/JPEG, PNG, SVG

### Conditions requises pour Image Assets (obligatoire)

Universal Display est pris en charge.

**Tailles d’annonces recommandées :** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x600, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x 90

**Serveurs d’annonces tiers pris en charge :** Vous pouvez utiliser des feuilles de balises de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, voir &quot;[Partenaires certifiés du service d’annonces](certified-ad-servers.md)&quot;.

## Publicités audio

### Screens pris en charge

Ordinateur de bureau, mobile, tablette, haut-parleurs intelligents et télévision connectée

### Serveurs publicitaires tiers pris en charge

Vous pouvez utiliser des feuilles de balises de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, voir &quot;[Partenaires certifiés du service d’annonces](certified-ad-servers.md)&quot;.

### Conditions requises pour Audio Assets (obligatoire)

**Type de fichier :** MP3, OGG, AAC

**Leaders (ardoise) :** Non autorisé

**Taille maximale du fichier :** 2 Mo

**Débit :** 128

**Longueur du fichier :** 0-60 s

#### Exigences supplémentaires pour les éditeurs

* **[!DNL iHeartRadio]**
   * Durée : 5, 15, 30 ou 60 secondes
   * Type de fichier : MP3
   * Taille maximale du fichier : 320 Kbit/s
   * Volume : 44,1 kGHz

* **[!DNL Pandora]**
   * Durée : 15 ou 30 secondes
   * Type de fichier : MP4 (in-app), MP3 (poste de travail)
   * Taille maximale du fichier : 2,2 Mo

* **[!DNL SoundCloud]**
   * Durée : 6, 15 ou 30 secondes
   * Type de fichier : MP3
   * Taille maximale du fichier : 5 Mo

* **[!DNL Spotify]**
   * Durée : jusqu’à 30 secondes
   * Type de fichier : OGG
   * Taille maximale du fichier : 500 Mo
   * Volume : RMS normalisé à -14 ; pic dBFS normalisé à -0,2 dBFS

* **[!DNL TargetSpot]**
   * Durée : 15, 30 ou 60 secondes
   * Type de fichier : MP3

* **[!DNL TuneIn]**
   * Durée : 10, 15 ou 30 secondes
   * Type de fichier : MP3, OGG
   * Volume : 44,1 kGHz

### Conditions requises pour les bannières publicitaires d’accompagnement (facultatif)

**Tailles prises en charge :** 300x250, 500x500, 640x640, 1024x1024

#### Exigences supplémentaires pour les éditeurs

* **[!DNL iHeartRadio]:**
   * Type de fichier : JPEG, JPG, PNG, GIF, SWF, HTML
   * Taille maximale du fichier : 2,2 Mo
   * Dimensions : 300 x 250

* **[!DNL Pandora]:**
   * Type de fichier : JPEG, GIF
   * Taille maximale du fichier : Taille : 100 Ko
   * Dimensions : 300 x 250 (mobile ou ordinateur de bureau) ou 500 x 500 (ordinateur de bureau)

* **[!DNL SoundCloud]:**
   * Type de fichier : JPG statique, PNG
   * Taille de fichier maximale : moins de 400 Ko
   * Dimensions : 1 024 x 1 024

* **[!DNL Spotify]:**
   * Type de fichier : JPG statique, PNG
   * Taille maximale du fichier : 200 Ko
   * Dimensions : 300 x 250

* **[!DNL TuneIn]:**
   * Type de fichier : JPEG, JPG, PNG, GIF, HTML
   * Taille maximale du fichier : 2 Mo
   * Dimensions : 300 x 250

## Publicités d’affichage natives

Chaque publicité peut inclure une image fixe ou un GIF mobile (paragraphe de film).

### Screens pris en charge

Les publicités sont diffusées par défaut sur les ordinateurs de bureau et les appareils mobiles. Le ciblage des périphériques est disponible pour ajuster la diffusion.

### Assets requise pour tous les formats natifs du flux

#### Ressource image

**Résolution :** Minimum 600 x 600 px ; minimum recommandé de 1 200 x 627 px

**Type de fichier :** JPEG (image publicitaire ou image de couverture de publicité vidéo), GIF (cinemograph)

**Taille de fichier :** Moins de 1 Mo (l’image doit être sans texte).

#### Logo du annonceur

**Résolution :** 80 x 80 px minimum ; minimum recommandé de 300 x 300 px

**Type de fichier :** JPEG ou PNG.

**Format :** rapport 1x1

>[!NOTE]
>
>Selon l’image sur laquelle il sera superposé, choisissez entre les ressources de logo claires ou sombres.

#### Texte/Copie

**Titre :** 200 caractères maximum ; 25 caractères recommandés

**Légende :** 200 caractères au maximum ; 100 caractères recommandés

**Parrainé par :** 200 caractères au maximum ; 30 caractères recommandés

**Appel à l’action (MoPub uniquement) :** 15 caractères maximum

>[!NOTE]
>
>La disposition finale est définie par l’éditeur au moment de l’exécution. Si une publicité dépasse le nombre de caractères recommandé, certains fournisseurs d’inventaire peuvent ne pas diffuser la publicité, ou l’éditeur ou le fournisseur de services de messagerie peut tronquer le texte.

#### URL de page d’entrée

URL de clic publicitaire avec des outils de suivi de clics facultatifs.

Conditions requises pour les outils de suivi des clics :

* Pixels de suivi d’impression tiers : format d’URL d’image 1x1 uniquement

* Suivi JavaScript de la visibilité : pris en charge pour IAS uniquement ; images 1x1 au format JS.append uniquement

* pixels de suivi des clics tiers : Doit rediriger vers la page d’entrée incorporée dans l’URL (redirection HTTP 302)

* Les outils de suivi des clics de la plateforme de gestion des données (DMP) avec 200 réponses ou plus ne sont pas pris en charge.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Créer plusieurs publicités tierces](ad-create-multiple.md)
>* [Modifier une publicité](ad-edit.md)
