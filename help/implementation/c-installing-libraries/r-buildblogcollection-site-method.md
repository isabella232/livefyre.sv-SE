---
description: Returnerar ett Collection-objekt som har instansierats som en bloggtyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-description: Returnerar ett Collection-objekt som har instansierats som en bloggtyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-title: buildBlogCollection, webbplatsmetod
solution: Experience Manager
title: buildBlogCollection, webbplatsmetod
uuid: 6a5ec6b9-bc32-467a-abe6-a57c6defe067
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# buildBlogCollection-webbplatsmetod{#buildblogcollection-site-method}

Returnerar ett Collection-objekt som har instansierats som en bloggtyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| title | Sträng | Samlingens titel. |
| articleId | Sträng | Ett unikt artikel-ID som du valde för att identifiera en samling på webbplatsen. |
| url | Sträng | Den kanoniska absoluta URL:en för den här samlingen. |

## Java-exempel {#section_nyl_ycs_rz}

```
Collection collection = site.buildBlogCollection(title, articleId, url); 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
var collection = site.buildBlogCollection(title, articleId, url); 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$collection = site->buildBlogCollection(title, articleId, url); 
```

## Python-exempel {#section_dwg_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

## Ruby-exempel {#section_enh_gds_rz}

```
collection = site.build_blog_collection(title, articleId, url) 
```

