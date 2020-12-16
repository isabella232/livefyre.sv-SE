---
description: Returnerar ett samlingsobjekt som har instansierats som en granskningstyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-description: Returnerar ett samlingsobjekt som har instansierats som en granskningstyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-title: buildReviewsMetod för samlingswebbplats
solution: Experience Manager
title: buildReviewsMetod för samlingswebbplats
uuid: 88af4c68-57de-4ae9-9394-550c94ede48f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
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

