---
title: buildCollection-webbplatsmetod
description: buildCollection-webbplatsmetod
exl-id: d5c9a2fb-2d30-44f4-8ebf-24b0ec7babee
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# buildCollection-webbplatsmetod{#buildcollection-site-method}

| Variabel | Typ | Beskrivning |
|--- |--- |--- |
| type | CollectionType | Samlingens typ. |
| title | Sträng | Samlingens titel. |
| articleId | Sträng | Ett unikt artikel-ID som du valde för att identifiera en samling på webbplatsen. |
| url | Sträng | Den kanoniska absoluta URL:en för den här samlingen. |

## Java-exempel {#section_nyl_ycs_rz}

```
Collection collection = site.buildCollection(type, title, articleId, url); 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
var collection = site.buildCollection(type, title, articleId, url); 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$collection = site->buildCollection(type, title, articleId, url); 
```

## Python-exempel {#section_dwg_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```

## Ruby-exempel {#section_enh_gds_rz}

```
collection = site.build_collection(type, title, articleId, url) 
```
