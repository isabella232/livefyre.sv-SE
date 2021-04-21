---
description: Returnerar ett samlingsobjekt som har instansierats som en granskningstyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
title: buildReviewsMetod för samlingswebbplats
exl-id: 581ad24c-d115-4ffb-93eb-936c2da6e3fa
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# buildReviewsMetod för samlingsplats{#buildreviewscollection-site-method}

Returnerar ett samlingsobjekt som har instansierats som en granskningstyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| title | Sträng | Samlingens titel. |
| articleId | Sträng | Ett unikt artikel-ID som du valde för att identifiera en samling på webbplatsen. |
| url | Sträng | Den kanoniska absoluta URL:en för den här samlingen. |


## Java-exempel {#section_nyl_ycs_rz}

```
Collection collection = site.buildReviewsCollection(title, articleId, url); 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
var collection = site.buildReviewsCollection(title, articleId, url); 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$collection = site->buildReviewsCollection(title, articleId, url); 
```

## Python-exempel {#section_dwg_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```

## Ruby-exempel {#section_enh_gds_rz}

```
collection = site.build_reviews_collection(title, articleId, url) 
```
