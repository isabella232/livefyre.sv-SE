---
description: Returnerar ett Collection-objekt som har instansierats som en Counting-typ. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
title: buildCountingCollection, webbplatsmetod
exl-id: 02186eff-1f2f-41e5-8232-033b646ef224
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# buildCountingCollection-webbplatsmetod{#buildcountingcollection-site-method}

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
