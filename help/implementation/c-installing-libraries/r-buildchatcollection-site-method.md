---
description: Returnerar ett Collection-objekt som har instansierats som en chatttyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-description: Returnerar ett Collection-objekt som har instansierats som en chatttyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
seo-title: buildChatCollection-webbplatsmetod
solution: Experience Manager
title: buildChatCollection-webbplatsmetod
uuid: 39ee32d0-29c9-47a8-a458-a3cf7a96db30
translation-type: tm+mt
source-git-commit: 2908c6988c706a49c391f0e607bb641bce3a7f0d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# buildChatCollection-webbplatsmetod{#buildchatcollection-site-method}

Returnerar ett Collection-objekt som har instansierats som en chatttyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| title | Sträng | Samlingens titel. |
| articleId | Sträng | Ett unikt artikel-ID som du valde för att identifiera en samling på webbplatsen. |
| url | Sträng | Den kanoniska absoluta URL:en för den här samlingen. |

## Java-exempel {#section_nyl_ycs_rz}

```
Collection collection = site.buildChatCollection(title, articleId, url); 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
var collection = site.buildChatCollection(title, articleId, url); 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$collection = site->buildChatCollection(title, articleId, url); 
```

## Python-exempel {#section_dwg_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url) 
```

## Ruby-exempel {#section_enh_gds_rz}

```
collection = site.build_chat_collection(title, articleId, url)
```
