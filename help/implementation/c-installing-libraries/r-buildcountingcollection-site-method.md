---
description: Returnerar ett Collection-objekt som har instansierats som en Counting-typ. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-description: Returnerar ett Collection-objekt som har instansierats som en Counting-typ. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-title: buildCountingCollection, webbplatsmetod
title: buildCountingCollection, webbplatsmetod
uuid: e293d66a-0025-4230-997e-295ce4625713
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# buildCountingCollection, webbplatsmetod{#buildcountingcollection-site-method}

Returnerar ett Collection-objekt som har instansierats som en Counting-typ. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| title | Sträng | Samlingens titel. |
| articleId | Sträng | Ett unikt artikel-ID som du valde för att identifiera en samling på webbplatsen. |
| url | Sträng | Den kanoniska absoluta URL:en för den här samlingen. |

## Java-exempel {#section_nyl_ycs_rz}

```
Collection collection = site.buildCountingCollection(title, articleId, url); 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
var collection = site.buildCountingCollection(title, articleId, url); 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$collection = site->buildCountingCollection(title, articleId, url); 
```

## Python-exempel {#section_dwg_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

## Ruby-exempel {#section_enh_gds_rz}

```
collection = site.build_counting_collection(title, articleId, url) 
```

