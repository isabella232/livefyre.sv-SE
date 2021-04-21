---
description: Returnerar ett Collection-objekt som har instansierats som en chatttyp. Kör create_or_update() från Collection-objektet för att slutföra byggprocessen.
title: buildChatCollection-webbplatsmetod
exl-id: b10f95de-9e6c-4fc3-987b-599717d5a9e7
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '94'
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
