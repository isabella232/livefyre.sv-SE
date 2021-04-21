---
description: Returnerar ett nytt Site-objekt.
title: getSite-nätverksmetod
exl-id: 88782da9-88c6-4e60-9a23-e46d68675d59
translation-type: tm+mt
source-git-commit: a2449482e617939cfda7e367da34875bf187c4c9
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# getSite-nätverksmetod{#getsite-network-method}

Returnerar ett nytt Site-objekt.
|Variabel|Typ|Beskrivning|
|— |— |— |
|siteId|String|Det Livefyre-angivna ID:t för webbplatsen eller programmet som samlingen tillhör. Till exempel: 303617.  |
|siteKey|String|Den hemliga nyckeln för siteId som tillhandahålls av Livefyre.  |

## Java-exempel {#section_nyl_ycs_rz}

```
Site site = network.getSite(siteId, siteKey); 
```

## NodeJS-exempel {#section_xkd_gds_rz}

```
var site = network.getSite(siteId, siteKey); 
```

## PHP-exempel {#section_ghf_gds_rz}

```
$site = $network->getSite(siteId, siteKey);
```

## Python-exempel {#section_dwg_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```

## Ruby-exempel {#section_enh_gds_rz}

```
site = network.get_site(siteId, siteKey) 
```
