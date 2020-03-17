---
description: 'null'
seo-description: 'null'
seo-title: buildCollection-webbplatsmetod
solution: Experience Manager
title: buildCollection-webbplatsmetod
uuid: 52abc42a-9506-4492-b219-f2e05eb79c5f
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

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
