---
description: Returnerar ett nytt Site-objekt.
seo-description: Returnerar ett nytt Site-objekt.
seo-title: getSite-nätverksmetod
solution: Experience Manager
title: getSite-nätverksmetod
uuid: 67de781e-5240-4be5-9e93-c614828e0bb5
translation-type: tm+mt
source-git-commit: 67aeb3de964473b326c88c3a3f81ff48a6a12652

---


# getSite-nätverksmetod{#getsite-network-method}

Returnerar ett nytt Site-objekt.
|Variabel|Typ|Beskrivning||—|—|—||siteId|String|Det Livefyre-angivna ID:t för webbplatsen eller programmet som samlingen tillhör. Till exempel: 303617.  ||siteKey|String|Den hemliga nyckeln för siteId som tillhandahålls av Livefyre.  |

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

