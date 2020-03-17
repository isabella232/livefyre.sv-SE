---
description: Returnerar ett Collection-objekt som har instansierats som en graderingstyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-description: Returnerar ett Collection-objekt som har instansierats som en graderingstyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-title: buildRatingsCollection, webbplatsmetod
title: buildRatingsCollection, webbplatsmetod
uuid: 5eea2ba3-48e1-4cd2-aa73-ea81788af1df
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildRatingsCollection, webbplatsmetod{#buildratingscollection-site-method}

Returnerar ett Collection-objekt som har instansierats som en graderingstyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| title | Sträng | Samlingens titel. |
| articleId | Sträng | Ett unikt artikel-ID som du valde för att identifiera en samling på webbplatsen. |
| url | Sträng | Den kanoniska absoluta URL:en för den här samlingen. |

## Java-exempel {#section_nyl_ycs_rz}

```
Collection collection = site.buildRatingsCollection(title, articleId, url); 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
var collection = site.buildRatingsCollection(title, articleId, url); 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$collection = site->buildRatingsCollection(title, articleId, url); 
```

## Python-exempel {#section_dwg_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```

## Ruby-exempel {#section_enh_gds_rz}

```
collection = site.build_ratings_collection(title, articleId, url) 
```
