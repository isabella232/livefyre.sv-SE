---
description: Returnerar ett Collection-objekt som har instansierats som en kommentarstyp. Kör createOrUpdate() från samlingsobjektet för att slutföra byggprocessen.
seo-description: Returnerar ett Collection-objekt som har instansierats som en kommentarstyp. Kör createOrUpdate() från samlingsobjektet för att slutföra byggprocessen.
seo-title: buildCommentsCollection, webbplatsmetod
solution: Experience Manager
title: buildCommentsCollection, webbplatsmetod
uuid: 0e5c062e-960d-4ab0-ba32-0965731a1571
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# buildCommentsCollection-webbplatsmetod{#buildcommentscollection-site-method}

Returnerar ett Collection-objekt som har instansierats som en kommentarstyp. Kör createOrUpdate() från samlingsobjektet för att slutföra byggprocessen.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| title | Sträng | Samlingens titel. |
| articleId | Sträng | Ett unikt artikel-ID som du valde för att identifiera en samling på webbplatsen. |
| url | Sträng | Den kanoniska absoluta URL:en för den här samlingen. |

## Java-exempel {#section_nyl_ycs_rz}

```
Collection collection = site.buildCommentsCollection(title, articleId, url);
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
var collection = site.buildCommentsCollection(title, articleId, url); 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$collection = site->buildCommentsCollection(title, articleId, url); 
```

## Python-exempel {#section_dwg_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```

## Ruby-exempel {#section_enh_gds_rz}

```
collection = site.build_comments_collection(title, articleId, url) 
```
