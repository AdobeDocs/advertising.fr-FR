---
title: Spécifications publicitaires
description: Référencez les spécifications publicitaires générales et spécifiques à l’éditeur.
feature: DSP Ads
exl-id: 133dfc0d-d839-4e06-a819-21e3e630830c
source-git-commit: a6f9bb2d714e7ddb22f74c9c614772eca30f9e40
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Spécifications pour les types d’annonces pris en charge

## Publicités vidéo (pré-roll, CTV et vidéo universelle)

### Screens pris en charge

Les publicités sont diffusées par défaut sur les ordinateurs de bureau, les appareils mobiles et les téléviseurs connectés. Le ciblage de l’appareil est disponible pour ajuster la diffusion.

### Serveurs Publicitaires Tiers Pris En Charge

Vous pouvez utiliser des feuilles de balises provenant de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, reportez-vous à la rubrique « [Partenaires certifiés de diffusion des publicités](certified-ad-servers.md) ».

### Conditions requises pour la vidéo haute définition Assets

**Type de balise vidéo :** VPAID 2.0 JavaScript ou VAST (CTV). Toutes les unités publicitaires VPAID doivent respecter la spécification [VPAID 2.0](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) définie par l’IAB (Interactive Advertising Bureau).

**Codec vidéo :** MP4/H.264

**Résolution :** 1 280 x 720 pour 720p, 1 920 x 1 080 pour 1 080p

**Débit :** 1 500 à 2 500 kbit/s pour 720p, 2 500 à 3 500 kbit/s pour 1 080p

**H.264 Profil/Niveau :** Profil élevé, niveau 3.1 pour 720p ; Profil élevé, niveau 4.0 pour 1080p

**Fréquence d’image vidéo :** 29,970 i/s (communément appelée 30 i/s) pour les pays NTSC, 25 i/s pour les pays PAL, 23,976 i/s (communément appelée 24 i/s) pour le contenu filmique

**Espace colorimétrique vidéo :** sous:2:échantillonnage YUV Chroma

**Entrelacement vidéo :** balayage progressif, c’est-à-dire non entrelacé. Aucun mouvement intra-champ (images de fusion) ni entrelacement.

**Leaders (ardoise) :** non autorisé

**Codec audio :** AAC-LC ou HE-AACv1

**Débit audio :** 128 à 192 kbit/s pour AAC-LC, 64 à 128 kbit/s pour HE-AACv1

**Canal audio :** mix stéréo à 2 canaux

**Fréquence d&#39;échantillonnage audio :** 44,1 kHz ou 48 kHz, selon le matériau source

**Niveaux audio :** 24 LUFS (+/- 2,0 dB) aux États-Unis selon ATSC A/85 ; 23 LUFS (+/- 1,0) dans l&#39;UE selon EBU R128

#### Exigences supplémentaires de l’éditeur pour les publicités TV connectées

* **A+E Network :** consultez les spécifications [ad de A+E Network](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **Discovery :** consultez les spécifications des annonces publicitaires [&#x200B; de Discovery](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **Disney (inclus Hulu) :** Voir les spécifications des [annonces publicitaires](https://www.disneyadvertising.com/mediakit/#specifications) de Disney.

* **HBO Max :** consultez les spécifications [ad de HBO Max](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUniversal:**

   * [Vidéo numérique](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [&#x200B; Livestream &#x200B;](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Paon](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount :** consultez les spécifications [ad de Paramount](https://www.paramount.com/digital-ads).

## Afficher les publicités

### Screens pris en charge

Les publicités sont diffusées par défaut sur les ordinateurs de bureau et les appareils mobiles. Le ciblage de l’appareil est disponible pour ajuster la diffusion.

### Types de fichiers pris en charge

**Image :** GIF, JPG/JPEG, PNG

**HTML5:** Types de fichiers image : GIF, JPG/JPEG, PNG, SVG

### Conditions requises pour Image Assets

Universal Display est pris en charge.

**Tailles d’annonces recommandées :** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x600, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Serveurs publicitaires tiers pris en charge :** vous pouvez utiliser des feuilles de balises provenant de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, reportez-vous à la rubrique « [Partenaires certifiés de diffusion des publicités](certified-ad-servers.md) ».

## Publicités audio

### Screens pris en charge

Ordinateur de bureau, mobile, tablette, haut-parleurs intelligents et télévision connectée

### Serveurs Publicitaires Tiers Pris En Charge

Vous pouvez utiliser des feuilles de balises provenant de [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid] et [!DNL Sizmek]. Pour obtenir la liste complète des fournisseurs pris en charge, reportez-vous à la rubrique « [Partenaires certifiés de diffusion des publicités](certified-ad-servers.md) ».

### Conditions requises pour Audio Assets

**Type de fichier :** MP3, OGG, AAC

**Leaders (ardoise) :** non autorisé

**Taille de fichier maximale :** 2 Mo

**Débit binaire :** 128

**File Length :** 0-60s

#### Autres exigences de l&#39;éditeur

* **[!DNL iHeartRadio]**
   * Durée : 5, 15, 30 ou 60 secondes
   * Type de fichier : MP3
   * Taille de fichier maximale : 320 kbit/s
   * Volume : 44,1 kHz

* **[!DNL Pandora]**
   * Durée : 15 ou 30 secondes
   * Type de fichier : MP4 (in-app), MP3 (desktop)
   * Taille de fichier maximale : 2,2 Mo

* **[!DNL SoundCloud]**
   * Durée : 6, 15 ou 30 secondes
   * Type de fichier : MP3
   * Taille de fichier maximale : 5 Mo

* **[!DNL Spotify]**
   * Durée : jusqu’à 30 secondes
   * Type de fichier : OGG
   * Taille de fichier maximale : 500MB
   * Volume : RMS normalisé à -14 ; pic de dBFS normalisé à -0,2 dBFS

* **[!DNL TargetSpot]**
   * Durée : 15, 30 ou 60 secondes
   * Type de fichier : MP3

* **[!DNL TuneIn]**
   * Durée : 10, 15 ou 30 secondes
   * Type de fichier : MP3, OGG
   * Volume : 44,1 kHz

### Conditions requises pour les bannières publicitaires associées (facultatif)

**Tailles prises en charge :** 300x250, 500x500, 640x640, 1 024x1 024

#### Autres exigences de l&#39;éditeur

* **[!DNL iHeartRadio]:**
   * Type de fichier : JPEG, JPG, PNG, GIF, SWF, HTML
   * Taille de fichier maximale : 2,2 Mo
   * Dimensions : 300x250

* **[!DNL Pandora]:**
   * Type de fichier : JPEG, GIF
   * Taille de fichier maximale : Taille : 100 Ko
   * Dimensions : 300 x 250 (mobile ou bureau) ou 500 x 500 (bureau)

* **[!DNL SoundCloud]:**
   * Type de fichier : JPG statique, PNG
   * Taille de fichier maximale : moins de 400 Ko
   * Dimensions : 1 024 x 1 024

* **[!DNL Spotify]:**
   * Type de fichier : JPG statique, PNG
   * Taille de fichier maximale : 200 Ko
   * Dimensions : 300x250

* **[!DNL TuneIn]:**
   * Type de fichier : JPEG, JPG, PNG, GIF, HTML
   * Taille de fichier maximale : 2 Mo
   * Dimensions : 300x250

## Publicités Display Natives

Chaque publicité peut inclure une image fixe ou un GIF en mouvement (cinemagraphe).

### Screens pris en charge

Les publicités sont diffusées par défaut sur les ordinateurs de bureau et les appareils mobiles. Le ciblage de l’appareil est disponible pour ajuster la diffusion.

### Assets requis pour tous les formats natifs dans le flux

#### Ressource Image

**Résolution :** minimum 600 x 600 px ; minimum recommandé de 1 200 x 627 px

**Type de fichier :** JPEG (image d’annonce ou image de couverture de publicité vidéo), GIF (cinémographie)

**Taille du fichier :** moins de 1 Mo (l’image doit être exempte de texte.)

#### Logo de l’annonceur

**Résolution :** minimum 80 x 80 px ; minimum recommandé de 300 x 300 px

**Type de fichier :** JPEG ou PNG.

**Format:** 1x1 rapport

>[!NOTE]
>
>Selon l’image sur laquelle elle sera superposée, choisissez entre des ressources de logo claires ou sombres.

#### Texte/Copie

**Titre :** 200 caractères maximum ; 25 caractères recommandés

**Légende :** 200 caractères au maximum ; 100 caractères recommandés

**Sponsorisé par :** 200 caractères maximum ; 30 caractères recommandés

**Call to action (MoPub uniquement) :** 15 caractères maximum

>[!NOTE]
>
>La disposition finale est définie par l’éditeur au moment de l’exécution. Si une publicité dépasse le nombre de caractères recommandé, certains fournisseurs d’inventaire peuvent ne pas diffuser la publicité, ou l’éditeur ou le fournisseur de services partagés peut tronquer le texte.

#### URL de la page de destination

URL de clic publicitaire avec des dispositifs de suivi des clics facultatifs.

Conditions requises pour les dispositifs de suivi des clics :

* Pixels de suivi d’impression tiers : format d’URL d’image 1x1 uniquement

* Suivi JavaScript de la visibilité : pris en charge pour IAS uniquement ; images 1x1 au format JS.append uniquement

* Pixels de suivi des clics tiers : redirection obligatoire vers la page de destination incorporée dans l’URL (redirection HTTP 302)

* Les dispositifs de suivi des clics de la plateforme de gestion des données (DMP) contenant 200 réponses ou plus ne sont pas pris en charge.

>[!MORELIKETHIS]
>
>* [À propos de la gestion des publicités](ad-about.md)
>* [Créer une publicité unique](ad-create.md)
>* [Créer plusieurs annonces publicitaires tierces](ad-create-multiple.md)
>* [Modifier une publicité](ad-edit.md)
